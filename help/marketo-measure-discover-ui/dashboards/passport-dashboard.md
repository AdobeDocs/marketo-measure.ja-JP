---
description: パスポートダッシュボード - [!DNL Marketo Measure]  – 製品
title: パスポートダッシュボード
feature: Reporting
exl-id: 0fbd9714-7d9c-4330-b35f-d011e17c3bfe
source-git-commit: 403b31acce25ddc9c1dcafbd53008b6e2868b3df
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 3%

---

# パスポートダッシュボード {#passport-dashboard}

Passport ダッシュボードを使用すると、マーケターは、指定された期間内の様々なステージを進みながら、リード、連絡先および商談を動的に確認できます。 特定の日付をフィルタリングすることで、その日のレコードのスナップショットを取得することもできます。

**ボードが回答する質問：**

* 任意の日に各非端末ステージに存在したリード、連絡先または商談の数
* 指定した期間において、各一時的ステージで進行した個別のリードまたは担当者の数は？
   * _例_：リード A が 2023 年 1 月 1 日にステージ 1 にあり、2023 年 3 月 31 日までにステージ 5 に進んだ場合、2023 年 Q1 のパスポート分析では、ステージ 1～5 にあるリード A がカウントされます。
* 特定の時間枠に各一時的ステージを通過したユニーク商談の数

## ダッシュボードコンポーネント {#dashboard-components}

### ステージ名によるステージ内の商談 {#opportunities-in-stage-by-stage-name}

* 各ステージは、特定の期間内にタッチポイントを通過した商談の数を示します。
   * その範囲内で商談が複数のステージを経て進行する場合、通過するすべてのステージでカウントされます。
* 「クローズ済み受注」や「クローズ済み失注」などの端末ステージは除外されます。
* 開始日と終了日は両方とも含まれます。

![](assets/passport-dashboard-1.png)

### ステージ内のリードまたは取引先責任者（ステージ名別） {#leads-or-contacts-in-stage-by-stage-name}

* 各ステージは、特定の期間内に通過したタッチポイントを持つリードまたは連絡先の数を示します。
   * 「リード」と「連絡先」のどちらを表示するかは、設定/アトリビューション設定/デフォルトのダッシュボードオブジェクトで設定する環境設定によって決まります。
   * リードまたはコンタクト先が、その範囲内で複数のステージを経て進行した場合、通過するすべてのステージでカウントされます。
* 「クローズ済み受注」や「クローズ済み失注」などの端末ステージは除外されます。
* 開始日と終了日は両方とも含まれます。

![](assets/passport-dashboard-2.png)

## フィルターウィンドウ {#filter-pane}

このダッシュボードには、次の設定とフィルターが備わっています。

* 日付（移行日に基づく）
* チャネル、サブチャネル
* キャンペーン
* セグメント

>[!MORELIKETHIS]
>
>* [Discover ダッシュボードの基本](/help/marketo-measure-discover-ui/dashboards/discover-dashboard-basics.md){target="_blank"}
>* [&#x200B; ダッシュボードデータ表示ポリシー &#x200B;](/help/marketo-measure-discover-ui/dashboards/dashboard-data-visibility-policy.md){target="_blank"}
