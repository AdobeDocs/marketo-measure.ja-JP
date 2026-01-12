---
description: Unbounce Script Manager [!DNL Marketo Measure]  の接続 –  [!DNL Marketo Measure]
title: Unbounce Script Manager への [!DNL Marketo Measure] の接続
exl-id: c3212bc3-1d8f-4da5-bb2d-11ffd2fb4e98
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 11%

---


# Unbounce Script Manager への [!DNL Marketo Measure] の接続 {#connecting-marketo-measure-to-unbounce-script-manager}

[!DNL Marketo Measure] は Unbounce と直接統合されているため、ランディングページコンバージョンのデジタルマーケティングソースを [!DNL Salesforce] で直接追跡できます。 接続を確立するには、[!DNL Marketo Measure] スクリプトを Unbounce Script Manager に追加します。 手順は次のとおりです。

1. [!DNL Unbounce] アカウントにログインします。
1. **[!UICONTROL 設定]**/**[!UICONTROL スクリプトマネージャー]**/**[!UICONTROL スクリプトを追加]** をクリックします。
1. ポップアップで [!UICONTROL  カスタムスクリプト ] を選択し、「[!DNL Marketo Measure Marketing Analytics]」という名前を付けます。 **[!UICONTROL スクリプトの詳細を追加]** をクリックします。
1. ヘッドの配置を選択します。 メインランディングページとフォーム確認ダイアログにスクリプトを含めます。 次の [!DNL Marketo Measure] スクリプトをボックスに貼り付けます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 保存]**」をクリックします。

[!DNL Marketo Measure] の統合は、unbounce.com ドメインを使用するドメインではなく、ドメイン（landing.mysite.comなど）でホストされている限り、バウンスランディングページで機能します。
