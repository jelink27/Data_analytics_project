<h1><wine_classfication葡萄酒分類資料集>  
<h2>wine_classfication資料集介紹及目標  
<h3>wine_classfication資料集內總共有13個特徵，3種分類結果(0、1、2) 
 
目標是利用這13個特徵，完成分類問題  
 
<h3>wine_classfication
  
葡萄酒資料集中有 13 個特徵。每個特徵都代表有關葡萄酒的某個特性或性質。

以下是葡萄酒資料集中每個特徵的具體含義：

* alcohol: 葡萄酒的酒精濃度。
* malic_acid: 葡萄酒中的苹果酸含量。
* ash: 葡萄酒中灰分的含量。
* alcalinity_of_ash: 葡萄酒灰分的碱度。
* magnesium: 葡萄酒中鎂的含量。
* total_phenols: 葡萄酒中总酚类物质的含量。
* flavanoids: 葡萄酒中的黄酮类化合物的含量。
* nonflavanoid_phenols: 葡萄酒中的非黄酮类酚类物质的含量。
* proanthocyanins: 葡萄酒中的花青素的含量。
* color_intensity: 葡萄酒的顏色強度。
* hue: 葡萄酒的色调。
* od280/od315_of_diluted_wines: 葡萄酒的 OD280/OD315 值。
* proline: 葡萄酒中的脯氨酸的含量。

 
<h4>2023/01/02 第一次嘗試用multiclass LogisticRegression完成分類問題  
混淆矩陣結果為：
 
              [[15  0  0]  
              [ 0 20  0]  
              [ 0  1 18]]  
 Accuracy為0.98  

![image]['https://github.com/jelink27/Data_analytics_project/blob/main/wine_classfication/wine_scatter.png']
