# 소수 구하기

## 1. 일일이 소수를 반복문을 돌리면서 하나하나 체크하는 방법
---> 이건 시간이 엄청 걸린다.

## 2. 에라토스테네스의 체(소수 구하기)
위의 코드는 해당 수보다 작은 모든 수로 나누어 보아서 소수인지를 판단하는 방법으로, 소수의 정의에 충실한 방법이면서 무식하지만 가장 강력한 방법이다. 한 개의 소수를 구할 때는 그런대로 괜찮은 방법인데 범위의 모든 소수를 구할 때는 효율적인 방법이 아니다. 소수를 구하기 위해 에라토스테네스가 제안한 방법은 다음과 같다.

에라토스테네스의 체 : 범위에서 합성수를 지우는 방식으로 소수를 찾는 방법. 1. 1은 제거 2. 지워지지 않은 수 중 제일 작은 2를 소수로 채택하고, 나머지 2의 배수를 모두 지운다. 3. 지워지지 않은 수 중 제일 작은 3을 소수로 채택하고, 나머지 3의 배수를 모두 지운다. 4. 지워지지 않은 수 중 제일 작은 5를 소수로 채택하고, 나머지 5의 배수를 모두 지운다. 5. (반복)

![image](https://user-images.githubusercontent.com/95357946/195898182-1d800752-6e8f-49aa-bf3d-879b035ad9dd.png)

이때 파이썬 루트를 쓸때 sqrt는 시간복잡도가 logn이라 n ** (1/2)로 직접 계산하는 것이 더 빠르다.
