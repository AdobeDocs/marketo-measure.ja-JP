---
description: Marketo Measure ユーザー向けマイレポートガイダンスの重複レコード
title: マイレポートの重複レコード
exl-id: 4ee42371-5b67-4c69-9b49-3249f33614d0
feature: Reporting
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 9%

---

# マイレポートの重複レコード {#duplicate-records-in-my-report}

>[!NOTE]
>
>ドキュメントに「[!DNL Marketo Measure]」を指定する手順が表示される場合がありますが、CRM には「[!DNL Bizible]」が表示されます。 アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

[!DNL Marketo Measure] の [!DNL Salesforce] レポートに進むと、レポート内で「重複」レコードが見つかることがあります。 標準提供のレポートを確認すると、こ [!DNL Marketo Measure] ような感覚が生じる可能性があります。

バイヤータッチポイントオブジェクトまたはBuyer Attribution Touchpointオブジェクトを使用してレポートする場合、リード、連絡先、または商談の数をレポートするのではなく、これらの標準オブジェクト（リード、連絡先、商談）に関連付けられたバイヤータッチポイントまたはバイヤ属性タッチポイントの数をレポートすることを理解することが重要です。

例として、次のレポートを見てみましょう。

これは **購入者タッチポイント連絡先** レポートです。 これは、個々の連絡先に関連付けられたタッチポイントの数を調べていることを意味します。

![ これは、購入者タッチポイント連絡先レポートです。 繰り返しますが、これは ](assets/marketo-reports-1.gif) のことを意味します。

ご覧のように、レポートには James Williams の連絡先が 3 人いるように見えるため、「重複」と考えている可能性があります。

ただし、このレポートには、James に関連するタッチポイント数が表示されています。 レポート内で、James に個々の FT （ファーストタッチ）、個々の LC、フォーム（リード作成タッチ）、PostLC タッチポイント（LC タッチポイントの後に発生するフォーム送信）があることを確認できます。

「取引先責任者数」を把握したい場合は、「カウント – ファーストタッチ」、「カウントリード作成タッチ」、「カウント - U字型」のフィールドを使用して、マーケティングインタラクションを行った取引先責任者の数を把握できます。

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure]  チュートリアル：Stock SFDC レポート ](https://experienceleague.adobe.com/en/docs/marketo-measure-learn/tutorials/onboarding/marketo-measure-102/stock-salesforce-reports){target="_blank"}
