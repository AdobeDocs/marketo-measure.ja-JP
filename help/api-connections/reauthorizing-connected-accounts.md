---
description: Marketo Measure ユーザー向けの Connected Accounts ガイダンスの再認証
title: 接続されたアカウントの再認証
exl-id: 7abd1d67-5bed-45bb-844f-0ffd23c3d7f8
feature: APIs, Integration
hidefromtoc: true
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---

# 接続されたアカウントの再認証 {#reauthorizing-connected-accounts}

アカウントが [!DNL Marketo Measure] アカウントから切断されると、プラットフォームのステータスが「認証が必要」に変わり、赤いキーアイコンが表示されます。

広告プラットフォームが切断され [!DNL Marketo Measure] と、コストデータをダウンロードできなくなります。また、自動タグ付けを有効にしている場合は、新しく作成した広告に [!DNL Marketo Measure] UTM パラメーターを追加します。 [!DNL Marketo Measure] カウントが切断されている間は、広告プラットフォームから作成されたタッチポイントに UTM パラメーターをさかのぼって追加することはできません。

CRM プラットフォームが切断され [!DNL Marketo Measure] と、[!DNL Marketo Measure] データの更新や新しいタッチポイントの組織へのプッシュができなくなります。 CRM 接続が再確立されると、アカウントの切断中に失 [!DNL Marketo Measure] たデータはすべてプッシュされます。

![CRM プラットフォームが切断されると、Marketo Measureは機能しなくなります &#x200B;](assets/utilizing-connections-7.png)

## 切断されたアカウントの再認証 {#re-authorizing-disconnected-accounts}

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} に移動し、ログインします。
1. 左上隅の **[!UICONTROL マイアカウント]** タブで [!UICONTROL &#x200B; 設定 &#x200B;] を選択します。
1. 左側の「統合」セクションを見つけ、「**[!UICONTROL 接続]**」をクリックします。
1. 再接続する必要があるアカウントの横にある赤い鍵の記号を選択します。
1. ポップアップウィンドウが表示され、アカウントのログインの詳細を指定するように求められます。
