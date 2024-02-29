---
description: "[!DNL Marketo Measure] Adobe Analyticsとの統合 — [!DNL Marketo Measure]"
title: "[!DNL Marketo Measure] との統合 [!DNL Adobe Analytics]"
exl-id: 3a125a15-eb74-454a-afb3-75746a1dfac6
feature: Integration
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 1%

---

# [!DNL Marketo Measure] と Adobe Analytics の統合 {#marketo-measure-integrations-with-adobe-analytics}

B2B 顧客属性の統合により、 [!DNL Marketo Measure] そしてAdobe Analyticsが彼らを豊かにする [!DNL Adobe Analytics] 次から派生した有用なメタデータを持つユーザープロファイル [!DNL Marketo Measure] アトリビューションエンジンと、CRM([!DNL Microsoft Dynamics] および [!DNL Salesforce]) をクリックします。 ご利用のお客様は、 [!DNL Adobe Analytics] および [!DNL Marketo Measure].

>[!PREREQUISITES]
>
>両方のアクティブな配信登録が必要です [!DNL Marketo Measure] および [!DNL Adobe Analytics].

## 統合の設定 {#configuring-the-integration}

1. 顧客コンソールで新しい顧客属性データソースをExperience Cloudします。 詳細な手順 [ここにあります](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=ja).

   後の手順で必要になる次の情報を控えておきます。

   * エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をお勧めします。

   * FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）

1. 顧客属性データソースを作成したら、 **[!UICONTROL 統合]** > **[!UICONTROL 接続]** 画面 [!DNL Marketo Measure] 管理者メニュー。

1. 次をクリック： **[!UICONTROL 新しい顧客属性接続の設定]** ボタンをクリックし、指示に従って顧客属性統合を設定します。 コアサービスコンソールで顧客属性ソースを作成する際に取得したエイリアス ID と FTP 接続情報の入力、およびにと同期する一連のアカウント属性の選択が求められます [!DNL Adobe Analytics] アカウント。

   また、組織 ID を入力する必要があります。Adobe IMSの組織 ID を入力する必要があります。 この ID は、Adobe Experience CloudAdmin Consoleの右下隅に表示されます。 この ID の検索方法について詳しくは、Adobeアカウントチーム（アカウントマネージャー）にお問い合わせください。

1. 接続の作成が完了したら、 [!DNL Marketo Measure] アカウントを使用するには、Experience Cloudコンソールに戻り、 [スキーマの検証](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/validate-schema.html?lang=en). FTP ファイルのアップロードについて心配する必要はありません。 [!DNL Marketo Measure] では、そのパーツを自動化しています。 必要な操作は、手順 1 で作成した顧客属性ソースの「表示/編集」スキーマ画面に移動し、各属性のデータタイプをAdobeに示すだけです [!DNL Marketo Measure] があなたに代わってアップロードされました。 必要に応じて、アップロードした属性の表示にわかりやすい名前を新しく作成することもできます。

   CRM アカウントオブジェクトの属性の同期を選択した場合は、新しい表示名を選択することを強くお勧めします。 [!DNL Marketo Measure] は、これらの属性の API レベルの名前のみを入力します。これらの名前は、通常、レポートでわかりやすい名前ではありません。

1. 最後の手順では、属性を使用するExperience Cloudアプリケーションの属性の購読を設定します。 次のサブスクリプションを設定できます： [!DNL Adobe Analytics] または [!DNL Adobe Target].  その方法の詳細 [ここにあります](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html).

## 属性の説明 {#attribute-descriptions}

新しい B2B 顧客属性接続を作成する場合、 [!DNL Marketo Measure] は、B2B 顧客属性の標準セットを自動的に作成します。 これらの属性については、次の表で説明します。

以下に示すものの他に、CRM のアカウントオブジェクトに添付する属性もアップロードできます。 複数のアカウントが特定のユーザーに結び付けられている場合、 [!DNL Marketo Measure] 一致するすべてのアカウント属性値をセミコロンで区切ったリストで入力します。

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
   <td>特定の Web 訪問者に関連付けられたアカウント名。 複数のアカウントが特定のユーザーに結び付けられている場合、 [!DNL Marketo Measure] は、一致するすべてのアカウント名をセミコロンで区切ったリストで入力します。<br/>
   <strong>注意：</strong> account.name は、アカウントオブジェクトの name 属性の Salesforce-API レベルの名前です。 統合設定のスキーマ検証手順（手順 4）で、この属性に対して適切な表示名（例：「会社」）を選択できます。</td>
  </tr>
  <tr> 
   <td>属性収益 — 急モデル &gt;</td> 
   <td>CRM でのクローズドウォンの商談との関連によってこの顧客に起因する売上高 ( [!DNL Marketo Measure] アトリビューションエンジン。<br/>
   各アトリビューションモデルに対して、次の属性の 1 つが [!DNL Marketo Measure] 購読ではを使用できます（例：「属性売上高 — フルパス」）。</td>
  </tr>
  <tr> 
   <td>最も深いファネルステージ</td> 
   <td>特定のユーザーに関連付けられたオープンオポチュニティの最も深いファネルステージ。</td>
  </tr>
  <tr> 
   <td>保留中の商談</td> 
   <td>CRM データに従って特定のユーザーが結び付けられるオポチュニティ ID のセミコロンで区切られたリスト。</td>
  </tr> 
 </tbody> 
</table>

**属性制限に関する注意**

この統合で表示される属性は、引き続き [!DNL Adobe Analytics] および [!DNL Adobe Target]. 属性購読で表示される属性のみ ( [統合の設定](#configuring-the-integration)) は、購読されているアプリケーションの制限としてカウントされます。

## よくある質問 {#faqs}

**この統合を使用して共有したい属性のセットを変更する方法を教えてください。**

が共有する属性の場合 [!DNL Marketo Measure] をAdobe IMS組織に追加します（この統合経由）。 [!DNL Adobe Analytics]の場合、コアサービスコンソールで設定した属性購読で表示される必要があります。 したがって、属性がに表示されないように属性を削除する場合は、 [!DNL Adobe Analytics]を使用する場合、属性購読を削除するだけでこれを実現できます。

B2B 顧客属性接続は、 [!DNL Marketo Measure] 接続設定から除外したい属性を使用して、再作成します。 同様に、統合に属性を追加するには、既存の接続を削除し、目的の属性を設定に追加して新しい接続を作成する必要があります。

上記の点を考慮して、属性接続を初めて設定する場合は、属性を選択する際にはできる限り包括的に設定することを強くお勧めします。

**この統合の使用例を教えてください。**

1. アカウントベースのトラフィック指標：アカウント名属性を使用して、Adobe Analyticsで 1 つ以上のターゲットアカウントのセグメントを作成し、ターゲットアカウントから発生するトラフィックのサブセットに関するサイトトラフィック指標を分析できます。
1. コンテンツ分析：売上高指標を使用して、製品やサービスを最終的に購入した顧客や、特定のファネルステージに到達した顧客に最も関与しているサイトコンテンツを分析します。
1. ライブディールのサポート： CRM の特定のオープンオポチュニティに関連付けられたユーザーのサイト行動を分析することで、セールスチームに実用的なインサイトを提供します。
