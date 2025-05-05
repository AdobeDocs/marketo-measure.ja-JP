---
description: 支出管理方法 –  [!DNL Marketo Measure]
title: 支出管理方法
exl-id: 36478d8d-986c-4d4f-8854-3287d6c57a9d
feature: Spend Management
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 2%

---

# 支出管理方法 {#spend-management-methods}

支出データは、[!DNL Marketo Measure] での ROI レポートを成功させるための鍵です。 すべてのチャネルとサブチャネルにわたって正確で包括的な ROI レポートを作成するには、適切な支出データを [!DNL Marketo Measure] に取り込む必要があります。

支出データを [!DNL Marketo Measure] に取り込む方法は 3 つあります。 各方法は、特定のデータ入力から支出データを取り込むように設計されています。

**1 API 接続アカウント**

API を介して [!DNL Marketo Measure] に接続した広告アカウントには、ROI レポートのために支出が自動的に取り [!DNL Marketo Measure] まれます。 接続したアカウントを確認し、費用を引き出すには、[!DNL Marketo Measure] アプリに移動して、「[!UICONTROL &#x200B; 統合 &#x200B;]」セクションの下の「[!UICONTROL &#x200B; 接続 &#x200B;]」タブを選択します。 API 接続の設定について詳しくは、[ 統合広告プラットフォーム ](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md#how-to-connect-ad-platforms) を参照してください。

**2 CRM キャンペーンコスト同期**

すべての [!DNL Marketo Measure] アカウントは、「[CRM キャンペーンコストの同期 ](/help/marketing-spend/spend-management/crm-campaign-costs.md#availability) と呼ばれる機能にアクセスできます。 デフォルトでは、この機能ビットは「No」に設定されていますが、いつでもオンにできます。

![](assets/spend-management-methods-1.png)

有効にすると、この機能により、次の条件を満たす任意の CRM キャンペーン/プログラムから支出が自動的に取り込まれます。

i.最初に、キャンペーン/プログラム [!DNL Marketo Measure]、作成された一致する [ キャンペーン同期ルール ](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md) または作成された一致する [ プログラム同期ルール ](/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/marketo-engage-programs-integration.md) から、または [ 購入者タッチポイント値を有効にする ](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md#how-to-create-a-campaign-and-sync-buyer-touchpoints) が、「すべてのキャンペーンメンバーを含める」または「応答済みの」キャンペーンメンバーを含める」タッチポイントを作成しているかどうかを調べます。

ii.キャンペーン/プログラムに開始日を入力する必要があります

iii.キャンペーン/プログラムに終了日を入力する必要があります

iv.実際のコスト （SFDC のキャンペーンの場合）または期間コスト （Marketoのプログラムの場合）を指定する必要があります。

**3 手動コストアップロード**

この方法を使用すると、API 連携アカウントまたは CRM キャンペーンコスト同期でカバーされていないチャネルとサブチャネルの [ 費用データを手動でアップロード ](/help/marketing-spend/spend-management/marketing-channel-costs.md#uploading-marketing-costs) できます。 [!DNL Marketo Measure] 設定でマーケティング費用セクションに移動すると、CSV ファイルを介して任意のチャネルの費用データをアップロードできます。

顧客は、[!DNL Marketo Measure] ーザーの特定の設定に応じて、これら 3 つの方法すべてを組み合わせて使用し、費用を管理できます。 費用を [!DNL Marketo Measure] にインポートする方法は 3 つあるので、Discover にあるマーケティング費用ボードを使用して、すべての費用データを包括的に把握することを強くお勧めします。 このボードは、すべてのチャネルとそれに関連する支出を表示できる唯一の場所です。 マーケティング費用ボードを使用すると、費用データにギャップがある場所や、ROI レポートの改善方法をすばやく特定するのに役立ちます。
