---
unique-page-id: 18874789
description: '"[!DNL Marketo Measure] 権限セット — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: "[!DNL Marketo Measure] 権限セット"
exl-id: 84b7aa24-3934-4584-af05-02e804d00a98
feature: Salesforce
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 5%

---

# [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets}

アクセスして割り当てる方法を説明します [!DNL Marketo Measure] Salesforce の権限セット。

## [!DNL Marketo Measure] 権限セット {#marketo-measure-permission-sets-1}

には、3 つの権限セットが含まれています。 [!DNL Marketo Measure] Salesforce パッケージ。 これらの権限セットは、 [!DNL Marketo Measure] 管理者、マーケターおよび標準ユーザー向け。

Salesforce で権限セットにアクセスして割り当てるには、次の手順に従います。

1. 「**[!UICONTROL 設定]**」をクリックします。
1. 左余白で、 **[!UICONTROL ユーザー]**&#x200B;を、 **[!UICONTROL 権限セット]**.
1. を選択します。 [!DNL Marketo Measure] 割り当てる権限セットです。
1. クリック **[!UICONTROL 割り当てを管理]**&#x200B;を、 **[!UICONTROL 割り当てを追加]**.
1. 権限セットのユーザーを選択し、 **[!UICONTROL 割り当て]**.

   ![](assets/1-5.png)

## [!DNL Marketo Measure] 権限セットの説明 {#marketo-measure-permission-sets-explained}

<table> 
 <tbody> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] 管理者</strong></span></td> 
   <td><span>SFDC 管理者がレコードの作成、読み取り、書き込み、削除を行えるようにします。 [!DNL Marketo Measure] オブジェクト。 次の条件に基づくライセンス： [!DNL Marketo Measure] SFDC へのデータのプッシュでは、この権限セットが有効になっている必要があります。 さらに、このライセンスでは、以前にリードが変換された場合に、変換済みのリードを編集する機能を持つことをお勧めします。 [!DNL Marketo Measure] レコードにデータを適用する。 これにより、Salesforce との間のレポートの正確性が確保されます。 [!DNL Marketo Measure]. 詳細は<a href="http://releasenotes.docs.salesforce.com/en-us/spring17/release-notes/rn_sales_leads_view_converted.htm">こちら</a>をご覧ください。</span></td> 
  </tr> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] マーケティングユーザ</strong></span></td> 
   <td><span>マーケティングユーザーがレコードの読み取りと書き込みを行えるようにします。 [!DNL Marketo Measure] オブジェクト。 マーケティングチームのすべてのメンバーが、 [!DNL Marketo Measure] マーケティングユーザーの権限セットが有効になっています。 <br></span></td> 
  </tr> 
  <tr> 
   <td><span><strong>[!DNL Marketo Measure] 標準ユーザ</strong></span></td> 
   <td><span>ユーザーが次のレコードを読み取れるようにします。 [!DNL Marketo Measure] オブジェクト。</span></td> 
  </tr> 
 </tbody> 
</table>

インバウンドのセールス開発チームとアカウント担当者は、次のメリットを得ることができます。 [!DNL Marketo Measure] データ。 これらの役割でを使用する場合 [!DNL Marketo Measure] レポート内のデータ、有効化 [!DNL Marketo Measure] 標準ユーザー権限セット。

>[!NOTE]
>
>また、接続したユーザーには、「マーケティングユーザー」が必要です [!DNL Salesforce] ユーザーレベルで有効になっているプロファイルを使用して、Campaign オブジェクトにアクセスできるようになります。 これを確認するには、次の場所をクリックします。 **[!UICONTROL 設定]** > **[!UICONTROL ユーザーを管理]** > **[!UICONTROL プロファイル]** > **[!UICONTROL マーケティングユーザー]** > **割り当てられたユーザー**.
