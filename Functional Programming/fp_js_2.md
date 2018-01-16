# 일급 함수

## 일급 함수란?
함수를 값으로 다룰수 있는 개념을 뜻함.

## 일급 함수의 특징
    * 변수나 데이터 구조안에 담을 수 있다.
    * 파라미터로 전달 할 수 있다.
    * 반환값(return value)으로 사용할 수 있다.
이것은 일급 객체(First Class Citizen)의 특징과 같다.

## 일급 함수 예시
```JS
// 1. 변수나 데이터 구조 안에 담을 수 있다.

// 변수에 익명 함수를 담는 경우
var f1 = function(a) {
    return a * a;
}

// 변수에 이미 정의되어있는 함수를 담는 경우
function add(a, b) {
    return a + b;
}
var f2 = add; 

// 2. 파라미터로 전달 할 수 있다.
function f2(f) {
    return f();     // 3. 반환값(return value)으로 사용할 수 있다.
}

f2( function(){
    return 10;
});

```
## 일급함수의 활용
### Add Maker
Add Maker 함수에는 클로저라는 개념이 등장한다.<br/>
* 클로저(Closer) <br/>
내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근 할 수 있다. 이러한 메커니즘을 클로저라고 한다. 
```JS
function add_maker(a) {
    //클로저 
    return function(b) {
        return a + b;   // add_maker의 a 값을 기억하고있는 익명 함수. 이 함수는 a를 참조만 할 뿐이므로 순수함수이게 된다.
    }
}

// ex
var add10 = add_maker(10);
// add_maker(10) 의 리턴인 아래 코드와 같게된다.
add10 = function(b) {
    return 10 + b;
}

// add10(20) 은 다음과 같이 해석할 수 있다.
add10(20);
function(20) {
    return 10 + 20;
}
```


## Summary

## Review

## Reference
* 위키피디아 - https://ko.wikipedia.org/wiki/%EC%9D%BC%EA%B8%89_%EA%B0%9D%EC%B2%B4
* 생활코딩 - https://opentutorials.org/course/743/6544
* 인프런(유인동 강사님) - https://www.inflearn.com/course-status-2/
