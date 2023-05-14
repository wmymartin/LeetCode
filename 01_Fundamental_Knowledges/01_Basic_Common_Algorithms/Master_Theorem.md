# 1. 时间复杂度
渐进时间复杂度，用符号 $O$ 表示，程序执行次数用代数式表示，我们取这个代数式的最高次项且忽略此项系数作为时间复杂度。例如，如果程序执行次数为 $3n^3+2n^2+n+1$ ，那么程序的`渐进时间复杂度`为 $O(n^3)$ 。

* 举例 $O(n^2)$ 时间复杂度

例一循环里计算 $n^2$ 次，例二循环运行 $2*n^2$ 但时间复杂度都是 $O(n^2)$ 

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

* 非递归程序时间复杂度的计算

简单方法是`数循环`，但不一定始终正确。

# 2. Master Theorem

* 符号

$T(n)$ 表示时间复杂度，它等于下面任意一个符号

$\Theta$ theta 等于的意思

$O$ big-oh 小于等于的意思

$o$ small-oh 小于的意思

$\Omega$ big omega 大于等于的意思

$\omega$ small omega 大于的意思

* 主定理（对于递归式的时间复杂度计算方法）

将一个规模为n的问题，通过分治得到 $a$ 个规模为 $\frac {n} {b}$ 的问题，每次递归带来的额外计算为 $f(n)$ ，那么我们得到以下的关系式:

$$T(n)=aT(\frac{n}{b})+f(n)$$

此外额外定义一个 $c_{crit}$ 它是这么计算的：
$$c_{crit}=\log_ba$$

那么存在以下关系：

1.  是


# 参考文献
https://www.luogu.com.cn/blog/Chanis/master
https://www.luogu.com.cn/blog/GJY-JURUO/master-theorem
