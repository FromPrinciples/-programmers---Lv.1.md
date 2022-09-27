# 짝수와 홀수
정수 num이 짝수일 경우 "Even"을 반환하고 홀수인 경우 "Odd"를 반환하는 함수, solution을 완성해주세요.

## 제한 조건
num은 int 범위의 정수입니다.
0은 짝수입니다.

|입출력 |예|
|--|--|
|num|	return|
|3	|"Odd"|
|4	|"Even"|

```java
class Solution {
    public String solution(int num) {
        String answer = "";
        
        /**
        *
        if (num % 2 == 0) {
            answer = "Even";
        } else {
            answer = "Odd";
        }
        return answer;
        */
        
        return num % 2 == 0 ? "Even" : "Odd";
    }
}
```

- num을 2로 나누었을 때 나머지가 없는 정수이면 짝수,
나머지가 존재하는 정수는 홀수로 정의하여 풀이!

---

# 평균 구하기

## 문제 설명

정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성해보세요.

## 제한사항
arr은 길이 1 이상, 100 이하인 배열입니다.
arr의 원소는 -10,000 이상 10,000 이하인 정수입니다.

|입출력| 예|
|--|--|
|arr	|return|
|[1,2,3,4]|	2.5|
|[5,5]|	5|

```java
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        double sum = 0;
        for (int i=0; i< arr.length; i++){
            sum += arr[i];
        }
        answer = sum / arr.length;
        return answer;
    }
   
}
```

- 0부터 배열 최대길이까지 증가하는 변수 i 선언
- 합계 변수 sum에 배열 인덱스[0] ~ 배열 인덱스[최대수] 합계 대입
- sum을 배열 인덱스 개수로 나눠서 정답에 대입하고 반환
