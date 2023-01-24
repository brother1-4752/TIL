# E35-38

# E35 비밀번호는 어떻게 저장할까?

### 비밀번호 시스템 구현 : 해시함수

- 해시함수 : 유저가 입력한 값을 무작위 값으로 변환한다.
- 규칙 1 : 동일한 입력값에 대한 동일한 출력값을 가진다.
    - 일대일 대응 관계를 유지.
- 규칙 2 : 입력값이 아주 살짝만 바꿔도 출력값은 아예 바뀐다.
    - 해시함수의 무작위성
- 규칙 3 : 반대로 입력해도 원래 값이 나오지 않는다.
    - 해시함수는 일방통행

### 해시함수도 위험성은 존재한다 : 레인보우 테이블

- 레인보우 테이블 : 해시 함수가 변경한 값을 원래의 값과 연결한 표.
- 해시 함수를 통과한 값은 레인보우 테이블에서 조회하면 원래 값에 접근할 수 있다.

### 최종 병기, 솔트

- 솔트 : 아주 조그마한 무작위 텍스트
- 12345와 같은 비밀번호를 무작위 텍스트인 솔트와 합쳐 해시 함수에 통과시키면, 보다 안전하다.

# E36-37 객체 지향 프로그래밍이란?

### 프로그래밍 패러다임이란?

- 프로그래밍을 하는 사고의 틀

```jsx
Class Player {
	constructor(name, health, skill){
		this.name=name;
		this.health = health
		this.skill = skill
		this.xp = 0;
	}
}
```

### 상속

```jsx
class Human {
	constructor(name){
		this.name = name;
		this.arms = 2;
		this.legs = 2;
	}
}

class Teenager extends Human{
	constructor(name){
		this.emotinal = true;
	}

	curse(){
		return `*(@!)&$^`;
	}
}

class Baby extends Human {
	constructor(name){
		this.cute = true;
	}

	crt(){
		return `wawawa`;
	}
}
```