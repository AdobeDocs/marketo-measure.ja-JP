---
unique-page-id: 18874658
description: 一般的な使用例 — [!DNL Marketo Measure]  — 製品ドキュメント
title: 一般的なユースケース
exl-id: bf271658-9460-4fb2-9a0f-0c7404348421
feature: Reporting
source-git-commit: e24e01a03218252c06c9a776e0519afbddbe2b8c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%

---

# 一般的なユースケース {#common-use-cases}

以下に、一般的な使用方法を示します [!DNL Marketo Measure Discover] マーケティングパフォーマンスに関する貴重なインサイトを得るため。

## チャネル別の売上高 {#revenue-by-channel}

マーケティング活動による売上高への影響をチャネル別に確認するには、 [!DNL Marketo Measure Discover]. デフォルトでは、グラフおよびタイルには、過去 12 ヶ月間のクローズドウォンの売上高がマーケティングチャネル別に分類して表示されます。 このデータは、役割ベースのビューの CMO ダッシュボードでも表示できます。

>[!TIP]
>
>ボードの上の指標フィルターを調整して、ROI、支出、パイプライン売上高、契約、商談、連絡先、またはリード別に要約されたグラフと表を表示します

## クローズ済み収益 {#closed-revenue}

マーケティングの全体的な売上高への影響を特定したい場合は、 [!DNL Marketo Measure Discover] が概要と CMO ダッシュボードのメインタイルに表示されます。指標フィルターは売上高に、日付タイプは終了日に設定されています。 日付タイプは、「タッチポイント日」および「作成日」（商談の作成日）にも変更できます。

## 作成済みの取引先責任者 {#contacts-created}

作成された連絡先の合計数をディメンション別にグループ化するには、Discover の概要または CMO ダッシュボードに移動し、タイルの上にあるフィルターを開き、指標フィルターを「連絡先」に調整して、日付タイプを作成日に移動します。 完了です。

合計コンタクト先数を取得する場合、または経時的な合計コンタクト先数を確認する場合は、成長ダッシュボードに移動し、「日付タイプ」を「作成日」に調整して、目的の期間を選択します。 取引先責任者と取引先責任者の推移は、このダッシュボード内の取引先責任者に焦点を当てたタイルです。

日付タイプは、タッチポイント日に変更することもできます。 マーケティングインタラクションが発生した日からの連絡先の数が表示されます。

## 作成済みリード {#leads-created}

作成されたリードの合計数をディメンション別にグループ化するには、Discover の概要または CMO ダッシュボードに移動し、タイルの上にあるフィルターを開き、指標フィルターを「リード」に調整し、日付タイプを「作成日」に調整します。 これで、各チャネルがリード作成にどのように貢献しているかを、優れたビジュアライゼーションで確認できます。

合計リード数を取得したり、経時的にリード作成を確認したりするには、成長ダッシュボードに移動し、「日付タイプ」を「作成日」に調整して、目的の日付範囲を選択します。 リードとリードの推移は、このダッシュボードのリードに焦点を当てたタイルです。

日付タイプは、タッチポイント日に変更することもできます。 マーケティングインタラクションが発生した日からのリード数が表示されます。

## 創出した商談 {#opportunities-created}

分類マーケティングがオポチュニティの作成に与える影響を表示するには、概要または CMO ボードを選択し、フィルターを展開して、指標フィルターを商談に調整し、日付タイプを作成日に変更します。

商談の合計値を確認したり、経時的なトレンドを表示したりするには、成長ダッシュボードを使用し、フィルターで「日付タイプ」を「作成日」に調整します。 このダッシュボードの「商談」タイルと「長期的な商談」タイルを確認します。

日付タイプは、（アクティビティの日付に基づいて）タッチポイント日に変更したり、クローズ日に変更したりして、クローズした獲得の合計数を表示したりできます _および_ クローズした商談 — 損失商談。

## クローズ済みの契約 {#closed-deals}

特定の期間内のクローズした契約に対するマーケティングの影響をチャネル別に分類して表示する場合は、概要または CMO ダッシュボードに移動し、指標フィルターを商談に、日付タイプをクローズ日に調整します。

契約の合計数や経時的なトレンドを確認するには、成長ダッシュボードを使用し、単に「Date Type」を「Close Date」に調整します。 また、日付タイプは、アクティビティの日付に基づいてタッチポイント日に変更したり、作成日に変更したりすると、クローズ日と同じ結果が表示されます。

## 生成されたパイプラインの売上高 {#pipeline-revenue-generated}

マーケティングがパイプラインに与えた影響と、その効果が最も高かったチャネルを確認したい場合は、 Discover 内の概要ダッシュボードまたは CMO ダッシュボードを使用し、指標フィルターを「パイプライン売上高」および「日付タイプ」に調整して、ディメンション別にグループ化されたパイプラインの合計売上高を表示します。

パイプラインの合計値を取得する場合、または経時的にトレンドを示すパイプラインの合計売上高を確認する場合は、成長ダッシュボードを使用し、「日付タイプ」を「タッチポイント日」に調整します。 また、日付タイプを「クローズ日」に変更して、将来のクローズ日に基づいてパイプラインの量を表示することもできます。

パイプライン売上高を見る際は、日付を将来の日付範囲に変更することをお勧めします。

## 有料検索 ROI {#paid-search-roi}

キャンペーンに関するインサイトや、有料検索活動のキーワードレベルの ROI を得たい場合は、Discover の役割に基づく表示の下にある広告 ROI ダッシュボードに移動します。 また、このダッシュボードには、有料広告からの売上高、支出、パイプライン売上高、リード、連絡先、商談および契約に関する情報も表示されます。

さらに、役割ベースの表示の下の有料メディアダッシュボードは、すべての有料メディアチャネルからのインプレッション数、クリック数、ページビュー数および訪問数を表示します。

## 総支出 {#total-spend}

支出の合計と分類を表示するには、概要ダッシュボードに移動し、支出に対する指標フィルターを調整します。

また、マーケティング費用ダッシュボードにも移動できます。このダッシュボードのメインタイルには、過去 12 ヶ月の支出チャネルがマーケティングチャネル別にグループ化されて表示されます。

Dimensionフィルターを変更して、グループをサブチャネル、キャンペーン、広告主、広告グループ、キーワード、プレースメント、サイトのいずれかに変更します。

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] 大学：概要 [!DNL Marketo Measure Discover]](https://universityonline.marketo.com/courses/bizible-discover/#/page/5c645586a7863a73ad3b23e6){target="_blank"}