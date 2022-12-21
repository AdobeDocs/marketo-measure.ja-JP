---
unique-page-id: 18874795
description: 追加中 [!DNL Marketo Measure] スクリプト — [!DNL Marketo Measure]  — 製品ドキュメント
title: 追加中 [!DNL Marketo Measure] スクリプト
exl-id: f8773037-04d7-4308-ba04-440e9b990d92
source-git-commit: 82cc8269bfdb26b6acf039d0ce0e06564f5e2612
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 0%

---

# 追加中 [!DNL Marketo Measure] スクリプト {#adding-marketo-measure-script}

[!DNL Marketo Measure] 追跡する JavaScript [!DNL Marketo Measure] をできるだけ早くすべての Web プロパティに追加する必要があります。 JavaScript をデプロイしたら、 [!DNL Marketo Measure] がデジタルデータの収集を開始します。 この記事では、 [!DNL Marketo Measure] JavaScript と、考慮に入れるその他の考慮事項。

>[!NOTE]
>
>次の条件を満たしていることを確認します。 [内の適切なドメインをすべて要求しました [!DNL Adobe Admin Console]](/help/marketo-measure-and-adobe/domain-management.md){target=&quot;_blank&quot;} をデプロイする以外に [!DNL Marketo Measure] JavaScript。

を使い始める際 [!DNL Marketo Measure]を追加するには、次の 2 つの方法があります [!DNL Marketo Measure] JavaScript を Web サイトに送信します。

* ハードコーディング
* Tag Management Systems

## ハードコーディング {#hard-coding}

ベストプラクティスとして、ハードコーディングを強くお勧めします [!DNL Marketo Measure] JavaScript を Web プロパティに追加します。 スクリプトをハードコードするには、終了タグの前にスクリプトを配置する必要があります `</head>` を設定します。

`<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

JavaScript を `<head>` を設定すると、 [!DNL Marketo Measure] スクリプトが最初に読み込まれ、参照情報が見つかりません。 この [!DNL Marketo Measure] JavaScript が非同期で読み込まれる。 ハードコーディングの場合、JavaScript はマーケティングオートメーションに手動で追加する必要があります。

>[!TIP]
>
>スクリプトが [GDPR 準拠](/help/security-and-compliance/compliance-related-resources/ensuring-consent-for-gdpr-in-marketo-measure-js.md){target=&quot;_blank&quot;}。

## Tag Management Systems {#tag-management-systems}

追加する場合 [!DNL Marketo Measure] ハードコーディングを使用した JavaScript は使用できません。もう 1 つの選択肢は、 [!DNL Marketo Measure] 次のようなTag Management System を使用したスクリプト [!DNL Google Tag Manager] (GTM) または Tealium。

タグ管理システムを使用して、 [!DNL Marketo Measure] JS は、スクリプトの読み込み時間の遅延により、5～10%のデータ損失を引き起こす可能性があります。 基本的に、タグ管理ツールの読み込みが十分に速く行われない場合、 [!DNL Marketo Measure] また、JS は十分な速さで読み込むことができず、最初のリファラー情報が失われる可能性があります。

一般的な方法は、 [!DNL Marketo Measure] タグ管理ツールを介した JS。タグ管理ツールを使用すると、タイミングやリソースがハードコーディングに移行する方が適しています。

追加するには [!DNL Marketo Measure] スクリプトをタグ管理ソリューションで実行する場合は、新しいタグを作成し、その中に JavaScript を追加する必要があります。 このタグは、追跡する Web サイト上のすべてのページに適用します。

[!DNL Marketo Measure] では、どのページビューでもタグを起動することをお勧めします。 さらに、 [!DNL Marketo Measure] 実行順序で最も優先度が高く、 [!DNL Marketo Measure] タグを使用して、最高のデータ品質を確保する必要があります。

詳細は次のとおりです。 [ここにある](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-via-google-tag-manager.md){target=&quot;_blank&quot;}。

## その他の考慮事項 {#additional-considerations}

[!DNL Marketo Measure] JavaScript はドメインベースなので、JavaScript がページ上にあり、ルートドメインがMarketo Measure アカウントの作成に使用したドメインと同じである限り、任意のサブドメインを自動的に処理できます。

ただし、別のドメインや国際ドメインを使用している場合は、 [!DNL Marketo Measure] コンサルタントが知っている。 ドメインは、 [!DNL Marketo Measure] 終わって [!DNL Marketo Measure] は、追加のドメインのデータをアカウントに関連付けることができます。 そのため、別のドメインや国際ドメインをお客様に送信してください [!DNL Marketo Measure] コンサルタント。

サードパーティのページを使用する場合は、のユースケースについて [!DNL Marketo Measure] コンサルタント。 一般に、 [!DNL Marketo Measure] JavaScript を使用して、該当する場合はこれらのページを追跡します。 これが不可能な場合は、CRM Campaign タッチポイントを介したトラッキングを、 [!DNL Marketo Measure] コンサルタント。

追跡すべきでないフォームがあるか [!DNL Marketo Measure] これらは必ずしも属性（登録解除フォーム、顧客ログインなど）に意味を持つわけではないので、 その場合は、除外コードを追加します [この記事では、](/help/marketo-measure-tracking/setting-up-tracking/excluding-marketo-measure-from-specific-forms.md){target=&quot;_blank&quot;} を各フォームに追加

セキュリティで保護されていないページがあるか。 その場合は、セキュリティで保護されたページとセキュリティで保護されていないページの間を移動すると、トラッキングセッションが中断されるので、セキュリティで保護したいと考えます。

Web チームと必ず会話し、ユーザーが知るようにしてください [!DNL Marketo Measure] JavaScript は、常に適切な Web プロパティ上にある必要があります。 新しいページ、フォーム、サイトが導入された場合は、必ず [!DNL Marketo Measure] JavaScript はプロトコルの一部です。

次の場合、 [!DNL Web Application Firewall (WAF)] 次の例に示すように、JavaScript の設定中に警告がトリガーされる場合は、ユーザーは WAF ルールを無効にするか、Cookie を許可リストに登録します。

![](assets/adding-marketo-measure-script-1.png)

## Formsが～に特に注意を払う {#forms-to-pay-extra-attention-to}

**マルチフォーム送信**

* 問題：1 つのフォーム送信の一部として、複数のリンクされたフォームがある場合、フォーム全体が送信されていなくても、最初のフォームがタッチポイントを生成する可能性があります。
* 解決策：フォームの 1 つに対し、次のようなレポートを強制的に送信する必要があります。 [!DNL Marketo Measure] キャッシュされたデータに基づいており、中断の慣行について話し合います。 一般に、 [レポートのユーザーコード](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-to-different-form-providers/ajax-form-handling.md){target=&quot;_blank&quot;} で解決できます。

**アカウントログイン（未作成）**

* 問題： [!DNL Marketo Measure] では、後続のアカウントログインではアトリビューションストーリーが希薄になるので、タッチポイントを作成しないことをお勧めします。
* 解決策：除外コードをアカウント/顧客/パートナーのログインフォームに追加します。

>[!NOTE]
>
>アカウントまたは体験版を作成するためのタッチポイントを作成することをお勧めします。

**アセットのダウンロード**

* 問題：アセットがゲーテッドなら、 [!DNL Marketo Measure] は、フォームの入力としてダウンロードを追跡します。 アセットがゲーテッドでない場合は、カスタマイズなしでレポートできる内容に制限があります。
* 解決策：追跡するアセットをゲートにする [!DNL Marketo Measure] JavaScript。 これがオプションではなく、そのタッチポイントを希望する場合は、代わりに CRM キャンペーンを同期することを検討してください。

**iFrames**

* 問題：iFrame は、基本的にページ内のページとして機能します。
* 解決策：この [!DNL Marketo Measure] フォームに正しく添付するには、JS を iFrame ヘッダー内に直接デプロイする必要があります。

**Lightbox**

* Lightbox は通常、iFrame を含むポップアップです
* 解決策：の [!DNL Marketo Measure] JS は、ホストされる iFrame のヘッダー内にデプロイする必要があります。

**ページ上の複数のフォーム**

* 問題：1 つのページに複数のフォームがホストされている場合、どの特定のフォームが [!DNL Marketo Measure] フォーム URL フィールド。
* 解決策：入力されたフォームを知る必要がある場合は、Web チームでの動的 URL ハッシュの設定を参照してください。

**Forms `<div>` 形式**

* 問題： [!DNL Marketo Measure] JS は、 `<div>` 形式を設定して、カスタムコードを必要とすることができます。
* 解決策：これら [レポートユーザーテンプレート](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-to-different-form-providers/ajax-form-handling.md)web 開発チームは、{target=&quot;_blank&quot;} を使用して、必要なコードを追加できます。

**チャット**

* 問題：チャットプロバイダを使用する場合は、特別な処理が必要になる場合があります。
* 解決策： [!DNL Marketo Measure] は、Drift、Olark、Livechat、LivePerson、SnapEngage と統合されています。 その他すべてのプラットフォームは、CRM キャンペーンメンバーシップを通じて追跡する必要があります。

**2 番目のドメイン**

* 問題： [!DNL Marketo Measure] JavaScript はドメインに固有なので、別のドメインまたは国際ドメインに対して追加の手順を実行する必要があります。 注意： [!DNL Marketo Measure] JS は、同じルートドメイン上のサブドメインを処理できます。
* 解決策：複数のルートドメインを所有している場合は、 [!DNL Marketo Measure] ドメインに JS を必ず追加し、 [!DNL Marketo Measure] 担当のドメインに手動で関連付ける必要があるドメインをコンサルタントが把握している [!DNL Marketo Measure] アカウント

## テスト [!DNL Marketo Measure] JavaScript {#testing-marketo-measure-javascript}

お使いの [!DNL Marketo Measure] コンサルタントは、Web サイトのテストを見つけて、 [!DNL Marketo Measure] JavaScript はすべてのページに存在します。 このテストの一部では、トラッキングが正しく返されるよう、テストの詳細を明確に示したいくつかのフォーム入力を送信します。

ただし、 [!DNL Marketo Measure] コンサルタントは、Web チームほど Web サイトに詳しくない可能性があります。 このため、Web チームやその他の適切なチームが Web サイトを十分にチェックし、上記のような複雑なフォームが使用されている場合は特に、Web サイトを十分にチェックすることが非常に重要です。 最終的に、チームは、必要なすべての Web プロパティが適切に追跡されるように責任を負いますが、複雑なフォームや状況を認識している場合は、 [!DNL Marketo Measure] テストに関するサポートが必要なコンサルタント。

自分でフォームをテストするには、次の手順に従います。

1. 常に匿名ブラウザーを使用するか、各フォーム送信テストの間のキャッシュをクリアして、毎回異なる電子メールアドレスを使用します。

   a.ベストプラクティスは、テストと時刻を示す内容を含んだ偽の E メールを使用することです。 例：testing830am@test.com.

1. 送信するフォームのページの URL と使用する電子メールを記録します。

1. フォーム送信用に CRM で作成されたレコード（リードまたは連絡先）を探し、タッチポイントが適切に作成されたことを確認します。

   a.以下の [!DNL Marketo Measure] を使用してページレイアウトを更新する場合は、リードと購入者タッチポイントなどの在庫レポート、リード/連絡先ページレイアウトを確認します。 [!DNL Marketo Measure] 詳細。

   b.データの処理には時間がかかる場合があります。
