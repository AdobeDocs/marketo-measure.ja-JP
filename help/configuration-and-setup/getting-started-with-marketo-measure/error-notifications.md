---
description: エラー通知 — [!DNL Marketo Measure]
title: エラー通知
feature: Fundamentals
source-git-commit: 1a274c83814f4d729053bb36548ee544b973dff5
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 83%

---

# エラー通知 {#error-notifications}

以下に、アプリ内通知または電子メールで受け取る可能性のあるエラーのリストを示します。 これらのいずれかを受け取った場合は、それぞれのトラブルシューティング手順に従ってください。 このトラブルシューティング手順で問題が解決しない場合は、[Marketo サポート](https://nation.marketo.com/t5/support/ct-p/Support)にお問い合わせください。

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
      <td>CRM の読み込み中に発生したエラー：API_DISABLED：このユーザの API 呼び出しが無効になっています</td>
      <td>Marketo Measure ユーザの API 権限が無効になっています。</td>
      <td>Salesforce ドキュメントの <a href="https://help.salesforce.com/s/articleView?language=en_US&amp;id=sf.branded_apps_commun_api_permset.htm&amp;type=5">API アクセスを有効にする方法</a>を参照してください。</td>
    </tr>
    <tr>
      <td>API_LIMIT_EXCEEDED</td>
      <td>CRM の書き出し中に発生したエラー：PI_LIMIT_EXCEEDED</td>
      <td>CRM の API 制限（24 時間）を超えました。</td>
      <td>API クレジット割り当ての調整については、CRM に関する次のドキュメントを参照してください。</p>
          <ul>
            <li><a href="https://learn.microsoft.com/ja-jp/dynamics365/fin-ops-core/dev-itpro/data-entities/service-protection-monitoring">Dynamics</a>
            </li>
            <li><a href="https://developer.salesforce.com/docs/atlas.en-us.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_api.htm">Salesforce</a>
            </li>
          </ul>
          <p>また、次の手順に従って、Marketo Measure で使用する CRM クレジットを調整できます。</p>
          <ul>
            <li><b>設定</b>／<b>CRM</b>／<b>一般</b>に移動します。</li>
            <li>1 日の CRM API 制限を更新します<br/>
              <ul>
                <li><b>メモ：デフォルトは 100,000 です。</b></li>
              </ul>
            </li>
          </ul>
          <p>
           <img src="assets/error-notifications-1.png">
          </p>
      </td>
    </tr>
    <tr>
      <td>INVALID_ADOBE_ANALYTICS_CONFIGURATION</td>
      <td>Adobe Analytics書き出し中にエラーが発生しました： INVALID_ADOBE_ANALYTICS_CONFIGURATION ：エラー：アップロードできません。 アップロードする前に、データソーススキーマを確認します。 データソース ID：1234</td>
      <td>Adobe Analytics 統合が正しく設定されていません。</td>
      <td>次のヘルプ記事を参照して、正しい設定を確認します。
        <ul>
          <li>
            <a href="/help/marketo-measure-and-adobe/marketo-measure-integrations-with-adobe-analytics.md">Marketo Measure と Adobe Analytics の統合</a>
          </li>
          <li>
            <a href="https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=ja">顧客属性ソースの作成とデータファイルのアップロード</a>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>INVALID_CURRENCY_ISO_CODE</td>
      <td>広告の読み込み中に発生したエラー：INVALID_CURRENCY_ISO_CODE：通貨 XXX は、Marketo Measure ではサポートされていません。
      <p>
      広告の読み込み中に発生したエラー：INVALID_CURRENCY_ISO_CODE : 1234 のアカウントの通貨 XXX は、Marketo Measure ではサポートされていません。</td>
      <td>サポートしていない通貨が検出されました。</td>
      <td>通知に示されるソースシステム ( 広告、CRM、Marketo) では、レコードに関連付けられた通貨が、サポートされ、有効な通貨であることを確認します。 サポートされる通貨は、ISO 通貨標準に基づいています。</td>
    </tr>
    <tr>
      <td>MISSING_CONVERTED_LEAD_PERMISSION</td>
      <td>CRM の書き出し中に発生したエラー：MISSING_CONVERTED_LEAD_PERMISSION</td>
      <td>Marketo Measure には変換済みリードの表示／編集権限がありません</td>
      <td>CRM でこの権限を有効にする方法については、次の Experience League ドキュメントを参照してください<br/>
          <a href="/help/marketo-measure-salesforce-reporting/additional-functionality/enabling-the-permission-to-edit-converted-leads.md">変換済みリードを編集する権限の有効化</a></td>
    </tr>
    <tr>
      <td>MISSING_FIELD_READ_PERMISSION</td>
      <td>CRM の読み込み中に発生したエラー：MISSING_FIELD_READ_PERMISSION：エンティティタイプ「Event」：INVALID_FIELD：<br/>
    SystemModstamp,IsDeleted,WhoId,bizible2__Bizible_Touchpoint_Date__c</td>
      <td>Marketo Measure には必須フィールドに対する読み取り権限がありません。</td>
      <td>Marketo Measure に必要な権限に関するガイダンスについては、次のヘルプ記事を参照してください。
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
      <td>CRM 読み込み中にエラーが発生しました：MISSING_REPLICATABLE_PERMISSION：Campaign に IsReplicatable 権限がありません</td>
      <td>この権限は、Salesforce オブジェクトで Marketo Measure と Salesforce の同期を維持するために必要です。</td>
      <td>オブジェクトに対する複製可能な権限の設定については、Salesforce のサポートにお問い合わせください。</td>
    </tr>
    <tr>
      <td>MISSING_OBJECT_READ_PERMISSION</td>
      <td>CRM 読み込み中にエラーが発生しました：MISSING_OBJECT_READ_PERMISSION：エンティティタイプキャンペーン：CRM エラーコード：MISSING_PERMISSION</td>
      <td>Marketo Measure には、必要なオブジェクトに対する読み取り権限がありません。</td>
      <td rowspan="2">Marketo Measure に必要な権限に関するガイダンスについては、次のヘルプ記事を参照してください。
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
      <td>CRM 書き出し中にエラーが発生しました：MISSING_OBJECT_WRITE_PERMISSION：エンティティタイプ 'bizible2_Bizible_Attribution_Touchpoint'：CRM エラーコード：MISSING_PERMISSION</td>
      <td>Marketo Measure には必要なオブジェクトに対する書き込み権限がありません。</td>
    </tr>
    <tr>
      <td>NULL_EMPTY_CURRENCY_ISO_CODE</td>
      <td>
        <p>
          CRM 読み込み中にエラーが発生しました：NULL_EMPTY_CURRENCY_ISO_CODE：MultiCurrency が RecordId 1234 に対して有効になっている場合、通貨 ISO コードは NULL または空です
      </td>
      <td>通貨は、サポートされている ISO 通貨コードである必要があります。</td>
      <td>通知に示されるソースシステム ( 広告、CRM、Marketo) では、レコードに関連付けられた通貨が、サポートされ、有効な通貨であることを確認します。 サポートされる通貨は、ISO 通貨標準に基づいています。</td>
    </tr>
    <tr>
      <td>OPERATION_TOO_LARGE</td>
      <td>CRM 読み込み中にエラーが発生しました：OPERATION_TOO_LARGE：アクティビティを正常にクエリするには、「すべてのデータを表示」権限が必要です。</td>
      <td>CRM 設定では、Marketo Measure が十分な量のデータセットをクエリすることができません</td>
      <td>Marketo Measure に、指定したオブジェクトに対する「すべてのデータを表示」権限を付与します。
      <p>
      「すべてのデータを表示」権限の詳細については、<a href="https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/users_profiles_view_all_mod_all.htm">こちらを参照してください</a>。</td>
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
