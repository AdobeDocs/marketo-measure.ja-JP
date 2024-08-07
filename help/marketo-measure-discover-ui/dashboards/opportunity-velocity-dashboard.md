---
description: 商談速度ダッシュボード - [!DNL Marketo Measure]  – 製品
title: 商談速度ダッシュボード
feature: Reporting
exl-id: d02455fd-8fca-435e-8ded-69abbbdcb3a4
source-git-commit: c5a799c20d15c9e14bbdc69f422cd1b90a121e37
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 4%

---

# 商談速度ダッシュボード {#opportunity-velocity-dashboard}

Velocity ダッシュボードは、見込み客がセールスファネル内を移動するペースの動的なビューを提供し、マーケターやセールスチームに、様々なチャネルにわたるコンバージョン時間に関する重要なインサイトを提供します。 このツールは、オポチュニティのライフサイクルやセールス段階を通じた進行の効率に関する重要な質問に答えるために非常に役立ちます。このツールを使用すると、成長とコンバージョンを加速するためのエンゲージメント戦略を最適化できます。

このダッシュボードが回答する質問：

* 平均して、リードのコンバージョンにはどのくらいの時間がかかりますか？
* 各ステージの平均で、リードまたは連絡先が次のステージに進むまでにかかる時間は？ この期間の時間的変化

## ダッシュボードコンポーネント {#dashboard-components}

### KPI タイル {#kpi-tile}

* **クローズ済み契約速度**：最初のステージからクローズまでの「クローズ済み受注」商談の平均日数。

### ステージ別商談速度 {#opportunity-velocity-by-stage}

棒グラフは、特定の期間に各販売ステージで費やした商談の平均期間（日数）を表示します。

グラフに対する質問：

* 指定した期間の平均で商談が最も時間を費やしているのは、どのステージですか？
* 「商談作成」ステージの商談の平均期間を「見込み客」ステージおよび「商談選定」ステージと比較してどうですか？

>[!NOTE]
>
>「商談作成」より前のステージでは、最新のタッチポイント日を「遷移イン」日として使用します。

![](assets/lead-velocity-dashboard-1.png)

### 商談速度の履歴 {#opportunity-velocity-over-time}

時系列の折れ線グラフには、指定した期間の各販売ステージでの商談の平均滞在時間（日数）が表示されます。

* ドリルダウン機能とアップ機能を使用して、月、四半期または年によってデータを分類します。
* 線の上にマウスポインターを置くと、詳細情報が表示されます。

グラフに対する質問：

* 観測された数か月間での、商談の各段階での滞在時間のトレンドは何ですか？
* 営業段階を通じて商談が最も速い進捗を経験したのは、どの月ですか？

![](assets/lead-velocity-dashboard-2.png)

### チャネル別商談速度 {#opportunity-velocity-by-channel}

棒グラフは、各ファネルステージにリード/連絡先が残っている平均期間（日数）を、チャネル別にセグメント化して表示します。

* 線の上にマウスポインターを置くと、詳細情報が表示されます。

グラフに対する質問：

* ファネルステージを通じて最も速い進捗を示しているチャネルはどれですか？
* 「見込み客」ステージの商談速度は、様々なチャネルでどのように異なりますか？

![](assets/lead-velocity-dashboard-3.png)

## フィルターウィンドウ {#filter-pane}

このダッシュボードには、次の設定とフィルターが備わっています。

* 日付
   * 基準：遷移イン日
* ステージ
* チャネル
* サブチャネル
* キャンペーン
* セグメント
