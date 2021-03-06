---
title: "他のユーザーから共有された ArcGIS マップとの対話"
description: "読み取りビューで ArcGis マップを使用します "
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: power bi, service, desktop, mobile
featuredvideoid: 
qualityfocus: monitoring
qualitydate: 06/23/2017
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/21/2018
ms.author: mihart
ms.openlocfilehash: 797b22ed6f07e64d7e4970f8f0dfe5e93a7c0ec4
ms.sourcegitcommit: 2ae323fbed440c75847dc55fb3e21e9c744cfba0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2018
---
# <a name="interacting-with-arcgis-maps-in-power-bi"></a>Power BI での ArcGIS マップとの対話
このトピックは、Power BI サービス、Desktop、またはモバイルで ArcGIS マップを "*使用する*" ユーザーを対象として書かれています。 作成者から ArcGIS マップを共有された場合、さまざまな方法でそのマップと対話できます。  ArcGIS マップの作成の詳細については、[Esri の ArcGIS マップのチュートリアル](power-bi-visualization-arcgis.md)をご覧ください。

ArcGIS マップと Power BI を組み合わせると、マッピングをマップ上のポイントの表現を越える、まったく新しいレベルに引き上げることができます。 基本マップ、場所の種類、テーマ、記号のスタイル、および参照レイヤーで使用可能なオプションを選択して、すばらしい有益なマップの視覚エフェクトを作成します。 空間分析を使用してマップ上で権限のあるデータのレイヤー (国勢調査データなど) を組み合わせることで、より深く理解できる視覚化されたデータを伝達します。

> [!TIP]
> GIS は Geographic Information Science (地理情報科学) の略です。
> 

ここで使用している例は、[Esri の ArcGIS マップのチュートリアル](power-bi-visualization-arcgis.md)で作成されるものと同じ ArcGIS マップです。 このチュートリアルでは、都市別の前年の売上を調べ、ストリート ベースマップとバブル シンボルを使って、サイズと平均世帯年収の参照レイヤーを表します。 マップには、3 つのピンと 1 つのドライブ時間半径 (紫) が含まれています。

![](media/power-bi-visualizations-arcgis/power-bi-arcgis-esri-new.png)

> [!TIP]
> 多くの例やユーザーの声を参照するには、[Esri のページを Power BI で](https://www.esri.com/powerbi)アクセスしてください。 その後、Esri が提供する [Power BI の ArcGIS マップの概要ページ](https://doc.arcgis.com/en/maps-for-powerbi/get-started/about-maps-for-power-bi.htm)を参照してください。
> 
> 

<br/>

## <a name="user-consent"></a>ユーザーの同意
仕事仲間から初めて ArcGIS マップを共有されると、Power BI にプロンプトが表示されます。 ArcGIS Maps for Power BI は [Esri](https://www.esri.com) によって提供されており、ArcGIS Maps for Power BI を利用するときは、Esri の使用条件およびプライバシー ポリシーが適用されます。 ArcGIS Maps for Power BI 視覚エフェクトの使用を希望する Power BI ユーザーは、同意ダイアログを受け入れる必要があります。

## <a name="selection-tools"></a>選択ツール
Power BI の ArcGIS マップでは 3 つの選択モードを使用できます。 一度に最大 250 のデータ ポイントを選ぶことができます。

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-tools2.png)

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-single2.png) 個々のデータ ポイントを選択します。

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-marquee2.png) マップに四角形を描画し、含まれるデータ ポイントを選択します。 複数の四角形の領域を選ぶには、Ctrl キーを使います。

![](media/power-bi-visualizations-arcgis/power-bi-esri-selection-reference-layer2.png) 参照レイヤー内で境界または多角形を使用して、含まれるデータ ポイントを選択することができます。

<br/>

## <a name="interacting-with-an-arcgis-map"></a>ArcGIS マップとの対話
使うことができる機能は、ユーザーが "*作成者*" (マップを作成したユーザー) か "*使用者*" (誰かから ArcGIS マップを共有されたユーザー) かによって異なります。 コンシューマー ([読み取りビュー](service-reading-view-and-editing-view.md)とも呼ばれる) として ArcGIS マップと対話する場合、以下の操作を使用できます。

* 他の視覚化の種類と同様に、[ダッシュボードへのピン留め](service-dashboard-pin-tile-from-report.md)、[表示](service-reports-show-data.md)、[基になるデータのエクスポート](power-bi-visualization-export-data.md)を行うことができ、[フォーカス モード](service-focus-mode.md)と[全画面表示](service-fullscreen-mode.md)でマップを表示することができます。    
* **[フィルター]** ウィンドウを展開し、フィルターを使ってマップを調べることができます。 レポートを閉じるとき、適用したフィルターは保存されません。    
    ![](media/power-bi-visualizations-arcgis/power-bi-filter-newer.png)  
* マップに参照レイヤーがある場合は、場所を選んでヒントに詳細を表示できます。 次の図では、Adams 郡を選択し、作成者がマップに追加した平均世帯年収参照レイヤーのデータを表示しています。
  
    ![](media/power-bi-visualizations-arcgis/power-bi-reference-layer.png)  
  
    この場合、グラフも表示されます。 グラフのバーを選ぶと、詳しいデータが表示されます。 Adams 郡の 79 世帯が年収 200,000 ドル以上であることがわかります。
  
    ![](media/power-bi-visualizations-arcgis/power-bi-tooltip-chart.png)
  
    矢印を選んで任意の追加グラフを表示できます。
* ベースマップの場所記号をポイントすると、ヒントに詳細が表示されます。     
  ![](media/power-bi-visualizations-arcgis/power-bi-arcgis-hover.png)
  
  > [!TIP]
  > 特定の場所を選ぶには、ズーム インが必要な場合があります。  または、重複している場所がある場合は、Power BI により一度に複数のヒントが表示されることがあります。 ヒント間を移動するには、矢印を選びます。
  > 
  > ![](media/power-bi-visualizations-arcgis/power-bi-3-screens.png)
  > 
  > 
* 作成者が ArcGIS マップにインフォグラフィックス レイヤーを追加している場合、マップの右上隅に追加データが表示されます。  たとえば、次の例ではマップ作成者が "Children under 14" を追加しています。
  
    ![](media/power-bi-visualizations-arcgis/power-bi-demographics.png)

## <a name="considerations-and-limitations"></a>考慮事項と制限事項
ArcGIS Maps for Power BI は、次のサービスとアプリケーションで使うことができます。

<table>
<tr><th>サービス/アプリ</th><th>使用できるかどうか</th></tr>
<tr>
<td>Power BI Desktop</td>
<td>はい</td>
</tr>
<tr>
<td>Power BI サービス (app.powerbi.com)</td>
<td>はい</td>
</tr>
<tr>
<td>Power BI モバイル アプリケーション</td>
<td>はい</td>
</tr>
<tr>
<td>Power BI Publish to Web</td>
<td>いいえ</td>
</tr>
<tr>
<td>Power BI Embedded</td>
<td>いいえ</td>
</tr>
<tr>
<td>Power BI サービスの埋め込み (PowerBI.com)</td>
<td>いいえ</td>
</tr>
</table>

**ArcGIS マップが表示されません。**    
ArcGIS Maps for Power BI を使うことができないサービスまたはアプリケーションでは、視覚エフェクトが Power BI のロゴを含む空のビジュアルとして表示されます。

**すべての住所がマップに表示されません**    
住所をジオコード化すると、最初の 1500 個の住所だけがジオコード化されます。 場所の名前または国のジオコード化は、1500 個の住所制限の対象には含まれません。

**Power BI の ArcGIS マップを使用する場合、料金はかかりますか。**

すべての Power BI ユーザーは追加コストなしで ArcGIS Map for Power BI を使うことができます。 これは **Esri** によって提供されるコンポーネントであり、ご利用の際には、この記事の前述のとおり、**Esri** が示す使用条件およびプライバシー ポリシーが適用されます。

**キャッシュに空きがないというエラー メッセージが表示されます**

これは対処中のバグです。  それまでの間は、エラー メッセージに表示されるリンクを選んで、Power BI キャッシュをクリアする手順を参照してください。

**オフラインで自分の ArcGIS マップを表示できますか。**

いいえ、Power BI でマップを表示するには、ネットワーク接続が必要です。

## <a name="next-steps"></a>次の手順
ヘルプの表示: **Esri** は、**ArcGIS Maps for Power BI** の機能セットに関する[包括的なドキュメント](https://go.microsoft.com/fwlink/?LinkID=828772)を提供します。

[**Power BI の ArcGIS マップ**](https://go.microsoft.com/fwlink/?LinkID=828771)に関する Power BI コミュニティ スレッドで、質問、最新情報の検索、問題の報告、および回答の検索を行うことができます。

改善の提案がある場合は、[Power BI のアイデア リスト](https://ideas.powerbi.com)に送信してください。

[Power BI の ArcGIS マップ製品ページ](https://www.esri.com/powerbi)

