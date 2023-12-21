---
description: 統合権限の概要 — [!DNL Marketo Measure]  — 製品ドキュメント
title: 統合権限の概要
hide: true
hidefromtoc: true
feature: APIs, Integration
source-git-commit: d7ded9075f7f5831314d59294327f1e4928baf8a
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 4%

---

# 統合権限の概要 {#integration-permissions-overview}

このガイドでは、Marketo Measureとのシームレスな統合に必要な権限の概要を説明し、各統合が問題なく効果的に動作するようにします。

<table>
<thead>
  <tr>
    <th style="width:10%">統合</th>
    <th style="width:20%">データタイプ
    <li>Web インタラクションデータ</li>
    <li>B2B システムデータ</li>
    <li>広告プラットフォームデータ</li></th>
    <th style="width:30%">追跡する内容</th>
    <th style="width:40%">権限の要件</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Salesforce</td>
    <td>B2B システムデータ    
</td>
    <td>Marketo Measureが追跡している：
    <p>
    <li>アカウント</li>
    <li>キャンペーン</li>
    <li>CampaignMember</li>
    <li>取引先責任者</li>
    <li>CurrencyConversionRange</li>
    <li>CurrencyStatus</li>
    <li>イベント</li>
    <li>FieldHistory （リード、連絡先、商談）</li>
    <li>リード</li>
    <li>商談</li>
    <li>OpportunityContactRole</li>
    <li>OpportunityHistory</li>
    <li>タスク</li>
<p>
作成されたタッチポイントおよびその他のデータは、アカウント、キャンペーン、キャンペーン、キャンペーンメンバー、事例、連絡先、リード、商談のカスタム bizible フィールドに書き込まれます。</td>
    <td><b>Salesforce 接続ユーザ権限（必須）</b>
    <p>
    <b>専用ユーザーのMarketo Measure管理者権限セット：</b> SFDC 管理者が marketo 測定オブジェクトに対して CRUD 操作を実行できるようにします。
    <br>
    <b>変換済みリードの権限セットを表示および編集：</b> これにより、Marketo Measureは、連絡先に変換された後にリードを装飾できます。
    <br>
    <b>Salesforce マーケティングユーザチェックボックス：</b> 「マーケティングユーザー」チェックボックスを使用すると、キャンペーンを作成し、キャンペーンインポートウィザードを使用できます。
    <br>
    <b>Marketo Measure Standard ユーザー：</b> ユーザーがMarketo Measureオブジェクトからレコードを読み取れるようにします。
    <p>
    <b>Salesforce 標準フィールド権限</b>
    <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Salesforce 標準オブジェクトとアクセス</a>
    <p>
    <b>Salesforce カスタムフィールドの権限</b>
    <br>
    お客様が使用できるカスタム Salesforce フィールドを保持する機能設定が用意されています。 これらの機能設定が定義されている場合、各 Salesforce フィールドに対する読み取りアクセスが必要です ( 例えば、CustomLeadSourceField 設定値が「LeadSource__c」に等しい場合、このフィールドに対する読み取りアクセスが必要です )。
    </td>
  </tr>
  <tr>
    <td>Dynamics</td>
    <td>B2B システムデータ</td>
    <td>Marketo Measureが追跡している：
    <p>
    <li>アカウント
<li>ActivityParty
<li>ActivityPointer
<li>キャンペーン
<li>CampaignItem （CampaignList はシステム内）
<li>CampaignResponse （システム内の CampaignMember）
<li>取引先責任者
<li>リード
<li>リスト（システム内のマーケティングリスト）
<li>ListMember （システム内の MarketingListMember）
<li>商談
<li>組織
<li>TransactionCurrency （システム内の CurrencyConversionRange と CurrencyStatus）
<li>予定， CampaignActivity，メール， FAX，インシデント解決，レター，電話，定期的な予定のマスター， ServiceAppointment，タスク
<li>bizible2_bizible_abtest
<li>bizible2_bizible_attribution_touchpoint
<li>bizible2_bizible_event
<li>bizible2_bizible_history
<li>bizible2_bizible_touchpoint
<p>
作成されたタッチポイントおよびその他のデータは、アカウント、キャンペーン、キャンペーン、Campaign 応答、連絡先、リード、リスト、商談、PhoneCall のカスタム bizible フィールドに書き込まれます</td>
    <td><b>Marketo Measureユーザーの権限</b>
<p>
CRM の他のユーザーとの問題を回避するために、Dynamics 内に専用のMarketo Measureユーザーを作成して、データのエクスポートとインポートをおこなうことをお勧めします。 Marketo Measureアカウントの作成時に使用されるユーザー名とパスワード、およびエンドポイント URL を控えておきます。
<p>
<b>セキュリティロール</b>
<p>
組織で Dynamics セキュリティロールを使用している場合は、接続しているユーザー、または専用のMarketo Measureユーザーが必要なエンティティに対して十分な読み取り/書き込み権限を持っていることを確認してください。
<br>
セキュリティロールは、[ 設定 ] &gt; [ セキュリティ ] &gt; [ セキュリティロール ] の順に選択します。
<br>
Marketo Measureのカスタムエンティティの場合は、すべてのエンティティに対して完全な権限が必要になります。
<p>
<b>Dynamics 標準フィールドの権限</b>
<br>
<a href="/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/marketo-measure-dynamics-schema.md">Marketo Measure Dynamics スキーマ</a>
<p>
<b>Dynamics カスタムフィールドの権限</b>
<br>
顧客がカスタムのタッチポイント設定の抑制/削除ルールに使用するリードまたは連絡先エンティティのフィールドに対する読み取りアクセス権が必要です。
<br>
顧客がセグメントルールまたはステージマッピングに使用するリードまたは商談エンティティのフィールドに対する読み取りアクセス権が必要です。
<br>
顧客がキャンペーン/マーケティングリストメンバーの同期に使用する Campaign、CampaignResponse、List エンティティの任意のフィールドに対する読み取りアクセス権が必要です。
</td>
  </tr>
  <tr>
    <td>Facebook</td>
    <td>広告プラットフォームデータ</td>
    <td>facebookとの統合の目的：
<p>
<li>顧客広告データのインポート</li>
<li>顧客広告コストデータのインポート</li>
<li>URL パラメーターを追加してクライアントの広告を更新する</li>
<p>
Marketo Measureは、アカウント、キャンペーン、広告グループ、広告、フィルター ID および URL を追跡しています。</td>
    <td><li>キャンペーンの作成、広告の管理、広告指標の取得には、ads_management 権限が必要です。</li>
<li>ユーザーがFacebook E メールにログインできるようにするには、電子メール権限が必要です。</li>
<p>
<b>スコープ</b>
<p>
<a href="https://developers.facebook.com/docs/permissions/reference/ads_management/">ads_management</a>
<br>
<li>プログラムによるキャンペーンの作成、広告の管理、指標の取得が可能です。</li>
<li>革新的なソリューションと差別化された広告主向けの価値を提供する広告管理ツールを構築します。</li>
<p>
<a href="https://developers.facebook.com/docs/permissions/reference/email">電子メール</a>
<br>
<li>ユーザーとコミュニケーションを取り、Facebookプロファイルに関連付けられた電子メールアドレスを使用して、ユーザーがアプリにログインできるようにします。</li></td>
  </tr>
  <tr>
    <td>LinkedIn</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>DoubleClick</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>AdWords</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Bing</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Marketo Engage</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Adobe Analytics</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Bizible Javascript</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</tbody>
</table>
