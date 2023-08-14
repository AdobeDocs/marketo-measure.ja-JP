---
unique-page-id: 18874763
description: '"[!DNL Microsoft Dynamics] CRM インストールガイド — Marketo Measure — 製品ドキュメント»'
title: '"[!DNL Microsoft Dynamics] CRM インストールガイド»'
exl-id: bc422c98-60bb-49ea-9bd1-c4149ae628b1
feature: Installation, Microsoft Dynamics
source-git-commit: a2a7657e8377fd5c556d38f6eb815e39d2b8d15e
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 1%

---

# [!DNL Microsoft Dynamics] CRM インストールガイド {#microsoft-dynamics-crm-installation-guide}

>[!NOTE]
>
>この場合、[!DNL Marketo Measure]」 （アドビのドキュメント内）。ただし、CRM には「Bizible」が表示されます。 アドビは現在、その更新をおこなっており、ブランディングの変更がまもなく CRM に反映される予定です。

## サポートされているバージョン {#supported-versions}

[!DNL Marketo Measure] は、次をサポートします。 [!DNL Microsoft Dynamics CRM] バージョン：

* [!DNL Microsoft Dynamics 2016] （オンラインおよびオンプレミス）
* [!DNL Microsoft Dynamics 365] （オンラインおよびオンプレミス）

接続と認証の場合、 [!DNL Marketo Measure] は、次の Active Directory Federated Services(ADFS) バージョンをサポートしています。

* ADFS 4.0 - [!DNL Windows Server 2016]
* ADFS 5.0 - [!DNL Windows Server 2019]

## 管理ソリューションのインストール {#install-the-managed-solution}

[ダウンロードとインストール](assets/marketo-measure-dynamics-extension.zip) Dynamics CRM 内の zip ファイル。

**[!UICONTROL 設定]** > **[!UICONTROL カスタマイズ]** > **[!UICONTROL ソリューション]** > **[!UICONTROL インポート]** （ボタン） > **[!UICONTROL ファイルを選択]**.

![](assets/1.png)

>[!NOTE]
>
>次の 2 つのスクリーンショットは、ソリューションのアップグレード中に撮影されたものなので、実際のスクリーンショットとは少し異なる場合があります。

![](assets/2.png)

![](assets/3.png)

## [!DNL Marketo Measure] ユーザーの権限 {#marketo-measure-user-permissions}

専用の [!DNL Marketo Measure] Dynamics 内のユーザーが、CRM の他のユーザーとの問題を回避するために、データのエクスポートおよびインポートに使用します。 ユーザー名とパスワード、およびエンドポイント URL をメモしておきます。これは、 [!DNL Marketo Measure] アカウント。

## セキュリティロール {#security-roles}

組織で Dynamics セキュリティロールを使用している場合は、接続されているユーザーまたは専用のユーザーを確認してください [!DNL Marketo Measure] ユーザーには、必要なエンティティに対する十分な読み取り/書き込み権限があります。

セキュリティロールは次の場所にあります。 **[!UICONTROL 設定]** > **[!UICONTROL セキュリティ]** > **[!UICONTROL セキュリティロール]**.

の場合 [!DNL Marketo Measure] カスタムエンティティの場合は、すべてのエンティティに対して完全な権限が必要になります。

>[!NOTE]
>
>オポチュニティをクローズするユーザーにも、完全な権限が必要になります。

![](assets/4.png)

Dynamics 標準エンティティについては、 [!DNL Marketo Measure] Dynamics スキーマドキュメント。 高いレベルでは [!DNL Marketo Measure] 適切なデータを収集し、管理ソリューションでインストールされるカスタムフィールドに書き込むには、特定のエンティティを読み取るだけで済みます。 新しい標準レコードは作成せず、標準フィールドも更新しません。

## ページレイアウトにタッチポイントを含める： {#include-touchpoints-on-page-layouts}

1. 各エンティティについて、フォームエディターに移動します。 これは、以下の場所にあります。 **[!UICONTROL 設定]** > **[!UICONTROL カスタマイズ]** > **[!UICONTROL システムのカスタマイズ]** > `[Entity]` > **[!UICONTROL Forms]**. または、レコードを表示しているときに、設定に表示されます。

   * 設定するエンティティ（アカウント、商談、連絡先、リード、キャンペーン）。

   * キャンペーンを設定するには、 **[!UICONTROL CRM]** > **[!UICONTROL キャンペーン]**.

   ![](assets/5.png)

1. ページレイアウト：最初に「[!UICONTROL 1 列]」タッチポイントを有効にするセクションのタイル。 この新しい列内には、アカウントエンティティ、商談エンティティ、連絡先エンティティ、リードエンティティ内の各フォームにサブグリッドを追加する必要があります。

   ![](assets/6.png)

   ![](assets/7.png)

1. サブグリッドでレンダリングするオブジェクト（購入者属性タッチポイントまたは購入者タッチポイント）を選択します。これは、オブジェクトの関係に依存します。 必要に応じて、「編集」ボタンをクリックして、表示する列を変更します。 管理ソリューションによってデフォルトのレイアウトが設定されました。

   購入者属性タッチポイントサブグリッド — アカウント、商談、連絡先\
   購入者タッチポイントサブグリッド — リードと連絡先

   ![](assets/8.png)

1. フォームの更新が完了したら、変更を発行して保存します。

## スキーマ関連の考慮事項 {#schema-related-considerations}

**売上高**

[!DNL Marketo Measure] は、デフォルトで、標準の「実際の売上高」フィールドを指します。 これを使用しない場合は、カスタムワークフローが必要になるので、ソリューションエンジニアまたはサクセスマネージャーに売上高を報告する方法を説明してください。

**クローズ日**

[!DNL Marketo Measure] は、標準の [ 実際の終了日 ] フィールドを指します。 これを使用していない場合や、「 Estimated Close Date 」フィールドも使用している場合は、お使いのソリューションエンジニアまたはサクセスマネージャーにプロセスを説明してください。 カスタムワークフローは、両方のフィールドを考慮する必要がある場合があります。

## Adobe Admin Consoleと ID プロバイダーの設定 {#set-up-your-adobe-admin-console-and-identity-provider}

を使用する最初の手順 [!DNL Marketo Measure] は、プロビジョニングされたAdobe Admin Consoleを作成してログインするためのものです。 ログイン手順が記載された電子メールがまだ届いていない場合は、 [!DNL Marketo Measure] アカウント担当者。

製品としてのAdobeスイート [!DNL Marketo Measure] は、Adobe Admin Console for Identity Managementのすべての機能を活用します。 追加のリソースを使用できます [ここにある](https://helpx.adobe.com/jp/enterprise/using/admin-console.html).

利用可能なすべてのリソース、ベストプラクティスおよびオプションを確認することをお勧めします。 [Identity Management](https://helpx.adobe.com/enterprise/using/set-up-identity.html).

Adobe Admin Console内でのIdentity Managementの設定に関するガイダンスと確認については、 [!DNL Marketo Measure] アカウント担当者。

を使用してユーザーの認証と承認を容易におこなえるように [!DNL Marketo Measure] インスタンスの場合、Adobe Admin Console内で次の手順を実行する必要があります。

**の設定 [!DNL Marketo Measure] 製品カード**

Adobe Admin Consoleにアクセスすると、 [!DNL Marketo Measure] 「概要」セクションに存在する製品インスタンス。

![](assets/microsoft-dynamics-crm-installation-guide-8a.png)

クリック [!DNL Marketo Measure] 製品カードには、 [!DNL Marketo Measure] インスタンス。 デフォルトでは、 [!DNL Marketo Measure] インスタンスには、「 」というプレフィックスが付いた独自のプロファイルがあります[!DNL Marketo Measure]&#39;. このインスタンス内のこのまたは他のプロファイルに追加された管理者またはユーザーは、にログインできます [!DNL Marketo Measure].

![](assets/microsoft-dynamics-crm-installation-guide-8b.png)

内で新しいプロファイルを作成する際に必要なアクションはありません。 [!DNL Marketo Measure] 製品インスタンス。

次の手順で、アクセス可能なユーザーの追加を開始します： [!DNL Marketo Measure]を参照してください。詳しくは、 [追加中 [!DNL Marketo Measure] 管理者と [!DNL Marketo Measure] ユーザー](#adding-marketo-measure-admins-and-marketo-measure-users) 」の節を参照してください。

## 追加中 [!DNL Marketo Measure] 管理者と [!DNL Marketo Measure] ユーザー {#adding-marketo-measure-admins-and-marketo-measure-users}

次の手順では、 [!DNL Marketo Measure] アプリケーションに反映されます。 これは、 [!DNL Marketo Measure] 製品カード。

| ユーザータイプ | 説明 |
|---|---|
| 管理者 | 管理者と権限を持つユーザーが、 [!DNL Marketo Measure] 更新と管理を完全に行えるアプリケーション [!DNL Marketo Measure] — 特定の構成オプション |
| ユーザ | これらは、 [!DNL Marketo Measure] 内の読み取り専用権限を持つアプリケーション [!DNL Marketo Measure] アプリ |

ユーザーを各グループに追加すると、そのユーザーの [リストされた ID タイプ](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/set-up-identity.ug.html).

>[!NOTE]
>
>次の条件を満たすために [!DNL Marketo Measure] 管理者 ( [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target="_blank"}) の場合、ユーザーはユーザーとして追加する必要があります _および_ 管理者 [!DNL Marketo Measure] 内の製品プロファイル [!DNL Marketo Measure] 製品カード。

**へのログイン[!DNL Marketo Measure]**

製品プロファイルにユーザーを追加すると、そのユーザーは [!DNL Marketo Measure] インスタンスを選択して、 **Adobe IDでログイン** オプション： [experience.adobe.com/marketo-measure](https://experience.adobe.com/marketo-measure){target="_blank"}.

![](assets/microsoft-dynamics-crm-installation-guide-15.png)

## 接続とデータプロバイダーの設定 {#configuring-your-connections-and-data-providers}

にログインした後、 [!DNL Marketo Measure] アプリケーションを使用し、Adobe Admin Consoleでユーザーとして設定されている場合、次の手順は、様々なデータ接続を設定することです。

**データプロバイダーとしての CRM**

1. を [!DNL Marketo Measure] アカウントを選択し、 **[!UICONTROL マイアカウント]** ドロップダウンして「 」を選択します。 **[!UICONTROL 設定]**.

   ![](assets/microsoft-dynamics-crm-installation-guide-16.png)

1. の下 [!UICONTROL 統合] 左側のナビゲーションで、 **[!UICONTROL 接続]**.

   ![](assets/microsoft-dynamics-crm-installation-guide-17.png)

1. 次をクリック： **[!UICONTROL 新しい CRM 接続の設定]** 」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-18.png)

1. 次の隣 [!UICONTROL Microsoft Dynamics CRM]をクリックし、 **[!UICONTROL 接続]** 」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-19.png)

1. 選択 [!UICONTROL 資格情報] または [!UICONTROL OAuth].

   ![](assets/microsoft-dynamics-crm-installation-guide-20.png)

   >[!NOTE]
   >
   >OAuth の詳細については、を参照してください。 [この記事](/help/marketo-measure-and-dynamics/getting-started-with-marketo-measure-and-dynamics/oauth-with-azure-active-directory-for-dynamics-crm.md). プロセスに関するご質問は、 [!DNL Marketo Measure] アカウント担当者。

1. この例では、「資格情報」を選択します。 資格情報を入力し、「 **[!UICONTROL 次へ]**.

接続後、Dynamics 接続の詳細が「CRM/MAP 接続」リストに表示されます。

**広告アカウント接続**

広告アカウントをに接続するには [!DNL Marketo Measure]を開始するには、まず [!UICONTROL 接続] タブ内の [!DNL Marketo Measure] アプリケーション。

1. 上記の手順 1 および 2 に従います。 _データプロバイダーとしての CRM_ 」セクションに入力します。

1. 次をクリック： **[!UICONTROL 新しい CRM 接続の設定]** 」ボタンをクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-21.png)

1. 目的のプラットフォームを選択します。

   ![](assets/microsoft-dynamics-crm-installation-guide-22.png)

**[!DNL Marketo Measure]JavaScript**

次の条件を満たすため [!DNL Marketo Measure] web アクティビティを追跡するには、複数の設定手順があります。

1. 次をクリック： **[!UICONTROL マイアカウント]** ドロップダウンして「 」を選択します。 **[!UICONTROL アカウント設定]**.

   ![](assets/microsoft-dynamics-crm-installation-guide-23.png)

1. 電話番号を入力してください。 「 Web サイト」で、に使用するプライマリルートドメインを入力します。 [!DNL Marketo Measure] 追跡機能を使用できます。 終了したら「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/microsoft-dynamics-crm-installation-guide-24.png)

   >[!NOTE]
   >
   >複数のルートドメインを追加するには、 [!DNL Marketo Measure] アカウント担当者。

1. The [[!DNL Marketo Measure] JavaScript](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script.md) その後、サイト全体とランディングページに配置する必要があります。 ランディングページのヘッド内でスクリプトをハードコーディングするか、Tag Managementシステムを使用して次のようなスクリプトを追加することをお勧めします。 [Google Tag Manager](/help/marketo-measure-tracking/setting-up-tracking/adding-marketo-measure-script-via-google-tag-manager.md).

   >[!NOTE]
   >
   >デフォルトでは、 [!DNL Marketo Measure] は、ジョブが CRM にデータを送信するたびに、API クレジットごとに 200 件のレコードをエクスポートします。 ほとんどのお客様にとって、これは、 [!DNL Marketo Measure] CRM の CPU リソース要件。 ただし、ワークフローやトリガーなど複雑な CRM 設定を持つお客様の場合は、バッチサイズを小さくすると CRM のパフォーマンスが向上する可能性があります。 この目的のために [!DNL Marketo Measure] 顧客が CRM エクスポートのバッチサイズを設定できます。 この設定は、 [!DNL Marketo Measure] Web アプリケーションとお客様は、200（デフォルト）、100、50、25 のバッチサイズから選択できます。
   >
   >この設定を変更する場合、小さいバッチサイズでは、CRM からより多くの API クレジットを消費することに注意してください。 CRM で CPU がタイムアウトしたり、CPU 負荷が高くなったりした場合にのみ、バッチサイズを小さくすることをお勧めします。

   >[!NOTE]
   >
   >Dynamics へのMarketo Measureのデータの書き出しを無効にしても、既存のデータは削除されません。 既存のデータの削除については、Dynamics サポートにお問い合わせください。
