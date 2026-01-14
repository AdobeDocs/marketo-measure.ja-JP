---
description: Marketo Measure ユーザー向け  [!DNL Marketo Measure]  プロファイルガイダンスの作成
title: ' [!DNL Marketo Measure] プロファイルの作成'
exl-id: dab2e2cb-fbd3-464a-9bd7-e9bf153d9848
feature: Salesforce
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---

# [!DNL Marketo Measure] プロファイルの作成 {#creating-a-marketo-measure-profile}

[!DNL Marketo Measure] プロファイルの作成方法を説明します。 [!DNL Marketo Measure] プロファイルを作成することで、データを CRM にプッシュする際に検証エラーが発生するのを防ぐことができます。

1. 特定の [!DNL Marketo Measure] プロファイルを作成します。

   * [!DNL Marketo Measure] Administrator 権限セットの割り当て
   * コンバート済みリードを表示および編集する権限を有効にする

   >[!NOTE]
   >
   >このプロファイルは、[!DNL System Admin] プロファイルのクローンにすることができます

1. 専用の [!DNL Marketo Measure] ユーザーを作成しました。

   * 新しい [!DNL Marketo Measure] プロファイルをそのユーザーに割り当てます。
   * 「マーケティングユーザー」をユーザーレベルの権限として有効にする

1. すべてのトリガー、ワークフロー、プロセスからこのプロファイルを除外します。
1. [!DNL Marketo Measure] アカウントにログインし、新しいユーザーで [!DNL Salesforce] の接続を再認証します。

   * [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"} に移動し、新しいユーザーの実稼働Salesforceの資格情報を使用してログインします
   * 「[!UICONTROL  マイアカウント ]」ドロップダウン内の「[!UICONTROL  設定 ]」を選択します
   * 「[!UICONTROL  統合 ]」グループ内の「[!UICONTROL  接続 ]」を選択します
   * 現在接続されている [!DNL Salesforce] 接続の右側にあるキーアイコンをクリックし、「実稼動を再認証」を選択します。 プロンプトが表示されたら、新しいユーザー資格情報で再度ログインします

   完了!

   専用の [!DNL Marketo Measure] プロファイルの作成に関するご質問は、Adobe アカウントチーム（アカウントマネージャー）または [Marketo サポート ](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} にお問い合わせください。
