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
html, body {
  margin: 0;
  padding: 0;
  background: #f4f7fb;
  font-family: "Segoe UI", "Hiragino Sans", "Yu Gothic", sans-serif;
}
.page {
  width: 297mm;
  height: 210mm;
  margin: 0 auto;
  padding: 10mm;
  box-sizing: border-box;
  background: #ffffff;
  box-shadow: 0 4mm 12mm rgba(15, 23, 42, 0.08);
  display: flex;
  flex-direction: column;
}
.header {
  text-align: center;
  margin-bottom: 6mm;
}
.header h1 {
  margin: 0 0 2mm;
  font-size: 20pt;
  letter-spacing: 0.05em;
  color: #0a3069;
}
.header p {
  margin: 0;
  font-size: 12pt;
  color: #4a5568;
}
.canvas {
  flex: 1;
  border: 0.4mm solid #d0d7de;
  border-radius: 4mm;
  background: #ffffff;
  padding: 5mm;
  box-sizing: border-box;
}
.mermaid {
  width: 100%;
  height: 100%;
}
.mermaid svg {
  width: 100%;
  height: 100%;
}
.caption {
  text-align: right;
  margin-top: 3mm;
  font-size: 9pt;
  color: #6b7280;
}
@media (max-width: 1024px) {
  .page {
    width: 100vw;
    height: auto;
    padding: 4vw;
  }
  .canvas {
    min-height: 70vh;
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
    fontSize: "16px",
    primaryColor: "#E7F1FF",
    primaryTextColor: "#0A3069",
    primaryBorderColor: "#1F6FEB",
    lineColor: "#1F6FEB"
  },
  flowchart: {
    curve: "basis",
    padding: 25,
    nodeSpacing: 80,
    rankSpacing: 120,
    htmlLabels: true,
    useMaxWidth: true
  }
});
</script>
</head>

<body>
<div class="page">
  <div class="header">
    <h1>草野弘道FP｜現状把握フローチャート</h1>
    <p>イエス・ノーで進めるデジタル施策診断</p>
  </div>

  <div class="canvas">
    <div class="mermaid">
flowchart LR
    Q1{"オンラインからの<br>問い合わせが安定している？"}
    Q2{"相談数は増えて<br>対応負荷を感じる？"}
    Q3{"自動化の仕組みを<br>導入済み？"}
    A["【A】改善余地の洗い出し"]
    B["【B】LINE自動化構築"]
    Q4{"集客は安定しているが<br>リピートや口コミに課題？"}
    C["【C】口コミ・再来導線強化"]
    D["【D】ブランド拡大（動画・SEO）"]
    Q5{"SNSや検索からの<br>問い合わせがほとんど無い？"}
    Q6{"まずは認知拡大を<br>優先したい？"}
    E["【E】動画・SNS露出強化"]
    F["【F】検索導線整備"]
    Q7{"見込み客は集まるが<br>契約に繋がらない？"}
    Q8{"個別対応の負担が大きい？"}
    Q9{"既存顧客フォローの<br>仕組みは整っている？"}
    G["【G】セミナーで信頼醸成"]
    H["【H】高度AIで効率化"]
    I["【I】既存顧客情報発信＋AI要約"]

    Q1 -->|Yes| Q2
    Q1 -->|No| Q5

    Q2 -->|Yes| Q3
    Q2 -->|No| Q4

    Q3 -->|Yes| A
    Q3 -->|No| B

    Q4 -->|Yes| C
    Q4 -->|No| D

    Q5 -->|Yes| Q6
    Q5 -->|No| Q7

    Q6 -->|Yes| E
    Q6 -->|No| F

    Q7 -->|Yes| Q8
    Q7 -->|No| Q9

    Q8 -->|Yes| B
    Q8 -->|No| G

    Q9 -->|Yes| H
    Q9 -->|No| I
    </div>
  </div>

  <div class="caption">A4横 297×210mm レイアウト（GitHub Pages 用）</div>
</div>
</body>
</html>
