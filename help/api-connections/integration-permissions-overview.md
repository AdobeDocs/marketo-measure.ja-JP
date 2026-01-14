---
description: Marketo Measure ユーザー向けの統合権限の概要ガイダンス
title: 統合権限の概要
feature: APIs, Integration
exl-id: c45598fe-0c33-459a-9fde-de7f6906bd0c
source-git-commit: fcd8e276c85669ddf12bd7404fb12d3e99b2642a
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 3%

---


# 統合権限の概要 {#integration-permissions-overview}

このガイドでは、Marketo Measureとのシームレスな統合に必要な権限の概要を説明し、各統合が問題なく効果的に機能することを確認します。

<table>
<thead>
  <tr>
    <th style="width:10%">統合</th>
    <th style="width:25%">データタイプ
    <li>Web インタラクションデータ</li>
    <li>B2B システムデータ</li>
    <li>広告プラットフォームデータ</li></th>
    <th style="width:25%">トラッキング対象</th>
    <th style="width:40%">権限の要件</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Salesforce</td>
    <td>B2B システムデータ
</td>
    <td>Marketo Measureがトラッキング中：
    <p>
    <li>アカウント</li>
    <li>キャンペーン</li>
    <li>CampaignMember</li>
    <li>取引先責任者</li>
    <li>CurrencyConversionRange</li>
    <li>CurrencyStatus</li>
    <li>イベント</li>
    <li>FieldHistory （リード、連絡先、機会）</li>
    <li>リード</li>
    <li>商談</li>
    <li>OpportunityContactRole</li>
    <li>OpportunityHistory</li>
    <li>タスク</li>
<p>
作成されたタッチポイントやその他のデータは、アカウント、キャンペーン、キャンペーンメンバー、ケース、連絡先、リード、商談のカスタム bizible フィールドに書き込まれます。</td>
    <td><b>Salesforce Connected User Permissions （必須） </b>
    <p>
    <b> 専用ユーザーのMarketo Measure管理者権限セット：</b> SFDC管理者が Marketo メジャーオブジェクトに対して CRUD 操作を実行できるようにします。
    <br>
    <b> コンバート済みリードの表示と編集権限セット：</b> これにより、Marketo Measureで連絡先にコンバートされた後のリードを修飾できます。
    <br>
    <b>Salesforce マーケティングユーザーチェックボックス：</b> マーケティングユーザーチェックボックスでは、キャンペーンを作成し、キャンペーンインポートウィザードを使用できます。
    <br>
    <b>Marketo Measure Standard ユーザー：</b> ユーザーがMarketo Measure オブジェクトからレコードを読み取れるようにします。
    <p>
    <b>Salesforce Standard フィールドの権限 </b>
    <br>
    <a href="/help/configuration-and-setup/how-marketo-measure-and-salesforce-interact.md">Salesforce標準オブジェクトおよびアクセス </a>
    <p>
    <b>Salesforce カスタムフィールドの権限 </b>
    <br>
    顧客が使用できるカスタム Salesforce フィールドを保持する機能設定を提供します。 これらの機能設定が定義されている場合、その機能設定に保存されている各 Salesforce フィールドへの読み取りアクセス権が必要になります（例えば、CustomLeadSourceField 設定の値が「LeadSource__c」に等しい場合、このフィールドへの読み取りアクセス権が必要になります）。
    </td>
  </tr>
  <tr>
    <td>Dynamics</td>
    <td>B2B システムデータ</td>
    <td>Marketo Measureがトラッキング中：
    <p>
    <li>アカウント
<li>ActivityParty
<li>ActivityPointer
<li>キャンペーン
<li>CampaignItem （システムの CampaignList）
<li>CampaignResponse （システムの CampaignMember）
<li>取引先責任者
<li>リード
<li>リスト（システムの MarketingList）
<li>ListMember （アドビのシステムでは MarketingListMember）
<li>商談
<li>組織
<li>TransactionCurrency （システムでは CurrencyConversionRange および CurrencyStatus）
<li>予定，CampaignActivity, メール，Fax, インシデント解決，レター，電話，定期的な予定マスター，ServiceAppointment, タスク
<li>bizible2_bizible_abtest
<li>bizible2_bizible_attribution_touchpoint
<li>bizible2_bizible_event
<li>bizible2_bizible_history
<li>bizible2_bizible_touchpoint
<p>
作成されたタッチポイントやその他のデータは、アカウント、キャンペーン、CampaignResponse、連絡先、リード、リスト、商談、通話のカスタム bizible フィールドに書き込まれます</td>
    <td><b>Marketo Measure ユーザーの権限 </b>
<br>
CRM 内の他のユーザーとの問題を回避するために、を通じてデータを書き出しおよび読み込む専用のMarketo Measure ユーザーを Dynamics 内に作成することをお勧めします。 Marketo Measure アカウントの作成時に使用されるユーザー名とパスワード、エンドポイント URL をメモします。
<p>
<b> セキュリティ上の役割 </b>
<br>
Dynamics セキュリティーロールを使用している場合は、接続ユーザーまたは専用のMarketo Measure ユーザーに、必要なエンティティに対する十分な読み取り/書き込み権限があることを確認します。
<br>
セキュリティの役割は、設定/セキュリティ/セキュリティの役割の場所にあります。
<br>
Marketo Measureのカスタムエンティティの場合は、すべてのエンティティに対する完全な権限が必要になります。
<p>
<b>Dynamics Standard フィールドの権限 </b>
<br>
<a href="/help/marketo-measure-dynamics-schema.md">Marketo Measure Dynamics スキーマ </a>
<p>
<b>Dynamics カスタムフィールドの権限 </b>
<br>
顧客がカスタムのタッチポイント設定の抑制/削除ルールに使用したいリードまたは連絡先エンティティ上の任意のフィールドに対する読み取りアクセス権が必要です。
<br>
顧客がセグメントルールまたはステージマッピングに使用する、リードまたは商談エンティティ上のフィールドに対する読み取りアクセス権が必要です。
<br>
Campaign/MarketingList メンバーの同期に使用したい Campaign、CampaignResponse および List エンティティのフィールドに対する読み取りアクセス権が必要です。
</td>
  </tr>
  <tr>
    <td>Facebook</td>
    <td>広告プラットフォームデータ</td>
    <td>Facebook との統合により、次のことが可能になります。
<p>
<li>顧客広告データの読み込み</li>
<li>顧客広告コストデータのインポート</li>
<li>URL パラメーターを追加してクライアントの広告を更新します</li>
<p>
Marketo Measureは、アカウント、キャンペーン、広告グループ、広告、フィルター ID および URL をトラッキングします。</td>
    <td><li>キャンペーンの作成、広告の管理または広告指標の取得を行うには、ads_management 権限が必要です。</li>
<li>ユーザーが Facebook メールにログインするには、メール権限が必要です。</li>
<p>
<b> 範囲 </b>
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/ads_management/">ads_management</a>
<br>
<li>プログラムによるキャンペーンの作成、広告の管理および指標の取得を行います。</li>
<li>広告主に革新的なソリューションと差別化された価値を提供する広告管理ツールを構築します。</li>
<br>
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/email"> 電子メール </a>
<br>
<li>ユーザーとのコミュニケーションを行い、Facebook プロファイルに関連付けられたメールアドレスでアプリにログインさせる。</li></td>
  </tr>
  <tr>
    <td>LinkedIn</td>
    <td>広告プラットフォームデータ
    <p>
    B2B システムデータ（CRM アクティビティに分類されたフォームや送信を含むリード生成フォームデータ）。</td>
    <td>Marketo Measureは、LinkedIn 広告キャンペーン、クリエイティブ、コストデータのほか、リード生成Formsと応答をトラッキングしています。 読み込んだデータに基づいて、LinkedIn タッチポイントを生成し、リードフォームの回答を顧客のリードに関連付けることができます。</td>
    <td><li>Marketo Measureでコストデータをダウンロードするには、キャンペーンマネージャーまたはアカウントマネージャーの役割が必要です。 （一の項の範囲）</li>
    <br>
    <li>Marketo Measureがリード生成フォームデータにアクセスするには、スーパー管理者（ページ管理者ロール、範囲の行 2）またはリード生成Forms Manager （有料メディア管理者ロール、範囲の行 3）が必要です</li>
    <br>
    <li>Marketo Measureで自動タグ付けを操作するには、スーパー管理者（ページ管理者ロール、範囲の行 2）またはスポンサー付きコンテンツポスター（有料メディア管理者ロール、範囲の行 3）が必要です</li>
    <p>
    <b> 範囲 </b>
    <br>
    <a href="https://www.linkedin.com/campaignmanager/accounts"> ポータルでのユーザーロールの設定（LinkedIn アカウントへのログインが必要） </a> - <a href="https://www.linkedin.com/help/lms/answer/a425731/user-roles-and-functions-in-campaign-manager"> ユーザーロールの概要 </a>：ユーザーロール、ユーザー権限の表示と管理、アカウントマネージャーやキャンペーンマネージャーなどの役割の割り当て
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en"> ページ管理者ロールの設定 – <a href="https://www.linkedin.com/help/linkedin/answer/a541981/linkedin-page-admin-roles-overview"> ページ管理者ロールの定義 </a>：目的の管理ページでのページ管理者ロール
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en"> 有料メディア管理者ロールの設定（有料メディア管理者を探す） – <a href="https://www.linkedin.com/help/linkedin/answer/a554540"> 有料メディア管理者定義 </a>：有料メディア管理者ロール</td>
  </tr>
  <tr>
    <td>DoubleClick</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、広告主、キャンペーン、（カスタム）ランディングページ、広告、クリエイティブ、プレースメントおよびサイトをトラッキングします。</td>
    <td><li>ユーザーのプライマリ Google アカウントの E メール アドレスが必要です</li>
<li>Campaign Manager 360 アカウントへのアクセスに必要な Campaign Manager 権限</li>
<ul>
<li>DoubleClick 広告主レポートの表示と管理</li>
<li>DoubleClick キャンペーンマネージャーの表示と管理ディスプレイ広告キャンペーン</li>
<p>
    <b> 範囲 </b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>：主要なGoogle アカウントのメールアドレスを確認する
    <p>
     <a href="https://www.googleapis.com/auth/dfareporting">https://www.googleapis.com/auth/dfareporting</a>：広告主向け DoubleClick レポートの表示と管理
    <p>
     <a href="https://www.googleapis.com/auth/dfatrafficking">https://www.googleapis.com/auth/dfatrafficking</a>: DoubleClick Campaign マネージャー（DCM）のディスプレイ広告キャンペーンを表示および管理します</td>
  </tr>
  <tr>
    <td>AdWords</td>
    <td>広告プラットフォームデータ</td>
    <td>AdWords との統合により、次のことが可能になります。
<p>
<li>顧客広告データの読み込み</li>
<li>顧客広告コストデータのインポート</li>
<li>URL パラメーターを追加してクライアントの広告を更新/URL トラッキングテンプレートを更新</li>
<p>
Marketo Measureは、キャンペーン、広告グループ、クリエイティブ、サイトリンクおよびキーワードをトラッキングします。</td>
    <td><li>ユーザーのプライマリ Google アカウントの E メール アドレスが必要です</li>
<p>
    <b> 範囲 </b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>：主要なGoogle アカウントのメールアドレスを確認する</td>
  </tr>
  <tr>
    <td>Bing</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、キャンペーン、広告グループ、クリエイティブおよびキーワードをトラッキングしています。</td>
    <td><li>ユーザーは、Microsoft アカウントで「オフラインアクセス」を許可する必要があります（これにより、ログインしていない場合でも、エンドユーザーの UserInfo へのMarketo Measure アクセスが許可されます）。 その方法については、<a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">Microsoftのページ </a> を参照してください。</li>
<p>
    <b> 範囲 </b>
    <br>
    <a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access</a>：権限を付与したデータへのアクセスを維持します。</td>
  </tr>
  <tr>
    <td>Marketo Engage</td>
    <td>B2B システムデータ</td>
    <td>Marketo統合によって、Marketo Measureは、Marketoのアクティビティ、ユーザー、プログラムおよびプログラムメンバーシップを収集できます。 さらに、Marketo Measureは、Marketo web アクティビティをMarketo Measure リードタッチポイントにリンクする目的で、Marketo Cookie （Munchkin ID<a href="/help/marketo-engage-programs-integration.md#cookie-mapping"> を追跡します（詳しくは、こちらを参照 </a>。
    <p>
    <i>MarketoとMarketo Measureを統合した結果、Marketo Measure Cookie ID もマッピングされ、Marketo Munchkin ID と同期されるようになりました。 これは、FT と LC の両方のタッチをMarketo アクティビティに関連付けるのではなく、匿名のファーストタッチを web セッションに関連付けることのできるギャップを埋めるのに役立ちます。</i>
    </td>
    <td>お客様は、専用のMarketo Engage API ユーザーを作成し、Marketo Measureに資格情報を提供する必要があります。 追加の権限設定は必要ありません。 <a href="/help/set-up-marketo-connection.md#configuring-the-integration">詳細情報</a>。</td>
  </tr>
  <tr>
    <td>Adobe Analytics</td>
    <td>B2B システムデータ</td>
    <td>B2B 顧客属性の統合により、Marketo MeasureとAdobe Analyticsの相互ユーザーは、Adobe Analytics アトリビューションエンジンおよび CRM との同期機能から得られる貴重なメタデータを使用して、Marketo Measure ユーザープロファイルをエンリッチメントできます（Microsoft DynamicsとSalesforce）。 <a href="/help/adobe-analytics.md">詳細情報</a>。</td>
    <td>お客様は、Analytics インスタンスにデータをアップロードする場所に、Marketo Measureにエイリアス ID と FTP サーバー資格情報を提供する必要があります。
    <p>
    プロセスの後半の手順で必要になるので、次の情報に注意してください。
    <p>
    <li>エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をお勧めします</li>
    <li>FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）</li>
    <p>
    <a href="/help/adobe-analytics.md#configuring-the-integration">詳細情報</a></td>
  </tr>
  <tr>
    <td>Bizible Javascript</td>
    <td></td>
    <td><a href="/help/marketo-measure-tracking/data-collected-by-javascript.md">bizible.js が収集するデータ </a>.</td>
    <td></td>
  </tr>
</tbody>
</table>

>[!MORELIKETHIS]
>[エラー通知](/help/configuration-and-setup/error-notifications.md){target="_blank"}
