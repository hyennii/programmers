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

or

```javaScript
function solution(num1, num2) {
    var answer = num1 / num2;
    return Math.floor(answer);
}
```
<br>

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
