## 몫 구하기
<br>

<img src="https://user-images.githubusercontent.com/107667966/202994527-8c7c4c70-001d-4d59-a1e9-fd0836385304.png" width="500">

```javaScript
function solution(num1, num2) {
    var answer = parseInt(num1/num2);
    return answer;
}
```
1) parseInt() 함수
: 문자열 인자를 파싱하여 특정 진수(수의 진법 체계에서 기준이 되는 값)의 정수를 반환
<br><br>

또는

```javaScript
function solution(num1, num2) {
    var answer = num1 / num2;
    return Math.floor(answer);
}
```
2) Math.floor()로 소수점 이하 버리기
-----------------------------------------
## 나머지 구하기
<br>

<img src="https://user-images.githubusercontent.com/107667966/203000109-f7c71d3c-46d1-4792-9327-c0207651725c.png" width="500">

```javaScript
function solution(num1, num2) {
    var answer = (num1%num2);
    return answer;
}
```
1) % : 나누고 남은 나머지
---------------------------------------
## 숫자 비교하기
<br>

<img src="https://user-images.githubusercontent.com/107667966/203244085-a66fb952-acd7-4da9-a70e-be89e592a522.png" width="500">

```javaScript
function solution(num1, num2) {
    if (num1 == num2){
        return 1;
    }
    else{
        return -1;
    }
}
```
1) if문 사용
<br><br>

또는

```javaScript
function solution(num1, num2) {
    var answer = num1 === num2 ? 1 : -1;
    return answer;
}
```
2) 비교연산자 사용
  - A===B : A와 B의 값과 데이터 타입이 같은가?
  - A==B : A와 B의 값이 같은가?
  - A!=B : A와 B의 값이 다른가?
---------------------------------------------------------
## 양꼬치
<br>

<img src="https://user-images.githubusercontent.com/107667966/205222694-daaf016f-37a2-46da-bb1d-86caee01443b.png" width="500">

```javaScript
function solution(n, k) {
    return (12000*n) + (2000*k) - parseInt(n/10)*2000;
}
```
1) parseInt() 를 이용해 정수값만 산출하게 하여, n이 10의 배수일 때만 계산 가능하도록 함.
<br> (이외에 Math.floor()함수, Math.trunc()함수도 동일하게 가능)
-----------------------------------------
## 아이스 아메리카노
<br>

<img src="https://user-images.githubusercontent.com/107667966/215038619-1b120c90-53cd-4f73-bcb7-690fef48527d.png" width="500">

*제한사항 : 0 < money ≤ 1,000,000

```javaScript
function solution(money) {
    if(money <= 1000000 && money > 0){
        let i = parseInt(money/5500)
        let m = money-(5500*i)
        
        let answer = [i, m]
        return answer;
    }
}
```
