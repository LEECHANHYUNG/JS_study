# 타입 변환과 단축 평가

- 타입 변환은 기존 원시 값을 사용해 다른 타입의 새로운 원시 값을 생성

#### `명시적 타입 변환`

- 타입 캐스팅

```javascript
var a = 10;
var str = a.toString();		
```

`문자열 타입으로 변환`

```
String(1)
(1).toString();
```

`숫자 타입으로 변환`

```javascript
Number('0');
parseInt('0');
```



#### `암묵적 타입 변환`

- 타입 강제 변환

---

## 단축 평가

`&&`

- 둘다 참이면 두 번째 피연산자 반환

`||`

- 첫 번째 피연산자 → true이면 그대로 반환

→ `&&` 와 `||` 는 타입을 변환하지 않고 그대로 반환한다.

---

### 옵셔널 체이닝 연산자 ?.

- 좌항의 피연산자가 null 또는 undefined인 경우 undefined
- 그렇지 않으면 우항의 프로퍼티 참조를 이어간다.

```javascript
var elem = null;
var value = elem?.value;
```



---

### null 병합 연산자 ??

- 좌항의 피연산자가 null 또는 undefined인 경우 우항의 피연산자를 반환
- 그렇지 않으면 좌항의 피연산자를 반환

```javascript
var foo = null ?? 'default string';
```

- 기본값 설정에 유리

