---
description: Marketo Measure ユーザー向けのレポートのマーケティング支出ガイダンス
title: マーケティング費用のレポート
exl-id: 46b0f81c-acd1-47a5-bf75-6a943edb9009
feature: Reporting, Spend Management
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: d24e0b99-7796-5c7d-831d-d71a1d725f01
    internal-label: Reporting
  - id: e3b4b95f-0bb9-5cb3-a479-9dcb943dca3f
    internal-label: Spend Management
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%
---
# マーケティング費用のレポート {#report-marketing-spend}

## マーケティング支出表 {#marketing-spend-table}

マーケティング支出テーブルには、チャネル、サブチャネル、キャンペーンの各行の通貨を表示する新しい列が含まれています。 この新しい列は、複数の通貨が有効になっていない場合でも、すべての顧客に表示されます。

このテーブルには、様々な通貨の組み合わせが含まれています。 単一の通貨で任意のチャネル、サブチャネルまたはキャンペーンの合計を取得するには、マーケティング費用ダッシュボードを参照してください。

## コストのアップロード {#upload-costs}

ユーザーがコストファイルをダウンロードすると、ファイルには、各行の通貨を含む新しい列も含まれます。 使用可能な通貨は、CRMに設定および保存されている通貨のみです。 お使いの通貨（USD、CAD、JPY、EUR）の3文字の略語コードを知る必要があります。認識できない通貨でファイルをアップロードすると、ファイルのアップロードに失敗します。

## 広告統合のコスト {#costs-from-ad-integrations}

[!DNL Marketo Measure]がAdWords、Bing、Facebook、Doubleclickなどの接続されたプラットフォームからコストをインポートする場合、レポートされた通貨も使用します。 マーケティング費用テーブルに表示されると、通貨はチャネル、サブチャネル、キャンペーンと共に表示されます。

広告プロバイダーの通貨がCRMから引き出された通貨と一致しない場合は、[!DNL Marketo Measure Discover]に「Mixed Currencies」エラーが表示される可能性があります。 これを修正するには、CRM管理者が不明な通貨のコンバージョンを追加する必要があります。

## コンバージョン済みのマーケティング費用への移行 {#migrate-to-converted-marketing-spend}

従来、マーケティング費用は1つの（USD）通貨でしか発生していなかったため、報告されたすべての支出を新しい通貨に変更するために必要な作業はわずかです。 お客様のアカウントで複数の通貨が有効になっていない場合でも、USD以外の法人通貨が1つしかない場合は、この移行を行う必要があります。

1. 現在の支出ファイルをCSVにダウンロード
1. 「通貨」列には、想定される通貨として「[!UICONTROL USD]」が表示されます。 「[!UICONTROL USD]」のすべての出現箇所を手動で置き換えるか、検索+置換を使用して、すべての「[!UICONTROL USD]」インスタンスを「[!UICONTROL EUR]」や「[!UICONTROL GBP]」などの独自の企業通貨に変更できます。
1. ファイルを保存し、[!DNL Marketo Measure]にアップロードし直してください。
1. 報告されたコストはすべて、新しい通貨として表示されます。
