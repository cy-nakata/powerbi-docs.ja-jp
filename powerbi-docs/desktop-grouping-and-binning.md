---
title: "Power BI Desktop でグループ化とビン分割を使用する"
description: "Power BI Desktop で要素をグループ化およびビン分割する方法について説明します。"
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
ms.date: 01/19/2018
ms.author: davidi
ms.openlocfilehash: 6d398a7594cfde65d878cbd317a2669b945da9e6
ms.sourcegitcommit: a973bc6adc88507932e7e1535a74208e3842f5c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/20/2018
---
# <a name="use-grouping-and-binning-in-power-bi-desktop"></a>Power BI Desktop でグループ化とビン分割を使用する
**Power BI Desktop** は、ビジュアルを作成するとき、基になっているデータで見つかった値に基づいて、データをチャンク (または **グループ**) に集計します。 多くの場合は問題ありませんが、チャンクの表示方法の調整が必要になる場合もあります。 たとえば、3 つの製品カテゴリを 1 つの大きなカテゴリ (1 つの *グループ*) にしたい場合などです。 または、売上を均等に分割した 923,983 ドルではなく 1,000,000 ドルのビン サイズにしたいこともあります。

Power BI Desktop では、データ ポイントを**グループ化**して、ビジュアルでのデータと傾向の表示、分析、調査をいっそう明確にすることができます。 また、**ビン サイズ** (**ビン分割**とも呼ばれます) を定義して、意味のある方法でデータを視覚化しやすい等しいサイズのグループにビジュアルを入れることもできます。

### <a name="using-grouping"></a>グループ化の使用
**グループ化**を使うには、Ctrl キーを押しながら要素をクリックして複数の要素を選びます。 次に、複数選択した要素の 1 つを右クリックし、表示されるメニューで *[グループ]* を選びます。

![](media/desktop-grouping-and-binning/grouping-binning_1.png)

作成されたグループはビジュアルの **[凡例]** バケットに追加され、**[フィールド]** の一覧にも表示されます。

![](media/desktop-grouping-and-binning/grouping-binning_2.png)

作成したグループのメンバーは、**[凡例]** バケットまたは **[フィールド]** の一覧でフィールドを右クリックし、*[グループの編集]* を選ぶことで、簡単に編集できます。

![](media/desktop-grouping-and-binning/grouping-binning_3.png)

表示される **[グループ]** ウィンドウでは、新規グループの作成や既存グループの変更を行うことができます。 **[グループとメンバー]** ボックスで**グループ**のタイトルをダブルクリックして新しい名前を入力することで、グループの*名前を変更*することもできます。

このウィンドウでは、グループに関するすべての操作を行うことができます。 **[グループに属していない値]** の一覧から、新しいグループまたは既存のグループのいずれかに、項目を追加することができます。 新しいグループを作るには、**[グループに属していない値]** ボックスで複数の項目を選び (Ctrl キーを押しながらクリック)、そのボックスの下の **[グループ]** ボタンをクリックします。

グループに属していない値を既存のグループに追加するには、グループに属していない値を選び、それを追加する既存のグループを選んで、**[グループ]** ボタンをクリックします。 グループから項目を削除するには、**[グループとメンバー]** ボックスで項目選び、**[グループ解除]** をクリックします。 また、グループに属していないカテゴリを **[その他]** グループに入れるか、またはグループに属さないままにするかを選択できます。

![](media/desktop-grouping-and-binning/grouping-binning_4.png)

> [!NOTE]
> 既存のビジュアルで複数選択することなく、**[フィールド]** で任意のフィールドのグループを作成することもできます。 それには、フィールドを右クリックし、表示されるメニューの **[グループ]** を選びます。
> 
> 

### <a name="using-binning"></a>ビン分割の使用
**Power BI Desktop** の数値フィールドと時間フィールドに対してビンのサイズを設定できます。 ビン分割を使って、**Power BI Desktop** に表示されるデータを適切なサイズに設定できます。

ビンのサイズを適用するには、**[フィールド]** を右クリックして **[グループ]** を選びます。

![](media/desktop-grouping-and-binning/grouping-binning_5.png)

**[グループ]** ウィンドウで、**[ビンのサイズ]** を適切なサイズに設定します。

![](media/desktop-grouping-and-binning/grouping-binning_6.png)

**[OK]** を選ぶと、**[フィールド]** ウィンドウに新しいフィールドが表示されます。フィールド名の後には "*(ビン)*" が追加されています。 その後は、フィールドをキャンバスにドラッグして、ビジュアルでビンのサイズを使うことができます。

![](media/desktop-grouping-and-binning/grouping-binning_7.png)

**ビン分割**を実際に使っている様子は、こちらの[ビデオ](https://www.youtube.com/watch?v=BRvdZSfO0DY)でご覧いただけます。

**グループ化**と**ビン分割**を使ってレポートのビジュアルに意図したとおりにデータを表示する方法がわかります。

