---
description: 統合権限の概要 — [!DNL Marketo Measure]  — 製品ドキュメント
title: 統合権限の概要
hide: true
hidefromtoc: true
feature: APIs, Integration
source-git-commit: 9196877384140d60a22012b43ea960017528f4d5
workflow-type: tm+mt
source-wordcount: '239'
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
    <br>
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
<br>
作成されたタッチポイントおよびその他のデータは、アカウント、キャンペーン、キャンペーン、キャンペーンメンバー、事例、連絡先、リード、商談のカスタム bizible フィールドに書き込まれます。</td>
    <td><b>Salesforce 接続ユーザ権限（必須）</b>
    <br>
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
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</tbody>
</table>
