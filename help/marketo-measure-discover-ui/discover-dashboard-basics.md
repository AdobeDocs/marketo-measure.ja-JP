---
description: ダッシュボードの基本を確認 –  [!DNL Marketo Measure]  – 製品
title: Discover ダッシュボードの基本
feature: Reporting
exl-id: 597a4f7c-4965-4bcb-bf28-607abc9b7545
source-git-commit: c6090ce0c3ac60cd68b1057c369ce0b3b20aeeee
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 2%

---


# Discover ダッシュボードの基本 {#discover-dashboard-basics}

この記事では、再設計されたインターフェイスの基本的な機能を説明し、データに簡単にアクセスして解釈できるようにします。 フィルターウィンドウのダイナミクスを掘り下げて、ドリル機能、クロスフィルタリング、ツールチップなど、強化されたレポート機能の複雑さを明らかにします。

## フィルターウィンドウ {#filter-pane}

すべてのダッシュボードには様々なフィルターがあり、シームレスなナビゲーションとカスタマイズを実現する次のコントロールが付属しています。

<table style="table-layout:auto">
 <tbody>
  <tr>
   <th>名前</th>
   <th>説明</th>
  </tr>
  <tr>
   <td><b>フィルター切り替えボタン</b></td>
   <td>フィルターウィンドウの表示/非表示を切り替えます。
   <p><img src="assets/discover-dashboard-basics-1.png"></td>
  </tr>
  <tr>
   <td><b>検索バー</b></td>
   <td>フィルターウィンドウの上部にある検索を使用して、特定のフィルターを検索します。 各フィルターには独自の検索バーもあります。
   <p><img src="assets/discover-dashboard-basics-2.png"></td>
  </tr>
   <tr>
   <td><b>フィルターボタンをクリア</b></td>
   <td>フィルターをクリアするには、各フィルターの右上隅にある消しゴム アイコンをクリックします。
   <p><img src="assets/discover-dashboard-basics-3.png"></td>
  </tr>
  <tr>
   <td><b>「適用」ボタン</b></td>
   <td>をクリックして、フィルターの変更を確認してダッシュボードに実装します。
   <p><img src="assets/discover-dashboard-basics-3a.png"></td>
  </tr>
 </tbody>
</table>

## ビジュアルに対するフィルター {#filters-on-visual}

ビジュアルの右上隅にマウスポインターを置くと、適用されたフィルターの読み取り専用リストが表示されます。

![&#x200B; 適用されたフィルターを視覚的にフィルター表示するツールヒント &#x200B;](assets/discover-dashboard-basics-3b.png)

## レポートの機能 {#report-capabilities}

### ドリルダウンおよびドリルアップ {#drill-down-and-up}

* ビジュアルの上にマウスポインターを置くと、階層が含まれているかどうかが示されます。アクションバーにドリルコントロールオプションが表示されている場合は、そのことが示されます。

![&#x200B; ビジュアル上にドリルコントロールを表示する Discover ダッシュボード &#x200B;](assets/discover-dashboard-basics-4.png)

* グレーの背景で強調表示されている下向き矢印をクリックして、ドリルダウンをアクティブにします。 元に戻すには、ドリルアップアイコンを使用します。

![&#x200B; グラフで単一レベルのドリルダウンがアクティブ化される &#x200B;](assets/discover-dashboard-basics-5.png)

一度に 1 つのフィールドをドリルダウンするには、ドリルダウン・アイコンをオンにして、バーなどの視覚要素を選択します。

![&#x200B; グラフで一度に 1 つのフィールドをドリルダウン &#x200B;](assets/discover-dashboard-basics-6.gif)

二重矢印ドリルダウンアイコンを使用して、次の階層レベルに進みます。

![&#x200B; 二重矢印ドリルダウンを使用して次の階層に移動 &#x200B;](assets/discover-dashboard-basics-7.gif)

現在のビューに階層レベルを追加するには、フォークのようなアイコンを使用します。

![&#x200B; 分岐アイコンを使用した階層レベルの追加 &#x200B;](assets/discover-dashboard-basics-8.gif)

### ドリルスルー {#drill-through}

ビジュアルの背後にあるデータを表示するには、ビジュアル要素を右クリックし、「ドリルスルー」オプションを選択します。

![&#x200B; ビジュアルの詳細データへの右クリック・ドリルスルー &#x200B;](assets/discover-dashboard-basics-9.gif)

### データの書き出し {#export-data}

ビジュアルから基になるデータを書き出すには、右上隅にカーソルを合わせます。 「その他のオプション」ボタンをクリックし、「データの書き出し」を選択し、好みの形式を選択してから「書き出し」をクリックします。
![&#x200B; ダッシュボードビジュアルからのデータのエクスポートメニュー &#x200B;](assets/discover-dashboard-basics-10.gif)

### フォーカスモード {#focus-mode}

特定のビジュアルまたはタイルをズームインするには、右上隅にカーソルを置いて「フォーカス」ボタンを選択します。

![&#x200B; ダッシュボードビジュアルのフォーカスモードへの切り替え &#x200B;](assets/discover-dashboard-basics-11.gif)

### クロスフィルター {#cross-filtering}

あるビジュアライゼーションで値または軸のラベルを選択すると、レポートページ上の他のビジュアライゼーションがクロスフィルターされ、関連するフィルター済みデータのみが表示されます。

![&#x200B; グラフの値を選択したクロスフィルタリングのビジュアル &#x200B;](assets/discover-dashboard-basics-12.gif)

### ツールチップ {#tooltips}

ツールチップには、表示されるデータに関する補足詳細が表示されます。 視覚的要素の上にマウスポインターを置くと、コンテキストツールチップがポップアップされ、その特定のデータポイントに関連するインサイトや説明が提供されます。

![&#x200B; ダッシュボードビジュアル上でコンテキストデータを表示するツールヒントにマウスポインターを置く &#x200B;](assets/discover-dashboard-basics-13.gif)
