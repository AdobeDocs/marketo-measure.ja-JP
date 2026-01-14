---
description: Marketo Measure ユーザー向けのメールトラッキングパラメーターガイダンス
title: メールトラッキングパラメーター
exl-id: e2cfd59e-ce4a-4cbb-b64a-828d1db7410f
feature: Tracking
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# メールトラッキングパラメーター {#email-tracking-parameter}

[!DNL Marketo Measure] メールトラッキングパラメーターを使用すると、マーケターは、メールのクリックをフォーム送信として扱い、これらのアクションに対してタッチポイントが生成されるようにすることができます。 メールトラッキングパラメーターを使用しない場合、ユーザーがフォーム送信または web チャットを通じてサイトに実際にアクセスするまで、メールからのクリックスルーは「web 訪問」として扱われます。

## ユースケース  {#use-cases}

**ウェビナー登録**：マーケティングチームが、ウェビナーに登録するための単一のボタンを含む E メール招待状を送信します。 メールには既にそのユーザーの情報が含まれているので、シングルクリックで自動登録されます。 ランディングページにはメールトラッキングパラメーターが含まれているので、クリックスルーして確認ページに移動 [!DNL Marketo Measure] ると、メールアドレスを取得してクリックスルーをフォーム入力として扱い、タッチポイントを生成できます。

**コンテンツのダウンロード**：コンテンツマーケティングチームは、公開した最新の eBook をメールからの直接ダウンロードリンクでプロモーションしたいと考えています。 メールテンプレートを作成する場合、ダウンロード確認ページにはメールトラッキングパラメーターが含まれ、クリックスルー時にメールアドレスを取得で [!DNL Marketo Measure] ます。 サイト上のフォームに入力しなくても、コンテンツダウンロードのタッチポイントを生成で [!DNL Marketo Measure] ます。 これは、メールが、メールトラッキングパラメーターを使用して、確認ページに移動したためです。

## 仕組み {#how-it-works}

訪問者がサイトに到達す [!DNL Marketo Measure] と、メールアドレスまたは [!DNL Salesforce] ID を持つランディングページが見つかることを期待します。これにより、その訪問を「フォーム送信」に関連付け、そのアクティビティのタッチポイントを生成できます。

顧客は、通常どおりにメールテンプレートを作成します。 追跡するアクションをランディングページに追加する時間が来たら、マーケティング自動化プラットフォームが受け入れるトークン、変数タグ、マクロを決定して、個々の値を動的に表示する必要があります。

Marketo Measureでは、メールアドレス、Salesforce リード ID またはSalesforce連絡先 ID の値を使用できます。

## タグの例 {#tag-examples}

| マーケティングオートメーション | トークン/タグ/マクロ | 例 | サポート資料 |
| --- | --- | --- | --- |
| Marketo | {{lead.Email Address}} | <https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId={{lead.EmailAddress}}> | [&#x200B; トークン &#x200B;](https://experienceleague.adobe.com/docs/marketo/using/product-docs/demand-generation/landing-pages/personalizing-landing-pages/tokens-overview.html?lang=ja) 概要 |
| Pardot | %%email%% または %%user_crm_id%% | <https://engage.marketo.com/rs/460-TDH-945/images/BZ-B2B-Marketing-Attribution-101-ebook.pdf?mailId=%%email%%> | [Pardot 変数タグリファレンス &#x200B;](https://help.salesforce.com/s/articleView?language=en_US&id=pardot_variable_tags_reference.htm&type=5) |
| Hubspot | （エディターを使用して挿入） | 該当なし | [HubSpot によるコンテンツのパーソナライズ &#x200B;](https://knowledge.hubspot.com/website-pages/personalize-your-content) |
| Act-On | （Message Composer 経由で挿入） | 該当なし | [Act-On によるメールコンテンツのパーソナライズ &#x200B;](https://connect.act-on.com/hc/en-us/articles/360033436074-How-to-Personalize-Email-Content-with-CRM-Data) |

最後に、[!DNL Marketo Measure] 内でトラッキングパラメーターを指定して、メール [!DNL Marketo Measure] たは ID の値を特定できるようにする必要があります。 デフォルトは、上の例と下のスクリーンショットに示すように、「mailId」です。 [!DNL Marketo Measure] の設定に値を入力し、「**[!UICONTROL 保存]**」をクリックします。

![&#x200B; 最後に、Marketo Measure内でトラッキングパラメーターを指定する必要があります &#x200B;](assets/marketo-engage-activities-01.png)
