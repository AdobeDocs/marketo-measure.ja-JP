---
unique-page-id: 18874572
description: 重複レコードおよび  [!DNL Marketo Measure] - [!DNL Marketo Measure]
title: 重複レコードと [!DNL Marketo Measure]
exl-id: e340100c-120a-4771-946d-336a1458da4e
feature: Tracking
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 12%

---

# 重複するレコードと [!DNL Marketo Measure] {#duplicate-records-and-marketo-measure}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Marketo Measure] では、CRM 内の関連するリードまたは連絡先とデータを照合する際に、メールアドレスを一意の識別子として使用します。 同じメールアドレス [!DNL Marketo Measure] 持つ複数のリードまたは連絡先が見つかった場合、すべてのレコードに同じデータが表示されます。 この影響は、[!DNL Marketo Measure] ーザーとのリードまたは連絡先についてレポートしている際に生じ、購入者タッチポイントを持つ一意のユーザーの数を誤って水増しする可能性があります。

[!DNL Marketo Measure] Reporting では、どのような表示になりますか？

_例レポート：購入者タッチポイントを持つ [!DNL Marketo Measure] 人物_

![](assets/1-1.png)

kelsey@adobe.comの [!DNL Marketo Measure] の人物 ID は、そのメールアドレスに存在するリードと連絡先の両方があることがわかります。 このレポートには、2 つのファーストタッチ、2 つのリード作成タッチ、および 2 つの PostLC インタラクションが報告されています。 これらの重複レコードは、タッチポイントの日付とタッチポイント情報を共有するため、同一人物であるにもかかわらず、2 人の人物が異なるという結論が出る可能性があります。

**推奨事項**

* レポートに対する収益を最大化するために、CRM 内で重複排除ツールを使用して、新しい一意のレコードのみを確実に作成することをお勧めします。 これは、マーケティング自動化ツールまたは CRM 内にインストールされた別のソフトウェアで行うことができます。 [!DNL Marketo Measure] は記録を自動的に重複排除することはなく、当社のソフトウェアを通じてこのサービスを提供しません。
* 重複を識別する際にレコードを手動で結合する方法もあります。 このプロセスには時間がかかり、面倒な場合がありますが、正確なレポートを出力するには、時間を投資する価値があります。
