---
unique-page-id: 18874684
description: キャンペーン同期日 — [!DNL Marketo Measure]  — 製品ドキュメント
title: キャンペーンの同期日
exl-id: 66ce9948-9297-47ef-8b16-0ac45c5664fc
feature: Channels
source-git-commit: 38c721d10ac33ae85da1d425b6af53b9e3dfd0a1
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%

---

# キャンペーンの同期日 {#campaign-sync-dates}

キャンペーン同期日機能の機能と、この機能の使用例を説明します。

>[!NOTE]
>
>この記事では、古いプロセスについて説明します。 ユーザーには、 [新しく改善されたアプリ内プロセス](/help/channel-tracking-and-setup/offline-channels/custom-campaign-sync.md){target="_blank"}.

**[!DNL Marketo Measure]必要なパッケージ：6.9 以降**

この機能は、 [!DNL Salesforce] キャンペーンオブジェクト：

* タッチポイントの開始日
* タッチポイント終了日

特定のキャンペーンで購入者タッチポイントが有効になると、キャンペーンの同期日によって、個々のキャンペーンにタッチポイントの日付パラメーターを設定できるようになります。 例えば、2017 年 3 月 1 日にタッチポイント終了日を追加する場合、 [!DNL Marketo Measure] は、その日以前にキャンペーンに追加されたキャンペーンメンバーに対してのみタッチポイントを作成します。 [!DNL Marketo Measure] では、2017 年 3 月 1 日以降に追加されたキャンペーンメンバーのタッチポイントは作成されません。

![](assets/1.gif)

同様に、キャンペーンにタッチポイントの開始日（2017 年 1 月 1 日など）を追加する場合、 [!DNL Marketo Measure] では、2017 年 1 月 1 日以前にキャンペーンに追加されたキャンペーンメンバーにタッチポイントを作成しません。 タッチポイント終了日を追加する場合や、その逆の場合は、タッチポイント開始日を追加する必要はありません。

## ユースケース {#use-cases}

**タッチポイントのバックフィル**

マーケティングチームが特定のマーケティング活動に utm パラメーターを追加しない場合があります。 キャンペーンの同期日を使用すると、（オンライン活動に SFDC キャンペーンを使用している場合）ミスしたデータをバックフィルできます。 5 月 1 日から始まる電子メールキャンペーンを実行しているのに、チームが 5 月 15 日までその電子メールキャンペーンに utm パラメーターを追加していなかったとします。 SFDC キャンペーンを通じて電子メールのコンバージョンを追跡する場合は、そのキャンペーンに 5 月 15 日のタッチポイント終了日を設定し、キャンペーンの「応答済み」メンバーのタッチポイントを有効にすることができます。 このアクションは、 [!DNL Marketo Measure] :5 月 15 日までのすべての応答にタッチポイントを作成します。

**遡及的なキャンペーンメンバーシップタッチポイント**

新規の [!DNL Marketo Measure] のお客様は、SFDC キャンペーン経由で追跡したマーケティングデータの一部を取り込みたい場合があります。 ただし、オンライン SFDC キャンペーンに対してタッチポイントを有効にする場合は、以降、アトリビューションの二重カウントの問題が発生する可能性があります。 [!DNL Marketo Measure] は、オンラインマーケティング活動のタッチポイントを自動的に作成しています。 データの二重カウントを避けるために、Campaign タッチポイントの終了日を使用して、 [!DNL Marketo Measure] を SFDC キャンペーンに設定します。 例えば、SFDC で追跡していたソーシャルキャンペーンに遡及的なコンバージョンを追加する場合は、 [!DNL Marketo Measure] 7 月 1 日に（オンラインタッチポイントを作成している）JavaScript を編集し、Social SFDC キャンペーンを編集して、7 月 1 日と等しいタッチポイント終了日を含め、そのキャンペーンの購入者タッチポイントを有効にできます。

タッチポイントの終了日に関しては、他にも多くの使用例が考えられます。 特定の状況を見つけ出すのに役立つ場合は、 [Marketoサポート](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}.

>[!MORELIKETHIS]
>
>[[!DNL Marketo Measure] 大学：キャンペーンおよびキャンペーンメンバーフィールド](https://learn.bizible.com/2-bizible-customization/137720https://universityonline.marketo.com/courses/bizible-fundamentals-channel-management/#/page/5c63007334d9f0367662b758)