---
description: '[!DNL Marketo Measure] CRM パッケージなしの統合 – [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] CRM パッケージレス統合'
exl-id: a4f31d82-63ec-4bb2-bc8b-d3495e61af4f
feature: Integration
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: 7da342c5-06ee-5869-b3e8-b73d5bf75a9d
    internal-label: Integration
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 4%
---

# [!DNL Marketo Measure] CRM パッケージレス統合 {#marketo-measure-crm-packageless-integration}

アクセスが限られている、CRMの所有権、価値実現までの時間が長い、法的な影響などの理由で、マーケティング部門がCRMからマーケティングレポートを実行する（またはアクセスできる）ことを望んでいるわけではありません。 [!DNL Marketo Measure] クイックスタートのパスを下ると、CRMへの依存をできる限り少なくして[!DNL Marketo Measure]を効果的に実装して実行できます。

## 標準[!DNL Marketo Measure] インストール {#standard-marketo-measure-installation}

標準の[!DNL Marketo Measure] インストールを通じて、[!DNL Salesforce] パッケージまたは[!DNL Microsoft Dynamics] マネージド ソリューションをインストールする必要があります。 インストールには、[!DNL Marketo Measure]がデータを書き込むことができるCRMに追加されるカスタムオブジェクト/エンティティとカスタムフィールドが含まれます。

[!DNL Marketo Measure]とのパッケージレス統合は、CRMでカスタムオブジェクト/エンティティまたはカスタムフィールドを作成したくない顧客向けです。 また、外部Data Warehouseを使用しているお客様にも適しています。

## 権限 {#permissions}

[!DNL Marketo Measure] CRM パッケージを使用しない統合では、引き続きリードや連絡先などの標準のCRM オブジェクトにアクセスする必要があります。 専用ユーザーは、適切なデータアクセス権限を持っているため、接続されたユーザーとして機能することをお勧めします。

すべてのデータがCRMから適切に取得されていることを確認するには、次のセキュリティとアクセシビリティ設定が必要です。専用ユーザーのプロファイルのすべてのデータを表示します。 この権限セットは、[!DNL Marketo Measure]に標準オブジェクトからデータをダウンロードするために必要なアクセス権を与えます。 この権限セットはプロファイルレベルです。

## ID プロバイダーとデータ接続の設定 {#setup-your-identity-provider-and-data-connections}

以下のガイドでは、[!DNL Salesforce] パッケージまたは[!DNL Microsoft Dynamics] マネージドソリューションをインストールする手順をスキップし、権限と統合手順のみに従います。

[!DNL Salesforce]人のお客様が[ここ](/help/configuration-and-setup/install-set-up.md)をクリックします。

[!DNL Microsoft Dynamics]人のお客様が[ここ](/help/microsoft-dynamics-crm-installation-guide.md)をクリックします。

これらの手順を完了した後、統合は運用的である必要があります。 問題が発生した場合は、[!DNL Marketo Measure]担当者または[Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}にお問い合わせください。

>[!NOTE]
>[!DNL Marketo Measure] CRM パッケージレス統合から開始する場合は、後でSalesforce パッケージまたはMicrosoft Dynamics Managed Solutionをインストールできます。
