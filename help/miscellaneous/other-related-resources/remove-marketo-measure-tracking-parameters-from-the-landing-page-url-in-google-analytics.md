---
unique-page-id: 18874736
description: Google Analyticsのランディングページ URLから [!DNL Marketo Measure]  トラッキングパラメーターを削除 –  [!DNL Marketo Measure]
title: Google Analytics のランディングページ URL からの [!DNL Marketo Measure] トラッキングパラメーターの削除
exl-id: ec81ba4a-bb10-49fd-b62e-5a1bc9e1a023
feature: Tracking
TQID: https://experienceleague.adobe.com/vKhwWUT0VQ1Kr-3-dWVWt08S4848Q0Bn4HYrGgHawb8
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 8%

---

# Google Analyticsのランディングページ URLから[!DNL Marketo Measure] トラッキングパラメーターを削除 {#remove-marketo-measure-tracking-parameters-from-the-landing-page-url-in-google-analytics}

[!DNL Google Analytics]でランディングページを表示する際に、URLからトラッキングパラメーターを削除する場合があります。 それ以外は、個々の行に分割されます。

幸いなことに、これは簡単な修正です。

1. [!DNL Google Analytics]で、[!UICONTROL 管理者] >[!UICONTROL 設定の表示] >[!UICONTROL URL クエリパラメーターの除外]に移動します。
1. ボックスに「_bt,_bk,_bm,_bn,_bg」と入力します（引用符を除く）。
1. 下にスクロールして、**[!UICONTROL 保存]**&#x200B;をクリックします。

   [!DNL Google Analytics]はデータを再処理しません。 したがって、この変更は今後のみ反映され、過去のデータはbt、bk、およびbm パラメーターで引き続き表示されます。
