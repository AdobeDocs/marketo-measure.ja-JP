---
unique-page-id: 27656737
description: レポートマーケティング費用 — [!DNL Marketo Measure]  — 製品ドキュメント
title: マーケティング費用のレポート
exl-id: 46b0f81c-acd1-47a5-bf75-6a943edb9009
source-git-commit: 54337a0a65b79d80ebeae6531f5e92f4f48721a7
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# マーケティング費用のレポート {#report-marketing-spend}

## マーケティング費用表 {#marketing-spend-table}

マーケティング支出テーブルに、各チャネル、サブチャネル、キャンペーン行の通貨を表示する新しい列が追加されます。 この新しい列は、多通貨が有効になっていない場合でも、すべての顧客に対して表示されます。

表に様々な通貨が混在して表示されます。 単一の通貨でチャネル、サブチャネルまたはキャンペーンの合計を取得する必要がある場合は、マーケティング費用ダッシュボードを参照してください。

## コストのアップロード {#upload-costs}

ユーザーがコストファイルをダウンロードすると、ファイルには各行の通貨を示す新しい列も含まれます。 許容できる通貨は、CRM に設定および格納された通貨のみです。 お使いの通貨の 3 文字の省略コード (USD、CAD、JPY、EUR) を知る必要があり、ファイルが認識できない通貨でアップロードされると、ファイルのアップロードが失敗します。

## 広告統合によるコスト {#costs-from-ad-integrations}

条件 [!DNL Marketo Measure] は、AdWords、Bing、Facebook、Doubleclick など、接続されたプラットフォームからコストを読み込みます。レポートされた通貨も使用します。 マーケティング費用テーブルに表示されると、通貨がチャネル、サブチャネル、キャンペーンと共に表示されます。

広告プロバイダーの通貨が CRM から取り込まれた通貨と一致しない場合、「混在通貨」エラーが [!DNL Marketo Measure Discover] その通貨を換算できなかったからです。 これを修正するには、CRM 管理者が不明な通貨のコンバージョンを追加する必要があります。

## コンバージョン済みのマーケティング費用に移行 {#migrate-to-converted-marketing-spend}

マーケティング支出は歴史的に単一 (USD) の通貨に過ぎないので、報告されたすべての支出を新しい通貨に変更するのに必要な作業量は少なくなります。 アカウントで多通貨が有効になっていない場合でも、USD 以外の会社通貨が 1 つある場合は、この移行を行う必要があります。

1. 現在の支出ファイルを CSV にダウンロード
1. 通貨列に「[!UICONTROL USD]「想定通貨として。 「[!UICONTROL USD]」をクリックするか、検索と置換を使用して、[!UICONTROL USD]&quot;インスタンスを自分の会社通貨（例： &quot;）に[!UICONTROL EUR]&quot;または&quot;[!UICONTROL GBP]「」など。
1. ファイルを保存し、にアップロードし直します。 [!DNL Marketo Measure].
1. レポートされたコストがすべて新しい通貨として表示されます。
