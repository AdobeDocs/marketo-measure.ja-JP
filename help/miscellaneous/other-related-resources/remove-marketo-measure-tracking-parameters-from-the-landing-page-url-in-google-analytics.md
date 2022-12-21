---
unique-page-id: 18874736
description: 削除 [!DNL Marketo Measure] ランディングページ URL からのトラッキングパラメーター (Google Analyticsー ) - [!DNL Marketo Measure]  — 製品ドキュメント
title: 削除 [!DNL Marketo Measure] ランディングページ URL からのトラッキングパラメーター (Google Analytics)
exl-id: ec81ba4a-bb10-49fd-b62e-5a1bc9e1a023
source-git-commit: 09ffdbb0b1baeed870a3145268997e63a3707c97
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# 削除 [!DNL Marketo Measure] ランディングページ URL からのトラッキングパラメーター (Google Analytics) {#remove-marketo-measure-tracking-parameters-from-the-landing-page-url-in-google-analytics}

でランディングページを表示する際に [!DNL Google Analytics]に値を指定しない場合、URL からトラッキングパラメーターを削除する必要があります。 そうしないと、個々の行に分割されます。

幸い、これは簡単な修正です。

1. In [!DNL Google Analytics]に移動します。 [!UICONTROL 管理者] >[!UICONTROL 設定を表示] >[!UICONTROL URL クエリパラメーターの除外].
1. ボックスに「_bt,_bk,_bm,_bn,_bg」と入力します（引用符を除く）。
1. 下にスクロールして、 **[!UICONTROL 保存]**.

   次の点に注意してください。 [!DNL Google Analytics] はデータを再処理しません。 したがって、この変更は前に進む方向にのみ反映され、過去のデータは bt、bk、bm の各パラメータと共に表示されます。
