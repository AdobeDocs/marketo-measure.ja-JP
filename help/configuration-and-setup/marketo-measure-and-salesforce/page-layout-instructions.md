---
unique-page-id: 18874799
description: ページレイアウト手順 — [!DNL Marketo Measure]
title: ページレイアウトの手順
exl-id: 627377f0-d0cf-448c-a7b5-7eb5634b9627
feature: Salesforce
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# ページレイアウトの手順 {#page-layout-instructions}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」 （ドキュメント内）が表示されますが、CRM には「Bizible」が表示されます。 アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

簡単に [!DNL Marketo Measure] データを確認するには、[!UICONTROL アカウント]、[!UICONTROL 取引先責任者]、[!UICONTROL リード]、[!UICONTROL 商談]、[!UICONTROL キャンペーン]の各オブジェクトのページレイアウトを更新することをお勧めします。手順は、以下のオブジェクトページレイアウトごとに分かれています。

まず、[!DNL Salesforce] 設定に移動して、「[!UICONTROL カスタマイズ]」タブを見つけます。

## キャンペーンオブジェクト {#campaign-object}

次の項目を追加することをお勧めします。 [!DNL Marketo Measure] フィールドを SFDC Campaign に追加し、サンドボックスにのみ使用できます。 このフィールドを使用して、タッチポイントの生成をテストできます。実稼動環境では、 [!DNL Marketo Measure] タッチポイント日付の一括更新ボタン。 この [!DNL Marketo Measure] フィールドを実稼動環境に追加しました。これは、キャンペーン同期ルールを作成できるためです。

1. 「ビルド」オプションで「**[!UICONTROL キャンペーン]**」を選択します。

1. 「**[!UICONTROL ページレイアウト]**」をクリックします。

   ![](assets/1-1.jpg)

1. クリック **[!UICONTROL 編集]** をクリックします。

   ![](assets/2-1.jpg)

1. 「[!UICONTROL フィールド]」オプション内で、「**[!UICONTROL Buyer Touchpoints を有効化]**」フィールドを選択して、ページ上の任意の場所にドラッグします。次に、「**[!UICONTROL タッチポイント開始日]**」フィールドと「**[!UICONTROL タッチポイント終了日]**」フィールドを追加します。

   ![](assets/3-2.png)

1. 次に、ページ上部で、クイック検索メニューの「[!UICONTROL ボタン]」オプションをクリックします。

1. 「**[!UICONTROL Touchpoint 日の一括更新]**」ボタンをカスタムボタンセクションにドラッグします。

   ![](assets/4-1.jpg)

1. 「**[!UICONTROL 保存]**」をクリックします。

   >[!NOTE]
   >
   >複数の Campaign レコードタイプを使用する場合は、 **[!UICONTROL 購入者タッチポイントの有効化]** フィールドに入力します。 参照： [この記事](/help/channel-tracking-and-setup/offline-channels/configurations-for-multiple-campaign-record-types.md) 」を参照してください。

## リード {#leads}

1. 「ビルド」オプションで「**[!UICONTROL リード]**」を選択します。

1. 「**[!UICONTROL ページレイアウト]**」をクリックします。

1. クリック **[!UICONTROL 編集]** をクリックします。 複数のページレイアウトに「Buyer Touchpoints」セクションを含めることができます。

1. クイック検索メニュー内の左側にある [VisualForce] ページオプションをクリックします。

1. セクションを作成し、「Buyer Touchpoints」という名前を付けます。

   >[!NOTE]
   >
   >これらのセクションごとに「1 列」形式を選択します。

1. **[!UICONTROL Marketo Measure リード関連リスト]** VisualForce ページをページレイアウトセクションにドラッグします。

   ![](assets/5-1.png)

1. レンチを [!DNL VisualForce] 「高さ」を「100」に変更し、スクロールバーを有効にします。

1. メニューに戻り、 [!UICONTROL キャンバスアプリ] を参照し、タッチポイントの下に「Marketo Measure Insights」というセクションを作成します。 [!DNL VisualForce] セクションを作成しました。

   >[!NOTE]
   >
   >これらのセクションごとに「1 列」形式を選択します。

1. 新規作成したセクションに [!DNL Marketo Measure Insights] キャンバスアプリをドラッグします。「**保存**」をクリックします。Salesforce が即座に認識しないので、キャンバスアプリにドロップする前にまずページレイアウトを保存する必要が生じる場合があります。そのため、セクションを作成した後、ページレイアウトを保存し、再度編集して、そのセクション内にキャンバスアプリをドラッグします。 これは、すべてのオブジェクトに当てはまります。

   >[!NOTE]
   >
   >の [!DNL Marketo Measure Insights] キャンバスアプリが正しく機能しない問題を修正しました。 [権限は適切に設定する必要があります](/help/configuration-and-setup/marketo-measure-insights-canvas-app/marketo-measure-insights-configuration.md).

   >[!TIP]
   >
   >ほとんどのユーザーは（FT）または（LC）で終わるフィールドを使用しませんが、その理由は、それらが、[!DNL Marketo Measure] タッチポイントがオブジェクトとして存在するようになる前からのレガシーフィールだからです。

を使用している場合、 [!DNL Marketo Measure] ABM 機能 [追加のページレイアウト手順については、ここをクリックしてください。](/help/advanced-marketo-measure-features/account-based-marketing/account-based-marketing-overview.md).

## 取引先責任者 {#contacts}

1. 「ビルド」オプションで「**[!UICONTROL 取引先責任者]**」を選択します。

1. 「**[!UICONTROL ページレイアウト]**」をクリックします。

1. 編集するページレイアウトを選択します。

   クイック検索メニュー内の「関連リスト」オプションに移動し、**[!UICONTROL Buyer Touchpoints]** に関連するリストを追加します。

1. レンチアイコンをクリックし、次の列をこの順序で追加します。

   * Buyer Touchpoint
   * マーケティングチャネル
   * Touchpoint ソース
   * 広告キャンペーン名
   * Touchpoint の位置
   * Touchpoint の日付

1. 並べ替え基準：Touchpoint 日（昇順）。

   ![](assets/6.jpg)

1. 「ボタン」オプションを展開し、「**[!UICONTROL 新規]**」の選択を解除します。

   ![](assets/7.png)

1. メニューの「[!UICONTROL 関連リスト]」オプションに戻り、**[!UICONTROL Buyer Attribution Touchpoint]** 関連リストを追加します。

1. レンチアイコンをクリックし、次の列をこの順序で追加します。

   * アトリビューションタッチポイント
   * マーケティングチャネル
   * 商談
   * 広告キャンペーン名
   * Touchpoint のタイプ
   * Touchpoint の位置
   * アトリビューション％ W-字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * 収益 W 字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * Touchpoint の日付

1. [!UICONTROL Touchpoint 日]／[!UICONTROL 昇順]で並べ替えます。

1. 「ボタン」セクションを展開し、「**[!UICONTROL 新規]**」の選択を解除します。

1. 「**[!UICONTROL 保存]**」をクリックします。

## 商談 {#opportunities}

1. 「ビルド」オプションで「**[!UICONTROL 商談]**」を選択します。

1. 「**[!UICONTROL ページレイアウト]**」をクリックします。

1. 編集するページレイアウトを選択します。

1. **[!UICONTROL Buyer Attribution Touchpoint]** 関連リストを追加し、レンチをクリックして、商談に次の列を追加します。

   * アトリビューションタッチポイント
   * マーケティングチャネル
   * 取引先責任者
   * 広告キャンペーン名
   * Touchpoint のタイプ
   * Touchpoint の位置
   * アトリビューション％ W-字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * 収益 W 字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * Touchpoint の日付

1. [!UICONTROL Touchpoint 日]／[!UICONTROL 昇順]で並び替えます。

1. 「[!UICONTROL ボタン]」セクション内の「**[!UICONTROL 新規]**」の選択を解除します。

1. 「**[!UICONTROL 保存]**」をクリックします。

## アカウント {#accounts}

1. 「ビルド」オプションで「**[!UICONTROL アカウント]**」を選択します。

1. 「**[!UICONTROL ページレイアウト]**」をクリックします。

1. 編集するページレイアウトを選択します。

1. **[!UICONTROL Buyer Attribution Touchpoint]** 関連リストを追加し、レンチをクリックして、次の列を追加します。

   * アトリビューションタッチポイント
   * マーケティングチャネル
   * 商談
   * 広告キャンペーン名
   * Touchpoint のタイプ
   * Touchpoint の位置
   * アトリビューション％ W-字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * 収益 W 字型（_または最も堅牢なアトリビューションモデル（フルパスやカスタムなど）_）
   * Touchpoint の日付

1. 並べ替え基準：タッチポイントの日付／昇順。

1. 「[!UICONTROL ボタン]」セクション内の「**[!UICONTROL 新規]**」の選択を解除します。

1. 「**[!UICONTROL 保存]**」をクリックします。

を使用している場合、 [!DNL Marketo Measure] ABM 機能、 [追加のページレイアウト手順](/help/advanced-marketo-measure-features/account-based-marketing/account-based-marketing-overview.md).
