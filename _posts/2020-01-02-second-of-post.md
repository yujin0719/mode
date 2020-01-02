---
layout: post
title:  "무식하게 풀기(brute-force)"
date:   2020-01-02 23:10:00 +0900
categories: Algorithm
---

## Brute-Force는 가능한 경우의 수를 일일이 나열하면서 정답을 찾는 방법이다. 

### 재귀호출(recursion)

``` 
재귀함수는 자신이 수행할 작업을 유사한 형태의 여러 조각으로 쪼갠 뒤, 그 중 한 조각을 수행하고, 나머지를 자기 자신을 호출해 실행하는 함수이다. 
```

* 1부터 n까지의 합을 계산하는 반복 함수
```
int sum(int n){
  int ret = 0;
  for(int i = 1; i <= n; ++i)
    ret += i;
   return ret;
 }
 ```
 
 * 재귀함수로 변환
 ```
 int recursiveSum(int n){
  if(n == 1)
    return 1;
   return n+ recursiveSum(n-1);
 }
 ```
 
 
