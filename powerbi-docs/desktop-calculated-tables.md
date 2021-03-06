---
title: "Power BI Desktop で計算テーブルを使用する"
description: "Power BI Desktop の計算テーブル"
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: d8ec3de8fc60501f44a76e090d1d35f21fa75f2b
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2018
---
# <a name="using-calculated-tables-in-power-bi-desktop"></a>Power BI Desktop で計算テーブルを使用する
計算テーブルを使うと、モデルに新しいテーブルを追加できます。 しかし、値のクエリを実行してデータ ソースから新しいテーブルの列に値を読み込む代わりに、テーブルの値を定義する Data Analysis Expressions (DAX) 数式を作成することができます。 Power BI Desktop では、レポート ビューまたはデータ ビューの [新しいテーブル] 機能を使用して計算テーブルを作成します。

ほとんどの場合、外部データ ソースからモデルにデータをインポートします。 それでも、計算テーブルにはいくつかの利点があります。 計算テーブルは、一般に計算の途中経過に最適です。データ モデルの一部として格納されるのではなく、その場で計算されたりクエリの一部として計算されたりするものです。

クエリの一部として作成するテーブルとは違って、レポート ビューまたはデータ ビューで作成する計算テーブルは、モデルに既に読み込まれているデータに基づいて作成されます。 たとえば、2 つのテーブルの和集合またはクロス結合を選択できます。

通常のテーブルと同じように、計算テーブルには他のテーブルとのリレーションシップを設定できます。 計算テーブルの列にもデータ型や書式設定があり、データ カテゴリに所属させることもできます。 列に好きな名前を付けたり、列を他のフィールドと同じようにレポートのビジュアルに追加したりできます。 データを取得したテーブルのいずれかが最新の情報に更新されるか、他の方法で更新されると、計算テーブルは再計算されます。

計算テーブルは、結果の計算に [Data Analysis Expressions](https://msdn.microsoft.com/library/gg413422.aspx) (DAX) を使用します。これは、Power BI Desktop で取り扱っているようなリレーショナル データを操作することを意図した数式言語です。 DAX は 200 以上の関数、演算子、およびコンストラクトを含むライブラリを提供しているため、数式を作成する際の柔軟性が非常に高く、データ分析に必要なほとんどすべての計算結果を得ることができます。

## <a name="lets-look-at-an-example"></a>例を見てみましょう
Contoso 社のプロジェクト マネージャー Jeff は、北西部の従業員のテーブルと、南西部の従業員のテーブルを持っています。 Jeff は、2 つのテーブルを合わせて 1 つのテーブルにしたいと考えています。

**NorthwestEmployees**

 ![](media/desktop-calculated-tables/calctables_nwempl.png)

**SoutwestEmployees**

 ![](media/desktop-calculated-tables/calctables_swempl.png)

この 2 つのテーブルを合わせて 1 つの計算テーブルにする操作は非常に簡単です。 計算テーブルはレポート ビューとデータ ビューのどちらでも作成できますが、新しい計算テーブルをすぐに確認できるので、データ ビューで操作すると少し簡単になります。

**データ ビュー**の **[モデリング]** タブで **[新しいテーブル]**をクリックします。 数式バーが表示されます。

 ![](media/desktop-calculated-tables/calctables_formulabarempty.png)

次の数式を入力します。

 ![](media/desktop-calculated-tables/calctables_formulabarformula.png)

Western Region Employees という名前の新しいテーブルが作成されます。

 ![](media/desktop-calculated-tables/calctables_westregionempl.png)

この新しい Western Region Employees テーブルは、フィールドの一覧に他のテーブルと同じように表示されます。 他のテーブルとのリレーションシップを作成したり、計算列やメジャーを追加したり、任意のフィールドを他のテーブルと同じようにレポートに追加したりできます。

 ![](media/desktop-calculated-tables/calctables_fieldlist.png)

## <a name="functions-for-calculated-tables"></a>計算テーブル用の関数
計算テーブルは、テーブルを返す任意の DAX 式を使って定義できます。別のテーブルを単に参照するだけでも構いません。 例:

 ![](media/desktop-calculated-tables/calctables_formulabarsimpleformula.png)

DAX による計算テーブルを使うと、分析上の多くの課題を解決できます。 ここでは、計算テーブルについて簡単に紹介するだけにします。 計算テーブルを使用する際に役立つ一般的な DAX テーブル関数には、次のようなものが含まれています。

&lt;TABLE&gt; DISTINCT VALUES CROSSJOIN UNION NATURALINNERJOIN NATURALLEFTOUTERJOIN INTERSECT CALENDAR CALENDARAUTO

これらの関数と、テーブルを返す他の DAX 関数については、「[DAX 関数リファレンス](https://msdn.microsoft.com/ee634396.aspx)」をご覧ください。

