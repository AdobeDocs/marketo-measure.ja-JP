---
description: Adobe Analyticsとの[!DNL Marketo Measure]統合 –  [!DNL Marketo Measure]
title: ' [!DNL Adobe Analytics]との統合[!DNL Marketo Measure]'
exl-id: 3a125a15-eb74-454a-afb3-75746a1dfac6
feature: Integration
TQID: https://experienceleague.adobe.com/6IzJMn8-MWNL1vIX5-O1f7CgCmBtSAituyE2rfYLKPQ
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2:
  - id: c8f57308-7e33-4e41-a385-b55041c78939
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 968
ht-degree: 2%

---

# [!DNL Marketo Measure] と Adobe Analytics の統合 {#marketo-measure-integrations-with-adobe-analytics}

B2B顧客属性の統合により、[!DNL Marketo Measure]およびAdobe Analyticsの相互ユーザーは、[!DNL Marketo Measure]属性エンジンから派生した貴重なメタデータと、CRM （[!DNL Microsoft Dynamics]および[!DNL Salesforce]）との同期機能を通じて、[!DNL Adobe Analytics]のユーザープロファイルを強化できます。 [!DNL Adobe Analytics]と[!DNL Marketo Measure]を使用しているすべてのお客様が無料で利用できます。

>[!PREREQUISITES]
>
>[!DNL Marketo Measure]と[!DNL Adobe Analytics]の両方にアクティブなサブスクリプションが必要です。

## 統合の設定 {#configuring-the-integration}

1. Experience Cloud コンソールで新しい顧客属性データ Sourceを作成します。 詳細な手順[については、こちらを参照してください](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=ja)。

   後の手順で必要となる次の情報に注意してください。

   * エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をおすすめします

   * FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）

1. 顧客属性データ Sourceを作成したら、管理メニュー[!DNL Marketo Measure]の&#x200B;**[!UICONTROL 統合]** > **[!UICONTROL 接続]**&#x200B;画面に移動して、設定プロセスを続行します。

1. 「**[!UICONTROL 新しい顧客属性接続の設定]**」ボタンをクリックし、手順に従って顧客属性の統合を設定します。 UIでは、コアサービスコンソールでCustomer Attributes Sourceを作成する際に取得したエイリアス IDおよびFTP接続情報の入力を求めるメッセージが表示されます。 [!DNL Adobe Analytics] アカウントに同期するアカウント属性のセットを選択します。

   Adobe IMS組織IDを入力します。 このIDは、Adobe Experience Cloud Admin Consoleの右下隅に表示されます。 このIDを見つける方法について詳しくは、Adobe アカウントチーム（アカウントマネージャー）にお問い合わせください。

1. [!DNL Marketo Measure] アカウントでの接続の作成が完了したら、Experience Cloud コンソールに戻って[&#x200B; スキーマを検証](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/validate-schema.html?lang=ja)する必要があります。 FTP ファイルのアップロードについて心配する必要はありません。[!DNL Marketo Measure]は、その部分を自動化しました。 手順1で作成した顧客属性Sourceの「表示/編集」スキーマ画面に移動し、[!DNL Marketo Measure]が自分に代わってアップロードした各属性のデータタイプをAdobeに伝えます。 必要に応じて、アップロードされた属性に対して新しい表示用の名前を作成することもできます。

   CRM アカウントオブジェクトから属性を同期するように選択した場合は、新しい表示名を選択することを強くお勧めします。[!DNL Marketo Measure]はこれらの属性のAPI レベル名のみを入力するため、通常、レポートに適していません。

1. 最後の手順は、で属性を使用するExperience Cloud アプリケーションの属性サブスクリプションを設定することです。 [!DNL Adobe Analytics]または[!DNL Adobe Target]のサブスクリプションを設定できます。  その方法について詳しくは、[こちらを参照してください](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/subscription.html?lang=ja)。

## 属性の説明 {#attribute-descriptions}

B2B顧客属性接続を作成すると、[!DNL Marketo Measure]は標準のB2B顧客属性セットを自動的に作成します。 これらの属性については、次の表で説明します。

以下に示す属性に加えて、アカウントオブジェクトに添付されている属性をCRMにアップロードすることもできます。 指定されたユーザーに複数のアカウントが関連付けられている場合、[!DNL Marketo Measure]は、セミコロン区切りのリストにすべての一致するアカウント属性値を入力します。

<table> 
 <colgroup> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <td><b>属性名</b></td> 
   <td><b>説明</b></td>
  </tr> 
  <tr> 
   <td>Account.Name</td> 
   <td>特定のweb訪問者に関連付けられたアカウント名。 指定されたユーザーに複数のアカウントが関連付けられている場合、[!DNL Marketo Measure]は、セミコロン区切りのリストにすべての一致するアカウント名を入力します。<br/>
   <strong>注：</strong> account.nameは、アカウントオブジェクトのname属性のSalesforce API レベルの名前です。 統合設定（ステップ 4）のスキーマ検証ステップで、この属性のより良い表示名（例：「会社」）を選択できます。</td>
  </tr>
  <tr> 
   <td>帰属収益 – ‹MODEL›</td> 
   <td>[!DNL Marketo Measure] アトリビューションエンジンで計算された、CRMで商談成立した商談との関連付けにより、この顧客に起因する収益。<br/>
   [!DNL Marketo Measure] サブスクリプションで使用できる各アトリビューションモデルに対して、これらの属性の1つが存在します（例：「Attributed Revenue - Full Path」）。</td>
  </tr>
  <tr> 
   <td>Deepest Funnel Stage</td> 
   <td>特定のユーザーに関連するオープンオポチュニティの最も深いfunnelステージ。</td>
  </tr>
  <tr> 
   <td>保留中の商談</td> 
   <td>CRM データに従って特定のユーザーが関連付けられている商談IDのセミコロン区切りのリスト。</td>
  </tr> 
 </tbody> 
</table>

**属性制限に関するメモ**

この統合によって表示された属性は、[!DNL Adobe Analytics]および[!DNL Adobe Target]の契約上の属性制限に対してカウントされます。 属性サブスクリプションを介して表示される属性のみ（手順5、[統合の設定](#configuring-the-integration)）は、購読アプリケーションの制限に対してカウントされます。

## よくある質問（FAQ） {#faqs}

**この統合を介して共有する属性のセットを変更するにはどうすればよいですか？**

この統合を介して[!DNL Marketo Measure]がAdobe IMS組織に共有する属性を[!DNL Adobe Analytics]で表示して使用するには、コアサービスコンソールで設定された属性サブスクリプションを使用して表示する必要があります。 したがって、[!DNL Adobe Analytics]に表示されないように属性を削除する場合は、属性のサブスクリプションを削除するだけで、これを実現できます。

[!DNL Marketo Measure]でB2B顧客属性接続を削除し、共有する必要のない属性を使用して接続の設定から削除して再作成することもできます。 同様に、統合に属性を追加するには、既存の接続を削除し、目的の属性を設定に追加した新しい接続を作成する必要があります。

上記を考慮すると、属性の接続を初めて設定する場合は、属性を選択する際にできるだけ包括的にすることをお勧めします。

**この統合の使用例を教えてください。**

1. Account-Based Traffic Metrics: Account Name属性を使用すると、Adobe Analyticsで1つ以上のターゲットアカウントのセグメントを作成し、ターゲットアカウントから発信されたトラフィックのサブセットに対してのみサイトトラフィック指標を分析できます。
1. Content Analytics：売上指標を使用して、自社の商品やサービスを購入した顧客や、funnelの特定の段階に到達した顧客に対して、最もエンゲージメントの高いサイトコンテンツを特定します。
1. ライブディールのサポート：CRM内の特定のオープンオポチュニティに関連するユーザーのサイト行動を分析することで、営業部門に実用的なinsightを提供します。
