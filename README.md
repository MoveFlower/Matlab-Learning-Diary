# Matlab-Learning-Diary
记录学习过程。

## 实验一：求解方程组
### 没有使用克莱姆法则或行最简行列式，只是暴力解方程组
clear all//清除之前的所以order
syms FT2 m2 g a FT1 m1 r R J1 J2;
S=solve([FT2-m2*g==m2*r*a],[m1*g-FT1==m1*a*R],[FT2*r-R*FT1==(J1+J2)*a],[FT1],[FT2],[a])
S=[S.FT1 S.FT2 S.a]

Accound:
1. syms        : 定义为参数
2. solve       ：待解方程组
3. S.x S.y S.z : 待解未知数
