---
unique-page-id: 35586080
description: LinkedInの統合 –  [!DNL Marketo Measure]
title: LinkedInの統合
exl-id: 705209ef-1ece-496c-ac2f-6a31055bd993
feature: APIs, Integration
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '2653'
ht-degree: 1%

---

# LinkedInの統合 {#linkedin-integration}

## 概要 {#overview}

linkedInとの [!DNL Marketo Measure] 統合は、次の 2 つの部分に分かれます。

スポンサードコンテンツ：スポンサードコンテンツ統合を使用 [!DNL Marketo Measure] ると、[!DNL LinkedIn] 広告の宛先 URL をタグ付けすることができます。これにより、最終的に、ユーザーがタッチポイントジャーニー全体を通じて [!DNL Marketo Measure] ーザーを追跡し、アクティビティを特定の [!DNL LinkedIn] Campaign およびクリエイティブにマッピングし直すことができます。 これにより、顧客のアクティビティの ROI に関するインサイト [!DNL LinkedIn] 顧客に提供されます。

リード生成Forms: LinkedInのリード生成Formsとの統合を通じて、Marketo MeasureはLinkedIn プラットフォームを通じて送信されたフォームに関するインサイトを得ます。 これらのフォーム入力は、CRM または [!DNL Marketo Engage] インスタンスからのリードと照合され、属性の対象となります。 キャンペーン、クリエイティブ、フォームを生成するのに役立つフォームに関するインサイトを活用して、チームはLinkedInのマーケティングと広告費用をさらに最適化できるようになりました。

## 利用可能性 {#availability}

すべてのユーザーが利用できます。

## 要件 {#requirements}

**キャンペーンマネージャーの役割**

広告データ [!DNL Marketo Measure] 広告コストデータをダウンロードするには、Campaign マネージャーで次のいずれかの役割が必要です。

* 請求管理者
* アカウントマネージャ
* キャンペーンマネージャー

詳細情報：[Campaign Manager のユーザーの役割と機能 ](https://www.linkedin.com/help/lms/answer/a425731/user-roles-and-functions-in-campaign-manager)。

**有料メディア管理者ロール**

スポンサークリエイティブを作成/更新するには、次のいずれかの有料メディア管理者ロールが [!DNL Marketo Measure] 要です。

* スポンサーコンテンツのポスター
* リード生成Forms マネージャー

詳細情報：[LinkedInページの管理者ロール ](https://www.linkedin.com/help/linkedin/answer/4783/linkedin-page-admin-roles-overview)。

他にも、統合に必要な [!DNL LinkedIn] の役割が **ありません**。 これらの役割は、多くの場合、必要な役割と誤解されているので、違いがあることに注意してください！

**ページ管理者の役割**

リード生成フォーム [!DNL Marketo Measure] リードをダウンロードまたは統合するには、次のページ管理者の役割が必要です。

* スーパー管理者

詳細情報：[LinkedInページの管理者ロール ](https://www.linkedin.com/help/linkedin/answer/4783/linkedin-page-admin-roles-overview)。

## LinkedIn広告タイプ {#linkedin-ad-types}

[!DNL Marketo Measure] は以下をサポートします。

**スポンサードコンテンツ：** スポンサードコンテンツを使用すると、会社をフォローしているメンバー以外のメンバーの [!DNL LinkedIn] フィードにもコンテンツを配信できます。 スポンサー付きコンテンツは、特定のオーディエンスをターゲットにすることができ、広告主がデスクトップ、モバイル、タブレット全体の [!DNL LinkedIn] プラットフォームでエンゲージメントを行っている場所と時間に [!DNL LinkedIn] ーザーメンバーにリーチするのに役立ちます。 リード生成Formsによるスポンサー付きコンテンツがサポートされます。

[!DNL Marketo Measure] がサポートするスポンサー付きコンテンツ広告の種類は、シングル画像広告とビデオ広告（リード生成Formsを通して）です。 スキーマが複雑なため、カルーセル広告はサポートされていません。

[!DNL Marketo Measure] は、スポンサー付きメッセージ、テキスト広告、動的広告をサポートしていません。

![](assets/one.png)

>[!TIP]
>
>スポンサーのないコンテンツソースに基づくキャンペーンや支出（「テキスト広告」や「スポンサー付きインメール」のキャンペーンタイプなど）の場合、[!DNL Marketo Measure] れらのキャンペーンタイプのトラッキングは本質的にはサポートされません __。 このようなキャンペーンの支出を「スポンサーコンテンツ」の支出と並べて追跡したい場合は、マーケティング支出 CSV を使用して、その支出を手動で記録してください。

## 仕組み：スポンサードコンテンツ {#how-it-works-sponsored-content}

>[!NOTE]
>
>最初に使用する前に、[!DNL Marketo Measure][!UICONTROL  設定 ]/[!UICONTROL  統合 ]/[!UICONTROL Ads]/[!UICONTROL LinkedIn リード生成Formsを有効にする ] に移動して、この機能設定を有効にする必要があります。

**[!DNL LinkedIn's]独自の自動タグ付けの要件**

ランディングページ [!DNL Marketo Measure] 自動タグ付けされるので、[!DNL LinkedIn] campaign のパフォーマンスを追跡するのに役立ちます。

一意 [!DNL Marketo Measure]LinkedIn Share を持つクリエイティブを検索し、その末尾に `?_bl={creativeId}` パラメーターを追加します。

**株式の複製**

この [!DNL Marketo Measure/LinkedIn] 統合では、既存のクリエイティブをコピー/クローン/複製しないでください。 共有が見つかり、1 つのクリエイティブでのみ使用されてい [!DNL Marketo Measure] ことが検出された場合、クリエイティブや共有を再作成しなくても、共有にそのままタグを付けることができます。すべての広告履歴（インプレッション、クリック数、共有）が残ります。

共有が複数のクリエイティブで共有されていることが判明した [!DNL Marketo Measure]、一意のセットを作成するには、一時停止、コピー、再タグ付けのプロセスを経る必要があります。 [!DNL Marketo Measure] は、ライブクリエイティブを一時停止してアーカイブするので、インプレッション数、クリック数、ソーシャルシェアを含む広告履歴を消去して、すべてを適切に自動タグ付けします。

[!DNL Marketo Measure] 今後は、[!DNL LinkedIn] の共有を複製せず、すべてのクリエイティブと共有をできるだけ一意に保つことをお勧めします。これにより、広告履歴を消去することなく、トラッキングを簡単に追加できます。

**短縮 URL**

余分な手順が必要な理由は、LinkedInではリンク先 URL を短縮 URL （bit.ly、goog.le など）にできるため、長く解決された URL は表示されず、解決され [!DNL Marketo Measure]URL にトラッキングパラメーターを追加する必要が [!DNL Marketo Measure] るからです。 この問題を回避するには、広告を再作成す [!DNL Marketo Measure] 前に短縮 URL を検索し、URL を展開してから、解決された URL とそのすべてのパラメーターを含む新しい広告を作成し、タグを追加で [!DNL Marketo Measure] ます。 新しい広告を作成すると、広告履歴（インプレッション数、クリック数、共有）が消去されるので、短縮 URL にタグ付けする権限が必要になります。

短縮 URL を頻繁に使用すると、クリエイティブに大きな影響を与える可能性があります。 新しい広告を作成したり広告履歴を消去したりせずにランディングページにタグを付け [!DNL Marketo Measure] きるように、短縮 URL を使用しないことをお勧めします。

**プロセス**

それでは、いくつかの例から始めましょう。 持っていると言ってみましょう…

クリエイティブ A：共有 123\
クリエイティブ B：共有 234\
クリエイティブ C：共有 234\
クリエイティブ D：共有 234

![](assets/two.png)

`1)` [!DNL Marketo Measure] では、最初に「アクティブ」ステータスのすべてのキャンペーン、クリエイティブ、共有を確認します。 [!DNL Marketo Measure] は、一時停止、アーカイブまたはキャンセルされた広告をタグ付けしません。 広告が一時停止していた場合に「[!UICONTROL  アクティブ ]」に設定すると、再びアクティブになった時点でタグが付けられます。 一意の共有が見つかった場合、つまり複数のクリエイティブまたはキャンペーンで使用されていない場合（例：クリエイティブ A : Share 123）、カスタムパラメーター `>> ?_bl={creativeId}` を共有 URL に追加し [!DNL Marketo Measure] す。

`2)` ここで、共有が共有されて一意性が失われた場合（例えば、クリエイティブ B は 234 を共有、クリエイティブ C は 234 を共有、クリエイティブ D は 234 を共有）、[!DNL Marketo Measure] は類似したすべてのクリエイティブ（クリエイティブ B、クリエイティブ C およびクリエイティブ D）を一時停止してアーカイブします。

`3)` [!DNL Marketo Measure] では、アーカイブされるクリエイティブ B のコンテンツをコピーする 3 つの新しいクリエイティブ（クリエイティブ E、クリエイティブ F、クリエイティブ G）を作成します。

`4)` [!DNL Marketo Measure] はまた、Share 234 の内容をコピーする 3 つの新しい共有（Share 345、Share 456 および Share 567）を作成しますが、独自の `?_bl` タグ付けが用意されています。

`5)` [!DNL Marketo Measure] は、共有が共有されないことを定期的に確認する必要があります。共有される場合は、上記の手順 2 でプロセスを再開します。

>[!NOTE]
>
>これを実装すると、お客様はクリエイティブ B の広告履歴を失います。Share 234、Creative C : Share 234 および Creative D : Share 234 は、Creative E : Share 345、Share F : Share 456 および Creative G : Share 567 にそれぞれ再作成されるので、これらは共有されません。

![](assets/three.png)

## 仕組み：リード生成Forms {#how-it-works-lead-gen-forms}

**[!DNL LinkedIn's]独自の自動タグ付けの要件**

ランディングページ [!DNL Marketo Measure] 自動タグ付けされるので、[!DNL LinkedIn] campaign のパフォーマンスを追跡するのに役立ちます。

一意 [!DNL Marketo Measure]LinkedIn Share を持つクリエイティブを検索し、その末尾に `?_bl={creativeId}` パラメーターを追加します。

**プロセス**

Ad Form API[!DNL LinkedIn's]Ad Form Response API を通じて、広告アカウントのフォーム送信データを収集し、メールアドレスを CRM またはMarketoのリードに関連付けることができます。

LinkedIn フォームには、複数のメールアドレスを含めることができます。 フォームの回答をダウンロードすると、仕事用メール、メールアドレス（プライマリフォームフィールド）、または有効なメール値を持つカスタムフィールドの優先度を持つメールアドレスが検索されます。

キャンペーンやクリエイティブのステータスに関係なく、すべてのフォームの応答はタッチポイントになります。 [!DNL Marketo Measure] には 90 日間のルックバック制限が [!DNL Marketo Measure] り、90 日を経過したフォーム応答にアクセスできませんが、[!DNL Marketo Measure] と [!DNL LinkedIn] の統合が有効になっている期間が長いほど、[!DNL Marketo Measure] を通じて多くのリード生成フォームタッチポイントが表示されます。

>[!NOTE]
>
>LinkedInの費用は、スポンサー付きコンテンツキャンペーンの一部として引き続きダウンロードされます。

**CRM またはMarketoでのリード生成Formsのトラッキング**

[!DNL Marketo Measure] とLinkedIn リード生成のForms統合が存在する前は、お客様はフォーム送信をMarketo プログラムや CRM キャンペーンにプッシュしてフォームをトラッキングし、これらのアクティビティに関するアトリビューションを受け取るのが一般的でした。 リード生成Forms設定が有効になったら、これらのフォーム送信が二重にカウントされないようにする必要があります。 次の点を確認してください。

* CRM オブジェクトの「購入者タッチポイントを有効にする」フィールドが「なし」または「すべてのキャンペーンメンバーを除外」に設定されている
* 関連するMarketo プログラムまたはMarketo アクティビティルールを更新します
* 関連する CRM キャンペーンルールを更新

>[!NOTE]
>
>linkedIn API には 90 日間のルックバック制限があるので、Marketoまたは CRM ルールを使用している場合、ルールの終了日を、[!DNL Marketo Measure] で統合を有効にした日付より 90 日前に設定することをお勧めします。

## Touchpoint の詳細 {#touchpoint-details}

[!DNL Marketo Measure] がLinkedIn クリエイティブでランディングページに正常にタグ付けされたら、タッチポイントで解決済みの広告データを確認できます。 表示されるはずのデータ値のマッピングを次に示します。

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th style="width:30%">タッチポイントフィールド</th> 
   <th>サンプル値</th> 
  </tr> 
  <tr> 
   <td>広告 Id</td>
   <td>84186224</td>
  </tr> 
  <tr> 
   <td>広告コンテンツ</td>
   <td>copy-1-image-2-man マーケターの 95%#B2B、需要創造戦略が成功したと考えています。 詳細情報：[!DNL https]://lnkd.in/jgdi50vKrgv</td>
  </tr> 
  <tr> 
   <td>広告グループ Id</td>
   <td>(空白)</td>
  </tr> 
  <tr> 
   <td>広告グループ名</td>
   <td>(空白)</td>
  </tr> 
  <tr> 
   <td>広告キャンペーン Id</td>
   <td>138949954</td>
  </tr> 
  <tr> 
   <td>広告キャンペーン名</td>
   <td>SU - COM Accounts - Demand Skills</td>
  </tr> 
  <tr> 
   <td>広告宛先 URL <b>*</b></td>
   <td>https://www.adobe.com/marketing-attribution-for-demand-generation-leaders?_bl=84186217</td> 
  </tr> 
  <tr> 
   <td>フォーム/URL</td> 
   <td>info.bizible.com/demo</td> 
  </tr> 
  <tr> 
   <td>フォーム URL – 未加工</td> 
   <td>info.bizible.com/demo</td> 
  </tr> 
  <tr> 
   <td>キーワード Id</td> 
   <td>(空白)</td> 
  </tr> 
  <tr> 
   <td>キーワード一致タイプ</td> 
   <td>(空白)</td> 
  </tr> 
  <tr> 
   <td>ランディングページ</td> 
   <td>https://www.adobe.com/marketing-attribution-for-demand-generation-leaders</td> 
  </tr> 
  <tr> 
   <td>ランディングページ – 未加工</td> 
   <td>https://www.adobe.com/marketing-attribution-for-demand-generation-leaders?_bl=84186217</td> 
  </tr> 
  <tr> 
   <td>マーケティングチャネル</td> 
   <td>有料ソーシャル</td> 
  </tr> 
  <tr> 
   <td>マーケティングチャネル – パス</td> 
   <td>ペイドソーシャル。LinkedIn</td> 
  </tr> 
  <tr> 
   <td>中</td> 
   <td>「cpc」または「リード生成フォーム」</td> 
  </tr> 
  <tr> 
   <td>参照元ページ</td> 
   <td>www.linkedin.com/</td> 
  </tr> 
  <tr> 
   <td>参照元ページ – 未加工</td> 
   <td>www.linkedin.com/</td> 
  </tr> 
  <tr> 
   <td>フレーズを検索</td> 
   <td>(空白)</td> 
  </tr> 
  <tr> 
   <td>Touchpoint のタイプ</td> 
   <td>ウェブフォーム</td>
  </tr> 
  <tr> 
   <td>Touchpoint ソース</td>
   <td>LinkedIn</td>
  </tr> 
 </tbody> 
</table>

**&#42;**_「広告宛先 URL」フィールドは、スポンサー付きコンテンツの場合にのみ入力されます。 リード生成Forms用には入力されません。_

<br>

## コスト {#costs}

[!DNL Marketo Measure] は [!DNL LinkedIn] と直接統合されているので、キャンペーンとクリエイティブごとに記録された支出を毎日ダウンロードします。 お客様が [!DNL Marketo Measure] アプリケーション内の [!DNL LinkedIn] 費用についてレポートする必要はなくなりました。

他の広告統合と同様に、[!DNL Marketo Measure] では、すべてのキャンペーン、クリエイティブ、コストを配置するマーケティングチャネルルール [!DNL LinkedIn] 定義しています。 このルールを使用するには、顧客が有料 [!DNL LinkedIn] ールの取り組みに新しい行を挿入する必要があります。 新規または既存のチャネルを指定できます。 リファラー列で、[!DNL Marketo Measure] タグを持つ任意のタッチポイントとして定義し [!DNL Marketo Measure] 定義「[[!DNL LinkedIn] Paid]」を使用します。

![](assets/four.png)

## [!DNL Marketo Measure] Discover {#marketo-measure-discover}

リード生成のForms レポートをサポートするために、[!DNL Marketo Measure] Discover にいくつかの機能強化が行われました。

**ペイドメディアボード**

リード生成Forms タイル：LinkedInのフォーム入力数を含む新しいタイルです。 このカウントのドリルスルーでは、アクティビティ ID、フォーム日、フォーム名、および電子メールアドレスが表示されます。

**係合パスボード**

イベントのジャーニー：統合を通じて取得されるフォーム用に、「アクティビティ」イベントタイプと中程度の「リード生成フォーム」が含まれます。 ドリルスルービューには、キャンペーン、クリエイティブ、フォームの詳細が含まれます。

## スポンサー付きコンテンツに関するよくある質問 {#sponsored-content-faq}

**暗い分け前とは何ですか？**

ダークシェアとは、会社のページに投稿されず、すぐにクリエイティブとして作成されて直接追加される投稿です。 作成 [!DNL Marketo Measure] れたクリエイティブが会社のページの上部に表示されず、再び昇格しないように、暗いシェアを使用して背後で立ち上げることができます。

**実際にはどのステータス [!DNL Marketo Measure] タグ付けされますか？**

[!DNL LinkedIn] Campaign とクリエイティブには、アクティブ、一時停止、アーカイブ済み、キャンセルの 4 種類のステータスがあります。 アクティブなキャンペーンとクリエイティブにのみタグを付けます。 他のステータスをタグ付けすると、再度アクティブに設定されます。 [!DNL Marketo Measure] では、一時停止、アーカイブ、キャンセルされたキャンペーンやクリエイティブのタグ付けは行われませんが、ステータスがアクティブに変わると、タグ付けが再開されます。

**[!DNL Marketo Measure] がタグ付けに使用している値は何ですか？**

宛先 URL の末尾に、パラメーター `&_bl={creativeId}`[!DNL Marketo Measure] 追加されます。`{creativeId}` はLinkedInのクリエイティブ ID です。 クリエイティブ ID を使用 [!DNL Marketo Measure] ると、各クリエイティブが 1 つのキャンペーンにのみ属す [!DNL LinkedIn] ことができるので、非常に基本的な広告構造を持つので、キャンペーン ID を決定することもできます。

**古いクリエイティブで新しいバージョン [!DNL Marketo Measure] 作成するとどうなりますか？**

共有 [!DNL Marketo Measure] 再作成して新しいクリエイティブに配置すると、古いクリエイティブがアーカイブされます。 これが、アーカイブされ [!DNL Marketo Measure] キャンペーンやクリエイティブにタグ付けしない理由でもあります。そうしないと、[!DNL Marketo Measure] が無期限にタグ付けしようとしてループします。

**作成した広告の宛先 URL が元の広告と一致しないのはなぜですか？**

解決され [!DNL Marketo Measure]URL にトラッキングパラメーターを追加する必要がありますが、API で提示される URL は、すべてのパラメーターが存在しない短縮 URL にすることができます。 この問題を回避するために、[!DNL Marketo Measure] は追加を再作成する前に短縮 URL を検索し、解決してから、解決された URL とそのすべてのパラメーターを使用して新しい広告を作成し、タグを追加で [!DNL Marketo Measure] ます。

**広告にタグを付けていますか？ すべてのランディングページに bl パラメーターが表示されません。**

一部のマーケターが、タグ付けできない宛先 URL に画像リンクを配置し [!DNL Marketo Measure] いるので、広告コンテンツ内で URL を検索します。 短縮 URL にタグ付 [!DNL Marketo Measure] する権限がある場合は、URL を展開してタグ付けしますが、LinkedInのコピー構造により、テキスト内で自動的に短縮されます。 タグは、LinkedIn短縮 URL 内に存在します。この URL は、ランディングページ – 未加工フィールドではなく、タッチポイントの「広告コンテンツ」フィールドに表示されます。

**いやいや、私のチームの誰かが誤って共有をクローンしました。 一時停止してもいいですか**

心配しないで。 [!DNL Marketo Measure] は、プログラムによって、一意でなくなった（つまり、別のクリエイティブにコピーされた）共有をチェックします。 そのコピーが検出され [!DNL Marketo Measure] ら、通常のフローに従ってタグ付けし、新しい広告を作成します。

**以前、広告のレビューが保留になっていました。 タグ付け後にレビューが再び保留 [!DNL Marketo Measure] れるのはなぜですか？**

LinkedInでは、作成または変更されたすべての広告は、投稿される前に通常のセキュリティプロセスを経る必要があります。 [!DNL Marketo Measure] は、6 時間ごとに新しい広告をスキャンするので、できるだけ早く広告を傍受しようとしますが、追加の手順 [!DNL LinkedIn's] 伴い、ローンチを数時間遅らせる可能性があります。

**広告に 2 つの URL があります。 タグ付けされるのはどれ**

両方。 [!DNL Marketo Measure] 統合により、広告のクリックスルー画像から宛先 URL にタグを付けることができますが、広告の説明の短縮 URL も自動的に更新されます。

![](assets/five.png)

**[!DNL LinkedIn ads] アカウントを接続しました。 リンクにタグ [!DNL Marketo Measure] 付けないのはなぜですか？**

接続した [!DNL LinkedIn] ユーザーは適切な編集アクセス権を持っている必要があります。つまり、ユーザーはアカウントマネージャー、キャンペーンマネージャーまたはクリエイティブマネージャーである必要があります。

**自分のクリエイティブがコピーされるかどうかを知るにはどうすればよいですか？ クリエイティブが同じシェアを使用しているかどうかを確認することはできますか？**

共有 ID は [!DNL LinkedIn] レポートでは提供されていないので、クリエイティブと共有のマッピングを確認する明確で明白な方法はありません。 クリエイティブがコピーである可能性が疑われる場合は、[!DNL LinkedIn] Campaign マネージャーで広告を開いて手動で確認できます。新しいタブで広告が開き、URL で共有 ID を確認できます。

![](assets/six.png)

## リード生成Formsに関するよくある質問 {#lead-gen-forms-faq}

**この機能強化のコストはどれくらいですか？**

このオファリングは、有料の [!DNL Marketo Measure] サブスクリプションに含まれています。

**統合は遡及的ですか？**

はい、過去の広告フォームの応答をLinkedInからダウンロードしますが、90 日間のルックバックウィンドウに制限されています。 [!DNL Marketo Measure] とLinkedInの統合が有効になっている期間が長いほど、[!DNL Marketo Measure] を通じてリード生成フォームのタッチポイントが多く表示されます。

ダウンロードする特定の日付を設定するオプションはありませんが、抑制する必要があるタッチポイントがある場合は、オプションでタッチポイント削除ルールを設定できます。

**既に [!DNL Marketo Measure] LinkedIn広告統合を使用している場合、これは自動的に有効になりますか？**

いいえ、すべてのお客様に対して自動的にダウンロードを開始するわけではありませんが、この機能を設定で有効にするための非常に簡単なスイッチです。

**フォームデータは使用できますか？**

フォームデータは、フォーム ID とフォーム名を含む [!DNL Marketo Measure] Discover を通じて利用できます。 CRM のタッチポイントオブジェクトでは、まだフォームの詳細を使用できません。

**以前にMarketo プログラムまたは CRM キャンペーンと同期されていた [!DNL LinkedIn] リードはどうなりますか？**

重複を避けるために、[!DNL Marketo Measure] のルールを調整して、これらの特定のプログラムやキャンペーンからタッチポイントを生成することをお勧めします。 linkedIn API には 90 日間のルックバック制限があるので、Marketoまたは CRM ルールを使用している場合、ルールの終了日を、[!DNL Marketo Measure] で統合を有効にした日付より 90 日前に設定することをお勧めします。 これ以降は、より多くのインサイト [!DNL Marketo Measure] 詳細を得ながら、これらのリードをダウンロードできます。

**自動タグ付けやトラッキングは含まれていますか？**

いいえ、これは他の [!DNL Marketo Measure] 統合とは異なります。 ランディングページの変更（ランディングページへのクリックスルーがないので）ではなく、LinkedInから関連情報をダウンロードして [!DNL Marketo Measure] 内のアクティビティとして扱うだけです。
