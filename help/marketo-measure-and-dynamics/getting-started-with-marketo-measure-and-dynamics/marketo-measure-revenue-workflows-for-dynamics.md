---
unique-page-id: 37356132
description: Dynamicsの[!DNL Marketo Measure]収益ワークフロー –  [!DNL Marketo Measure]
title: Dynamicsの[!DNL Marketo Measure]収益ワークフロー
exl-id: 0e64201a-bc65-4a6d-9192-09c14c810c4a
feature: Microsoft Dynamics
TQID: https://experienceleague.adobe.com/JuO-Wg0yApkF8GK--qS4tHkBweWLDbkg6Bd-qNXGUDE
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 791
ht-degree: 0%

---

# Dynamicsの[!DNL Marketo Measure]収益ワークフロー {#marketo-measure-revenue-workflows-for-dynamics}

## パート 1：見積もり収益と実際の収益 {#part-estimated-revenue-vs-actual-revenue}

[!DNL Marketo Measure]は、標準の収益フィールド （実収益）を1つポイントしますが、Dynamicsには、実収益と推定収益の2つの標準収益フィールドがあります。 「もっと知る」ダッシュボードでパイプライン収益を利用できるようにするには、商談がオープンかクローズか（ウォン）に応じて、「見積もり収益」または「実収益」フィールドから正しい金額を取得するために、カスタムフィールドとワークフローが必要です。

手順1: Dynamicsでカスタム商談金額フィールドを作成する

>[!NOTE]
>
>すべてのDynamics収益フィールドには、基本フィールドと通常のフィールドがあります。 ベースフィールドを無視します。

手順2：手順1で作成したカスタム商談金額フィールドと[!DNL Marketo Measure]商談金額フィールドの両方を更新するワークフローを作成します。

>[!NOTE]
>
>「Dynamics アカウントを使用して検索」の「[!DNL Marketo Measure] Opportunity Amount （bizible2_bizible_opportunity_amount）」フィールドを指定することはできません。 Dynamicsのお客様は、[!DNL Marketo Measure]が「もっと知る」で指すように、カスタム商談金額フィールドを作成する必要があります。 完了したら、お客様は、カスタム商談金額フィールドの[!DNL Marketo Measure]商談金額（bizible2_bizible_opportunity_amount） **および**&#x200B;の両方&#x200B;**を更新するワークフローを作成する必要があります。**[!DNL Marketo Measure] Opportunity Amount フィールドにはパッケージが付属していますが、カスタムフィールドを作成する必要があります。

金額ワークフロー手順：

**ワークフロー#1**：商談 – [!DNL Marketo Measure]件の商談金額フィールドとカスタムフィールド =推定収益

このワークフローは、予定収益が変更されるたびにオープン商談で実行され、[!DNL Marketo Measure]商談金額フィールドとカスタムフィールドを更新して、予定収益フィールドと等しくします。 ワークフローは「リアルタイム」で実行するように設定する必要がありますが、オープンな商談を更新するために「オンデマンド」で実行することもできます。

[!DNL Marketo Measure]の連絡先に、カスタム商談金額フィールドの名前を入力します。 [!DNL Marketo Measure] アプリの商談設定を更新して、カスタム商談金額フィールドの名前を含めます。 レポートで使用するフィールドを検索します。

**ワークフロー#2**：商談 – [!DNL Marketo Measure]件の商談金額フィールドとカスタムフィールド =実際の収益

このワークフローは、ユーザーが商談をクローズし、[!DNL Marketo Measure]商談金額フィールドとカスタムフィールドを更新し、商談がクローズとしてロックされる前に、商談クローズフォームに実際の収益を追加した場合に開始されます。

## パート 2：見積もりクローズ日と実際のクローズ日の比較 {#part-estimated-close-date-vs-actual-close-date}

デフォルトでは、Dynamicsには「見積クローズ日」と「実際のクローズ日」の2つのストック クローズ日フィールドがあるため、デフォルトではパイプライン収益データはダッシュボードで使用できません。 [!DNL Marketo Measure]は、ダッシュボード内の1つのクローズ日フィールドのみをポイントでき、実際のクローズ日をポイントしています。

「実際のクローズ日」フィールドにオープン商談にデータがない場合、オープン商談用のデータはダッシュボードにありません。 ただし、両方の日付フィールドをサポートするために、オポチュニティステージに基づいたワークフローが必要です。

1. 商談オブジェクト （[!DNL Marketo Measure] カスタム終了日）にカスタム終了日フィールドを作成します。
1. ワークフローを作成して、[!DNL Marketo Measure] カスタム終了日フィールドを、商談が開いているか閉じているかに応じて、予定終了日または実際の終了日のいずれかからの日付で更新します（ワークフローを保存してリアルタイムで実行する必要がありますが、現在のすべての開いている商談を更新するには、少なくとも1回「オンデマンド」で実行する必要があります）。
1. ワークフローをテストし、機能することを確認します。
1. お客様は、カスタム終了日API名を[!DNL Marketo Measure]に指定できます。
1. [!DNL Marketo Measure]は、[!DNL Marketo Measure] アプリ設定を更新して、ダッシュボードの[!DNL Marketo Measure] カスタム終了日フィールドを指すようにします。

   上記の手順が完了したら、ワークフローを実行して、過去の商談に関するカスタム [!DNL Marketo Measure]商談額フィールドと[!DNL Marketo Measure] カスタム成約日フィールドの両方を更新し、正しいデータを反映します。 これにより、変更されたオン/バイフィールドが変更される可能性があります。そのため、問題が発生していないかどうかをチームで確認する必要があります。

クローズした商談を更新するには…

1. ワークフローがアクティブになるまで、[!DNL Marketo Measure]の開始日から終了した商談を分離します。 ワークフローを通じて更新する必要がある過去の商談のグループです。
1. すべてのレコードをExcelにエクスポートします。
1. Excel ファイルを開き、コンテンツを有効にします。
1. 実際のクローズ日データを[!DNL Marketo Measure] カスタム クローズ日にコピーします。
1. 実際の収益データを[!DNL Marketo Measure] カスタム商談金額&#x200B;**および** [!DNL Marketo Measure]商談金額にコピーします（2つのフィールドがあります）。
1. ファイルを保存。
1. ファイルを読み込みます。 Dynamicsは、これを更新する既存のレコードを含むファイルとして認識します。
1. インポートファイルのエラーを確認します。

>[!NOTE]
>
>このドキュメントで説明するワークフローは、フィールドを更新して、[!DNL Marketo Measure]が「もっと知る」で正しいデータを表示できるようにする方法の1つにすぎません。 同じタスクを達成する別の方法があれば、それを実行できます。 基本的に、次のことを実現できるワークフローが必要です。
>
> * Opp = Openの場合は、カスタムのクローズ日フィールド、カスタムの商談金額フィールドおよび[!DNL Marketo Measure] opp金額フィールドをそれぞれ、見積もりクローズ日と見積もり収益に等しい値に更新します。
> * 商談=クローズ日の場合は、カスタムのクローズ日フィールド、カスタムの商談金額フィールドおよび[!DNL Marketo Measure]商談金額フィールドをそれぞれ実際のクローズ日と実際の収益に更新します。
