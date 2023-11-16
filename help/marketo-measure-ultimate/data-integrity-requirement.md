---
description: '''[!DNL Marketo Measure] 究極のデータ整合性要件 — [!DNL Marketo Measure]  — 製品ドキュメント`'
title: '''[!DNL Marketo Measure] 究極のデータ整合性要件`'
hide: true
hidefromtoc: true
feature: Integration, Tracking, Attribution
source-git-commit: 3725ef14f90269ebdada1d81692f3b7283e6ec6e
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 22%

---

# [!DNL Marketo Measure] 究極のデータ整合性要件 {#marketo-measure-ultimate-data-integrity-requirement}

[!DNL Marketo Measure] は、受信 AEP データセットを検証し、データが属性の目的で十分で一貫性があることを確認します。 データの整合性要件を満たさないと、 [!DNL Marketo Measure] システム。 このドキュメントでは、データの整合性要件の詳細を説明し、データ検査のクエリ例を示し、null 値を持つ必須フィールドに対する解決策を推奨します。

## エンティティオブジェクト {#entity-object}

<table>
  <tr>
    <th>XDM クラス</th>
    <th>XDM フィールドグループ</th>
    <th>XDM パス</th>
    <th>XDM タイプ</th>
    <th>データソースフィールド</th>
    <th>必須?</th>
    <th>注意</th>
  </tr>
  <tbody>
    <tr>
      <td colspan="7"><strong>アカウント</strong> (Marketoの Salesforce、会社、特定アカウントのアカウント )</td>
    </tr>
    <tr>
      <td rowspan="6">XDM ビジネスアカウント</td>
      <td></td>
      <td>accountKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 123@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 123</td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>XDM ビジネスアカウントの詳細</td>
      <td>accountName</td>
      <td>文字列</td>
      <td>名前</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="7"><strong>Campaign</strong> (Salesforce 用キャンペーン、Marketo用プログラム )</td>
    </tr>
    <tr>
      <td rowspan="8">XDM ビジネスキャンペーン</td>
      <td></td>
      <td>campaignKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 55555@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 55555</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>campaignName</td>
      <td>文字列</td>
      <td>名前</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>campaignType</td>
      <td>文字列</td>
      <td>CampaignType</td>
      <td>いいえ</td>
      <td>チャネルマッピングの場合</td>
    </tr>
    <tr>
      <td></td>
      <td rowspan="5">XDM ビジネスキャンペーンの詳細</td>
      <td>channelName</td>
      <td>文字列</td>
      <td>ChannelName</td>
      <td>いいえ</td>
      <td>チャネルマッピングの場合</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignStartDate</td>
      <td>date-time</td>
      <td>StartDate</td>
      <td>いいえ</td>
      <td>キャンペーンコスト</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignEndDate</td>
      <td>date-time</td>
      <td>EndDate</td>
      <td>いいえ</td>
      <td>キャンペーンコスト</td>
    </tr>
    <tr>
      <td></td>
      <td>actualCost.amount</td>
      <td>number</td>
      <td>コスト</td>
      <td>いいえ</td>
      <td>キャンペーンコスト</td>
    </tr>
    <tr>
      <td></td>
      <td>actualCost.currencyCode</td>
      <td>
        <p>文字列</p>
        <p>^[A-Z]{3}$</p>
      </td>
      <td>CurrencyIsoCode</td>
      <td>いいえ</td>
      <td>キャンペーンコスト</td>
    </tr>
    <tr>
      <td colspan="7"><strong>キャンペーンメンバー</strong> (Salesforce のキャンペーンメンバー、Marketoのプログラムメンバーシップ )</td>
    </tr>
    <tr>
      <td rowspan="14">XDM ビジネスキャンペーンメンバー</td>
      <td></td>
      <td>campaignMemberKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 987654321@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignMemberKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 987654321</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignMemberKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignMemberKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 333@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceID</td>
      <td>文字列</td>
      <td>リード ID または連絡先 ID</td>
      <td>はい</td>
      <td>
        <p>例： - 333（データソーステーブルに応じて、リード ID または連絡先 ID）。</p>
        <p>リードまたは連絡先への外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 55555@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceID</td>
      <td>文字列</td>
      <td>キャンペーン ID</td>
      <td>はい</td>
      <td>
        <p>例： - 55555。</p>
        <p>キャンペーンの外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>campaignKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td rowspan="4">XDM ビジネスキャンペーンメンバーの詳細</td>
      <td>b2b.personType</td>
      <td>文字列</td>
      <td>"リード"または"連絡先"</td>
      <td>はい</td>
      <td>データソーステーブルに応じて、「リード」または「連絡先」に設定する必要があります。 ほとんどの使用例では、この値を「連絡先」に設定することをお勧めします</td>
    </tr>
    <tr>
      <td></td>
      <td>memberStatus</td>
      <td>文字列</td>
      <td>ステータス</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>hasRelponed</td>
      <td>boolean</td>
      <td>HasRelponed</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>firstRelponedDate</td>
      <td>date-time</td>
      <td>FirstRespondedDate</td>
      <td>いいえ</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="7"><strong>人物</strong> (Salesforce の連絡先またはリード、Marketoの担当者 )</td>
    </tr>
    <tr>
      <td>XDM 個人プロファイル</td>
      <td rowspan="11">XDM ビジネス人物の詳細</td>
      <td>b2b.personKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 333@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.personKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 333（データソーステーブルに応じて、リード ID または連絡先 ID になります）</td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.personKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.personKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>workEmail.address</td>
      <td>
        <p>文字列</p>
        <p>メール</p>
      </td>
      <td>メール</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.personStatus</td>
      <td>文字列</td>
      <td>ステータス</td>
      <td>リードの担当者タイプのみはい</td>
      <td>b2b.personType が「リード」の場合にのみ必要です</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.isConverted</td>
      <td>boolean</td>
      <td>IsConverted</td>
      <td>リードの担当者タイプのみはい</td>
      <td>b2b.personType が「リード」の場合にのみ必要です</td>
    </tr>
    <tr>
      <td></td>
      <td>b2b.personType</td>
      <td>文字列</td>
      <td>"リード"または"連絡先"</td>
      <td>はい</td>
      <td>データソーステーブルに応じて、「リード」または「連絡先」に設定する必要があります。 ほとんどの使用例では、この値を「連絡先」に設定することをお勧めします</td>
    </tr>
    <tr>
      <td></td>
      <td>extendedWorkDetails.jobTitle</td>
      <td>文字列</td>
      <td></td>
      <td>いいえ</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td rowspan="4">XDM ビジネス人物コンポーネント</td>
      <td>personComponents.sourceAccountKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>いいえ</td>
      <td>
        <p>例： - 123@999-abc-888.Marketo。</p>
        <p>sourceAccountKey フィールドのセットは、真の連絡先レコード（アカウントにリンクされた担当者レコードとして定義）に対してのみ「必須」です。 見つからない場合は、データセットは拒否されませんが、アトリビューションの結果は表示されません。</p>
        <p>personComponents は配列ですが、Marketo Measureは最初の要素 personComponents[0] のみを取ります</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>personComponents.sourceAccountKey.sourceID</td>
      <td>文字列</td>
      <td>アカウント ID</td>
      <td>いいえ</td>
      <td>
        <p>例： - 123。</p>
        <p>外部キーからアカウントへ</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>personComponents.sourceAccountKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>いいえ</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>personComponents.sourceAccountKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>いいえ</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td colspan="7"><strong>商談</strong> (Salesforce の商談、Marketoの商談 )</td>
    </tr>
    <tr>
      <td rowspan="13">XDM ビジネスオポチュニティ</td>
      <td></td>
      <td>opportunityKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 77777@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 77777</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 123@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceID</td>
      <td>文字列</td>
      <td>アカウント ID</td>
      <td>はい</td>
      <td>
        <p>例： - 123。</p>
        <p>外部キーからアカウントへ</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>accountKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityName</td>
      <td>文字列</td>
      <td>名前</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityStage</td>
      <td>文字列</td>
      <td>ステージ</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityType</td>
      <td>文字列</td>
      <td></td>
      <td>いいえ</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td rowspan="5">XDM ビジネスオポチュニティの詳細</td>
      <td>isWon</td>
      <td>boolean</td>
      <td>IsWon</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>isClosed</td>
      <td>boolean</td>
      <td>IsClosed</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>expectedCloseDate</td>
      <td>日</td>
      <td>CloseDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityAmount.amount</td>
      <td>number</td>
      <td>金額</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityAmount.currencyCode</td>
      <td>
        <p>文字列</p>
        <p>^[A-Z]{3}$</p>
      </td>
      <td>CurrencyIsoCode</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="7"><strong>商談連絡先の役割（商談連絡先の役割を属性の購買グループとして使用する計画の場合にのみ必要）</strong></td>
    </tr>
    <tr>
      <td rowspan="16">XDM ビジネスオポチュニティ人物関係</td>
      <td></td>
      <td>personKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 333@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceID</td>
      <td>文字列</td>
      <td>取引先責任者 ID</td>
      <td>はい</td>
      <td>
        <p>例： - 333。</p>
        <p>連絡先への外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>personKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>isPrimary</td>
      <td>boolean</td>
      <td>IsPrimary</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 77777@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceID</td>
      <td>文字列</td>
      <td>商談 ID</td>
      <td>はい</td>
      <td>
        <p>例： - 77777。</p>
        <p>商談に対する外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityPersonKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 222222@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityPersonKey.sourceID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 222222</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityPersonKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td>opportunityPersonKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>personRole</td>
      <td>文字列</td>
      <td>ロール</td>
      <td>いいえ</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td colspan="7"><strong>コンバージョン率 ( 複数の通貨を使用する場合にのみ必要。Marketo Measureに対して有効化できるコンバージョン率データセットは 1 つだけです )</strong></td>
    </tr>
    <tr>
      <td rowspan="7">コンバージョン</td>
      <td></td>
      <td>extSourceSystemAudit.externalKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 8888@0x012345.Salesforce</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.externalKey.sourceId</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>例： - 8888</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.externalKey.sourceInstanceId</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 0x012345</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.externalKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： Salesforce</td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.createdDate</td>
      <td>date-time</td>
      <td>CreatedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>extSourceSystemAudit.lastUpdatedDate</td>
      <td>date-time</td>
      <td>ModifiedDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>isDeleted</td>
      <td>boolean</td>
      <td></td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td rowspan="5">通貨換算レートの詳細</td>
      <td>conversionRate</td>
      <td>number</td>
      <td>ConversionRate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>endDate</td>
      <td>日</td>
      <td>NextStartDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>startDate</td>
      <td>日</td>
      <td>StartDate</td>
      <td>はい</td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td>sourceISOCode</td>
      <td>文字列</td>
      <td>ISOCode</td>
      <td>はい</td>
      <td>例： EUR</td>
    </tr>
    <tr>
      <td></td>
      <td>targetISOCode</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>Marketo Measureで設定されたデフォルトの通貨コード（USD など）</td>
    </tr>
  </tbody>
</table>

## ExperienceEvent {#experienceevent}

<table style="table-layout:auto">
  <tr>
    <th>XDM クラス</th>
    <th>XDM フィールドグループ</th>
    <th>XDM パス</th>
    <th>XDM タイプ</th>
    <th>データソースフィールド</th>
    <th>必須?</th>
    <th>注意</th>
  </tr>
  <tbody>
    <tr>
      <td colspan="7"><strong>アクティビティ</strong></td>
    </tr>
    <tr>
      <td rowspan="3">XDM ExperienceEvent</td>
      <td></td>
      <td>_ID</td>
      <td>文字列</td>
      <td>ID</td>
      <td>はい</td>
      <td>はい</td>
    </tr>
    <tr>
      <td></td>
      <td>eventType</td>
      <td>文字列</td>
      <td>ActivityType</td>
      <td>はい</td>
      <td>はい</td>
    </tr>
    <tr>
      <td></td>
      <td>timestamp</td>
      <td>date-time</td>
      <td>アクティビティ日</td>
      <td>はい</td>
      <td>はい</td>
    </tr>
    <tr>
      <td></td>
      <td>人物識別子</td>
      <td>personKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 333@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>personKey.sourceID</td>
      <td>文字列</td>
      <td>リード ID または連絡先 ID</td>
      <td>はい</td>
      <td>
        <p>例： - 333（データソーステーブルに応じて、リード ID または連絡先 ID）。</p>
        <p>リードまたは連絡先への外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>personKey.sourceInstanceID</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>personKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>はい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>キャンペーンに追加</td>
      <td>leadOperation.addToCampaign.campaignKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.addToCampaign タイプのみはい</td>
      <td>例： - 55555@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.addToCampaign.campaignKey.sourceId</td>
      <td>文字列</td>
      <td>キャンペーン ID</td>
      <td>leadOperation.addToCampaign タイプのみはい</td>
      <td>
        <p>例： - 55555。</p>
        <p>キャンペーンの外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.addToCampaign.campaignKey.sourceInstanceId</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.addToCampaign タイプのみはい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.addToCampaign.campaignKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.addToCampaign タイプのみはい</td>
      <td>例： - Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td>キャンペーン進行のステータス変更済み</td>
      <td>leadOperation.campaignProgression.campaignKey.sourceKey</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.campaignProgression タイプのみはい</td>
      <td>例： - 55555@999-abc-888.Marketo</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.campaignProgression.campaignKey.sourceId</td>
      <td>文字列</td>
      <td>キャンペーン ID</td>
      <td>leadOperation.campaignProgression タイプのみはい</td>
      <td>
        <p>例： - 55555。</p>
        <p>キャンペーンの外部キー</p>
      </td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.campaignProgression.campaignKey.sourceInstanceId</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.campaignProgression タイプのみはい</td>
      <td>例： - 999-abc-888</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>leadOperation.campaignProgression.campaignKey.sourceType</td>
      <td>文字列</td>
      <td></td>
      <td>leadOperation.campaignProgression タイプのみはい</td>
      <td>例： - Marketo</td>
    </tr>
  </tbody>
</table>

## サポートされる ExperienceEvent タイプ {#experienceevent-type-supported}

<table>
  <tr>
    <th>イベントタイプ</th>
    <th>XDM イベントタイプ</th>
    <th>説明</th>
  </tr>
  <tbody>
    <tr>
      <td>新規リード</td>
      <td>leadOperation.newLead</td>
      <td>新しいマーケティングリードの作成と詳細の記録に使用します</td>
    </tr>
    <tr>
      <td>リードのコンバート</td>
      <td>leadOperation.convertLead</td>
      <td>マーケティングリードが、セールスユーザーに割り当てられたセールス資格を持つ連絡先に変換される場合に使用します</td>
    </tr>
    <tr>
      <td>注目のアクション</td>
      <td>leadOperation.interestingMoment</td>
      <td>見込み客による高価値のアクティビティの追跡に使用</td>
    </tr>
    <tr>
      <td>フォームの入力</td>
      <td>web.formFilledOut</td>
      <td>人物が Web ページ上のフォームに入力する際に、詳細をキャプチャするために使用します</td>
    </tr>
    <tr>
      <td>メールの配信停止</td>
      <td>directMarketing.emailUnsubscribed</td>
      <td>人物が電子メールから購読解除する際に、詳細をキャプチャするために使用します</td>
    </tr>
    <tr>
      <td>メールを開く</td>
      <td>directMarketing.emailOpened</td>
      <td>人物がマーケティング電子メールを開く際に、詳細をキャプチャするために使用します</td>
    </tr>
    <tr>
      <td>メールをクリック</td>
      <td>directMarketing.emailClicked</td>
      <td>人物がマーケティング電子メール内のリンクをクリックする際に、詳細をキャプチャするために使用します</td>
    </tr>
    <tr>
      <td>進行状況のステータスの変更</td>
      <td>leadOperation.statusInCampaignProgressionChanged</td>
      <td>キャンペーンでのリードのステータスが変更された際に、詳細をキャプチャするために使用します</td>
    </tr>
    <tr>
      <td>エンゲージメントプログラムに追加（育成に追加）</td>
      <td>leadOperation.addToCampaign</td>
      <td>特定のキャンペーンに人を追加する場合に使用します。</td>
    </tr>
  </tbody>
</table>

上記の表でサポートされていないイベントタイプに対して、「注目のアクション」イベントタイプを使用します。 サブタイプ「注目のアクション」を示すカスタムフィールドを追加します。

## データ検査のクエリ例 {#query-examples-for-data-inspection}

次に、AEP データレイクで取り込んだデータセットを検査するクエリの例を示します。 データセットに対して使用するには、以下のクエリ例にあるテーブル名を、実際のデータセットテーブル名に置き換えます。

すべてのカウントは 0 になると予想されます。

personType フィールドには、「リード」または「連絡先」の値のみが存在し、null 値は存在しないと想定します。

すべての「連絡先」担当者レコードに対して、アカウント外部キーが存在すると想定します。

「リード」担当者レコードの場合、アカウント外部キーは存在せず、必須ではありません。 「リード」担当者レコードを「連絡先」担当者レコード（推奨）として取り込む場合、その担当者レコードのアカウント外部キーは不要です。

### XDM ビジネスアカウント {#xdm-business-account}

```
select 'account source id', count(*) from salesforce_account where accountKey.sourceId is null
union all
select 'account source type', count(*) from salesforce_account where accountKey.sourceType is null
union all
select 'account source instance id', count(*) from salesforce_account where accountKey.sourceInstanceId is null
union all
select 'account source key', count(*) from salesforce_account where accountKey.sourceKey is null
union all
select 'account name', count(*) from salesforce_account where accountName is null
union all
select 'created date', count(*) from salesforce_account where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_account where extSourceSystemAudit.lastUpdatedDate is null;
```

### XDM ビジネスキャンペーン {#xdm-business-campaign}

```
select 'campaign source id', count(*) from salesforce_campaign where campaignKey.sourceId is null
union all
select 'campaign source type', count(*) from salesforce_campaign where campaignKey.sourceType is null
union all
select 'campaign source instance id', count(*) from salesforce_campaign where campaignKey.sourceInstanceId is null
union all
select 'campaign source key', count(*) from salesforce_campaign where campaignKey.sourceKey is null
union all
select 'campaign name', count(*) from salesforce_campaign where campaignName is null
union all
select 'created date', count(*) from salesforce_campaign where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_campaign where extSourceSystemAudit.lastUpdatedDate is null;
```

### XDM ビジネスキャンペーンメンバー {#xdm-business-campaign-member}

```
select 'campaign member source id', count(*) from salesforce_campaign_member where campaignMemberKey.sourceId is null
union all
select 'campaign member source type', count(*) from salesforce_campaign_member where campaignMemberKey.sourceType is null
union all
select 'campaign member source instance id', count(*) from salesforce_campaign_member where campaignMemberKey.sourceInstanceId is null
union all
select 'campaign member source key', count(*) from salesforce_campaign_member where campaignMemberKey.sourceKey is null
union all
select 'campaign source id', count(*) from salesforce_campaign_member where campaignKey.sourceId is null
union all
select 'campaign source type', count(*) from salesforce_campaign_member where campaignKey.sourceType is null
union all
select 'campaign source instance id', count(*) from salesforce_campaign_member where campaignKey.sourceInstanceId is null
union all
select 'campaign source key', count(*) from salesforce_campaign_member where campaignKey.sourceKey is null
union all
select 'person source id', count(*) from salesforce_campaign_member where personKey.sourceId is null
union all
select 'person source type', count(*) from salesforce_campaign_member where personKey.sourceType is null
union all
select 'person source instance id', count(*) from salesforce_campaign_member where personKey.sourceInstanceId is null
union all
select 'person source key', count(*) from salesforce_campaign_member where personKey.sourceKey is null
union all
select distinct 'person type', b2b.personType from salesforce_campaign_member
union all
select 'member status', count(*) from salesforce_campaign_member where memberStatus is null
union all
select 'has responded', count(*) from salesforce_campaign_member where hasResponded is null
union all
select 'created date', count(*) from salesforce_campaign_member where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_campaign_member where extSourceSystemAudit.lastUpdatedDate is null;
```

### XDM ビジネス担当者 {#xdm-business-person}

```
select 'person source id', count(*) from marketo_person where b2b.personKey.sourceId is null
union all
select 'person source type', count(*) from marketo_person where b2b.personKey.sourceType is null
union all
select 'person source instance id', count(*) from marketo_person where b2b.personKey.sourceInstanceId is null
union all
select 'person source key', count(*) from marketo_person where b2b.personKey.sourceKey is null
union all
select 'email', count(*) from marketo_person where workEmail.address is null
union all
select 'Lead - person status', count(*) from marketo_person where b2b.personType = 'Lead' and b2b.personStatus is null
union all
select 'Lead - is converted', count(*) from marketo_person where b2b.personType = 'Lead' and b2b.isConverted is null
union all
select distinct 'person type', b2b.personType from marketo_person
union all
select 'created date', count(*) from marketo_person where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from marketo_person where extSourceSystemAudit.lastUpdatedDate is null;
```

```
select 'person source id', count(*) from salesforce_contact where b2b.personKey.sourceId is null
union all
select 'person source type', count(*) from salesforce_contact where b2b.personKey.sourceType is null
union all
select 'person source instance id', count(*) from salesforce_contact where b2b.personKey.sourceInstanceId is null
union all
select 'person source key', count(*) from salesforce_contact where b2b.personKey.sourceKey is null
union all
select 'email', count(*) from salesforce_contact where workEmail.address is null
union all
select 'Lead - person status', count(*) from salesforce_contact where b2b.personType = 'Lead' and b2b.personStatus is null
union all
select 'Lead - is converted', count(*) from salesforce_contact where b2b.personType = 'Lead' and b2b.isConverted is null
union all
select distinct 'person type', b2b.personType from salesforce_contact
union all
select 'account source id', count(*) from salesforce_contact where b2b.personType = 'Contact' and personComponents[0].sourceAccountKey.sourceId is null
union all
select 'account source type', count(*) from salesforce_contact where b2b.personType = 'Contact' and personComponents[0].sourceAccountKey.sourceType is null
union all
select 'account source instance id', count(*) from salesforce_contact where b2b.personType = 'Contact' and personComponents[0].sourceAccountKey.sourceInstanceId is null
union all
select 'account source key', count(*) from salesforce_contact where b2b.personType = 'Contact' and personComponents[0].sourceAccountKey.sourceKey is null
union all
select 'created date', count(*) from salesforce_contact where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_contact where extSourceSystemAudit.lastUpdatedDate is null;
```

### XDM ビジネスオポチュニティ {#xdm-business-opportunity}

```
select 'opportunity source id', count(*) from salesforce_opportunity where opportunityKey.sourceId is null
union all
select 'opportunity source type', count(*) from salesforce_opportunity where opportunityKey.sourceType is null
union all
select 'opportunity source instance id', count(*) from salesforce_opportunity where opportunityKey.sourceInstanceId is null
union all
select 'opportunity source key', count(*) from salesforce_opportunity where opportunityKey.sourceKey is null
union all
select 'account source id', count(*) from salesforce_opportunity where accountKey.sourceId is null
union all
select 'account source type', count(*) from salesforce_opportunity where accountKey.sourceType is null
union all
select 'account source instance id', count(*) from salesforce_opportunity where accountKey.sourceInstanceId is null
union all
select 'account source key', count(*) from salesforce_opportunity where accountKey.sourceKey is null
union all
select 'opportunity name', count(*) from salesforce_opportunity where opportunityName is null
union all
select 'opportunity stage', count(*) from salesforce_opportunity where opportunityStage is null
union all
select 'is won', count(*) from salesforce_opportunity where isWon is null
union all
select 'is closed', count(*) from salesforce_opportunity where isClosed is null
union all
select 'expected close date', count(*) from salesforce_opportunity where expectedCloseDate is null
union all
select 'opportunity amount', count(*) from salesforce_opportunity where opportunityAmount.amount is null
union all
select 'currency code', count(*) from salesforce_opportunity where opportunityAmount.currencyCode is null
union all
select 'created date', count(*) from salesforce_opportunity where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_opportunity where extSourceSystemAudit.lastUpdatedDate is null;
```

### XDM ExperienceEvent {#xdm-experienceevent}

```
select 'id', count(*) from marketo_activity where _id is null
union all
select 'event type', count(*) from marketo_activity where eventType is null
union all
select 'timestamp', count(*) from marketo_activity where timestamp is null
union all
select 'person source id', count(*) from marketo_activity where personKey.sourceId is null
union all
select 'person source type', count(*) from marketo_activity where personKey.sourceType is null
union all
select 'person source instance id', count(*) from marketo_activity where personKey.sourceInstanceId is null
union all
select 'person source key', count(*) from marketo_activity where personKey.sourceKey is null
union all
select 'addToCampaign campaign id', count(*) from marketo_activity where eventType = 'leadOperation.addToCampaign' and leadOperation.addToCampaign.campaignKey.sourceId is null
union all
select 'addToCampaign campaign type', count(*) from marketo_activity where eventType = 'leadOperation.addToCampaign' and leadOperation.addToCampaign.campaignKey.sourceType is null
union all
select 'addToCampaign campaign instance id', count(*) from marketo_activity where eventType = 'leadOperation.addToCampaign' and leadOperation.addToCampaign.campaignKey.sourceInstanceId is null
union all
select 'addToCampaign campaign key', count(*) from marketo_activity where eventType = 'leadOperation.addToCampaign' and leadOperation.addToCampaign.campaignKey.sourceKey is null
union all
select 'statusInCampaignProgressionChanged campaign id', count(*) from marketo_activity where eventType = 'leadOperation.campaignProgression.campaignKey.sourceKey' and leadOperation.campaignProgression.campaignKey.sourceId is null
union all
select 'statusInCampaignProgressionChanged campaign type', count(*) from marketo_activity where eventType = 'leadOperation.campaignProgression.campaignKey.sourceKey' and leadOperation.campaignProgression.campaignKey.sourceType is null
union all
select 'statusInCampaignProgressionChanged campaign instance id', count(*) from marketo_activity where eventType = 'leadOperation.campaignProgression.campaignKey.sourceKey' and leadOperation.campaignProgression.campaignKey.sourceInstanceId is null
union all
select 'statusInCampaignProgressionChanged campaign key', count(*) from marketo_activity where eventType = 'leadOperation.campaignProgression.campaignKey.sourceKey' and leadOperation.campaignProgression.campaignKey.sourceKey is null;
```

```
select 'id', count(*) from salesforce_task where _id is null
union all
select 'event type', count(*) from salesforce_task where eventType is null
union all
select 'timestamp', count(*) from salesforce_task where timestamp is null
union all
select 'person source id', count(*) from salesforce_task where personKey.sourceId is null
union all
select 'person source type', count(*) from salesforce_task where personKey.sourceType is null
union all
select 'person source instance id', count(*) from salesforce_task where personKey.sourceInstanceId is null
union all
select 'person source key', count(*) from salesforce_task where personKey.sourceKey is null;
```

### コンバージョン {#conversion}

```
select 'conversion rate', count(*) from currency_conversion_rate where conversionRate is null
union all
select 'end date', count(*) from currency_conversion_rate where endDate is null
union all
select 'start date', count(*) from currency_conversion_rate where startDate is null
union all
select 'source ISO Code', count(*) from currency_conversion_rate where sourceISOCode is null
union all
select 'target ISO Code', count(*) from currency_conversion_rate where targetISOCode is null
union all
select 'source id', count(*) from currency_conversion_rate where extSourceSystemAudit.externalKey.sourceId is null
union all
select 'source type', count(*) from currency_conversion_rate where extSourceSystemAudit.externalKey.sourceType is null
union all
select 'source instance id', count(*) from currency_conversion_rate where extSourceSystemAudit.externalKey.sourceInstanceId is null
union all
select 'source key', count(*) from currency_conversion_rate where extSourceSystemAudit.externalKey.sourceKey is null
union all
select 'created date', count(*) from salesforce_contact where extSourceSystemAudit.createdDate is null
union all
select 'last updated date', count(*) from salesforce_contact where extSourceSystemAudit.lastUpdatedDate is null;
```

## NULL 値を持つ必須フィールドに対する推奨ソリューション {#recommended-solution-for-required-fields-with-a-null-value}

フィールドマッピングで計算フィールドを使用して、フィールドをデフォルトで NULL 以外の値に設定することをお勧めします。 次に 2 つの例を示します。

* 一部のオポチュニティレコードの opportunityName が null の場合は、次の計算フィールドをフィールドマッピングで作成して使用します
   * `iif(name != null && name != "", name, "Unknown")`

* 一部の experienceevent レコードの leadOperation.campaignProgression.campaignID が null の場合は、フィールドマッピングで次の計算フィールドを作成して使用します
   * `iif(leadOperation.campaignProgression.campaignID != null && leadOperation.campaignProgression.campaignID != "" , to_object("sourceType", "Marketo", "sourceInstanceID", "123-abc-321", "sourceID", leadOperation.campaignProgression.campaignID, "sourceKey", concat(leadOperation.campaignProgression.campaignID,"@123-abc-321.Marketo")), iif(eventType == "leadOperation.statusInCampaignProgressionChanged", to_object("sourceType", "Marketo", "sourceInstanceID", "123-abc-321", "sourceID", "Unknown", "sourceKey", "Unknown@123-abc-321.Marketo"), null))`

