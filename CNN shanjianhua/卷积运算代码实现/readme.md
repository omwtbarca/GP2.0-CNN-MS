```mermaid
	gantt
dateFormat  YYYY-MM-DD
title See it again Conor McGregor👑
excludes weekdays 2024-01-10
section A section
Completed task            :done,    des1, 2022-11-03,2022-12-08
Active task               :active,  des2, 2022-11-09, 3d
Future task               :         des3, after des2, 5d
Future task2              :         des4, after des3, 5d
	
```

```mermaid
	graph TD
subgraph   CNN-5X2
A[特征图处理-卷积运算]-->b[非填充]
A-->C[0填充]
	end
```
|bingo|非填充|0填充|
|---|---|---|
|图像模糊|
|图像锐化|
|边缘检测|
|Sobel|
|Prewitt|
|Laplace|
* 4种数据预处理方法 (axis=0 列，axis=1 行)
	* 中心化 Y=X-aver;xi-x-
	* 自标度化 Y=(x-aver)/std
	* 标准化
		* 色谱面积最大化 xi=xi/sum.xi
		> Y=X.T S=Y.sum (axis=0) Y=Y/S Y=Y.T
		* 质谱最大归一化 xi=xi/max.x
		> Y=X.T max=Y.max (axis=0) Y=Y/max Y=Y.T
	 	
	 	
<summary>Formulas</summary>
<details>
  
  ![image](https://user-images.githubusercontent.com/87826552/199670299-d426c999-4f68-4d96-94b9-d342cd14ee6a.png)

</details>
