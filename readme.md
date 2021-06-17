# ロジスティック回帰　(Logistic Regression)
- 二値分類のための線形モデル
## オッズ比 (odds ratio)
- p は正事象(予測したい事象)の確率
- 分数で表すとこのようになる。  
![png-1](https://user-images.githubusercontent.com/54165015/122390759-493da280-cfad-11eb-911c-b15141789f4c.png)
- y = 1  
![png-2](https://user-images.githubusercontent.com/54165015/122390988-82761280-cfad-11eb-8067-c0118a40a0b2.png)


## シグモイド関数(Sigmoid Function)
- [証明](https://risalc.info/src/sigmoid-function.html)  
- ![png-4](https://user-images.githubusercontent.com/54165015/122391324-d7b22400-cfad-11eb-835e-fcc63447ba98.png)  
- eはネイピア数 = 2.71821...  
- xは総入力　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　
``` python
import numpy as np

def sigmoid(x):
  return 1.0 / (1.0 + np.exp(-x))
```
- 活性化関数
- 滑らかであり、線が切れていないので微分可能
- データ点が特定のクラスに所属している確率を予測すること
- あらゆる入力値を0.0～1.0の範囲の数値に変換して出力する関数  
- 単調増加関数  
S (x + a) > s(x)  
