---
unique-page-id: 37356027
description: '"[!DNL Marketo Measure] CRM パッケージレスの統合 — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: '"[!DNL Marketo Measure] CRM パッケージレス統合»'
exl-id: a4f31d82-63ec-4bb2-bc8b-d3495e61af4f
source-git-commit: 993a326c377b3b6ff48c4e0114b59297f9ca2ca6
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 2%

---

# [!DNL Marketo Measure] CRM パッケージレス統合 {#marketo-measure-crm-packageless-integration}

アクセスが制限されているか、CRM の所有権、価値の創出に時間がかかるか、法的な影響があるかにかかわらず、すべてのマーケティングチームが CRM からマーケティングレポートを実行したい（またはアクセスできる）わけではありません。 ～の道を下る [!DNL Marketo Measure] クイックスタートを使用すると、を効果的に実装および実行できます [!DNL Marketo Measure] CRM への依存をできるだけ少なく抑えて

## 標準 [!DNL Marketo Measure] インストール {#standard-marketo-measure-installation}

標準を使用 [!DNL Marketo Measure] インストールするには、 [!DNL Salesforce] パッケージまたは [!DNL Microsoft Dynamics] 管理ソリューション。 インストールには、カスタムオブジェクト/エンティティと、CRM に追加されるカスタムフィールドが含まれます。 [!DNL Marketo Measure] その後、はにデータを書き込むことができます。

とのパッケージレスな統合 [!DNL Marketo Measure] は、CRM でカスタムオブジェクト/エンティティやカスタムフィールドを作成したくないお客様向けです。 また、外部データウェアハウスを使用しているお客様にも便利なオプションです。

## 権限 {#permissions}

A [!DNL Marketo Measure] CRM パッケージレスの統合では、引き続き、リードや連絡先などの標準の CRM オブジェクトにアクセスする必要があります。 接続されたユーザーには適切なデータアクセス権限が付与されるので、専用のユーザーを接続ユーザーとして使用することを強くお勧めします。

すべてのデータが CRM から正しく取り込まれるようにするには、次のセキュリティとアクセシビリティの設定が必要です。専用ユーザーのプロファイルのすべてのデータを表示します。 この権限セットは [!DNL Marketo Measure] 標準オブジェクトからデータをダウンロードするために必要なアクセス。 この権限セットはプロファイルレベルです。

## ID プロバイダーとデータ接続のセットアップ {#setup-your-identity-provider-and-data-connections}

以下のガイドで、 [!DNL Salesforce] パッケージまたは [!DNL Microsoft Dynamics] 管理ソリューションに保存され、権限と統合手順にのみ従います。

[!DNL Salesforce] 顧客、クリック [ここ](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md).

[!DNL Microsoft Dynamics] 顧客、クリック [ここ](/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/microsoft-dynamics-crm-installation-guide.md).

上記の手順をすべて完了したら、準備が整いました。 途中で問題が発生した場合は、お気軽に連絡を取ってください [!DNL Marketo Measure] 代理人または [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

>[!NOTE]
>
>最初に [!DNL Marketo Measure] CRM パッケージレスの統合は、後で Salesforce パッケージまたはMicrosoft Dynamics Managed Solution をインストールできます。
