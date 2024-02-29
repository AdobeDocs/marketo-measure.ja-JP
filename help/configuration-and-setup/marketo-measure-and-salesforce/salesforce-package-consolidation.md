---
description: '[!DNL Salesforce] パッケージ統合 — [!DNL Marketo Measure]'
title: '[!DNL Salesforce] パッケージ統合'
exl-id: ae559f5f-91bf-4504-9d5a-af47f95ca01f
feature: Salesforce
source-git-commit: 518a984b0d8d640290bd9b637221fcdc0948e5b9
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 5%

---

# [!DNL Salesforce] パッケージの統合 {#salesforce-package-consolidation}

ユーザーエクスペリエンスを向上し、使い方を簡単にするために、既存のパッケージを 1 つの包括的なパッケージにコンパイルしています。

## パッケージの除去 {#package-retirement}

この統合の結果、現在の V1、V2_EXT、V2_Security およびすべてのレポートパッケージは、2023 年 8 月以降に廃止されます。 既に V2 パッケージがインストールされている場合は、新しい統合バージョンに更新する必要があります。

## 新しい統合パッケージ {#new-consolidated-package}

新しく統合された V2 パッケージは、以前のパッケージのすべての機能を組み込み、ユーザーエクスペリエンスを向上させます。 この更新されたパッケージは、マーケティングと販売のパフォーマンストラッキングをより効率的におこなえ、顧客の行動に関するより深いインサイトを得ることができます。

レポート機能を強化するための新しいフィールドが 2 つあります。

* form_name：BT/BAT オブジェクトで使用できるようになったこのフィールドにより、ユーザーはフォーム名に基づいてレポートを作成できます。
* user_touchpoint_id：このフィールドを使用すると、ユーザーは一意のユーザータッチポイント数 (`bizible2__User_Touchpoint_V2__c` （Salesforce 内）。

## サポートと移行 {#support-and-transition}

The [サポートチーム](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} は、質問に答え、新しい統合パッケージへのスムーズな移行を確実におこなうための支援を提供します。

## 必要なアクション {#retired-actions}

* 既に V2 パッケージがインストールされている場合は、新しい統合バージョンに更新する必要があります。
* レポートパッケージにレポートやダッシュボードがある場合は、すべてのフィールドが統合パッケージに存在するので、変更を加えることなく簡単に再作成できます。
* V2_EXT パッケージのフィールドを使用するレポートがある場合は、次の手順で、統合パッケージでレポートを再作成できます。
   * V2_EXT フィールドのすべてのデータはタッチポイントフィールドで使用できるので、タッチポイント位置にフィルターを追加することで、レポートを変更して、対応する V2 タッチポイントフィールドからデータを取得できます。
   * 「アウトリーチ」テキストを含む広告コンテンツ FT を使用して、すべてのリードを取得する例。
      * V2_EXT クエリ：
         * bizible2_ext__Ad_Content_FT__c には Outreach が含まれています

![](assets/package-consolidation-1.png)

* 統合パッケージ内の対応するクエリ：
   * bizible2__Touchpoint_Position__c には FT AND が含まれています
   * bizible2__Ad_Content__c に Outreach が含まれています

![](assets/salesforce-package-consolidation-2.png)

## よくある質問 {#faq}

**統合パッケージは、既存のパッケージ内のフィールドと競合しますか？**

統合パッケージをインストールする前に、パッケージをアンインストールする必要はありません。 フィールドは別の名前空間にあるので、競合は発生しません。

**現在のパッケージのデータをバックフィルするにはどうすればよいですか？**

チケットを提出できます [サポートあり](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} BT/BAT データのバックフィルと再処理を行って、タッチポイント ID とフォーム ID のフィールドに入力します。

**V1 および V2_EXT パッケージのフィールドは、統合パッケージで使用できますか。**

あります。統合パッケージには、V1 と同じフィールドが含まれ、タッチポイントフィールドを介したオブジェクトおよび V2_EXT フィールドによる分類がさらに行われます。

**V2_EXT フィールドを使用するレポートは、統合パッケージで再作成できますか。**

あります。次の手順に従います： [必要なアクション](#retired-actions) 」セクションに入力します。
