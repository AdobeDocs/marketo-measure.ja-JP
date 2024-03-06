---
unique-page-id: 37356030
description: E メールトラッキングパラメーター — [!DNL Marketo Measure]
title: メールトラッキングパラメーター
exl-id: e2cfd59e-ce4a-4cbb-b64a-828d1db7410f
feature: Tracking
source-git-commit: 4787f765348da71bc149c997470ce678ba498772
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 4%

---

# メールトラッキングパラメーター {#email-tracking-parameter}

The [!DNL Marketo Measure] 電子メールトラッキングパラメーターを使用すると、マーケターは電子メールのクリックをフォーム送信として処理し、それらのアクションに対してタッチポイントが生成されるようにできます。 電子メールトラッキングパラメーターを使用しない場合、電子メールからのクリックスルーは、フォーム送信または Web チャットを通じて実際にサイトに関与するまでは、「Web 訪問」としてのみ扱われます。

## ユースケース  {#use-cases}

**ウェビナー登録**：マーケティングチームは、ウェビナーに登録するための 1 つのボタン付きの電子メール招待を送信します。 E メールには既に人物の情報が含まれているので、シングルクリックで自動登録されます。 ランディングページには E メールトラッキングパラメーターが含まれているので、クリックスルーして確認ページに到達した場合に、 [!DNL Marketo Measure] では、電子メールアドレスを取り込み、クリックスルーをフォームの入力として扱うことができます。これにより、タッチポイントが生成されます。

**コンテンツのダウンロード**：コンテンツマーケティングチームは、電子メールから直接ダウンロードリンクを使用して公開した最近の eBook をプロモーションしたいと考えています。 E メールテンプレートを作成すると、ダウンロード確認ページには、クリックスルー時に E メールトラッキングパラメーターが含まれます。 [!DNL Marketo Measure] は電子メールアドレスをキャプチャできます。 サイト上のフォームに入力する必要はありません。 [!DNL Marketo Measure] は、コンテンツのダウンロード用のタッチポイントを生成できます。 これは、E メールが、E メールトラッキングパラメーターを使用して確認ページにランディングしたからです。

## 仕組み {#how-it-works}

訪問者がサイトに到達したとき、 [!DNL Marketo Measure] は、電子メールアドレスまたは [!DNL Salesforce] ID を使用して、その訪問を「フォーム送信」に関連付け、そのアクティビティのタッチポイントを生成できます。

顧客は、通常どおりに E メールテンプレートを作成します。 追跡するアクションのランディングページにを追加する場合は、各アクションの値を動的に表示するためにマーケティングオートメーションプラットフォームが受け入れるトークン、変数タグ、マクロを決定する必要があります。

Marketo Measureは、メールアドレス、Salesforce リード ID、Salesforce 連絡先 ID のいずれかの値を受け入れます。

## タグ例 {#tag-examples}

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
   <th><p>支持材</p></th> 
  </tr> 
  <tr> 
   <td><p>Marketo</p></td> 
   <td><p>{{lead.Email Address}} </p></td> 
   <td><p>https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId={{lead.EmailAddress}}</p></td> 
   <td><p>https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/personalizing-landing-pages/tokens-overview.html</p></td> 
  </tr> 
  <tr> 
   <td><p>Pardot</p></td> 
   <td><p>%%email%% </p><p>または</p><p>%%user_crm_id%%</p></td> 
   <td><p>https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId=%%email%%</p></td> 
   <td><p>https://help.salesforce.com/s/articleView?language=en_US&amp;id=pardot_variable_tags_reference.htm&amp;type=5</p></td> 
  </tr> 
  <tr> 
   <td><p>Hubspot</p></td> 
   <td><p>（エディターを使用して挿入）</p></td> 
   <td><p>該当なし</p></td> 
   <td><p>https://knowledge.hubspot.com/website-pages/personalize-your-content</p></td> 
  </tr> 
  <tr> 
   <td><p>Act-On</p></td> 
   <td><p>（Message Composer を使用して挿入）</p></td> 
   <td><p>該当なし</p></td> 
   <td><p>https://connect.act-on.com/hc/en-us/articles/360033436074-How-to-Personalize-Email-Content-with-CRM-Data</p></td> 
  </tr> 
 </tbody> 
</table>

最後に、内部で [!DNL Marketo Measure]に値を指定する場合は、トラッキングパラメーターを指定して、 [!DNL Marketo Measure] で電子メールまたは ID 値を見つけることができます。 デフォルトは、上の例と下のスクリーンショットに示すように、「mailId」です。 の設定に値を入力します。 [!DNL Marketo Measure]を選択し、次に **[!UICONTROL 保存]**.

![](assets/one.png)
