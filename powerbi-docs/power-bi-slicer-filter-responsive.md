---
title: "Power BI でサイズを変更することが可能なレスポンシブ スライサーの作成"
description: "レポートに合わせてサイズを変更できるレスポンシブ スライサーの作成方法について説明します。"
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
ms.date: 12/08/2017
ms.author: maggies
ms.openlocfilehash: f95f126cc6a7c95fbe3227b712281a7d3f81e320
ms.sourcegitcommit: b780b7108fd9b52398b8377b52836f0e0fedc96e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2017
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi-preview"></a>Power BI (プレビュー) でサイズを変更することが可能なレスポンシブ スライサーの作成

レスポンシブ スライサーは、レポート上の領域に合わせてサイズが変わります。 レスポンシブ スライサーでは、異なるサイズに変更したり、水平から正方形や垂直などの異なる図形に変更できます。また、スライサー内の値を変更することで、スライサー自体を並べ替えることができます。 Power BI Desktop と Power BI サービスでは、水平スライサーおよび日付/範囲スライサーをレスポンシブにできます。 日付/範囲スライサーのタッチ領域も向上しているため、指を使用してより簡単に変更できるようになりました。 レスポンシブ スライサーは必要に応じて小さくまたは大きくすることができます。また、Power BI サービスと Power BI モバイル アプリのレポートにちょうど収まるように自動的にサイズ変更することもできます。 

![レスポンシブ スライサーは、さまざまな図形にすることができます。](media/power-bi-slicer-filter-responsive/responsive-slicer-gif.gif)

## <a name="create-a-slicer"></a>スライサーの作成

動的スライサーを作成する最初の手順は、基本的なスライサーを作成することです。 

1. **[視覚化]** ウィンドウで **[スライサー]** アイコン ![スライサー アイコン](media/power-bi-slicer-filter-responsive/power-bi-slicer-icon.png) を選択します。
2. フィルターを適用するフィールドを **[フィールド]** にドラッグします。

    ![スライサーにフィールドを追加する](media/power-bi-slicer-filter-responsive/power-bi-slicer-field.png)

## <a name="convert-to-a-horizontal-slicer"></a>水平スライサーに変換する

1. スライサーを選択し、**[視覚化]** ウィンドウで **[書式]** タブを選択します。
2. **[全般]** セクションを展開し、**[方向]** で **[横]** を選択します。

    ![スライサーを水平に設定する](media/power-bi-slicer-filter-responsive/power-bi-slicer-horizontal.png) 

1.  より多くの値を表示する場合は、幅を広げます。

     ![スライサーの幅を広げる](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-horizontal.png)

## <a name="make-it-responsive-and-experiment-with-it"></a>スライサーをレスポンシブにして試す

この手順は簡単です。 

1. **[書式]** タブの **[全般]** セクションの **[方向]** の下で、**[レスポンシブ (プレビュー)]** を **[オン]** にスライドします。  

    ![スライサーがレスポンシブになりました](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-responsive.png)

1. これでレスポンシブ スライサーを試すことができます。 コーナーをドラッグして高さを変えたり、幅を変えたりします。 非常に小さくすると、フィルターのアイコンだけが表示されるようになります。

    ![レスポンシブ スライサーが非常に小さくてフィルターのアイコンだけが表示されている状態](media/power-bi-slicer-filter-responsive/power-bi-slicer-small-filter-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a>電話レポート レイアウトに追加する

Power BI Desktop では、レポートのページごとに電話レイアウトを作成することができます。 ページに電話レイアウトがある場合、携帯電話では縦長ビューで表示されます。 それ以外の場合、横長ビューで表示する必要があります。 

1. **[ビュー]** メニューで **[電話レイアウト]** を選択します。

     ![[電話レイアウト] アイコン、[ビュー] メニュー](media/power-bi-slicer-filter-responsive/power-bi-phone-layout-menu.png)
    
1. 電話レポートに必要なすべてのビジュアルをグリッドにドラッグします。 レスポンシブ スライサーをドラッグするときに、希望のサイズにします。このケースでは、フィルターのアイコンだけです。

    ![電話レポート レイアウトにスライサーを追加する](media/power-bi-slicer-filter-responsive/power-bi-slicer-phone-layout.png)

詳細については、「[Power BI 電話アプリ用に最適化したレポートを作成する](desktop-create-phone-report.md)」をお読みください。

## <a name="make-a-time-or-range-slicer-responsive"></a>時間スライサーまたは範囲スライサーをレスポンシブにする

同じ手順を使用して、時間スライサーまたは範囲スライサーをレスポンシブにすることができます。 **[レスポンシブ]** を **[オン]** に設定した後、次のことに注意してください。

- ビジュアルは、キャンバスで許容されるサイズに応じて、入力ボックスの順序を最適化します。 
- データ要素の表示は、スライサーをできるだけ使用できるようにするため、キャンバスで許容されるサイズに基づいて最適化されます。 
- スライダーの新しい丸いハンドルバーは、タッチ操作を最適化します。 
- ビジュアルが小さくなりすぎて役に立たない場合、その場所でビジュアルの種類を表すアイコンになります。 これを操作するには、ダブルタップしてフォーカス モードで開きます。 これにより、機能を失うことなく、レポート ページ上の貴重なスペースを節約できます。

## <a name="next-steps"></a>次の手順

- [チュートリアル: Power BI サービスのスライサー](power-bi-visualization-slicers.md)
- 他にわからないことがある場合は、 [Power BI コミュニティで質問してみてください](http://community.powerbi.com/)。