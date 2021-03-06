---
title: "Power BI の SQL Server Analysis Services ライブ データ"
description: "Power BI の SQL Server Analysis Services ライブ データ。 これは、エンタープライズ ゲートウェイ用に構成されたデータ ソースを使用して実行されます。"
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/10/2017
ms.author: maghan
ms.openlocfilehash: a2a0b2ae9f663f5bd2ba1c599f4f55232c0d1973
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2018
---
# <a name="sql-server-analysis-services-live-data-in-power-bi"></a>Power BI の SQL Server Analysis Services ライブ データ
Power BI では、ライブ SQL Server Analysis Services サーバーに接続できる方法が 2 つあります。 **[データの取得]** で SQL Server Analysis Services サーバーに接続する方法と、既に Analysis Services サーバーに接続している [Power BI Desktop ファイル](service-desktop-files.md)または [Excel ブック](service-excel-workbook-files.md)に接続する方法です。

 >[!IMPORTANT]
 >* ライブ Analysis Services サーバーに接続するには、オンプレミス データ ゲートウェイが管理者によってインストールおよび構成されている必要があります。 詳細については、「[オンプレミス データ ゲートウェイ](service-gateway-onprem.md)」をご覧ください。
 >* ゲートウェイを使用する場合、データはオンプレミスに残ります。  そのデータに基づいて作成されたレポートは、Power BI サービスに保存されます。 
 >* [Q&A 自然言語クエリ](service-q-and-a-direct-query.md)は、Analysis Services ライブ接続に対するプレビュー段階です。

## <a name="to-connect-to-a-model-from-get-data"></a>[データの取得] からモデルに接続するには
1. **マイ ワークスペース**で、**[データの取得]** を選択します。 グループワーク スペースが利用可能である場合、グループワーク スペースに変更することもできます。
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdatabutton.png)
2. **[データベースとその他]** を選択します。
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_1.png)
3. **[SQL Server Analysis Services]** > **[接続]** を選択します。 
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_2.png)
4. サーバーを選択します。 一覧にサーバーが表示されていない場合、それは、ゲートウェイとデータソースが構成されていないか、アカウントがゲートウェイのデータソースの **[ユーザー]** タブにリストされていないことを意味します。 管理者に確認してください。
5. 接続するモデルを選択します。 表形式または多次元モデルのいずれかを選択できます。

モデルに接続すると、Power BI サイトの **マイ ワークスペース/データセット**に表示されます。 グループ ワークスペースに切り替わると、データセットがグループ内に表示されます。

![](media/sql-server-analysis-services-tabular-data/connecttoas_dataset_5.png)

## <a name="dashboard-tiles"></a>ダッシュボードのタイル
レポートからダッシュ ボードにビジュアルをピンで固定すると、そのピンで固定されたタイルは 10 分間隔で自動的に更新されます。 オンプレミスの Analysis Services サーバー データが更新されると、タイルは 10 分後に自動更新されます。

## <a name="next-steps"></a>次の手順
[オンプレミス データ ゲートウェイ](service-gateway-onprem.md)  
[Analysis Services データ ソースの管理](service-gateway-enterprise-manage-ssas.md)  
[オンプレミス データ ゲートウェイのトラブルシューティング](service-gateway-onprem-tshoot.md)  
他にわからないことがある場合は、 [Power BI コミュニティを利用してください](http://community.powerbi.com/)。

