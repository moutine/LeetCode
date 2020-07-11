# 2020.07.10
## diary
1. 
## practice
### tag: greedy medium
### 910. Smallest Range II
1. 题意：一串数，每个数可以加或者减K一次，求改变后“最大值和最小值差值最小”的数组
2. 思路：
![910图示](https://pic.leetcode-cn.com/79a2c51caabde6667f1ff5442ae19b861b4aaa04fccc627433ef04ced70214e6-910.jpg)
```
就是求
min(max(b,d) - min(a,c))
或者
非‘Z’型的特殊情况
```
3. 难点： 画画图，一开始可能会走弯路，总结下就可以拨开迷雾看到本质
