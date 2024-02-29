---
unique-page-id: 18874652
description: '"[!DNL Marketo Measure] ビュースルーアトリビューションに関する FAQ - [!DNL Marketo Measure]  — 製品ドキュメント»'
title: '"[!DNL Marketo Measure] ビュースルーアトリビューションに関する FAQ»'
exl-id: d20e88f3-3ff8-4381-a4b8-6862798caa74
feature: Attribution
source-git-commit: cc786cb3af08fa36af91ef22f4dba3072c9617eb
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 6%

---

# [!DNL Marketo Measure] ビュースルーアトリビューションに関するよくある質問 {#marketo-measure-view-through-attribution-faq}

## アトリビューション全体に対するビューとは {#what-is-view-through-attribution}

The [!DNL Marketo Measure] [!UICONTROL ビュースルーアトリビューション] 機能には、アトリビューションモデルに広告インプレッションを含める機能が含まれます。

## はなぜですか？ [!UICONTROL ビュースルーアトリビューション] 重要？ {#why-is-view-through-attribution-important}

従来、リターゲティングやインプレッション広告は、アトリビューション分析でマーケティング担当者が考慮するのが困難でした。 見込み客は、後からリターゲティング広告にさらされる場合がありますが、実際にこれらの広告の 1 つをクリックして、同じセッション内でフォームに入力することはほとんどありません。 アトリビューションを通じたビューソリューションでは、誰かがインプレッション広告に触れたかどうかをトレースできるようになりました。 このタッチポイントは、個々のレコードに追加され、見込み客がクライアントになるまで持ち越されます。 この情報を使用して、マーケターは、リターゲティング広告のパフォーマンスに関するより優れたインサイトを得ることができます。

## この設定には何が関係していますか？ {#what-is-involved-in-setting-this-up}

次の条件を満たすため [!DNL Marketo Measure] 広告インプレッションの測定を開始するには、Doubleclick Campaign Manager に配置する必要があるインプレッションタグがあります。 タグを実装すると、インプレッションがログに保存され、残りの処理はアドビがおこないます。 アトリビューションを通じたビューの測定に興味がある場合は、サクセスマネージャーにお問い合わせください。

## どの広告プラットフォームがサポートされていますか？ {#which-ad-platforms-are-supported}

現在、 [!DNL Doubleclick] キャンペーンマネージャー。

## アトリビューションはどのように計算されますか？ {#how-is-the-attribution-calculated}

インプレッションデータとそのコンバージョンに対する影響を、あらゆるステージおよびマーケティングチャネルにわたって慎重に分析しました。 以下の表に示すように、配分はモデルによって異なります。

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

## これはでどのように表示されますか？ [!DNL Salesforce?] {#what-will-this-look-like-in-salesforce}

[!DNL Marketo Measure] は、ディスプレイ広告に公開された任意のリードに単一のインプレッションタッチポイントを作成します。 最初に Web サイト (FT) にアクセスしてフォーム (LC) に入力した後でも、ユーザーをマッピングできます。 タッチポイントには、広告キャンペーン名/ID、広告 ID、広告コンテンツ、サイト名/ID、プレースメント名/ID、マーケティングチャネル、地域、リファラーページなどの広告情報が含まれます。

ビュースルーアトリビューションモデルは、クライアントとそのデータに依存します。
