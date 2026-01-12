---
description: シングルサインオン -  [!DNL Marketo Measure]
title: シングルサインオン
exl-id: a328e9cb-8352-4693-8a44-533e08f1a29c
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 93%

---


# シングルサインオン {#single-sign-on}

SSO（シングルサインオン）の SAML（Security Assertion Markup Language）により、ユーザは [!DNL Marketo Measure] アプリにログインする際に会社の ID プロバイダーを通じて認証できます。SSO を使用すると、ユーザは一度認証するだけで、個別のアプリを認証する必要がなくなります。すべてのユーザが組織内に [!DNL Salesforce] または [!DNL Google] アカウントを持っているとは限りません。そのため、SAML はエンタープライズのお客様にとって必須です。規模を拡大するために、[!DNL Marketo Measure] は会社 ID プロバイダーをサポートできる SAML ソリューションを開発しました。

>[!NOTE]
>企業が異なる ID プロバイダー（例えば、Ping ID、Okta）を使用している可能性があります。 以下の設定手順および UI で使用される用語は、ID プロバイダーで使用される用語と直接一致しない場合があります。

## 要件 {#requirements}

* [!DNL Marketo Measure] アプリの AccountAdmin 権限を持つユーザ
* お客様の ID プロバイダーへの管理アクセス権を持つユーザ

## はじめに {#getting-started}

はじめに、[!DNL Marketo Measure] アプリケーションの設定／セキュリティ／認証ページに移動します。次に、ログインタイプをカスタム SSO に切り替えて、設定オプションを確認します。認証をテストし、ページの下部にある「**[!UICONTROL 保存]**」ボタンをクリックするまで、変更は有効になりません。

![ カスタム SSO ログインタイプオプションを使用した認証設定ページ ](assets/single-sign-on-1.png)

## 処理 {#process}

[!DNL Marketo Measure] シングルサインオンでは、[!DNL Marketo Measure] アカウントからロックアウトされる危険を回避するために、一連の手順で認証設定を行う必要があります。

ID プロバイダーで [!DNL Marketo Measure] アプリケーションを設定します。手順については、以下にリストされている外部ドキュメントを参照してください。

    a. シングルサインオン URL、受信者 URL、宛先 URL、SAML Assertion Customer Service（ACS）URL の入力を求めるプロンプトが表示されたら、[https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest]（https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest）を使用します
    
    b. オーディエンス制限 URL またはアプリケーション定義の一意の識別子の入力を求めるプロンプトが表示されたら、[https://BizibleLPM]（https://biziblelpm/）を使用します

[!DNL Marketo Measure] アプリケーションでカスタム SSO に切り替えます

    a. アカウントに対して請求先グループが有効になると、[!UICONTROL 設定]／[!UICONTROL セキュリティ]／[!UICONTROL 認証]
    
    に移動できます。b. デフォルトでは、ログインタイプは「CRM ユーザ」に設定されます
    
    c. ログインタイプを「カスタム SSO」に切り替えて、設定プロセスを開始します。

ID プロバイダー設定の接続設定を入力します

    a. ID プロバイダーは、必要な設定フィールドを抽出する IdP メタデータ .xml ドキュメントを提供する可能性があります。.xml ドキュメントのコンテンツを読み込むか、ID プロバイダーの設定プロセス中に取得した出力から以下の 3 つのフィールドに入力します。**両方を行う必要はありません。**
    
    i. IdP URL： [!DNL Marketo Measure]  アプリケーションでユーザーを認証するために、 [!DNL Marketo Measure]  が示す必要がある URL。「リダイレクト URL」と呼ばれることもあります。
    ii.IdP 発行者：ID プロバイダーの一意の ID。「外部キー」と呼ばれることもあります。
    iii.IdP 証明書： [!DNL Marketo Measure]  がすべての ID プロバイダーの応答の署名を検証および検証できる公開鍵。

ユーザのトークンの有効期限を分単位で設定します。

    a.  [!DNL Marketo Measure]  には、1～1440 分の整数を指定できます。ユーザのセッション時間が経過すると、新しいページに移動したユーザはログオフされます。

ユーザ属性設定を行って、それぞれの名、姓、メールアドレスにマッピングします。

    a. SAML 属性を入力すると、 [!DNL Marketo Measure]  は渡された情報によってユーザを認識できます。
    
    i. メール属性：ID プロバイダーがユーザのメールアドレスに使用する属性名を指定します。
    ii.名属性：ID プロバイダーがユーザの名に使用する属性名を指定します。
    iii.姓属性：ID プロバイダーがユーザの姓に使用する属性名を指定します。
    
    b. ヒント：ここで SAML 設定をテストすると、このセクションで使用できるメール、名、姓の属性の解析が行われます。

![ ユーザー属性マッピングフィールドを含む SAML 設定フォーム ](assets/single-sign-on-2.png)

ユーザロール設定を行って、IdP から分類されたそれぞれのロールまたはグループにマッピングします。

    a. お客様は、ID プロバイダーで定義されたグループに基づいて  [!DNL Marketo Measure]  ユーザロールを割り当てることができます。SAML 属性を入力すると、 [!DNL Marketo Measure]  はユーザのロールとグループを  [!DNL Marketo Measure]  のユーザ権限にマッピングできます。 [!DNL Marketo Measure]  管理者がアカウントを更新するための十分な権限を持てるように、これらのロールを設定することを強くお勧めします。
    
    b. ロールまたはグループがマッピングされていない場合、デフォルト設定では、ID プロバイダーのすべての従業員に標準ユーザアクセス権があります。
    
    i.  [!DNL Marketo Measure] 標準ユーザ：  [!DNL Marketo Measure]  アプリケーションへの読み取り専用アクセス権が必要なユーザに、（SSO プロバイダーからの）ロールまたはグループの値を指定します。
    ii. [!DNL Marketo Measure] アカウント管理者ユーザ：  [!DNL Marketo Measure]  アプリケーションへの管理アクセス権が必要なユーザに、（SSO プロバイダーからの）ロールまたはグループの値を指定します。つまり、ロールには、アカウントに関連する設定を変更するアクセス権があります。
    iii.IdP には、「Bizible 標準ユーザ」または「Bizible アカウント管理ユーザ」属性に入力した値を格納する「グループ」の正確な名前を持つ属性が必要です。
    
    c. 複数のロールまたはグループを 1 つのロールにマッピングする必要がある場合は、各値をコンマで区切って入力します。

![ 「標準のユーザー」オプションと「管理者」オプションを使用したユーザーロールマッピング設定 ](assets/single-sign-on-3.png)

シングルサインオン設定をテストします

    a.「保存」をクリックする前に、「[!UICONTROL SAML 認証をテスト]」ボタンをクリックして、設定が正しく行われていることを確認する必要があります。
    
    b.「失敗」エラーが表示された場合は、メッセージに従って、もう一度試してください。

![ 「SAML 認証をテスト」ボタンと検証ステータスメッセージ ](assets/single-sign-on-4.png)

設定を保存し、新しいカスタムサインイン URL で[!UICONTROL シングルサインオン]を使用するよう同僚に指示します。

    a. 重要：新しい認証設定を保存すると、CRM ユーザによるログインが無効になり、カスタム SSO が有効になっているので、新しいページに移動するとセッションが終了する可能性があります。

![ 認証設定と確認メッセージの「保存」ボタン ](assets/single-sign-on-5.png)

お試しください。

    a. 新しいカスタムサインイン URL を使用し、ID プロバイダーの資格情報で  [!DNL Marketo Measure]  アプリケーションへのログインを試みます。
    
    b. 形式は「https://apps.adobe.com/business/[accountName]」のようになります。
    
    c. おめでとうございます。アカウントの  [!DNL Marketo Measure]  アプリケーションでシングルサインオンが正常に設定されました。

![ 成功した SSO ログイン確認画面 ](assets/single-sign-on-6.png)

>[!NOTE]
>SSO を設定した後は、[!DNL Marketo Measure] アプリケーション内にユーザを追加する必要はなくなります。ユーザプロビジョニングは、ID プロバイダー内で直接処理する必要があります。

## CRM ユーザ（詳細設定） {#crm-users-advanced-setup}

デフォルトでは、すべてのアカウントは CRM 資格情報を使用して [!DNL Marketo Measure] アプリケーションにアクセスできます。場合によっては、アカウント所有者はアクセスを特定のロールに制限し、アクティブな CRM ライセンスを持つすべてのユーザにはアクセスを公開しない必要があります。詳細設定を使用すると、CRM のロールとグループを [!DNL Marketo Measure] ユーザー権限にマッピングできます。

ロールまたはグループをマッピングしていない場合、デフォルト設定では、CRM 内のすべてのアクティブなライセンスに標準ユーザアクセス権が付与されます。

* [!DNL Marketo Measure] 標準ユーザ：[!DNL Marketo Measure] アプリケーションへの読み取り専用アクセス権が必要なユーザにロールまたはグループの値を指定します。
* [!DNL Marketo Measure] アカウント管理ユーザ：[!DNL Marketo Measure] アプリケーションへの管理アクセス権が必要なユーザにロールまたはグループの値を指定します。つまり、ロールには、アカウントに関連する設定を変更するアクセス権があります。

複数のロールまたはグループを 1 つのロールにマッピングする必要がある場合は、各値をコンマで区切って入力します。

**Salesforce ロール**

[!DNL Salesforce] ロールには、各ロールの名前を使用します。すべてのロールは、[!UICONTROL 設定]／[!UICONTROL ユーザを管理]／[!UICONTROL ロール]メニューにあります。

![ ユーザーを管理の下の役割を示すSalesforce設定メニュー ](assets/6.png)

**Dynamics ロール**

[!DNL Dynamics] ロールには、各セキュリティロールの名前を使用します。すべてのセキュリティロールは、[!UICONTROL 設定]／[!UICONTROL セキュリティ]／[!UICONTROL セキュリティロール]メニューにあります。

![ セキュリティ ロールへの Dynamics 設定メニューのナビゲーション ](assets/7.png)

![ 使用可能な役割オプションを示す Dynamics セキュリティーロールリスト ](assets/8.png)

**Google ユーザ**

カスタム SSO を設定すると、[!UICONTROL ユーザ]ページが更新され、Google ログインで追加した外部ユーザのみが表示されます。アクセス権を持つすべてのユーザは SSO 設定を通じて定義されるので、追加の外部ユーザがここにリストされます。

![ 外部のGoogle ログインユーザーを表示するユーザーページ ](assets/9.png)

有効な [!DNL Google] アカウントのみを追加でき、ユーザロールを定義する必要があります。

## 外部リンク {#external-links}

* [Okta](https://developer.okta.com/standards/SAML/setting_up_a_saml_application_in_okta)
* [Ping Identity](https://docs.pingidentity.com:443/bundle/p1_enterpriseConfigSsoSaml_cas/page/enableAppWithoutURL.html)
* [OneLogin](https://onelogin.service-now.com/support?id=kb_article&sys_id=b2c91143db109700d5505eea4b9619d5)
* [Active Directory](https://docs.microsoft.com/ja-jp/azure/active-directory/active-directory-saas-custom-apps)
