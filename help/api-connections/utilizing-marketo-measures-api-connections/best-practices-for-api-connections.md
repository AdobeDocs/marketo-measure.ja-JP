---
description: API 接続のベストプラクティス — [!DNL Marketo Measure]  — 製品ドキュメント
title: API 接続のベストプラクティス
exl-id: b8550e4e-a567-427f-b5d3-50232553a066
feature: APIs, Integration
source-git-commit: a2a7657e8377fd5c556d38f6eb815e39d2b8d15e
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 2%

---

# API 接続のベストプラクティス {#best-practices-for-api-connections}

## 概要 {#overview}

[!DNL Marketo Measure] は、との API 接続を提供します [!DNL Google AdWords], [!DNL Microsoft Bing Ads], [!DNL Facebook Ads]、およびLinkedIn これらの API 接続を使用すると、 [!DNL Marketo Measure] を使用して、広告プラットフォームから様々なデータを取り込み、購入者タッチポイントデータでレポートできます。 これらの API 接続の主な特長は、支出データを自動的に取り込む機能で、ROI レポートのデータを手動でアップロードするのに要する時間と労力を節約できる点です。 これらの API 接続の設定は、 [!DNL Marketo Measure] これらのチャネルを追跡するために役立ちますが、レポートを強化する貴重な詳細情報を提供します。

The [!DNL Marketo Measure] API 接続は、アカウントの非常に貴重な側面であり、アドビのベストプラクティスレコメンデーションは、お客様およびお客様のチームがアドビの接続を最大限に活用するのに役立ちます。

## ベストプラクティス {#best-practice}

接続する広告プラットフォームに関係なく、次のガイドラインに留意する必要があります。

* 管理者を使用した接続
* 1 つのプラットフォームに対して複数の広告アカウントを接続できます
* 可能な限り全ての広告アカウントを連携させて、支出のレポートを自動化します
* 可能な場合は、常にトラッキングテンプレートを実装します。 このテンプレートは、広告アカウントが切断された場合でも、確実に [!DNL Marketo Measure] は、引き続き詳細な広告の詳細を取り込むことができます

それぞれを最適化するには [!DNL Marketo Measure] API には、次のベストプラクティスを遵守してください。

**[!DNL Facebook]**：自動タグ付けを使用した接続

自動タグ付けを有効にする前に、広告履歴を csv に書き出します。 自動タグ付けを有効にすると、 [!DNL Marketo Measure].

ベストプラクティスの推奨事項に従うことで、 [!DNL Marketo Measure] [!DNL Facebook] API では、次のことが可能になります。

* すべて自動タグ付け [!DNL Facebook] 必要な広告 [!DNL Marketo Measure] パラメーター `_bf ={creative}`
* すべてのアクティブな広告コスト情報をダウンロード [!DNL Facebook] 広告

>[!NOTE]
>
>次のトラッキングテンプレートはありません： [!DNL Facebook]の場合、API は広告の詳細を収集するために、自動タグ付け (_bf) パラメーターに依存します。

**AdWords**：アカウントレベルでトラッキングテンプレートを実装し、自動タギングを有効にします。

[!DNL Marketo Measure] では、アカウントレベル、キャンペーンレベル、広告グループレベルのトラッキングテンプレートを使用することをお勧めします。広告履歴の中断や削除のリスクを伴わずに、すべての広告のパラメーターの追加と減算が可能になるからです。

ベストプラクティスの推奨事項に従うことで、 [!DNL Marketo Measure] AdWords API は次のことを可能にします。

* すべての AdWords 広告に [!DNL Marketo Measure] パラメーター `_bk={keyword}, _bt={creative}, _bm={matchtype}, _bn={network}, _bg={adgroupID}`
* すべてのアクティブな AdWords 広告にわたる広告コスト情報のダウンロード

**Bing**：アカウントレベルでトラッキングテンプレートを実装し、自動タギングを有効にします。

を設定する際に、広告履歴が失われるリスクはありません。 [!DNL Bing] 他の一部の API 接続とは異なり、API 接続です。

ベストプラクティスの推奨事項に従うことで、 [!DNL Marketo Measure] Bing API では、次のことが可能になります。
* 次のパラメーターを使用して、すべての Bing Ads に自動タグ付けする `_bt={adid}, utm_medium=cpc, utm_source=bing, utm_term={keyword}`
* すべてのアクティブな Bing 広告にわたる広告コスト情報のダウンロード

**LinkedIn**：自動タグ付けを使用した接続

自動タグ付けを有効にすると、共有が再作成され、新しいクリエイティブに配置されます。古いクリエイティブはアーカイブされます。

ベストプラクティスの推奨事項に従うことで、 [!DNL Marketo Measure] LinkedIn API では、次のことが可能になります。

* 必要に応じて、広告タイプがスポンサー付きコンテンツであるすべてのLinkedIn広告に自動タグ付けします [!DNL Marketo Measure] parameter_bl={creativeId}. このパラメーターはクリエイティブ ID を取り込み、 [!DNL Marketo Measure] をクリックして、キャンペーンとクリエイティブの情報を解決します。
* アクティブでサポートされているすべてのコスト情報をダウンロード [!DNL LinkedIn] 広告

>[!NOTE]
>
>次のトラッキングテンプレートはありません： [!DNL LinkedIn]の場合、API は自動タグ付け (_bl) パラメーターに基づいて、可能なすべての広告の詳細を収集します。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

アドビのベストプラクティスに従えば、接続が切断された場合にデータが失われるのを防ぐことができますが、接続を毎月、可能な限り定期的に確認することをお勧めします。 これは、 [!UICONTROL 接続] 」セクションに [!DNL Marketo Measure] アプリを使用して、赤いキーアイコンが存在しないことを確認し、接続解除されたアカウントを通知します。

API 接続アカウントが切断された場合、 [!DNL Marketo Measure] では、支出データを取り込んだり、新しい広告にタグを付けたりすることはできません。 可能な場合は、トラッキングテンプレートを常に実装することをお勧めするのは、そのためです。 このテンプレートは、広告アカウントが切断された場合でも、確実に [!DNL Marketo Measure] は、引き続き広告にタグを付け、詳細な広告の詳細を取り込むことができます。 再接続すると、支出データがバックフィルされ、有料チャネルレポートの中断が最小限に抑えられます。

切断と再認証の理由には次のものが含まれます。

* 接続している担当者アカウントに対するパスワードの変更
* その人はもう会社にいません
* API の更新

チームで上記のシナリオが発生した場合は、 [!DNL Marketo Measure] 再認証が必要ないことを確認するアプリケーションです。

>[!MORELIKETHIS]
>
>* [統合広告プラットフォーム (API)](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md)
>* [入札管理ツールの [!DNL Marketo Measure]](/help/api-connections/utilizing-marketo-measures-api-connections/how-bid-management-tools-affect-marketo-measure.md) への影響
>* [[!DNL Marketo Measure] API パラメーターの説明](/help/api-connections/utilizing-marketo-measures-api-connections/marketo-measure-parameters.md)
>* [Facebook API の概要](/help/api-connections/utilizing-marketo-measures-api-connections/facebook-api.md)
>* [[!DNL LinkedIn] 統合の概要](/help/api-connections/utilizing-marketo-measures-api-connections/linkedin-integration.md)
>* [AdWords 統合の概要](/help/api-connections/utilizing-marketo-measures-api-connections/understanding-marketo-measure-adwords-tagging.md)
>* [接続された API アカウントの再認証](/help/api-connections/utilizing-marketo-measures-api-connections/reauthorizing-connected-accounts.md)
