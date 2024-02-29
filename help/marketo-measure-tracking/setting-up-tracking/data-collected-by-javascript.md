---
description: JavaScript で収集されるデータ — [!DNL Marketo Measure]
title: JavaScript で収集されるデータ
feature: Tracking
source-git-commit: 915e9c5a968ffd9de713b4308cadb91768613fc5
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 98%

---

# JavaScript で収集されるデータ {#data-collected-by-javascript}

デプロイメント時に Marketo Measure JavaScript で収集されるデータについて説明します。

**サンプルリクエスト：**

```
https://cdn.bizible.com/m/ipv?_biz_r=https%3A%2F%2Fwww.google.com%2F&_biz_h=-1801745101&_biz_u=7059e81415f34f7bbaf40fe32fdcba21&_biz_s=8cbeed&_biz_l=https%3A%2F%2Fwww.zendesk.com%2Fservice%2F&_biz_t=1676483822155&_biz_i=Customer%20service%20software%20for%20the%20best%20customer%20experiences%20%7C%20Zendesk&_biz_n=0&rnd=235938&cdn_o=a&_biz_z=1676483822155
```

<br>

Marketo Measure では、すべてのタイプのリクエストについて次の一般的なデータを収集します。

<table>
<thead>
  <tr>
    <th>起源</th>
    <th>名前</th>
    <th>データタイプ</th>
    <th>目的</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>リクエストヘッダー</td>
    <td>IP アドレス</td>
    <td>文字列</td>
    <td>ユーザの場所は、GeoIP 参照を通じて推測されます。このデータは一時的で、永続的に保存されません。</td>
  </tr>
  <tr>
    <td>リクエストヘッダー</td>
    <td>ユーザエージェント文字列</td>
    <td>文字列</td>
    <td>ユーザが使用しているデバイスを決定します。</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_u</td>
    <td>文字列</td>
    <td>Bizible cookie ID。</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_l</td>
    <td>文字列</td>
    <td>現在のページ URL。</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_t</td>
    <td>長さ</td>
    <td>アクティビティのタイムスタンプ。</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_i</td>
    <td>文字列</td>
    <td>現在のページタイトル。</td>
  </tr>
</tbody>
</table>

上記の一般的なデータに加えて、bizible.js では、以下に示すリクエストタイプに応じて追加データも追加します。

<table>
<thead>
  <tr>
    <th>リクエストタイプ</th>
    <th>リクエストパス</th>
    <th>追加のクエリパラメーター</th>
    <th>データタイプ</th>
    <th>目的</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>ページビュー</td>
    <td>/ipv</td>
    <td>_biz_r</td>
    <td>文字列</td>
    <td>リファラーのページ URL。</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td>_biz_h</td>
    <td>文字列</td>
    <td>ハッシュ化されたクライアントの画面解像度。</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td>_biz_c</td>
    <td>文字列</td>
    <td>オプションのパラメーター。このパラメーターが存在する場合、トラッキングする前にユーザの同意を待つようにテナントが bizible.js を設定し、bizible.js がトラッキングに対するユーザの同意を受け取ったことを示します。</td>
  </tr>
  <tr>
    <td>フォーム送信</td>
    <td>/frm</td>
    <td>eMail</td>
    <td>文字列</td>
    <td>プレーンテキストのメールアドレス。</td>
  </tr>
  <tr>
    <td>ユーザー ID マッピング</td>
    <td>/u</td>
    <td>mapType</td>
    <td>enum</td>
    <td>bizible.js で検出されたユーザー ID マッピングの種類（Marketo Munchkin ID と Adobe ECID）</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td>mapValue</td>
    <td>文字列</td>
    <td>上記の統合の実際のサードパーティ cookie ID の値。</td>
  </tr>
</tbody>
</table>

>[!NOTE]
>
>Bizible は、Marketo Measure の旧名称です。
