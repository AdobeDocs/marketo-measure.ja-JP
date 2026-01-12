---
description: 統合された広告プラットフォーム - [!DNL Marketo Measure]
title: 統合された広告プラットフォーム
exl-id: df30ee8a-8b07-4f14-94e8-cc482fca8b18
feature: APIs, Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '1712'
ht-degree: 0%

---


# 統合された広告プラットフォーム {#integrated-ad-platforms}

[!DNL Marketo Measure] には、Google AdWords、Microsoft BingAds、[!DNL Facebook] Ads および DoubleClick Campaign Manager との API 接続があります。 これらの API 接続を通じて、[!DNL Marketo Measure] はデータを簡単に取り込み、外部のバイヤーアプリと共に CRM にプッシュできます。 コストやデータを手動でアップロードする必要はありません。 代わりに、アカウントは単に [!DNL Marketo Measure] アプリに接続して承認される必要があります。 [!DNL Marketo Measure] の後、マーケティングコストがプラットフォームから自動的にダウンロードされ、[!DNL Marketo Measure] アプリに読み込まれます。 AdWords、BingAds または [!DNL Facebook] Ads の自動タグ付けを有効にするよう選択した場合、[!DNL Marketo Measure] のパラメーターが広告の URL に自動的に追加されます。

## 広告プラットフォームの接続方法 {#how-to-connect-ad-platforms}

各プラットフォームの詳細を説明する前に、これらのアカウントを [!DNL Marketo Measure] に接続する方法について説明します。 まず [!DNL Marketo Measure] アプリにログインし、画面左上の **[!UICONTROL マイアカウント]** タブにある **[!UICONTROL 設定]** オプションに移動します。 次に、左側の **[!UICONTROL 統合]** セクションの下の **[!UICONTROL 接続]** を選択します。

以下の画像に示すように、新しい広告接続を設定するボタンが表示されます。

![ 新しい広告接続を設定ボタンを含む接続ページ ](assets/2.png)

[!UICONTROL  新しい広告接続の設定 ] ボタンをクリックすると、4 種類の広告 [!UICONTROL  接続 ] イオンタイプを含むウィンドウ（以下に示す）がポップアップ表示されます。 「接続」をクリックすると、別のウィンドウが表示されて資格情報の入力を求められます。 資格情報を入力し、「[!UICONTROL  認証 ]」をクリックしてアカウントを [!DNL Marketo Measure] に接続します。

![ 使用可能なアカウントタイプを使用したMarketo Measure ads 接続モーダル ](assets/select-account-type.png)

## Google AdWords {#google-adwords}

[!DNL Google AdWords] で広告を作成する際は、手動でのタグ付け、自動でのタグ付け、トラッキングテンプレートの作成のいずれかの方法でキャンペーンにタグ付けすることをお勧めします。 AdWords URL に手動でタグを付ける場合は、広告の URL の末尾にパラメーターを定義して追加する必要があります。 手動のタグ付けを使用すると、Google以外のプラットフォームがパラメーターによって収集されたデータを容易に読み取ることができます。

トラッキングテンプレートは、Googleが ValueTrack パラメーターと呼ぶパラメーターを追加するために提供するツールです。 これらは、UTM やその他のタグ付けパラメーターと同じ方法で機能します。

## 自動タギングが有効な場合の処理 {#what-happens-when-auto-tagging-is-enabled}

[!DNL Marketo Measure] アカウント内のトラッキングテンプレートを [!DNL AdWords] で検索：

* *オプション A*：追跡テンプレートが見つかりました。 パラメーター [!DNL Marketo Measure] テンプレートに追加されます。
* *オプション B*：サードパーティのリダイレクトが見つかった。 追跡テンプレートにサードパーティのリダイレクトが見つかっ [!DNL Marketo Measure] 場合は、何も実行できません。 [!DNL Marketo Measure] のタグをサードパーティ製システムに手動で追加する必要があります。 サードパーティのリダイレクトの例として、Kenshoo や Marin などの入札管理ツールがあります。 [ 入札管理ツールの影響  [!DNL Marketo Measure]](/help/api-connections/how-bid-management-tools-affect-marketo-measure.md){target="_blank"} の詳細をご覧ください。

* *オプション C*：追跡テンプレートが見つからない。 [!DNL Marketo Measure] べての広告宛先 URL をスキャンして、[!DNL Marketo Measure] のパラメーターを確認します。 スキャンに基づいて、次の場合：
   * パラメーターが見つかりました。設定が完了しました。
   * パラメーターが見つかりません：[!DNL Marketo Measure] のパラメーターを広告宛先 URL の末尾に追加します。 [!DNL Marketo Measure] は、作成後 2 時間以内に新しい広告を追加します。 パラメーターはテンプレートに追加されないことに注意してください。

詳しくは、[[!DNL AdWords]  自動タグ付け機能 ](/help/api-connections/understanding-marketo-measure-adwords-tagging.md){target="_blank"} を参照してください。

## Adwords の自動タギング [!DNL Marketo Measure] 有効にする方法 {#how-to-enable-marketo-measure-auto-tagging-for-adwords}

自動タギング [!DNL Marketo Measure] 有効にする前に、**Adwords アカウント内のアカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートが有効になっていることを確認します。 これは、自動タギングを有効にする Adwords アカウント [!DNL Marketo Measure] 必要です。** トラッキングテンプレートを有効にすると、広告パフォーマンス履歴データの損失を防ぐことができます。 キーワード、サイトリンク、または広告レベルでトラッキングテンプレートを有効にすると、広告はレビューと承認プロセスを経て、広告のパフォーマンス履歴が再開される可能性があることに注意してください。 有効なトラッキングテンプレートがない場 [!DNL Marketo Measure]、[!DNL Marketo Measure] のトラッキングパラメーターを広告の「最終 URL」に直接追加しますが、広告履歴データが失われる可能性もあります。

追跡テンプレートを設定したら、以下の手順に従って自動タギング [!DNL Marketo Measure] 有効にします。 メモ：アカウント [!DNL Marketo Measure] 一時停止されている広告も自動タグ付けされます。

1. [!DNL Marketo Measure] アカウント （[experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}）にサインインします。

1. [!UICONTROL  マイアカウント ]/[!UICONTROL  設定 ]/[!UICONTROL  統合 ]/[!UICONTROL  接続 ] に移動します。

   ![ 既存の広告アカウントとの接続リスト ](assets/4.png)

1. 自動タギングを有効にする Adwords アカウントの横にある鉛筆アイコン [!DNL Marketo Measure] クリックします。

   ![ 自動タギング切り替えを使用した広告アカウント設定パネル ](assets/5.png)

1. 右上隅で、「自動タギング **[!UICONTROL を「はい]** に切り替え **[!UICONTROL ま]**。 ページの下部にある **[!UICONTROL 詳細情報]** をクリックしてテキストボックスを展開し、「**[!UICONTROL 保存]** をクリックします。 自動タグ付けの設定が完了しました。

   ![Marketo Measureでの自動タグ付けの確認モーダル ](assets/6.png)

## [!DNL Marketo Measure] パラメーターを使用して AdWords にトラッキングテンプレートを設定する方法 {#how-to-set-up-a-tracking-template-in-adwords-with-marketo-measure-parameters}

AdWords では、[!UICONTROL  アカウント ]、[!UICONTROL  キャンペーン ] または広告グループのレベルでトラッキングテンプレートを追加する必要があることに注意してください。 トラッキングテンプレートをキーワード、サイトリンク、広告の各レベルに追加した場合は、広告のレビューと承認のプロセスを実行する必要があり、広告のパフォーマンス履歴が再度開始される恐れがあります。 詳しくは、[ トラッキングテンプレートの作成 ](https://support.google.com/adwords/answer/6076199?hl=en#tracking){target="_blank"} を参照してください。

1. [!DNL Google AdWords] アカウントにログインします。
1. 左側のナビゲーションバーから [!UICONTROL  キャンペーン ] ビューに移動します
1. 左側のナビゲーションバーの「[!UICONTROL  設定 ]」にも移動します。
1. 上部の「[!UICONTROL  アカウント設定 ]」ビューに切り替えます
1. 「[!UICONTROL  トラッキング ]」セクションを展開します
1. 追跡テンプレートに次のテキスト文字列のいずれかを貼り付けて、テンプレートの値を設定します。

   * すべての URL に疑問符が含まれる場合は、次の URL テキストを使用します。

   `{lpurl}&_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}`

   * URL に疑問符がない場合は、次の URL テキストを追加します。

   `{lpurl}?_bt={creative}&_bk={keyword}&_bm={matchtype}&_bn={network}&_bg={adgroupid}*`

   URL を手動でタグ付けするときにエラーが発生しないように、通常は UTM パラメーターを自動的に生成することをお勧めします。 これは、AdWords や [!DNL Marketo Measure] パラメーターによる自動タグ付けを意味する必要はありません。指定された情報に基づいて URL のパラメーターを自動的に生成することで、プロセスを簡略化するツールが複数あります。

   >[!TIP]
   >トラッキングテンプレートが無効であるというエラーが表示された場合は、ブラウザーのキャッシュをクリアして再試行してください。多くの場合、これによって問題が解決します。

## [!DNL Google AdWords] の UTM タグを自動生成する方法 {#how-to-automatically-generate-utm-tags-for-google-adwords}

UTM タグは、最初は作成が困難に見えるかもしれませんが、UTM パラメーターを使用して URL を簡単に作成できるツールは多数あります。 次のいずれかのリソースを使用するか、web で他のツールを検索できます。 [!DNL Marketo Measure] はこれらのプラットフォームやツールを推奨したり保証したりしないことに注意してください。

**[!DNL Google URL]Builder**

Google URL ビルダーは、UTM タグを使用して正しい形式の URL を作成するための標準ツールです。 各パラメーターの URL と目的の値を入力し、「[!UICONTROL URL を生成 ]」をクリックします。 これは、タグ付けする URL が少数しかない場合に使用する理想的なツールです。 ツールにアクセスします [ こちら ](https://support.google.com/analytics/answer/1033867?hl=ja){target="_blank"}。

**EpikOne が生成したGoogle スプレッドシート**

このスプレッドシートには、タグ付けされた宛先 URL を自動的に生成する数式が含まれています。 これは、多数のリンクをタグ付けする必要がある場合に使用する優れたツールです。 スプレッドシート [ こちら ](https://spreadsheets.google.com/ccc?key=p7c_HKcmspSUfEYSO0gskKw&hl=en){target="_blank"} にアクセスします。

**Rafflecopter リンク タグ付けツール**

Rafflecopter が作成したスプレッドシートは、[!DNL EpikOne's] のスプレッドシートの変更版です。 また、タグ付けされた宛先リンクを自動生成して使用する数式も含まれています。

これらの各ツールには、ニーズに合わせて使用および変更する方法の詳細な手順が記載されています。 このツールは [ こちら ](https://docs.google.com/spreadsheets/d/1QCIr1WUJQHE68cA4VTks2XE7nxuryaUymCEy_23-Oew/edit#gid=0){target="_blank"} から利用できます。

**驚くべき UTM ビルダーを実現**

これは、UTM タグをすばやく生成できるChrome拡張機能です。 [ こちら ](https://chrome.google.com/webstore/detail/effin-amazing-utm-builder/eoaapiimcaimddnfhfnifgkinmpcbccp?hl=en){target="_blank"} で見つけます。

## Bing Ads {#bing-ads}

Bing Ads は、URL の自動タグ付けを有効にしたり、[!DNL Marketo Measure] などのサードパーティツールを使用して広告にタグを付けたりできる統合プラットフォームです。 [!DNL Bing Ads] は UTM パラメーターにも依存します。

統合では、以下の広告タイプをサポートしています。

* テキスト広告
* モバイル広告
* テキスト広告を展開

Bing Ads の自動タグ付け機能では、次の UTM パラメーターが追加されます。

* Utm_source
* Utm_medium
* Utm_term

Bing Ads の自動タギングでは、次のカスタムパラメーターも追加されます。

`_bt={adid}`

文字列は次のようになります。

`{lpurl}?_bt={adid}&utm_term={keyword}&utm_source=Bing_Yahoo&utm_medium=CPC`

必要に応じて、最終的 [!DNL Bing Ads]URL でカスタムタグを使用して、より精度の高いパラメーターを追加できるので、注意が必要です。

必要に応じてトラッキングテンプレートを使用できますが、[!DNL Bing Ads] と [!DNL Marketo Measure] の統合は必須ではありません。 これは、履歴を変更 [!DNL Bing] ずに広告を編集でき、宛先 URL[!DNL Marketo Measure] 更新できるためです。

自動タグ付けは、カスタムの [!DNL Marketo Measure] パラメーターが自動的に追加されるように、[!DNL Marketo Measure] を通じて有効にする必要があります。 Bing Ads で過去の広告パフォーマンス履歴が失われるリスクはありません。

プラットフォームへのタグの追加について詳しくは、[[!DNL Bing Ads]](https://advertise.bingads.microsoft.com/en-us/blog/post/august-2016/upgraded-urls-now-available-in-bing-ads-an-easier-way-to-manage-your-tracking-urls){target="_blank"} の web サイトを参照してください。

## Facebook 広告 {#facebook-ads}

[!DNL Marketo Measure] と [!DNL Facebook] の統合により、広告情報を自動的にダウンロードし、URL にパラメーターをタグ付けできます。 自動タグ付 [!DNL Marketo Measure] を通じてキャンペーンと広告セットの情報を取り込みます。 広告セットが広告グループ名フィールドに表示されます。 [!DNL Facebook] プラットフォームでの URL タグの設定について詳しくは、[!DNL Facebook] [ ビジネス ](https://www.facebook.com/business/help/1016122818401732/?ref=u2u){target="_blank"} ページを参照してください。

[!DNL Facebook Ads] を使用した自動タグ付けを有効にする前に、以前のパフォーマンス履歴を CSV として書き出すことが重要です。 この時点で、_bf パラメーター [!DNL Marketo Measure] 使用してタグが [!DNL Facebook Ads] び出されると、[!DNL Facebook] は広告を新しいものとして読み取り、パフォーマンス履歴を消去します。 したがって、自分自身や組織にとって価値がある場合は、以前のパフォーマンスのレコードを書き出すことが重要です。

[!DNL Facebook] アカウントはいつでも [!DNL Marketo Measure] アプリに接続でき、データは失われません。自動タグ付けが有効な場合にのみ、パフォーマンス履歴が消去されます。

[ 広告レポートの書き出しについて詳しくは、Facebook の ](https://www.facebook.com/business/help/393890194130036){target="_blank"} この記事 [!DNL Facebook] を参照してください。

## LinkedIn スポンサー付きコンテンツ {#linkedin-sponsored-content}

LinkedIn 統合を使用 [!DNL Marketo Measure] ると、スポンサー付きコンテンツの宛先 URL[!DNL LinkedIn] タグ付けできます。これにより、[!DNL Marketo Measure] ーザーは、タッチポイントジャーニー全体を通じてユーザーを追跡し、アクティビティを特定の [!DNL LinkedIn] Campaign とCreativeにマッピングすることができます。 これにより、顧客のアクティビティの ROI に関するインサイト [!DNL LinkedIn] 顧客に提供されます。 [!DNL Marketo Measure] は、一意の [!DNL LinkedIn] Share を持つクリエイティブを検索し、その最後に `?_bl={creativeId}` パラメーターを追加します。

[!DNL LinkedIn] 共有は複数のキャンペーンおよびクリエイティブで使用できるので、一意性を維持するために、既存のクリエイティブをコピー/クローン/複製しないでください。 共有が見つかり、1 つのCreativeでのみ使用されることが検出された場 [!DNL Marketo Measure]、クリエイティブや共有を再作成する必要なく、共有にそのままタグを付けることができます。すべての広告履歴（インプレッション、クリック数、共有）は残ります。

共有が複数のクリエイティブで共有されていることが判明した [!DNL Marketo Measure]、一意のセットを作成するには、一時停止、コピー、再タグ付けのプロセスを経る必要があります。 ライブクリエイティブ [!DNL Marketo Measure] 一時停止してアーカイブします。つまり、インプレッション数、クリック数およびソーシャルシェアを含むクリエイティブもアーカイブされます。

## 非統合型プラットフォーム {#non-integrated-platforms}

[!DNL Marketo Measure] と統合されていないプラットフォームの場合、[!DNL Marketo Measure] の自動タグ付け機能は使用できません。 パラメーターは手動で追加する必要があります。
