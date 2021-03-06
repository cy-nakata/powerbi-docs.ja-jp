---
title: "Power BI で Azure 監査ログに接続する"
description: "Power BI 用 Azure Audit Logs"
services: powerbi
documentationcenter: 
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/06/2018
ms.author: sarinas
ms.openlocfilehash: 1116da997123b29313a7614a3911f4b24c577dd8
ms.sourcegitcommit: c24e5d7bd1806e0d637e974b5143ab5125298fc6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2018
---
# <a name="connect-to-azure-audit-logs-with-power-bi"></a>Power BI で Azure 監査ログに接続する
Azure 監査ログのコンテンツ パックを利用して、監査ログに格納されている情報を分析したり、視覚化したりすることができます。 Power BI は、データを取得し、そのまま使えるダッシュボードをビルドし、取得したデータに基づくレポートを作成します。

[Azure 監査ログのコンテンツ パック](https://app.powerbi.com/getdata/services/azure-audit-logs)に接続するか、Power BI と [Azure 監査ログとの統合](https://powerbi.microsoft.com/integrations/azure-audit-logs)について詳細をお読みください。

## <a name="how-to-connect"></a>接続する方法
1. 左側のナビゲーション ウィンドウの下部にある **[データの取得]** を選択します。  
   
    ![](media/service-connect-to-azure-audit-logs/getdata.png)
2. **[サービス]** ボックスで、 **[取得]**を選択します。  
   
    ![](media/service-connect-to-azure-audit-logs/services.png) 
3. **[Azure 監査ログ]** > **[取得]** の順に選択します。  
   
   ![](media/service-connect-to-azure-audit-logs/azureauditlogs.png)
4. プロンプトが表示されたら、 **Azure サブスクリプション ID**を入力します。 [サブスクリプション ID](#FindingParams) を確認する方法について詳しくは、以下をご覧ください。   
   
    ![](media/service-connect-to-azure-audit-logs/parameters.png)
5. **[認証方法]** として**[oAuth2]** を選択し、**[サイン イン]** をクリックします。
   
    ![](media/service-connect-to-azure-audit-logs/creds.png)
6. アカウントの資格情報を入力して、サインイン プロセスを終了します。
   
    ![](media/service-connect-to-azure-audit-logs/login.png)
7. Power BI は、Azure 監査ログのデータを取得して、すぐに使用できるダッシュボードとレポートを作成します。 
   
    ![](media/service-connect-to-azure-audit-logs/dashboard.png)

**実行できる操作**

* ダッシュボード上部にある [Q&A ボックスで質問](power-bi-q-and-a.md)してみてください。
* ダッシュボードで[タイルを変更](service-dashboard-edit-tile.md)できます。
* [タイルを選択](service-dashboard-tiles.md)して基になるレポートを開くことができます。
* データセットは毎日更新されるようにスケジュール設定されますが、更新のスケジュールは変更でき、また **[今すぐ更新]** を使えばいつでも必要なときに更新できます。

## <a name="system-requirements"></a>システム要件
Azure 監査ログのコンテンツ パックには、Azure Portal の監査ログへのアクセスが必要です。 詳しくは、[ここ](https://azure.microsoft.com/documentation/articles/insights-debugging-with-events/)をご覧ください。

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>パラメーターの見つけ方
サブスクリプション ID を確認するには、2 つの簡単な方法があります。

1. https://portal.azure.com から &gt; [参照] -&gt; [サブスクリプション] -&gt; [サブスクリプション ID]
2. https://manage.windowsazure.com から -&gt; [設定] -&gt; [サブスクリプション ID]

サブスクリプション ID は数字や文字の長いセットで、上記の手順 \#4 の例のようになります。 

## <a name="troubleshooting"></a>トラブルシューティング
資格情報エラーまたは、更新しようとして資格情報が正しくないためにエラーが表示される場合は、Azure 監査ログのコンテンツ パックのすべてのインスタンスを削除し、再接続してみてください。

## <a name="next-steps"></a>次の手順
[Power BI の概要](service-get-started.md)  
[Power BI - 基本的な概念](service-basic-concepts.md)  

