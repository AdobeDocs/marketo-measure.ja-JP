---
unique-page-id: 18874736
description: 削除 [!DNL Marketo Measure] ランディングページ URL からのトラッキングパラメーター (Google Analyticsー ) - [!DNL Marketo Measure]  — 製品ドキュメント
title: Google Analytics のランディングページ URL からの [!DNL Marketo Measure] トラッキングパラメーターの削除
exl-id: ec81ba4a-bb10-49fd-b62e-5a1bc9e1a023
feature: Tracking
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 18%

---

# Google Analytics のランディングページ URL からの[!DNL Marketo Measure]トラッキングパラメーターの削除 {#remove-marketo-measure-tracking-parameters-from-the-landing-page-url-in-google-analytics}

でランディングページを表示する際に [!DNL Google Analytics]に値を指定しない場合、URL からトラッキングパラメーターを削除する必要があります。 そうしないと、個々の行に分割されます。

幸い、これは簡単な修正です。

1. In [!DNL Google Analytics]に移動します。 [!UICONTROL 管理者] >[!UICONTROL 設定を表示] >[!UICONTROL URL クエリパラメーターの除外].
1. ボックスに「_bt,_bk,_bm,_bn,_bg」と入力します（引用符を除く）。
1. 下にスクロールして、 **[!UICONTROL 保存]**.

   次の点に注意してください。 [!DNL Google Analytics] はデータを再処理しません。 したがって、この変更は前に進む方向にのみ反映され、過去のデータは bt、bk、bm の各パラメータと共に表示されます。
