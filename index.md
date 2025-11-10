---
layout: default
---

# 草野弘道FP｜現状把握フローチャート
<style>
.mermaid {
  max-width: 1200px;       /* 表示幅を広げたい場合はここを調整 */
  margin: 0 auto;
}
.mermaid svg {
  width: 100%;
  height: auto;
}
</style>
<script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
<script>
mermaid.initialize({
  startOnLoad: true,
  theme: "default",
  themeVariables: { fontSize: "18px" },      // ノード内文字を大きく
  flowchart: { useMaxWidth: false, nodeSpacing: 70, rankSpacing: 60 }
});
</script>

## フローチャート（イエス・ノーで進む）

<div class="mermaid">
flowchart TD
    Q1(["Q1. すでにオンラインでお客様の問い合わせが安定的に来ていますか？"])
    Q2(["Q2. 相談数は増えているけれど、対応に時間が取られていると感じますか？"])
    Q3(["Q3. 相談対応の自動化や効率化の仕組みは導入済みですか？"])
    A["【A】改善余地の洗い出しへ"]
    B["【B】LINE公式アカウントの自動化構築"]
    Q4(["Q4. 集客は安定しているが、既存顧客のリピートや口コミ促進に課題がありますか？"])
    C["【C】口コミ・再来導線強化"]
    D["【D】さらなるブランドの拡大（動画・SEO）"]
    Q5(["Q5. SNSや検索からの問い合わせがほとんどありませんか？"])
    Q6(["Q6. まずは「認知」を広げる施策を優先しますか？"])
    E["【E】動画・SNS露出強化"]
    F["【F】検索導線の整備（Googleビジネス・ブログ）"]
    Q7(["Q7. 見込み客は集まるが、相談や契約に結び付かないのが悩みですか？"])
    Q8(["Q8. 個別対応の負担が重いですか？"])
    Q9(["Q9. 既存顧客のフォローや情報提供の仕組みは整っていますか？"])
    G["【G】セミナー・教育コンテンツで信頼醸成"]
    H["【H】高度なAI活用で効率化"]
    I["【I】既存顧客向け情報発信とAI要約"]

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

## 各ゴールと推奨ツール

（※ここに README と同じ説明を続けて貼り付けてください）
