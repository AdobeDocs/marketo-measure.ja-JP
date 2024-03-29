---
unique-page-id: 18874779
description: カスタムアトリビューションモデルと設定 — [!DNL Marketo Measure]
title: カスタムアトリビューションモデルと設定
exl-id: 7b156db2-9ac6-4d32-ac67-06c0aa15d651
feature: Attribution, Custom Models
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 1%

---

# カスタムアトリビューションモデルと設定 {#custom-attribution-model-and-setup}

以下に、 [!DNL Marketo Measure] カスタムアトリビューションモデルとその設定方法を参照してください。

## カスタム属性モデル {#custom-attribution-model}

The [!DNL Marketo Measure] カスタムアトリビューションモデルを使用すると、モデルに含めるタッチポイントまたはカスタムステージを選択できます。 ユーザーは、これらのタッチポイントおよびステージに関連する売上高クレジットの割合を制御できます。または、 [!DNL Marketo Measure] 機械学習モデル。

## カスタムアトリビューションモデルの設定方法 {#how-to-set-up-your-custom-attribution-model}

1. カスタムモデルに含めるステージを決定します。

   カスタムアトリビューションモデルの作成を開始するには、マーケティングチームにとって重要なステージを選択する必要があります。 また、 [!DNL Marketo Measure] マイルストーンステージ（FT、LC、OC、クローズ済み）カスタムモデルに最大 6 つのリード/連絡先ステータスまたは商談ステージを追加できます。 例えば、MQL ステージをカスタムモデルに含めるのは一般的です。 マーケティングチームは、MQL ステージへの移行を推進している取り組みやチャネルを知りたがることがよくあります。

   ログイン先 [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}. に移動します。 [!UICONTROL マイアカウント] > [!UICONTROL 設定] /、「 CRM 」セクションで「 」を選択します。 **[!UICONTROL ステージマッピング]**.

   次に、 **[!UICONTROL モデルに含める]** ボックス。

   >[!NOTE]
   >
   >最大 6 つのカスタムステージを使用できます（デフォルトは FT、LC、OC、Closed を含みません）。

   ![](assets/1-1.png)

   >[!NOTE]
   >
   >_すべて_ ステージが非アクティブであるか、使用されなくなった場合でも、リード/連絡先および商談のステージはここに表示されます。 [!DNL Salesforce]. これらのステージを削除する場合は、 [!DNL Salesforce].

   ステージを選択したら、必ず **[!UICONTROL 保存して処理]** 」ボタンをクリックします。 これで、ステージが **[!UICONTROL 属性設定]** 」タブに移動し、各ステージにアトリビューションの割合を割り当てることができます。 また、カスタムステージは、Demand Waterfall 内のリードまたは商談のステージとしてマーケティングパフォーマンススイートに表示されます。

   モデルに含める他のステージがあるが、それらがに含まれていない場合。 [!UICONTROL リード/連絡先ステータス] または [!UICONTROL 商談のステージ] リストから、CRM のフィールドに基づいて独自のカスタムステージを定義できます。

   次の例では、日付フィールドを使用してカスタム「MQL」ステージを定義します。 ルールでは、「MQL 日付」フィールドが空でない場合は MQL と見なし、カスタムモデルに含める必要があると述べています。 また、販売サイクルの進行に従うように、カスタムステージを作成した後に並べ替えることも重要です。

   ![](assets/2-1.png)

   >[!CAUTION]
   >
   >カスタムフィールドの履歴追跡を有効にすることを忘れないでください。

カスタムフィールドがカスタムモデルで使用される場合、フィールド履歴の追跡を CRM で有効にする必要があります。 フィールド履歴の追跡を有効にする手順については、 [カスタムモデルの設定：フィールド履歴の追跡を有効にする](/help/advanced-marketo-measure-features/custom-attribution-models/custom-model-setup-enable-field-history-tracking.md).

1. カスタムモデルの属性の割合を決定します。

   次に移動： **[!UICONTROL 属性設定]** in [!DNL Marketo Measure] アプリ。カスタムステージは、アトリビューションテーブル内のここに表示されます。 アトリビューションテーブルには、 [!DNL Marketo Measure] アトリビューションモデルと、各モデルのアトリビューションの重み付けです。 最初の 5 つのモデルのアトリビューションの割合は固定され、変更できません。

   右端の「**[!UICONTROL カスタム]**「」と入力すると、カスタムアトリビューションモデルの各ステージに対して、パーセンテージの重み付けを設定できます。 「カスタム」列で各ステージの値を入力し、 **[!UICONTROL 保存して再処理]** 完了したら、

   の左側 _カスタム_ 列は **[!DNL Marketo Measure]機械学習モデル**. 機械学習モデルは、各カスタムステージで発生した処理に基づいて、契約に勝つための相対的な重要度に基づいてアトリビューションの重み付けを計算します。 機械学習モデルについて詳しくは、 [機械学習モデルに関する FAQ](/help/advanced-marketo-measure-features/custom-attribution-models/machine-learning-model-faq.md).

   ![](assets/3.png)

## タッチポイントの位置 {#touchpoint-positions}

アトリビューションの割合が保存および処理されると、タッチポイントが更新され、新しいステージおよび位置を受け取ります。 ステージの遷移の前に最近発生したタッチポイントは、そのステージのクレジットを受け取ります（下図を参照）。 カスタムの重み付けと売上高も再配分されます。

![](assets/4.png)

## ファネルステージとカスタムモデルステージの違い {#the-difference-between-funnel-stages-and-custom-model-stages}

カスタムモデルを有効にしていない場合でも、マーケティングファネルにカスタムステージを表示できるようになりました。 これは、ファネルステージ機能を使用することで実現します。 ファネルステージで、ファネルにステージを追加できるようになりましたが、ステージのアトリビューションは表示されません。

ファネルステージは、引き続きタッチポイントとして追跡され、CRM でタッチポイントポジションとして表示されます。 カスタムモデルがない場合、これらのタッチポイントは、フォーム入力がある場合は依然としてミドルタッチアトリビューションを受け取り、Web 訪問の場合は 0 アトリビューションクレジットを受け取る場合があります。

以下に示すように、ファネルステージの他に、デリジェンスステージも追加しました。 つまり、位置に Diligence が含まれるタッチポイントがありますが、カスタムモデルが有効（最大 10%）になっていない場合、それらのタッチポイントはミドルタッチ属性クレジットのみを受け取ります。

![](assets/5.png)

>[!NOTE]
>
>BAT カスタムモデルの動作は、中間タッチがない場合に、カスタムモデルのミドルタッチパーセントを他のステージに均等に分割することです。
