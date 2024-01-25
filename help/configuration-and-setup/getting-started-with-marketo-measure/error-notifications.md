---
description: エラー通知 — [!DNL Marketo Measure]  — 製品ドキュメント
title: エラー通知
hide: true
hidefromtoc: true
feature: Fundamentals
source-git-commit: b4fadc6519761975736ce7a0e4f99a30c589c9af
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 1%

---

# エラー通知 {#error-notifications}

以下に、アプリ内通知または電子メールで受け取る可能性のあるエラーのリストを示します。 これらのいずれかを受け取った場合は、それぞれのトラブルシューティング手順に従ってください。 これらの手順で問題が解決しない場合は、 [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support).

<table>
  <tbody>
    <tr>
      <th style="width:31%">エラーコード</th>
      <th style="width:23%">通知の例</th>
      <th style="width:23%">説明</th>
      <th style="width:23%">トラブルシューティング手順</th>
    </tr>
    <tr>
      <td>API_DISABLED</td>
      <td>CRM インポート中にエラーが発生しました： API_DISABLED ：このユーザーの API 呼び出しが無効になっています</td>
      <td>Marketo Measureユーザーの API 権限が無効になっています。</td>
      <td>次の Salesforce ドキュメントを参照してください： <a href="https://help.salesforce.com/s/articleView?id=sf.branded_apps_commun_api_permset.htm&amp;type=5">API アクセスを有効にする方法</a>.</td>
    </tr>
    <tr>
      <td>API_LIMIT_EXCEEDED</td>
      <td>CRM エクスポート中にエラーが発生しました： PI_LIMIT_EXCEEDED</td>
      <td>CRM の API 制限を超えました（24 時間）。</td>
      <td>API クレジット割り当ての調整については、CRM に関する次のドキュメントを参照してください。</p>
          <ul>
            <li><a href="https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/service-protection-monitoring">Dynamics</a>
            </li>
            <li><a href="https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm">Salesforce</a>
            </li>
          </ul>
          <p>また、次の手順に従って、Marketo Measureで CRM クレジットを調整できます。</p>
          <ul>
            <li>に移動します。 <b>設定</b> &gt; <b>CRM</b> &gt; <b>一般</b></li>
            <li>1 日の CRM API 制限の更新<br/>
              <ul>
                <li><b>注意：デフォルトは 100,000 です。</b></li>
              </ul>
            </li>
          </ul>
          <p>
           <img src="assets/error-notifications-1.png">
          </p>
      </td>
    </tr>
    <tr>
      <td>INVALID_CONFIGURATION_ANALYTICS_CONFIGURATION</td>
      <td>AdobeAnalytics 書き出し中にエラーが発生しました： INVALID_ERROR_ANALYTICS_CONFIGURATION :ADOBE：アップロードできません。 アップロードする前に、データソーススキーマを確認してください。 データソース ID:1234</td>
      <td>Adobe Analytics統合が正しく設定されていません。</td>
      <td>次のヘルプ記事を参照して、正しい設定を確認します。
        <ul>
          <li>
            <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md">Marketo MeasureとAdobe Analyticsの統合</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html">顧客属性ソースの作成とデータファイルのアップロード</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>INVALID_CURRENCY_ISO_CODE</td>
      <td>広告のインポート中にエラーが発生しました： INVALID_CURRENCY_ISO_CODE：通貨 XXX はMarketo Measureでサポートされていません。
      <p>
      広告のインポート中にエラーが発生しました： INVALID_CURRENCY_ISO_CODE : 1234 のアカウントの通貨 XXX は、Marketo Measureではサポートされていません。</td>
      <td>サポートされていない通貨が検出されました。</td>
      <td>通知に示されるソースシステム ( 広告、CRM、Marketo) で、レコードに関連付けられた通貨がサポートされ、有効な通貨であることを確認します。 サポートされる通貨は、ISO 通貨標準に基づいています。</td>
    </tr>
    <tr>
      <td>MISSING_CONVERTED_LEAD_PERMISSION</td>
      <td>CRM エクスポート中にエラーが発生しました： MISSING_CONVERTED_LEAD_PERMISSION</td>
      <td>Marketo Measureには変換済みリードの表示/編集権限がありません</td>
      <td>CRM でこの権限を有効にする方法については、次のExperience Leagueドキュメントを参照してください<br/>
          <a href="/help/marketo-measure-salesforce-reporting/additional-functionality/enabling-the-permission-to-edit-converted-leads.md">変換済みリードを編集する権限の有効化</a></td>
    </tr>
    <tr>
      <td>MISSING_FIELD_READ_PERMISSION</td>
      <td>CRM インポート中にエラーが発生しました： MISSING_FIELD_READ_PERMISSION ：エンティティタイプ「Event」 : INVALID_FIELD :<br/>
    SystemModstamp,IsDeleted,WhoId,bizible2__Bizible_Touchpoint_Date__c</td>
      <td>Marketo Measureには必須フィールドに対する読み取り権限がありません。</td>
      <td>Marketo Measureで必要な権限については、次のヘルプ記事を参照してください。
        <ul>
          <li><a href="/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/marketo-measure-dynamics-schema.md">Dynamics</a>
          </li>
          <li><a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Salesforce</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>MISSING_ISREPLICATABLE_PERMISSION</td>
      <td>CRM インポート中にエラーが発生しました： MISSING_REPLICATABLE_PERMISSION :Campaign に IsReplicatable 権限がありません</td>
      <td>この権限は、Salesforce オブジェクトでMarketo Measureと Salesforce の同期を維持するために必要です。</td>
      <td>オブジェクトに対する複製可能な権限の設定に関してサポートが必要な場合は、Salesforce のサポートにお問い合わせください。</td>
    </tr>
    <tr>
      <td>MISSING_OBJECT_READ_PERMISSION</td>
      <td>CRM インポート中にエラーが発生しました： MISSING_OBJECT_READ_PERMISSION ：エンティティタイプキャンペーン`: CRM エラーコード： MISSING_PERMISSION</td>
      <td>Marketo Measureには、必要なオブジェクトに対する読み取り権限がありません。</td>
      <td rowspan="2">Marketo Measureで必要な権限については、次のヘルプ記事を参照してください。
          <ul>
            <li><a href="/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/marketo-measure-dynamics-schema.md">Dynamics</a>
            </li>
            <li><a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Salesforce</a>
            </li>
          </ul>
      </td>
    </tr>
    <tr>
      <td>MISSING_OBJECT_WRITE_PERMISSION</td>
      <td>CRM エクスポート中にエラーが発生しました： MISSING_OBJECT_WRITE_PERMISSION ：エンティティタイプ'bizible2_Bizible_Attribution_Touchpoint': CRM エラーコード： MISSING_PERMISSION</td>
      <td>Marketo Measureには必要なオブジェクトに対する書き込み権限がありません。</td>
    </tr>
    <tr>
      <td>NULL_EMPTY_CURRENCY_ISO_CODE</td>
      <td>
        <p>
          CRM インポート中にエラーが発生しました： NULL_EMPTY_CURRENCY_ISO_CODE: MultiCurrency が RecordId 1234 に対して有効になっている場合、通貨 ISO コードは NULL または空です
      </td>
      <td>通貨は、サポートされている ISO 通貨コードである必要があります。</td>
      <td>通知に示されるソースシステム ( 広告、CRM、Marketo) で、レコードに関連付けられた通貨がサポートされ、有効な通貨であることを確認します。 サポートされる通貨は、ISO 通貨標準に基づいています。</td>
    </tr>
    <tr>
      <td>OPERATION_TOO_LARGE</td>
      <td>CRM インポート中にエラーが発生しました： OPERATION_TOO_LARGE ：アクティビティを正常にクエリするには、「すべてのデータを表示」権限が必要です。</td>
      <td>CRM 設定では、Marketo Measureが十分な量のデータセットをクエリできません</td>
      <td>Marketo Measureに、指定したオブジェクトに対する「すべてのデータを表示」権限を付与します。
      <p>
      「すべてのデータを表示」権限の詳細 <a href="https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/users_profiles_view_all_mod_all.htm">ここにあります</a>.</td>
    </tr>
    <tr>
      <td>UNSUPPORTED_CRM_PACKAGE_VERSION</td>
      <td>CRM インポート中にエラーが発生しました： UNSUPPORTED_CRM_PACKAGE_VERSION : CRM パッケージを更新してください</td>
      <td>検出された現在のパッケージはサポートされなくなりました。</td>
      <td>パッケージを最新バージョンにアップグレードします。
        <ul>
          <li><a href="/help/configuration-and-setup/marketo-measure-and-salesforce/best-practices-for-marketo-measure-crm-package.md">ベストプラクティス</a>
          </li>
          <li><a href="/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/microsoft-dynamics-crm-installation-guide.md">Dynamics</a>
          </li>
          <li><a href="/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-salesforce-package-installation-and-set-up.md">Salesforce</a>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
