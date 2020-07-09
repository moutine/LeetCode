# 2020.07.09
## diary
1. 
## practice
### tag: greedy medium
### 842. Split Array into Fibonacci Sequence
1. 题意：将一串数字拆成斐波那契数列
2. 思路：别想着什么奇巧淫技，递归就完事了，虽然看见递归就心绞痛。
```
用i,j,k三个量表示“[a,b,c]|a+b=c”中a,b,c的起始数字索引传进递归函数,
以0开头的多位数不行
b是最后一个数 结束
a+b != c 不行
a加入答案数列
callself
```
（提早判断出可以返回的情况叫剪枝）

3. 难点：克服心绞痛
