<h1>寶可夢對戰資料  
<h3>combats.csv -> 歷史對戰紀錄 y  
pokemon.csv -> 寶可夢素質資料  
tests.csv -> 兩隻寶可夢對戰  

資料處理流程紀錄  
* Type 2大量缺失值需補 (386/800) null ,fillna('empty')   

* object 資料類別轉換 -> category類別型別  

* Legendary從bool轉換成int (0,1)  

* 使用pandas的get_dummies對Type1 Type2做One Hot Encoding後用join合併 (Type有兩個1)  

* 把原本Type1 Type2改成數值  
    #將寶可夢屬性轉為數值表示 透過cat.categories查詢類別的標籤  
    dict(enumerate(pokemon_df['Type 2'].cat.categories))  
    {0: 'Bug',  
     1: 'Dark',  
     2: 'Dragon',  
     3: 'Electric',  
     4: 'Fairy',  
     5: 'Fighting',  
     6: 'Fire',  
     7: 'Flying',  
     8: 'Ghost',  
     9: 'Grass',  
     10: 'Ground',  
     11: 'Ice',  
     12: 'Normal',  
     13: 'Poison',  
     14: 'Psychic',  
     15: 'Rock',  
     16: 'Steel',  
     17: 'Water',  
     18: 'empty'}  
     
    #用數字取代原本的資料集
    pokemon_df['Type 1'] = pokemon_df['Type 1'].cat.codes  
    pokemon_df['Type 2'] = pokemon_df['Type 2'].cat.codes  
 
 * 資料分割  
 
 * 標準化
 
 * 建立模型、儲存最好權重  
 
 * matplotlib看訓練結果  
 
 
