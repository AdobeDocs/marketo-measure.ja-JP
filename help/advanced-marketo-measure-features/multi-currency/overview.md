---
unique-page-id: 27656735
description: 概要 –  [!DNL Marketo Measure]
title: 概要
exl-id: 2076521c-b579-457c-ab1c-263b1da4dd89
feature: Multi-Currency
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# 概要 {#overview}

現在、[!DNL Marketo Measure] アプリケーションでは単一通貨（USD と想定）のみがサポートされていますが、世界中に顧客がいて、独自の企業通貨とユーザー通貨についてレポートする必要があることはわかっています。 この機能を使用すると、レポートされた費用や売上高を [!DNL Marketo Measure] で表示する際に、CRM で使用されているのと同じ通貨を切り替えることができます。

## 利用可能性 {#availability}

階層 2 以上。

## 要件 {#requirements}

[!DNL Marketo Measure] は顧客の CRM から通貨の設定を自動的に取り込みます。 CRM と一致するよ [!DNL Marketo Measure] に手動で設定する必要がなくなりました。 通貨設定は、「CRM」の「一般」ページにあります。

[!DNL Salesforce] では、顧客は「多通貨の有効化」を有効にする必要があります。 必要に応じて、顧客は「Yes, I want to enable Advanced Currency Management （はい、高度な通貨管理を有効にします）」を選択することもできます。

Dynamics では、顧客は、複数通貨の設定で静的為替レートを設定できます。 Dynamics には「高度な通貨管理」という概念はありません。

## 規約 {#terms}

| **期間** | 説明 |
|---|---|
| **高度な通貨** | お客様は高度な通貨管理と複数通貨を有効にしています。つまり、期間ごとに異なるコンバージョンレートを設定できます。 |
| **企業通貨** | これらは、CRM で組織によってリストおよび宣言される様々な通貨で、すべてコンバージョン率を持ちます。 [!DNL Marketo Measure] れらの値をインポートし、これらの通貨を製品内のユーザーが利用できるようにします。 |
| **通貨ロケール** | 会社情報ページで設定された、組織に使用される単一通貨。 |
| **現地通貨（またはユーザー通貨）** | ユーザープロファイル上の 1 人のユーザーに設定される通貨。ユーザーが各自の現地通貨で任意の金額を表示できるようになります。 ユーザーが現地通貨を選択するには、組織が通貨を宣言して設定する必要があります。 |
| **単一通貨** | CRM で多通貨を使用しないけれど、組織が異なる通貨で実行されているので、「通貨ロケール」を持つ顧客に使用します。 これは引き続き組織の単一通貨ですが、コンバージョンはありません。 |
| **単純な通貨** | 顧客は複数通貨を有効にしていますが、通貨ごとの静的コンバージョンレートがあります。 |
