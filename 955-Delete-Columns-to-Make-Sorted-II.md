# 2020.06.21
## diary
1. lexicographic order, 字典序

2. Java
```
String A, B;  //字典序，A < B, 则A.compareTo(B) < 0
```
## practice
### tag: greedy medium
### 955. Delete Columns to Make Sorted II
1. 题意：
给一个Array\<String\>，String长度相同，把String叠着放，求删除最少的列，保证删后的Array\<String\>按字典序排列
2. 思路：
我！读！了！几百遍！题目！终于！读懂了！这一句！淦！
```
the final array has its elements in lexicographic order (A[0] <= A[1] <= A[2] ... <= A[A.length - 1]).
```
__这里的A[i]指的是第i个字符串__

__所以！！__

基于字典序比较大小的字符串，天生就有__“前面字母相同比较后面字母”__的规则

——————————

开始列符合字典序：不需要删，结束

while(开始列不符合字典序 && 不符合的原因不是相连字母相等)：

--删，
    
--删后开始列符合字典序：不需要再删，return
    
--删后开始列不符合字典序但不符合的原因是相连字母相等：不需要再删，进行__遍历__，return
——————————

__遍历：__

  __用boolean[]记录遍历列时，前一未删列当前上下行是否符合字典序，__

  --符合，那么当前列当前上下行不符合也没关系;

  --不符合，那就要删了当前列，因为前面false(前一未删列当前上下行字母相等，记为false,因为要等着后面的字母帮忙确定符合字典序),就指着当前列符合才能变成true(符合字典序)呢

3. 难点： 读懂题目
