# 行列について
>数学の線型代数学周辺分野における行列（ぎょうれつ、英: matrix）は、数や記号や式などを行と列に沿って矩形状に配列したものである。行の数と列の数が同じ行列は行列の和（英語版）が成分ごとの計算によって与えられる。行列の積の計算はもっと複雑で、2 つの行列がかけ合わせられるためには、積の左因子の列の数と右因子の行の数が一致していなければならない。 wikipediaより

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

積は形が違くても行数と列数が同じであれば計算できます。
+ 積
```math
\left(\begin{matrix} 
A_1 & A_2 \\ 
A_3 & A_4 \\ 
\end{matrix}\right)
\left(\begin{matrix} 
B_1 & B_2 \\ 
B_3 & B_4 \\ 
\end{matrix}\right)
 = 
\left(\begin{matrix} 
A_1B_1 + A_2B_3 & A_1B_2 + A_2B_4 \\ 
A_3B_1 + A_4B_3 & A_3B_2 + A_4B_4 \\ 
\end{matrix}\right)
```

```math
\left(\begin{matrix} 
A_1 & A_2 & A_3 & A_4\\ 
A_5 & A_6 & A_7 & A_8\\ 
A_9 & A_a & A_b & A_c \\ 
A_d & A_e & A_f & A_{10} \\ 
\end{matrix}\right)
\left(\begin{matrix} 
B_1 \\
B_2 \\ 
B_3 \\
B_4 \\ 
\end{matrix}\right)
 = 
\left(\begin{matrix} 
A_1B_1 + A_2B_2 + A_3B_3 + A_4B_4 \\
A_5B_1 + A_6B_2 + A_7B_3 + A_8B_4 \\
A_9B_1 + A_aB_2 + A_bB_3 + A_cB_4 \\
A_dB_1 + A_eB_2 + A_fB_3 + A_{10}B_4 \\
\end{matrix}\right)
```

+ 商
複雑なので使う際に自分で調べて～
[逆行列](https://manabitimes.jp/math/1153)

## 3D計算

### 回転
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
> Θ:回転角度

### 拡大縮小
```math
\left(\begin{matrix} 
S_x & 0 & 0 & 0 \\ 
0 & S_y & 0 & 0 \\ 
0 & 0 & S_z & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```
> S<sub>x</sub>: X軸方向の倍率  
> S<sub>y</sub>: Y軸方向の倍率  
> S<sub>z</sub>: Z軸方向の倍率  


### 平行移動
```math
\left(\begin{matrix} 
1 & 0 & 0 & T_x \\ 
0 & 1 & 0 & T_y \\ 
0 & 0 & 1 & T_z \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```
>T<sub>x</sub>: X軸方向の移動量  
T<sub>y</sub>: Y軸方向の移動量
T<sub>z</sub>: Z軸方向の移動量

### せん断
> せん断とは、、、
<img width="320" alt="せん断" src="https://user-images.githubusercontent.com/38420559/199863531-b6c50612-2f88-4f24-b19a-358311ff3075.png">
画像のように四角形の画像を平行四辺形へ変形させること

```math
\left(\begin{matrix} 
1 & H_{yx} & H_{zx} & 0 \\ 
H_{xy} & 1 & H_{zy} & 0 \\ 
H_{xz} & H_{yz} & 1 & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{matrix}\right)
```
>H<sub>xy</sub>​: XY平面でのX軸方向の係数
H<sub>yx</sub>: XY平面でのY軸方向の係数
H<sub>xz</sub>: XZ平面でのX軸方向の係数
H<sub>zx</sub>​: XZ平面でのZ軸方向の係数
H<sub>yz</sub>​: YZ平面でのY軸方向の係数
H<sub>zy</sub>: YZ平面でのZ軸方向の係数


自分は特に使うことがないので詳しくは下記のサイトへゴー

[アフィン変換の説明](https://pdwslmr.netlify.app/posts/3d-prog/affine-transformation/)

a