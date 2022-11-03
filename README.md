# 行列について
`数学の線型代数学周辺分野における行列（ぎょうれつ、英: matrix）は、数や記号や式などを行と列に沿って矩形状に配列したものである。行の数と列の数が同じ行列は行列の和（英語版）が成分ごとの計算によって与えられる。行列の積の計算はもっと複雑で、2 つの行列がかけ合わせられるためには、積の左因子の列の数と右因子の行の数が一致していなければならない。 wikipediaより`

よくわかりません

<img width="151" alt="行列" src="https://user-images.githubusercontent.com/38420559/199785189-dcbae3d0-0f79-4371-b971-617de1a8cba1.png">

XYZの行があり、Mの行で移動量を指し示します。


<img width="151" alt="行列" src="https://user-images.githubusercontent.com/38420559/199781909-7e47a849-c86a-4cdd-a39d-f8c49d9eeac6.png">

一番下の列は1の帳尻合わせなので主に０です。

## 行列四則演算
和と差は形が同じではないといけない
+ 和
```math
\left(\begin{matrix} 
A_a & A_b \\ 
A_c & A_d \\ 
\end{matrix}\right)
+
\left(\begin{matrix} 
B_a & B_b \\ 
B_c & B_d \\ 
\end{matrix}\right)
 = 
\left(\begin{matrix} 
A_a+B_a & A_b+B_b \\ 
A_c+B_c & A_d+B_d \\ 
\end{matrix}\right)
```

+ 差
```math
\left(\begin{matrix} 
A_a & A_b \\ 
A_c & A_d \\ 
\end{matrix}\right)
-
\left(\begin{matrix} 
B_a & B_b \\ 
B_c & B_d \\ 
\end{matrix}\right)
 = 
\left(\begin{matrix} 
A_a-B_a & A_b-B_b \\ 
A_c-B_c & A_d-B_d \\ 
\end{matrix}\right)
```

積は形が違くても計算できます。
+ 積
```math
\left(\begin{matrix} 
A_a & A_b \\ 
A_c & A_d \\ 
\end{matrix}\right)
\left(\begin{matrix} 
B_a & B_b \\ 
B_c & B_d \\ 
\end{matrix}\right)
 = 
\left(\begin{matrix} 
A_aB_a + A_bB_c & A_aA_b + A_bB_d \\ 
A_cB_a + A_dB_c & A_cA_b + A_dB_d \\ 
\end{matrix}\right)
```
## ３D計算

### 回転
$$Θ:回転角度$$
X軸まわりの回転：
```math
\left(\begin{matrix} 
1 & 0 & 0 & 0 \\ 
0 & cosΘ & -sinΘ & 0 \\ 
0 & sinΘ & cosΘ & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```

Y軸まわりの回転：
```math
\left(\begin{matrix} 
cosΘ & 0 & sinΘ & 0 \\ 
0 & 1 & 0 & 0 \\ 
-sinΘ & 0 & cosΘ & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```

Z軸まわりの回転：
```math
\left(\begin{matrix} 
cosΘ & -sinΘ & 0 & 0 \\ 
sinΘ & cosΘ & 0 & 0 \\ 
0 & 0 & 1 & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```

### 拡大縮小
```math
\left(\begin{matrix} 
S_x & 0 & 0 & 0 \\ 
0 & S_y & 0 & 0 \\ 
0 & 0 & S_z & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```
```math
S_x: X軸方向の倍率 \
S_y: Y軸方向の倍率 \
S_z: Z軸方向の倍率 
```

### 平行移動

![inspecter](https://user-images.githubusercontent.com/38420559/199782039-78545f35-8d89-4250-a284-a3c01985aa3c.png)
