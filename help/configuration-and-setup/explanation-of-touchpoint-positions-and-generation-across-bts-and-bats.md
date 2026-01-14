---
description: BT をまたいだタッチポイントの位置と生成の説明およびMarketo Measure ユーザー向けのガイダ  [!DNL BATs]  ス
title: BT と [!DNL BATs] にわたる Touchpoint の位置と生成の説明
exl-id: 4903f917-a366-4767-a126-5216d2377399
feature: Touchpoints
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 3%

---


# BT と [!DNL BATs] 間でのタッチポイント位置と生成の説明 {#explanation-of-touchpoint-positions-and-generation-across-bts-and-bats}

**タッチポイントポジションの作成とバイヤージャーニーの流れ**

データを使用してレポートを正常に作成するには、Buyer Touchpointのポジションとそのトリガー方法 [!DNL Marketo Measure] 理解することが重要です。 見込み客が購入者のジャーニーを進む際にどのような行動を取り、タッチポイントデータでどのように表示されるかを明確に理解する必要があります。 このトピックについて詳しくは、「タッチポイントの生成とマッピング [[!UICONTROL  の記事を確認するこ ]](/help/configuration-and-setup/touchpoint-generation-and-mapping.md) をお勧めします。

[!DNL Marketo Measure] には、バイヤージャーニーの様々なステップによってトリガーされる様々なタッチポイントのポジションがあります。 [!DNL Marketo Measure] データのレポートには、バイヤータッチポイント（BT）とバイヤ属性タッチポイント（BAT）の 2 つのタッチポイントデータのセットがあります。 これらのデータセットは、異なるオブジェクトに関連するため、位置が若干異なる場合があります。 このトピックについて詳しくは、[ バイヤータッチポイント（BT）とバイヤ属性タッチポイント（BAT）の違い ](/help/configuration-and-setup/difference-between-buyer-touchpoints-and-buyer-attribution-touchpoints.md) の記事を確認することをお勧めします。

**買い手タッチポイント（BT）**：これらは、個々のユーザーとそのジャーニーに関連付けられたタッチポイントであり、その個人に固有になります。 次の標準提供レポートは、Buyer Touchpoint データに基づいて作成されます。

* [!DNL Marketo Measure] 101:ID 別のリード
* [!DNL Marketo Measure] 101：チャネル別のリード
* [!DNL Marketo Measure] 101：リード/取引先責任者（ID 別）
* [!DNL Marketo Measure] 101：チャネル別のリード/担当者

次に、個人のジャーニーの場所と、その役職を得るために実行したアクションを説明するBuyer Touchpointの役職の概要を示します。

<table>
 <tbody>
  <tr>
   <th>Buyer Touchpoint（BT）の位置づけ</th>
   <th>タッチポイントタイプ（タッチポイントをトリガーできるアクション）</th>
   <th>タッチポイントの説明</th>
  </tr>
  <tr>
   <td>ファーストタッチ（FT）</td>
   <td>ウェブ訪問</td>
   <td>個人がブランドと行う最初のマーケティングインタラクション</td>
  </tr>
  <tr>
   <td>リード作成（LC）</td>
   <td>フォーム入力 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>最初のフォームは、個人が持つ項目（通常はフォーム送信ですが、キャンペーン/プログラムを含めることもできます）を入力します</td>
  </tr>
  <tr>
   <td>ポスト LC</td>
   <td>フォーム入力 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>LC （または後続のキャンペーン/プログラムを含める）の後に個人が完了するフォーム</td>
  </tr>
 </tbody>
</table>

**バイヤー属性タッチポイント（BATS）**：これは、商談とそのジャーニーに関連付けられているタッチポイントです。 これらのタッチポイントは、商談とその連絡先に接続されているため、収益に接続されています。 次の標準提供レポートは、Buyer Attribution Touchpoint データに基づいて作成されます。

* [!DNL Marketo Measure] 101：商談（ID 別）
* [!DNL Marketo Measure] 101:ID チャネル別の商談

<table>
 <tbody>
  <tr>
   <th>Buyer Attribution Touchpoint（BAT）ポジション</th>
   <th>タッチポイントタイプ（タッチポイントをトリガーできるアクション）</th>
   <th>タッチポイントの説明</th>
  </tr>
  <tr>
   <td>ファーストタッチ（FT）</td>
   <td>ウェブ訪問</td>
   <td>連絡先がブランドと行った最初のマーケティングインタラクション</td>
  </tr>
  <tr>
   <td>リード作成（LC）</td>
   <td>フォーム入力 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>連絡先に最初に入力されたフォーム（通常はフォーム送信ですが、キャンペーン/プログラムに含まれる場合もあります）</td>
  </tr>
  <tr>
   <td>オポチュニティの作成</td>
   <td>フォーム入力 <strong>OR</strong> Web 訪問 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>商談の作成時に最も近いマーケティングインタラクション</td>
  </tr>
  <tr>
   <td>クローズ済み/失注</td>
   <td>フォーム入力 <strong>OR</strong> Web 訪問 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>商談がクローズ済み（受注または失注）の場合に最も近いマーケティングインタラクション</td>
  </tr>
  <tr>
   <td>ミドルタッチ</td>
   <td>フォーム入力 <strong>OR</strong> キャンペーン/プログラムを含める</td>
   <td>連絡先がオンラインフォームに入力し、マイルストーンタッチポイントと一致しない場合</td>
  </tr>
 </tbody>
</table>

[!DNL Marketo Measure] には、個人のジャーニーとオポチュニティを明確に理解するための、これら 2 つのタッチポイントデータのセットがあります。 これらの 2 つのタッチポイントデータセットを使用すると、funnelの上部からfunnelの下部に何が起こったかを明確に把握できます。

次の例は、バイヤータッチポイント（BT）からバイヤ属性タッチポイント（BAT）へのデータのフローを示しています。 この例では、ユーザー A とユーザー B は、両方とも同じ Opportunity の一部で、作成日は 2020 年 3 月 7 日、クローズ日は 2020 年 5 月 6 日です。

**ユーザー A** Buyer Touchpoint データセット

* ファーストタッチ（FT） – 有料検索.AdWords - 2019 年 9 月 1 日（PT）
* リード作成（LC） – オーガニック検索Google - 2019 年 11 月 20 日
* Post LC （フォーム入力） – ウェビナー – 2020 年 3 月 4 日（PT）

**ユーザー B** Buyer Touchpoint データセット

* ファーストタッチ（FT） – ペイドソーシャル.Facebook - 8/26/2019
* リード作成（LC） – オーガニック検索。Yahoo - 2020 年 2 月 20 日
* Post LC （フォーム入力） – メール - 2020 年 5 月 1 日（PT）

**商談** Buyer Attribution Touchpointのデータは次のように読まれます…

* ファーストタッチ（FT） – ペイドソーシャル.Facebook - 8/26/2019
   * （アカウント **商談** 真の _ファーストタッチ_ を持っているので、ユーザー B から）
* リード作成（LC） – オーガニック検索Google - 2019 年 11 月 20 日
   * （アカウント/商談の真の **リード作成** を持っているので、_ユーザー A_ から）
* オポチュニティの作成（OC） – ウェビナー – 2020 年 3 月 4 日（PT）
   * （**ユーザー A** からの Post LC タッチポイントは、2020 年 3 月 7 日（PT）に作成される商談に対する最新のインタラクションであったので、_OC タッチポイント_ になります）
* 受注案件 – メール - 2020 年 5 月 1 日（Pt）
   * （**人物 B** からの投稿 LC タッチポイントは、商談が 2020 年 5 月 6 日にクローズされる必要がある最新のインタラクションであったので、_クローズ済み受注タッチポイント_ になります）
