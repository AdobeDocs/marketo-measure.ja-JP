---
description: '"[!DNL Marketo Measure] Salesforce パッケージのインストールとセットアップ — [!DNL Marketo Measure]  — 製品ドキュメント»'
title: '"[!DNL Marketo Measure] [!DNL Salesforce] パッケージのインストールとセットアップ»'
exl-id: ed58bc1e-cfb0-48db-aa53-96204e12de2e
source-git-commit: b59c79236d3e324e8c8b07c5a6d68bd8176fc8a9
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# [!DNL Marketo Measure] Salesforce パッケージのインストールとセットアップ {#marketo-measure-salesforce-package-installation-and-set-up}

インストールする前に [!DNL Marketo Measure] [!DNL Salesforce] ベースパッケージを最初に [!DNL Salesforce] サンドボックスを開いてから、Salesforce 本番インスタンスに移動します。

>[!NOTE]
>
>一度 [!DNL Marketo Measure] アカウントが [!DNL Salesforce] 実稼動インスタンスの場合、後方に移動してサンドボックスに接続することはできません。 また、 [!DNL Marketo Measure] アカウントは 1 つにのみ接続できます [!DNL Salesforce] 実稼動インスタンス。

この [!DNL Marketo Measure] 基本パッケージに含まれる内容：

* 7 カスタム [!DNL Marketo Measure] オブジェクト
* カスタム [!DNL Marketo Measure] フィールド
* 25 [!DNL Stock] レポート

[!DNL Marketo Measure] は、標準を読み取ることができます [!DNL Salesforce] ただし、オブジェクト、フィールド、レコードは [!DNL Marketo Measure] では、データを更新またはプッシュすることはありません。 が収集するすべてのデータ [!DNL Marketo Measure] JavaScript は [!DNL Marketo Measure] カスタムオブジェクトおよびフィールド。

以下の手順に従って、 [!DNL Marketo Measure Salesforce] ベースパッケージ。

1. 匿名ブラウザーを使用して、 [Salesforce Appexchange](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3000000B3KLuEAN){target=&quot;_blank&quot;} にログインし、ログインします。

1. を [!DNL Marketo Measure] サンドボックスまたは実稼動環境にパッケージ化します。

1. にログインします。 [!DNL Salesforce] 管理者として。

1. 選択 **[!UICONTROL インストール] （すべてのユーザー）**.

   ![](assets/marketo-measure-salesforce-package-installation-and-set-up-1.png)

1. インストールが完了したら、表示できます。

   ![](assets/marketo-measure-salesforce-package-installation-and-set-up-2.png)

インストールが完了したら、 [[!DNL Salesforce] ページレイアウト](/help/configuration-and-setup/marketo-measure-and-salesforce/page-layout-instructions.md){target=&quot;_blank&quot;} を [!DNL Marketo Measure] フィールドを設定します。

>[!NOTE]
>
>詳しくは、 [!DNL Marketo Measure] 作成および権限セット [使用方法](/help/configuration-and-setup/marketo-measure-and-salesforce/marketo-measure-permission-sets.md){target=&quot;_blank&quot;}。

## インストール [!DNL Marketo Measure] ダッシュボードパッケージ {#install-marketo-measure-dashboard-package}

この [!UICONTROL ダッシュボード] 拡張機能パッケージには、3 つの事前ビルドダッシュボードが含まれています。 インストールをお勧めします [!UICONTROL 範囲] すべてのユーザーの実稼動環境。

1. パッケージを [[!DNL Salesforce] Appexchange](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t610000001jI6){target=&quot;_blank&quot;}。

1. 選択 **[!UICONTROL すべてのユーザーにインストール]**.

   ![](assets/marketo-measure-salesforce-package-installation-and-set-up-3.png)

## の作成 [!DNL Marketo Measure] プロファイルとユーザー {#creating-a-marketo-measure-profile-and-user}

[!DNL Marketo Measure] 接続された [!DNL Salesforce] ユーザーの [!DNL Marketo Measure] アプリを使用します。

タッチポイントデータを [!DNL Salesforce] インスタンス、接続したユーザーは、 [!DNL Marketo Measure] カスタムオブジェクト（例：購入者のタッチポイントおよび購入者のアトリビューションのタッチポイント）および標準 [!DNL Salesforce] リードや連絡先などのオブジェクト。

の作成 [!DNL Marketo Measure] プロファイルを使用して、Salesforce にデータをプッシュする際に検証エラーが発生しないようにします。

手順 1:特定の [!DNL Marketo Measure] profile

1. 次の権限を割り当てます。

* &quot;[!DNL Marketo Measure] 管理者権限セット»
   * 管理されたアクセス許可セットを使用すると、SFDC 管理者は、レコードの作成、読み取り、書き込み、削除を SFDC 管理者が実行できます。 [!DNL Marketo Measure] オブジェクト。
* &quot;変換済みリードの表示と編集権限セット&quot;
   * これにより、 [!DNL Marketo Measure] 連絡先に変換した後にリードを装飾するため この権限セットが有効になっていない場合、データトラッキングに大きなギャップが生じる可能性があります。

>[!NOTE]
>
>このプロファイルは、システム管理者プロファイルのクローンにすることができます。

手順 2:専用のを作成 [!DNL Marketo Measure] ユーザーを設定して、 [!DNL Marketo Measure] を [!DNL Salesforce] インスタンス

1. 新しい [!DNL Marketo Measure] そのユーザーに対するプロファイル。

1. ユーザーレベルの権限として「マーケティングユーザー」を有効にします。

* この [!UICONTROL マーケティングユーザー] チェックボックスを使用すると、キャンペーンを作成し、キャンペーンインポートウィザードを使用できます。 このオプションが選択されていない場合、ユーザーはキャンペーンと高度なキャンペーン設定の表示、1 つのリードまたは連絡先に関するキャンペーン履歴の編集、キャンペーンレポートの実行のみが可能です。 [!DNL Marketo Measure] キャンペーンオブジェクトに対して読み書きを実行する機能が必要です。

手順 3:すべてのトリガー、ワークフロー、プロセスからこのプロファイルを除外

手順 4:にログインします。 [!DNL Marketo Measure] アカウントをアカウントして再認証 [!DNL Salesforce] 新しいユーザーとの接続

1. apps.bizible.com に移動し、新しいユーザー実稼動環境でログインします。 [!DNL Salesforce] 資格情報。

1. 選択 **[!UICONTROL 設定]** 内 **[!UICONTROL マイアカウント]** 」ドロップダウンリストから選択できます。

1. 選択 **[!UICONTROL 接続]** 内 **[!UICONTROL 統合]** グループ化。

1. 現在接続されているの右にあるキーアイコンをクリックします。 [!DNL Salesforce] 接続して選択 **実稼動環境での再認証**. 新しいユーザー資格情報を使用して再度ログインします（要求された場合）。
