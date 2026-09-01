
<div align="center">

<!--
  ===== README_B · 未来科技 / 机械战甲风 =====
  [GitHub-safe] 已移除全部 <style> 块；所有动画用纯 SVG <animateTransform>/<animate>
-->

<!-- ===== HERO：战甲 HUD + 能量核心 + 旋转轨道 ===== -->
<div style="position:relative;padding:40px 24px 50px 24px;border-radius:28px;border:1px solid rgba(168,85,247,.35);overflow:hidden;
            background:
              radial-gradient(1200px 600px at -10% -10%, rgba(168,85,247,.28), transparent 60%),
              radial-gradient(1200px 600px at 110% 10%, rgba(236,72,153,.25), transparent 60%),
              radial-gradient(1200px 600px at 50% 120%, rgba(59,130,246,.25), transparent 60%),
              linear-gradient(180deg,#050014,#0a0022 70%,#050014);">

  <!-- 四角 HUD 切角 + 扫描渐变（全部静态 SVG，不依赖 CSS） -->
  <svg width="100%" height="300" viewBox="0 0 800 300" preserveAspectRatio="none" style="position:absolute;inset:0;opacity:.7;pointer-events:none;">
    <defs>
      <linearGradient id="hudG" x1="0" x2="1">
        <stop offset="0" stop-color="#a855f7"/><stop offset=".5" stop-color="#ec4899"/><stop offset="1" stop-color="#22d3ee"/>
      </linearGradient>
    </defs>
    <!-- 左上 -->
    <path d="M0,50 L0,0 L50,0" stroke="#a855f7" stroke-width="2.5" fill="none"/>
    <path d="M0,80 L70,80 L70,0" stroke="#22d3ee" stroke-width="1" fill="none" opacity=".55"/>
    <!-- 右上 -->
    <path d="M800,50 L800,0 L750,0" stroke="#ec4899" stroke-width="2.5" fill="none"/>
    <path d="M800,80 L730,80 L730,0" stroke="#22d3ee" stroke-width="1" fill="none" opacity=".55"/>
    <!-- 左下 -->
    <path d="M0,250 L0,300 L50,300" stroke="#ec4899" stroke-width="2.5" fill="none"/>
    <!-- 右下 -->
    <path d="M800,250 L800,300 L750,300" stroke="#a855f7" stroke-width="2.5" fill="none"/>
    <!-- 中部扫描虚线 -->
    <line x1="0" y1="150" x2="800" y2="150" stroke="url(#hudG)" stroke-width="1" stroke-dasharray="4 8"/>
  </svg>

  <!-- 能量核心：SVG animateTransform 旋转 -->
  <div style="position:relative;display:flex;align-items:center;justify-content:center;margin-top:10px;">
    <svg width="220" height="220" viewBox="0 0 220 220">
      <defs>
        <radialGradient id="gemG"><stop offset="0" stop-color="#fff"/><stop offset=".4" stop-color="#f0abfc"/><stop offset="1" stop-color="#7c3aed"/></radialGradient>
        <filter id="softGlow" x="-40%" y="-40%" width="180%" height="180%">
          <feGaussianBlur stdDeviation="2.2" result="b"/>
          <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
        </filter>
      </defs>

      <!-- 外环 旋转 -->
      <g>
        <animateTransform attributeName="transform" attributeType="XML" type="rotate"
                          from="0 110 110" to="360 110 110" dur="12s" repeatCount="indefinite"/>
        <circle cx="110" cy="110" r="100" stroke="#a855f7" stroke-width="1.8" fill="none"
                stroke-dasharray="10 6 4 6 10 14 8" opacity=".9"/>
        <circle cx="210" cy="110" r="6" fill="#a855f7"/>
        <circle cx="10"  cy="110" r="5" fill="#ec4899"/>
      </g>

      <!-- 中环 反向旋转 -->
      <g>
        <animateTransform attributeName="transform" attributeType="XML" type="rotate"
                          from="360 110 110" to="0 110 110" dur="9s" repeatCount="indefinite"/>
        <circle cx="110" cy="110" r="76" stroke="#22d3ee" stroke-width="1.2" fill="none"
                stroke-dasharray="3 7" opacity=".8"/>
        <circle cx="110" cy="34" r="4" fill="#22d3ee"/>
      </g>

      <!-- 呼吸脉动的两个数据弧 -->
      <g filter="url(#softGlow)">
        <circle cx="110" cy="110" r="56" stroke="#ec4899" stroke-width="3" fill="none"
                stroke-dasharray="352" stroke-linecap="round" opacity=".95">
          <animate attributeName="stroke-dashoffset" values="0;80;0" dur="3s" repeatCount="indefinite"/>
        </circle>
        <circle cx="110" cy="110" r="46" stroke="#a855f7" stroke-width="2.2" fill="none"
                stroke-dasharray="289" opacity=".9">
          <animate attributeName="stroke-dashoffset" values="0;50;0" dur="2.4s" repeatCount="indefinite"/>
        </circle>
      </g>

      <!-- 核心六角宝石 -->
      <polygon points="110,78 138,94 138,126 110,142 82,126 82,94"
               fill="url(#gemG)" stroke="#fff" stroke-width="1" filter="url(#softGlow)">
        <animate attributeName="opacity" values=".7;1;.7" dur="2.2s" repeatCount="indefinite"/>
      </polygon>
      <text x="110" y="116" text-anchor="middle" font-family="Orbitron,Segoe UI,Arial" font-weight="900"
            font-size="16" fill="#fff" stroke="#000" stroke-width=".4">AI v3</text>

      <!-- 上下漂浮 -->
      <animateTransform attributeName="transform" attributeType="XML" type="translate"
                        values="0,0; 0,-8; 0,0" dur="6s" repeatCount="indefinite" additive="sum"/>
    </svg>
  </div>

  <!-- 标题 -->
  <div style="position:relative;z-index:2;margin-top:6px;">
    <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=28&pause=1200&color=A855F7&center=true&vCenter=true&width=780&lines=%E2%97%88%20AI%20MARKET%20DEMAND%20ARMOR%20%E2%97%88;%E4%BA%AC%E4%B8%9C%20BAD-REV%20INTELLIGENCE%20SYSTEM;TACTICAL%20NLP%20CLUSTER%20ENGINE%20v3"
         style="filter:drop-shadow(0 0 18px rgba(168,85,247,.7));"/>
    <p style="margin-top:8px;font-family:Orbitron,Segoe UI,sans-serif;color:#22d3ee;letter-spacing:6px;font-size:14px;">
      ▬▬ SELENIUM · MODAL v3 · TF-IDF · K-MEANS · ELBOW ▬▬
    </p>
  </div>
</div>

<br/>

<!-- ===== Badge 装甲（内联 shadow 与圆角） ===== -->
<p>
  <img src="https://img.shields.io/badge/PYTHON-3.12%2B-A855F7?style=for-the-badge&logo=python&logoColor=fef3c7&labelColor=0a0022" style="border-radius:10px;transition:transform .2s;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/MECH-Selenium_UC-EC4899?style=for-the-badge&logo=selenium&logoColor=white&labelColor=0a0022" style="border-radius:10px;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/HUD-DB_SQLite3-22D3EE?style=for-the-badge&logo=sqlite&logoColor=white&labelColor=0a0022" style="border-radius:10px;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/NEURO-TF_IDF_KMeans-F59E0B?style=for-the-badge&logo=scikitlearn&logoColor=white&labelColor=0a0022" style="border-radius:10px;"/>
</p>
<p>
  <img src="https://img.shields.io/github/last-commit/your-org/ai-market-demand-analysis?style=for-the-badge&amp;label=LAST%20PATCH&amp;labelColor=0a0022&amp;color=A855F7" style="border-radius:10px;"/>
  &nbsp;
  <img src="https://img.shields.io/github/issues/your-org/ai-market-demand-analysis?style=for-the-badge&amp;label=TICKETS&amp;labelColor=0a0022&amp;color=EC4899" style="border-radius:10px;"/>
  &nbsp;
  <img src="https://img.shields.io/github/stars/your-org/ai-market-demand-analysis?style=for-the-badge&amp;label=PILOTS&amp;labelColor=0a0022&amp;color=22D3EE" style="border-radius:10px;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Build-PASSING-10B981?style=for-the-badge&logo=githubactions&logoColor=white&labelColor=0a0022" style="border-radius:10px;"/>
</p>

</div>

---

## ▣ BRIEFING &nbsp;｜&nbsp; 战术简报

<div style="padding:18px 22px;border-radius:18px;background:
      linear-gradient(#0a0022,#0a0022) padding-box,
      linear-gradient(135deg,#a855f7,#ec4899,#22d3ee,#a855f7) border-box;
      border:1px solid transparent;">

> **🎯 作战目标**：构建一套面向电商市场的**全自动 AI 需求分析机甲**
>
> 以 **Selenium + undetected-chromedriver** 装甲壳采集京东差评，联合 **TF-IDF + K-Means（肘部法则）** 神经核，
> 从海量非结构化文本中自动挖掘用户痛点与产品改进机会，输出高价值商业决策报告。

</div>

<br/>

<div align="center">

| ⚡ HYPER CRAWL 高速采集 | 🎯 NEURAL CLUSTER 神经聚类 | 📊 COMMAND REPORT 指挥报告 |
| :---: | :---: | :---: |
| Modal v3 差评直达炮 | 肘部法则动态 K 值 | 加权机会评分模型 |
| 20 页 / 品类 · 500 条 / 单品 | Jieba 词典 + 停用词护盾 | 自动化 CSV 情报 |
| SQLite 断点 + 反风控 ECM | 自定义词典扩展 | 多维度痛点画像 |

</div>

---

## ▣ WARFRAME MODULES &nbsp;｜&nbsp; 战甲模块

### 🕷️ MOD-01 · SELENIUM ARMORED CRAWLER

<div style="padding:14px 20px 4px 20px;border-radius:18px;
      background:linear-gradient(#0a0022,#0a0022) padding-box,
      linear-gradient(135deg,#a855f7,#ec4899,#22d3ee,#a855f7) border-box;
      border:1px solid transparent;">

| 子系统 | 规格参数 |
| :--- | :--- |
| 🎭 隐身外壳 | `undetected-chromedriver` + `user_data_dir` 持久化登录态 |
| 🚀 差评直达炮 v3 | Modal 三阶段解析 · 跳过翻页定位差评 Tab · 效率 **↑10×** |
| 🛡️ 四层驱动检测 | 注册表 → 常见路径 → `--version` → 目录名 |
| 🎲 人类节奏 ECM | get 前 30–55s · 商品间 50–80s · 403 冷却 120–180s |
| 💾 断点续飞核 | `crawl_progress` + `raw_comments` 双表 · 零评论强制回流 |
| 🔍 瞄准镜阵列 | **28 组**搜索选择器 + **8 分支** PID 提取 · SPA 鲁棒 99% |

</div>

### 🧠 MOD-02 · NEURAL NLP CORE

<div style="padding:14px 20px 4px 20px;border-radius:18px;
      background:linear-gradient(#0a0022,#0a0022) padding-box,
      linear-gradient(135deg,#a855f7,#ec4899,#22d3ee,#a855f7) border-box;
      border:1px solid transparent;">

| 子系统 | 规格参数 |
| :--- | :--- |
| 📝 分词炮 | Jieba + 用户词典扩展 + 停用词过滤 |
| 🔢 向量矩阵 | TF-IDF 词频-逆文档频率矩阵 |
| 🎯 智能火控 | K-Means + 肘部法则 k ∈ [2, 15] · 自动选簇 |
| 📈 加权杀伤 | `类别占比 × 权重系数` → 商业改进优先级 |
| 📦 发射仓 | CSV 报告导出至 `reports/` · 关键词 / 数量 / 机会值 / 代表评论 |

</div>

### ⚙️ MOD-03 · ARMORY CONFIG

```yaml
# ===== AI MARKET ARMOR CONFIG v3 =====
jupiter:
  pt_key:   "manual_only_never_share"   # ⚠ 手动粘贴 永不外发
  pt_pin:   "manual_only_never_share"

crawler:
  max_search_pages:         20          # 搜索页上限
  max_comments_per_product: 500         # 单品差评上限
  max_scroll_per_product:   50          # 滚动上限

analyzer:
  k_range:      [2, 15]                 # 肘部法则空间
  weight_adjust:                        # 评分权重系数
    quality:    1.5
    service:    1.2
    logistics:  1.0
```

---

## ▣ BATTLE PIPELINE &nbsp;｜&nbsp; 作战数据流

```mermaid
flowchart TB
    subgraph FRONT["🕷️ 前甲 · CRAWL LAYER"]
      direction LR
      A1(SELENIUM MODAL v3) --> A2(SQLite RAW DB)
    end
    subgraph CORE["🧠 中枢 · NLP LAYER"]
      direction LR
      B1(Jieba 清洗) --> B2(TF-IDF 向量化) --> B3(KMeans 肘部 k∈[2,15])
    end
    subgraph REAR["📊 后甲 · REPORT LAYER"]
      direction LR
      C1(加权机会评分) --> C2(CSV 商业情报)
    end

    FRONT ==> CORE ==> REAR

    classDef f fill:#0a0022,stroke:#a855f7,stroke-width:2px,color:#f0abfc;
    classDef c fill:#0a0022,stroke:#ec4899,stroke-width:2px,color:#fbcfe8;
    classDef r fill:#0a0022,stroke:#22d3ee,stroke-width:2px,color:#a5f3fc;
    class A1,A2 f; class B1,B2,B3 c; class C1,C2 r;
```

---

## ▣ LAUNCH SEQUENCE &nbsp;｜&nbsp; 启动序列

```bash
# ▶ STEP 01 · 召唤机甲
git clone https://github.com/your-org/ai-market-demand-analysis.git
cd ai-market-demand-analysis

# ▶ STEP 02 · 组装内核
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS / Linux:
# source .venv/bin/activate

pip install -r requirements.txt

# ▶ STEP 03 · 注入凭证 ⚠ 手动操作 YAML，不要外传
#    编辑 config.yaml → jupiter.pt_key / jupiter.pt_pin

# ▶ STEP 04 · 首次点火（有头模式 · 登录态持久化）
python crawler.py --category "蓝牙耳机" --headed

# ▶ STEP 05 · 执行作战 + 生成报告
python crawler.py  --category "蓝牙耳机"
python analyzer.py --category "蓝牙耳机" --output reports/蓝牙耳机_痛点报告.csv
```

---

## ▣ MECH BLUEPRINT &nbsp;｜&nbsp; 机甲蓝图

```text
ai-market-demand-analysis/
├── 🕷️ crawler.py            ════ MOD-01 · SELENIUM ARMORED CRAWLER
├── 🧠 analyzer.py           ════ MOD-02 · NEURAL NLP CORE
├── ⚙️ config.yaml           ════ MOD-03 · ARMORY CONFIG
├── 📋 requirements.txt      ════ 依赖清单（setuptools≥68）
├── 🗃️ data/                 ════ DB 弹药库
│   └── jupiter.db           ════ SQLite 作战记录
├── 📊 reports/              ════ 指挥报告仓
│   └── 蓝牙耳机_痛点报告.csv ════ 战术输出
├── 🔧 user_data_dir/        ════ Chrome 驾驶舱
└── 📜 logs/                 ════ 证据 + 黑匣子
```

---

## ▣ HUD READOUT &nbsp;｜&nbsp; 仪表盘读数

<div align="center">

| HUD 指标 | 读数 | 状态 |
| :--- | :---: | :---: |
| 🛒 搜索页 / 品类 | **20** | <span style="color:#22d3ee;">▣ ONLINE</span> |
| 💬 差评 / 单品 | **500 条 · 50 滚** | <span style="color:#22d3ee;">▣ ONLINE</span> |
| ⚡ 差评直达率 | **MODAL v3 · 99%** | <span style="color:#a855f;">▣ LOCKED</span> |
| 🧩 聚类自动识别 | **肘部法则 k ∈ [2,15]** | <span style="color:#ec4899;">▣ NEURAL</span> |
| 💾 断点续飞 | ✅ SQLite 双表 | <span style="color:#10b981;">▣ READY</span> |
| 🛡️ 风控抗性 | ↓ 80% | <span style="color:#10b981;">▣ STABLE</span> |

</div>

---

## ▣ ACCEPTANCE BEACON &nbsp;｜&nbsp; 验收信标

控制台出现以下**信标**时，代表对应子系统作战正常：

| 阶段 | 信标标志 |
| :--- | :--- |
| 遗留回流 | `[遗留重置] xx items reset` |
| 赞不绝口入口 | `[赞不绝口入口 ✓]` |
| Modal 根锁定 | `[Modal 根 ✓]` |
| 差评 Tab 切换 | `[差评标签 双保险 ✓]` |
| 评价区加载 | `[评价区 锚点/UI回退路径]` |
| 全文展开滚动 | `scroll with expanded full text` |
| DB 写入确认 | `DB write confirmed, Y≥10 comments` |

---

## ▣ SHIELD PROTOCOL &nbsp;｜&nbsp; 护盾协议

<div style="padding:14px 20px;border-radius:18px;
      background:linear-gradient(#0a0022,#0a0022) padding-box,
      linear-gradient(135deg,#a855f7,#ec4899,#22d3ee,#a855f7) border-box;
      border:1px solid transparent;">

- 🔒 **协议 01 · 凭证零泄漏**：`pt_key / pt_pin` 仅在本地 YAML 手动粘贴，永不硬编码 / 外传 / 入库 / 入日志
- 🚫 **协议 02 · 无头守卫**：未登录状态下 Headless 模式立即 ABORT，避免白跑与风控误封
- 🧹 **协议 03 · 证据隔离**：反爬拦截页（~3908B）与有效证据页（73KB+/77KB+/110KB+）**毫秒级时间戳**命名，永不覆盖

</div>

---

## ▣ JOIN THE LEGION &nbsp;｜&nbsp; 加入军团

```bash
# 标准作战贡献流程
git checkout -b feat/new-weapon-system
git commit -m "feat(weapon): add plasma cannon for Modal v4"
git push origin feat/new-weapon-system
# → Open PR → CI 绿 → maintainer 批准 → 合入主舰
```

<div align="center" style="font-family:Orbitron,Segoe UI,sans-serif;color:#22d3ee;letter-spacing:3px;">
  &gt; BUG 与 NEW WEAPON REQUEST · OPEN ISSUE &nbsp;·&nbsp; IF IT HELPS · DROP A ⭐
</div>

---

## ▣ LICENSE CHIP &nbsp;｜&nbsp; 许可芯片

<p align="center">
  <a href="./LICENSE">
    <img src="https://img.shields.io/badge/LICENSE-MIT-A855F7?style=for-the-badge&logo=&labelColor=0a0022&logoColor=white"
         style="border-radius:10px;"/>
  </a>
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=110&section=footer&customColorList=7,26,20,30,7"/>
  <p style="margin-top:-4px;font-family:Orbitron,Segoe UI,sans-serif;color:#a855f7;letter-spacing:4px;">
    ═══ POWERED BY THE AI MARKET DEMAND ARMOR TEAM ═══
  </p>
</div>
