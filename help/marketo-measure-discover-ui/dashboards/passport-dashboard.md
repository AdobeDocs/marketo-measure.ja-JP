---
description: Passport ダッシュボード — [!DNL Marketo Measure]  — 製品
title: パスポートダッシュボード
feature: Reporting
exl-id: 0fbd9714-7d9c-4330-b35f-d011e17c3bfe
source-git-commit: 403b31acce25ddc9c1dcafbd53008b6e2868b3df
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 3%

---

# パスポートダッシュボード {#passport-dashboard}

Passport ダッシュボードを使用すると、マーケターは、指定した期間内に様々なステージに移行するリード、連絡先、商談の動的なビューを提供できます。 特定の日付に対してフィルターを適用すると、その日のレコードのスナップショットを取得することもできます。

**取締役会の回答に関する質問：**

* 任意の日に各非ターミナルステージに存在したリード、連絡先、商談の数は？
* 指定した期間中に、各一時的なステージを進んだ個別のリードまたは連絡先の数は？
   * _例_：リード A が1/1/2023のステージ 1 にあり、ステージ 5 by 3/31/2023に進んだ場合、2023 年第 1 四半期の Passport 分析では、ステージ 1 ～ 5 のリード A がカウントされます。
* 特定の期間内に各一時的なステージを通過したユニークなオポチュニティはいくつですか？

## ダッシュボードコンポーネント {#dashboard-components}

### ステージ名別の商談 {#opportunities-in-stage-by-stage-name}

* 各ステージには、特定の期間にタッチポイントを通過した商談の数が表示されます。
   * オポチュニティがその範囲内の複数のステージを経て進むと、通過するすべてのステージでカウントされます。
* 終了段階（「獲得しました」や「損失しました」など）は除外されます。
* 開始日と終了日は両方とも含まれます。

![](assets/passport-dashboard-1.png)

### ステージ名別のリードまたはステージ内の連絡先 {#leads-or-contacts-in-stage-by-stage-name}

* 各ステージには、特定の期間内にリードまたはタッチポイントを通過した連絡先の数が表示されます。
   * 「リード」と「連絡先」のどちらを表示するかは、設定/属性設定/デフォルトのダッシュボードオブジェクトで設定した環境設定によって決まります。
   * リードまたは連絡先がその範囲内の複数のステージを進むと、通過するすべてのステージでカウントされます。
* 終了段階（「獲得しました」や「損失しました」など）は除外されます。
* 開始日と終了日は両方とも含まれます。

![](assets/passport-dashboard-2.png)

## フィルターウィンドウ {#filter-pane}

このダッシュボードには、次の設定とフィルターが備わっています。

* 日付（遷移日に基づく）
* チャネル、サブチャネル
* キャンペーン
* セグメント

>[!MORELIKETHIS]
>
>* [Discover ダッシュボードの基本](/help/marketo-measure-discover-ui/dashboards/discover-dashboard-basics.md){target="_blank"}
>* [ダッシュボードデータ表示ポリシー](/help/marketo-measure-discover-ui/dashboards/dashboard-data-visibility-policy.md){target="_blank"}
