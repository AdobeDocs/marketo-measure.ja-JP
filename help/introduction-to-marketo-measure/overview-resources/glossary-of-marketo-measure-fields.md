---
unique-page-id: 18874586
description: Marketo Measure フィールドの用語集 - Marketo Measure - 製品ドキュメント
title: Marketo Measure フィールドの用語集
exl-id: 8e23b102-6d4f-4919-b361-04d1b184e710
feature: Fundamentals
source-git-commit: 8ac315e7c4110d14811e77ef0586bd663ea1f8ab
workflow-type: tm+mt
source-wordcount: '3211'
ht-degree: 100%

---

# Marketo Measure フィールドの用語集 {#glossary-of-marketo-measure-fields}

この記事では、Marketo Measure 基本パッケージから Salesforce に追加されたすべての Marketo Measure フィールドの用語集について説明します。また、フィールドが見つけることができるオブジェクトや各フィールドにどのように情報が入力されるかに関する情報が掲載されています。

各 Marketo Measure フィールドがどのオブジェクトに関連しているかを示すマップについては、[こちらを参照](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-object-and-field-taxonomy.md)してください。

[A](#a) · [B](#b) · [C](#c) · [D](#d) · [E](#e) · [F](#f) · [G](#g) · H · I · J · [K](#k) · [L](#l) · [M](#m) · N · [O](#o) · [P](#p) · Q · [R](#r) · [S](#s) · [T](#t) · [U](#u) · [V](#v) · W · X · Y · Z

## A {#a}

**アカウント** | Buyer Attribution Touchpoint で見られる

このフィールドには、BAT に関連付けられたアカウント名が入力されます。

**広告キャンペーン ID** | Buyer Touchpoint、Buyer Attribution Touchpoint で見られる

このフィールドには 3 つの方法で入力できます。

`1)` タッチポイントが有料検索（AdWords または Bing Ads のどちらか）に起因する場合、広告プラットフォームの広告キャンペーン ID がここに表示されます。

`2)` タッチポイントが有料検索に起因しない場合、このフィールドは、ランディングページ URL の utm_campaign 値を使用して入力されます。

例：`http://info.marketomeasure.com/adwords-for-lead-generation?utm_source=Event&utm_medium=booth&utm_campaign=Marketo%20Virtual%20Event%20sep2014`

この例では、広告キャンペーン ID は、次のように表示されます。__GAId__ Marketing Virtual Event sept2014

`3)` タッチポイントがオフライン Salesforce キャンペーン（会議、ディナーなど）に起因する場合、広告キャンペーン ID には、Salesforce キャンペーン ID が表示されます

上記のいずれも該当しない場合、このフィールドは空になります。

**広告キャンペーン名** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索（AdWords／Bing Ads）に起因する場合、広告プラットフォームの広告キャンペーン名がここに表示されます。

`2)` タッチポイントが有料検索に起因せず、ランディングページ URL に utm_campaign の値が含まれている場合、その値がここに入力されます。

`3)` タッチポイントが Salesforce キャンペーンに起因する場合、Salesforce キャンペーンの名前がここに表示されます。

`4)` これには、Marketo Measure アカウント内で作成したアクティビティから生成される Touchpoints 用に定義されたキャンペーン名が入力されます。

上記のいずれも該当しない場合、このフィールドは空になります。

**広告キャンペーン名（FT）**| Buyer Touchpoint

このフィールドには、広告キャンペーン名と同じように入力されます。ただし、このフィールドは、特に、ファーストタッチタッチポイントを生成した広告キャンペーンの名前を表示します。

**広告キャンペーン名（LC）**| Buyer Touchpoint

このフィールドには、広告キャンペーン名と同じように入力されます。ただし、このフィールドは、特に、リード作成タッチポイントを生成した広告キャンペーンの名前を表示します。

**広告コンテンツ** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索（AdWords／Bing Ads）に起因する場合、フィールドには、広告プラットフォームからの完全な広告コピーが表示されます。

`2)` タッチポイントが有料検索に起因しない場合、このフィールドには、ランディングページ URL の utm_content 値が表示されます。

`3)` これには、Touchpoint を生成した関連するアクティビティからの件名の値が入力されます。

上記のいずれも該当しない場合、このフィールドは空になります。

**広告のリンク先 URL** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、このフィールドには、検索エンジンから広告をクリックした後に転送される URL の宛先が表示されます。

タッチポイントが有料検索に起因しない場合、フィールドは空になります。

**広告グループ ID** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、AdWords／Bing Ads からの広告グループ ID がここに表示されます。

タッチポイントが有料検索に起因しない場合、フィールドは空になります。

**広告グループ名** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、AdWords／Bing Ads からの広告グループ名がここに表示されます。

タッチポイントが有料検索に起因しない場合、フィールドは空になります。

**広告 ID** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、AdWords／Bing Ads からの広告 ID がここに表示されます。

`2)` Touchpoint が CRM アクティビティから生成される場合、これには、アクティビティの外部 ID が入力されます。

タッチポイントが有料検索に起因しない場合、フィールドは空になります。

**アトリビューション % カスタムモデル** | Buyer Attribution Touchpoint

カスタムアトリビューションモデルを使用している場合、このフィールドには、カスタムモデルに設定された値に応じた、タッチポイントに起因する収益の割合が表示されます。

カスタムモデルを使用していない場合、このフィールドは空になります。

**アトリビューション % ファーストタッチ** | Buyer Attribution Touchpoint

このフィールドには、ファーストタッチモデルに応じた、タッチポイントに起因する収益の割合が表示されます。

**アトリビューション % フル** | Buyer Attribution Touchpoint

このフィールドには、フルパスモデルに応じた、タッチポイントに起因する収益の割合が表示されます。

**アトリビューション % リード作成** | Buyer Attribution Touchpoint

このフィールドには、リード作成モデルに応じた、タッチポイントに起因する収益の割合が表示されます。

**アトリビューション % U 字型** | Buyer Attribution Touchpoint

このフィールドには、U 字型モデルに応じた、タッチポイントに起因する収益の割合が表示されます。

**アトリビューション % W 字型** | Buyer Attribution Touchpoint

このフィールドには、W 字型モデルに応じた、タッチポイントに起因する収益の割合が表示されます。

[ページの先頭に戻るには、こちらをクリック](#top)

## B {#b}

**Marketo Measure 商談額** | Salesforce 商談

商談の収益をレポートするためにカスタム金額フィールドを使用している場合、Marketo Measure では、これらのカスタム金額フィールドを読み取ることができません。Marketo Measure 商談額は、Marketo Measure で商談のカスタム金額フィールドを読み取ることを可能にするワークフローを作成するために使用される、非表示のフィールドです。

**ブラウザー** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web セッション中に使用された web ブラウザーのタイプが表示されます（Chrome、Safari、Firefox など）。

[ページの先頭に戻るには、こちらをクリック](#top)

## C {#c}

**連絡先** | Buyer Touchpoint、Buyer Attribution Touchpoint

フィールドには、タッチポイントが属する連絡先が表示されます。

**カウント - カスタムモデル** | Buyer Attribution Touchpoint

カスタムアトリビューションモデルを使用している場合、このフィールドには、カスタムモデルに設定された値に従ってタッチポイントに付与された、収益クレジットの割合が表示されます（10 進数形式）。

カスタムモデルを使用していない場合、このフィールドは空になります。

**カウント - カスタムモデル** | Buyer Touchpoint

カスタムアトリビューションモデルを使用している場合、このフィールドには、カスタムモデルに設定された値に従ってタッチポイントに付与された、アトリビューションクレジットの割合が表示されます（10 進数形式）。このフィールドは、Buyer Touchpoint オブジェクトに関連するので、収益クレジットの反映ではなく、単にアトリビューションクレジットのみの反映です。

カスタムモデルを使用していない場合、このフィールドは空になります。

**カウント - ファーストタッチ** | Buyer Attribution Touchpoint

このフィールドには、ファーストタッチモデルに従ってタッチポイントに付与された、収益クレジットの割合が表示されます（10 進数形式）。

**カウント - ファーストタッチ** | Buyer Touchpoint

このフィールドには、ファーストタッチモデルに従ってタッチポイントに付与された、アトリビューションクレジットの割合が表示されます（10 進数形式）。タッチポイントがファーストタッチの場合、このフィールドは、常に 1.0 になります（100％アトリビューションクレジットを含む）。タッチポイントがファーストタッチでない場合、このフィールドは、常に 0 になります（0％アトリビューションクレジットを含む）。

このフィールドは、Buyer Touchpoint オブジェクトに関連するので、収益クレジットの反映ではなく、単にアトリビューションクレジットのみの反映です。

**カウント - フルパス** | Buyer Attribution Touchpoint

このフィールドには、フルパスモデルに従ってタッチポイントに付与された、収益の割合が表示されます（10 進数形式）。

**カウント - リード作成タッチ** | Buyer Attribution Touchpoint

このフィールドには、リード作成モデルに従ってタッチポイントに付与された、収益クレジットの割合が表示されます（10 進数形式）。

**カウント - リード作成タッチ** | Buyer Touchpoint

このフィールドには、リード作成モデルに従ってタッチポイントに付与された、アトリビューションクレジットの割合が表示されます（10 進数形式）。タッチポイントがリード作成タッチの場合、このフィールドは、常に 1.0 になります（100％アトリビューションクレジットを含む）。タッチポイントがリード作成タッチでない場合、このフィールドは、常に 0 になります（0％アトリビューションクレジットを含む）。

このフィールドは、Buyer Touchpoint オブジェクトに関連するので、収益クレジットの反映ではなく、単にアトリビューションクレジットのみの反映です。

**カウント - U 字型** | Buyer Attribution Touchpoint

このフィールドには、U 字型モデルに従ってタッチポイントに付与された、収益クレジットの割合が表示されます（10 進数形式）。

**カウント - U 字型** | Buyer Touchpoint

このフィールドには、U 字型モデルに従ってタッチポイントに付与された、アトリビューションクレジットの割合が表示されます（10 進数形式）。U 字型モデルでは、クレジットは、ファーストタッチ、リード作成タッチおよびファーストタッチからリード作成タッチの間で発生した任意の中間フォーム申請の間で分割されます。

このフィールドは、Buyer Touchpoint オブジェクトに関連するので、収益クレジットの反映ではなく、単にアトリビューションクレジットのみの反映です。

**カウント - W 字型** | Buyer Attribution Touchpoint

このフィールドには、W 字型モデルに従ってタッチポイントに付与された、クレジットの割合が表示されます（10 進数形式）。

[ページの先頭に戻るには、こちらをクリック](#top)

## D {#d}

レポートされた日付 | Marketo Measure ABTest、Marketo Measure イベント

Marketo Measure イベント - ユーザーが web サイトで特定のアクションを起こして、イベントをアクティブ化した日付

Marketo Measure ABTest - ユーザーが web サイト上の A/B テストに参加した日付

[ページの先頭に戻るには、こちらをクリック](#top)

## E {#e}

**イベント名** | Marketo Measure イベント

このフィールドには、イベントをトリガーしたアクションの名前が表示されます（例：ページビュー）。

**イベント値** | Marketo Measure イベント

イベントの説明（例：ホームページ）

**実験名** | Marketo Measure ABTest

このフィールドには、実験の名前が表示されます（例：Trial Button）

**実験 ID** |Marketo Measure AB テスト

各実験の一意の ID コード

[ページの先頭に戻るには、こちらをクリック](#top)

## F {#f}

フォーム URL | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、フォーム入力が発生したページの URL の短縮バージョンが表示されます（UTM パラメーターなし）

フォーム URL - 未加工 | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、フォーム入力が発生したページ URL 全体が表示されます（UTM パラメーターを含む）

[ページの先頭に戻るには、こちらをクリック](#top)

## G {#g}

ジオ市区町村 | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web サイトを訪問したリード／連絡先の市区町村の名前が表示されます。これは、逆引き IP 参照によって行われます。

ジオ国 | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web サイトを訪問したリード／連絡先の国が表示されます。これは、逆引き IP 参照によって行われます。

ジオ地域 | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web サイトを訪問したリード／連絡先の地域または都道府県が表示されます。これは、逆引き IP 参照によって行われます。

[ページの先頭に戻るには、こちらをクリック](#top)

## K {#k}

**キーワード ID** | Buyer Touchpoint、Buyer Attribution Touchpoint

タッチポイントが有料検索に起因する場合、このフィールドには、広告プラットフォーム（Adwords／Bing Ads）からのキーワード ID が表示されます。

このタッチポイントが有料検索に起因しない場合、このフィールドは空になります。

**キーワード一致タイプ** | Buyer Touchpoint、Buyer Attribution Touchpoint

タッチポイントが有料検索に起因する場合、このフィールドには、広告プラットフォーム（Adwords／Bing）からの一致タイプが表示されます。

**キーワードテキスト** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、このフィールドには、広告プラットフォーム（Adwords／Bing Ads）からのキーワードテキストまたはランディングページ URL の _bk パラメーターからの値が表示されます。

例：`http://info.marketomeasure.com/intro-guide-b2b-marketing-attribution?_bt=12345678&_bk=marketing%20attribution&_bm=p&gclid=ABc123def456ghi789jkl`

`2)` タッチポイントが有料検索に起因しない場合、このフィールドには、ランディングページ URL からの utm_term 値が表示されます。

`http://www.marketomeasure.com/blog/lead-generation?utm_source=linkedin&utm_medium=Social&utm_campaign=ABC%20Blog&utm_content=Lead%20Gen&utm_term=lead%20gen`.

タッチポイントが有料検索に起因しない場合、または no utm_term 値がない場合、このフィールドは空になります。

[ページの先頭に戻るには、こちらをクリック](#top)

## L {#l}

**ランディングページ** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web セッション中に訪問された最初の web ページの URL の短縮バージョンが表示されます（UTM パラメーターなし）。

**ランディングページ - 未加工** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、web セッション中に訪問された最初の web ページの URL 全体が表示されます（UTM パラメーターを含む）。

**リード** | Buyer Touchpoint、Marketo Measure 顧客

このフィールドには、タッチポイントが属するリードの名前が表示されます。

[ページの先頭に戻るには、こちらをクリック](#top)

## M {#m}

**マーケティングチャネル** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、タッチポイントが属するマーケティングアクティビティまたはマーケティングチャネルの一般グループが表示されます（例：有料検索、直接、ソーシャルなど）。タッチポイントは、Marketo Measure アプリでのチャネルの設定方法に応じてグループ化されます。マーケティングチャネルついて、またはチャネルの設定方法について詳しくは、[こちらを参照](/help/channel-tracking-and-setup/online-channels/online-custom-channel-setup.md)してください。

**マーケティングチャネル - パス** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、マーケティングチャネルおよびタッチポイントが属するサブチャネルが表示されます。以下の例では、マーケティングチャネル - パスは、Social.Linkedin です（つまり、マーケティングチャネルが Social で、サブチャネルが LinkedIn）。

![](assets/1-3.png)

**メディア** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、Adwords／Bing Ads からのメディアがここに表示されます（例：CPC）。

`2)` タッチポイントが有料検索に起因しない場合、このフィールドには、ランディングページ URL からの utm_medium 値が表示されます。

`3)` タッチポイントがオフラインキャンペーンに起因する場合、このフィールドには、Salesforce キャンペーンの「タイプ」フィールドが表示されます。

`4)` これには、Touchpoint を生成した関連するアクティビティからのアクティビティタイプの値が入力されます。

上記のいずれも該当しない場合は、Marketo Measure によってメディア値が自動的に設定されます。

[ページの先頭に戻るには、こちらをクリック](#top)

O

**商談** | Buyer Attribution Touchpoint

このフィールドには、BAT が属する商談が表示されます。

[ページの先頭に戻るには、こちらをクリック](#top)

P

**プラットフォーム** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、コンピューターまたは電話のタイプおよび web セッション中に使用されたオペレーティングシステムのタイプが表示されます。

[ページの先頭に戻るには、こちらをクリック](#top)

R

**参照元ページ** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、お客様の web サイトに転送されたリード／連絡先が最後にいた web ページの URL（UTM パラメーターなし）が表示されます。

例：

- タッチポイントが有料／オーガニック検索に起因する場合、フィールドには、検索エンジンの URL が表示されます

- タッチポイントがソーシャルに起因する場合、フィールドには、ソーシャル web サイトの URL が表示されます（例：LinkedIn）

**参照元ページ - 未加工** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、参照 URL 全体が表示されることを除いて、参照元ページと同じ情報が表示されます（UTM パラメーターを含む）。

**収益 - カスタムモデル** | Buyer Attribution Touchpoint

カスタムアトリビューションモデルを使用している場合、このフィールドには、カスタムモデルに設定されたアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

カスタムモデルを使用していない場合、ドルの金額は 0 になります。

**収益 - ファーストタッチ** | Buyer Attribution Touchpoint

このフィールドには、ファーストタッチモデルでのアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

**収益 - フルパス** | Buyer Attribution Touchpoint

このフィールドには、フルパスモデルでのアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

**収益 - リード作成タッチ** | Buyer Attribution Touchpoint

このフィールドには、リード作成モデルでのアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

**収益 - U 字型** | Buyer Attribution Touchpoint

このフィールドには、U 字型モデルでのアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

**収益 - W 字型** | Buyer Attribution Touchpoint

このフィールドには、W 字型モデルでのアトリビューションの割合に応じた、タッチポイントに起因する収益額（ドル）が表示されます。

[ページの先頭に戻るには、こちらをクリック](#top)

S

**Salesforce キャンペーン** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、タッチポイントが属する Salesforce キャンペーンが表示されます。

**検索語句** | Buyer Touchpoint、Buyer Attribution Touchpoint

タッチポイントが有料またはオーガニック検索に起因する場合、このフィールドには、検索エンジンに入力された検索語句が表示されます。ただし、プライバシー上の理由により、この情報は、通常、使用できません。

**セグメント** | Buyer Attribution Touchpoint

このフィールドには、タッチポイントが属するセグメントが表示されます。これは、Marketo Measure アプリでセグメンテーションルールをどのように設定したかによって異なります。

[ページの先頭に戻るには、こちらをクリック](#top)

T

**Touchpoint 日** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントがオンラインソースに起因する場合、このフィールドには、タッチポイントが発生した日時が表示されます。

`2)` タッチポイントがオフラインイベントに起因する場合、このフィールドには、Salesforce キャンペーンで設定された日時またはキャンペーン同期ルールで選択された日付フィールドからの日時が表示されます。

`3)` タッチポイントがアクティビティに起因する場合、このフィールドには、アクティビティルールで Touchpoint 日として選択されたフィールドの日時が表示されます。

**Touchpoint 日（FT）**| Buyer Touchpoint

このフィールドは、Touchpoint 日と同じですが、特に、ファーストタッチタッチポイントが発生した日時が表示されます。

**Touchpoint 日（LC）**| Buyer Touchpoint

このフィールドは、Touchpoint 日と同じですが、特に、リード作成タッチポイントが発生した日時が表示されます。

**Touchpoint の位置** | Buyer Touchpoint、Buyer Attribution Touchpoint

このフィールドには、タッチポイントの位置が表示されます。タッチポイントの位置は、カスタマージャーニーの主要なマイルストーンタッチポイントを反映します（例：FT、フォーム、LC、OC、クローズ）。タッチポイントの位置は、カスタマージャーニーのどのタイミングで発生したかによって異なり、単一のタッチポイントは、複数の位置を持つことがあります。タッチポイントの位置の違いを次に示します。

ファーストタッチ（FT）- ブランドに対して誰かが行う最初のマーケティングインタラクション

リード作成（LC）- 最初の既知のマーケティングインタラクション（通常、フォーム申請または Salesforce キャンペーンを含める）

フォーム - 訪問者がオンラインフォームに記入するとき

商談作成（OC）- 商談が作成されたときに最も近いマーケティングインタラクション

クローズ - 商談がクローズ（獲得または損失）したときに最も近いマーケティングインタラクション

**Touchpoint ソース** | Buyer Touchpoint、Buyer Attribution Touchpoint

`1)` タッチポイントが有料検索に起因する場合、このフィールドには、広告プラットフォームの名前（AdWords／BingAds）が表示されます

`2)` タッチポイントがオーガニック検索に起因する場合、このフィールドには、検索エンジンの名前が表示されます

`3)` #1 や #2 に該当せず、utm_source 値がタッチポイントのランディングページ URL に存在する場合、その値がここに表示されます

`4)` Touchpoint が CRM キャンペーンから生成される場合、これは、CRM キャンペーンとして入力されます。

`5)` Touchpoint が CRM アクティビティから生成される場合、これは、CRM アクティビティとして入力されます。

上記のいずれも該当しない場合は、このフィールドは、「Web Direct」または「Web」として入力されます。

**Touchpoint ソース（FT）**| Buyer Touchpoint

このフィールドは、Touchpoint ソースと同じですが、特に、ファーストタッチタッチポイントのソースが表示されます。

**Touchpoint ソース（LC）**| Buyer Touchpoint

このフィールドは、Touchpoint ソースと同じですが、特に、リード作成タッチポイントのソースが表示されます。

**タッチポイントのタイプ** | Buyer Touchpoint および Buyer Attribution Touchpoint で見られる。

このフィールドには、Touchpoint のインタラクションのタイプが表示されます。JavaScript タッチポイントの場合、web 訪問、web フォームまたは web チャットとして表示されます。CRM キャンペーンタッチポイントタッチポイント、CRM として表示されます。Activity Touchpoints のタスクまたはイベントタイプが入力されます。

[ページの先頭に戻るには、こちらをクリック](#top)

U

**UniqueId** | Buyer Touchpoint、Buyer Attribution Touchpoint

各タッチポイントに関連付けられた一意の ID

**ユーザー ID** | Marketo Measure ABTest

各用途に対する Optimizely の一意の ID コード

[ページの先頭に戻るには、こちらをクリック](#top)

## V {#v}

**バリエーション** | Marketo Measure ABTest

A/B テストのバリエーションの名前

**バリエーション ID** | Marketo Measure ABTest

各 A/B テストバリエーションの一意の ID コード。

[ページの先頭に戻るには、こちらをクリック](#top)
