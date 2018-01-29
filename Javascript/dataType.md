# JavaScript 의 데이터 타입

## 1. JavaScript의 데이터타입 종류
* 수 (Number)
* 문자열 (String)
* 부울 (Boolean)
* 함수 (Function)
* 객체 (Object)
    * 함수 (Function)
    * 배열 (Array)
    * 날짜 (Date)
    * 정규식 (RegExp)
* 기호 (Symbol) (ES2015에 새롭게 추가)
* 널 (Null)
* 정의되지 않음 (Undefined)

## 2. 데이터타입 별 특징

### 2.1 수 (Numbers)
* 자바스크립트의 수는 정수와 같은 개념이 없다.
```JS
// 이런 경우가 생길 수 있다.
0.1 + 0.2 = 0.30000000000000004
```

* 덧셈, 뺄셈, 계수 (또는 나머지) 연산을 포함하는 표준 산술 연산자가 지원된다.
```JS
Math.sin(3.5);  // 사인
var circumference = 2 * Math.PI * r; // PI(3.141592...)
```

* parseInt() 함수를 사용하여 문자열을 정수로 변환할 수 있다. 이는 다음과 같이 옵션으로 주어지는 두번째 매개변수를 밑으로 하여 수행할 수 있다.
```JS
parseInt('123', 10); // 123
parseInt('010', 10); // 10
//OR 8진수 16진수 표기법
parseInt('010');  //  8
parseInt('0x10'); // 16
```

* 단항 연산자 ' + ' 를 활용해 문자열을 숫자로 변환
```JS
+ '42';   // 42
+ '010';  // 10
+ '0x10'; // 16
```

* 문자열이 수가 아닌 경우 NaN ("Not a Number" (수가 아님)을 줄인 약자)로 불리는 특별한 값을 돌려준다.
```JS
// 1. 문자열을 숫자로 변환할 때
parseInt('hello', 10); // NaN

// 2. NaN 과 연산
NaN + 5; // NaN

// isNaN() 함수를 통해 입력값 검증도 가능하다.
isNan(NaN); // true
```

* JavaScript는 또 특별한 값 Infinity와 -Infinity를 가지고 있다.
```JS
1 / 0; //  Infinity
-1 / 0; // -Infinity
// 내장 함수 isFinite()를 사용하여 Infinity, -Infinity 및 NaN 값을 테스트 할 수 있다.
isFinite(1 / 0);     // false
isFinite(-Infinity); // false
isFinite(NaN);       // false
```

## Reference
JavaScript 재입문하기 (JS ​튜토리얼) - https://developer.mozilla.org/ko/docs/A_re-introduction_to_JavaScript