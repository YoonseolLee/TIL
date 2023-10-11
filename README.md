# TIL

## 2023.09.27

### 프로그래머스

1. 길이가 다른 두 배열의 값을 비교할 땐 이중반복문을 사용한다.

2. 반복문 안에서 선언한 변수는, 반복문 밖에서 다시 사용할 수 없다.

3. Math 클래스의 세가지 함수 - ceil(), floor(), round()

4. 형변환: 연산이 끝나고 형변환을 하는게 아니라, 형변환을 시키고 연산을 한다.
   ex. (double)num1/num2 _1000; -> num1,num2을 double로 변환 후 (num1 / num2 _ 1000)을 함

5. 문자열을 뒤집을 땐 StringBuffer + reverse() + toString()을 이용하자. (배열 뒤집기 아님 주의)

6. 배열을 뒤집을 땐 Collection.reverse() 를 사용하자.

## 2023.09.28

1. 자바에서 배열 내용을 출력해보려고 배열 자체에서 toString()을 사용하면 배열의 내용이 아니라 배열의 주소값이 출력된다. 배열의 내용을 출력하려면 Arrays.toString()을 사용하자.

2. main 메소드 안에서 객체를 선언하면 메인 메서드 안에서만 접근할 수 있고, 메인 메소드의 실행이 끝나면 객체가 소멸된다.

3. 배열을 메서드에 전달할 때 중괄호 {}를 사용해서 배열을 리터럴로 선언하는 것은 허용되지 않는다.
   대신에 배열을 직접 생성(new)하고 값을 할당해야 한다.

4. ArrayList, LinkedList의 메소드는 거의 겹친다.

5. replace(기존문자, 바뀔문자) 를 사용하면 문자열의 특정 인덱스를 치환할 수 있다.

6. ReplaceAll 함수는 자신이 바꾸고싶은 문자로 문자열을 전부 치환시킨다.

7. String[] arr = my_string.split("")

8. 나눗셈을 할 때는 반드시 하나의 값이 실수(double)여야한다.

9. StringBuilder는 StringBuffer와 비슷한 자료형으로, 사용법도 같다. StringBuffer는 멀티 스레드 환경에서 안전하고, StringBuilder는 StringBuffer보다 성능이 우수하다. 따라서 동기화를 고려할 필요가 없는 상황에서는 StringBuffer보다 StringBuilder를 사용하는 것이 유리하다. 멀티 스레드 환경에는 StringBuffer를 쓰자.

## 2023.09.30

### 이것이 자바다

1. 함수형 프로그래밍이란 함수를 정의하고 이 함수를 데이터 처리부로 보내 데이터를 처리하는 기법이다.

2. 인터페이스의 익명 구현 객체를 람다식으로 표현하기 위해선, 인터페이스가 단 하나의 추상메소드만 가져야 한다. 그리고 인터페이스가 단 하나의 추상 메소드를 가질 때, 이를 함수형 인터페이스라고 한다.

3. 람다의 전반적인 것들을 배웠다. 익숙해지려면 많은 수련이 필요할 것이다.

### git

4.  브랜치 생성은 git branch 브랜치명
    브랜치 이동은 git switch 브랜치명
    브랜치 합치기는 main/master 브랜치로 이동한 뒤에 git merge 브랜치명
    브랜치마다 commit 내역을 그래프로 보고싶으면 git log --graph --oneline --all
    브랜치 합칠 때 conflict가 발생하면 파일열어서 수정하고 git add, git commit 하기

5.  3-way merge
    fast-forward
    rebase
    squash

### 프로그래머스

6. 메서드를 호출할 때, 메서드에 전달되는 인수(매개변수)는 변수 또는 리터럴 값으로 전달되어야 한다.

7. 메서드를 호출하더라도, 메서드를 변수에 저장(ex.a=method())하지 않으면 해당 메소드를 사용할 수 없다.

8. 나머지가 있다는 것은 곧 반올림이 가능할 수도 있다는걸 내포한다(0.5654 -> 0.6, use ceil).

9. charAt: String으로 저장된 문자열 중에서 한 글자만 선택해서 char타입으로 변환해주는 메소드이다.
   isLowerCase / isUpperCase: 소문자/대문자 여부를 확인한다.
   toLowerCase/ toUpperCase: 소문자/대문자로 변환한다.

### JavaPlayground

10. @BeforeEach: 이 어노테이션을 사용하면 각각의 테스트 메서드가 실행되기 전에 공통적인 설정 또는 초기화 작업을 수행한다.

11. isEqualTo는 값(내용)을 비교하며, 자료형이 서로 다른 경우엔 쓰지 말자.

12. ParameterizedTest: 여러 개의 테스트를 한번에 작성하기 위한 테스트

13. 주로 세트 또는 컬렉션과 단일 값 간의 동등성을 확인하려면
    `assertThat(numbers.contains(input)).isTrue();`와 같이 `contains` 메서드를 사용하는 것이 좋다. 컬렉션 자체와 단일 값 사이의 동등성 비교는 일반적으로 의미가 없으며 실패할 가능성이 높다.

14. @csvSource: csvSource를 활용하면 "중복 있는 코드"를 "중복 없는 코드"로 다시 구현할 수 있게끔 한다.

## 2023.10.02 ~ 2023.10.04

1. 스트림은 내부 반복자이다. 처리 속도가 빠르고, 람다식으로 다양한 요소를 처리할 수 있다. 또한 중간 처리와 최종 처리를 수행하도록 파이프라인을 만들 수 있다.

### TDD 연습

2. 테스트코드의 리턴타입이 꼭 void인것만은 아니다! 익숙함에 실수하지 말자.

3. while문을 사용하는 주요 이유 두가지
   a. 사용자 상호작용: 프로그램이 사용자와 상호작용(input)할 때 사용된다.
   b. 루프 탈출조건: while 루프는 특정 조건이 충족될 때까지 반복된다.

4. break 쓰는걸 까먹지 말자....

5. StringTokenizer를 사용하면 배열 안의 단어수를 세는데 편리하다. (countTokens() 사용)

6. 인스턴스 변수는 main 메소드에서 직접 접근할 수 없다. main 메소드는 정적(static) 메서드이며, 정적 메서드에서는 인스턴스 변수에 직접 접근할 수 없다.

## 2023.10.06

### TDD 연습

1. main 메소드 안에서 메소드를 만들 수 없다.

2. 에러 메시지를 출력하려면 System.err.println() 을 사용하자.

3. System.exit(1)을 입력하면 프로그램이 종료된다.

4. if문의 반대(=false)를 손쉽게 작성하려면 조건문 맨 앞에 !를 붙이면 된다.

5. count = count + 1; 을 count++;로 바꿔쓰면 가독성이 좋아진다.

6. 반복문이 반복될 때마다 ++되는 변수(ex.count)는 반복문 밖에서 선언해야한다.
   -> int count = 0;

7. 스트림에서 메소드 체이닝을 자주 쓰므로 익숙해지도록 하자

8. 중간 처리 기능인 필러링의 메소드에는 distinct(), filter()가 있다.

### 디자인

9. 추상화: 사물들의 공통된 특징을 파악해 인식의 대상으로 삼는 행위다. 추상화가 가능한 개체들은 개체가 소유한 특성의 이름으로 하나의 집합을 이룬다. 그러므로 추상화한다는 것은 여러 개체들을 집합으로 파악한다는 것과 같다.

10. 캡슐화: 캡슐화는 특히 낮은 결합도를 유지할 수 있게 해주는 객체지향 설계 원리다. 캡슐화는 정보 은닉을 통해 높은 응집도와 낮은 결합도를 갖도록 한다.

## 2023.10.11

### 우테코 연습

1. 매직 넘버를 친절한 이름의 상수로 빼주도록 하자.
2. main 메소드 안에서 클래스의 인스턴스를 생성한 후에, 인스턴스 메소드를 불러와야 한다.
3. getter는 값을 리턴하는 것이지, 출력하는 것이 아니다.
4. while 조건문과 상태라는 특성을 활용하면 숫자를 통해 프로그램을 제어하는데 편리하다.
