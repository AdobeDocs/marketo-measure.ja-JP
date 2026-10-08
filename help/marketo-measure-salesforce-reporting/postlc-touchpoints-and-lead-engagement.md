---
description: リードと連絡先に対してPostLC タッチポイントを作成し、更新および制限する方法について説明します
title: PostLC Touchpoints とリードエンゲージメント
exl-id: 3ee5c571-195e-46c7-b150-fedcbc3614cb
feature: Touchpoints
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: 32d2f1bc-61d0-598c-a8bf-f6fbc8920276
    internal-label: Touchpoints
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 4%
---
# PostLC Touchpoints とリードエンゲージメント {#postlc-touchpoints-and-lead-engagement}

[!DNL Marketo Measure]件のリード後の作成（PostLC）の顧客接点は、マルチタッチアトリビューションモデル（W-Shape以上）を使用しているお客様が利用できます。 リードまたはコンタクトがweb サイトに戻ってフォームに入力し続けると、これらのフォーム送信はPostLC タッチポイントとして登録されます。 これらのタッチポイントを利用すれば、どのようなコンテンツがリードをサイトに導き、最初のコンバージョンから長い間エンゲージメントし続けるのかを確認できます。 PostLCのタッチポイントは、商談のすべての中間接点とアトリビューションクレジットを共有します。10%のアトリビューションクレジットは、中間接点に割り当てられ、すべての顧客接点に均等に配分されます。

![Marketo Measure Post-Lead Creation （PostLC）のタッチポイントは、](assets/additional-functionality-1.png)を使用しているお客様が利用できます

[!DNL SFDC]に表示されるPostLC タッチポイントの数を調整できます。 通常は、最大5つのPostLC タッチポイントをプッシュすることをお勧めします。各タッチポイントは、[!DNL SFDC]で1 KBを占めます。

>[!NOTE]
>
>PostLC タッチポイントの設定を調整する方法については、この記事の最後を参照してください。

PostLCのタッチポイントは動的です。 リードまたは連絡先がPostLC フォームを送信し続けると、[!DNL Marketo Measure]はCRMのPostLC タッチポイントを更新して、最新のフォーム送信を表示します。 具体的には、5つのPostLC タッチポイントの制限を設定した場合、[!DNL Marketo Measure]は常に5つの&#x200B;_最新_ タッチポイントをCRMにプッシュします。  この例では、このアカウントはPostLC制限を4つのタッチポイントに設定しています。 このリードは、CRMに含めることができるPostLC タッチポイントの最大数に既に達しています。 最後のPostLC タッチは2018年2月6日でした。 このユーザーが次の日に別のフォームに入力する場合、[!DNL Marketo Measure]は2017年11月9日から最初のPostLC タッチポイントを削除し、2018年2月7日から最新のタッチポイントを追加します。

![PostLC タッチポイントは動的です。 リードまたは取引先責任者が引き続き送信する場合](assets/additional-functionality-2.png)

>[!NOTE]
>
>[!DNL Marketo Measure]は、リードまたは取引先責任者のPostLC タッチポイントのみを更新し、商談のPostLC アトリビューション タッチポイントは更新しません。 連絡先に関連するすべてのPostLC タッチポイントが商談に含まれます。

## PostLC タッチポイント設定の変更方法 {#how-to-change-postlc-touchpoint-settings}

リードまたは連絡先のPostLC タッチポイント設定を調整するには、次の手順に従います。

**リード**

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}で[!DNL Marketo Measure] アカウントにログインし、[!UICONTROL 設定]に移動します。

1. CRMで、「**[!UICONTROL リード]**」を選択します。

1. リードにプッシュするPostLC タッチポイントの数を入力し、**[!UICONTROL 保存]**&#x200B;をクリックします。

   ![1. &#x200B;](assets/additional-functionality-3.png)にプッシュするpostLC タッチポイントの数を入力します

**取引先責任者**

1. [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure?lang=ja){target="_blank"}で[!DNL Marketo Measure] アカウントにログインし、[!UICONTROL 設定]に移動します。

1. CRMで、「**[!UICONTROL 連絡先]**」を選択します。

1. 連絡先にプッシュするPostLC タッチポイントの数を入力し、**[!UICONTROL 保存]**&#x200B;をクリックします。

   ![1. &#x200B;](assets/additional-functionality-4.png)にプッシュするpostLC タッチポイントの数を入力します
