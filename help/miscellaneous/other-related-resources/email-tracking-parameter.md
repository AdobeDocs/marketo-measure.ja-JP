---
unique-page-id: 37356030
description: メールトラッキングパラメーター –  [!DNL Marketo Measure]
title: メールトラッキングパラメーター
exl-id: e2cfd59e-ce4a-4cbb-b64a-828d1db7410f
feature: Tracking
source-git-commit: 5a3494763c80ac636306c7ac8d080383d2358a59
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 7%

---

# メールトラッキングパラメーター {#email-tracking-parameter}

[!DNL Marketo Measure]電子メールトラッキングパラメーターを使用すると、マーケターは電子メールのクリックをフォーム送信として処理し、これらのアクションに対してタッチポイントを生成できます。 メールトラッキングパラメーターを使用しない場合、ユーザーがフォーム送信やweb チャットを通じて実際にサイトとエンゲージするまで、メールからのクリックスルーは「web訪問」としてのみ扱われます。

## ユースケース  {#use-cases}

**ウェビナー登録**: マーケティング部門は、ウェビナーに登録するためのボタンを1つ押すだけで、招待メールを送信します。 メールには既に相手の情報が含まれているため、シングルクリックで自動登録されます。 ランディングページには電子メール追跡パラメーターが含まれているため、クリックして確認ページにアクセスすると、[!DNL Marketo Measure]は電子メールアドレスを取得し、クリックをフォーム入力として扱い、タッチポイントを生成できます。

**コンテンツのダウンロード**: コンテンツマーケティング部門は、電子メールから直接ダウンロードリンクを使用して公開した最近の電子書籍を宣伝したいと考えています。 電子メールテンプレートが構築されると、ダウンロード確認ページに電子メールトラッキングパラメーターが含まれるため、クリックすると[!DNL Marketo Measure]が電子メールアドレスを取得できます。 サイトでフォームに入力しなくても、[!DNL Marketo Measure]はコンテンツのダウンロード用のタッチポイントを生成できます。 これは、電子メールがメールトラッキングパラメーターを使用して確認ページに表示されたためです。

## 仕組み {#how-it-works}

訪問者がサイトにアクセスすると、[!DNL Marketo Measure]はメールアドレスまたは[!DNL Salesforce] IDを持つランディングページを見つけることを期待します。これにより、その訪問を「フォーム送信」に関連付け、そのアクティビティのタッチポイントを生成できます。

顧客は、通常通りメールテンプレートを作成します。 追跡するアクションのランディングページに追加する準備が整ったら、各ユーザーの値を動的に表示するために、MA プラットフォームが受け入れるトークン、変数タグ、マクロのいずれかを決定する必要があります。

Marketo Measureでは、電子メールアドレス、Salesforce リード ID、またはSalesforce連絡先IDの値を使用できます。

## タグの例 {#tag-examples}

<table> 
 <colgroup> 
  <col> 
  <col> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th><p>マーケティングオートメーション</p></th> 
   <th><p>トークン/タグ/マクロ </p></th> 
   <th><p>例</p></th> 
   <th><p>支持材料</p></th> 
  </tr> 
  <tr> 
   <td><p>Marketo</p></td> 
   <td><p>'{{lead.Email Address}}' </p></td> 
   <td><p>https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId='{{'lead.EmailAddress'}'</p></td> 
   <td><p>https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/personalizing-landing-pages/tokens-overview.html?lang=ja</p></td> 
  </tr> 
  <tr> 
   <td><p>Pardot</p></td> 
   <td><p>%%email%% </p><p>または</p><p>%%user_crm_id%%</p></td> 
   <td><p>https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId=%%email%%</p></td> 
   <td><p>https://help.salesforce.com/s/articleView?language=en_US&amp;id=pardot_variable_tags_reference.htm&amp;type=5</p></td> 
  </tr> 
  <tr> 
   <td><p>Hubspot</p></td> 
   <td><p>（エディターを介して挿入）</p></td> 
   <td><p>該当なし</p></td> 
   <td><p>https://knowledge.hubspot.com/website-pages/personalize-your-content</p></td> 
  </tr> 
  <tr> 
   <td><p>アクションオン</p></td> 
   <td><p>（Message Composerを使用して挿入）</p></td> 
   <td><p>該当なし</p></td> 
   <td><p>https://connect.act-on.com/hc/en-us/articles/360033436074-How-to-Personalize-Email-Content-with-CRM-Data</p></td> 
  </tr> 
 </tbody> 
</table>

最後に、[!DNL Marketo Measure]内でトラッキングパラメーターを指定して、[!DNL Marketo Measure]が電子メールまたはIdの値を見つけられるようにする必要があります。 上記の例と以下のスクリーンショットに示すように、デフォルトは「mailId」です。 値を[!DNL Marketo Measure]の設定に入力し、**[!UICONTROL 保存]**&#x200B;をクリックします。

![](assets/one.png)
