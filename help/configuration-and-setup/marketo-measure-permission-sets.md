---
description: '[!DNL Marketo Measure] 権限セット - [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] 権限セット'
exl-id: 84b7aa24-3934-4584-af05-02e804d00a98
feature: Salesforce
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 6%

---

# [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets}

Salesforceで権限セットにアクセスして割り当て [!DNL Marketo Measure] 方法を説明します。

## [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets-1}

[!DNL Marketo Measure] Salesforce パッケージには、3 つの権限セットが含まれています。 管理者、マーケターおよび標準ユーザーは、これらの権限セットを使用して [!DNL Marketo Measure] にアクセスできます。

Salesforceで権限セットにアクセスして割り当てるには：

1. 「**[!UICONTROL 設定]**」をクリックします。
1. 左の余白で、[**[!UICONTROL ユーザー]**] をクリックし、次に [**[!UICONTROL アクセス許可セット]**] をクリックします。
1. 割り当てる [!DNL Marketo Measure] 権限セットを選択します。
1. **[!UICONTROL 割り当てを管理]** をクリックしてから、**[!UICONTROL 割り当てを追加]** をクリックします。
1. アクセス権セットのユーザを選択し、[**[!UICONTROL 割り当て]**] をクリックします。

   ![1.権限セットのユーザーを選択し、「割り当て」をクリックします。](assets/bizible-full-1.png)

## [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets-explained}

<table>
 <tbody>
  <tr>
   <td><span><strong>[!DNL Marketo Measure] 管理者</strong></span></td>
   <td><span>SFDC管理者が、[!DNL Marketo Measure] オブジェクトからレコードを作成、読み取り、書き込み、削除する機能を付与します。 データをSFDCにプッシュ [!DNL Marketo Measure] るライセンスでは、この権限セットを有効にする必要があります。 また、データをレコードに適用する前にリードが変換されたシナリオでは、このライセンスに変換されたリードを編集する機能があるこ [!DNL Marketo Measure] をお勧めします。 これにより、Salesforceと [!DNL Marketo Measure] の間のレポートの精度が確保されます。 詳細は<a href="https://help.salesforce.com/articleView?id=release-notes.rn_sales_leads_view_converted.htm&type=5&release=206&language=en_us">こちら</a>をご覧ください。</span></td>
  </tr>
  <tr>
   <td><span><strong>[!DNL Marketo Measure] マーケティングユーザ</strong></span></td>
   <td><span>マーケティングユーザーが [!DNL Marketo Measure] オブジェクトからレコードを読み取りおよび書き込めるようにします。 マーケティングチームのすべてのメンバーは、[!DNL Marketo Measure] マーケティングユーザー権限セットを有効にする必要があります。 <br></span></td>
  </tr>
  <tr>
   <td><span><strong>[!DNL Marketo Measure] 標準ユーザー</strong></span></td>
   <td><span>オブジェクトからレコードを読み取る権限 [!DNL Marketo Measure] ユーザーに付与します。</span></td>
  </tr>
 </tbody>
</table>

インバウンドの営業開発チームやアカウント責任者は、[!DNL Marketo Measure] のデータからメリットを得る場合があります。 これらの役割がレポートで [!DNL Marketo Measure] データを使用する場合は、[!DNL Marketo Measure] Standard ユーザー権限セットを有効にします。

>[!NOTE]
>
>さらに、Campaign オブジェクトにアクセスするには、接続に使用するユーザーのユーザーレベルで「マーケティングユーザー」 [!DNL Salesforce] プロファイルが有効になっている必要があります。 これを確認するには、**[!UICONTROL 設定]**/**[!UICONTROL ユーザーを管理]**/**[!UICONTROL プロファイル]**/**[!UICONTROL マーケティングユーザー]**/**割り当てられたユーザー** をクリックします。
