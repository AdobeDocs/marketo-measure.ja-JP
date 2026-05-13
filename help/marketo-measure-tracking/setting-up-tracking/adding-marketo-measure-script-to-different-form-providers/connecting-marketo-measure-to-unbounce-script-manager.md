---
unique-page-id: 18874743
description: バウンス解除スクリプト マネージャーに [!DNL Marketo Measure] を接続しています –  [!DNL Marketo Measure]
title: Unbounce Script Manager への [!DNL Marketo Measure] の接続
exl-id: c3212bc3-1d8f-4da5-bb2d-11ffd2fb4e98
feature: Tracking
TQID: https://experienceleague.adobe.com/Bo0BFhBLbNfX89BScumswE7WvVzztOak1P38xcXdk1M
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 10%

---

# [!DNL Marketo Measure]をバウンス解除スクリプト マネージャーに接続しています {#connecting-marketo-measure-to-unbounce-script-manager}

[!DNL Marketo Measure]はバウンス解除と直接統合され、ランディングページのコンバージョンのデジタルマーケティングソースを[!DNL Salesforce]で直接追跡できます。 接続するには、バウンス解除スクリプトマネージャーに[!DNL Marketo Measure] スクリプトを追加するだけです。 手順は次のとおりです。

1. [!DNL Unbounce] アカウントにログインします。
1. **[!UICONTROL 設定]** > **[!UICONTROL Script Manager]** > **[!UICONTROL スクリプトを追加]**&#x200B;をクリックします。
1. ポップアップで「[!UICONTROL &#x200B; カスタムスクリプト &#x200B;]」を選択し、「[!DNL Marketo Measure Marketing Analytics]」という名前を付けます。 「**[!UICONTROL スクリプトの詳細を追加]**」をクリックします。
1. ヘッドの配置を選択します。 メインランディングページとフォーム確認ダイアログにスクリプトを含めます。 下の[!DNL Marketo Measure] スクリプトをボックスに貼り付けます。

   `<script type="text/javascript" src="https://cdn.bizible.com/scripts/bizible.js" async=""></script>`

1. 「**[!UICONTROL 保存]**」をクリックします。

[!DNL Marketo Measure]統合は、unbounce.com ドメインを使用していないドメイン（landing.mysite.comなど）でホストされている限り、バウンス解除ランディングページで機能します。
