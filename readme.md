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

## 対数尤度(Log-likelihood)
[Qiita参照](https://qiita.com/kenmatsu4/items/b28d1b3b3d291d0cc698)  
1.正規分布を例にすると、正規分布の確率密度関数は  
<img width="306" alt="スクリーンショット 2021-06-19 10 40 11" src="https://user-images.githubusercontent.com/54165015/122627484-bc006800-d0ea-11eb-9492-04ef5576ddb8.png">  
こうなる。  
尤度関数の基本概念は、「サンプリングしてデータが観測された後、そのデータは元々どういうパラメーターを持つ確率分布から生まれたものだったか？」と言う問いに答えるためのもの
ここで、標本が10個手に入り、それが正規分布に従うことは分かっているが、平均、標準偏差がわからない時に、その標本がそれぞれ独立
していると仮定する。  
独立であるため、Pは確率密度の積になる。  
P(X1, X2,,,,,,) = p(X1) * P(X2)……..  
これはすべて正規分布であるので、確率密度関数をぶちこむ。  
P(X1, X2,,,,,,) = f(X1) * f(X2)……..  
展開するとこうなる。  
<img width="427" alt="スクリーンショット 2021-06-19 10 48 29" src="https://user-images.githubusercontent.com/54165015/122627653-e43c9680-d0eb-11eb-8600-2121e919e9ba.png">  
ただ、平均、標準偏差を求めたいので、左辺を変更する。
<img width="427" alt="スクリーンショット 2021-06-19 10 49 59" src="https://user-images.githubusercontent.com/54165015/122627686-19e17f80-d0ec-11eb-962f-f102e81d66e7.png">




