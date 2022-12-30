<h1>kc_house  
<h2>是一個用於房價預測的資料集。這個資料集包含關於美國華盛頓州諾爾曼市郊區房屋的資訊，包括房屋的地理位置、建築面積、房間數量、地下室面積等等。  
  
<h3>特徵及意義   


* id：房屋的唯一識別碼。  
* date：房屋出售的日期。  
* price：房屋的售價。  
* bedrooms：房屋裡有幾間臥室。  
* bathrooms：房屋裡有幾間浴室。  
* sqft_living：房屋的居住面積（平方英尺）。  
* sqft_lot：房屋所在地的土地面積（平方英尺）。  
* floors：房屋有幾層樓。  
* waterfront：房屋是否位於水邊。  
* view：房屋的景觀。  
* condition：房屋的狀態。  
* grade：房屋的等級。  
* sqft_above：房屋的地上面積（平方英尺）。  
* sqft_basement：房屋的地下室面積（平方英尺）。  
* yr_built：房屋建造的年份。  
* yr_renovated：房屋最近一次翻修的年份。  
* zipcode：房屋所在地的郵遞區號。  
* lat：房屋所在地的緯度。  
* long：房屋所在地的經度。 
* sqft_living15：房屋周圍 15 平方英尺以內的居住面積（平方英尺）。 
* sqft_lot15：房屋周圍 15 平方英尺以內的土地面積（平方英尺）。  

<h2>解題思路  
<h3>房價預測為一個回歸問題，但特徵較多，所以房價跟單一特徵之間可能並無線性關係(或全部都有?  
不使用線性回歸，可考慮使用多項式回歸或是NN進行訓練。

<h2>model-1 使用NN 不加入dropout或L1 L2正規化<h2>    
```python3
#建立第一個sequential型別的model
model = keras.Sequential(name='model-1')

#第一層區全連階層設為64個unit，輸入shape=4 實際上輸入資料為(batch_size, 21)
model.add(layers.Dense(64,activation='relu',input_shape=(21,)))

#第二層全連階層設為64個unit
model.add(layers.Dense(64,activation='relu'))

#最後一層設為一個unit
model.add(layers.Dense(1))

#顯示網路模型架構
model.summary()
```
