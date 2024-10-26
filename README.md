# java-racingcar-precourse

---

## **기능 요구 사항**

초간단 자동차 경주 게임을 구현한다.

- **사용자 입력 기능**
    - [x] `자동차 이름 입력`: 쉼표로 구분된 자동차 이름을 입력받아 처리하는 기능
    - [x] `시도 횟수 입력`: 사용자가 시도 횟수를 입력받아 처리하는 기능
- **게임 진행 기능**
    - [x] `경주 시작`: 경주 상태를 초기화하고 입력된 정보를 기반으로 게임을 시작하는 기능
    - [x] `경주 진행`: 각 시도마다 자동차들의 위치를 업데이트하는 기능
    - [x] `단계별 경주 진행 상태 출력`: 각 시도 후 현재 진행 상태를 출력하는 기능
- **게임 결과 기능**
    - [x] `우승자 판별`: 최종 위치를 비교하여 우승 자동차를 판별하는 기능
    - [x] `우승자 출력`: 판별된 우승자를 출력하는 기능

### **예외처리**

- [ ] 사용자가 잘못된 값을 입력할 경우`IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.
    - [x] 자동차의 이름을 입력할 때, 5자를 초과하면 예외로 처리해야 한다.
    - [ ] 이동하는 횟수를 입력할 때, 정수 범위를 초과하면 예외로 처리해야 한다.
    - [ ] 이동하는 횟수를 입력할 때, 숫자가 아닌 값이 들어온다면 예외 처리해야 한다.

### **입출력 요구 사항**

### **입력**

- 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)

```
pobi,woni,jun

```

- 시도할 횟수

```
5

```

### **출력**

- 차수별 실행 결과

```
pobi : --
woni : ----
jun : ---

```

- 단독 우승자 안내 문구

```
최종 우승자 : pobi

```

- 공동 우승자 안내 문구

```
최종 우승자 : pobi, jun

```

### **실행 결과 예시**

```
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni :
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun

```

## **프로그래밍 요구 사항 1**

- [x] JDK 21 버전에서 실행 가능해야 한다.
- [x] 프로그램 실행의 시작점은`Application`의`main()`이다.
- [x] `build.gradle`파일은 변경할 수 없으며,**제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.**
- [x] 프로그램 종료 시`System.exit()`를 호출하지 않는다.
- [x] 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다.
- [x] 자바 코드 컨벤션을 지키면서 프로그래밍한다.
  기본적으로[Java Style Guide](https://github.com/woowacourse/woowacourse-docs/blob/main/styleguide/java)
  를 원칙으로 한다.

## **프로그래밍 요구 사항 2**

- [ ]  indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
    - [ ] 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
    - [ ] 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메서드)를 분리하면 된다.
- [ ] 3항 연산자를 쓰지 않는다.
- [ ] 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- [ ] JUnit 5와 AssertJ를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다.

### **라이브러리**

- `camp.nextstep.edu.missionutils`에서 제공하는`Randoms`및`Console`API를 사용하여 구현해야 한다.
    - Random 값 추출은`camp.nextstep.edu.missionutils.Randoms`의`pickNumberInRange()`를 활용한다.
    - 사용자가 입력하는 값은`camp.nextstep.edu.missionutils.Console`의`readLine()`을 활용한다.

### **사용 예시**

```- 0에서 9까지의 정수 중 한 개의 정수 반환 ```