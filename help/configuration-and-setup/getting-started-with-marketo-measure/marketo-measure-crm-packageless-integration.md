---
description: '[!DNL Marketo Measure] CRM パッケージレス統合 –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] CRM パッケージレス統合'
exl-id: a4f31d82-63ec-4bb2-bc8b-d3495e61af4f
feature: Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 2%

---


# [!DNL Marketo Measure] CRM パッケージレス統合 {#marketo-measure-crm-packageless-integration}

すべてのマーケティングチームが、アクセスの制限、CRM の所有権、価値創出までの時間の延長、法的な影響などの理由にかかわらず、CRM からマーケティングレポートを実行する（またはアクセス権を持つ）わけではありません。 クイックスタートの道筋を進め [!DNL Marketo Measure] と、できるだけ CRM に依存することなく、効果的に [!DNL Marketo Measure] を実装して実行できます。

## 標準 [!DNL Marketo Measure] インストール {#standard-marketo-measure-installation}

標準の [!DNL Marketo Measure] インストールを通じて、[!DNL Salesforce] パッケージまたは [!DNL Microsoft Dynamics] Managed Solution をインストールする必要があります。 インストールには、CRM に追加され、データの書き込み先となるカスタムオブジェクト/エンティティ [!DNL Marketo Measure] カスタムフィールドが含まれます。

[!DNL Marketo Measure] とのパッケージレス統合は、CRM でカスタムオブジェクト/エンティティやカスタムフィールドを作成したくない顧客のためです。 また、外部Data Warehouseを使用しているお客様にも適したオプションです。

## 権限 {#permissions}

[!DNL Marketo Measure] の CRM パッケージレス統合でも、リードや連絡先などの標準の CRM オブジェクトへのアクセスが必要です。 適切なデータアクセス権限を持つ専用のユーザーが、接続ユーザーとして機能することをお勧めします。

すべてのデータが CRM から正しく取り込まれていることを確認するには、セキュリティとアクセシビリティに関する次の設定が必要です。専用ユーザーのプロファイルのすべてのデータを表示。 このアクセス権セットは、標準オブジェクトからデータをダウンロードするために必要なアクセス権を [!DNL Marketo Measure] に付与します。 この権限セットはプロファイルレベルです。

## ID プロバイダーとデータ接続のセットアップ {#setup-your-identity-provider-and-data-connections}

以下のガイドでは、[!DNL Salesforce] パッケージまたは [!DNL Microsoft Dynamics] Managed Solution をインストールする手順をスキップし、権限と統合手順にのみ従ってください。

[!DNL Salesforce] のお客様は [&#x200B; こちら &#x200B;](/help/configuration-and-setup/marketo-measure-and-salesforce/install-set-up.md) をクリックしてください。

[!DNL Microsoft Dynamics] のお客様は [&#x200B; こちら &#x200B;](/help/marketo-measure-and-dynamics/microsoft-dynamics-crm-installation-guide.md) をクリックしてください。

これらの手順を完了すると、統合は動作するようになります。 問題が発生した場合は、[!DNL Marketo Measure] 担当者または [Marketo サポート &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。

>[!NOTE]
>[!DNL Marketo Measure] CRM パッケージレス統合から始める場合は、後でSalesforce パッケージまたはMicrosoft Dynamics Managed Solution をインストールできます。
