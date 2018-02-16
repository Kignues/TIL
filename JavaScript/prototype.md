# 자바스크립트의 프로토 타입

## 1. 프로토타입의 뜻
프로토타입(Proto Type) 은 원형이라는 뜻이다. 자바스크립트에서 객체 원형을 프로토타입 이라고 칭한다.

## 2. 프로토타입을 통한 상속
```JS
function Student() {
    this.grade = 3;
    this.subject = "math";
}

var student1 = new Student();
var student2 = new Student();

console.log(student1.grade);    // 3
console.log(student1.subject);    // math

console.log(student2.grade);    // 3
console.log(student2.subject);    // math
```

## Reference
생활코딩 - https://opentutorials.org/course/743/6573