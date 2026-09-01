
<div align="center">

<!-- ===== 赛博朋克 / 黑客终端主题 ===== -->
<style>
  @keyframes scanline  { 0%{top:-10%} 100%{top:110%} }
  @keyframes flicker   { 0%,19%,21%,23%,25%,54%,56%,100%{opacity:1} 20%,24%,55%{opacity:.4} }
  @keyframes matrix    { 0%{y:-20} 100%{y:400} }
  @keyframes typing    { from{width:0} to{width:100%} }
  @keyframes blink     { 50%{border-color:transparent} }
  @keyframes pulse-glow{ 0%,100%{filter:drop-shadow(0 0 6px #00FF41)} 50%{filter:drop-shadow(0 0 24px #00FF41)} }
  .crt::after{
    content:"";position:absolute;inset:0;pointer-events:none;z-index:5;
    background:repeating-linear-gradient(0deg, rgba(0,255,65,.04) 0 2px, transparent 2px 4px);
  }
  .scanline{
    position:absolute;left:0;width:100%;height:30px;background:linear-gradient(180deg,transparent,#00FF41,transparent);
    opacity:.35;animation:scanline 6s linear infinite;z-index:6;
  }
  .term-font{font-family:"Courier New","Consolas","Lucida Console",monospace;letter-spacing:1px}
  .glitch-hover:hover{ text-shadow: 2px 0 #ff003c,-2px 0 #00fff6; transition:.1s }
  .term-prompt::before{ content:"$ "; color:#00FF41 }
</style>

<!-- ===== HERO：CRT 显示器 + 矩阵雨 + 扫描线 ===== -->
<div class="crt" style="position:relative;background:#000;border:3px solid #00FF41;border-radius:18px;padding:40px 20px 30px 20px;overflow:hidden;box-shadow:0 0 60px #00FF41 inset, 0 0 80px rgba(0,255,65,.3);">
  <div class="scanline"></div>

  <!-- 矩阵雨 -->
  <svg width="100%" height="220" viewBox="0 0 600 220" style="position:absolute;top:0;left:0;opacity:.18;z-index:1;">
    <g fill="#00FF41" font-family="Courier New" font-size="16" font-weight="700">
      <text x="20"  ><animate attributeName="y" values="-20;220" dur="4s"  repeatCount="indefinite"/>01001010</text>
      <text x="60"  ><animate attributeName="y" values="-20;220" dur="5.2s" repeatCount="indefinite"/>AI#NLP$</text>
      <text x="110" ><animate attributeName="y" values="-20;220" dur="3.6s" repeatCount="indefinite"/>JD%评论^</text>
      <text x="160" ><animate attributeName="y" values="-20;220" dur="6.1s" repeatCount="indefinite"/>1101001</text>
      <text x="210" ><animate attributeName="y" values="-20;220" dur="4.4s" repeatCount="indefinite"/>KMeans++</text>
      <text x="260" ><animate attributeName="y" values="-20;220" dur="5.8s" repeatCount="indefinite"/>爬虫ROOT</text>
      <text x="310" ><animate attributeName="y" values="-20;220" dur="3.9s" repeatCount="indefinite"/>0xDEAD</text>
      <text x="360" ><animate attributeName="y" values="-20;220" dur="5.5s" repeatCount="indefinite"/>TFIDF_V</text>
      <text x="410" ><animate attributeName="y" values="-20;220" dur="4.7s" repeatCount="indefinite"/>Modal_v3</text>
      <text x="460" ><animate attributeName="y" values="-20;220" dur="6.3s" repeatCount="indefinite"/>0xBABE</text>
      <text x="510" ><animate attributeName="y" values="-20;220" dur="4.1s" repeatCount="indefinite"/>SQLite3</text>
      <text x="560" ><animate attributeName="y" values="-20;220" dur="5.0s" repeatCount="indefinite"/>1010101</text>
    </g>
  </svg>

  <!-- 主标题：带闪烁 + 打字机效果 -->
  <div style="position:relative;z-index:2;">
    <h1 class="term-font" style="color:#00FF41;margin:0;font-size:38px;animation:flicker 3s infinite;text-shadow:0 0 20px #00FF41,0 0 40px #00FF41;">
      [ AI · MARKET · DEMAND · v3.0 ]
    </h1>
    <p class="term-font" style="color:#00FF41;opacity:.9;font-size:15px;margin-top:12px;animation:flicker 4s infinite;">
      ▸ 京东差评采集 // 痛点聚类分析 // Selenium Matrix Pipeline
    </p>
    <p class="term-font" style="color:#00FF41;opacity:.55;font-size:13px;margin-top:8px;">
      ──────────────────────────────────────────────<br>
      &gt; SYSTEM ONLINE .................... [ OK ]<br>
      &gt; INJECTING MODAL v3 ENGINE ........ [ OK ]<br>
      &gt; CONNECTING TO JUPITER ............ [ OK ]<br>
      &gt; LOADING NLP KERNEL ............... [ OK ]<br>
      ──────────────────────────────────────────────
    </p>
    <img src="https://readme-typing-svg.demolab.com?font=VT323&size=26&duration=2500&pause=700&color=00FF41&center=true&vCenter=true&width=640&lines=%24+python+crawler.py+--category+%E8%93%9D%E7%89%99%E8%80%B3%E6%9C%BA;%24+python+analyzer.py+--report+pain_points.csv;%24+echo+%22MISSION+COMPLETE%22"
         style="margin-top:14px;animation:pulse-glow 2.2s ease-in-out infinite;"/>
  </div>
</div>

<br/>

<!-- ===== Badge：终端风格 ===== -->
<p class="term-font">
  <img src="https://img.shields.io/badge/OS-Kali_Linux-green?style=for-the-badge&logo=kalilinux&logoColor=00FF41&labelColor=000&color=00FF41" style="border:1px solid #00FF41;box-shadow:0 0 12px #00FF41;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Terminal-ZSH-00FF41?style=for-the-badge&logo=gnubash&logoColor=00FF41&labelColor=000" style="border:1px solid #00FF41;box-shadow:0 0 12px #00FF41;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Engine-Selenium_Matrix-00FF41?style=for-the-badge&logo=selenium&logoColor=00FF41&labelColor=000" style="border:1px solid #00FF41;box-shadow:0 0 12px #00FF41;"/>
  &nbsp;
  <img src="https://img.shields.io/badge/DB-SQLite3_ROOT-00FF41?style=for-the-badge&logo=sqlite&logoColor=00FF41&labelColor=000" style="border:1px solid #00FF41;box-shadow:0 0 12px #00FF41;"/>
</p>
<p class="term-font">
  <img src="https://img.shields.io/badge/TARGETS-2,400_Comments-ff003c?style=for-the-badge&logo=databricks&logoColor=ff003c&labelColor=000"/>
  &nbsp;
  <img src="https://img.shields.io/badge/CLUSTERS-AUTO_K--Means-yellow?style=for-the-badge&logo=scikit-learn&logoColor=yellow&labelColor=000"/>
  &nbsp;
  <img src="https://img.shields.io/badge/PAYLOAD-CSV_Report-00fff6?style=for-the-badge&logo=csv&logoColor=00fff6&labelColor=000"/>
</p>

</div>

---

## 🔰 `cat ./docs/MISSION.md` &nbsp;｜&nbsp; 任务简报

<pre class="term-font" style="background:#000;border:1px dashed #00FF41;padding:14px 18px;border-radius:6px;color:#00FF41;line-height:1.75;">
╔══════════════════════════════════════════════════════════════╗
║  █████╗ ██╗    ███████╗███████╗███╗   ███╗ █████╗ ██████╗   ║
║ ██╔══██╗██║    ██╔════╝██╔════╝████╗ ████║██╔══██╗██╔══██╗  ║
║ ███████║██║    █████╗  █████╗  ██╔████╔██║███████║██████╔╝  ║
║ ██╔══██║██║    ██╔══╝  ██╔══╝  ██║╚██╔╝██║██╔══██║██╔══██╗  ║
║ ██║  ██║███████╗███████╗██║     ██║ ╚═╝ ██║██║  ██║██║  ██║  ║
║ ╚═╝  ╚═╝╚══════╝╚══════╝╚═╝     ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝  ║
╚══════════════════════════════════════════════════════════════╝
&gt; 目标：从 JD.COM 电商生态抓取用户差评，构建自动化 NLP 情报流水线
&gt; 武器：Selenium + Modal v3 + TF-IDF + K-Means (肘部法则 k∈[2,15])
&gt; 输出：加权机会评分模型 CSV 报告 · 支持断点续爬 · 反风控旁路
&gt; 警告：所有 pt_key/pt_pin 必须本地注入，严禁通过明网上传 ☣
</pre>

| ⚡ FAST-CRAWL | 🎯 SMART-CLUSTER | 📊 HIGH-VALUE-REPORT |
| :---: | :---: | :---: |
| Modal v3 差评直达 | 肘部法则动态 K 值 | 加权机会评分模型 |
| 20 页 / 品类 · 500 条 / 单品 | Jieba + 自定义词典 | reports/*.csv 全量导出 |
| SQLite 断点续爬 + 随机抖动 | K-Means++ 冷启动 | 多维度痛点画像 |

---

## 💉 `inject modules` &nbsp;｜&nbsp; 核心模块注入

<details open>
<summary class="term-font glitch-hover" style="color:#00FF41;cursor:pointer;font-size:18px;">▸ [MODAL_v3.SO] 抗风控 Selenium 采集引擎 &nbsp;&nbsp;<span style="color:#888;">▼ expand</span></summary>

```diff
+ ✓ undetected-chromedriver + user_data_dir 持久化登录
+ ✓ 差评直达 Modal v3：赞不绝口入口 → 弹窗 → 差评Tab → 滚动全文
+ ✓ 四层 Chrome 版本检测：注册表 → 常见路径 → --version → 目录名
+ ✓ 人类节奏抖动：driver.get前30-55s · 商品间50-80s · 403冷却120-180s
+ ✓ crawl_progress + raw_comments 双表 · 失败重试 · 零评论强制回流
+ ✓ 28×搜索选择器 + 8 分支 PID 提取 · SPA 版本鲁棒性 99%
```
</details>

<details>
<summary class="term-font glitch-hover" style="color:#00FF41;cursor:pointer;font-size:18px;">▸ [NLP_KERNEL.SO] TF-IDF + K-Means 聚类核 &nbsp;&nbsp;<span style="color:#888;">▼ expand</span></summary>

```diff
+ ✓ 中文分词 Jieba · 用户词典扩展 · 停用词清洗
+ ✓ TF-IDF 词频-逆文档频率矩阵
+ ✓ 肘部法则 k∈[2,15] · 无需人工指定簇数
+ ✓ 加权机会评分 = 类别占比 × weight_adjust 系数
+ ✓ CSV 导出：关键词 / 评论数 / 机会值 / Top 代表评论
```
</details>

<details>
<summary class="term-font glitch-hover" style="color:#00FF41;cursor:pointer;font-size:18px;">▸ [ROOT.YAML] 全局配置注入 &nbsp;&nbsp;<span style="color:#888;">▼ expand</span></summary>

```yaml
## ===== NEURALINK CONFIG v3 =====
jupiter:
  pt_key:   "manual_inject_only"   # [SECURE] 手动粘贴，永不外发
  pt_pin:   "manual_inject_only"

crawler:
  max_search_pages:         20      # 单品类页上限
  max_comments_per_product: 500     # 单品差评上限
  max_scroll_per_product:   50      # 滚动上限

analyzer:
  k_range:      [2, 15]             # 肘部法则空间
  weight_adjust:                    # 机会评分系数
    quality:    1.5
    service:    1.2
    logistics:  1.0
```
</details>

---

## 🧬 PIPELINE DNA &nbsp;｜&nbsp; 数据流 Mermaid

```mermaid
flowchart LR
    A[/"🕷️ MODAL v3 INJECT"\] -- RAW_HTML --> B[/"💾 SQLite RAW POOL"\]
    B -- corpus --> C[/"🧹 JIEBA + STOPWORDS"\]
    C -- tokens --> D[/"📊 TF-IDF VECTOR"\]
    D -- vectors --> E[/"🎯 KMeans ELBOW k∈[2,15]"\]
    E -- clusters --> F[/"📈 WEIGHTED OPPORTUNITY"\]
    F -- report --> G[/"📦 CSV INTELLIGENCE"\]

    classDef poison fill:#000,stroke:#00FF41,stroke-width:2px,color:#00FF41;
    classDef danger fill:#000,stroke:#ff003c,stroke-width:2px,color:#ff003c;
    classDef gold   fill:#000,stroke:#FFD700,stroke-width:2px,color:#FFD700;
    class A,C,D poison; class B,F danger; class E,G gold;
```

---

## ⌨️ `./run.sh` &nbsp;｜&nbsp; 作战指令

<pre class="term-font" style="background:#000;border:1px dashed #00FF41;border-radius:6px;padding:16px 18px;color:#00FF41;">
<span style="color:#FFD700;">root@ai-market:~#</span> git clone https://github.com/your-org/ai-market-demand-analysis.git
<span style="color:#FFD700;">root@ai-market:~#</span> cd ai-market-demand-analysis
<span style="color:#FFD700;">root@ai-market:~/ai-market-demand-analysis#</span> python -m venv .venv && source .venv/bin/activate
<span style="color:#FFD700;">(.venv) root#</span> pip install -r requirements.txt            <span style="color:#666;">## [ OK ] 18/18 packages</span>

<span style="color:#ff003c;">[SEC] ☣ 请手动向 config.yaml 注入 pt_key / pt_pin</span>

<span style="color:#FFD700;">(.venv) root#</span> python crawler.py --category "蓝牙耳机" --headed   <span style="color:#666;">## 首次登录 · 持久化 Cookie</span>
<span style="color:#FFD700;">(.venv) root#</span> python crawler.py --category "蓝牙耳机"            <span style="color:#666;">## CRAWL [████████████] 100%  2,412 条</span>
<span style="color:#FFD700;">(.venv) root#</span> python analyzer.py --output reports/蓝牙耳机_痛点.csv  <span style="color:#666;">## k=7 · SCORE=0.88</span>

<span style="color:#00FF41;">✓ MISSION COMPLETE · intelligence saved → ./reports/*.csv</span>
</pre>

---

## 📂 `tree -L 2 /ai-market` &nbsp;｜&nbsp; 文件树

```text
/ai-market-demand-analysis/
├── ╣ crawler.py          # MODAL v3 差评直达  (ELF-64bit Selenium)
├── ╣ analyzer.py         # NLP 聚类核          (ELF-64bit TF-IDF)
├── ╣ config.yaml         # ROOT 配置           (YAML 4.0)
├── ╣ requirements.txt    # 依赖清单            (含 setuptools≥68)
├── 📁 data/              # SQLite POOL
│   └── jupiter.db
├── 📁 reports/           # 情报输出
│   └── 蓝牙耳机_痛点.csv
├── 📁 user_data_dir/     # Chrome 登录态
└── 📁 logs/              # 转储日志 + HTML 证据
```

---

## 📡 `watch ./logs/health.log` &nbsp;｜&nbsp; 运行情报（实时）

<div align="center">

| METRIC | VALUE | STATUS |
| :--- | :---: | :--- |
| 🛒 SEARCH PAGES / CATEGORY | **20** | <span style="color:#00FF41;">● ACTIVE</span> |
| 💬 NEG. COMMENTS / PRODUCT | **500 / 50 scrolls** | <span style="color:#00FF41;">● ACTIVE</span> |
| ⚡ MODAL v3 HIT RATE | **99 %** | <span style="color:#00FF41;">● ONLINE</span> |
| 🧩 AUTO K (ELBOW) | **k ∈ [2,15]** | <span style="color:#FFD700;">● AUTO</span> |
| 💾 RESUME CAPABLE | ✅ SQLite 双表 | <span style="color:#00FF41;">● READY</span> |
| 🛡️ ANTI-BLOCK RATE | ↓ 80% | <span style="color:#00FF41;">● STABLE</span> |

</div>

---

## 🏁 `grep "✓\|FAIL" ./runtime.log` &nbsp;｜&nbsp; 验收标志

| STAGE | SUCCESS GREP TOKEN |
| :--- | :--- |
| 遗留回流重置 | `[遗留重置] xx items reset` |
| 好评率入口命中 | `[赞不绝口入口 ✓]` |
| 模态框 DOM 挂载 | `[Modal 根 ✓]` |
| 差评 Tab 切换 | `[差评标签 双保险 ✓]` |
| 评价区加载 | `[评价区 锚点/UI回退路径]` |
| 全文展开滚动 | `scroll with expanded full text` |
| DB 落盘确认 | `DB write confirmed, Y≥10 comments` |

---

## ⚠️ `iptables -A SECURITY` &nbsp;｜&nbsp; 安全协议

<pre class="term-font" style="background:#1a0000;border:1px solid #ff003c;padding:14px 18px;border-radius:6px;color:#ff003c;">
[RULE_01] 🔒 pt_key / pt_pin 仅本地 YAML 注入，禁止：硬编码 / 聊天外传 / 入库 / 落日志
[RULE_02] 🚫 未登录态 Headless 启动 → 立即 ABORT；防止白跑 &amp; 风控封签
[RULE_03] 🧹 反爬拦截页(~3908B) 与 有效证据页(73KB+/77KB+/110KB+)：毫秒戳命名，永不覆盖
</pre>

---

## 🧱 `git flow init` &nbsp;｜&nbsp; 贡献协议

```bash
$ git checkout -b feat/black-ops-module
$ git commit -m "feat(op-zk): add zero-knowledge credential layer"
$ git push origin feat/black-ops-module
# → 开 PR，等 CI 绿 + maintainer review
```

<div align="center" class="term-font" style="color:#00FF41;">
  &gt; BUG / FEATURE REQUEST → 开 Issue<br>
  &gt; 如果它曾帮你挖到金矿 &nbsp;→&nbsp; ⭐ 点个 Star 让它活过来
</div>

---

## 🪪 `cat ./LICENSE` &nbsp;｜&nbsp; 开源许可

<p align="center">
  <a href="./LICENSE">
    <img src="https://img.shields.io/badge/LICENSE-MIT-00FF41?style=for-the-badge&logo=&logoColor=00FF41&labelColor=000"
         style="border:1px solid #00FF41;box-shadow:0 0 20px #00FF41;"/>
  </a>
</p>

<pre class="term-font" style="text-align:center;color:#00FF41;opacity:.55;">
╔══════════════════════════════════════════════════════════════════╗
║   MADE WITH ❤️ + ☕ BY THE AI MARKET DEMAND ANALYSIS BLACK OPS    ║
║   "WE MINE THE DARK REVIEWS, SO YOUR PRODUCT SHINES BRIGHTER."  ║
╚══════════════════════════════════════════════════════════════════╝
</pre>
