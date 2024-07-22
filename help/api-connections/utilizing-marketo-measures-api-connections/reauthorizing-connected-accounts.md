---
unique-page-id: 18874690
description: 接続されたアカウントの再認証 –  [!DNL Marketo Measure]
title: 接続されたアカウントの再認証
exl-id: 7abd1d67-5bed-45bb-844f-0ffd23c3d7f8
feature: APIs, Integration
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 3%

---

# 接続されたアカウントの再認証 {#reauthorizing-connected-accounts}

アカウントが [!DNL Marketo Measure] アカウントから切断されると、プラットフォームのステータスが「認証が必要」に変わり、赤いキーアイコンが表示されます。

広告プラットフォームが切断され [!DNL Marketo Measure] と、コストデータをダウンロードできなくなります。また、自動タグ付けを有効にしている場合は、新しく作成した広告に [!DNL Marketo Measure] UTM パラメーターを追加します。 [!DNL Marketo Measure] カウントが切断されている間は、広告プラットフォームから作成されたタッチポイントに UTM パラメーターをさかのぼって追加することはできません。

CRM プラットフォームが切断され [!DNL Marketo Measure] と、[!DNL Marketo Measure] データの更新や新しいタッチポイントの組織へのプッシュができなくなります。 CRM 接続が再確立されると、アカウントの切断中に失 [!DNL Marketo Measure] たデータはすべてプッシュされます。

![](assets/1-1.png)

## 切断されたアカウントの再認証 {#re-authorizing-disconnected-accounts}

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} に移動し、ログインします。
1. 左上隅の **[!UICONTROL マイアカウント [!UICONTROL  タブで ] 設定]** を選択します。
1. 左側の「統合」セクションを見つけ、「**[!UICONTROL 接続]**」をクリックします。
1. 再接続する必要があるアカウントの横にある赤い鍵の記号を選択します。
1. ポップアップウィンドウが表示され、アカウントのログインの詳細を指定するように求められます。
