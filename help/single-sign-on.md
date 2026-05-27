---
description: Marketo Measure ユーザー向けのシングルサインオンガイダンス
title: シングルサインオン
exl-id: a328e9cb-8352-4693-8a44-533e08f1a29c
source-git-commit: 7a4661c8d42214d32e5360dc45d6d880b08ef37c
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 54%

---

# シングルサインオン {#single-sign-on}

SSO（シングルサインオン）の SAML（Security Assertion Markup Language）により、ユーザは [!DNL Marketo Measure] アプリにログインする際に会社の ID プロバイダーを通じて認証できます。 SSO を使用すると、ユーザは一度認証するだけで、個別のアプリを認証する必要がなくなります。 すべてのユーザが組織内に [!DNL Salesforce] または [!DNL Google] アカウントを持っているとは限りません。そのため、SAML はエンタープライズのお客様にとって必須です。 規模を拡大するために、[!DNL Marketo Measure] は会社 ID プロバイダーをサポートできる SAML ソリューションを開発しました。

>[!CAUTION]
>
>この記事では、シングルサインオン（SSO）と高度な CRM ユーザ管理について説明します。 アカウントを **2020年9月10日（PT）以降**&#x200B;にプロビジョニングした場合は、SSO と ID 管理が [&#x200B; [!DNL Marketo Measure]  統合のために Adobe Admin Console](/help/implementation-guide.md) 内で設定されるので、この記事は無視してください。

>[!NOTE]
>
>会社は様々な ID プロバイダー（Ping Identity、Okta など）を使用している可能性があります。 以下の設定手順および UI で使用される用語は、ID プロバイダーで使用される用語と直接一致しない場合があります。

## 要件 {#requirements}

* [!DNL Marketo Measure] アプリの AccountAdmin 権限を持つユーザ
* お客様の ID プロバイダーへの管理アクセス権を持つユーザ

## はじめに {#getting-started}

はじめに、[!DNL Marketo Measure] アプリケーションの設定／セキュリティ／認証ページに移動します。 次に、ログインタイプをカスタム SSO に切り替えて、設定オプションを確認します。 認証をテストし、ページの下部にある「**[!UICONTROL 保存]**」ボタンをクリックするまで、変更は有効になりません。

![開始するには、](assets/compliance-resources-1.png)の設定セキュリティ認証ページに移動します

## 処理 {#process}

[!DNL Marketo Measure] シングルサインオンでは、[!DNL Marketo Measure] アカウントからロックアウトされる危険を回避するために、一連の手順で認証設定を行う必要があります。

ID プロバイダーで [!DNL Marketo Measure] アプリケーションを設定します。 手順については、以下にリストされている外部ドキュメントを参照してください。

    a. シングルサインオン URL、受信者URLまたは宛先URL、SAML アサーションカスタマーサービス （ACS） URLの入力を求められた場合は、[https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest] （https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest） 
    
    bを使用します。 オーディエンス制限URLまたはアプリケーション定義の一意の識別子の入力を求められたら、[https://BizibleLPM] （https://biziblelpm/） 
を使用します
[!DNL Marketo Measure] アプリケーションでカスタム SSO に切り替えます

    a. 請求グループがアカウントに対して有効になると、[!UICONTROL 設定] >>[!UICONTROL &#x200B; セキュリティ &#x200B;] >> [!UICONTROL 認証]
    
    bに移動できるようになります。 デフォルトでは、ログインタイプは「CRM ユーザー」に設定されます。
    
    c. ログインタイプを「カスタム SSO」に切り替えて、設定プロセスを開始します。

ID プロバイダー設定の接続設定を入力します

    a. ID プロバイダーは、必須の設定フィールドを引き出すIdP メタデータ .xml ドキュメントを提供する場合があります。 .xml ドキュメントのコンテンツを読み込むか、ID プロバイダーの設定プロセス中に取得した出力から以下の 3 つのフィールドに入力します。 **&#x200B; 両方を完了する必要はありません。**
    
    i。 IdP URL: ユーザーを [!DNL Marketo Measure]  アプリケーションに認証するために [!DNL Marketo Measure] が指定する必要があるURL。 「リダイレクト URL」と呼ばれることもあります。
    ii。 IdP 発行者：ID プロバイダーの一意の ID。 「外部キー」と呼ばれることもあります。
    iii. IdP 証明書： [!DNL Marketo Measure]  がすべての ID プロバイダーの応答の署名を検証および検証できる公開鍵。

ユーザのトークンの有効期限を分単位で設定します。

    a.  [!DNL Marketo Measure]  には、1～1440 分の整数を指定できます。 ユーザのセッション時間が経過すると、新しいページに移動したユーザはログオフされます。

ユーザ属性設定を行って、それぞれの名、姓、メールアドレスにマッピングします。

    a. SAML属性を入力すると、 [!DNL Marketo Measure] は渡された情報によってユーザーを認識できます。
    
    i. メール属性：ID プロバイダーがユーザーの電子メールアドレスに使用する属性名を指定します。
    ii. 名の属性：ID プロバイダーがユーザーの名に使用する属性名を指定します。
    iii. 姓の属性：ID プロバイダーがユーザーの姓に使用する属性名を指定します。
    
    b. ヒント：SAML設定を今すぐテストすると、このセクションで使用できるEmail、First Name、Last Name属性が解析されます。

![b. ヒント：SAML設定を今すぐテストすると、](assets/discover-control-1.png)を解析します

ユーザロール設定を行って、IdP から分類されたそれぞれのロールまたはグループにマッピングします。

    a. お客様には、ID プロバイダーで定義されたグループに基づいて [!DNL Marketo Measure]  ユーザーの役割を割り当てるオプションがあります。 SAML 属性を入力すると、 [!DNL Marketo Measure]  はユーザのロールとグループを  [!DNL Marketo Measure]  のユーザ権限にマッピングできます。 アカウントを更新するのに十分な権限を [!DNL Marketo Measure] 管理者が持つように、これらの役割を設定することを強くお勧めします。
    
    b. 役割またはグループがマッピングされていない場合、デフォルト設定は、ID プロバイダーのすべての従業員が標準ユーザーアクセス権を持つことです。
    
    i. [!DNL Marketo Measure] 標準ユーザー： [!DNL Marketo Measure]  アプリケーションへの読み取り専用アクセス権を持つ必要があるユーザーに対して（SSO プロバイダーから）役割またはグループの値を提供します。
    ii. [!DNL Marketo Measure]  アカウント管理者ユーザー： [!DNL Marketo Measure]  アプリケーションへの管理アクセス権を持つユーザーに（SSO プロバイダーから）役割提供します。 つまり、役割は、アカウントに関連する設定や設定を変更するためのアクセス権を持っています。
    iii. 「Bizible Standard User」または「Bizible Account Admin User」属性に入力した値を格納する「groups」の正確な名前を持つIdPの属性が必要です。
    
    c. 複数の役割またはグループを役割にマッピングする場合は、各値をコンマで区切って入力します。

![c。 複数の役割またはグループを1つの役割にマッピングする必要がある場合、](assets/discover-control-2.png)

シングルサインオン設定をテストします

    a. 「保存」をクリックする前に、「[!UICONTROL SAML認証をテスト &#x200B;]」ボタンをクリックして、設定が正しく設定されていることを確認する必要があります。
    
    b. 「失敗」エラーが表示された場合は、メッセージに従って再試行してください。

![b. 「失敗」エラーが表示された場合は、メッセージに従って試行してください](assets/discover-control-3.png)

設定を保存し、新しいカスタムサインイン URL で[!UICONTROL シングルサインオン]を使用するよう同僚に指示します。

    a. 重要：新しい認証設定を保存すると、CRM ユーザーによるログインを無効にし、カスタム SSOを有効にしているため、新しいページに移動するとセッションが終了する可能性があります。

![a. 重要：新しい認証設定を保存すると、次のことが可能になります。](assets/discover-control-3.png)

お試しください。

    a. 新しいカスタム サインイン URLを使用し、ID プロバイダーの資格情報を使用して [!DNL Marketo Measure]  アプリケーションに再度ログインしてみてください。
    
    b. 形式は、「https://apps.adobe.com/business/[accountName]&#39;
    
    c」のようになります。 これで完了です。 アカウントの  [!DNL Marketo Measure]  アプリケーションでシングルサインオンが正常に設定されました。

![c。 これで完了です。 シングル サインオンを](assets/discover-control-3.png)に正常に設定しました

>[!NOTE]
>
>SSO を設定した後は、[!DNL Marketo Measure] アプリケーション内にユーザを追加する必要はなくなります。 ユーザプロビジョニングは、ID プロバイダー内で直接処理する必要があります。

## CRM ユーザ（詳細設定） {#crm-users-advanced-setup}

デフォルトでは、すべてのアカウントは CRM 資格情報を使用して [!DNL Marketo Measure] アプリケーションにアクセスできます。 場合によっては、アカウント所有者はアクセスを特定のロールに制限し、アクティブな CRM ライセンスを持つすべてのユーザにはアクセスを公開しない必要があります。 詳細設定を使用すると、CRM のロールとグループを [!DNL Marketo Measure] ユーザー権限にマッピングできます。

ロールまたはグループをマッピングしていない場合、デフォルト設定では、CRM 内のすべてのアクティブなライセンスに標準ユーザアクセス権が付与されます。

* [!DNL Marketo Measure] 標準ユーザ：[!DNL Marketo Measure] アプリケーションへの読み取り専用アクセス権が必要なユーザにロールまたはグループの値を指定します。
* [!DNL Marketo Measure] アカウント管理ユーザ：[!DNL Marketo Measure] アプリケーションへの管理アクセス権が必要なユーザにロールまたはグループの値を指定します。 つまり、ロールには、アカウントに関連する設定を変更するアクセス権があります。

複数のロールまたはグループを 1 つのロールにマッピングする必要がある場合は、各値をコンマで区切って入力します。

**Salesforce ロール**

[!DNL Salesforce] ロールには、各ロールの名前を使用します。 すべてのロールは、[!UICONTROL 設定]／[!UICONTROL ユーザを管理]／[!UICONTROL ロール]メニューにあります。

![Salesforce ロールの場合は、各ロールの名前を使用します。 すべての役割](assets/discover-control-3.png)

**Dynamics ロール**

[!DNL Dynamics] ロールには、各セキュリティロールの名前を使用します。 すべてのセキュリティロールは、[!UICONTROL 設定]／[!UICONTROL セキュリティ]／[!UICONTROL セキュリティロール]メニューにあります。

![Dynamics ロールの場合は、各セキュリティ ロールの名前を使用します。 すべて](assets/discover-control-3.png)

![Dynamics ロールの場合は、各セキュリティ ロールの名前を使用します。 すべて](assets/discover-control-3.png)

**Google ユーザ**

カスタム SSO を設定すると、[!UICONTROL ユーザ]ページが更新され、Google ログインで追加した外部ユーザのみが表示されます。 アクセス権を持つすべてのユーザは SSO 設定を通じて定義されるので、追加の外部ユーザがここにリストされます。

![&#x200B; カスタム SSOを設定すると、ユーザーページは](assets/discover-control-3.png)になります

有効な [!DNL Google] アカウントのみを追加でき、ユーザロールを定義する必要があります。

## 外部リンク {#external-links}

* [Okta](https://developer.okta.com/standards/SAML/setting_up_a_saml_application_in_okta)
* [Ping Identity](https://docs.pingidentity.com:443/bundle/p1_enterpriseConfigSsoSaml_cas/page/enableAppWithoutURL.html)
* [OneLogin](https://onelogin.service-now.com/support?id=kb_article&sys_id=b2c91143db109700d5505eea4b9619d5)
* [Active Directory](https://docs.microsoft.com/ja-jp/azure/active-directory/active-directory-saas-custom-apps)
