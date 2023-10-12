---
unique-page-id: 18874672
description: ' [!DNL Marketo Measure]  と  [!DNL Salesforce]  の相互作用 - Marketo Measure - 製品ドキュメント'
title: ' [!DNL Marketo Measure]  と  [!DNL Salesforce]  の相互作用'
exl-id: c2f9d7ce-c5b8-4664-8f92-cb54255190cd
feature: Salesforce
source-git-commit: afb7805e375f26cc1b2473802582b1999e92cd8b
workflow-type: ht
source-wordcount: '1719'
ht-degree: 100%

---

# [!DNL Marketo Measure] と [!DNL Salesforce] の相互作用 {#how-marketo-measure-and-salesforce-interact}

>[!NOTE]
>
>アドビのドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には「Bizible」と表示されます。アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

[!DNL Marketo Measure] と Salesforce の関係を大まかに見てみましょう。

## Salesforce と [!DNL Marketo Measure] {#salesforce-and-marketo-measure}

[!DNL Marketo Measure] アカウントが作成され、[!DNL Salesforce] が接続されると、[!DNL Marketo Measure] 管理パッケージがインストールされ、[!DNL Marketo Measure] Salesforce ユーザが編集権限を持っている限り、[!DNL Marketo Measure] はマーケティングデータを CRM インスタンスにプッシュし始めます。

[!DNL Marketo Measure] Salesforce パッケージをインストールしていない場合、[!DNL Marketo Measure] は Salesforce インスタンスにデータを書き込みません。

![](assets/1-3.png)

デフォルトでは、ジョブが CRM にデータを送信するたびに、[!DNL Marketo Measure] は API クレジットごとに 200 件のレコードを書き出します。これにより、ほとんどの顧客に、[!DNL Marketo Measure] が消費する API クレジットと CRM の CPU リソース要件との間の最適なバランスが提供されます。ただし、ワークフローやトリガーなど複雑な CRM 設定を持つ顧客の場合は、バッチサイズを小さくすると CRM のパフォーマンスの向上に役立つ場合があります。この目的のために、[!DNL Marketo Measure] では顧客が CRM 書き出しのバッチサイズを設定できます。これは、[!DNL Marketo Measure] web アプリケーションの[!UICONTROL 設定]／[!UICONTROL CRM]／[!UICONTROL 一般]ページで設定でき、顧客は 200（デフォルト）、100、50、25 のバッチサイズから選択できます。

![](assets/how-bizible-and-salesforce-interact-2.png)

この設定を変更する場合、バッチサイズが小さいほど CRM からの API クレジットをより多く消費することに注意してください。CRM で CPU タイムアウトまたは高い CPU 負荷が発生している場合のみ、バッチサイズを小さくすることをお勧めします。

## Salesforce 標準オブジェクトとアクセス {#salesforce-standard-objects-and-access}

これには、[!DNL Marketo Measure] がやり取りする [!DNL Salesforce] 標準オブジェクトと、接続が確立され [!DNL Marketo Measure] パッケージがインストールされた後にこれらのオブジェクトに追加するカスタムフィールドが一覧表示されます。そのままでは、[!DNL Marketo Measure] は標準の [!DNL Salesforce] オブジェクトフィールドに書き込みません。

**リード**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>メール</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ステータス</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CreatedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedContactId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedOpportunityId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsConverted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>Web サイト</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>会社</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Account__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

**取引先責任者**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>アカウント</p></td> 
   <td><p>標準</p></td> 
   <td><span>x</span></td> 
   <td><br></td> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>メール</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>作成日</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

**事例**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CreatedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>SuppliedEmail</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_FT__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source_LC__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

**アカウント**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>Web サイト</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Engagement_Score__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

**商談**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>アカウント</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td><br></td> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CreatedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsWon</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsClosed</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CloseDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>StageName</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>金額</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Bizible_Opportunity_Amount__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

**キャンペーン**

<table> 
 <colgroup> 
  <col> 
  <col> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>メール</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ステータス</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CreatedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedContactId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>ConvertedOpportunityId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsConverted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>Web サイト</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>会社</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>タイプ</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td><br></td> 
  </tr> 
 </tbody> 
</table>

**キャンペーンメンバー**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>ID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CreatedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>LastModifiedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsDeleted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>FirstRespondedDate</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>HasRelponed</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CONTACTID</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>leadId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>IsConverted</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>CampaignId</p></td> 
   <td><p>標準</p></td> 
   <td><p>x</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Bizible_Touchpoint_Date__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Status_Date__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Status_Contact__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Status_Leade__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Status_Opportunity__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Salesforce アカウント内での削除イベントを Marketo Measure が確実にキャプチャするには、以下のオブジェクトに対する複製可能な権限が必要です。複製可能な権限は、次のオブジェクトに標準で付属しています。
>
>* アカウント
>* キャンペーン
>* キャンペーンメンバー
>* 取引先責任者
>* イベント
>* リード
>* 商談
>* タスク


## [!DNL Salesforce] の [!DNL Marketo Measure] カスタムオブジェクト {#marketo-measure-custom-objects-in-salesforce}

SFDC の標準オブジェクトでのカスタムフィールドの作成とは別に、[!DNL Marketo Measure] パッケージがインストールされ、カスタムオブジェクトがいくつか作成されます。以下に、これらのカスタムオブジェクトのリストと、[!DNL Marketo Measure] が書き込むフィールドを示す表を示します。

**Buyer Touchpoint**

Buyer Touchpoint は、取引先責任者、リード、事例のマーケティングインタラクションをカプセル化する [!DNL Marketo Measure] カスタムオブジェクトです。

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>bizible2__Bizible_Person__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__SF_Campaign__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__UniqueId__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_Path__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Type__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Content__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Group_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Group_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Placement_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Placement_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Site_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Site_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Form_URL__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Form_URL_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Platform__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Browser__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_City__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_Country__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_Region__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_MatchType__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Position__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_Text__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Medium__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Referrer_Page__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Referrer_Page_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Search_Phrase__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Segment__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_First_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_Lead_Creation_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_U_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Destination_URL__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Case__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Contact__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
 </tbody> 
</table>

**[!DNL Marketo Measure]担当者**

[!DNL Marketo Measure] 担当者は、リードオブジェクト、取引先責任者オブジェクトおよび事例オブジェクトに関連する [!DNL Marketo Measure] カスタムオブジェクトです。

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>bizible2__UniqueId__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Lead__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Case__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Contact__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x </p></td> 
  </tr> 
 </tbody> 
</table>

## Buyer Attribution Touchpoint {#buyer-attribution-touchpoint}

Buyer Attribution Touchpoint は、商談に対するマーケティングの影響をカプセル化する [!DNL Marketo Measure] カスタムオブジェクトです。

**Buyer Attribution Touchpoint**

<table> 
 <tbody> 
  <tr> 
   <th><p>フィールド</p></th> 
   <th><p>標準／カスタム</p></th> 
   <th><p>読み取り</p></th> 
   <th><p>書き込み</p></th> 
  </tr> 
  <tr> 
   <td><p>bizible2__Account__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__SF_Campaign__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Contact__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Opportunity__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__UniqueId__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Marketing_Channel_Path__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Type__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Content__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Group_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Group_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Campaign_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Placement_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Placement_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Site_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Site_Name__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Form_URL__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Form_URL_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Platform__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Browser__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_City__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_Country__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Geo_Region__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_Id__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_MatchType__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Position__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Keyword_Text__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Landing_Page_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Medium__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Referrer_Page__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Referrer_Page_Raw__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Search_Phrase__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Date__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Touchpoint_Source__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Segment__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_First_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_Lead_Conversion_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_U_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_W_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_Custom_Model__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Attribution_Custom_Model_2__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_First_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_Lead_Creation_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_U_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_W_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_Custom_Model__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Count_Custom_Model_2__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Ad_Destination_URL__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_First_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_Lead_Creation_Touch__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_U_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_W_Shaped__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_Custom_Model__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
  <tr> 
   <td><p>bizible2__Revenue_Custom_Model_2__c</p></td> 
   <td><p>カスタム</p></td> 
   <td><p>x</p></td> 
   <td><p>x</p></td> 
  </tr> 
 </tbody> 
</table>
