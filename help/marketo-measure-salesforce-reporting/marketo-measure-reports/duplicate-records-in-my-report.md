---
unique-page-id: 18874634
description: マイレポートの重複レコード - [!DNL Marketo Measure]
title: マイレポートの重複レコード
exl-id: 4ee42371-5b67-4c69-9b49-3249f33614d0
feature: Reporting
source-git-commit: b84909fbb34a1d8f739ebeea3400ef8816e17d32
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 10%

---

# マイレポートの重複レコード {#duplicate-records-in-my-report}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRM には「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Salesforce] の [!DNL Marketo Measure] レポートに進むと、レポート内で「重複」レコードが見つかることがあります。 標準提供のレポートを確認すると、こ [!DNL Marketo Measure] ような感覚が生じる可能性があります。

バイヤータッチポイントオブジェクトまたはBuyer Attribution Touchpointオブジェクトを使用してレポートする場合、リード、連絡先、または商談の数をレポートするのではなく、これらの標準オブジェクト（リード、連絡先、商談）に関連付けられたバイヤータッチポイントまたはバイヤ属性タッチポイントの数をレポートすることを理解することが重要です。

例として、次のレポートを見てみましょう。

これは **購入者タッチポイント連絡先** レポートです。 これは、個々の連絡先に関連付けられたタッチポイントの数を調べていることを意味します。

![](assets/1.gif)

ご覧のように、レポートには James Williams の連絡先が 3 人いるように見えるため、「重複」と考えている可能性があります。

ただし、このレポートには、James に関連するタッチポイント数が表示されています。 レポート内で、James に個々の FT （ファーストタッチ）、個々の LC、フォーム（リード作成タッチ）、PostLC タッチポイント（LC タッチポイントの後に発生するフォーム送信）があることを確認できます。

「取引先責任者数」を把握したい場合は、「カウント – ファーストタッチ」、「カウントリード作成タッチ」、「カウント - U字型」のフィールドを使用して、マーケティングインタラクションを行った取引先責任者の数を把握できます。

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] Tutorials: SFDC レポートのストック ](https://experienceleague.adobe.com/ja/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-102/stock-salesforce-reports){target="_blank"}
