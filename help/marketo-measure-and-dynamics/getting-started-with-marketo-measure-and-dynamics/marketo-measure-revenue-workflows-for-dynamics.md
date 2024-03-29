---
unique-page-id: 37356132
description: "[!DNL Marketo Measure] Dynamics の収益ワークフロー — [!DNL Marketo Measure]"
title: '"[!DNL Marketo Measure] Dynamics の収益ワークフロー»'
exl-id: 0e64201a-bc65-4a6d-9192-09c14c810c4a
feature: Microsoft Dynamics
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# [!DNL Marketo Measure] Dynamics の収益ワークフロー {#marketo-measure-revenue-workflows-for-dynamics}

## 第 1 部：推定売上高と実際の売上高 {#part-estimated-revenue-vs-actual-revenue}

[!DNL Marketo Measure] は初期設定の 1 つの標準収益フィールド（実際の収益）を指しますが、Dynamics には、実際の収益と推定売上高の 2 つの標準収益フィールドがあります。 Discover ダッシュボードでパイプライン売上高を利用するには、カスタムフィールドとワークフローを使用して、商談がオープンかクローズ（獲得）かに応じて、「推定売上高」フィールドと「実際の売上高」フィールドのどちらかから正しい金額を取得する必要があります。

手順 1:Dynamics でカスタム商談額フィールドを作成する

>[!NOTE]
>
>すべての Dynamics 収益フィールドには、基本フィールドと標準フィールドがあります。 ベースフィールドを無視します。

手順 2：手順 1 で作成したカスタム商談額フィールドと、 [!DNL Marketo Measure] 商談の金額フィールド。

>[!NOTE]
>
>我々は、 [!DNL Marketo Measure] Dynamics アカウントを使用した Discover の商談額 (bizible2_bizible_opportunity_amount) フィールド。 Dynamics のお客様は、次のカスタム商談額フィールドを作成する必要があります： [!DNL Marketo Measure] をクリックして、Discover 内のを指します。 完了したら、更新するワークフローを作成する必要があります **両方** の [!DNL Marketo Measure] 商談額 (bizible2_bizible_opportunity_amount) **および** カスタム商談額フィールド。 The [!DNL Marketo Measure] 商談額フィールドにはパッケージが付属しますが、カスタムフィールドを作成する必要があります。

ワークフローの指示数の合計：

**ワークフロー#1**：オポチュニティ — 更新 [!DNL Marketo Measure] 商談額フィールドおよびカスタムフィールド=推定売上高

このワークフローは、推定収益が変更されるたびにオープン商談に対して実行され、 [!DNL Marketo Measure] 「商談の金額」フィールドとカスタムフィールドが「推定売上高」フィールドと同じ値になるように設定します。 ワークフローは「リアルタイム」に設定する必要がありますが、「オンデマンド」で実行して、進行中の商談を更新することもできます。

次の項目を指定： [!DNL Marketo Measure] カスタム商談額フィールドの名前を持つ連絡先。 顧客が [!DNL Marketo Measure] アプリの商談設定：カスタムの商談額フィールドの名前を含めます。 これにより、レポートで使用するフィールドを Discover に知らせます。

**ワークフロー#2**：オポチュニティ — 更新 [!DNL Marketo Measure] 商談額フィールドおよびカスタムフィールド=実際の売上高

ユーザーが商談を閉じ、 [!DNL Marketo Measure] 商談がクローズ済みとしてロックダウンされる前に、商談のクローズ済みフォームに実際の収益が追加された商談額フィールドおよびカスタムフィールド。

## 第 2 部：推定クローズ日と実際のクローズ日 {#part-estimated-close-date-vs-actual-close-date}

Dynamics には、デフォルトで、「推定クローズ日」と「実際クローズ日」の 2 つの在庫クローズ日フィールドがあるので、デフォルトでは、パイプライン収益データはダッシュボードでは使用できません。 [!DNL Marketo Measure] は、ダッシュボードの 1 つの終了日フィールドのみを指し、実際の終了日を指しています。

オープン商談の「実績クローズ日」フィールドにデータがない場合、ダッシュボードにオープン商談のデータが表示されません。 ただし、両方の日付フィールドをサポートするには、商談のステージに基づいてワークフローが必要です。

1. 商談オブジェクトのカスタムクローズ日フィールドの作成 ([!DNL Marketo Measure] カスタム終了日を参照 )。
1. ワークフローを作成して、 [!DNL Marketo Measure] 商談がオープンかクローズかに応じて、Estimated Close Date または Actual Close Date の日付を含むカスタム・クローズ日フィールド（ワークフローはリアルタイムで実行する必要がありますが、現在のオープン商談を更新するには少なくとも 1 回は「オンデマンド」で実行する必要があります）。
1. ワークフローをテストし、動作を確認します。
1. カスタム終了日 API 名を次に指定するお客様： [!DNL Marketo Measure].
1. [!DNL Marketo Measure] を更新するには、 [!DNL Marketo Measure] を示すアプリ設定 [!DNL Marketo Measure] ダッシュボードのカスタム終了日フィールド。

   上記の手順が完了したら、ワークフローを実行して両方のカスタムを更新します [!DNL Marketo Measure] 「商談額」フィールドと [!DNL Marketo Measure] 正しいデータを反映する履歴商談のカスタムクローズ日フィールド。 これにより、変更された「On」/「By」フィールドが変更される可能性があるので、問題が発生したかどうかをチームに確認する必要があります。

クローズした商談を更新するには…

1. 次の期間以降にクローズした商談を分離 [!DNL Marketo Measure] 開始日は、ワークフローがアクティブになるまでです。 これは、ワークフローを介して更新する必要がある履歴商談のグループです。
1. すべてのレコードを Excel にエクスポートします。
1. Excel ファイルを開き、コンテンツを有効にします。
1. 実際のクローズ日データのコピー先 [!DNL Marketo Measure] カスタムクローズ日。
1. 実際の売上高データのコピー先 [!DNL Marketo Measure] カスタム商談額 **および** [!DNL Marketo Measure] 商談の金額（2 つのフィールドがあります）。
1. ファイルを保存します。
1. ファイルをインポートします。 Dynamics は、更新する既存のレコードを含むファイルとしてこれを認識します。
1. インポートファイルでエラーが発生していないかを確認します。

>[!NOTE]
>
>このドキュメントで概要を説明するワークフローは、フィールドの更新に関する簡単な方法です。 [!DNL Marketo Measure] を使用すると、Discover に正しいデータを表示できます。 同じ仕事を別の方法でやるなら、それを取りに行くことができます。 基本的に、次のようなワークフローが必要になります。
>
> * 商談=オープンの場合は、カスタムクローズ日フィールド、カスタム商談額フィールドを更新し、 [!DNL Marketo Measure] 商談の金額フィールドが、それぞれ「推定クローズ日」と「推定売上高」に等しくなります。
> * 商談=獲得クローズの場合、カスタムクローズ日フィールド、カスタム商談額フィールドを更新し、 [!DNL Marketo Measure] 商談額フィールドが「実際のクローズ日」と「実際の収益」にそれぞれ等しくなります。
