---
description: Marketo Measure ユーザー向けにJavaScript ガイダンスで収集されたデータ
title: JavaScript で収集されるデータ
feature: Tracking
exl-id: 83814168-9d3e-45ac-b514-df58f0b2e90b
hidefromtoc: 'yes'
product_v2:
  - id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
    internal-label: Marketo Measure
feature_v2:
  - id: dcbeff6e-0253-5a4b-9ac2-1b67cc4a6286
    internal-label: Tracking
source-git-commit: 940fee4abd0e09b6bf513b5e7526d3c242bd31c7
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 77%
---
# JavaScript で収集されるデータ {#data-collected-by-javascript}

デプロイメント時に Marketo Measure JavaScript で収集されるデータについて説明します。

**サンプルリクエスト：**

```text
https://cdn.bizible.com/m/ipv?_biz_r=https%3A%2F%2Fwww.google.com%2F&_biz_h=-1801745101&_biz_u=7059e81415f34f7bbaf40fe32fdcba21&_biz_s=8cbeed&_biz_l=https%3A%2F%2Fwww.zendesk.com%2Fservice%2F&_biz_t=1676483822155&_biz_i=Customer%20service%20software%20for%20the%20best%20customer%20experiences%20%7C%20Zendesk&_biz_n=0&rnd=235938&cdn_o=a&_biz_z=1676483822155
```

<br>

Marketo Measure では、すべてのタイプのリクエストについて次の一般的なデータを収集します。

| 起源 | 名前 | データタイプ | 目的 |
| --- | --- | --- | --- |
| リクエストヘッダー | IP アドレス | 文字列 | ユーザーの場所は、GeoIP 参照を通じて推測されます。 このデータは一時的で、永続的に保存されません。 |
| リクエストヘッダー | ユーザーエージェント文字列 | 文字列 | ユーザーが使用しているデバイスを決定します。 |
| クエリパラメーター | `_biz_u` | 文字列 | Bizible cookie ID。 |
| クエリパラメーター | `_biz_l` | 文字列 | 現在のページ URL。 |
| クエリパラメーター | `_biz_t` | 長さ | アクティビティのタイムスタンプ。 |
| クエリパラメーター | `_biz_i` | 文字列 | 現在のページタイトル。 |

上記の一般的なデータに加えて、bizible.js では、以下に示すリクエストタイプに応じて追加データも付加します。

| リクエストタイプ | リクエストパス | 追加のクエリパラメーター | データタイプ | 目的 |
| --- | --- | --- | --- | --- |
| ページビュー | `/ipv` | `_biz_r` | 文字列 | リファラーのページ URL。 |
|  |  | `_biz_h` | 文字列 | ハッシュ化されたクライアントの画面解像度。 |
|  |  | `_biz_c` | 文字列 | オプションのパラメーター。 このパラメーターが存在する場合は、追跡する前にユーザーの同意を待つようにテナントが`bizible.js`を設定し、`bizible.js`が追跡するユーザーの同意を受信したことを示します。 |
| フォーム送信 | `/frm` | `eMail` | 文字列 | プレーンテキストのメールアドレス。 |
| ユーザー ID マッピング | `/u` | `mapType` | 列挙 | 検出された`bizible.js`のユーザーID マッピングの種類（Marketo Munchkin IDおよびAdobe ECID） |
|  |  | `mapValue` | 文字列 | 上記の統合の実際のサードパーティ cookie ID の値。 |

>[!NOTE]
>
>Bizible は、Marketo Measure の旧名称です。
