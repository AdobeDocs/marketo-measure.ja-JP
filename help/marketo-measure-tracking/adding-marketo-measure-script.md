---
description: 追加  [!DNL Marketo Measure]  スクリプト - [!DNL Marketo Measure]
title: ' [!DNL Marketo Measure]  スクリプトの追加'
exl-id: f8773037-04d7-4308-ba04-440e9b990d92
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 57%

---


# [!DNL Marketo Measure] スクリプトの追加 {#adding-marketo-measure-script}

[!DNL Marketo Measure] で追跡する [!DNL Marketo Measure] JavaScript は、できるだけ早くすべての web プロパティに追加する必要があります。JavaScriptをデプロイすると、[!DNL Marketo Measure] がデジタルデータの収集を開始します。 この記事では、JavaScriptのデプロイ方法とその他 [!DNL Marketo Measure] 考慮事項の概要を説明します。

>[!NOTE]
>[!DNL Marketo Measure] JavaScript のデプロイに加えて、[適切なドメインをすべて  [!DNL Adobe Admin Console]](/help/marketo-measure-and-adobe/domain-management.md){target="_blank"} で要求する必要があります。

[!DNL Marketo Measure] の使用を開始する際、[!DNL Marketo Measure] JavaScript を web サイトに追加するには次の 2 つの方法があります。

* ハードコード
* タグ管理システム

## ハードコード {#hard-coding}

ベストプラクティスとして、[!DNL Marketo Measure] JavaScript を web プロパティにハードコードすることを強くお勧めします。スクリプトをハードコードするには、サイトのすべてのページのクローズド `</head>` ージの前にスクリプトを配置する必要があります。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

JavaScriptをページの `<head>` にハードコードすると、[!DNL Marketo Measure] スクリプトが最初に読み込まれ、参照情報が失われることはありません。 [!DNL Marketo Measure] JavaScript は非同期で読み込まれます。ハードコードする場合は、JavaScript をマーケティングオートメーションに手動で追加する必要があります。

>[!TIP]
>スクリプトが [GDPR に準拠 &#x200B;](/help/security/ensuring-consent-for-gdpr-in-marketo-measure-js.md){target="_blank"} していることを確認する方法を説明します。

## タグ管理システム {#tag-management-systems}

ハードコーディング [!DNL Marketo Measure] 使用してJavaScriptを追加できない場合は、[!DNL Marketo Measure] （GTM）や Tealium などのTag Management System を使用して [!DNL Google Tag Manager] スクリプトを追加する方法もあります。

タグ管理システムを使用して [!DNL Marketo Measure] JS をデプロイすると、スクリプトの読み込み時間の待ち時間が原因で、データが 5～10% 失われる可能性があります。 基本的に、タグ管理ツールが十分に早く読み込まれない場合、[!DNL Marketo Measure] JS も十分に早く読み込むことができず、最初のリファラー情報が失われる可能性があります。

一般的な方法として、タイミング／リソースがハードコードに移行するのが適切になるまで、タグ管理ツールを通じて [!DNL Marketo Measure] JS をデプロイします。

タグ管理ソリュ [!DNL Marketo Measure] ションを通じてスクリプトを追加するには、タグを作成し、その中にJavaScriptを追加する必要があります。 このタグを、追跡する web サイト上のすべてのページに適用します。

[!DNL Marketo Measure] では、すべてのページビューでタグが起動されるようにすることをお勧めします。また、最も優先順位の高い処理を実行順序で行い、最も高いデータ品質を確保 [!DNL Marketo Measure] るために、[!DNL Marketo Measure] タグの前に同期スクリプトがないことを確認することをお勧めします。

詳しくは、[こちらを参照](/help/marketo-measure-tracking/adding-marketo-measure-script-via-google-tag-manager.md){target="_blank"}してください。

## 追加の考慮事項 {#additional-considerations}

[!DNL Marketo Measure] JavaScript はドメインベースであるので、JavaScript がページ上にあり、ルートドメインが Marketo Measure アカウントの作成に使用されたドメインと同じである限り、任意のサブドメインを自動的に処理できます。

ただし、個別のドメインまたは国際ドメインを使用している場合は、[!DNL Marketo Measure] コンサルタントに必ずお知らせください。追加のドメインのデータをアカウントに結び付けることがで [!DNL Marketo Measure] るように、ドメインは [!DNL Marketo Measure] 側でアカウントに手動で追加する必要があります。 そのため、[!DNL Marketo Measure] コンサルタントには、個別のドメインや国際的なドメインを送信してください。

サードパーティのページを使用している場合は、ユースケースについて [!DNL Marketo Measure] コンサルタントと話し合ってください。 一般に、必要に応じて、JavaScriptのカスタムバージョンを追加して、それら [!DNL Marketo Measure] ページをトラッキングできるかどうかを知る必要があります。 それが不可能な場合は、[!DNL Marketo Measure] コンサルタントが CRM キャンペーンタッチポイントを使用したトラッキングを調査します。

アトリビューションに対応していないフォーム（例えば、登録解除フォーム、顧客ログインなど）があり、[!DNL Marketo Measure] でトラッキングすべきでないフォームはありますか？ その場合は、除外コード [&#x200B; この記事 &#x200B;](/help/marketo-measure-tracking/excluding-marketo-measure-from-specific-forms.md){target="_blank"} を各フォームに追加します

セキュリティで保護されていないページはありますか？安全なページと安全でないページの間を移動すると、トラッキングセッションが中断されるので、これらを保護する必要があります。

必ず web チームと話し合って、[!DNL Marketo Measure] JavaScript を常に適切な web プロパティに配置する必要があることを理解する必要があります。新しいページ／フォーム／サイトを導入する場合は、[!DNL Marketo Measure] JavaScript のデプロイがプロトコルの一部であることを確認します。

JavaScriptの設定中に [!DNL Web Application Firewall (WAF)] 警告がトリガーされた場合、次の例のように、そのWAF ルールを無効にするか、cookie を許可リストに加えるできます。

![&#x200B; 例Marketo Measure スクリプトのWAF警告プロンプト &#x200B;](assets/adding-marketo-measure-script-1.png)

## 特別な注意を払うべきフォーム {#forms-to-pay-extra-attention-to}

**複数フォームの送信**

* 問題：1 つのフォーム送信の一部として複数のリンクされたフォームがある場合、完全なフォームが送信されていなくても、最初のフォームがタッチポイントを生成する可能性があります。
* 解決策：いずれかのフォームで、キャッシュされたデータに基づいてユーザーが [!DNL Marketo Measure] することをレポートし、放棄のベストプラクティスについて話し合う必要があります。 一般に、[レポートユーザーコード](/help/marketo-measure-tracking/ajax-form-handling.md){target="_blank"}でこれを解決できます。

**アカウントログイン（未作成）**

* 問題：[!DNL Marketo Measure] では、アトリビューションストーリーが希薄になる傾向があるので、その後のアカウントログインではタッチポイントを作成しないことをお勧めします。
* 解決策：除外コードをアカウント／顧客／パートナーのログインフォームに追加します。

>[!NOTE]
>アカウントまたは体験版を作成するためのタッチポイントを作成することをお勧めします。

**アセットのダウンロード**

* 問題：アセットがゲートされている場合、[!DNL Marketo Measure] はダウンロードをフォーム入力として追跡します。 アセットがゲートされていない場合、カスタマイズせずにレポートできる内容には制限があります。
* 解決策：[!DNL Marketo Measure] JavaScript で追跡する場合は、アセットの出入りを制御します。それはできないけれど、そのためのタッチポイントは気に入っているという場合は、代わりに CRM キャンペーンを同期することを検討します。

**iFrame**

* 問題：iFrame は、基本的にページ内のページとして機能します。
* 解決策：フォームに正しく添付するために、[!DNL Marketo Measure] JS を iFrame ヘッダー内に直接デプロイする必要があります。

**Lightbox**

* Lightbox は通常、iFrame を含むポップアップです
* 解決策：[!DNL Marketo Measure] JS は、ホストされる iFrame のヘッダー内にデプロイする必要があります。

**ページ上の複数のフォーム**

* 問題：ページ上に複数のフォームがホストされる場合、[!DNL Marketo Measure] フォーム URL フィールドに入力された特定のフォームがわからない場合があります。
* 解決策：どのフォームに入力されたかを知る必要がある場合は、web チームでの動的 URL ハッシュの設定を検討してください。

**`<div>` 形式で編成されるフォーム**

* 問題：[!DNL Marketo Measure] JS は、`<div>` 形式で編成されるフォームを認識するのが難しいので、カスタムコードが必要になる場合があります。
* 解決策：これらの[レポートユーザーテンプレート](/help/marketo-measure-tracking/ajax-form-handling.md){target="_blank"}は、web 開発チームが必要なコードを追加するために使用できます。

**チャット**

* 問題：チャットプロバイダーを使用する場合は、特別な処理が必要になる場合があります。
* 解決策：[!DNL Marketo Measure] は、Drift、Olark、Livechat、LivePerson、SnapEngage と統合されています。他のすべてのプラットフォームは、CRM キャンペーンメンバーシップを通じて追跡する必要があります。

**2 番目のドメイン**

* 問題：JavaScript[!DNL Marketo Measure] ドメイン固有なので、個別のドメインや国際的なドメインに対して追加の手順を実行する必要があります。 [!DNL Marketo Measure] JS は、同じルートドメインのサブドメインを処理できます。
* 解決策：複数のルートドメインを所有しており、[!DNL Marketo Measure] で追跡する場合は、必ずドメインに JS を追加し、[!DNL Marketo Measure] アカウントに手動で関連付ける必要があるドメインを [!DNL Marketo Measure] コンサルタントにお知らせください。

## [!DNL Marketo Measure] JavaScript のテスト {#testing-marketo-measure-javascript}

[!DNL Marketo Measure] コンサルタントは、web サイトをスポットテストし、すべてのページにJavaScriptが存在 [!DNL Marketo Measure] ることを確認するのに役立ちます。 このテストの一部では、トラッキングが正しく返されることを確認するために、テストの詳細が明確に示されたフォーム入力をいくつか送信します。

ただし、[!DNL Marketo Measure] コンサルタントは、web チームほど web サイトに精通していない可能性があります。このため、特に上記のような複雑なフォームを使用している場合は、web チームまたはその他の適切なチームが web サイトを徹底的にチェックすることが非常に重要です。必要なすべての web プロパティが適切に追跡されていることを確認するのは最終的にチームの責任ですが、複雑なフォームや状況を認識している場合は、[!DNL Marketo Measure] コンサルタントにテストのサポートを依頼してください。

フォームを自分でテストするには、次の手順に従います。

1. 各フォーム送信テストの間には、常に匿名ブラウザーを使用するかキャッシュをクリアし、毎回異なるメールアドレスを使用します。

   a. ベストプラクティスとして、テストであることと時刻を示す内容を含む偽のメールを使用します。例：testing830am@test.com。

1. フォームを送信するページの URL と、使用したメールを記録します。

1. そのフォーム送信に対して CRM（リードまたは連絡先）で作成されたレコードを見つけて、タッチポイントが適切に作成されたことを確認します。

   a. [!DNL Marketo Measure] の詳細でページレイアウトを更新することを選択した場合は、購入者のタッチポイントを持つリードなどの [!DNL Marketo Measure] ストックレポートを使用したり、リード／連絡先ページレイアウトを確認したりできます。

   b. データの処理に時間がかかる場合があります。
