---
unique-page-id: 18874690
description: 接続されたアカウントの再認証 — [!DNL Marketo Measure]  — 製品ドキュメント
title: 接続されたアカウントの再認証
exl-id: 7abd1d67-5bed-45bb-844f-0ffd23c3d7f8
source-git-commit: 65e7f8bc198ceba2f873ded23c94601080ad0546
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# 接続されたアカウントの再認証 {#reauthorizing-connected-accounts}

アカウントが [!DNL Marketo Measure] アカウントの場合、プラットフォームのステータスは「認証が必要」に変わり、赤い鍵のアイコンが表示されます。

広告プラットフォームが切断された場合、 [!DNL Marketo Measure] はコストデータをダウンロードできなくなります。また、自動タグ付けを有効にしている場合は、 [!DNL Marketo Measure] 新しく作成された広告に対する UTM パラメーター。 [!DNL Marketo Measure] アカウントの切断中に広告プラットフォームから作成されたタッチポイントに UTM パラメーターを遡って追加することはできません。

CRM プラットフォームが切断された場合、 [!DNL Marketo Measure] を更新できません [!DNL Marketo Measure] 新しいタッチポイントを組織に取り込むか、プッシュします。 CRM 接続が再確立されたら、 [!DNL Marketo Measure] は、アカウントの切断中にミスされたデータをプッシュします。

![](assets/1-1.png)

## 切断されたアカウントの再認証 {#re-authorizing-disconnected-accounts}

1. に移動します。 [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target=&quot;_blank&quot;} にログインし、ログインします。
1. 選択 **[!UICONTROL 設定]** の下に [!UICONTROL マイアカウント] 」タブをクリックします。
1. 左側の「統合」セクションを見つけ、 **[!UICONTROL 接続]**.
1. 再接続する必要があるアカウントの横にある赤い鍵記号を選択します。
1. ポップアップウィンドウが表示され、アカウントのログインの詳細を入力するよう求められます。
