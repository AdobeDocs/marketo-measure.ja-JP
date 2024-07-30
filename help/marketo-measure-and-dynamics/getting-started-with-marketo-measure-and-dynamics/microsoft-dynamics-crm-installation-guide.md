---
unique-page-id: 18874763
description: 「[!DNL Microsoft Dynamics] CRM インストールガイド - Marketo Measure - 製品ドキュメント」
title: 「[!DNL Microsoft Dynamics] CRM インストールガイド」
exl-id: bc422c98-60bb-49ea-9bd1-c4149ae628b1
feature: Installation, Microsoft Dynamics
source-git-commit: 706f60a3b35e524da816b1d70abd363f0f02a1ba
workflow-type: ht
source-wordcount: '970'
ht-degree: 100%

---

# [!DNL Microsoft Dynamics] CRM インストールガイド {#microsoft-dynamics-crm-installation-guide}

>[!NOTE]
>
>ドキュメント内に「[!DNL Marketo Measure]」を指定する手順が記載されている場合がありますが、CRM には引き続き「Bizible」と表示されます。アドビは現在更新に取り組んでおり、ブランディングの変更はまもなく CRM に反映される予定です。

## サポートされているバージョン {#supported-versions}

[!DNL Marketo Measure] は、次の [!DNL Microsoft Dynamics CRM] バージョンをサポートします。

* [!DNL Microsoft Dynamics 2016]（オンラインおよびオンプレミス）
* [!DNL Microsoft Dynamics 365]（オンラインおよびオンプレミス）

接続と認証の場合、[!DNL Marketo Measure] は、次の Active Directory Federated Services（ADFS）バージョンをサポートします。

* ADFS 4.0 - [!DNL Windows Server 2016]
* ADFS 5.0 - [!DNL Windows Server 2019]

## 管理ソリューションのインストール {#install-the-managed-solution}

Dynamics CRM 内に zip ファイルを[ダウンロードしてインストール](assets/marketo-measure-dynamics-extension.zip)します。

**[!UICONTROL 設定]**／**[!UICONTROL カスタマイズ]**／**[!UICONTROL ソリューション]**／**[!UICONTROL 読み込み]**（ボタン）／**[!UICONTROL ファイルを選択]**&#x200B;を選択します。

![](assets/1.png)

>[!NOTE]
>
>次の 2 つのスクリーンショットは、ソリューションのアップグレード中に撮影されたものなので、実際のスクリーンショットとは少し異なる場合があります。

![](assets/2.png)

![](assets/3.png)

## [!DNL Marketo Measure] ユーザの作成 {#creating-a-marketo-measure-user}

CRM 内の他のユーザとの問題を回避するために、Dynamics 内で専用の Marketo Measure ユーザを「アプリケーションユーザ」として作成し、データを書き出しおよび読み込むことをお勧めします。ユーザ名、パスワード、およびエンドポイント URLは [!DNL Marketo Measure] アカウントの作成時に使用されるので、書き留めておきます。

## セキュリティロール {#security-roles}

組織が Dynamics セキュリティロールを使用している場合は、接続されているユーザまたは専用の [!DNL Marketo Measure] ユーザが、必要なエンティティに対する十分な読み取り/書き込み権限を持っていることを確認します。

セキュリティロールは、**[!UICONTROL 設定]**／**[!UICONTROL セキュリティ]**／**[!UICONTROL セキュリティロール]**&#x200B;にあります。

[!DNL Marketo Measure] カスタムエンティティの場合、すべてのエンティティに対する完全な権限が必要です。

また、標準エンティティの読み取り／書き込み権限に加えて、キャンペーンの「作成」権限も必要です。

>[!NOTE]
>
>また、商談をクローズするユーザにも完全な権限が必要です。

![](assets/4.png)

Dynamics の標準エンティティについては、[!DNL Marketo Measure] Dynamics スキーマドキュメントを参照してください。大まかに言うと、[!DNL Marketo Measure] は、特定のエンティティを読み取り、適切なデータを収集し、管理ソリューションと共にインストールされるカスタムフィールドに書き込みます。標準レコードは作成されず、標準フィールドは更新されません。

## ページレイアウトにタッチポイントを含める： {#include-touchpoints-on-page-layouts}

1. 各エンティティについて、フォームエディターに移動します。これは、**[!UICONTROL 設定]**／**[!UICONTROL カスタマイズ]**／**[!UICONTROL システムをカスタマイズ]**／`[Entity]`／**[!UICONTROL フォーム]**&#x200B;で見つけることができます。または、レコードの表示中に設定で見つけることもできます。

   * 設定するエンティティ：アカウント、商談、取引先責任者、リード、キャンペーン。

   * キャンペーンを設定するには、**[!UICONTROL CRM]**／**[!UICONTROL キャンペーン]**&#x200B;で「キャンペーンの同期」オプションをオンにする必要があります。

   ![](assets/5.png)

1. まず、タッチポイントを有効にするセクションに [!UICONTROL 1 列]タイルを追加します。この新しい列内で、アカウント、商談、取引先責任者、リードの各エンティティ内の各フォームにサブグリッドを追加する必要があります。

   ![](assets/6.png)

   ![](assets/7.png)

1. サブグリッドでレンダリングするオブジェクト（Buyer Attribution Touchpoints または Buyer Touchpoints）を選択します。これは、オブジェクトの関係に応じて異なります。必要に応じて、「編集」ボタンをクリックして、表示される列を変更します。デフォルトのレイアウトは、管理ソリューションによって設定されます。

   Buyer Attribution Touchpoint サブグリッド - アカウント、商談、および取引先責任者\
   Buyer Touchpoint サブグリッド - リードと取引先責任者

   ![](assets/8.png)

1. フォームの更新が完了したら、変更を公開して保存します。

## スキーマ関連の考慮事項 {#schema-related-considerations}

**収益**

[!DNL Marketo Measure] は、デフォルトで標準の「実収益」フィールドを指します。これを使用していない場合は、カスタムワークフローが必要となるので、ソリューションエンジニアまたはサクセスマネージャーに収益を報告する方法を説明します。

**クローズ日**

[!DNL Marketo Measure] は、標準の「実際クローズ日」フィールドを指します。これを使用していない場合や、「推定クローズ日」フィールドも使用している場合は、ソリューションエンジニアまたはサクセスマネージャーにプロセスを説明します。両方のフィールドを考慮するには、カスタムワークフローが必要になる場合があります。

## 接続とデータプロバイダーの設定 {#configuring-your-connections-and-data-providers}

[!DNL Marketo Measure] アプリケーションにログインし、Adobe Admin Console でユーザとして設定したら、次の手順で様々なデータ接続を設定します。

**データプロバイダーとしての CRM**

1. [!DNL Marketo Measure] アカウントで、**[!UICONTROL マイアカウント]**&#x200B;ドロップダウンをクリックし、「**[!UICONTROL 設定]**」を選択します。

   ![](assets/microsoft-dynamics-crm-installation-guide-16.png)

1. 左側のナビゲーションの[!UICONTROL 統合]で、「**[!UICONTROL 接続]**」をクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-17.png)

1. 「**[!UICONTROL 新しい CRM 接続を設定]**」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-18.png)

1. [!UICONTROL Microsoft Dynamics CRM] の横にある「**[!UICONTROL 接続]**」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-19.png)

1. 「[!UICONTROL 資格情報]」または「[!UICONTROL OAuth]」を選択します。

   ![](assets/microsoft-dynamics-crm-installation-guide-20.png)

   >[!NOTE]
   >
   >OAuth について詳しくは、[この記事](/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/oauth-with-azure-active-directory-for-dynamics-crm.md)を参照してください。プロセスについてご質問がある場合は、[!DNL Marketo Measure] アカウント担当者にお問い合わせください。

1. この例では、「資格情報」を選択します。資格情報を入力し、「**[!UICONTROL 次へ]**」をクリックします。

接続後、CRM/MAP 接続リストに Dynamics 接続の詳細が表示されます。

**広告アカウントの接続**

広告アカウントを [!DNL Marketo Measure] に接続するには、まず [!DNL Marketo Measure] アプリケーション内の「[!UICONTROL 接続]」タブにアクセスします。

1. 上記の&#x200B;_データプロバイダーとしての CRM_ の節の手順 1 と 2 に従います。

1. 「**[!UICONTROL 新しい CRM 接続を接続]**」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-21.png)

1. 目的のプラットフォームを選択します。

   ![](assets/microsoft-dynamics-crm-installation-guide-22.png)

**[!DNL Marketo Measure]JavaScript**

[!DNL Marketo Measure] で Web アクティビティを追跡するには、複数の設定手順があります。

1. **[!UICONTROL マイアカウント]**&#x200B;ドロップダウンをクリックし、「**[!UICONTROL アカウント設定]**」を選択します。

   ![](assets/microsoft-dynamics-crm-installation-guide-23.png)

1. 電話番号を入力します。Web サイトで [!DNL Marketo Measure] のトラッキングに使用するプライマリルートドメインをWeb サイトに入力します。終了したら「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-24.png)

   >[!NOTE]
   >
   >複数のルートドメインを追加するには、[!DNL Marketo Measure] アカウント担当者にお問い合わせください。

1. 次に、[[!DNL Marketo Measure] JavaScript](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md) をサイト全体とランディングページ全体に配置する必要があります。ランディングページの先頭にスクリプトをハードコードするか、[Google タグマネージャー](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-via-google-tag-manager.md)などのタグ管理システムを通じて追加することをお勧めします。

   >[!NOTE]
   >
   >デフォルトでは、ジョブが CRM にデータを送信するたびに、[!DNL Marketo Measure] は API クレジットごとに 200 件のレコードを書き出します。これにより、ほとんどの顧客に、[!DNL Marketo Measure] が消費する API クレジットと CRM の CPU リソース要件との間の最適なバランスが提供されます。ただし、ワークフローやトリガーなど複雑な CRM 設定を持つ顧客の場合は、バッチサイズを小さくすると CRM のパフォーマンスの向上に役立つ場合があります。この目的のために、[!DNL Marketo Measure] では顧客が CRM 書き出しのバッチサイズを設定できます。これは、[!DNL Marketo Measure] Web アプリケーションの設定／CRM／一般ページで設定でき、顧客は 200（デフォルト）、100、50、25 のバッチサイズから選択できます。
   >
   >この設定を変更する場合、バッチサイズが小さいほど CRM からの API クレジットをより多く消費することに注意してください。CRM で CPU タイムアウトまたは高い CPU 負荷が発生している場合のみ、バッチサイズを小さくすることをお勧めします。

   >[!NOTE]
   >
   >Marketo Measure による Dynamics へのデータの書き出しを無効にしても、既存のデータは削除されません。既存のデータの削除に関するヘルプについては、Dynamics サポートにお問い合わせください。

   >[!MORELIKETHIS]
   >
   >[エラー通知](/help/configuration-and-setup/getting-started-with-marketo-measure/error-notifications.md){target="_blank"}
