---
title: "Power BI Desktop で SAP HANA を使用する"
description: "Power BI Desktop で SAP HANA を使用する"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 9cbeb0b2504612a9eb32fdad1d95fd90b57e07d9
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2017
---
# <a name="use-sap-hana-in-power-bi-desktop"></a>Power BI Desktop で SAP HANA を使用する
Power BI Desktop を利用し、 **SAP HANA** データベースにアクセスできるようになりました。 **SAP HANA**を使用するには、Power BI Desktop **SAP HANA** データ接続が機能するように、SAP HANA ODBC ドライバーをローカルのクライアント コンピューターにインストールする必要があります。 SAP HANA ODBC ドライバーは、[SAP Software Download Center](https://support.sap.com/swdc) からダウンロードできます。 SAP Software Download Center で、Windows コンピューター用の SAP HANA CLIENT を検索します。 **SAP Software Download Center** は構成が頻繁に変更されるので、サイトのナビゲーションに関する具体的なガイダンスはありません。

**SAP HANA** データベースに接続するには、次の画像のように、**[データの取得] > [データベース] > [SAP HANA データベース]** を選びます。

![](media/desktop-sap-hana/sap-hana-1.png)

SAP HANA データベースに接続するとき、*server:port* の形式でサーバー名とポートを指定します。次の画像の例では、*ServerXYZ* という名前のサーバーと *30015* ポートが使用されています。

![](media/desktop-sap-hana/sap-hana-2.png)

このリリースで、[DirectQuery](desktop-use-directquery.md) モードの **SAP HANA** が Power BI Desktop と Power BI サービスでサポートされるようになりました。DirectQuery モードの **SAP HANA** を使用するレポートを Power BI サービスに公開したり、アップロードしたりできます。 DirectQuery モードで **SAP HANA** を使用しないときも、Power BI サービスにレポートを公開したり、アップロードしたりできます。

### <a name="supported-features-for-sap-hana"></a>SAP HANA でサポートされる機能
このリリースでは、次の一覧に示すように **SAP HANA**向けに多くの機能が用意されています。

* **SAP HANA** 用 Power BI コネクタでは SAP ODBC ドライバーを使用し、優れた使いやすさを実現
* **SAP HANA** では DirectQuery およびインポート オプションの両方をサポート
* Power BI では HANA 情報モデル (分析ビューや計算ビューなど) をサポートし、ナビゲーションを最適化
* **SAP HANA** では、ダイレクト SQL 機能を使用して行および列テーブルへの接続も可能
* HANA モデル向けに最適化されたナビゲーションを採用
* Power BI は、 **SAP HANA** の変数および入力パラメーターをサポート

### <a name="installing-the-sap-hana-odbc-driver"></a>SAP HANA ODBC ドライバーのインストール
### <a name="limitations-of-sap-hana"></a>SAP HANA の制限
**SAP HANA**を使用する場合、次に示すいくつかの制限があります。

* NVARCHAR 文字列は最大 4,000 文字の Unicode 文字に切り捨てられる
* SMALLDECIMAL はサポートされていない
* VARBINARY はサポートされていない
* 有効な日付は 1899/12/30 から 9999/12/31 まで

