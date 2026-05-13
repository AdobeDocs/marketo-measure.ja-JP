---
unique-page-id: 18874680
description: '[!DNL Facebook] API - [!DNL Marketo Measure]'
title: '[!DNL Facebook] API'
exl-id: d6d18545-baae-4103-b0a6-c3de681ec833
feature: APIs, Integration, UTM Parameters
TQID: https://experienceleague.adobe.com/yW6j0Ha8-O0-AQo2ledBBpzji3hy7UHxFPa5L-9WNEg
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2: id: c8f57308-7e33-4e41-a385-b55041c78939id: fb43f4c1-87d9-4081-8df1-6fe7e6e5cdc8
subfeature_v2: id: fabdc8ff-b627-44fc-b09d-973166bc2b14
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 498
ht-degree: 4%

---

# [!DNL Facebook] API {#facebook-api}

## はじめに {#introduction}

AdWordsと[!DNL Bing Ads]統合と同様に、[!DNL Facebook]統合では、次の2つの基本的なアクションを実行します。

* [!DNL Marketo Measure] パラメーター（_bf）を使用して、すべての[!DNL Facebook]広告に自動タグ付け
* すべてのアクティブなFacebook広告の広告コスト情報をダウンロード

## [!DNL Facebook]統合の設定方法 {#how-to-configure-the-facebook-integration}

設定に関しては、[!DNL Marketo Measure] アプリ内で完了する7つの手順があります。

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}に移動してログインします。
1. マイアカウントで、**[!UICONTROL 設定]**&#x200B;を選択します。
1. 「統合」で「**[!UICONTROL 接続]**」を選択します。
1. 「**[!UICONTROL 新しい広告接続を設定]**」を選択すると、ポップアップが表示されます。 **[!UICONTROL Facebook]**&#x200B;を選択し、Facebookの資格情報を使用してログインします。

   >[!NOTE]
   >
   >[!DNL Facebook Ads] アカウントに接続するユーザーは、[!DNL Facebook Ads] アカウント内の管理者である必要があります。

1. [!DNL Marketo Measure]がFacebook アカウントに接続されたら、アカウントの横にある鉛筆アイコンをクリックします。
1. このビューで、「自動タグ付け？」トグルを「はい」に移動します。 次に、[!UICONTROL 詳細情報] セクションにあるチェックボックスを選択して、利用条件に同意します。 [!UICONTROL 自動タグ付け] トグルがまだ&#39;[!UICONTROL はい]&#39;に設定されていることを確認してください。

## アカウントの接続 {#connecting-the-account}

![](assets/1.gif)

## 自動タグ付けを有効にする {#enabling-autotagging}

>[!NOTE]
>
>自動タグ付けを有効にすると、タグ付けするすべての広告のコンバージョン履歴とソーシャルプルーフがリセットされます。 自動タグ付けを有効にする前に、[このデータをCSV](https://www.facebook.com/business/help/205067636197240)として書き出すことを強くお勧めします。

![](assets/2-2.png)

統合を有効にすると、[!DNL Marketo Measure]は広告レベルのコストを[!DNL Marketo Measure Marketing ROI] ダッシュボードにダウンロードし始めます。

統合が正しく機能するには、[!DNL Facebook] アカウントで自動タグ付けを有効にする必要があります。 これにより、システムがすべての広告リンクに_bf パラメーターを追加できるようになります。 このプロセスでは、既に[!DNL Facebook]広告に追加されている他のトラッキングパラメーターの上に新しいパラメーターが追加されます。

![](assets/3.gif)

## フィールド マッピング {#field-mapping}

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
   <td><p>[[!DNL Facebook] キャンペーン名]または[utm_campaign]が指定されている場合</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ Id</p></td> 
   <td><p>[[!DNL Facebook] Ad Set Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>広告グループ名</p></td> 
   <td><p>[[!DNL Facebook] Ad Set Name]</p></td> 
  </tr> 
  <tr> 
   <td><p>タッチポイントソース</p></td> 
   <td><p>「[!DNL Facebook]」または[utm_source]が指定されている場合</p></td> 
  </tr> 
  <tr> 
   <td><p>中</p></td> 
   <td><p>"Social"、または[utm_medium]が指定されている場合</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Id、またはCreative_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[utm_contentから生成されたカスタム Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad Content、またはCreative_Name （Data Warehouse）</p></td> 
   <td><p>[utm_content]を指定します</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword_Name （Data Warehouse）またはKeyword_Text</p></td> 
   <td><p>[utm_term]が指定されている場合</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] Ad Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Name （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] Ad Name]</p></td> 
  </tr> 
  <tr> 
   <td><p>Keyword_Unique_Id （Data Warehouse）</p></td> 
   <td><p>[utm_termから生成されたカスタム Id]</p></td> 
  </tr> 
  <tr> 
   <td><p>Ad_Provider （Data Warehouse）</p></td> 
   <td><p>"[!DNL Facebook]"</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Unique_ID （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] Account #]</p></td> 
  </tr> 
  <tr> 
   <td><p>Account_Name （Data Warehouse）</p></td> 
   <td><p>[[!DNL Facebook] アカウント名]</p></td> 
  </tr> 
 </tbody> 
</table>

## よくある質問 {#faq}

**Q: [!DNL Marketo Measure]がサポートしている[!DNL Facebook]広告は何ですか？**

A: カルーセル、単一画像。 現時点では、ビデオ、スライドショー、コレクションは使用できません。

**Q: ソーシャルプルーフとは何ですか？**

回答：ソーシャルプルーフとは、いいね！、クリック、コメント、共有などの目に見えるエンゲージメントのことです。

**Q: [!DNL Marketo Measure]さんが広告にタグを付けるとどうなりますか？**

回答：[!DNL Facebook]では広告を編集できないため、[!DNL Marketo Measure]はクリエイティブを削除する必要があります。クリエイティブには宛先URLが含まれています。その後、新しいパラメーターを使用して広告を再作成してください。

**Q: [!DNL Marketo Measure]が[!DNL Facebook]広告をすべて更新するのはなぜですか？**

A: [!DNL Marketo Measure] プロセスでは、すべての広告が再アクティブ化された場合に備えて、すべての広告にタグを付けます。

**Q：接続されたユーザーに必要な権限は何ですか？**

A: ads_management, email

**Q：支出データの読み込みにどのくらいの時間がかかりますか？**

A: 1時間

**Q：広告データの読み込みにどのくらいの時間がかかりますか？**

A: 4時間
