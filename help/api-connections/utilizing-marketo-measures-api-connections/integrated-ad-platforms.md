---
unique-page-id: 18874594
description: 統合広告プラットフォーム — [!DNL Marketo Measure]  — 製品ドキュメント
title: 統合広告プラットフォーム
exl-id: df30ee8a-8b07-4f14-94e8-cc482fca8b18
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '1749'
ht-degree: 0%

---

# 統合広告プラットフォーム {#integrated-ad-platforms}

[!DNL Marketo Measure] には、Google AdWords、Microsoft BingAds、 [!DNL Facebook] 広告と DoubleClick Campaign Manager を参照してください。 これらの API 接続を通じて、 [!DNL Marketo Measure] は、外部の購入者アプリと共に、簡単にデータを取り込んで CRM にプッシュできます。 コストやデータを手動でアップロードする必要はありません。 代わりに、アカウントは、 [!DNL Marketo Measure] アプリを使用します。 [!DNL Marketo Measure] が自動的にマーケティングコストをプラットフォームからダウンロードし、 [!DNL Marketo Measure] アプリを使用します。 AdWords、BingAds、または [!DNL Facebook] 広告、 [!DNL Marketo Measure] は、広告の URL に自動的にパラメーターを追加します。

## 広告プラットフォームの接続方法 {#how-to-connect-ad-platforms}

各プラットフォームの詳細を確認する前に、これらのアカウントを [!DNL Marketo Measure]. 最初に、 [!DNL Marketo Measure] アプリケーションに移動し、 **[!UICONTROL 設定]** オプションを **[!UICONTROL マイアカウント]** 」タブをクリックします。 次に、 **[!UICONTROL 接続]** の下に **[!UICONTROL 統合]** 」セクションを開きます。

以下の画像に示すように、新しい広告の接続を設定するボタンが表示されます。

![](assets/2.png)

次に、 [!UICONTROL 新しい広告接続の設定] ボタン、ウィンドウ（下図を参照）が 4 つの広告でポップアップ表示されます [!UICONTROL 接続]イオンタイプ。 「接続」をクリックすると、別のウィンドウが開き、資格情報の入力を求められます。 資格情報を入力し、「 [!UICONTROL 許可] アカウントを接続する [!DNL Marketo Measure].

![](assets/select-account-type.png)

## Google AdWords {#google-adwords}

広告を [!DNL Google AdWords]を使用する場合は、手動タグ付け、自動タグ付け、トラッキングテンプレートの作成の 3 つの方法のいずれかでキャンペーンにタグ付けすることをお勧めします。 AdWords URL の手動タグ付けは、広告の URL の末尾にパラメーターを定義し追加することに依存します。 手動タグ付けを使用すると、Google以外のプラットフォームでも、パラメーターで収集されたデータを簡単に読み取ることができます。

トラッキングテンプレートは、Googleが ValueTrack パラメーターを呼び出すものを追加するためのツールです。 これらは、UTM や他のタグ付けパラメーターと同じ方法で機能します。

## 自動タギングが有効な場合の動作 {#what-happens-when-auto-tagging-is-enabled}

[!DNL Marketo Measure] でのトラッキングテンプレートの検索 [!DNL AdWords] アカウント：

* *オプション A*:トラッキングテンプレートが見つかりました。 [!DNL Marketo Measure] パラメーターをテンプレートに追加します。
* *オプション B*:サードパーティのリダイレクトが見つかりました。 トラッキングテンプレートにサードパーティのリダイレクトが見つかった場合、 [!DNL Marketo Measure] どのアクションも実行できません。 手動で [!DNL Marketo Measure] タグをサードパーティシステムに追加する必要があります。 サードパーティのリダイレクトの例としては、Kenshoo や Marin などの入札管理ツールがあります。 方法の詳細 [入札管理ツールの影響 [!DNL Marketo Measure]](/help/api-connections/utilizing-marketo-measures-api-connections/how-bid-management-tools-affect-marketo-measure.md){target=&quot;_blank&quot;}。

* *オプション C*:トラッキングテンプレートが見つかりません。 [!DNL Marketo Measure] は、 [!DNL Marketo Measure] パラメーター。 スキャンに基づいて、次の場合に選択します。
   * 次のパラメーターが見つかりました。設定が完了しました。
   * パラメーターが見つかりません： [!DNL Marketo Measure] は、広告のリンク先 URL の末尾にパラメーターを追加します。 [!DNL Marketo Measure] は、作成後 2 時間以内に新しい広告を追加します。 パラメーターはテンプレートに追加されないことに注意してください。

詳しくは、 [[!DNL AdWords] 自動タグ付け機能](/help/api-connections/utilizing-marketo-measures-api-connections/understanding-marketo-measure-adwords-tagging.md){target=&quot;_blank&quot;}。

## 有効にする方法 [!DNL Marketo Measure] Adwords の自動タギング {#how-to-enable-marketo-measure-auto-tagging-for-adwords}

有効にする前に [!DNL Marketo Measure] 自動タグ付け **Adwords アカウント内のアカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートが有効になっていることを確認してください。 これは、 [!DNL Marketo Measure] 自動タグ付けが有効になっています。** トラッキングテンプレートを有効にすると、広告パフォーマンス履歴データが失われるのを防ぐことができます。 キーワード、サイトリンク、広告レベルでトラッキングテンプレートを有効にすると、広告がレビューと承認のプロセスを経て、広告のパフォーマンス履歴が再開する可能性があることに注意してください。 有効なトラッキングテンプレートがない場合、 [!DNL Marketo Measure] が [!DNL Marketo Measure] トラッキングパラメーターを広告の「最終 URL」に直接追加すると、広告履歴データが失われる可能性があります。

トラッキングテンプレートを作成したら、以下の手順に従ってを有効にしてください。 [!DNL Marketo Measure] 自動タグ付け。 注意： [!DNL Marketo Measure] また、アカウント内の一時停止した広告に対しても自動タグ付けがおこなわれます。

1. ログイン先 [!DNL Marketo Measure] アカウント [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target=&quot;_blank&quot;}。

1. に移動します。 [!UICONTROL マイアカウント] > [!UICONTROL 設定] > [!UICONTROL 統合] > [!UICONTROL 接続].

   ![](assets/4.png)

1. 使用する Adwords アカウントの横にある鉛筆アイコンをクリックします。 [!DNL Marketo Measure] 自動タグ付けが有効になっています。

   ![](assets/5.png)

1. 右上隅で、 **[!UICONTROL 自動タギング]** 切り替え **[!UICONTROL はい]**. ページの下部で、 **[!UICONTROL 詳細情報]** テキストボックスを展開し、 **[!UICONTROL 保存]**. 自動タグ付けの設定が完了しました。

   ![](assets/6.png)

## AdWords でのトラッキングテンプレートの設定方法と使用方法 [!DNL Marketo Measure] パラメーター {#how-to-set-up-a-tracking-template-in-adwords-with-marketo-measure-parameters}

トラッキングテンプレートは、 [!UICONTROL アカウント], [!UICONTROL Campaign] または AdWords の広告グループレベル。 キーワード、サイトリンク、広告レベルにトラッキングテンプレートを追加する場合、広告はレビューと承認のプロセスを経る必要があり、広告のパフォーマンス履歴を再開するリスクがあります。 詳細情報： [トラッキングテンプレートの作成](https://support.google.com/adwords/answer/6076199?hl=en#tracking){target=&quot;_blank&quot;}。

1. にログインします。 [!DNL Google AdWords] アカウント。
1. 次に移動： [!UICONTROL キャンペーン] 左側のナビゲーションバーから表示
1. 」に移動します。[!UICONTROL 設定]」 （左側のナビゲーションバーにも表示）
1. 「[!UICONTROL アカウント設定]``上部に表示
1. 「[!UICONTROL トラッキング]&quot;セクション
1. トラッキングテンプレートに次のいずれかの文字列を貼り付けて、テンプレートの値を設定します。

   * すべての URL に疑問符がある場合は、次の URL テキストを使用します。

   `{lpurl}&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

   * URL に疑問符がない場合は、次の URL テキストを追加します。

   `{lpurl}?_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}*`

   URL に手動でタグ付けする際にエラーが発生しないようにするには、通常、UTM パラメーターを自動的に生成することをお勧めします。 AdWords や [!DNL Marketo Measure] パラメーターを使用する場合、指定した情報に基づいて URL のパラメーターを自動的に生成することでプロセスを簡略化する複数のツールがあります。

   >[!TIP]
   >
   >トラッキングテンプレートが無効であるというエラーが表示される場合は、ブラウザーのキャッシュをクリアして、もう一度やり直してください。これにより、問題が解決することがよくあります。

## の UTM タグを自動的に生成する方法 [!DNL Google AdWords] {#how-to-automatically-generate-utm-tags-for-google-adwords}

UTM タグは、最初は作成が難しいように見えますが、UTM パラメーターを使用して URL を簡単に作成できる多くのツールが用意されています。 次のいずれかのリソースを使用するか、Web で他のツールを検索します。 次の点に注意してください。 [!DNL Marketo Measure] は、これらのプラットフォームおよびツールに対する何らかの承認または保証を行いません。

**[!DNL Google URL]ビルダー**

Google URL Builder は、UTM タグを使用して正しく書式設定された URL を作成するための標準ツールです。 URL と各パラメーターの目的の値を入力し、「[!UICONTROL URL を生成]&quot;. タグ付けする URL が一握りしかない場合に使用するのに最適なツールです。 ツールにアクセス [ここ](https://support.google.com/analytics/answer/1033867?hl=ja){target=&quot;_blank&quot;}。

**EpikOne で生成されたGoogleスプレッドシート**

このスプレッドシートには、タグ付き宛先 URL を自動的に生成する数式が含まれています。 これは、多数のリンクをタグ付けする必要がある場合に使用する優れたツールです。 スプレッドシートへのアクセス [ここ](https://spreadsheets.google.com/ccc?key=p7c_HKcmspSUfEYSO0gskKw&amp;hl=en){target=&quot;_blank&quot;}。

**Rafflecopter リンクタグ付けツール**

Rafflecopter が作成したスプレッドシートは、 [!DNL EpikOne's] スプレッドシート。 また、使用するタグ付き宛先リンクを自動生成する数式も含まれています。

これらの各ツールには、ニーズに合わせての使用方法と変更方法に関する詳細な手順が含まれています。 このツールを使用できます。 [ここ](https://docs.google.com/spreadsheets/d/1QCIr1WUJQHE68cA4VTks2XE7nxuryaUymCEy_23-Oew/edit#gid=0){target=&quot;_blank&quot;}。

**Effin Amazing UTM Builder**

このツールは、UTM タグをすばやく生成できる Chrome 拡張機能です。 検索 [ここ](https://chrome.google.com/webstore/detail/effin-amazing-utm-builder/eoaapiimcaimddnfhfnifgkinmpcbccp?hl=en){target=&quot;_blank&quot;}。

## Bing Ads {#bing-ads}

Bing Ads は、URL の自動タギングを有効にしたり、次のようなサードパーティツールを使用したりできる統合プラットフォームです。 [!DNL Marketo Measure]、広告にタグを付けます。 [!DNL Bing Ads] は UTM パラメーターにも依存しています。

Bing Ads の自動タグ付け機能により、次の UTM パラメーターが追加されます。

* Utm_source
* Utm_medium
* Utm_term

Bing Ads の自動タグ付けでも、次のカスタムパラメーターが追加されます。

`_bt={adid}`

文字列は次のようになります。

`{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`

注意すべき点は [!DNL Bing Ads] では、最終的な URL でカスタムタグを使用して、必要に応じてさらに多くのパラメーターを追加し、より精度を高めることができます。

必要に応じてトラッキングテンプレートを使用できますが、 [!DNL Bing Ads] および [!DNL Marketo Measure] を統合します。 これは、 [!DNL Bing] 履歴を変更せずに広告を編集できるようにします。 [!DNL Marketo Measure] は宛先 URL を更新できます。

自動タグ付けは、 [!DNL Marketo Measure] そのために [!DNL Marketo Measure] パラメーターは自動的に追加されます。 Bing Ads を使用して過去の広告パフォーマンス履歴を失うリスクはありません。

次にアクセス： [[!DNL Bing Ads]](https://advertise.bingads.microsoft.com/en-us/blog/post/august-2016/upgraded-urls-now-available-in-bing-ads-an-easier-way-to-manage-your-tracking-urls){target=&quot;_blank&quot;} の Web サイトを参照してください。

## Facebook 広告 {#facebook-ads}

この [!DNL Marketo Measure] ～との統合 [!DNL Facebook] では、広告情報を自動的にダウンロードし、URL にパラメーターをタグ付けできます。 [!DNL Marketo Measure] は、自動タグ付けを通じてキャンペーンおよび広告セット情報を取り込みます。 広告セットが「広告グループ名」フィールドに入力されます。 での URL タグの設定について詳しくは、 [!DNL Facebook] プラットフォームで、 [!DNL Facebook] [ビジネス](https://www.facebook.com/business/help/1016122818401732/?ref=u2u){target=&quot;_blank&quot;} ページ。

で自動タグ付けを有効にする前に [!DNL Facebook Ads]の場合は、以前のパフォーマンス履歴を CSV 形式で書き出すことが重要です。 この時点で、 [!DNL Marketo Measure] タグ [!DNL Facebook Ads] _bf パラメータを持つ [!DNL Facebook] は、広告を新規として読み取り、パフォーマンス履歴を消去します。 したがって、以前のパフォーマンスの記録がお客様およびお客様の組織にとって価値のあるものである場合は、その記録を書き出すことが重要です。

なお、 [!DNL Facebook] いつでも～に対して説明する [!DNL Marketo Measure] アプリとデータは失われません。パフォーマンス履歴が消去されるのは、自動タギングが有効な場合のみです。

[この記事をご覧ください](https://www.facebook.com/business/help/393890194130036)facebookからの {target=&quot;_blank&quot;} [!DNL Facebook] 広告レポート。

## linkedInスポンサー付きコンテンツ {#linkedin-sponsored-content}

LinkedIn統合により、 [!DNL Marketo Measure] 宛先 URL をタグ付けするには、次の手順に従います。 [!DNL LinkedIn] スポンサー付きコンテンツ ( 最終的には [!DNL Marketo Measure] を使用して、タッチポイントジャーニー全体をフォローし、アクティビティを特定の [!DNL LinkedIn] Campaign と Creative。 これにより、顧客の ROI に関するインサイトが得られます [!DNL LinkedIn] アクティビティ。 [!DNL Marketo Measure] ユニークなクリエイティブを検索します [!DNL LinkedIn] 共有して `?_bl={creativeId}` パラメーターを最後に追加する必要があります。

理由： [!DNL LinkedIn] 共有は複数のキャンペーンおよびクリエイティブで使用できます。独自性を維持するために、既存のクリエイティブのコピー/複製/複製をおこなわないようにしてください。 共有が見つかり、1 つのクリエイティブでのみ使用されると検出された場合、 [!DNL Marketo Measure] は、クリエイティブまたは共有を再作成しなくても、そのまま共有にタグ付けでき、すべての広告履歴（インプレッション数、クリック数、共有数）が残ります。

共有が複数のクリエイティブで共有されるとすぐに、 [!DNL Marketo Measure] 一意のセットを作成するには、を一時停止、コピー、再タグ付けするプロセスを実行する必要があります。 [!DNL Marketo Measure] は、ライブクリエイティブを一時停止およびアーカイブします。つまり、インプレッション数、クリック数およびソーシャル共有を含むクリエイティブもアーカイブされます。

## 非統合プラットフォーム {#non-integrated-platforms}

と統合されていないプラットフォームの場合 [!DNL Marketo Measure]、 [!DNL Marketo Measure] 自動タグ付け機能は使用できません。 パラメーターは手動で追加する必要があります。
