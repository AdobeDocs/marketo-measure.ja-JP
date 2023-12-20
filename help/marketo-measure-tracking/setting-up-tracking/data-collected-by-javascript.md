---
description: JavaScript で収集されるデータ — [!DNL Marketo Measure]  — 製品ドキュメント
title: JavaScript で収集されるデータ
feature: Tracking
source-git-commit: 4d91899f6126a83b29170c7c5bbe146ed49ad9b0
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 8%

---

# JavaScript で収集されるデータ {#data-collected-by-javascript}

デプロイ時にMarketo Measure JavaScript で収集されるデータについて説明します。

リクエストの例：
`https://cdn.bizible.com/m/ipv?_biz_r=https%3A%2F%2Fwww.google.com%2F&_biz_h=-1801745101&_biz_u=7059e81415f34f7bbaf40fe32fdcba21&_biz_s=8cbeed&_biz_l=https%3A%2F%2Fwww.zendesk.com%2Fservice%2F&_biz_t=1676483822155&_biz_i=Customer%20service%20software%20for%20the%20best%20customer%20experiences%20%7C%20Zendesk&_biz_n=0&rnd=235938&cdn_o=a&_biz_z=1676483822155`

Marketo Measureは、すべてのタイプのリクエストに対して、次の共通データを収集します。

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
    <td>ユーザーの場所は GeoIP ルックアップを通じて推測されます。 このデータは一時的で、永久に保存されません。</td>
  </tr>
  <tr>
    <td>リクエストヘッダー</td>
    <td>ユーザーエージェント文字列</td>
    <td>文字列</td>
    <td>ユーザーが使用しているデバイスを決定します。</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_u</td>
    <td>文字列</td>
    <td>Bizible cookie ID</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_l</td>
    <td>文字列</td>
    <td>現在のページの URL</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_t</td>
    <td>long</td>
    <td>アクティビティのタイムスタンプ</td>
  </tr>
  <tr>
    <td>クエリパラメーター</td>
    <td>_biz_i</td>
    <td>文字列</td>
    <td>現在のページのタイトル</td>
  </tr>
</tbody>
</table>

上記の共通データに加えて、bizible.js は、以下に示すリクエストの種類に応じて、追加のデータも追加します。

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
    <td>Pageview</td>
    <td>/ipv</td>
    <td>_biz_r</td>
    <td>文字列</td>
    <td>リファラーページの URL。</td>
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
    <td>オプションのパラメーター。 このパラメータが存在する場合、テナントは、追跡前にユーザーの同意を待つように bizible.js を設定し、bizible.js が追跡対象のユーザーの同意を受け取ったことを示します。</td>
  </tr>
  <tr>
    <td>フォーム送信</td>
    <td>/frm</td>
    <td>eMail</td>
    <td>文字列</td>
    <td>プレーンテキストの E メールアドレス。</td>
  </tr>
  <tr>
    <td>ユーザー ID マッピング</td>
    <td>/u</td>
    <td>mapType</td>
    <td>enum</td>
    <td>bizible.js が検出したユーザー ID マッピングの種類 (Marketo Munchkin ID とAdobeECID)</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td>mapValue</td>
    <td>文字列</td>
    <td>上記の統合の実際のサードパーティ cookie ID 値。</td>
  </tr>
</tbody>
</table>

>[!NOTE]
>
>Bizible はMarketo Measureの旧名称です。
