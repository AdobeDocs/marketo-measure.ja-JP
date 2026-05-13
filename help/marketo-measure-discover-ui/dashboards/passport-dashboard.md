---
description: パスポートダッシュボード - [!DNL Marketo Measure]  – 製品
title: パスポートダッシュボード
feature: Reporting
exl-id: 0fbd9714-7d9c-4330-b35f-d011e17c3bfe
TQID: https://experienceleague.adobe.com/SlIfN-Y5sttJQUeLgA-JA-H-lbRJMS8BrgBYdnhmgZk
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 2%

---

# パスポートダッシュボード {#passport-dashboard}

パスポートダッシュボードでは、リード、コンタクト、商談が、指定した期間内にさまざまなステージを通過する際の動的なビューをマーケターに提供します。 特定の日付をフィルタリングすることで、ユーザーはその日のレコードのスナップショットを取得することもできます。

**掲示板の回答に対する質問：**

* 選択した日に、ターミナル以外の各ステージにどれだけのリード、コンタクト、商談が存在しましたか？
* 特定の期間を通して、それぞれの一時的なステージを通過したリードまたはコンタクトの数を確認します。
   * _例_: リード Aが2023年1月1日のステージ 1にいて、2023年3月31日までにステージ 5に進んだ場合、2023年第1四半期のパスポート分析では、ステージ 1から5のリード Aがカウントされます。
* 特定の時間枠の間に各一時的なステージを通過したユニークな機会はいくつありますか？

## ダッシュボードコンポーネント {#dashboard-components}

### ステージ名によるステージ内の商談 {#opportunities-in-stage-by-stage-name}

* 各段階は、特定の期間内に通過した顧客接点がある商談の数を示します。
   * オポチュニティがそのスパン内の複数のステージを進む場合、通過するあらゆるステージでカウントされます。
* 「クローズド・ウォン」や「クローズド・ロスト」などの終端ステージは除外されます。
* 開始日と終了日の両方が含まれます。

![](assets/passport-dashboard-1.png)

### ステージ名でステージ内のリードまたはコンタクト {#leads-or-contacts-in-stage-by-stage-name}

* 各ステージには、特定の時間枠で通過したリードまたは顧客接点のあるコンタクトの数が表示されます。
   * 「リード」と「連絡先」のどちらを表示するかは、設定/アトリビューション設定/デフォルトダッシュボードオブジェクトで設定された環境設定によって決まります。
   * リードまたはコンタクトがそのスパン内の複数のステージを進む場合、通過するあらゆるステージで数えられます。
* 「クローズド・ウォン」や「クローズド・ロスト」などの終端ステージは除外されます。
* 開始日と終了日の両方が含まれます。

![](assets/passport-dashboard-2.png)

## フィルターパネル {#filter-pane}

このダッシュボードには、次の設定とフィルターが用意されています。

* 日付（移行日に基づく）
* チャネル、サブチャネル
* キャンペーン
* セグメント

>[!MORELIKETHIS]
>
>* [Discover ダッシュボードの基本](/help/marketo-measure-discover-ui/dashboards/discover-dashboard-basics.md){target="_blank"}
>* [&#x200B; ダッシュボードデータの可視化ポリシー](/help/marketo-measure-discover-ui/dashboards/dashboard-data-visibility-policy.md){target="_blank"}
