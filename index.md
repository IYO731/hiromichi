---
layout: none
---

<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>草野弘道FP｜現状把握フローチャート</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
:root {
  --page-width: 297mm;
  --page-height: 210mm;
  --page-padding: 12mm;
  --bg-color: #f1f5fb;
  --page-bg: #ffffff;
  --primary: #0a3069;
  --accent: #1f6feb;
}
* {
  box-sizing: border-box;
}
html, body {
  margin: 0;
  padding: 0;
  background: var(--bg-color);
  font-family: "Segoe UI", "Hiragino Sans", "Yu Gothic", sans-serif;
}
.wrapper {
  width: var(--page-width);
  height: var(--page-height);
  margin: 12mm auto;
  padding: var(--page-padding);
  background: var(--page-bg);
  border-radius: 6mm;
  box-shadow: 0 6mm 18mm rgba(15, 23, 42, 0.15);
  display: flex;
  flex-direction: column;
}
header {
  text-align: center;
  margin-bottom: 6mm;
}
header h1 {
  margin: 0 0 1mm;
  font-size: 26pt;
  letter-spacing: 0.05em;
  color: var(--primary);
  font-weight: 700;
}
header p {
  margin: 0;
  font-size: 13pt;
  color: #4a5568;
  letter-spacing: 0.03em;
  font-weight: 500;
}
canvas-flow {
  flex: 1;
  border: 0.6mm solid #d0d7de;
  border-radius: 4mm;
  padding: 6mm;
  background: #ffffff;
  display: block;
}
.mermaid {
  width: 100%;
  height: 100%;
}
.mermaid svg {
  width: 100% !important;
  height: 100% !important;
}
.mermaid svg text {
  font-size: 22px !important;
  font-weight: 700 !important;
  font-family: "Segoe UI", "Hiragino Sans", "Yu Gothic", sans-serif !important;
  fill: var(--primary) !important;
}
.mermaid svg .label foreignObject > div {
  font-size: 22px !important;
  font-weight: 700 !important;
  line-height: 1.35;
  color: var(--primary);
}
.caption {
  margin-top: 4mm;
  text-align: right;
  font-size: 11pt;
  color: #6b7280;
  font-weight: 500;
}

/* レスポンシブ（スマホ・タブレット）表示 */
@media (max-width: 1200px) {
  .wrapper {
    width: 100vw;
    height: auto;
    margin: 0;
    border-radius: 0;
    padding: 4vw;
  }
  canvas-flow {
    min-height: 75vh;
  }
}
</style>

<script type="module">
import mermaid from "https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs";
mermaid.initialize({
  startOnLoad: true,
  theme: "default",
  themeVariables: {
    fontFamily: "'Segoe UI', 'Hiragino Sans', 'Yu Gothic', sans-serif",
    fontSize: "22px",
    fontWeight: "700",
    primaryColor: "#e8f1ff",
    primaryTextColor: "#0a3069",
    primaryBorderColor: "#1f6feb",
    lineColor: "#1f6feb",
    edgeLabelBackground: "#ffffff"
  },
  flowchart: {
    diagramPadding: 30,
    nodeSpacing: 110,
    rankSpacing: 140,
    curve: "basis",
    htmlLabels: true,
    padding: 12,
    useMaxWidth: true,
    wrap: true
  }
});
</script>
</head>

<body>
<div class="wrapper">
  <header>
    <h1>草野弘道FP｜現状把握フローチャート</h1>
    <p>イエス・ノーで進めるデジタル施策診断</p>
  </header>

  <canvas-flow>
    <div class="mermaid">
flowchart LR
    classDef decision fill:#e8f1ff,stroke:#1f6feb,stroke-width:3px,color:#0a3069;
    classDef action fill:#cfe1ff,stroke:#1f6feb,stroke-width:3px,color:#0a3069;

    Q1{"オンラインからの<br>問い合わせが\n安定している？"}
    Q2{"相談数は増えており\n対応負荷を感じる？"}
    Q3{"自動化の仕組みを\n導入済み？"}
    GoalA["【A】改善余地の洗い出し"]
    GoalB["【B】LINE自動化構築"]
    Q4{"集客は安定しているが\nリピート・口コミに課題？"}
    GoalC["【C】口コミ・再来導線強化"]
    GoalD["【D】ブランド拡大\n（動画・SEO）"]
    Q5{"SNSや検索からの\n問い合わせが少ない？"}
    Q6{"まずは認知拡大を\n優先したい？"}
    GoalE["【E】動画・SNS露出強化"]
    GoalF["【F】検索導線整備"]
    Q7{"見込み客は集まるが\n契約・相談に繋がらない？"}
    Q8{"個別対応の負担が大きい？"}
    Q9{"既存顧客フォローの\n仕組みは整っている？"}
    GoalG["【G】セミナーで信頼醸成"]
    GoalH["【H】高度AIで効率化"]
    GoalI["【I】既存顧客情報発信＋AI要約"]

    Q1 -->|はい| Q2
    Q1 -->|いいえ| Q5

    Q2 -->|はい| Q3
    Q2 -->|いいえ| Q4

    Q3 -->|はい| GoalA
    Q3 -->|いいえ| GoalB

    Q4 -->|はい| GoalC
    Q4 -->|いいえ| GoalD

    Q5 -->|はい| Q6
    Q5 -->|いいえ| Q7

    Q6 -->|はい| GoalE
    Q6 -->|いいえ| GoalF

    Q7 -->|はい| Q8
    Q7 -->|いいえ| Q9

    Q8 -->|はい| GoalB
    Q8 -->|いいえ| GoalG

    Q9 -->|はい| GoalH
    Q9 -->|いいえ| GoalI

    class Q1,Q2,Q3,Q4,Q5,Q6,Q7,Q8,Q9 decision;
    class GoalA,GoalB,GoalC,GoalD,GoalE,GoalF,GoalG,GoalH,GoalI action;
    </div>
  </canvas-flow>

  <div class="caption">A4横 297×210mm レイアウト｜Mermaid Flowchart</div>
</div>
</body>
</html>
