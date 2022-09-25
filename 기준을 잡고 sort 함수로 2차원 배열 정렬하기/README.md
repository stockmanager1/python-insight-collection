# lambda를 시용해서 sort 정렬

## 첫 번째 값 이용하기

lst = [[2, 1], [3, 4], [1, 2], [1, 3], [3, 2]]
lst.sort(key=lambda x:x[0])
print(lst)

 [[1, 2], [1, 3], [2, 1], [3, 4], [3, 2]]



## 두 번째 값 이용하기

x: ( ) 의 괄호안에 튜플 형식으로 집어넣는다. 
이 때 -를 하게되면 역으로 정렬시킬 수 있다. 
여기서는 먼저 0번째 인덱스에 대해서 오름차순으로 정렬한 뒤, 
동일한 값의 경우 내림차순으로 재정렬된다.

lst = [[2, 1], [3, 4], [1, 2], [1, 3], [3, 2]]
lst.sort(key=lambda x: (x[0], -x[1]))
print(lst)

 [[1, 3], [1, 2], [2, 1], [3, 4], [3, 2]]

## 결론 
즉 정리하자면 

sort 함수는 lambda를 사용해서 정렬 기준을 변화시킬 수 있다.
그리고 사용 형태는 lambda x : ~~ 형태로 사용이 된다.

lambda x : x[0]은 2차원 리스트에서 각 1차원에 대한 0번째를
기준으로 정렬한다는 의미

 
lambda x : x[1]은 2차원 리스트에서 각 1차원에 대한 1번째를
기준으로 정렬한다는 의미

그리고 lambda x : -x[0]처럼 -가 붙으면 reverse로 정렬한다는 의미

lambda x : (x[1],x[0])은 각 1차원 리스트에서 1번째 항을 기준으로
정렬하고 그 1번째 항에서 같은 것에 대해 0번째 리스트를 
기준으로 졍렬한다.

## 관련 백준 문제
[좌표 정렬하기 - 11650](https://github.com/stockmanager1/baejoon-study--TIL/tree/main/%EB%B0%B1%EC%A4%80/Silver/11650.%E2%80%85%EC%A2%8C%ED%91%9C%E2%80%85%EC%A0%95%EB%A0%AC%ED%95%98%EA%B8%B0)

[좌표 정렬하기 2 - 11651](https://github.com/stockmanager1/baejoon-study--TIL/tree/main/%EB%B0%B1%EC%A4%80/Silver/11651.%E2%80%85%EC%A2%8C%ED%91%9C%E2%80%85%EC%A0%95%EB%A0%AC%ED%95%98%EA%B8%B0%E2%80%852)
