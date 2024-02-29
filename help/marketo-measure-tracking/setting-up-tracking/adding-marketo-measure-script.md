---
unique-page-id: 18874795
description: 追加中 [!DNL Marketo Measure] スクリプト — [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure]  スクリプトの追加'
exl-id: f8773037-04d7-4308-ba04-440e9b990d92
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 82%

---

# [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script}

[!DNL Marketo Measure] で追跡する [!DNL Marketo Measure] JavaScript は、できるだけ早くすべての web プロパティに追加する必要があります。JavaScript をデプロイしたら、[!DNL Marketo Measure] はデジタルデータの収集を開始します。この記事では、[!DNL Marketo Measure] JavaScript をデプロイする方法と考慮すべき追加の考慮事項について説明します。

>[!NOTE]
>
>[!DNL Marketo Measure] JavaScript のデプロイに加えて、[適切なドメインをすべて  [!DNL Adobe Admin Console]](/help/marketo-measure-and-adobe/domain-management.md){target="_blank"} で要求する必要があります。

[!DNL Marketo Measure] の使用を開始する際、[!DNL Marketo Measure] JavaScript を web サイトに追加するには次の 2 つの方法があります。

* ハードコード
* タグ管理システム

## ハードコード {#hard-coding}

ベストプラクティスとして、[!DNL Marketo Measure] JavaScript を web プロパティにハードコードすることを強くお勧めします。スクリプトをハードコードするには、スクリプトを終了の前に配置する必要があります `</head>` を選択できます。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

JavaScript を `<head>` を設定すると、 [!DNL Marketo Measure] スクリプトが最初に読み込まれ、参照情報が見つかりません。 [!DNL Marketo Measure] JavaScript は非同期で読み込まれます。ハードコードする場合は、JavaScript をマーケティングオートメーションに手動で追加する必要があります。

>[!TIP]
>
>スクリプトが GDPR に準拠していることを確認する方法については、[こちら](/help/security-and-compliance/compliance-related-resources/ensuring-consent-for-gdpr-in-marketo-measure-js.md){target="_blank"}を参照してください。

## タグ管理システム {#tag-management-systems}

追加する場合 [!DNL Marketo Measure] ハードコーディングを使用した JavaScript は使用できません。もう 1 つのオプションとして、 [!DNL Marketo Measure] 次のようなTag Management System を使用したスクリプト [!DNL Google Tag Manager] (GTM) または Tealium。

タグ管理システムを使用して、 [!DNL Marketo Measure] JS は、スクリプトの読み込み時間の遅延により、5～10%のデータ損失を引き起こす可能性があります。 基本的に、タグ管理ツールが十分に早く読み込まれない場合、[!DNL Marketo Measure] JS も十分に早く読み込むことができず、最初のリファラー情報が失われる可能性があります。

一般的な方法として、タイミング／リソースがハードコードに移行するのが適切になるまで、タグ管理ツールを通じて [!DNL Marketo Measure] JS をデプロイします。

追加するには [!DNL Marketo Measure] スクリプトをタグ管理ソリューションで使用する場合は、新しいタグを作成し、その中に JavaScript を追加する必要があります。 このタグを、追跡する web サイト上のすべてのページに適用します。

[!DNL Marketo Measure] では、すべてのページビューでタグが起動されるようにすることをお勧めします。さらに、最高のデータ品質を確保するために、実行順序で [!DNL Marketo Measure] に最高の優先度を与え、[!DNL Marketo Measure] タグの前に同期スクリプトがないことを確認することが最善です。

詳しくは、[こちらを参照](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-via-google-tag-manager.md){target="_blank"}してください。

## 追加の考慮事項 {#additional-considerations}

[!DNL Marketo Measure] JavaScript はドメインベースであるので、JavaScript がページ上にあり、ルートドメインが Marketo Measure アカウントの作成に使用されたドメインと同じである限り、任意のサブドメインを自動的に処理できます。

ただし、個別のドメインまたは国際ドメインを使用している場合は、[!DNL Marketo Measure] コンサルタントに必ずお知らせください。[!DNL Marketo Measure] が追加のドメインのデータをアカウントに関連付けることができるように、[!DNL Marketo Measure] 側でドメインをアカウントに手動で追加する必要があります。そのため、別のドメインや国際ドメインを [!DNL Marketo Measure] コンサルタント。

サードパーティのページを使用する場合は、[!DNL Marketo Measure] コンサルタントとユースケースについて話し合ってください。一般に、 [!DNL Marketo Measure] JavaScript を使用して、該当する場合はこれらのページを追跡します。 これが不可能な場合は、CRM Campaign タッチポイントを介したトラッキングを、 [!DNL Marketo Measure] コンサルタント。

必ずしもアトリビューションを意味しないことから、[!DNL Marketo Measure] で追跡すべきではないフォーム（購読解除フォーム、顧客ログインなど）はありますか？その場合は、除外コードを追加します。 [この記事では、](/help/marketo-measure-tracking/setting-up-tracking/excluding-marketo-measure-from-specific-forms.md){target="_blank"} 各フォーム

セキュリティで保護されていないページはありますか？その場合は、セキュリティで保護されたページとセキュリティで保護されていないページの間を移動すると、トラッキングセッションが中断されるので、セキュリティで保護したいと考えます。

必ず web チームと話し合って、[!DNL Marketo Measure] JavaScript を常に適切な web プロパティに配置する必要があることを理解する必要があります。新しいページ／フォーム／サイトを導入する場合は、[!DNL Marketo Measure] JavaScript のデプロイがプロトコルの一部であることを確認します。

JavaScript の設定中に [!DNL Web Application Firewall (WAF)]（WAF）の警告がトリガーされた場合、ユーザーは、次の例に示すように、その WAF ルールを無効にするか、Cookie を許可リストに登録することができます。

![](assets/adding-marketo-measure-script-1.png)

## 特別な注意を払うべきフォーム {#forms-to-pay-extra-attention-to}

**複数フォームの送信**

* 問題：単一のフォーム送信の一部として複数のリンクされたフォームがある場合、完全なフォームが送信されなくても、最初のフォームがタッチポイントを生成する可能性があります。
* 解決策：いずれかのフォームを強制的にユーザーに報告する必要があります。 [!DNL Marketo Measure] キャッシュされたデータに基づいており、中断の慣行について話し合います。 一般に、[レポートユーザーコード](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-to-different-form-providers/ajax-form-handling.md){target="_blank"}でこれを解決できます。

**アカウントログイン（未作成）**

* 問題：[!DNL Marketo Measure] では、アトリビューションストーリーが希薄になる傾向があるので、その後のアカウントログインではタッチポイントを作成しないことをお勧めします。
* 解決策：除外コードをアカウント／顧客／パートナーのログインフォームに追加します。

>[!NOTE]
>
>アカウントまたは体験版を作成するためのタッチポイントを作成することをお勧めします。

**アセットのダウンロード**

* 問題：アセットがゲートされている場合、[!DNL Marketo Measure] はフォーム入力としてダウンロードを追跡します。アセットがゲートされていない場合、カスタマイズせずにレポートできる内容には制限があります。
* 解決策：[!DNL Marketo Measure] JavaScript で追跡する場合は、アセットの出入りを制御します。それはできないけれど、そのためのタッチポイントは気に入っているという場合は、代わりに CRM キャンペーンを同期することを検討します。

**iFrame**

* 問題：iFrame は、基本的にページ内のページとして機能します。
* 解決策：フォームに正しく添付するには、[!DNL Marketo Measure] JS を iFrame のヘッダー内に直接デプロイする必要があります。

**Lightbox**

* Lightbox は通常、iFrame を含むポップアップです
* 解決策：[!DNL Marketo Measure] JS は、ホストされる iFrame のヘッダー内にデプロイする必要があります。

**ページ上の複数のフォーム**

* 問題：ページ上に複数のフォームがホストされる場合、[!DNL Marketo Measure] フォーム URL フィールドに入力された特定のフォームがわからない場合があります。
* 解決策：入力されたフォームを把握する必要がある場合は、web チームと動的 URL ハッシュの設定を検討します。

**`<div>` 形式で編成されるフォーム**

* 問題：[!DNL Marketo Measure] JS は、`<div>` 形式で編成されるフォームを認識するのが難しいので、カスタムコードが必要になる場合があります。
* 解決策：これらの[レポートユーザーテンプレート](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-to-different-form-providers/ajax-form-handling.md){target="_blank"}は、web 開発チームが必要なコードを追加するために使用できます。

**チャット**

* 問題：チャットプロバイダーを使用する場合は、特別な処理が必要になる場合があります。
* 解決策：[!DNL Marketo Measure] は、Drift、Olark、Livechat、LivePerson、SnapEngage と統合されています。他のすべてのプラットフォームは、CRM キャンペーンメンバーシップを通じて追跡する必要があります。

**2 番目のドメイン**

* 問題：[!DNL Marketo Measure] JavaScript はドメイン固有であるので、個別のドメインまたは国際ドメインに対しては追加の手順を実行する必要があります。[!DNL Marketo Measure] JS は同じルートドメイン上のサブドメインを処理できます。
* 解決策：複数のルートドメインを所有しており、[!DNL Marketo Measure] で追跡する場合は、必ずドメインに JS を追加し、[!DNL Marketo Measure] アカウントに手動で関連付ける必要があるドメインを [!DNL Marketo Measure] コンサルタントにお知らせください。

## [!DNL Marketo Measure] JavaScript のテスト {#testing-marketo-measure-javascript}

[!DNL Marketo Measure] コンサルタントは、web サイトのスポットテストをサポートして、[!DNL Marketo Measure] JavaScript がすべてのページに存在することを確認します。このテストの一部として、トラッキングが適切に返されるよう、テストの詳細を明確に示したいくつかのフォーム入力を送信します。

ただし、[!DNL Marketo Measure] コンサルタントは、web チームほど web サイトに精通していない可能性があります。このため、特に上記のような複雑なフォームを使用している場合は、web チームまたはその他の適切なチームが web サイトを徹底的にチェックすることが非常に重要です。必要なすべての web プロパティが適切に追跡されていることを確認するのは最終的にチームの責任ですが、複雑なフォームや状況を認識している場合は、[!DNL Marketo Measure] コンサルタントにテストのサポートを依頼してください。

自分でフォームをテストするには、次の手順に従います。

1. 各フォーム送信テストの間には、常に匿名ブラウザーを使用するかキャッシュをクリアし、毎回異なるメールアドレスを使用します。

   a. ベストプラクティスとして、テストであることと時刻を示す内容を含む偽のメールを使用します。例：testing830am@test.com。

1. フォームを送信するページの URL と使用するメールを記録します。

1. そのフォーム送信に対して CRM（リードまたは連絡先）で作成されたレコードを見つけて、タッチポイントが適切に作成されたことを確認します。

   a. [!DNL Marketo Measure] の詳細でページレイアウトを更新することを選択した場合は、購入者のタッチポイントを持つリードなどの [!DNL Marketo Measure] ストックレポートを使用したり、リード／連絡先ページレイアウトを確認したりできます。

   b. データの処理には時間がかかる場合があります。
