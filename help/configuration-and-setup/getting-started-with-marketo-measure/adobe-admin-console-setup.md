---
description: Adobe Admin Console の設定 - Marketo Measure - 製品ドキュメント
title: Adobe Admin Console の設定
feature: Installation
exl-id: f9edacae-79e0-408c-ac37-bbe67c185f2d
source-git-commit: 666812e8bf095170d611cd694b5d0ac5151d8fdd
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 85%

---

# Adobe Admin Console の設定 {#adobe-admin-console-setup}

[!DNL Marketo Measure] を使用する最初の手順は、プロビジョニングされた Adobe Admin Console を作成してログインすることです。ログイン手順が記載されたメールが届いていない場合は、[!DNL Marketo Measure] アカウント担当者にお問い合わせください。

## Adobe Admin Console と ID プロバイダーの設定 {#set-up-your-adobe-admin-console-and-identity-provider}

[!DNL Marketo Measure] は、Adobe Suite 内の製品として、Adobe Admin Console for Identity Management の全機能を使用します。その他のリソースは、[こちらを参照](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)してください。

[Identity Management](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html?lang=jp) で利用できるすべてのリソース、ベストプラクティス、オプションを確認することをお勧めします。

Adobe Admin Console 内での Identity Management の設定に関するガイダンスと確認については、[!DNL Marketo Measure] アカウント担当者にお問い合わせください。

[!DNL Marketo Measure] インスタンスでのユーザ認証と承認を容易にするには、Adobe Admin Console 内で次の手順を実行する必要があります。

**[!DNL Marketo Measure] 製品カードの設定**

Adobe Admin Console にアクセスすると、「概要」セクションに [!DNL Marketo Measure] 製品インスタンスが表示されます。

![](assets/adobe-admin-console-setup-1.png)

[!DNL Marketo Measure] 製品カードをクリックすると、すべての [!DNL Marketo Measure] インスタンスが表示されます。デフォルトでは、各 [!DNL Marketo Measure] インスタンスには「[!DNL Marketo Measure]」という接頭辞が付いた独自のプロファイルがあります。このインスタンス内のこのプロファイルや他のプロファイルに追加された管理者またはユーザは、[!DNL Marketo Measure] にログインできるようになります。

![](assets/adobe-admin-console-setup-2.png)

[!DNL Marketo Measure] 製品インスタンス内でプロファイルを作成する際に必要なアクションはありません。

[!DNL Marketo Measure] にアクセスできるユーザの追加を開始するには、以下の[&#x200B;  [!DNL Marketo Measure]  管理者と  [!DNL Marketo Measure]  ユーザの追加](#adding-marketo-measure-admins-and-marketo-measure-users)の節を参照してください。

## [!DNL Marketo Measure] 管理者と [!DNL Marketo Measure] ユーザの追加 {#adding-marketo-measure-admins-and-marketo-measure-users}

次の手順では、ユーザを追加して [!DNL Marketo Measure] アプリケーションへのアクセスを付与します。これは、[!DNL Marketo Measure] 製品カードの管理者およびユーザディレクトリで実行できます。

| ユーザタイプ | 説明 |
|---|---|
| 管理者 | これらは、[!DNL Marketo Measure] 固有の設定オプションを更新および管理する完全な機能を持つ、[!DNL Marketo Measure] アプリケーションの管理者およびパワーユーザです。 |
| ユーザ | これらは、[!DNL Marketo Measure] アプリケーション内で読み取り専用権限を持つ [!DNL Marketo Measure] アプリケーションの標準ユーザです。 |

ユーザを各グループに追加すると、そのユーザの[リストされた ID タイプ](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html?lang=jp)が表示されます。

>[!NOTE]
>
>[!DNL Marketo Measure] 管理者（[experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}）になるには、_製品カード内のすべての_ 製品プロファイルで、ユーザー [!DNL Marketo Measure] および [!DNL Marketo Measure] 管理者）として追加される必要があります。

**[!DNL Marketo Measure]** へのログイン

製品プロファイルに追加されたユーザーは、[!DNL Marketo Measure]experience.adobe.com/marketo-measure **で「** Adobe IDでログイン [」オプションを選択することで、](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} インスタンスにアクセスできます。

![](assets/adobe-admin-console-setup-3.png)
