---
unique-page-id: 18874652
description: 「[!DNL Marketo Measure] アトリビューションに関する FAQ - [!DNL Marketo Measure]」
title: 「[!DNL Marketo Measure] ビュースルーのアトリビューションに関するよくある質問」
exl-id: d20e88f3-3ff8-4381-a4b8-6862798caa74
feature: Attribution
source-git-commit: 48962b999fdd16fe96d18708ec301e64a39bc76e
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 25%

---

# [!DNL Marketo Measure] ビュースルーアトリビューションに関するよくある質問 {#marketo-measure-view-through-attribution-faq}

## ビュースルーアトリビューションとは {#what-is-view-through-attribution}

[!DNL Marketo Measure][!UICONTROL  ビュースルーアトリビューション ] 機能には、アトリビューションモデルに広告インプレッションを含める機能が含まれています。

>[!IMPORTANT]
>
>プライバシーに関する懸念により、サードパーティ Cookie は廃止されます。Google Chrome が 2024 年第 3 四半期に発表したサードパーティ Cookie の廃止は、事実上、この形式のトラッキングの終了を意味します。その結果、アドビでは、サードパーティ Cookie に依存する Marketo Measure 機能、特に、Google／DoubleClick インプレッション Cookie を使用するクロスドメイントラッキングとビュースルーアトリビューションを廃止します。Marketo Measure のその他の機能に影響はありません。また、ファーストパーティ cookie の使用にも影響はありません。Google のスケジュールを考慮すると、上記 2 つの機能の廃止予定日は 2024年6月1日（PT）です。この日付より前に収集された関連データは、アドビのお客様が引き続き使用できます。

## [!UICONTROL  ビュースルーアトリビューション ] が重要な理由 {#why-is-view-through-attribution-important}

これまでは、リターゲティングやインプレッション広告をマーケターがアトリビューション分析で考慮することは困難でした。 潜在的なクライアントは、時間が経つとリターゲティング広告にさらされる可能性がありますが、実際にこれらの広告の 1 つをクリックして、同じセッション内のフォームに入力する可能性は低いです。 アドビのビュースルーアトリビューションソリューションには、誰かがインプレッション広告にさらされたかどうかを追跡する機能が追加されました。 このタッチポイントは個々のレコードに追加され、見込み客がクライアントになるまで続行されます。 この情報により、マーケターは、リターゲティング広告のパフォーマンスに関するより良いインサイトを得ることができます。

## この設定には何が含まれますか？ {#what-is-involved-in-setting-this-up}

広告インプレッションの測定を開始 [!DNL Marketo Measure] るには、Doubleclick Campaign Manager にインプレッションタグを配置する必要があります。 タグが実装されると、インプレッション数がログに保存され、残りの処理を行います。 アトリビューションを通じたビューの測定に興味がある場合は、サクセスマネージャーにお問い合わせください。

## サポートされている広告プラットフォームを教えてください。 {#which-ad-platforms-are-supported}

現在、[!DNL Doubleclick] Campaign Manager をサポートしています。

## アトリビューションはどのように計算されますか？ {#how-is-the-attribution-calculated}

インプレッションデータとそのコンバージョンへの影響について、すべてのステージとマーケティングチャネルにわたって慎重に分析しました。 分布は、以下の表から分かるように、モデルによって異なります。

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
   <th>U 字型</th> 
   <th>W 字型</th> 
   <th>フルパス</th> 
   <th>カスタムモデル</th> 
  </tr> 
  <tr> 
   <td><strong>インプレッション</strong></td> 
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

## [!DNL Salesforce?] では、どのような表示になるか {#what-will-this-look-like-in-salesforce}

デ [!DNL Marketo Measure] スプレイ広告に公開されたリードに対して、単一のインプレッションタッチポイントを作成します。 ユーザーが最初に web サイト（FT）にアクセスしてフォーム（LC）に入力した後でも、ユーザーをマッピングできます。 タッチポイントには、広告キャンペーン名/ID、広告 ID、広告コンテンツ、サイト名/ID、プレースメント名/ID、マーケティングチャネル、地域、リファラーページなどの広告情報が含まれます。

ビュースルー属性モデルは、クライアントとそのデータに依存します。
