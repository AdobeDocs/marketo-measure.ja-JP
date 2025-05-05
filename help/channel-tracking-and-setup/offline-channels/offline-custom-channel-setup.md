---
unique-page-id: 18874598
description: オフライン カスタム チャネルの設定 –  [!DNL Marketo Measure]
title: オフラインカスタムチャネル設定
exl-id: c5697714-1a79-40bd-8b7c-e10768f4ef67
feature: Channels
source-git-commit: b84909fbb34a1d8f739ebeea3400ef8816e17d32
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 1%

---

# オフラインカスタムチャネル設定 {#offline-custom-channel-setup}

## はじめに {#getting-started}

[!DNL Marketo Measure] でのオンラインチャネルルールの処理方法と比較すると、オフラインチャネルルールではスプレッドシートを使用する必要がないことがわかります。 ただし、実装計画にはシートが用意されており、オフラインチャネルを整理する方法を考える際に役立ちます。

スプレッドシートには、次の 3 つの列があります。

![](assets/1-2.png)

**[!UICONTROL Salesforce] キャンペーンタイプ** -[!DNL Salesforce] で特定されたキャンペーンタイプをここに追加

* 例えば、メール、ウェビナー、会議など、タッチポイントの属性を設定するこのフィールドに対して作成した値を指定できます。

**[!UICONTROL チャネル]** – さまざまなマーケティングチャネルをここに追加します

**[!UICONTROL サブチャネル]** – 対応するサブチャネルをここに追加します

## オフラインチャネルロジック {#offline-channel-logic}

オフラインチャネルのロジック [!DNL Marketo Measure]、キャンペーンオブジェクト（特に [!DNL Salesforce] キャンペーンタイプ）によって決定されます。 オフラインの各作業には、夕食や展示会などの [!DNL Salesforce] キャンペーンタイプが必要です。これは、このフィールドを利用して、マッピング [!DNL Marketo Measure] るチャネルとサブチャネルを把握できるためです。

SFDC キャンペーンタイプは、[!DNL Salesforce] キャンペーンタイプの下に表示されるオフラインチャネルのタブに表示されます。 買 [!DNL Marketo Measure] 手タッチポイントが関連付けられているキャンペーンの場合にのみ、SFDC キャンペーンタイプをインポートできます。

![](assets/2-2.png)

[!DNL Marketo Measure] アプリでチャネル/サブチャネルマッピングを作成できる場所です。 これには、[!DNL Marketo Measure] アプリでの新しいチャネルとサブチャネルの作成が含まれる可能性があります。これは、以下の画像に示すように、アプリの「チャネルを作成」セクションで行います。 タッチポイントのプッシュ先を把握する [!DNL Marketo Measure] めに、新しいチャネルとサブチャネルを作成する必要があります。 キャンペーンタイプのマッピング方法を決定できます。

![](assets/3-2.png)

## チャネルマッピングの例 {#channel-mapping-example}

例えば、1 年に 2 回の [!DNL Salesforce] 会議に出席するとします。 しかし、各会議は非常に異なっており、ユニークなターゲットオーディエンスを持っています。 この 2 つのうちどちらが価値をもたらすかを知りたい。 [!DNL Salesforce] 環境では、1 月のイベントにキャンペーンタイプとして「会議」を指定し、チャネルに「[!DNL Salesforce]」という名前を付け、サブチャネルに「1 月の会議」という名前を付けることができます。

次に、6 月の会議でも同じことを行います。 これは会議でもあるため、同じキャンペーンタイプ（この場合は「会議」）を指定することもできます。 チャンネルは同じで [!DNL Salesforce] く、この 2 番目の会議のサブチャンネルは「6 月の会議」です。 これは、組織の観点から見ると理にかなっています。 ただし、両方のキャンペーンのキャンペーンタイプが同じなので、これらのルールを読んで適用すると、[!DNL Marketo Measure] のロジックでは非常に混乱します。 スクリプト [!DNL Marketo Measure]、1 つのタイプから 2 つの異なるサブチャネルにデータをマッピングできません。 つまり、サブチャネルごとに新しいキャンペーンタイプを作成する必要がありますが、サブチャネルは同じチャネルを持つことができます。

次に、[!DNL Marketo Measure] が読めないロジックの例を示します。

![](assets/4-2.png)

上記のシナリオでは、同じキャンペーンタイプを 2 つの異なるサブチャネルにマッピングできないので、一意のキャンペーンタイプを作成する必要があります。 代わりに、次のような一意のタイプを設定する必要があります。

![](assets/5-2.png)

既存のキャンペーンタイプをチャネルマップに含め、「NULL」をチャネルとして追加する必要があります。

時間をかけて、既存のレコードタイプの数と特性、組み込むレコードタイプ、および上記の情報に基づいて追加のキャンペーンを作成する必要があるかどうかを [!DNL Salesforce] 認します。 必要な情報をすべて入力したら、アップロードする準備が整います。

詳しくは、[ オフライン  [!DNL Salesforce]  キャンペーンの  [!DNL Marketo Measure]](/help/channel-tracking-and-setup/offline-channels/legacy-processes/syncing-offline-campaigns.md) との同期を参照してください。

## オンラインマーケティング活動における SFDC キャンペーンの処理 {#handling-sfdc-campaigns-for-online-marketing-efforts}

マーケティングチームは、様々なデジタルマーケティングの取り組みを追跡する [!DNL Salesforce] キャンペーンを作成するのが一般的です。 この方法に問題はありませんが、ダイレクトメールや会議などの真のオフラインキャンペーンとは異なる方法でこれらのキャンペーンを扱うことが重要です。 デジタルイベント（Web サイト上で実行されるインタラクション）に関連するキャンペーンは、[!DNL Marketo Measure] と同期しないでください。 これらのキャンペーンを同期すると、[!DNL Marketo Measure] JavaScriptが既にオンラインの取り組みをトラッキングしているので、タッチポイントの重複が発生します。

オンラインアクティビティのキャンペーンを処理するもう 1 つのヒントは、[!DNL Salesforce] キャンペーンタイプを NULL にマッピングすることです。 それには、以下の画像に示すように、まず [!DNL Marketo Measure] アプリに NULL というタイトルのチャネルを作成します。 これは、[!DNL Marketo Measure] アプリの「**チャネルを作成** セクションにあります。 これは、同期すべきでないキャンペーンが誤って同期された場合に役立ちます。 NULL の下にバケット化されたすべてのものを確認することで、キャンペーンを見つけて同期ステータスを修正するのは簡単です。

![](assets/6-2.png)

## アプリへのオフラインチャネルルールの入力 {#entering-your-offline-channel-rules-to-the-app}

カスタムルールを使用してスプレッドシートを編集および更新したら、次の手順は、このチャネルマッピングを [!DNL Marketo Measure] アプリで再作成することです。実際にオフラインチャネルのスプレッドシートをアップロードすることはありません。 代わりに、以下の画像に示すように、選択リストボックスに情報を入力します。 この情報を確認するには、「**[!UICONTROL チャネル]**」セクションの「**[!UICONTROL オフラインチャネル]**」をクリックします。

![](assets/7-2.png)

>[!TIP]
>
>[!DNL Salesforce] キャンペーンタイプがチャネルマッピングに取り込まれる _タイミング_ を決定 [!DNL Marketo Measure] たい場合は、 **[!UICONTROL 設定]**/**[!UICONTROL キャンペーン]**/**[!UICONTROL フィールド]**/**[!UICONTROL タイプ]** に移動します。 その後、どの値が選択リストに含まれ、どの値が非アクティブかを確認できます。 非アクティブなチャネルは、「[!UICONTROL &#x200B; オフラインチャネル &#x200B;]」セクションで選択可能なタイプとして表示されません。 このプロセスには、数分から最大 48 時間かかる場合があります。

完了したら「**[!UICONTROL 保存]**」をクリック [!DNL Marketo Measure] ます。変更内容がアップロードされ、データが再処理されます。

>[!MORELIKETHIS]
>
>* [[!DNL Marketo Measure] チュートリアル：オフラインチャネルのマッピング](https://experienceleague.adobe.com/ja/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-salesforce/mapping-offline-channels){target="_blank"}
>
>* [[!DNL Marketo Measure] Tutorials: オフラインキャンペーンを同期しています ](https://experienceleague.adobe.com/en/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-salesforce/syncing-offline-campaigns){target="_blank"}
>
>* [Marketo Engage プログラムの統合 ](/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/marketo-engage-programs-integration.md#channel-mapping){target="_blank"}
