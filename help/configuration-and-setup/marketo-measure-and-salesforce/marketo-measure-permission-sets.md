---
unique-page-id: 18874789
description: '[!DNL Marketo Measure]権限セット - [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] 権限セット'
exl-id: 84b7aa24-3934-4584-af05-02e804d00a98
feature: Salesforce
TQID: https://experienceleague.adobe.com/Taoe3f0JfNQ6R-zdMVPJsbdswgNuii-XAyzEsb4MdCk
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 5%

---

# [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets}

Salesforceで[!DNL Marketo Measure]権限セットにアクセスして割り当てる方法について説明します。

## [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets-1}

[!DNL Marketo Measure] Salesforce パッケージには、3つの権限セットが含まれています。 これらの権限セットは、管理者、マーケター、標準ユーザーに[!DNL Marketo Measure]へのアクセスを提供します。

Salesforceで権限セットにアクセスして割り当てるには：

1. 「**[!UICONTROL 設定]**」をクリックします。
1. 左マージンで、「**[!UICONTROL ユーザー]**」、「**[!UICONTROL 権限セット]**」の順にクリックします。
1. 割り当てる[!DNL Marketo Measure]権限セットを選択します。
1. 「**[!UICONTROL 割り当てを管理]**」をクリックし、「**[!UICONTROL 割り当てを追加]**」をクリックします。
1. 権限セットのユーザーを選択し、**[!UICONTROL 割り当て]**&#x200B;をクリックします。

   ![](assets/1-5.png)

## [!DNL Marketo Measure]権限セットの説明 {#marketo-measure-permission-sets-explained}

<table> 
 <tbody> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] 管理者</strong></span></td> 
   <td><span>SFDC管理者に、[!DNL Marketo Measure] オブジェクトからレコードを作成、読み取り、書き込み、削除する機能を提供します。 [!DNL Marketo Measure]がデータをSFDCにプッシュするライセンスでは、この権限セットを有効にする必要があります。 また、このライセンスには、データをレコードに適用する[!DNL Marketo Measure]前にリードが変換されるシナリオで、コンバージョン済みリードを編集する機能があることをお勧めします。 これにより、Salesforceと[!DNL Marketo Measure]間のレポートの正確性が確保されます。 詳細は<a href="https://help.salesforce.com/articleView?id=release-notes.rn_sales_leads_view_converted.htm&amp;type=5&amp;release=206&amp;language=en_us">こちら</a>をご覧ください。</span></td> 
  </tr> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] マーケティングユーザ</strong></span></td> 
   <td><span>マーケティングユーザーに、[!DNL Marketo Measure] オブジェクトからのレコードの読み取りと書き込みを許可します。 マーケティング チームのすべてのメンバーは、[!DNL Marketo Measure] マーケティングユーザー権限セットを有効にする必要があります。 <br></span></td> 
  </tr> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] 標準ユーザー</strong></span></td> 
   <td><span>ユーザーに[!DNL Marketo Measure] オブジェクトからレコードを読み取る機能を提供します。</span></td> 
  </tr> 
 </tbody> 
</table>

インバウンドセールス開発チームとアカウントの上級管理職は、[!DNL Marketo Measure]件のデータから恩恵を受けることができます。 これらの役割がレポートで[!DNL Marketo Measure] データを使用する場合は、[!DNL Marketo Measure]標準ユーザー権限セットを有効にします。

>[!NOTE]
>
>さらに、接続しているユーザーがCampaign オブジェクトにアクセスするには、ユーザーレベルで「マーケティングユーザー」 [!DNL Salesforce] プロファイルを有効にする必要があります。 これを確認するには、**[!UICONTROL 設定]** > **[!UICONTROL ユーザーの管理]** > **[!UICONTROL プロファイル]** > **[!UICONTROL マーケティングユーザー]** > **割り当てユーザー**&#x200B;をクリックします。
