---
unique-page-id: 18874767
description: Boomerang ステージの設定 –  [!DNL Marketo Measure]
title: ブーメランステージの設定
exl-id: 00dd2826-27a3-462e-a70e-4cec90d07f92
feature: Boomerang
TQID: https://experienceleague.adobe.com/2H-AGYIsCbmW2sakkMBRPTcz6LWn48HJEcfCwanx8kw
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 5%

---

# ブーメランステージの設定 {#setting-up-boomerang-stages}

>[!AVAILABILITY]
>
>Boomerang機能は、Tier 2のお客様に対してのみ有効です。 より高いレベルのアカウントをリクエストするには、Adobe アカウントチーム（担当のアカウントマネージャー）にお問い合わせください。

アカウントの[!UICONTROL Boomerang] ステージを有効にするには、アカウント管理者である必要があります。 または、[Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}に連絡して有効にすることもできます。 機能を有効にした後、次の手順に従って設定します。

## ブーメランのステージ設定 {#boomerang-stage-setup}

1. [!UICONTROL  ステージマッピング ]に移動します。 「[!UICONTROL Boomerang]」というタイトルの列で、追跡するステージの横にあるボックスを選択します。

   ![](assets/1-2.png)

1. 「[!UICONTROL  アトリビューション設定]」タブに移動し、表示する各ステージのタッチポイントの数を入力します。 最大10個まで指定できます。 デフォルトは1に設定されています。

   ![](assets/2-2.png)

1. 「**[!UICONTROL 保存]**」をクリックします。

   >[!NOTE]
   >
   >これらの変更に従ってデータを再処理するには、24～48時間かかります。

## カスタムモデルアトリビューションによるブーメランステージの設定 {#boomerang-stage-setup-with-custom-model-attribution}

1. [!UICONTROL  ステージマッピング ]に移動します。 「[!UICONTROL Boomerang]」というタイトルの列で、追跡するステージの横にあるボックスを選択します。

   ![](assets/3-1.png)

1. これらのブーメランのステージをカスタムモデルに含め、アトリビューションクレジットを受け取りたい場合は、必ず「[!UICONTROL  カスタムモデル ]」列の下にあるボックスも選択してください。

   ![](assets/4-1.png)

1. 「[!UICONTROL  アトリビューション設定]」タブに移動します。 ブーメラン段階におけるアトリビューションに対する重み付けを決定します。 オプションは、最初に発生したアトリビューション、最後に発生したアトリビューションに重みを付けるか、すべてのオカレンスに均等に分割することです。

   ![](assets/5-1.png)

1. 表示したい各ステージの出現回数を入力します。 最大10個まで指定できます。 デフォルトは1に設定されています。

   ![](assets/6-1.png)

1. カスタムモデルに含まれているBoomerang ステージに割り当てるアトリビューションの割合を設定します。 すべての段階の合計アトリビューションが最大100%になります。 「**[!UICONTROL 保存して処理]**」をクリックします。

   ![](assets/7-1.png)

   >[!NOTE]
   >
   >これらの変更に従ってデータを再処理するには、24～48時間かかります。
