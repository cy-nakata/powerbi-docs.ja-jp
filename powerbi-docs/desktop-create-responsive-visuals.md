---
title: "Power BI のビジュアルのサイズを最適化する"
description: "Power BI Desktop および Power BI サービスで Power BI 電話アプリ用にビジュアルを最適化する方法について説明します。"
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: a059c01d6e9e08851434f71a1f36ac096054e291
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2017
---
# <a name="optimize-a-power-bi-visual-for-any-size"></a>Power BI のビジュアルのサイズを最適化する
ダッシュ ボードまたはレポート内のビジュアルを "*レスポンシブ*" に設定することができます。これにより、ビジュアルは画面のサイズに関係なく、最大量のデータとインサイトを表示できるように動的に変化します。

ビジュアルがサイズを変更するとき、Power BI はデータ ビューを優先します (たとえば、自動的に余白を削除し凡例をビジュアルの上部に移動します)。これにより、ビジュアルは小さくなっても引き続き有益な情報を提供できます。 電話の Power BI モバイル アプリのビジュアルでは、応答性が特に役立ちます。

![レスポンシブ ビジュアルのサイズ変更](media/desktop-create-responsive-visuals/power-bi-responsive-visual.gif)

X 軸と Y 軸のある任意のビジュアルおよびスライサーで応答性を有効にできます。

## <a name="turn-on-responsiveness-in-power-bi-desktop"></a>Power BI Desktop で応答性をオンにする
1. Power BI Desktop の **[表示]** タブで、**[デスクトップ レイアウト]** になっていることを確認します。
   
    ![[デスクトップ レイアウト] アイコン](media/desktop-create-responsive-visuals/power-bi-desktop-layout.png)
2. ビジュアルを選択し、**[視覚エフェクト]** ウィンドウで **[書式]** セクションを選択します。
3. **[全般]** を展開し、**[レスポンシブ]** を **[オン]** にスライドさせます。
   
    ![レスポンシブがオン](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     これで、[電話用に最適化したレポートを作成](desktop-create-phone-report.md)し、このビジュアルを追加すると、ビジュアルのサイズが適切に変化します。

## <a name="turn-on-responsiveness-in-the-power-bi-service"></a>Power BI サービスの応答性をオンにする
Power BI サービスでレポートのビジュアルの応答性をオンにします。 レポートを編集できるようにする必要があります。

1. Power BI サービス ([https://powerbi.com](https://powerbi.com)) のレポートで、**[レポートの編集]** を選択します。
2. ビジュアルを選択し、**[視覚エフェクト]** ウィンドウで **[書式]** セクションを選択します。
3. **[全般]** を展開し、**[レスポンシブ]** を **[オン]** にスライドさせます。
   
    ![レスポンシブがオン](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     これで、[ダッシュボードの電話ビューを作成](service-create-dashboard-mobile-phone-view.md)し、このビジュアルを追加すると、ビジュアルのサイズが適切に変化します。

## <a name="next-steps"></a>次の手順
* [Power BI 電話アプリ用に最適化したレポートを作成する](desktop-create-phone-report.md)
* [Power BI でダッシュボードの Phone ビューを作成する](service-create-dashboard-mobile-phone-view.md)
* [電話用に最適化された Power BI レポートを表示する](mobile-apps-view-phone-report.md)
* 他にわからないことがある場合は、 [Power BI コミュニティで質問してみてください](http://community.powerbi.com/)。

