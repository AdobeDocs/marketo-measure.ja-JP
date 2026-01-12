---
description: Google Analytics のランディングページ URL からの [!DNL Marketo Measure] トラッキングパラメーターの削除
title: Google Analytics のランディングページ URL からの [!DNL Marketo Measure] トラッキングパラメーターの削除
exl-id: ec81ba4a-bb10-49fd-b62e-5a1bc9e1a023
feature: Tracking
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 19%

---


# Google Analytics[!DNL Marketo Measure] ランディングページ URL からのトラッキングパラメーターの削除 {#remove-marketo-measure-tracking-parameters-from-the-landing-page-url-in-google-analytics}

[!DNL Google Analytics] でランディングページを表示する際に、URL からトラッキングパラメーターを削除しなければならないことがあります。 それ以外の場合は、個別の行に分割されます。

幸いなことに、これは簡単な修正です。

1. [!DNL Google Analytics] で、[!UICONTROL  管理者 ]/[!UICONTROL  設定を表示 ]/[!UICONTROL URL クエリパラメーターを除外 ] に移動します。
1. ボックスに「_bt,_bk,_bm,_bn,_bg」と入力します（引用符を除く）。
1. 下にスクロールして、「**[!UICONTROL 保存]**」をクリックします。

   [!DNL Google Analytics] はデータを再処理しないことに注意してください。 したがって、この変更は今後にのみ反映され、過去のデータは bt、bk、bm のパラメーターで引き続き表示されます。
