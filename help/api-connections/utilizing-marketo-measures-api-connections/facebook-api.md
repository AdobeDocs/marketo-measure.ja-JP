---
unique-page-id: 18874680
description: "[!DNL Facebook] API - [!DNL Marketo Measure]"
title: "[!DNL Facebook] API"
exl-id: d6d18545-baae-4103-b0a6-c3de681ec833
feature: APIs, Integration, UTM Parameters
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 3%

---

# [!DNL Facebook] API {#facebook-api}

## はじめに {#introduction}

AdWords と [!DNL Bing Ads] の統合と同様に、[!DNL Facebook] の統合では次の 2 つの基本的なアクションを実行します。

* [!DNL Marketo Measure] のパラメーター（_bf）を使用してすべての [!DNL Facebook] 広告を自動タグ付け
* アクティブなすべてのFacebook広告の広告コスト情報のダウンロード

## [!DNL Facebook] 統合の設定方法 {#how-to-configure-the-facebook-integration}

セットアップについては、[!DNL Marketo Measure] アプリ内で 7 つの手順を完了する必要があります。

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} に移動し、ログインします。
1. マイアカウントで **[!UICONTROL 設定]** を選択します。
1. 「統合」で **[!UICONTROL 「接続]**」を選択します。
1. **[!UICONTROL 新しい広告接続の設定]** を選択すると、ポップアップが表示されます。 **0&rbrace;Facebook&rbrace; を選択し、Facebookの資格情報を使用してログインします。**

   >[!NOTE]
   >
   >[!DNL Facebook Ads] アカウントに接続するユーザーは、[!DNL Facebook Ads] アカウント内の管理者である必要があります。

1. facebook アカウント [!DNL Marketo Measure] 接続したら、アカウントの横にある鉛筆アイコンをクリックします。
1. このビュー内で、「自動タグ付け？」 「はい」に切り替えます。 次に、「[!UICONTROL &#x200B; 詳細情報 &#x200B;]」セクションにあるチェックボックスをオンにして、利用条件に同意します。 [!UICONTROL &#x200B; 自動タグ付け &#x200B;] の切り替えが「[!UICONTROL &#x200B; はい &#x200B;]」に設定されていることを確認します。

## アカウントの接続 {#connecting-the-account}

![](assets/1.gif)

## 自動タギングの有効化 {#enabling-autotagging}

>[!NOTE]
>
>自動タギングを有効にすると、タグ付けしたすべての広告のコンバージョン履歴とソーシャル校正がリセットされます。 自動タギングを有効にする前に、[&#x200B; このデータを CSV として書き出す &#x200B;](https://www.facebook.com/business/help/205067636197240) ことを強くお勧めします。

![](assets/2-2.png)

統合を有効にすると、広告レベルのコスト [!DNL Marketo Measure]&#x200B;[!DNL Marketo Measure Marketing ROI] ダッシュボードにダウンロードされるようになります。

統合が正しく機能するには、[!DNL Facebook] アカウントで自動タグ付けを有効にする必要があります。 これにより、システムはすべての広告リンクに_bf パラメーターを追加できます。 このプロセスは、既に [!DNL Facebook] 広告に追加した他のトラッキングパラメーターの上に新しいパラメーターを追加します。

![](assets/3.gif)

## フィールドマッピング {#field-mapping}

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th><p><strong>タッチポイントフィールド</strong></p></th> 
   <th><p><strong>値</strong></p></th> 
  </tr> 
  <tr> 
   <td><p>広告キャンペーン Id</p></td> 
   <td><p>[[!DNL Facebook] キャンペーン Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告キャンペーン名 </p></td> 
   <td><p>[[!DNL Facebook] キャンペーン名 ]、または指定されている場合は [utm_campaign]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ Id</p></td> 
   <td><p>[[!DNL Facebook] 広告セット Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ名</p></td> 
   <td><p>[[!DNL Facebook] 広告セット名 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Touchpoint ソース</p></td> 
   <td><p>「[!DNL Facebook]」、指定されている場合は [utm_source]</p></td> 
  </tr> 
  <tr> 
   <td><p>中</p></td> 
   <td><p>「ソーシャル」、または指定されている場合は [utm_medium]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告 Id または Creative_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[utm_content から生成されたカスタム ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告コンテンツまたはクリエイティブ名（Data Warehouse）</p></td> 
   <td><p>[utm_content] （指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword Text または Keyword_Name （Data Warehouse）</p></td> 
   <td><p>[utm_term] （指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] 広告 Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Name （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] 広告名 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[utm_term から生成されたカスタム ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Provider （Data Warehouse）</p></td> 
   <td><p>"[!DNL Facebook]"</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Unique_ID （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] アカウント番号 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Name （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] アカウント名 ]</p></td> 
  </tr> 
 </tbody> 
</table>

## よくある質問 {#faq}

**Q:[!DNL Marketo Measure] でサポートされている [!DNL Facebook] 広告は何ですか？**

A：カルーセル、単一の画像。 現時点では、ビデオ、スライドショー、コレクションではありません。

**Q：ソーシャルプルーフとは何ですか？**

A：ソーシャルプルーフは、いいね、クリック、コメント、共有など、目に見えるエンゲージメントです。

**Q：広告にタグ [!DNL Marketo Measure] 付けるとどうなりますか？**

回答：[!DNL Facebook] では広告を編集できません。宛先 URL を含 [!DNL Marketo Measure] クリエイティブを削除してから、新しいパラメーターで広告を再作成する必要があります。

**Q：すべての [!DNL Facebook] 広告 [!DNL Marketo Measure] 更新する理由を教えてください。**

A:[!DNL Marketo Measure] のプロセスは、再アクティブ化された場合に備えてすべての広告にタグを付けることです。

**Q：接続されたユーザーに必要な権限を教えてください。**

A: ads_management, email

**Q：費用データのインポートにはどの程度の時間がかかりますか？**

A: 1 時間

**Q：広告データのインポートにはどの程度の時間がかかりますか？**

A: 4 時間
