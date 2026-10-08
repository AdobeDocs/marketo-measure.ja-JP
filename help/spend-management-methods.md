---
description: Marketo Measure ユーザー向けの支出管理方法ガイダンス
title: 支出管理方法
exl-id: 36478d8d-986c-4d4f-8854-3287d6c57a9d
feature: Spend Management
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: e3b4b95f-0bb9-5cb3-a479-9dcb943dca3f
    internal-label: Spend Management
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 2%
---
# 支出管理方法 {#spend-management-methods}

[!DNL Marketo Measure]のROI レポートを成功させるには、支出データが重要です。 すべてのチャネルとサブチャネルで正確かつ包括的なROI レポートを作成するには、適切な支出データが[!DNL Marketo Measure]に取り込まれていることを確認する必要があります。

[!DNL Marketo Measure]に支出データを取り込む方法は3つあります。 各メソッドは、特定のデータ入力から支出データを取得するように設計されています。

**1個のAPI接続アカウント**

APIを介して[!DNL Marketo Measure]に接続した広告アカウントには、ROI レポート用に支出が自動的に[!DNL Marketo Measure]に取り込まれます。 接続したアカウントと支出を引き込んだアカウントを確認するには、[!DNL Marketo Measure] アプリに移動し、[!UICONTROL 統合] セクションの「[!UICONTROL 接続]」タブを選択します。 API接続の設定について詳しくは、[統合広告プラットフォーム ](/help/api-connections/integrated-ad-platforms.md)を参照してください。

**2 CRM キャンペーンコスト同期**

すべての[!DNL Marketo Measure] アカウントは、[CRM キャンペーンのコストを同期](/help/crm-campaign-costs.md)という機能にアクセスできます。 デフォルトでは、この機能ビットは「いいえ」に設定されていますが、いつでもオンにできます。

![すべてのMarketo Measure アカウントは、Sync](assets/spend-management-1.png)という機能にアクセスできます

この機能を有効にすると、次の条件を満たすCRM キャンペーン/プログラムから支出が自動的に取り込まれます。

私は。 [!DNL Marketo Measure]は、最初に、キャンペーン/プログラムが作成された一致する[ キャンペーン同期ルール ](/help/channel-tracking-and-setup/custom-campaign-sync.md)から、または作成された一致する[ プログラム同期ルール ](/help/marketo-engage-programs-integration.md)から、タッチポイントを作成しているかどうかを確認します。または、[購入者タッチポイントを有効にする値](/help/channel-tracking-and-setup/syncing-offline-campaigns.md)は、「すべてのキャンペーンメンバーを含める」または「応答済み」キャンペーンメンバーを含める」です。

ii. 開始日は、キャンペーン/プログラムに入力する必要があります

iii. 終了日は、キャンペーン/プログラムに入力する必要があります

iv. 実際のコスト（SFDCのキャンペーンの場合）または期間コスト（Marketoのプログラムの場合）を指定する必要があります。

**3手作業によるコストのアップロード**

この方法を使用すると、API接続アカウントまたはCRM Campaign Cost Syncでカバーされていないチャネルとサブチャネルの支出データ ](/help/marketing-channel-costs.md)を[手動でアップロードできます。 [!DNL Marketo Measure]設定の「マーケティング費用」セクションに移動すると、任意のチャネルのCSV ファイルを介して費用データをアップロードできます。

お客様は、これらの3つの方法をすべて組み合わせて、[!DNL Marketo Measure]の特定の設定に応じて、支出を管理できます。 [!DNL Marketo Measure]に支出を読み込む方法は3つあるので、「もっと知る」にあるマーケティング支出ボードを使用して、すべての支出データを包括的に表示することを強くお勧めします。 このボードは、すべてのチャネルとそれに関連する支出を確認できる唯一の場所です。 マーケティング費用ボードは、費用データにギャップがある場所をすばやく特定し、ROI レポートを改善する方法に役立ちます。
