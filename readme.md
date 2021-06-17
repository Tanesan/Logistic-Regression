# ロジスティック回帰　(Logistic Regression)
- 二値分類のための線形モデル
## オッズ比 (odds ratio)
- p は正事象(予測したい事象)の確率
$$\frac{(1 - p)}{p}$$
- y = 1
```math
$$logit(p) =  \log\frac{(1 - p)}{p}$$
```

## シグモイド関数(Sigmoid Function)
- データ点が特定のクラスに所属している確率を予測すること
- あらゆる入力値を0.0～1.0の範囲の数値に変換して出力する関数
```math
 \varsigma _{a}={\frac {1}{1+e^{-ax}}}={\frac {\tanh+1}{2}}
```
