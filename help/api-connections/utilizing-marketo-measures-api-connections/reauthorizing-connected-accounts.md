---
unique-page-id: 18874690
description: 接続されたアカウントの再認証 – [!DNL Marketo Measure]
title: 接続されたアカウントの再認証
exl-id: 7abd1d67-5bed-45bb-844f-0ffd23c3d7f8
feature: APIs, Integration
TQID: 'https://experienceleague.adobe.com/mp53G9-w1l43mBQM1ijW8tTh7rNQ75cPAimZA-kdLvs'
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: c8f57308-7e33-4e41-a385-b55041c78939
    internal-label: Integrations
  - id: fb43f4c1-87d9-4081-8df1-6fe7e6e5cdc8
    internal-label: APIs
  - id: 7da342c5-06ee-5869-b3e8-b73d5bf75a9d
    internal-label: Integration
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 5%
---
# 接続されたアカウントの再認証 {#reauthorizing-connected-accounts}

アカウントが[!DNL Marketo Measure] アカウントから切断されると、プラットフォームのステータスが「承認必須」に変わり、赤いキーアイコンが表示されます。

広告プラットフォームが切断されると、[!DNL Marketo Measure]はコストデータをダウンロードできなくなります。また、自動タグ付けが有効になっている場合は、新しく作成された広告に[!DNL Marketo Measure] UTM パラメーターを追加します。 アカウントが切断されている間、広告プラットフォームから作成されたタッチポイントにUTM パラメーターを過去にさかのぼって追加することはできません。[!DNL Marketo Measure]

CRM プラットフォームが切断された場合、[!DNL Marketo Measure]は[!DNL Marketo Measure] データを更新したり、新しいタッチポイントを組織にプッシュしたりすることはできません。 CRM接続が再確立されると、[!DNL Marketo Measure]は、アカウントが切断されたときに見逃したデータをすべてプッシュします。

![](assets/1-1.png)

## 切断されたアカウントの再認証 {#re-authorizing-disconnected-accounts}

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}に移動してログインします。
1. 左上隅の「[!UICONTROL  マイアカウント ]」タブで「**[!UICONTROL 設定]**」を選択します。
1. 左側の「統合」セクションを見つけて、**[!UICONTROL 接続]**&#x200B;をクリックします。
1. 再接続する必要があるアカウントの横にある赤いキー記号を選択します。
1. ポップアップウィンドウが表示され、アカウントのログイン詳細を入力するよう求められます。
