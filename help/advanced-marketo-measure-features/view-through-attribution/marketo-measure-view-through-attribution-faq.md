---
unique-page-id: 18874652
description: '[!DNL Marketo Measure] アトリビューションに関するFAQによる表示 –  [!DNL Marketo Measure]'
title: '[!DNL Marketo Measure] ビュースルーアトリビューションに関するよくある質問'
exl-id: d20e88f3-3ff8-4381-a4b8-6862798caa74
feature: Attribution
TQID: https://experienceleague.adobe.com/JL9J8c0qR5xOVFvzVaxrBKgBR0MO4WhcdUjQTX9Y2i0
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 33%

---

# [!DNL Marketo Measure] ビュースルーアトリビューションに関するよくある質問 {#marketo-measure-view-through-attribution-faq}

## View Through Attributionとは何ですか？ {#what-is-view-through-attribution}

[!DNL Marketo Measure] [!UICONTROL  ビュースルーアトリビューション ]機能には、アトリビューションモデルに広告インプレッションを含める機能が含まれています。

>[!IMPORTANT]
>
>プライバシーに関する懸念により、サードパーティ Cookie は廃止されます。 Google Chrome が 2024 年第 3 四半期に発表したサードパーティ Cookie の廃止は、事実上、この形式のトラッキングの終了を意味します。 その結果、アドビでは、サードパーティ Cookie に依存する Marketo Measure 機能、特に、Google／DoubleClick インプレッション Cookie を使用するクロスドメイントラッキングとビュースルーアトリビューションを廃止します。 Marketo Measure のその他の機能に影響はありません。 また、ファーストパーティ cookie の使用にも影響はありません。 Google のスケジュールを考慮すると、上記 2 つの機能の廃止予定日は 2024年6月1日（PT）です。 この日付より前に収集された関連データは、アドビのお客様が引き続き使用できます。

## [!UICONTROL  ビュースルー属性]が重要なのはなぜですか？ {#why-is-view-through-attribution-important}

従来、リターゲティングやインプレッション広告は、マーケターがアトリビューション分析で説明するのが困難でした。 潜在的な顧客は、何度もリターゲティング広告にさらされる可能性がありますが、実際にこれらの広告のいずれかをクリックして、同じセッションでフォームに入力する可能性は低くなります。 「View Through Attribution」ソリューションでは、誰かがインプレッション広告に接触したかどうかを追跡できるようになりました。 このタッチポイントは個人レコードに追加され、見込み客が顧客になるまで処理されます。 これにより、マーケターはリターゲティング広告のパフォーマンスについて、より優れたinsightを入手できるようになります。

## 設定には何が必要ですか？ {#what-is-involved-in-setting-this-up}

[!DNL Marketo Measure]が広告インプレッションの測定を開始するには、Doubleclick Campaign Managerにインプレッション タグを配置する必要があります。 タグが実装されると、インプレッションはログに保存され、残りは私たちが処理します。 アトリビューションによる顧客像の測定に関心がある場合は、サクセスマネージャーにお問い合わせください。

## サポートされている広告プラットフォーム？ {#which-ad-platforms-are-supported}

現在[!DNL Doubleclick] Campaign Managerをサポートしています。

## アトリビューションの計算方法？ {#how-is-the-attribution-calculated}

「インプレッションデータが、あらゆる段階やマーケティングチャネルを通じてコンバージョンに与える影響を慎重に分析しました。 分布はモデルによって異なります。下の表を参照してください。

<table> 
 <colgroup> 
  <col> 
  <col> 
  <col> 
  <col> 
  <col> 
  <col> 
  <col> 
 </colgroup> 
 <tbody> 
  <tr> 
   <th><br></th> 
   <th>ファーストタッチ</th> 
   <th>リード作成</th> 
   <th>U 字形</th> 
   <th>W 字型</th> 
   <th>フルパス</th> 
   <th>カスタムモデル</th> 
  </tr> 
  <tr> 
   <td><strong>印象</strong></td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>10%</td> 
   <td>10%</td> 
   <td>10%</td> 
   <td>カスタム</td> 
  </tr> 
  <tr> 
   <td><strong>FT</strong></td> 
   <td>100%</td> 
   <td>0%</td> 
   <td>35%</td> 
   <td>26.6%</td> 
   <td>20%</td> 
   <td>カスタム</td> 
  </tr> 
  <tr> 
   <td><strong>LC</strong></td> 
   <td>0%</td> 
   <td>100%</td> 
   <td>35%</td> 
   <td>26.6%</td> 
   <td>20%</td> 
   <td>カスタム</td> 
  </tr> 
  <tr> 
   <td><strong>OC</strong></td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>26.6%</td> 
   <td>20%</td> 
   <td>カスタム</td> 
  </tr> 
  <tr> 
   <td><strong>クローズ</strong></td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>20%</td> 
   <td>カスタム</td> 
  </tr> 
  <tr> 
   <td><strong>ミドルネーム</strong></td> 
   <td>0%</td> 
   <td>0%</td> 
   <td>20%</td> 
   <td>10%</td> 
   <td>10%</td> 
   <td>カスタム</td> 
  </tr> 
 </tbody> 
</table>

## [!DNL Salesforce?]でどう表示されるか {#what-will-this-look-like-in-salesforce}

[!DNL Marketo Measure]は、ディスプレイ広告に公開されたリードに対して、1つのインプレッション タッチポイントを作成します。 ユーザーが初めてweb サイト（FT）にアクセスし、フォーム（LC）に入力した後でも、ユーザーをマッピングできます。 タッチポイントには、広告キャンペーン名/ID、広告ID、広告コンテンツ、サイト名/ID、プレースメント名/ID、マーケティングチャネル、地域、リファラーページなどの広告情報が含まれます。

ビュースルーアトリビューションモデルは、クライアントとそのデータによって異なります。
