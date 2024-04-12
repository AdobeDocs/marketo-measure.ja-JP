---
description: API 接続のベストプラクティス - [!DNL Marketo Measure]
title: API 接続のベストプラクティス
exl-id: b8550e4e-a567-427f-b5d3-50232553a066
feature: APIs, Integration
source-git-commit: 9e672d0c568ee0b889461bb8ba6fc6333edf31ce
workflow-type: ht
source-wordcount: '737'
ht-degree: 100%

---

# API 接続のベストプラクティス {#best-practices-for-api-connections}

## 概要 {#overview}

[!DNL Marketo Measure] では、[!DNL Google AdWords]、[!DNL Microsoft Bing Ads]、[!DNL Facebook Ads]、LinkedIn との API 接続を提供します。これらの API 接続により、[!DNL Marketo Measure] では広告プラットフォームから様々なデータを取り込み、Buyer Touchpoint データでレポートできます。 これらの API 接続の主な機能は、支出データを自動的に取り込む機能で、ROI レポート用にデータを手動でアップロードするのにかかる時間と労力を節約できます。これらの API 接続の設定は、[!DNL Marketo Measure] でこれらのチャネルを追跡するために必須ではありませんが、レポートを強化する貴重な詳細情報を提供します。

[!DNL Marketo Measure] API 接続は、アカウントの非常に貴重な側面であり、アドビのベストプラクティスのレコメンデーションは、お客様とお客様のチームがアドビの接続を最大限に活用するのに役立ちます。

## ベストプラクティス {#best-practice}

接続している広告プラットフォームに関係なく、次のガイドラインに留意することが重要です。

* 管理者を使用して接続します
* 1 つのプラットフォームに複数の広告アカウントを接続できます
* 可能なすべての広告アカウントを接続して、支出レポートを可能な限り自動化します
* 可能な場合は、常にトラッキングテンプレートを実装します。このテンプレートにより、広告アカウントを切断した場合でも、[!DNL Marketo Measure] ではきめ細かい広告の詳細を取り込むことができます。

各 [!DNL Marketo Measure] API を最適化するには、次のベストプラクティスを遵守してください。

**[!DNL Facebook]**：自動タグ付けを使用した接続

自動タグ付けを有効にする前に、広告履歴を CSV に書き出します。自動タグ付けを有効にすると、[!DNL Marketo Measure] によってタグ付けされたすべての広告のコンバージョン履歴と社会的証明がリセットされます。

ベストプラクティスのレコメンデーションに従うことで、[!DNL Marketo Measure] [!DNL Facebook] API では次の操作を実行できます。

* すべての [!DNL Facebook] Ads に必要な [!DNL Marketo Measure] パラメーター `_bf ={creative}` を自動タグ付けする
* すべてのアクティブな [!DNL Facebook] Ads にわたる広告コスト情報をダウンロードする

>[!NOTE]
>
>[!DNL Facebook] にはトラッキングテンプレートがありません。API は自動タグ付き（_bf）パラメーターに依存して広告の詳細を収集します。

**AdWords**：アカウントレベルでトラッキングテンプレートを実装し、自動タグ付けを有効にする

[!DNL Marketo Measure] では、アカウントレベル、キャンペーンレベルまたは広告グループレベルのトラッキングテンプレートを使用することをお勧めします。これにより、広告履歴の中断や削除のリスクなしに、すべての広告のパラメーターを追加および削除できます。

ベストプラクティスのレコメンデーションに従うことで、[!DNL Marketo Measure] AdWords API では次の操作を実行できます。

* すべての AdWords 広告に [!DNL Marketo Measure] パラメーターの `_bk={keyword}, _bt={creative}, _bm={matchtype}, _bn={network}, _bg={adgroupID}` を自動タグ付けする
* 有効なすべての AdWords 広告の広告費用情報をダウンロードする

**Bing**：アカウントレベルでトラッキングテンプレートを実装し、自動タグ付けを有効にする

他の API 接続とは異なり、[!DNL Bing] API 接続を設定する際に広告履歴が失われるリスクはありません。

ベストプラクティスのレコメンデーションに従うことで、[!DNL Marketo Measure] Bing API では次の操作を実行できます。
* `_bt={adid}, utm_medium=cpc, utm_source=bing, utm_term={keyword}` のパラメーターを使用して、すべての Bing Ads に自動タグ付けする
* すべてのアクティブな Bing Ads をまたいだ広告コスト情報をダウンロードする

**LinkedIn**：自動タグ付けを使用して接続

自動タグ付けを有効にすると、共有が再作成され、新しいクリエイティブに配置され、古いクリエイティブがアーカイブされます。

ベストプラクティスのレコメンデーションに従うことで、[!DNL Marketo Measure] LinkedIn API では次の操作を実行できます。

* 広告タイプがスポンサー付きコンテンツであるすべての LinkedIn 広告に、必要な [!DNL Marketo Measure] パラメーター _bl={creativeId} を自動タグ付けする。このパラメーターではクリエイティブ ID を取り込み、[!DNL Marketo Measure] でキャンペーンとクリエイティブ情報を解決できます。
* すべてのアクティブな、サポートされている [!DNL LinkedIn] 広告の広告コスト情報をダウンロードする

>[!NOTE]
>
>[!DNL LinkedIn] にはトラッキングテンプレートがありません。API は自動タグ付き（_bl）パラメーターに依存して、考えられるすべての広告の詳細を収集します。

## メンテナンスのベストプラクティス {#best-practice-for-maintenance}

アドビのベストプラクティスに従うことで、接続を切断した場合でもデータの損失を防ぐことができますが、定期的に（可能であれば毎月）接続を確認することをお勧めします。[!DNL Marketo Measure] アプリの「[!UICONTROL 接続]」セクションで、アカウントが切断されていることを示す赤いキーアイコンが表示されていないことを確認します。

API に接続されたアカウントを切断すると、[!DNL Marketo Measure] では支出データを取り込んだり、新しい広告にタグを付けたりすることができません。このため、可能であればトラッキングテンプレートを実装することを常にお勧めします。このテンプレートにより、広告アカウントを切断した場合でも、[!DNL Marketo Measure] では引き続き広告にタグを付け、きめ細かい広告の詳細を取り込むことができます。再接続すると、支出データがバックフィルされ、有料チャネルのレポートへの中断は最小限に抑えられます。

切断と再認証の理由には、次のものが含まれます。

* 接続されている個人取引先のパスワードの変更
* そのユーザが会社に存在していない
* API の更新

お客様のチームで上記のシナリオが発生した場合は、[!DNL Marketo Measure] アプリで API 接続を確認して、再認証する必要がないことを確認してください。

>[!MORELIKETHIS]
>
>* [統合された広告プラットフォーム（API）](/help/api-connections/utilizing-marketo-measures-api-connections/integrated-ad-platforms.md)
>* [入札管理ツールの  [!DNL Marketo Measure]](/help/api-connections/utilizing-marketo-measures-api-connections/how-bid-management-tools-affect-marketo-measure.md) への影響
>* [[!DNL Marketo Measure]  API パラメーターの説明](/help/api-connections/utilizing-marketo-measures-api-connections/marketo-measure-parameters.md)
>* [Facebook API の概要](/help/api-connections/utilizing-marketo-measures-api-connections/facebook-api.md)
>* [[!DNL LinkedIn]  統合の概要](/help/api-connections/utilizing-marketo-measures-api-connections/linkedin-integration.md)
>* [AdWords 統合の概要](/help/api-connections/utilizing-marketo-measures-api-connections/understanding-marketo-measure-adwords-tagging.md)
>* [接続された API アカウントの再認証](/help/api-connections/utilizing-marketo-measures-api-connections/reauthorizing-connected-accounts.md)
