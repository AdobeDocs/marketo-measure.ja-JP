---
unique-page-id: 18874572
description: レコードの複製および [!DNL Marketo Measure] - [!DNL Marketo Measure]
title: 重複レコードと [!DNL Marketo Measure]
exl-id: e340100c-120a-4771-946d-336a1458da4e
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 7%

---

# レコードの複製および [!DNL Marketo Measure] {#duplicate-records-and-marketo-measure}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」 （ドキュメント内）が表示されますが、CRM には「Bizible」が表示されます。 アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

[!DNL Marketo Measure] は、CRM で関連するリードまたは連絡先とデータを照合する際に、電子メールアドレスを一意の識別子として使用します。 条件 [!DNL Marketo Measure] は、同じメールアドレスを持つ複数のリードまたは連絡先を検索します。すべてのレコードで同じデータが表示されます。 この影響は、次のアイテムを持つリードまたは連絡先のレポートを作成する際に発生します： [!DNL Marketo Measure] とは、購入者タッチポイントを持つ個別訪問者の数を誤って水増しする可能性があります。

これはでどのように表示されますか。 [!DNL Marketo Measure] 報告？

_サンプルレポート： [!DNL Marketo Measure] 購入者タッチポイントを持つ担当者。_

![](assets/1-1.png)

を参照してください。 [!DNL Marketo Measure] kelsey@adobe.comの担当者 ID。この電子メールアドレスにはリードと連絡先の両方が存在します。 このレポートでは、最初のタッチが 2 回、リード作成タッチが 2 回、PostLC インタラクションが 2 回レポートされます。 これらの重複レコードは、タッチポイントの日付とタッチポイントの情報を共有し、同じ人物であるにもかかわらず、2 人が異なる人物であると結論付ける可能性があります。

**推奨**

* レポートでの再来訪を最大化するには、CRM 内の重複排除ツールを使用して、新しい一意のレコードのみを確実に作成することをお勧めします。 これは、マーケティングオートメーションツールまたは CRM 内にインストールされた別のソフトウェアを使用して実行できます。 [!DNL Marketo Measure] は自動的にデデュープレコードを実行せず、アドビのソフトウェアを通じてこのサービスを提供しません。
* 重複を識別する際に、レコードを手動で結合する方法もあります。 このプロセスには時間がかかり、面倒な作業が必要になる場合がありますが、正確なレポート作成の結果は、時間に対する投資に値します。
