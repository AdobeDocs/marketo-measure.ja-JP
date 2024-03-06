---
description: Adobe Admin Console の設定 - Marketo Measure - 製品ドキュメント
title: Adobe Admin Console の設定
feature: Installation
exl-id: f9edacae-79e0-408c-ac37-bbe67c185f2d
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 34%

---

# Adobe Admin Console の設定 {#adobe-admin-console-setup}

を使用する最初の手順 [!DNL Marketo Measure] は、プロビジョニングされたAdobe Admin Consoleを作成してログインするためのものです。 ログイン手順が記載された電子メールを受け取っていない場合は、 [!DNL Marketo Measure] アカウント担当者。

## Adobe Admin Console と ID プロバイダーの設定 {#set-up-your-adobe-admin-console-and-identity-provider}

製品としてのAdobeスイート [!DNL Marketo Measure] は、 Adobe Admin Console for Identity Managementのすべての機能を使用します。 その他のリソースは、[こちらを参照](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)してください。

使用可能なリソース、ベストプラクティスおよびオプションを確認することをお勧めします。 [Identity Management](https://helpx.adobe.com/enterprise/using/set-up-identity.html).

Adobe Admin Console内でのIdentity Managementの設定に関するガイダンスと確認については、 [!DNL Marketo Measure] アカウント担当者。

ユーザーの認証および承認を容易にするために、 [!DNL Marketo Measure] インスタンスの場合、Adobe Admin Console内では次の手順が必要です。

**[!DNL Marketo Measure] 製品カードの設定**

Adobe Admin Consoleにアクセスすると、 [!DNL Marketo Measure] 「概要」セクションにある製品インスタンス。

![](assets/adobe-admin-console-setup-1.png)

クリック [!DNL Marketo Measure] 製品カードには、 [!DNL Marketo Measure] インスタンス。 デフォルトでは、各 [!DNL Marketo Measure] インスタンスには「[!DNL Marketo Measure]」というプレフィックスが付いた独自のプロファイルがあります。このインスタンス内のこのプロファイルや他のプロファイルに追加された管理者またはユーザは、[!DNL Marketo Measure] にログインできるようになります。

![](assets/adobe-admin-console-setup-2.png)

内でプロファイルを作成する際に必要なアクションはありません。 [!DNL Marketo Measure] 製品インスタンス。

次の手順で、アクセス可能なユーザーの追加を開始します： [!DNL Marketo Measure]（を参照） [追加中 [!DNL Marketo Measure] 管理者と [!DNL Marketo Measure] ユーザー](#adding-marketo-measure-admins-and-marketo-measure-users) 」の節を参照してください。

## [!DNL Marketo Measure] 管理者と [!DNL Marketo Measure] ユーザの追加 {#adding-marketo-measure-admins-and-marketo-measure-users}

次の手順では、ユーザを追加して [!DNL Marketo Measure] アプリケーションへのアクセスを付与します。これは、[!DNL Marketo Measure] 製品カードの管理者およびユーザディレクトリで実行できます。

| ユーザタイプ | 説明 |
|---|---|
| 管理者 | これらは、[!DNL Marketo Measure] 固有の設定オプションを更新および管理する完全な機能を持つ、[!DNL Marketo Measure] アプリケーションの管理者およびパワーユーザです。 |
| ユーザ | これらは、 [!DNL Marketo Measure] 内の読み取り専用権限を持つアプリケーション [!DNL Marketo Measure] アプリ |

ユーザーを各グループに追加すると、そのユーザーの [リストされた ID タイプ](https://helpx.adobe.com/enterprise/using/set-up-identity.html).

>[!NOTE]
>
>次の条件を満たす [!DNL Marketo Measure] 管理者 ( [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}) の場合、ユーザーはユーザーとして追加する必要があります _および_ 管理者 [!DNL Marketo Measure] 内の製品プロファイル [!DNL Marketo Measure] 製品カード。

**[!DNL Marketo Measure]** へのログイン

製品プロファイルにユーザーを追加すると、そのユーザーは [!DNL Marketo Measure] インスタンスを選択 **Adobe IDでログイン** オプション： [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}.

![](assets/adobe-admin-console-setup-3.png)
