# 2020.07.08
## diary
1. C++中int转为string转为stringstream转为int
``` 
Input: int N;
string num = to_string(N);
stringstream s(num);
int ret = 0;
s>>ret;
Output: int ret;
```

## practice
### tag: greedy medium
### 738. Monotone Increasing Digits
1. 题意：给出一个数，求小于这个数的最大的高位数到低位数递增的数
2. 思路：从后往前遍历，遇到递增趋势，则把高方向位上的数减一（后面低位上的数都变成9，但会有多次遇到递增趋势的情况，所以最后统一变9即可）
3. 难点：不是找到最前面的递增趋势就行，而是每次遇到递增趋势都要把高一位的减一，因为：
__3332__
不减一，递增趋势滞留在“个-十“位之间
减了一，递增趋势在“百-千“位之间

（我觉得这里还要注意一个位上是0的情况，但题解好像都没有注意）,看下面的代码，由于判断条件的限制，是不会在0的基础上减一的，或者说0在高位就没有上面说的递增趋势
```
if(num[i] < num[i-1]){
  pos = i;
  num[i-1]--;
}
```
