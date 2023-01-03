<h1>breast_cancer_classfication  

<h2>是一個包含病患30種特徵，以及是否罹患乳癌為target的資料集
  
<h3>特徵及意義   

* mean radius: 半徑的平均值。
* mean texture: 紋理的平均值。
* mean perimeter: 周長的平均值。
* mean area: 面積的平均值。
* mean smoothness: 平滑度的平均值。
* mean compactness: 簇狀的平均值。
* mean concavity: 凹陷度的平均值。
* mean concave points: 凹陷點的平均數量。
* mean symmetry: 對稱性的平均值。
* mean fractal dimension: 分形維度的平均值。
* radius error: 半徑的標準誤差。
* texture error: 紋理的標準誤差。
* perimeter error: 周長的標準誤差。
* area error: 面積的標準誤差。
* smoothness error: 平滑度的標準誤差。
* compactness error: 簇狀的標準誤差。
* concavity error: 凹陷度的標準誤差。
* concave points error: 凹陷點的標準誤差。
* symmetry error: 對稱性的標準誤差。
* fractal dimension error: 分形維度的標準誤差。
* worst radius: 最大半徑。
* worst texture: 最大紋理。
* worst perimeter: 最大周長。
* worst area: 最大面積。
* worst smoothness: 最大平滑度。
* worst compactness: 最大簇狀。
* worst concavity: 最大凹陷度。
* worst concave points: 最大凹陷點數量。
* worst symmetry: 最大對稱性。
* worst fractal dimension: 最大分形維度。

<h2>解題思路  
<h3>
1.可以先嘗試用heatmap判斷高關聯性的feature後，用scatter觀察是否有機會使用KNN完成分類   
2.因為特徵較多，考慮使用NN或者MLPClassifier  
<h3>
![image](https://github.com/jelink27/Data_analytics_project/blob/main/breast_cancer_classfication/breast_cancer_heatmap.png)  


```
MLP (Multilayer Perceptron) 是一種前饋神經網絡，也稱為多層感知器。它是一種常見的深度學習模型，用於對輸入數據進行分類或回歸預測。
MLP 由輸入層、隱藏層和輸出層組成，其中輸入層和輸出層中的芝麻節點分別稱為特徵和標籤。MLP 通過在隱藏層中進行非線性轉換，將輸入轉換為預測結果。
MLP 適用於許多不同的情境，例如文本分類、音頻識別、影像分類等。此外，由於 MLP 具有較強的表達能力，因此也可用於解決高維度資料的分類和回歸問題。
```
