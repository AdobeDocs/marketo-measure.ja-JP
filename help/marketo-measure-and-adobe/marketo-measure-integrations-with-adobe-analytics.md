---
description: "Adobe Analyticsとの [!DNL Marketo Measure] 統合 –  [!DNL Marketo Measure]"
title: "との [!DNL Marketo Measure] 統合  [!DNL Adobe Analytics]"
exl-id: 3a125a15-eb74-454a-afb3-75746a1dfac6
feature: Integration
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 1%

---

# [!DNL Marketo Measure] と Adobe Analytics の統合 {#marketo-measure-integrations-with-adobe-analytics}

B2B 顧客属性の統合により、[!DNL Marketo Measure] とAdobe Analyticsの相互ユーザーは、[!DNL Marketo Measure] アトリビューションエンジンおよび CRM との同期機能から得られる貴重なメタデータで [!DNL Adobe Analytics] スタムユーザープロファイルをエンリッチメントできます（[!DNL Microsoft Dynamics] と [!DNL Salesforce]）。 [!DNL Adobe Analytics] と [!DNL Marketo Measure] を使用するすべての顧客が無料で利用できます。

>[!PREREQUISITES]
>
>[!DNL Marketo Measure] と [!DNL Adobe Analytics] の両方に対してアクティブな購読が必要です。

## 統合の設定 {#configuring-the-integration}

1. Experience Cloudコンソールで新しい顧客属性データSourceを作成します。 手順について詳しくは [&#x200B; こちらを参照 &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=ja) してください。

   後の手順で必要になる、次の情報をメモします。

   * エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をお勧めします

   * FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）

1. 顧客属性データ Sourceが作成されたら、[!DNL Marketo Measure] admin メニューの **[!UICONTROL Integrations]**/**[!UICONTROL Connections]** 画面に移動して、設定プロセスを続けます。

1. **[!UICONTROL 新しい顧客属性接続の設定]** ボタンをクリックし、指示に従って顧客属性統合を設定します。 UI では、コアサービスコンソールで顧客属性Sourceを作成する際に取得したエイリアス ID および FTP 接続情報を入力するように求められます。 [!DNL Adobe Analytics] アカウントと同期するアカウント属性のセットを選択します。

   Adobe IMS組織 ID を入力します。 この ID は、Adobe Experience Cloud Admin Consoleの右下隅に表示されます。 この ID の見つけ方の詳細については、Adobeアカウントチーム（担当営業のアカウントマネージャー）にお問い合わせください。

1. [!DNL Marketo Measure] アカウントでのExperience Cloudの作成が完了したら、接続コンソールに戻って [&#x200B; スキーマを検証 &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/validate-schema.html?lang=ja) する必要があります。 FTP ファイルのアップロードについて心配する必要はありません [!DNL Marketo Measure]、この部分は自動的に追加されました。 手順 1 で作成した顧客属性Sourceの「表示/編集」スキーマ画面に移動し、ユーザーが代わりにアップロードした各属性に対するデータタイプをAdobeに指定し [!DNL Marketo Measure] す。 必要に応じて、アップロードした属性に新しい表示にわかりやすい名前を作成することもできます。

   CRM アカウントオブジェクトから属性を同期することを選択した場合は、新しい表示名を選択することを強くお勧めします。[!DNL Marketo Measure] れらの属性は通常、レポートに適さない API レベルの名前のみが入力されるからです。

1. 最後の手順では、属性を使用するExperience Cloudアプリケーションの属性サブスクリプションを設定します。 [!DNL Adobe Analytics] または [!DNL Adobe Target] の購読を設定できます。  その方法について詳しくは [&#x200B; こちらを参照 &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/subscription.html?lang=ja) してください。

## 属性の説明 {#attribute-descriptions}

B2B 顧客属性接続を作成すると、B2B 顧客属性の標準セット [!DNL Marketo Measure] 自動的に作成されます。 これらの属性について、次の表で説明します。

以下に示すリストに加えて、CRM のアカウントオブジェクトに添付されている属性をアップロードすることもできます。 指定のユーザーに複数のアカウントが関連付けられている場合、[!DNL Marketo Measure] は、一致するすべてのアカウント属性値をセミコロンで区切られたリストに入力します。

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
   <td>特定の web 訪問者に関連付けられたアカウント名。 指定のユーザーに複数のアカウントが関連付けられている場合、[!DNL Marketo Measure] は、一致するすべてのアカウント名をセミコロンで区切ったリストに入力します。<br/>
   <strong> メモ：</strong> account.name は、アカウントオブジェクトの name 属性の Salesforce-API レベルの名前です。 統合設定のスキーマ検証手順（手順 4）で、この属性に適した表示名（「会社」など）を選択できます。</td>
  </tr>
  <tr> 
   <td>起因する収益 – ‹モデル›</td> 
   <td>売上高は、[!DNL Marketo Measure] アトリビューションエンジンによって計算されたように、CRM での受注案件と関連付けられているため、この顧客に関連付けられます。<br/>
   これらの属性の 1 つは、ア [!DNL Marketo Measure] ットの購読で許可されるアトリビューションモデルごとに存在します（例：「アトリビューション済み収益 – フルパス」）。</td>
  </tr>
  <tr> 
   <td>最深ファネルステージ</td> 
   <td>特定のユーザーに関連付けられたオープンなオポチュニティの最も深いファネルステージ。</td>
  </tr>
  <tr> 
   <td>保留中の商談</td> 
   <td>CRM データに従って特定のユーザーが関連付けられているオポチュニティ ID のセミコロン区切りリスト。</td>
  </tr> 
 </tbody> 
</table>

**属性の制限に関するメモ**

この統合を通じて表示される属性は、[!DNL Adobe Analytics] および [!DNL Adobe Target] の契約上の属性制限に対してカウントされます。 属性の購読（[&#x200B; 統合の設定 &#x200B;](#configuring-the-integration) の手順 5）を介して表示された属性のみが、購読しているアプリケーションの制限にカウントされます。

## よくある質問 {#faqs}

**この統合を通じて共有する属性のセットを変更するにはどうすればよいですか？**

この統合を通じて [!DNL Marketo Measure] によってAdobe IMS組織に共有される属性を、[!DNL Adobe Analytics] で表示および使用するには、コアサービスコンソールで設定された属性購読を使用して表示する必要があります。 したがって、属性が [!DNL Adobe Analytics] に表示されないように属性を削除する場合は、属性の購読を削除するだけで済みます。

また、[!DNL Marketo Measure] で B2B 顧客属性の接続を削除し、接続設定から除外して共有したくない属性で再作成することもできます。 同様に、統合に属性を追加するには、既存の接続を削除し、目的の属性を設定に追加して新しい接続を作成する必要があります。

上記を考慮すると、属性接続を初めて設定する際には、属性を選択する際にできるだけ包括的にすることを強くお勧めします。

**この統合のユースケースの例を教えてください。**

1. アカウントベースのトラフィック指標：アカウント名の属性を使用すると、Adobe Analyticsで 1 つ以上のターゲットアカウントのセグメントを作成し、ターゲットアカウントから発生するトラフィックのサブセットのみを対象とするサイトトラフィック指標を分析できます。
1. コンテンツ分析：売上高指標を使用すると、最終的に製品やサービスを購入した顧客や、興味のある特定のファネルステージに到達した顧客に最も魅力的なサイトコンテンツを分析できます。
1. ライブディールサポート：CRM の特定のオープンオポチュニティに関連付けられたユーザーのサイト行動を分析することで、販売チームに実用的なインサイトを提供します。
