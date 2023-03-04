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
---------------------------------------------
## 옷가게 할인받기
<br>

<img src="https://user-images.githubusercontent.com/107667966/215671160-ed2985b0-0e1d-4f8e-87f9-f0fbac37e50e.png" width="400">

```javaScript
function solution(price) {
    
    if(price >= 500000){
        price *= 0.8;
    }else if(price >= 300000){
        price *= 0.9;
    }else if(price >= 100000){
        price *= 0.95;
    }
    return Math.floor(price);
}
```
1) 조건이 '이상' 이므로 큰것 부터
-------------------------------------------------
## 짝수의 합
<br>

<img src="https://user-images.githubusercontent.com/107667966/215679178-4f341d57-e477-40cc-a1be-65b6c2b28a7a.png" width="400">

```javaScript
function solution(n) {
    let answer = 0;
    for(i = 0;i <= n;i ++){
        if(i % 2 === 0){
            answer += i;
        }
    }
    return answer;
}
```
또는
```javaScript
function solution(n) {
    let answer = 0;
    for (let i=2; i<=n; i+=2)
        answer += i;
        
    return answer;
}
```
1) i값 2부터 시작, 반복문 i+=2로 하여 짝수 값만 반복 계산하도록
----------------------------------------------------
## 배열의 평균값
<br>

<img src="https://user-images.githubusercontent.com/107667966/218680162-fe027daa-8fee-438c-bb96-fe8200489190.png" width="400">

```javaScript
function solution(numbers) {
    var answer = 0;
    let sum = 0;

    for (var i=0;i<numbers.length;i++) {
      sum += numbers[i];
    }
    answer = sum / numbers.length;
    return answer;
}
```
1) 배열에 담김 요소들의 합 구하고
2) 위에서 구한 합을 배열의 길이로 나누기
-----------------------------------------------------
## 세균 증식
<br>

<img src="https://user-images.githubusercontent.com/107667966/218684020-bb4566e4-40c0-495a-8187-c54fb962b80f.png" width="400">

```javaScript
function solution(n, t) {
    answer = n * 2 ** t
    return answer;
}
```
1)  ** : 거듭제곱
--------------------------------------------------------
## 머쓱이보다 키 큰 사람
<br>

<img src="https://user-images.githubusercontent.com/107667966/218895637-67e5b5c7-0b93-4d34-884b-df3926ff0532.png" width="400">

```javaScript
function solution(array, height) {
    let answer = 0;
    for(let i = 0; i < array.length; i++){
        if(array[i] > height){
            answer ++
        }
    }
    return answer;
}
```
-----------------------------------------------------------
## 배열 원소의 길이
<br>

<img src="https://user-images.githubusercontent.com/107667966/218910978-bb0baf07-5352-49c7-b8a5-c6033750e78d.png" width="400">

```javaScript
function solution(strlist) {
    let answer = [];
    for(i = 0; i < strlist.length; i ++){
        answer[i]=strlist[i].length;
    }
    return answer;
}
```
------------------------------------------------------------
## 피자 나눠 먹기(3)
<br>

<img src="https://user-images.githubusercontent.com/107667966/218927674-9849af62-5132-49b0-a96c-fd58d89fac92.png" width="400">

```javaScript
function solution(slice, n) {
    let answer = Math.ceil(n/slice);
    return answer;
}
```
1) Math.ceil(); : 올림
-------------------------------------------------------------
## 피자 나눠 먹기(1)
<br>

<img src="https://user-images.githubusercontent.com/107667966/218934703-7b29b7e9-fe3b-42ff-bc4a-47dc396648d4.png" width="400">

```javaScript
function solution(n) {
    let i = 1;
    for(i = 1; i*7/n<1; i++){

    }
    return i;
}
```
-------------------------------------------------------------
## 문자열 뒤집기
<br>

<img src="https://user-images.githubusercontent.com/107667966/222904516-1a967d28-8aa4-429c-9c90-0f3ca8265a95.png" width="400">

```javaScript
function solution(my_string) {
    return Array.from(my_string).reverse().join('');
}
```
1. Array.from 함수 : 유사 배열 객체나 반복 가능한 객체를 얕게 복사해 새로운 Array 객체를 만든다
2. join() : 배열의 모든 요소를 연결해 하나의 문자열로 만든다
   - 필요한 경우 문자열로 변환되고, 생략하면 배열의 원소들의 쉼표로 구분
   - ex. join() : //n,o,r,a,j
   - join('') : //noraj
   - join(-) : //n-o-r-a-j
-------------------------------------------------------------
## 배열 뒤집기
<br>

<img src="https://user-images.githubusercontent.com/107667966/222905902-02c21fb5-053a-4133-8ef5-6295ba68d282.png" width="400">

```javaScript
function solution(num_list) {
    return num_list.reverse();
}
```
-------------------------------------------------------------
## 배열 두 배 만들기
<br>

<img src="https://user-images.githubusercontent.com/107667966/222906772-b8c2992e-9f40-4277-9816-71ed79359045.png" width="400">
                                                                                                                            
```javaScript
   function solution(numbers) {
    let answer = []
    for(i = 0; i < numbers.length; i++){
        answer.push(numbers[i]*2);
    }
    return answer;
}                                                                                                                         
```
1. push : 배열의 끝에 하나 이상의 요소를 추가하고, 배열의 새로운 길이를 반환한다. 
  - 원본 배열을 바꾼다.                                                                                                                            
