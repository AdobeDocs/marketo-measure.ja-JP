---
unique-page-id: 18874761
description: シングルサインオン — [!DNL Marketo Measure]
title: シングルサインオン
exl-id: a328e9cb-8352-4693-8a44-533e08f1a29c
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 1%

---

# シングルサインオン {#single-sign-on}

SSO（シングルサインオン）用の SAML（セキュリティアサーションマークアップ言語）を使用すると、ユーザーがログイン時に会社の ID プロバイダーを通じて認証できます。 [!DNL Marketo Measure] アプリを使用します。 SSO を使用すると、別々のアプリを認証する必要なく、ユーザーが 1 回認証できます。 すべてのユーザーが [!DNL Salesforce] または [!DNL Google] 組織内のアカウント。 拡大・縮小するには [!DNL Marketo Measure] は、会社の ID プロバイダーをサポートする SAML ソリューションを開発しました。

>[!CAUTION]
>
>この記事では、シングルサインオン (SSO) と高度な CRM ユーザー管理の概要を説明します。 アカウントがプロビジョニングされている場合 **9/10/2020以降**&#x200B;では、この記事は無視してください。SSO とIdentity Managementは [Adobe Admin Console [!DNL Marketo Measure] 統合](/help/configuration-and-setup/getting-started-with-marketo-measure/marketo-measure-quick-start.md).

>[!NOTE]
>
>会社が異なる ID プロバイダー（Ping ID、Okta など）を使用している可能性が高くなります。 以下の設定手順および UI で使用される用語が、ID プロバイダーで使用される用語と直接一致しない場合があります。

## 要件 {#requirements}

* で AccountAdmin 権限を持つユーザー [!DNL Marketo Measure] アプリ
* 顧客の ID プロバイダーへの管理者アクセス権を持つユーザー

## はじめに {#getting-started}

利用を開始するには、次の URL で、設定/セキュリティ/認証ページに移動します。 [!DNL Marketo Measure] アプリケーション。 次に、ログインの種類をカスタム SSO に切り替えて、設定オプションを確認します。 変更は、認証をテストし、 **[!UICONTROL 保存]** 」ボタンをクリックします。

![](assets/single-sign-on-1.png)

## 処理 {#process}

[!DNL Marketo Measure] シングルサインオンでは、一連の手順で認証設定を構成し、ロックアウトされるリスクを回避する必要があります。 [!DNL Marketo Measure] アカウント。

を設定します。 [!DNL Marketo Measure] ID プロバイダー内のアプリケーション。 手順については、以下に示す外部ドキュメントを参照してください。

    a.シングルサインオン URL、受信者 URL、または宛先 URL、SAML アサーションカスタマーサービス (ACS)URL の入力を求められたら、[https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest](https://apps.bizible.com/BizibleSAML2/ReceiveSSORequest) を使用します。
    
    b.オーディエンス制限 URL またはアプリケーション定義の一意の ID の入力を求められたら、[https://BizibleLPM](https://biziblelpm/) を使用します。

でカスタム SSO に切り替えます。 [!DNL Marketo Measure] アプリ

    a.アカウントに対して請求グループが有効になると、次のリンクからアクセスできるようになります。 [!UICONTROL 設定] >>[!UICONTROL セキュリティ] >> [!UICONTROL 認証]
    
    b.デフォルトでは、「ログインタイプ」は「CRM ユーザー」に設定されます。
    
    c.設定プロセスを開始するには、ログインタイプを「Custom SSO」に切り替えます。

ID プロバイダー構成の接続設定を入力します

    a. ID プロバイダーが IdP メタデータ.xml ドキュメントを提供し、必須の設定フィールドを取り出す場合があります。 .xml 文書のコンテンツを読み込むか、ID プロバイダの構成プロセス中に取得した出力から以下の 3 つのフィールドを入力します。 **両方を完了する必要はありません。**
    
    i. IdP URL: [!DNL Marketo Measure] ユーザーを認証するために、を示す必要があります。 [!DNL Marketo Measure] アプリケーション。 「リダイレクト URL」とも呼ばれます。
    2. IdP Issuer: ID プロバイダーの一意の ID。 「外部キー」とも呼ばれます。
    3. IdP 証明書：許可する公開鍵 [!DNL Marketo Measure] ：すべての ID プロバイダー応答の署名を検証および検証します。

ユーザーのトークンの有効期限を分単位で設定します。

    a. [!DNL Marketo Measure] では、1 ～ 1440 分の整数を使用できます。 ユーザーのセッション時間を超えると、新しいページに移動したユーザーはログオフされます。

を設定し、ユーザー属性設定を、それぞれの名、姓、電子メールアドレスにマッピングします。

    a. SAML 属性を入力する。 [!DNL Marketo Measure] は、通過した情報によってユーザーを認識できます。
    
    i.電子メール属性： ID プロバイダーがユーザーの電子メールアドレスに使用する属性名を指定します。
    2. First Name Attribute: ID プロバイダがユーザーの名として使用する属性名を指定します。
    3. 姓属性： ID プロバイダーがユーザーの姓に使用する属性名を指定します。
    
    b.ヒント：SAML 設定を今すぐテストする場合、このセクションで使用できる E メール、名、姓の属性が解析されます。

![](assets/single-sign-on-2.png)

を設定し、IdP から分類された各役割またはグループに、ユーザーの役割の設定をマッピングします。

    a.お客様は、 [!DNL Marketo Measure] ID プロバイダーで定義されたグループに基づくユーザーの役割。 SAML 属性を入力する。 [!DNL Marketo Measure] ユーザーの役割およびグループを [!DNL Marketo Measure] ユーザー権限。 これらの役割を設定して、 [!DNL Marketo Measure] 管理者は、アカウントを更新するのに十分な権限を持っています。
    
    b.ロールまたはグループがマッピングされていない場合、デフォルト設定では、ID プロバイダーのすべての従業員が標準ユーザーアクセス権を持ちます。
    
    i. [!DNL Marketo Measure] 標準ユーザー： （SSO プロバイダーから） [!DNL Marketo Measure] アプリケーション。
    2. [!DNL Marketo Measure] アカウント管理者ユーザー： （SSO プロバイダーから） [!DNL Marketo Measure] アプリケーション。 これは、お使いのアカウントに関連する設定を変更する権限をロールが持つことを意味します。
    3. IdP には、「Bizible Standard User」属性または「Bizible Account Admin User」属性に入力した値を格納する「グループ」の正確な名前を持つ属性が必要です。
    
    c.複数の役割またはグループを 1 つの役割にマッピングする場合は、各値をコンマで区切って入力します。

![](assets/single-sign-on-3.png)

シングルサインオン設定のテスト

    a. 「保存」をクリックする前に、 [!UICONTROL SAML 認証のテスト] 」ボタンをクリックして、設定が正しく設定されていることを確認します。
    
    b. 「failure」エラーが表示された場合は、メッセージに従って、もう一度試してください。

![](assets/single-sign-on-4.png)

設定を保存し、同僚に使用を促す [!UICONTROL シングルサインオン] 新しいカスタムログイン URL を使用します。

    a.重要：新しい認証設定を保存すると、CRM ユーザーによるログインを無効にし、カスタム SSO を有効にしたので、新しいページに移動するとセッションが終了する可能性があります。

![](assets/single-sign-on-5.png)

お試しください。

    a.新しいカスタムログイン URL を使用して、に再度ログインしようとします。 [!DNL Marketo Measure] ID プロバイダーの資格情報を持つアプリケーション。
    
    b.形式は「https://apps.adobe.com/business/[accountName]」のようになります。
    
    c.おめでとうございます。 シングルサインオンを [!DNL Marketo Measure] アカウントの申請

![](assets/single-sign-on-6.png)

>[!NOTE]
>
>SSO を設定した後は、 [!DNL Marketo Measure] アプリケーション。 ユーザープロビジョニングは、ID プロバイダー内で直接処理する必要があります。

## CRM ユーザ（詳細設定） {#crm-users-advanced-setup}

デフォルトでは、すべてのアカウントが [!DNL Marketo Measure] CRM 資格情報を使用するアプリケーション。 アカウント所有者が、アクティブな CRM ライセンスを持つすべてのユーザーに対して、アクセスを特定の役割に制限し、開かないようにする必要が生じる場合があります。 詳細設定を使用すると、CRM の役割とグループをにマッピングできます。 [!DNL Marketo Measure] ユーザー権限。

ロールまたはグループがマッピングされていない場合、デフォルト設定では、CRM 内のすべてのアクティブなライセンスに標準ユーザーアクセス権が付与されます。

* [!DNL Marketo Measure] Standard User：に対する読み取り専用アクセス権を持つユーザーの役割またはグループ値を指定します。 [!DNL Marketo Measure] アプリケーション。
* [!DNL Marketo Measure] アカウント管理者ユーザー： [!DNL Marketo Measure] アプリケーション。 これは、お使いのアカウントに関連する設定を変更する権限をロールが持つことを意味します。

複数の役割またはグループを 1 つの役割にマッピングする場合は、各値をコンマで区切って入力します。

**Salesforce ロール**

の場合 [!DNL Salesforce] 「役割」では、各役割の名前を使用します。 すべての役割は、 [!UICONTROL 設定] >[!UICONTROL ユーザーを管理] >[!UICONTROL 役割] メニュー。

![](assets/6.png)

**Dynamics の役割**

の場合 [!DNL Dynamics] 役割、各セキュリティ役割の名前を使用します。 すべてのセキュリティロールは、 [!UICONTROL 設定] >[!UICONTROL セキュリティ] >[!UICONTROL セキュリティロール] メニュー。

![](assets/7.png)

![](assets/8.png)

**Google Users**

カスタム SSO が設定されると、 [!UICONTROL ユーザー] ページが更新され、Googleのログインで追加された外部ユーザーのみが表示されるようになりました。 アクセス権を持つすべてのユーザーは SSO 設定を通じて定義されるので、追加の外部ユーザーをここに示します。

![](assets/9.png)

有効なのはのみ [!DNL Google] アカウントを追加でき、ユーザーロールを定義する必要があります。

## 外部リンク {#external-links}

* [Okta](https://developer.okta.com/standards/SAML/setting_up_a_saml_application_in_okta)
* [Ping ID](https://docs.pingidentity.com:443/bundle/p1_enterpriseConfigSsoSaml_cas/page/enableAppWithoutURL.html)
* [OneLogin](https://onelogin.service-now.com/support?id=kb_article&amp;sys_id=b2c91143db109700d5505eea4b9619d5)
* [Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-custom-apps)
