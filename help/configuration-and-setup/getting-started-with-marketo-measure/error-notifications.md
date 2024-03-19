---
description: エラー通知 — [!DNL Marketo Measure]
title: エラー通知
feature: Fundamentals
exl-id: ed07eed6-ddeb-4856-a1ac-ea3d571283f6
source-git-commit: 20f886a0c6f448956ad2fda2d21a25f8d9a5a6af
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 30%

---

# エラー通知 {#error-notifications}

以下に、アプリ内通知または電子メールで受け取る可能性のあるエラーのリストを示します。 これらのいずれかを受け取った場合は、それぞれのトラブルシューティング手順に従ってください。 このトラブルシューティング手順で問題が解決しない場合は、[Marketo サポート](https://nation.marketo.com/t5/support/ct-p/Support)にお問い合わせください。

完全な通知メッセージを表示するには、以下を参照してください： [!DNL Marketo Measure]をクリックし、 **すべて表示** をクリックします。

![](assets/error-notifications-1.png)

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
           <img src="assets/error-notifications-2.png">
          </p>
      </td>
    </tr>
    <tr>
      <td>CANNOT_EXECUTE_FLOW_トリガー</td>
      <td>CRM エクスポート中にエラーが発生しました： CANNOT_EXECUTE_FLOW_ENTITY ：エンティティタイプ「連絡先」Salesforce 管理者にこれらの詳細を伝えます。
制限を超えました。制限を超えた場合、組織がこの機能の上限を超えています。 エラー ID: 123456</td>
      <td>レコードは、Salesforce 組織で設定されたトリガーフロールールを満たしていないので、保存できません。</td>
      <td>通知メッセージの詳細を確認し、Salesforce 組織のフロートリガーを確認します。
フロートリガーに関する Salesforce ドキュメント <a href="https://admin.salesforce.com/blog/2023/what-is-a-record-triggered-flow#:~:text=A%20record%2Dtriggered%20flow%20allows,is%20created%20and%2For%20updated">ここにあります</a>.
      </td>
    </tr>
    <tr>
      <td>CANNOT_INSERT_UPDATE_ACTIVATE_ENTITY</td>
      <td>CRM エクスポート中にエラーが発生しました： CANNOT_INSERT_UPDATE_ACTIVATE_ENTITY ：エンティティタイプ「リード」: CRM ErrorCode : CANNOT_INSERT_UPDATE_ACTIVATE_ENTITY, CRM ErrorMessage : System.Limit Cpu CPU time limit, Recod Id:
      <p>
      CRM エクスポート中にエラーが発生しました： CANNOT_INSERT_UPDATE_ACTIVATE_ENTITY ：エンティティタイプ「アカウント」: CRM エラーコード： CANNOT_INSERT_UPDATE_ACTIVATE_ENTITY, CRM ErrorMessage ：エンティティタイプを更新できません：アカウント、レコード ID: 0123456</td>
      <td>トリガーがオブジェクトの更新や挿入を妨げています。
      <p>
      OR
      <p>
      オブジェクトに対する権限がありません。</td>
      <td>挿入/更新が失敗する原因となっているトリガーコードを確認します。 トリガーの詳細については、次の Salesforce ドキュメントを参照してください。
        <ul>
          <li><a href="https://help.salesforce.com/s/articleView?id=sf.code_manage_triggers.htm&amp;type=5">Apexトリガー</a>
          </li>
          <li><a href="https://admin.salesforce.com/blog/2023/what-is-a-record-triggered-flow#:~:text=A%20record%2Dtriggered%20flow%20allows,is%20created%20and%2For%20updated">フロートリガー</a>
          </li>
        </ul>
        <p>
        に必要なすべての権限を指定します。 <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Marketo Measureユーザー</a>.
      </td>
    </tr>
    <tr>
      <td>DUPLICATES_DETECTED</td>
      <td>CRM エクスポート中にエラーが発生しました： DUPLICATES_DETECTED ：エンティティタイプ「連絡先」: CRM ErrorCode : DUPLICATES_DETECTED, CRM ErrorMessage ：重複レコードを作成しています。 代わりに既存のレコードを使用することをお勧めします。RecordId: 0123456</td>
      <td>Salesforce 組織にインポートされるレコードは既に存在します。</td>
      <td><a href="https://help.salesforce.com/s/articleView?id=000390009&amp;type=1">「ルールの複製」設定を無効にする</a> 重複を許可する場合。
          <p>
          Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.</td>
    </tr>
    <tr>
      <td>DUPLICATE_VALUE</td>
      <td>CRM エクスポート中にエラーが発生しました： DUPLICATE_VALUE ：エンティティタイプ「リード」: CRM ErrorCode : DUPLICATE_VALUE、CRM ErrorMessage ：重複値が見つかりました： Email_Unique__c ID: 456 のレコードの値を複製します</td>
      <td>Salesforce 組織にインポートされるフィールドでは、値の重複は許可されていません。</td>
      <td>をオフにします。 <a href="https://help.salesforce.com/s/articleView?id=000390009&amp;type=1">"一意のチェックボックス"</a> Salesforce 内。
          <p>
          Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.</td>
    </tr>
    <tr>
      <td>ENTITY_IS_LOCKED</td>
      <td>CRM エクスポート中にエラーが発生しました： ENTITY_IS_LOCKED ：エンティティタイプ「アカウント」: CRM エラーコード： ENTITY_IS_LOCKED、CRM ErrorMessage ：このレコードはロックされています。 編集が必要な場合は、管理者にお問い合わせください。RecordId: 0123456</td>
      <td>レコードが承認プロセス中で、現在の承認者またはシステム管理者以外のユーザーがレコードの編集を試みます。</td>
      <td>
        <ul>
          <li>Salesforce 組織内のそのレコードの保留中の承認プロセスを解決します。</li>
          <li>Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>FIELD_FILTER_VALIDATION_EXCEPTION</td>
      <td>CRM エクスポート中にエラーが発生しました： FIELD_FILTER_VALIDATION_EXCEPTION ：エンティティタイプ「リード」: CRM エラーコード： FIELD_FILTER_VALIDATION_EXCEPTION、フィールド： User__C、CRM ErrorMessage：値が存在しないか、フィルター条件に一致しません。 「アカウントエグゼクティブ、インサイドセールス」の役割を持つユーザーを選択してください。RecordId: 0123456</td>
      <td>変更されたレコードが、オブジェクトで定義された参照フィルターを満たさなくなりました。</td>
      <td>Marketo Measureが変更しようとしているオブジェクトに対するフィルターを確認します。 詳しくは、 <a href="https://help.salesforce.com/s/articleView?id=000384756&amp;type=1">この Salesforce 記事</a> を参照してください。</td>
    </tr>
    <tr>
      <td>FIELD_INTEGRITY_EXCEPTION</td>
      <td>CRM エクスポート中にエラーが発生しました： FIELD_INTEGRITY_EXCEPTION ：エンティティタイプ'Lead': CRM ErrorCode: FIELD_INTEGRITY_EXCEPTION，フィールド：国、CRM ErrorMessage ：正しく表示されているにもかかわらず、この国に問題があります。 有効な国のリストから国/地域を選択してください。：国、レコード ID:0123456</td>
      <td>期待されたレコードのタイプが一致しません。</td>
      <td>最も一般的な例は、Salesforce 組織で設定された都道府県/国の命名規格に従っていないことです。これは、[ 州/国 ] フィールドが特定のピックリスト値のみを受け入れるように標準化されているからです。 この問題に対処するには、次の操作を行います。
        <ul>
          <li>レコードを更新して、そのフィールドで組織が受け入れた値に従います。 SFDC 管理者に問い合わせて、受け入れられた値のリストを取得してください。</li>
          <li><a href="https://help.salesforce.com/s/articleView?id=sf.admin_state_country_picklist_enable.htm&amp;type=5">都道府県/国の選択リストを無効にする</a>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>INACTIVE_OWNER_OR_USER</td>
      <td>CRM エクスポート中にエラーが発生しました： INACTIVE_OWNER_OR_USER ：エンティティタイプ「連絡先」: CRM ErrorCode : INACTIVE_OWNER_OR_USER, CRM ErrorMessage ：非アクティブなユーザー [1234] を連絡先所有者として実行した操作、RecordId: 0123456</td>
      <td>Marketo Measureに「非アクティブな所有者でレコードを更新」権限がありません。</td>
      <td>Marketo Measureに「<a href="https://help.salesforce.com/s/articleView?id=000386699&amp;type=1">非アクティブな所有者でレコードを更新</a>"権限。</td>
    </tr>
    <tr>
      <td>INSUFFICIENT_ACCESS_OR_READONLY</td>
      <td>CRM エクスポート中にエラーが発生しました： INSUFFICIENT_ACCESS_OR_READONLY ：エンティティタイプ「アカウント」: CRM ErrorCode : INSUFFICIENT_ACCESS_OR_READONLY, CRM ErrorMessage ：オブジェクト ID: [123]、RecordId: 456</td>
      <td>Marketo Measureにはオブジェクト/フィールドに対する権限がないか、オブジェクトが読み取り専用です。</td>
      <td>次を参照してください。 <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">Experience League記事</a> Marketo Measureに必要な権限に関するガイダンスを参照してください。</td>
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
      <td>MISSING_BIZIBLE_CUSTOM_FIELDS_PERMISSIONS</td>
      <td>CRM エクスポート中にエラーが発生しました： MISSING_BIZIBLE_CUSTOM_FIELDS_PERMISSIONS ：エンティティタイプ「キャンペーン」: CRM エラーコード： INVALID_FIELD_FOR_INSERT_UPDATE、フィールド： bizible2__UniqueId__c、CRM エラーメッセージ：フィールドを作成/更新するには： bizible2__UniqueId__c.このフィールドのセキュリティ設定を確認し、お使いのプロファイルまたは権限セットに対して読み取り/書き込みが行われていることを確認してください。</td>
      <td>Marketo Measureは bizible フィールドに対する権限がありません。</td>
      <td>「bizible2__」というプレフィックスが付いたすべてのフィールドに対する読み取りおよび書き込み権限が必要です。 これらのフィールドの完全なリストは、次のとおりです。 <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">この記事では、</a>.</td>
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
      <td>MISSING_RECORD_OBJECT_PERMISSIONS</td>
      <td>CRM エクスポート中にエラーが発生しました： MISSING_RECORD_OBJECT_PERMISSIONS ：エンティティタイプ'bizible2__Bizible_Touchpoint__c': CRM エラーコード： INSUFFICIENT_ACCESS_ON_CROSS_REFERENCE_ENTITY，フィールド：アカウント、CRM ErrorMessage：相互参照 id のアクセス権：0123456</td>
      <td>Marketo Measureに権限がありません。</td>
      <td>このエラーには、Salesforce 組織に固有の理由がいくつかあります。 この問題を解決できる一般的なトラブルシューティング手順を以下にいくつか示します。
        <ul>
          <li>それぞれに必要なすべての権限を確認する <a href="/help/configuration-and-setup/marketo-measure-and-salesforce/how-marketo-measure-and-salesforce-interact.md">オブジェクトとフィールド</a>.</li>
          <li>Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.</li>
          <li>Marketo Measure "を付与<a href="https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/users_profiles_view_all_mod_all.htm">すべて修正</a>"権限。</li>
        </ul>
      </td>
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
      <td>RECORD_NONCOMPLIANT_WITH_VALIDATION_RULES</td>
      <td>CRM エクスポート中にエラーが発生しました： RECORD_NONCOMPLIANT_WITH_VALIDATION_RULES ：エンティティタイプ「リード」: CRM エラーコード： FIELD_CUSTOM_VALIDATION_EXCEPTION、フィールド： Lead_Status_Reason__c、CRMErrorMessage：リードステータスを選択する必要があります理由、レコード ID: 0123456</td>
      <td>更新中のレコードは、Salesforce 組織の検証ルールセットを満たしていません。</td>
      <td>Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.
      <p>
      を更新します。 <a href="https://help.salesforce.com/s/articleView?id=sf.fields_about_field_validation.htm&amp;type=5">検証ルール</a>.</td>
    </tr>
    <tr>
      <td>RESTRICT_PICKLIST_VALUES_ENABLED</td>
      <td>CRM エクスポート中にエラーが発生しました： RESTRICT_PICKLIST_VALUES_ENABLED ：エンティティタイプ「Campaign」: CRM ErrorCode : INVALID_OR_NULL_FOR_RESTRICTED_PICKLIST、フィールド： Areas_of_Interest__c、CRMErrorMessage：制限された値リストフィールド：不明</td>
      <td>選択リストフィールドの設定で「選択リストを値セットで定義された値に制限」が有効になっている場合、またはフィールドに挿入される値は、オブジェクトのレコードタイプで使用できません。</td>
      <td>Salesforce 組織の制限候補リスト設定を無効にします。
          <p>
          Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.
      </td>
    </tr>
    <tr>
      <td>REQUIRED_FIELD_MISSING</td>
      <td>CRM エクスポート中にエラーが発生しました： MISSING_REQUIRED_FIELD ：エンティティタイプ「リード」: CRM ErrorCode : REQUIRED_FIELD_MISSING，フィールド： Product_Type__c, CRM ErrorMessage ：必須フィールドが見つかりません： [Product_Type__c],Id:</td>
      <td>検証ルールがオブジェクトの必須フィールドを指定する場合。</td>
      <td>Marketo Measureの専用ユーザーの除外先 <a href="https://trailhead.salesforce.com/content/learn/modules/validation-rules/bypass-your-validation-rules">カスタム検証ルール</a>.
      </td>
    </tr>
    <tr>
      <td>UNKNOWN_EXCEPTION</td>
      <td>CRM エクスポート中にエラーが発生しました： UNKNOWN_EXCEPTION ：エンティティタイプ「連絡先」 : CRM エラーコード：UNKNOWN_EXCEPTION、CRM エラーメッセージ：ポータルユーザーがパートナーアカウントを所有できない、レコード ID : 0123456</td>
      <td>Salesforce で未処理の例外が発生しました。</td>
      <td>問題が解決しない場合は、Salesforce に問題を報告し、エラーメッセージに数値をコピーします。</td>
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
