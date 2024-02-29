---
unique-page-id: 18874634
description: レポート内の重複レコード — [!DNL Marketo Measure]
title: マイレポートの重複レコード
exl-id: 4ee42371-5b67-4c69-9b49-3249f33614d0
feature: Reporting
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 10%

---

# マイレポートの重複レコード {#duplicate-records-in-my-report}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」と表示されるが、まだ「[!DNL Bizible]」と入力します。 アドビは現在、その更新を行っており、ブランディングの変更がまもなく CRM に反映される予定です。

次に進むと、 [!DNL Marketo Measure] のレポート [!DNL Salesforce]」と入力すると、レポート内で「重複した」レコードの検索が開始される場合があります。 この感覚は、レビューの際に感じるでしょう [!DNL Marketo Measure] 標準のレポートです。

Buyer Touchpoints オブジェクトや Buyer Attribution Touchpoint オブジェクトを使用してレポートを作成する場合、リード、連絡先、商談の数はレポートされなくなり、標準オブジェクト（リード、連絡先、商談）に関連する Buyer Touchpoints や Buyer Attribution Touchpoints の数がレポートされます。

次のレポートを例として見てみましょう。

これは、 **購入者タッチポイントを持つ連絡先** レポート。 つまり、個々の連絡先に関連付けられたタッチポイントの数を調べているということです。

![](assets/1.gif)

ご覧のように、レポートには 3 人の James Williams の連絡先が含まれているようで、「重複」と考えているかもしれません。

ただし、このレポートには、James に関連するタッチポイントの数が表示されます。 レポート内で、James には個別の FT（ファーストタッチ）、個別の LC、フォーム（リード作成タッチ）および PostLC タッチポイント（LC タッチポイントの後に実行されるフォーム送信）が含まれていることがわかります。

「連絡先の数」を理解するには、「カウント — ファーストタッチ」、「カウント — リード作成タッチ」または「カウント — U 字形」のフィールドを使用して、マーケティングインタラクションが発生した連絡先の数を把握します。

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] 大学：在庫 SFDC レポート](https://universityonline.marketo.com/courses/bizible-fundamentals-bizible-102/#/page/5c5cb68dfb384d0c9fb96cc4)
