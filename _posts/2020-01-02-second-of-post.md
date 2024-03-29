---
layout: post
title:  "무식하게 풀기(brute-force)"
date:   2020-01-02 23:10:00 +0900
categories: Algorithm
---

## Brute-Force는 가능한 경우의 수를 일일이 나열하면서 정답을 찾는 방법이다. 

### 1. 재귀호출(recursion)

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

### 2. 완전탐색: bruteforce와 같이 가능한 방법을 모두 만들어 보는 알고리즘은 완전탐색(exhausive search)이라고 한다. 
```
1. 완전 탐색은 최대 크기의 입력을 가정했을 때 답의 개수를 계싼하고 제한 시간 안에 생성할 수 있을지 가늠해야한다.
   가능하지 않다면 다른 설계 패러다임 사용
2. 가능한 모든 답의 후보를 만드는 과정을 여러개의 선택으로 나눈다.
3. 하나의 조각을 선택해 답의 일부로 만들고 나머지 답을 재귀 호출을 통해 완성한다.
4. 조각이 하나만 남은 경우, 기저사례로 선택해 처리한다. 
```

 
