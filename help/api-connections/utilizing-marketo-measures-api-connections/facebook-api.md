---
unique-page-id: 18874680
description: "[!DNL Facebook] API - [!DNL Marketo Measure]"
title: '"[!DNL Facebook] API»'
exl-id: d6d18545-baae-4103-b0a6-c3de681ec833
feature: APIs, Integration, UTM Parameters
source-git-commit: 741ab20845de2f3bcde589291d7446a5b4f877d8
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 3%

---

# [!DNL Facebook] API {#facebook-api}

## はじめに {#introduction}

AdWords &amp;と類似 [!DNL Bing Ads] 統合、 [!DNL Facebook] 統合には、次の 2 つの基本的なアクションがあります。

* すべて自動タグ付け [!DNL Facebook] 広告の [!DNL Marketo Measure] パラメータ (_bf)
* すべてのアクティブなFacebook広告にわたる広告コスト情報のダウンロード

## 設定方法 [!DNL Facebook] 統合 {#how-to-configure-the-facebook-integration}

設定に関しては、 [!DNL Marketo Measure] アプリを使用します。

1. に移動します。 [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} をクリックし、ログインします。
1. 「マイアカウント」で、「 **[!UICONTROL 設定]**.
1. 「統合」で、「 **[!UICONTROL 接続]**.
1. 選択 **[!UICONTROL 新しい広告接続の設定]** ポップアップが表示されます。 選択 **[!UICONTROL Facebook]** facebookの資格情報を使用してログインします。

   >[!NOTE]
   >
   >接続しているユーザー [!DNL Facebook Ads] アカウントは、 [!DNL Facebook Ads] アカウント。

1. 1 回 [!DNL Marketo Measure] がFacebookアカウントに接続されている場合は、アカウントの横にある鉛筆アイコンをクリックします。
1. このビュー内で、「自動タギング？」を移動します。 「はい」に切り替えます。 次に、 [!UICONTROL 詳細情報] のセクションを参照して、利用条件に同意する必要があります。 次を確認します。 [!UICONTROL 自動タグ付け] 切り替えは、引き続き「 」に設定されます。[!UICONTROL はい]&#39;.

## アカウントの接続 {#connecting-the-account}

![](assets/1.gif)

## 自動タギングの有効化 {#enabling-autotagging}

>[!NOTE]
>
>自動タグ付けを有効にすると、タグ付けしたすべての広告のコンバージョン履歴とソーシャル配達確認がリセットされます。 を強くお勧めします [このデータを CSV として書き出す](https://www.facebook.com/business/help/205067636197240) 自動タグ付けを有効にする前に

![](assets/2-2.png)

統合を有効にしたら、 [!DNL Marketo Measure] が、広告レベルのコストのダウンロードを開始します [!DNL Marketo Measure Marketing ROI] ダッシュボード。

統合が正しく機能するには、 [!DNL Facebook] アカウント。 これにより、システムはすべての広告リンクに_bf パラメータを追加できます。 このプロセスは、既に [!DNL Facebook] 広告。

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
   <td><p>広告キャンペーン ID</p></td> 
   <td><p>[[!DNL Facebook] キャンペーン ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告キャンペーン名 </p></td> 
   <td><p>[[!DNL Facebook] キャンペーン名 ]、または [utm_campaign]（指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ ID</p></td> 
   <td><p>[[!DNL Facebook] 広告セット ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ名</p></td> 
   <td><p>[[!DNL Facebook] 広告セット名 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Touchpoint ソース</p></td> 
   <td><p>"[!DNL Facebook]"、または [utm_source] （指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>中</p></td> 
   <td><p>"Social"、または [utm_medium]（指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>広告 ID、または Creative_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[utm_content から生成されたカスタム ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告コンテンツ、または Creative_Name (Data Warehouse)</p></td> 
   <td><p>[utm_content] を指定した場合は</p></td> 
  </tr> 
  <tr> 
   <td><p>キーワードテキスト、またはキーワード名 (Data Warehouse)</p></td> 
   <td><p>[utm_term] （指定されている場合）</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[[!DNL Facebook] 広告 ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Name (Data Warehouse)</p></td> 
   <td><p>[[!DNL Facebook] 広告名 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword_Unique_Id (Data Warehouse)</p></td> 
   <td><p>[utm_term から生成されたカスタム ID]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Provider (Data Warehouse)</p></td> 
   <td><p>"[!DNL Facebook]"</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Unique_ID (Data Warehouse)</p></td> 
   <td><p>[[!DNL Facebook] アカウント番号 ]</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Name (Data Warehouse)</p></td> 
   <td><p>[[!DNL Facebook] アカウント名 ]</p></td> 
  </tr> 
 </tbody> 
</table>

## よくある質問 {#faq}

**Q：何 [!DNL Facebook] 広告は、 [!DNL Marketo Measure]?**

A：カルーセル、単一の画像です。 現時点では、ビデオ、スライドショーまたはコレクションではありません。

**Q：ソーシャルプルーフとは何ですか。**

回答：Social の配達確認は、「いいね！」、クリック数、コメント数、共有数などのエンゲージメントが表示されます。

**Q：何が起こるか [!DNL Marketo Measure] 広告にタグを付けますか？**

A: [!DNL Facebook] 広告の編集を許可しない [!DNL Marketo Measure] リンク先 URL を含むクリエイティブを削除し、新しいパラメーターを使用して広告を再作成する必要があります。

**Q：なぜですか。 [!DNL Marketo Measure] すべてを更新 [!DNL Facebook] 広告？**

A: [!DNL Marketo Measure] プロセスでは、すべての広告が再アクティブ化された場合に備えてタグ付けされます。

**Q：接続したユーザーに必要な権限は何ですか？**

A:ads_management、email

**Q：支出データのインポートにはどのくらいの時間がかかりますか。**

A: 1 時間

**Q：広告データのインポートにはどのくらい時間がかかりますか？**

A: 4 時間
