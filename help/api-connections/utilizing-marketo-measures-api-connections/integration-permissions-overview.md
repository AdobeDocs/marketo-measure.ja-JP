---
description: 統合権限の概要 — [!DNL Marketo Measure]  — 製品ドキュメント
title: 統合権限の概要
feature: APIs, Integration
source-git-commit: b7aea1e0789b2f4f3fd4b250c0f66595618317bb
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 3%

---

# 統合権限の概要 {#integration-permissions-overview}

このガイドでは、Marketo Measureとのシームレスな統合に必要な権限の概要を説明し、各統合が問題なく効果的に動作するようにします。

<table>
<thead>
  <tr>
    <th style="width:10%">統合</th>
    <th style="width:25%">データタイプ
    <li>Web インタラクションデータ</li>
    <li>B2B システムデータ</li>
    <li>広告プラットフォームデータ</li></th>
    <th style="width:25%">追跡する内容</th>
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
    <br>
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
<br>
CRM の他のユーザーとの問題を回避するために、Dynamics 内に専用のMarketo Measureユーザーを作成して、データのエクスポートとインポートをおこなうことをお勧めします。 Marketo Measureアカウントの作成時に使用されるユーザー名とパスワード、およびエンドポイント URL を控えておきます。
<p>
<b>セキュリティロール</b>
<br>
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
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/ads_management/">ads_management</a>
<br>
<li>プログラムによるキャンペーンの作成、広告の管理、指標の取得が可能です。</li>
<li>革新的なソリューションと差別化された広告主向けの価値を提供する広告管理ツールを構築します。</li>
<br>
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/email">電子メール</a>
<br>
<li>ユーザーとコミュニケーションを取り、Facebookプロファイルに関連付けられた電子メールアドレスを使用して、ユーザーがアプリにログインできるようにします。</li></td>
  </tr>
  <tr>
    <td>LinkedIn</td>
    <td>広告プラットフォームデータ
    <p>
    B2B システムデータ（リード生成フォームデータ。CRM アクティビティに分類されたフォームと送信を含む）。</td>
    <td>Marketo Measureは、LinkedIn Ads キャンペーン、クリエイティブ、コストのデータに加え、リードジェネレーションFormsと応答を追跡しています。 インポートされたデータに基づいて、LinkedInタッチポイントを生成し、顧客のリードにリードフォームの回答を関連付けることができます。</td>
    <td><li>Marketo Measureがコストデータをダウンロードするには、キャンペーンマネージャーまたはアカウントマネージャーの役割が必要です。 （スコープ行 1）</li>
    <br>
    <li>Marketo Measureがリード生成フォームデータにアクセスするには、スーパー管理者（ページ管理ロール、スコープ行 2）またはリード生成Formsマネージャ（有料メディア管理ロール、スコープ行 3）が必要です</li>
    <br>
    <li>Marketo Measureが自動タグ付けを操作するには、スーパー管理（ページ管理の役割、スコープの行 2）またはスポンサー付きコンテンツポスター（有料メディア管理の役割、スコープの行 3）が必要です</li>
    <p>
    <b>スコープ</b>
    <br>
    <a href="https://www.linkedin.com/campaignmanager/accounts">ポータルでのユーザーの役割の設定 (LinkedInアカウントへのログインが必要 )</a> - <a href="https://www.linkedin.com/help/lms/answer/a425731/user-roles-and-functions-in-campaign-manager">ユーザーの役割の概要</a>：ユーザーの役割、ユーザーの表示、権限の管理、アカウントマネージャーやキャンペーンマネージャーなどの役割の割り当てをおこないます
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en">ページ管理者ロールの設定 — <a href="https://www.linkedin.com/help/linkedin/answer/a541981/linkedin-page-admin-roles-overview">ページ管理者の役割の定義</a>：目的の管理ページ上のページ管理者の役割
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en">有料メディア管理者の役割を設定します（有料メディア管理者を探します） - <a href="https://www.linkedin.com/help/linkedin/answer/a554540">有料メディア管理者の定義</a>：有料メディア管理者の役割</td>
  </tr>
  <tr>
    <td>DoubleClick</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、広告主、キャンペーン、（カスタム）ランディングページ、広告、クリエイティブ、プレースメントおよびサイトを追跡しています。</td>
    <td><li>ユーザーの主なGoogleアカウントの電子メールアドレスが必要です</li>
<li>Campaign Manager 360 アカウントにアクセスするには、Campaign Manager の権限が必要です</li>
<ul>
<li>DoubleClick の広告主レポートの表示と管理</li>
<li>DoubleClick キャンペーンマネージャーのディスプレイ広告キャンペーンの表示と管理</li>
<p>
    <b>スコープ</b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>：プライマリGoogleアカウントの電子メールアドレスを確認する
    <p>
     <a href="https://www.googleapis.com/auth/dfareporting">https://www.googleapis.com/auth/dfareporting</a>:DoubleClick for Advertisers レポートの表示と管理
    <p>
     <a href="https://www.googleapis.com/auth/dfatrafficking">https://www.googleapis.com/auth/dfatrafficking</a>:DoubleClick Campaign Manager (DCM) ディスプレイ広告キャンペーンを表示および管理します</td>
  </tr>
  <tr>
    <td>AdWords</td>
    <td>広告プラットフォームデータ</td>
    <td>AdWords との統合の目的は次のとおりです。
<p>
<li>顧客広告データのインポート</li>
<li>顧客広告コストデータのインポート</li>
<li>URL パラメーターを追加/URL トラッキングテンプレートを更新して、クライアントの広告を更新する</li>
<p>
Marketo Measureは、キャンペーン、広告グループ、クリエイティブ、サイトリンク、キーワードを追跡しています。</td>
    <td><li>ユーザーの主なGoogleアカウントの電子メールアドレスが必要です</li>
<p>
    <b>スコープ</b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>：プライマリGoogleアカウントの電子メールアドレスを確認する</td>
  </tr>
  <tr>
    <td>Bing</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、キャンペーン、広告グループ、クリエイティブ、キーワードを追跡しています。</td>
    <td><li>ユーザーは、Microsoftアカウントを使用して「オフラインアクセス」を許可する必要があります ( ログインしていない場合でも、Marketo Measureに対してエンドユーザーの UserInfo へのアクセス権を付与します )。 詳しくは、 <a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">Microsoftページ</a> その方法に関して</li>
<p>
    <b>スコープ</b>
    <br>
    <a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access</a>：権限に対するアクセス権を付与したデータへのアクセス権を維持します。</td>
  </tr>
  <tr>
    <td>Marketo Engage</td>
    <td>B2B システムデータ</td>
    <td>Marketo統合により、Marketo MeasureはMarketoアクティビティ、ユーザー、プログラム、プログラムのメンバーシップを収集できます。 また、Marketo Measureは、Marketo Web アクティビティをMarketo Measureリードタッチポイントにリンクする目的で、Marketo Cookie(Munchkin ID) を追跡します。 <a href="/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/marketo-engage-programs-integration.md#cookie-mapping">ここで説明するように</a>:
    <p>
    <i>Marketo MeasureとMarketoの統合により、Marketo Measure Cookie ID もMarketo Munchkin ID とマッピングおよび同期されるようになりました。 これにより、FT タッチと LC タッチの両方をMarketo Activity に関連付けるのではなく、匿名のファーストタッチを Web セッションに関連付けるのに役立ちます。</i>
    </td>
    <td>お客様は、専用のMarketo EngageAPI ユーザーを作成し、Marketo Measureに資格情報を提供する必要があります。 追加の権限設定は必要ありません。 <a href="/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/set-up-marketo-connection.md#configuring-the-integration">詳細情報</a></td>
  </tr>
  <tr>
    <td>Adobe Analytics</td>
    <td>B2B システムデータ</td>
    <td>B2B 顧客属性の統合により、Marketo MeasureとAdobe Analyticsの相互ユーザーは、Marketo Measureのアトリビューションエンジンから得られる有用なメタデータと、CRM(Microsoft Dynamics と Salesforce) との同期機能を通じて、Adobe Analyticsのユーザープロファイルを強化できます。 <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md">詳細情報</a></td>
    <td>お客様は、Analytics インスタンスにデータをアップロードする場所に、エイリアス ID と FTP サーバーの資格情報をMarketo Measureに提供する必要があります。
    <p>
    プロセスの後の手順の一部で必要になるので、次の情報を控えておきます。
    <p>
    <li>エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をお勧めします。</li>
    <li>FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）</li>
    <p>
    <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md#configuring-the-integration">詳細情報</a></td>
  </tr>
  <tr>
    <td>Bizible Javascript</td>
    <td></td>
    <td><a href="/help/marketo-measure-tracking/setting-up-tracking/data-collected-by-javascript.md">bizible.js が収集するデータ</a>.</td>
    <td></td>
  </tr>
</tbody>
</table>

>[!MORELIKETHIS]
>
>[エラー通知](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}
