# 1. 时间复杂度
渐进时间复杂度，用符号 $O$ 表示，程序执行次数用代数式表示，我们取这个代数式的最高次项且忽略此项系数作为时间复杂度。例如，如果程序执行次数为 $3n^3+2n^2+n+1$ ，那么程序的`渐进时间复杂度`为 $O(n^3)$ 。

* $ O(n^2) $ 时间复杂度

例一循环里计算 $n^2$ 次，例二循环运行 $2*n^2$ 但时间复杂度都是 $ O(n^2) $ 

```python
for i in range(n):
	for j in range(n):
		sum += a[i][j]
```

```python
for i in range(n):
	for j in range(n):
		sum += a[i][j]
for i in range(n):
	for j in range(n):
		mul *= a[i][j]
```