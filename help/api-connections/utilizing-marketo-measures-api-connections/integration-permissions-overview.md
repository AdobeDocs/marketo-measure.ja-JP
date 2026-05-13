---
description: 統合権限の概要 –  [!DNL Marketo Measure]
title: 統合権限の概要
feature: APIs, Integration
exl-id: c45598fe-0c33-459a-9fde-de7f6906bd0c
TQID: https://experienceleague.adobe.com/e0BkGPzfpf6LjR0eIUfOTLku8d-Dgm6Kh6Jlfs3cLBA
product_v2: id: e6fc4016-a972-4f36-8c30-a6a5f82ad0c8
feature_v2: id: c8f57308-7e33-4e41-a385-b55041c78939id: fb43f4c1-87d9-4081-8df1-6fe7e6e5cdc8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 9ceb54139bfa9b6ce7c2c5fbb4e25e649f5708a3
workflow-type: tm+mt
source-wordcount: 1406
ht-degree: 2%

---

# 統合権限の概要 {#integration-permissions-overview}

このガイドでは、Marketo Measureとのシームレスな連携を実現するために必要な権限について解説します。

<table>
<thead>
  <tr>
    <th style="width:10%">統合</th>
    <th style="width:25%">データタイプ
    <li>Web インタラクションデータ</li>
    <li>B2B システムデータ</li>
    <li>広告プラットフォームデータ</li></th>
    <th style="width:25%">アドビが追跡できること</th>
    <th style="width:40%">権限の要件</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Salesforce</td>
    <td>B2B システムデータ    
</td>
    <td>Marketo Measureが追跡しています。
    <p>
    <li>アカウント</li>
    <li>キャンペーン</li>
    <li>CampaignMember</li>
    <li>取引先責任者</li>
    <li>CurrencyConversionRange</li>
    <li>CurrencyStatus</li>
    <li>イベント</li>
    <li>フィールド履歴（リード、取引先責任者、商談）</li>
    <li>リード</li>
    <li>商談</li>
    <li>OpportunityContactRole</li>
    <li>OpportunityHistory</li>
    <li>タスク</li>
<p>
作成されたタッチポイントやその他のデータは、アカウント、キャンペーン、キャンペーンメンバー、ケース、取引先責任者、リード、商談のカスタム Bizible フィールドに書き込まれます。</td>
    <td><b>Salesforce Connected User Permissions （必須） </b>
    <p>
    <b>専用ユーザーのMarketo Measure Administrator権限セット：</b> SFDC管理者がmarketo measure オブジェクトに対してCRUD操作を実行できるようにします。
    <br>
    <b> コンバージョンしたリードの表示と編集パーミッションセット：</b>これにより、Marketo Measureはリードを連絡先に変換した後で装飾することができます。
    <br>
    <b>Salesforce Marketing User Checkbox:</b> Marketing User チェックボックスを使用すると、ユーザーはキャンペーンを作成し、キャンペーンの読み込みウィザードを使用できます。
    <br>
    <b>Marketo Measure標準ユーザー：</b>は、Marketo Measure オブジェクトからレコードを読み取ることができます。
    <p>
    <b>Salesforce標準フィールドの権限</b>
    <br>
    <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Salesforce標準オブジェクトとアクセス </a>
    <p>
    <b>Salesforce カスタムフィールドの権限</b>
    <br>
    お客様が使用できるカスタム Salesforce フィールドを保持するための機能設定を提供します。 これらの機能設定が定義されている場合は、機能設定に保存されている各salesforce フィールドへの読み取りアクセスが必要です（例：CustomLeadSourceSourceField設定値が「LeadSource__c」に等しい場合は、このフィールドへの読み取りアクセスが必要です）。
    </td>
  </tr>
  <tr>
    <td>Dynamics</td>
    <td>B2B システムデータ</td>
    <td>Marketo Measureが追跡しています。
    <p>
    <li>アカウント
<li>ActivityParty
<li>ActivityPointer
<li>キャンペーン
<li>CampaignItem （システム内のCampaignList）
<li>CampaignResponse （システムのCampaignMember）
<li>取引先責任者
<li>リード
<li>リスト（システム内のMarketingList）
<li>ListMember （システム内のMarketingListMember）
<li>商談
<li>組織
<li>TransactionCurrency （当社のシステムのCurrencyConversionRangeとCurrencyStatus）
<li>アポイントメント，キャンペーンアクティビティ，メール，ファックス，インシデント解決，手紙，電話，定期的なアポイントメントのマスター，サービストアメント，タスク
<li>bizible2_bizible_abtest
<li>bizible2_bizible_attribution_touchpoint
<li>bizible2_bizible_event
<li>bizible2_bizible_history
<li>bizible2_bizible_touchpoint
<p>
作成されたタッチポイントやその他のデータは、アカウント、キャンペーン、キャンペーン応答、連絡先、リード、リスト、商談、電話呼び出しのカスタム Bizible フィールドに書き込まれます</td>
    <td><b>Marketo Measure ユーザー権限</b>
<br>
CRM内の他のユーザーに関する問題を回避するために、Dynamics内に専用のMarketo Measure ユーザーを作成し、を通じてデータを書き出して読み込むことをお勧めします。 Marketo Measure アカウントの作成時に使用されるユーザー名とパスワード、およびエンドポイント URLに注意してください。
<p>
<b> セキュリティの役割</b>
<br>
組織でDynamics セキュリティ ロールを使用している場合は、接続されているユーザーまたは専用のMarketo Measure ユーザーに、必要なエンティティに対する十分な読み取り/書き込み権限があることを確認します。
<br>
セキュリティロールは、設定/セキュリティ/セキュリティロールにあります。
<br>
Marketo Measure カスタムエンティティの場合、すべてのエンティティに対する完全な権限が必要です。
<p>
<b>Dynamics標準フィールドの権限</b>
<br>
<a href="/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/marketo-measure-dynamics-schema.md">Marketo Measure Dynamics スキーマ </a>
<p>
<b>Dynamics カスタムフィールドの権限</b>
<br>
お客様がカスタムタッチポイント設定ルールの抑制/削除に使用するリードまたは連絡先エンティティのフィールドには、読み取りアクセス権が必要です。
<br>
お客様がセグメントルールまたはステージマッピングに使用するリードまたは商談エンティティのフィールドには、読み取りアクセス権が必要です。
<br>
お客様がCampaign/MarketingList メンバーの同期に使用するCampaign、CampaignResponse、およびList エンティティの任意のフィールドに対する読み取りアクセス権が必要です。
</td>
  </tr>
  <tr>
    <td>Facebook</td>
    <td>広告プラットフォームデータ</td>
    <td>Facebookと統合して、以下を行います。
<p>
<li>顧客広告データの読み込み</li>
<li>顧客広告のコストデータのインポート</li>
<li>URL パラメーターを追加してクライアントの広告を更新する</li>
<p>
Marketo Measureは、アカウント、キャンペーン、広告グループ、広告、フィルターID、URLを追跡します。</td>
    <td><li>キャンペーンの作成、広告の管理、広告指標の取得には、ads_management権限が必要です。</li>
<li>ユーザーがFacebook メールにログインできるようにするには、メール権限が必要です。</li>
<p>
<b>範囲</b>
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/ads_management/">ads_management</a>
<br>
<li>プログラムによるキャンペーンの作成、広告の管理、指標の取得などをおこないます。</li>
<li>広告主に革新的なソリューションと差別化された価値を提供する広告管理ツールを構築します。</li>
<br>
<br>
<a href="https://developers.facebook.com/docs/permissions/reference/email">電子メール </a>
<br>
<li>ユーザーとコミュニケーションを取り、Facebook プロファイルに関連付けられたメールアドレスを使用してアプリにログインできるようにします。</li></td>
  </tr>
  <tr>
    <td>LinkedIn</td>
    <td>広告プラットフォームデータ
    <p>
    B2B システムデータ（CRM アクティビティとして分類された、フォームや送信を含むリードジェネレーションフォームデータ）。</td>
    <td>Marketo Measureでは、LinkedInの広告キャンペーン、クリエイティブ、コストに関するデータと、リードジェネレーションのFormsと回答を追跡しています。 「インポートしたデータにもとづいてLinkedInの顧客接点を生成し、顧客向けのリードにリードフォームの応答を関連付けることができます。</td>
    <td><li>Marketo Measureでコストデータをダウンロードするには、Campaign ManagerまたはAccount Managerの役割が必要です。 （スコープの項1）</li>
    <br>
    <li>Marketo Measureがリードジェネレーションフォームのデータにアクセスするには、スーパー管理者（ページ管理者ロール、スコープ行2）またはリードジェネレーションForms Manager （有料メディア管理者ロール、スコープ行3）が必要です</li>
    <br>
    <li>Marketo Measureで自動タグ付けを操作するには、スーパー管理者（Page Admin Role、Scopes row 2）またはスポンサードコンテンツポスター（Paid Media Admin Role、Scopes row 3）が必要です</li>
    <p>
    <b>範囲</b>
    <br>
    <a href="https://www.linkedin.com/campaignmanager/accounts"> ポータルでユーザーの役割を設定する（LinkedIn アカウントへのログインが必要） </a> - <a href="https://www.linkedin.com/help/lms/answer/a425731/user-roles-and-functions-in-campaign-manager"> ユーザーの役割の概要</a>：ユーザーの役割、ユーザー権限の表示と管理、アカウントマネージャーやキャンペーンマネージャーなどの役割の割り当て
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en"> ページ管理者ロールの設定 – <a href="https://www.linkedin.com/help/linkedin/answer/a541981/linkedin-page-admin-roles-overview"> ページ管理者ロールの定義</a>：ページ管理者ロール（目的の管理ページ上）
    <p>
    <a href="https://www.linkedin.com/help/linkedin/answer/a570172/add-or-remove-admins-on-your-showcase-page?lang=en">有料メディア管理者の役割を設定（有料メディア管理者を探してください） - <a href="https://www.linkedin.com/help/linkedin/answer/a554540">有料メディア管理者の定義</a>：有料メディア管理者の役割</td>
  </tr>
  <tr>
    <td>DoubleClick</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、広告主、キャンペーン、（カスタム）ランディングページ、広告、クリエイティブ、プレースメント、サイトを追跡します。</td>
    <td><li>ユーザーのGoogle アカウントのメールアドレスが必要です</li>
<li>Campaign Manager 360 アカウントへのアクセスに必要なCampaign Manager権限</li>
<ul>
<li>DoubleClick広告主レポートの表示と管理</li>
<li>DoubleClick キャンペーンマネージャーの表示と管理の広告キャンペーン</li>
<p>
    <b>範囲</b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>: Google アカウントのメールアドレスを確認してください
    <p>
     <a href="https://www.googleapis.com/auth/dfareporting">https://www.googleapis.com/auth/dfareporting</a>：広告主向けDoubleClick レポートの表示と管理
    <p>
     <a href="https://www.googleapis.com/auth/dfatrafficking">https://www.googleapis.com/auth/dfatrafficking</a>: DoubleClick Campaign Manager （DCM）のディスプレイ広告キャンペーンを表示および管理します</td>
  </tr>
  <tr>
    <td>AdWords</td>
    <td>広告プラットフォームデータ</td>
    <td>Adobe AdWordsと統合することで、次のことが可能になります。
<p>
<li>顧客広告データの読み込み</li>
<li>顧客広告のコストデータのインポート</li>
<li>Url パラメーターを追加するか、Url トラッキングテンプレートを更新して、クライアントの広告を更新する</li>
<p>
Marketo Measureは、キャンペーン、広告グループ、クリエイティブ、サイトリンク、キーワードを追跡します。</td>
    <td><li>ユーザーのGoogle アカウントのメールアドレスが必要です</li>
<p>
    <b>範囲</b>
    <br>
    <a href="https://www.googleapis.com/auth/userinfo.email">https://www.googleapis.com/auth/userinfo.email</a>: Google アカウントのメールアドレスを確認してください</td>
  </tr>
  <tr>
    <td>Bing</td>
    <td>広告プラットフォームデータ</td>
    <td>Marketo Measureは、アカウント、キャンペーン、広告グループ、クリエイター、キーワードを追跡します。</td>
    <td><li>ユーザーは、Microsoft アカウントを使用して「オフラインアクセス」を付与する必要があります（ログインしていない場合でも、Marketo MeasureにエンドユーザーのUserInfoへのアクセス権を付与します）。 その方法については、<a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">Microsoftのページ </a>を参照してください。</li>
<p>
    <b>範囲</b>
    <br>
    <a href="https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access">https://learn.microsoft.com/en-us/deployoffice/overview-extended-offline-access</a>：権限へのアクセス権を与えたデータへのアクセス権を維持します。</td>
  </tr>
  <tr>
    <td>Marketo Engage</td>
    <td>B2B システムデータ</td>
    <td>Marketoとの統合により、Marketo MeasureはMarketo アクティビティ、人物、プログラム、およびプログラムメンバーシップを収集できます。 さらに、Marketo Measureは、Marketo web アクティビティをMarketo Measureのリードタッチポイントにリンクする目的で、Marketo Cookie （Munchkin ID）を追跡します。詳細については、<a href="/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/marketo-engage-programs-integration.md#cookie-mapping">こちらを参照してください</a>:
    <p>
    <i>Marketo MeasureとMarketoの統合の結果、Marketo Measure Cookie IDもMarketo Munchkin IDとマッピングおよび同期されるようになりました。 これにより、FTとLCの両方のタッチをMarketo アクティビティに関連付けるのではなく、匿名のファーストタッチをweb セッションに関連付けるためにギャップを埋めることができます。</i>
    </td>
    <td>お客様は、専用のMarketo Engage API ユーザーを作成し、資格情報をMarketo Measureに提供する必要があります。 追加の権限設定は必要ありません。 <a href="/help/marketo-measure-and-marketo/marketo-measure-integrations-with-marketo/set-up-marketo-connection.md#configuring-the-integration">詳細情報</a>。</td>
  </tr>
  <tr>
    <td>Adobe Analytics</td>
    <td>B2B システムデータ</td>
    <td>B2B顧客属性の統合により、Marketo MeasureとAdobe Analyticsの両方のユーザーは、Adobe Analyticsアトリビューションエンジンから得られた貴重なメタデータと、CRM （Microsoft DynamicsおよびSalesforce）との同期機能を通じて、Marketo Measureユーザープロファイルを強化できます。 <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md">詳細情報</a>。</td>
    <td>お客様は、Analytics インスタンスにデータがアップロードされる場所に、Marketo Measureにエイリアス IDとFTP サーバーの資格情報を提供する必要があります。
    <p>
    以下の情報に注意してください。この情報は、プロセスの後の手順で必要になります。
    <p>
    <li>エイリアス ID。任意の値を指定できます。 「marketomeasure_id」をおすすめします</li>
    <li>FTP サーバーのホスト名と資格情報（ユーザー名とパスワード）</li>
    <p>
    <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md#configuring-the-integration">詳細情報</a></td>
  </tr>
  <tr>
    <td>Bizible Javascript</td>
    <td></td>
    <td><a href="/help/marketo-measure-tracking/setting-up-tracking/data-collected-by-javascript.md">Bizible.jsが収集するデータ </a>。</td>
    <td></td>
  </tr>
</tbody>
</table>

>[!MORELIKETHIS]
>
>[エラー通知](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}
