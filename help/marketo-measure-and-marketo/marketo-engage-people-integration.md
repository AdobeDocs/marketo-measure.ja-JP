---
description: '[!DNL Marketo Engage] People 統合 –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Engage] People 統合'
exl-id: 51930e84-4ff8-4e35-9d44-ea017c24b051
feature: Integration
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 3%

---


# [!DNL Marketo Engage] People 統合 {#marketo-engage-people-integration}

Marketo人物統合を使用 [!DNL Marketo Measure] ると、Marketoから人物のダウンロードを開始し、トラッキング対象セッションと個人を結び付け、タッチポイントをエンゲージメントにマッピングできるようになります。 従来、[!DNL Marketo Measure] はタッチポイントを CRM から人物にマッピングすることしかできませんでした。そのため、マーケターはステージやトリガーを待って CRM と同期するのではなく、マーケティング活動を迅速に測定できます。

## 要件 {#requirements}

* 実稼動Marketo インスタンス
* 実稼動 [!DNL Salesforce] または実 [!DNL Microsoft Dynamics] 動インスタンス
* 任意の有料 [!DNL Marketo Measure] サブスクリプション
* SOLR を有効にする（これを有効にするには [&#128279;](https://nation.marketo.com/t5/Support/ct-p/Support){target="_blank"}Marketo サポートにお問い合わせください）

## 仕組み {#how-it-works}

現在のお客様は、既にお使 [!DNL Marketo Measure] の CRM からユーザーをダウンロードしています。 標準的なプロセスでは、[!DNL Marketo Measure] がユーザーをダウンロードし、メールアドレスを bizible.js で追跡した web セッションにマッピングします。

Marketoのユーザーのダウンロードが導入され、[!DNL Marketo Measure] は、CRM と同期されていない個人の大規模なプールに web セッションをマッピングできるようになりました。 これは通常、ユーザーが特定のステータスに達するまで待機した後に CRM にプッシュされる内部プロセスが原因です。

Marketo ユーザーを web セッションに正常にマッピングする [!DNL Marketo Measure]、アドビの処理により、関連するタッチポイントが生成され、最終的に [!DNL Marketo Measure Discover] でレポート可能になります。 そのMarketo ユーザーが CRM にプッシュされ [!DNL Marketo Measure] 場合、重複するシナリオを処理し、CRM ユーザーのタッチポイントを再作成して、最初のセットを「重複」としてマークします。

これらの重複を検出するために、[!DNL Marketo-Salesforce] または [!DNL Marketo-Dynamics] sync がMarketo Person のリード ID および連絡先 ID に入力されていることを確認します。 ID が正しく同期されている場合は、次のように、人物レコードに CRM ID が表示されます。

![a](assets/5a.png)

![b](assets/5b.png)

お客様は、[!DNL Marketo Measure] Discover 内でMarketo ユーザーと CRM ユーザーの完全なセットをレポートするオプションがあります。 CRM 人物のみのレポートに関心がある場合は、セグメントを作成してフィルタリングすることをお勧めします。

## [!DNL Marketo Measure Discover] {#marketo-measure-discover}

[!DNL Marketo Measure Discover] でリード（人物）に関するレポートを作成する場合、Marketoと CRM のリードの合計が表示されます。 Marketoの人物または CRM リードのみを対象としてレポートする場合は、ソースのセグメントカテゴリを作成してから、「Source システム」フィールドを使用してMarketoと CRM のセグメントルールを作成します。 セグメントを作成すると、Source カテゴリが表示され、[!DNL Marketo Measure Discover] のダッシュボードでフィルタリングできるようになります。

![Marketoと CRM リードの合計を表示するMarketo Measure Discover ダッシュボード &#x200B;](assets/bizible-discover-1.png)

![Source システムセグメントをハイライトしたフィルターの確認 &#x200B;](assets/bizible-discover-2.png)

## フィールド マッピング {#field-mappings}

<table>
 <colgroup>
  <col>
  <col>
 </colgroup>
 <tbody>
  <tr>
   <th><p><strong>biz_リード</strong></p></th>
   <th><p><strong>Marketo</strong></p></th>
  </tr>
  <tr>
   <td><p>ID</p></td>
   <td><p>id</p></td>
  </tr>
  <tr>
   <td><p>MODIFIED_DATE</p></td>
   <td><p>updatedAt<strong></strong></p></td>
  </tr>
  <tr>
   <td><p>CREATED_DATE</p></td>
   <td><p>createdAt</p></td>
  </tr>
  <tr>
   <td><p>EMAIL</p></td>
   <td><p>email</p></td>
  </tr>
  <tr>
   <td><p>WEB_SITE</p></td>
   <td><p>website</p></td>
  </tr>
  <tr>
   <td><p>COMPANY</p></td>
   <td><p>company</p></td>
  </tr>
  <tr>
   <td><p>IS_CONVERTED</p></td>
   <td><p>該当なし</p></td>
  </tr>
  <tr>
   <td><p>ACCOUNT_ID</p></td>
   <td><p>アカウント Id （L2A）</p></td>
  </tr>
  <tr>
   <td><p>BIZIBLE_STAGE</p></td>
   <td><p>ステータス</p></td>
  </tr>
  <tr>
   <td><p>IS_DELETED</p></td>
   <td><p>true/false</p></td>
  </tr>
 </tbody>
</table>

*Marketo会社エンティティのフィールドがユーザーの updatedAt 値に影響を与えない既知の動作問題があるので、web サイトや会社などの関連フィールドが更新され [!DNL Marketo Measure] と、updatedAt の日時の値が更新されないので、これらの値が変更されないことがわかります。 これは ABM 機能に影響を与えます。この機能では、リードのアカウントを解決するための新しいデータはありません。 現時点では回避策はありませんが、今後この問題に対処する予定です。

## よくある質問 {#faq}

**CRM と [!DNL Marketo Measure Discover] でリード数が異なるのはなぜですか？**

この統合により、Marketoから直接読み込んだリードに対してタッチポイントを作成できるので、CRM に同期されなかったリードが存在する可能性があり、タッチポイントは CRM リードに対してのみプッシュされるので、Discover 内のカウントが CRM よりも多くなる可能性があります。

**これはデータにどのように置き換わりますか？**

この統合は、現在の [!DNL Marketo Measure] インスタンス内のデータセットを実際に結合するので、何も置き換えられません。 現在の CRM リードに期待されるのは、2 年分のMarketo リードをダウンロードする際に、そのリードレコードを更新するだけで、Marketo リードとも一致していることを示すことです。 すべてがバックエンドで発生し、タッチポイントは同じままであることが予想されます。 また、適格なMarketo リードにより、タッチポイントがより多く表示されることも予想されます。 これらのMarketoのユーザーに一致する web セッションが見つかれば、[!DNL Marketo Measure] でカウントされたタッチポイントが表示され始めます。

**ユーザーをMarketoからダウンロードして、CRM 接続を切断することしかできますか？**

現時点では、できません。 今後もこの方法を使用できますが、Marketoから [!DNL Marketo Measure] にプログラム、オポチュニティ、取引を結び付けられるように、このMarketo統合の他のフェーズを構築する必要があります。

**Marketoのユーザーをすべて読み込みますか？**

現時点では、2018 年 1 月 1 日からユーザーをインポートするのが最も早いので、2 年以上のデータがあります。これは、CRM ダウンロードから適用するのと同じ動作です。 Marketoの接続が確立されると、2 年間の周期的な時間枠をダウンロードするように、改善された動作を実装します。

また、あらゆる人物タイプに対してフィルターを適用しないので、2 年以内のすべての人物が読み込まれ、タッチポイントの対象になります。

**SOLR とは何ですか？また、この機能を使用するために SOLR を有効にする必要があるのはなぜですか？**

Marketo インスタンスに対して SOLR を有効にする手順は、Marketoのハードウェア領域を解放する簡単な手順です。これにより、サブスクリプションで [!DNL Marketo Measure] 統合を利用できるようになります。 SOLR が有効になっていない場合、Marketo インスタンスから適切なユーザーをダウンロードすることが可能となる特定の呼び出しにはアクセスできません。
