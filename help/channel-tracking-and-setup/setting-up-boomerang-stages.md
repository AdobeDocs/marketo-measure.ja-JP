---
description: Marketo Measure ユーザー向けのBoomerang ステージガイダンスの設定
title: ブーメランステージの設定
exl-id: 00dd2826-27a3-462e-a70e-4cec90d07f92
feature: Boomerang
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: 1096bc28-f8ba-5a87-abf9-ad1b68c31f97
    internal-label: Boomerang
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 5%
---
# ブーメランステージの設定 {#setting-up-boomerang-stages}

>[!AVAILABILITY]
>
>Boomerang機能は、Tier 2および3のお客様に対してのみ有効です。 より高いレベルのアカウントをリクエストするには、Adobe アカウントチーム（担当のアカウントマネージャー）にお問い合わせください。

アカウントの[!UICONTROL Boomerang] ステージを有効にするには、アカウント管理者である必要があります。 または、[Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}に連絡して有効にすることもできます。 機能を有効にした後、次の手順に従って設定します。

## ブーメランのステージ設定 {#boomerang-stage-setup}

1. [!UICONTROL  ステージマッピング ]に移動します。 「[!UICONTROL Boomerang]」というタイトルの列で、追跡するステージの横にあるボックスを選択します。

   ![1. ステージマッピングに移動します。 「Boomerang」 ](assets/boomerang-stages-18.png)というタイトルの列の下

1. 「[!UICONTROL  アトリビューション設定]」タブに移動し、表示する各ステージのタッチポイントの数を入力します。 最大10個まで指定できます。 デフォルトは1に設定されています。

   ![1. 「アトリビューション設定」タブに移動し、数値](assets/boomerang-stages-19.png)を入力します

1. 「**[!UICONTROL 保存]**」をクリックします。

   >[!NOTE]
   >
   >これらの変更に従ってデータを再処理するには、24～48時間かかります。

## カスタムモデルアトリビューションによるブーメランステージの設定 {#boomerang-stage-setup-with-custom-model-attribution}

1. [!UICONTROL  ステージマッピング ]に移動します。 「[!UICONTROL Boomerang]」というタイトルの列で、追跡するステージの横にあるボックスを選択します。

   ![1. ステージマッピングに移動します。 「Boomerang」 ](assets/boomerang-stages-20.png)というタイトルの列の下

1. これらのブーメランのステージをカスタムモデルに含め、アトリビューションクレジットを受け取りたい場合は、必ず「[!UICONTROL  カスタムモデル ]」列の下にあるボックスも選択してください。

   ![1. これらのブーメラン段階も含めたい場合](assets/boomerang-stages-21.png)

1. 「[!UICONTROL  アトリビューション設定]」タブに移動します。 ブーメラン段階におけるアトリビューションに対する重み付けを決定します。 オプションは、最初に発生したアトリビューション、最後に発生したアトリビューションに重みを付けるか、すべてのオカレンスに均等に分割することです。

   ![1. 「アトリビューション設定」タブに移動します。 希望する方法を決定](assets/boomerang-stages-22.png)

1. 表示したい各ステージの出現回数を入力します。 最大10個まで指定できます。 デフォルトは1に設定されています。

   ![1. 各ステージの出現回数を入力します。](assets/boomerang-stages-23.png)

1. カスタムモデルに含まれているBoomerang ステージに割り当てるアトリビューションの割合を設定します。 すべての段階の合計アトリビューションが最大100%になります。 「**[!UICONTROL 保存して処理]**」をクリックします。

   ![1. ](assets/boomerang-stages-24.png)に割り当てるアトリビューションの割合を設定します

   >[!NOTE]
   >
   >これらの変更に従ってデータを再処理するには、24～48時間かかります。
