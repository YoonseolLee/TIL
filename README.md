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

## 2023.10.14

드디어 자소서 작성을 완성하였다! 이제 마음놓고 공부 할 수 있어서 후련하다.

### 우테코 연습

1. 비즈니스 로직, UI로직에 대해 알아보았고 블로그에 올렸다.
   나중에 코드를 작성할 때 둘을 분리해야 한다.
2. 명시적으로 생성자를 작성해 기본 생성자를 덮어쓰는 것을 잊지말자.
   초기화 로직이나 다른 설정이 없다면, 빈 생성자로 두는 것이 좋다.
3. Throwable result1: Throwable 클래스의 객체를 선언하는 것이다. Throwable은 모든 예외 클래스의 상위 클래스이므로 어떤 종류의 예외든 캐치할 수 있는 객체를 생성한다. result1 변수에 캐치된 예외를 저장할 것이다.
4. Throwable은 Java에서 모든 예외 클래스의 상위 클래스다. 따라서 Throwable 타입의 변수는 어떤 종류의 예외든 다룰 수 있는 객체를 나타낸다. 이를 통해 특정 예외 클래스에 의존하지 않고 모든 종류의 예외를 처리할 수 있다.
5. Collections.sort()를 통해 list를 오름차순 정렬할 수 있다.
6. asList와 List.of는 약간 다르다. 둘 다 불변의 리스트를 생성한다는 것은 동일하다.
   하지만 List.of는 Set으로 바꿀 수 없으며, null을 허용하지 않는다는 점에서 다르다.
   요약하자면 List.of가 더 까다로운 놈이다.

## 2023.10.15

### 우테코 연습

1. validateNumberInRange(int number, int startInclusive, int endInclusive)
   -> 검증할 숫자와 기준이 되는 두 숫자를 놓고 기준을 세워서 검증할 수 있는 메소드다.

2. 중복을 검사할 때 HashSet을 활용하면 편하다. 정규식을 사용해도 된다.

3. Enum은 보통 public으로 선언한다.

4. Enum의 생성자를 통해 값을 저장할 수 있다.

5. /\*\*

   - 구매 금액에 대한 모든 검증을 진행한다.
   - @param amount 구매 금액
   - @return 구매 금액 (int)
     \*/

   일상적으로 validation 메소드마다 파라미터 정보, 리턴 정보를 주석으로 명시하는 것 같다.

## 2023.10.16

1. 보통 View에 속하는 메소드는 public static void로 선언한다. Util도 마찬가지다. (불확실)
2. Constants, ErrorMessage는 상수이므로 public static final로 지정한다.
3. 원시값 포장은 String, int 등등 원시타입의 값을 이용해 속성을 표현하지 않고, 의미가 있는 객체로 포장하는 것이다. 줄여 말하자면 원시 타입의 변수를 객체로 포장한 것이다.
4. VO: 도메인에서 1개, 혹은 여러 개의 속성을 묶어서 특정 값을 나타내는 객체를 말한다.
5. VO의 조건1. equals & hashcode 메서드를 재정의해 동등성 비교가 가능하다.
   VO의 조건2. 불변 객체이다.

## 2023.10.16

1. 테스트 코드 작성 시 Given - When - Then 패턴을 활용하면 가독성 좋게 테스트 코드를 작성할 수 있다.

## 2023.10.20

1. Array와 ArrayList의 차이점과 특징 -> 블로그에 게시

## 2023.10.21

1. 반복문 생성 시 변수를 반복문 밖에서 선언하면 같은 변수를 n번 작업한다 -> 블로그 참고
2. 숫자야구 -> strike, ball을 0으로 초기화하는 메소드를 만드는 것을 잊지 말자.
3. boolean 변수를 활용하여, 미리 세팅을 false로 해놓은 다음, 특정 조건을 만족하는 경우 true로 바꿔서 프로그램을 종료시키는 방법이 존재한다.
4. List<String> inputList = new ArrayList<>(Arrays.asList(new String[]{"1", "2"}))
   -> 새 ArrayList를 생성하고, Arrays.asList 메서드를 사용하여 초기 요소로 "1"과 "2"를 가지는 문자열 배열을 변환하여 ArrayList에 대한 뷰를 생성한다. 이를 inputList에 저장한다.

## 2023.10.22 ~ 2023.10.30

1. 의존성 주입이란 필요한 객체를 직접 생성하거나 찾지 않고, 외부에서 넣어주는 방식이다.

2. getter 대신 Getter를 통해 얻은 상태값으로 하려고 했던 행동을 그 상태값을 가진 객체가 하도록 행동의 주체를 옮기는 방법을 사용하도록 하자.

3. setter 대신 생성자 오버로딩 or 빌더 or 정적 팩토리 메소드를 활용하자.

4. import static~ 은 사용하지 말자.

5. 출력하는 코드부분을 model 부분에서 관리해주는 것 보다, 별도의 class로 빼서 한번에 관리하면, 더욱 가독성이 좋은 코드를 만들 수 있다.

6. 변수를 인스턴스 변수로 두는 것이 나을지 혹은 지역 변수로 두는 것이 나을지 고민해보는 습관을 들이자.

## 2023.11.02

### 2주차 미션을 진행하며 배운 것들

1. 무조건 getter 사용을 지양하지는 말고, 필요에 따라 사용해도 괜찮다.

2. 원시값 포장 후 getter를 사용하는 것은 괜찮다.

3. TDD에서 Arrange - Act - Assert 패턴을 이용하면 테스트코드를 간편하게 작성할 수 있다.

4. 매직 넘버,리터럴 또한.. 무조건 상수처리 하는 것이 아니라 만약 사용자가 단번에 이해할 수 있다면 굳이 처리하지 않아도 괜찮다.

5. 주어진 요구조건이 "내부의 속성을 밖으로 꺼내는 것"이므로 이미 요구사항이 은닉하지 말것을 요구하고 있다.
   따라서 getter의 사용은 필연적이다.
   또한 이미 요구사항이 "은닉하지 말것을 요구"하므로 getter의 사용으로 인해 캡슐화가 깨어졌다고 할 수는 없다.

## 2023.11.21

## 3주차 미션을 진행하며 배운 것들

1. 중첩 클래스 사용 시, 거의 모든 경우에 inner class에 static을 붙이는 것이 좋다.

2. 외부에서 이미 생성된 객체(Name,Move) 를 생성자에서 받아 Car 객체를 초기화할 수도 있고, 아니면 String 타입의 CarName을 받아서 Name, Move 객체를 내부에서 생성하고 초기화할 수 있다.

3. 모든 검증을 Validation 관련 클래스에 넣을 필요는 없다.

4. InputView에서 출력(sysout)을 하지말고, OutputView가 출력을 담당하도록 하자.

5. View는 최대한 출력만 담당하도록 구조를 수정하면 모듈화가 향상될 것이다. 하지만 간단한 데이터 검증 및 변환 정도는 뷰에서 사용해도 좋다.

6. 생성자에서 검증하는 방법을 적극 활용해보자.

7. 불변 리스트: 수정을 방지하는 불변 리스트라는 것이 있다. Collections.unmodifiableList() 또는 List.copyOf()를 사용하여 만들 수 있는데, 전자는 원본 객체와의 참조가 끊어지지 않아 원본 리스트의 수정은 막지 못한다.

8. 컨트롤러는 비즈니스 로직을 알 필요가 없으며, 컨트롤러는 가능한 도메인 논리에 대해 가벼워야 한다.

9. public 메소드만 테스트해라. private 메소드를 꼭 테스트 해야 하는 상황이 온다면
   그건 높은 확률로 설계가 잘못 되었을 가능성이 높다.

10. 출력은 도메인 밖에서 하는 것이 좋다.

11. 매개변수에 final을 적용하는 것을 "매개변수의 불변성"이라고 한다. final 키워드를 사용하면 해당 매개변수는 메서드 내에서 값을 변경할 수 없게 된다.

12. 변수 이름에 자료형을 사용하지 말기 (ex.lottoList)

13. 메소드명은 15자 이하로 작성하기

## 2023.11.21

## 4주차 미션을 진행하며 배운 것들

1. 열거형 클래스는 toString() 메소드를 명시적으로 정의하지 않아도 enum 상수의 이름(name)을 문자열로 반환하는 기본 toString() 메소드를 제공한다.

2. 멤버 변수를 생성하는 부분에서, 각 객체를 재할당 할 필요가 없다면 불변성을 위해 final로 선언하는 것이 좋다.

3. 매개변수가 많으면 결합도 증가, 인터페이스 변경의 어려움, 가독성 감소의 단점이 생긴다.

4. 메소드를 또다른 메소드로 감싸는 것에는 장단점이 존재한다.
   장점: 가독성 향상 + 만약 감싼 메소드가 여러 곳에서 사용된다면, 해당 동작을 감싼 메소드를 만들어 코드의 중복을 피할 수 있다. 만약 추후에 동작이 변경되어야 할 때, 해당 변경은 한 곳에서만 이루어지면 된다.
   단점: 감싸는 메소드가 불필요하게 많아지면 코드가 더 복잡해질 수 있으므로 무의미한 래핑은 피해야 한다.

5. 로직의 처리와 출력 기능을 같은 메소드로 묶지 않는 것이 좋다.

6. while(true)를 사용하면 코드를 유지보수 하는 과정에서 무한루프에 빠질 가능성이 존재한다. 따라서 재귀함수나 do-while을 사용하도록 하자.

## 2023.11.24

## 스터디(숫자야구)

1. 강박적으로 모든 경우에 방법론을 적용할 필요는 없다. 오히려 가독성을 해치고 메모리양만 늘어나는 경우가 생길 수 있다.

2. 모든 상수를 상수 클래스에 등록할 필요는 없다. 특정 클래스에 종속적인 상수라면, 특정 클래스 안에서 상수를 선언하는 것도 괜찮다.

3. 공통적인 검증은 Validation 클래스에 넣고, 특정 클래스에만 적용되는 검증이면 해당 클래스에 검증메소드를 넣자.

4. while(true)는 유지보수에 좋지 않다. 재귀함수는 함수 stack이 계속 쌓여서 메모리가 낭비된다. 따라서 do-while을 애용하자.

5. 파생되어 나오는 값은 필드로 지정할 필요가 없다. 단, 다른 메소드나 클래스에서 사용되면 필드로 지정해라.

6. 조건문 내부에 논리연산자를 사용하면서까지 depth를 1로 만들 필요는 없다. 차라리 if(조건1) + if(조건2) 와 같이 이중 if문을 사용해보자.

7. do-while문은 while문이 true일 동안 반복문이 실행된다.

8. 예를 들어 List<Integer> randomNumbers = new ArrayList<>(); 와 같은 코드에서 우항을 작성하지 않으면 객체가 생성되지 않으므로 난수가 리스트에 들어가지 않는 문제가 발생한다. 따라서 꼭 객체생성하는 부분을 작성하자.

9. 두 개 이상의 인자를 전달할 때는, 객체로 만들어서 전달하면 된다. (ex. ballCount, strikeCount -> BallStrikeCount 클래스)

10. 게임 재시작 시 새로운 난수를 생성하게 하려면 리스트를 새로 초기화하는 기능을 추가하면 된다.

## 2023.11.26

1. 다른 클래스에서 함수를 사용할 때는 [class명].[함수명]으로 사용하시는 게 가독성이 좋다. 그렇게 하지 않으면 사용자가 해당 클래스에 있는 있는 함수로 인식하게 된다.

2. 객체를 많이 만들 필요가 전혀 없다. 하는 일이 별로 없으면 굳이 만들 필요가 없다.

3. 검증이 잘 작동하지 않으면 로직을 구체적으로 작성해보아라.
   true를 리턴하는 로직 대신 false를 리턴하는 로직으로 써본다던가..

4. List<Car> cars 라는 개념을 기억하자. 각각의 자동차를 Car 객체로 선언하고, 그것들을 포함하는 리스트 cars를 선언하는 것이다. 로또 미션에서 List<Lotto> LottoNumbers와 같은 개념이다.

5. Car 클래스에 필드로 name, price가 있다면 각각의 Car는 name과 price를 필드로 갖는다.

6. 레이싱게임에서 우승자의 타입은 무엇일까? String이 절대 아니다. 우승자는 Cars 중에 하나일 것이기 때문에 List<Cars> 이다!!

7. 입력값이 영어인지 검증하려면, Pattern.matches(패턴, 검사 대상); 을 통해 영어만으로 이루어져있는지 검사할 수 있다.

8. repeat()을 쓸 때는 (Math.max(0, 대상)) 과 함께 쓰자.

9. Enum은 기본적으로 모든 열거 상수가 동일한 타입을 가져야 한다.

## 2023.11.27

1. 파라미터의 개수가 많고, Controller, Service처럼 전체 프로젝트에서 구현체가 주로 하나만 사용된다면 IoC Container를, 파라미터의 개수가 많고, 파라미터에 들어가는 값이 매번 달라지는 Model은 Builder 패턴을 사용하자.

2. 의존관계 역전 원칙: 의존성 역전 원칙이란 객체는 구체적인 객체가 아닌 추상화에 의존해야 한다. 또한 의존관계를 맺을 때 자신보다 변화하기 쉬운 것을 의존해서는 안되고, 거의 변화가 없는 개념에 의존해야 한다. 예를 들면, 아이가 장난감을 갖고 노는데 어떤 경우에는 로봇을, 어떤 경우에는 레고를 가지고 놀 것이다. 이 경우에서 변하기 쉬운 것은 로봇, 레고, 모형 자동차다. 하지만 아이가 장난감을 가지고 논다는 사실은 변하기 어려운 개념이다.

3. 객체에서 의존하는 다른 객체가 너무 많아지는 문제를 IoC 컨테이너로 해결할 수 있다.

4. IoC(Inversion of Control; 제어의 역전): IoC는 소프트웨어 개발 디자인 원칙 중 하나로, 객체의 의존성 관리를 외부에서 하도록 한다. DI는 IoC를 지키는 방법 중 하나이다.

## 23.12.04

## 스터디(크리스마스)

1. 해당 월의 말일을 구할 땐, Calender 클래스의 cal.getActualMaximum(Calendar.DAY_OF_MONTH) 를 활용하면 된다. 단 월에는 -1을 해주어야 한다.

2. 도메인에서 모든 출력문구를 보내는 방법이 더 깔끔할 수도 있다.

3. if문을 두번 쓰지않고 첫번째 if문에 return;을 작성하면 두번째 if문을 쓸 필요가 없다.

4. Numberformat보다는 %d를 활용하면 간편하게 콤마를 숫자에 넣을 수 있다.

5. 객체를 만들면서 에러가 발생하는 경우에는 테스트코드 작성은 하지 않아도 된다.

6. 공백 포함여부를 검증하기 위해선 input.contains(" "), input == null 을 입력하면 된다.
   contains.null 은 불가능하므로 == null로 작성해야만 한다.
   그리고 입력값의 첫번째 값이 "0"인지 검사하기 위해선 startsWith()를 사용하면 된다.

7. 소수점 관련 계산을 할 땐 BigDecimal을 활용하자.

## 23.12.28

## 네트워크 기초

1. 네트워크의 종류는 크기와 연결 형태로 나눌 수 있다. 종류는 여러가지지만 필수만 작성하겠다.
   크기: LAN, WAN
   연결 형태: Star, Mesh

2. 네트워크의 통신방식
   유니 캐스트: 특정 대상이랑만 1대1로 통신하는 방식
   멀티 캐스트: 특정한 다수와 통신하는 방식
   브로드 캐스트: 같은 네트워크에 있는 모든 사용자와 통신하는 방식

3. 사용하고자 하는 기능에 따라 필요한 프로토콜이 달라진다.

4. 프로토콜은 하나만 사용되지는 않고 주로 함께 사용된다. Ethernet, IPv4, TCP, 데이터의 묶음을 패킷이라고 한다.

5. cmd에서 tracert(트레이스 라우팅) 명령어를 통해 지정된 IP 주소로의 경로 추적(Traceroute) 결과를 표시한다.
   이 명령을 실행하면 목적지 IP 주소로 가는 경로에 있는 네트워크 장치들과 데이터 패킷의 왕복 시간을 확인할 수 있다.

## 24.1.8

## Vue.js

1. App.vue: 최상위 루트 컴포넌트
   main.js: 가장 먼저 실행되는 자바스크립트 파일로써, Vue 인스턴스를 생성한다.

2. Vue CLI를 통해 빌드하면 소스코드가 하나의 파일로 합쳐지는데, 프로젝트가 커질수록 파일 용량이 커지기 때문에 사용자가 웹사이트에 접속할 때 큰 파일을 한번에 받으므로 렌더링 시간이 초기에 오래 걸다. 이 경우 장점은 로드만 되면 페이지 전환은 매우 빠르지만, 사용자가 사용하는 페이지가 별로 없다면, 사용하지도 않을 전체 페이지 코드를 다운 받음으로써 생기는 이점이 없다.

3. Lazy Load는 리소스를 컴포넌트 단위로 분리하여 컴포넌트 또는 라우터 단위로 필요한 것들만 그때 그때 다운받도록 하는 방법이다. Vue에서 Lazy Load 사용 시 주의할 것이 있다. 라우터에서 Lazy Load로 컴포넌트를 import한 것은 내부적으로 Vue CLI의 prefetch 기능이 사용되는 것이다. prefetch는 미래에 사용될 수 있는 리소스(about 같은 비동기 컴포넌트)를 캐시에 저장함으로써, 사용자가 접속할 때 아주 빠르게 리소스를 내려줄 수 있다. 아주 좋은 기능이지만, 비동기 컴포넌트로 정의된 모든 리소스를 당장 사용하지 않더라도 캐시에 담는 비용이 발생한다.

4. 결론만 얘기하자면 오히려 초기 렌더링은 prefetch를 사용하지 않아야 더 빨리 로딩이 된다. 또한 정말 필요한 컴포넌트에 대해서 prefetch 기능을 적용하는 것이 좋다. 라우터를 통해 이동되는 컴포넌트에 사용되는 리소스 크기가 크지 않다면 prefetch를 사용하지 않아도 큰 지장은 없다.

5. Vue.js는 SPA 개발을 위한 프레임워크로써 MVVM 패턴을 사용하며, 컴포넌트를 사용한 높은 재사용성을 가진다.

## Spring

1. 웹 개발의 방법(방식)을 정적 컨텐츠, MVC와 템플릿 엔진, API로 나눌 수 있다.

- 정적 컨텐츠 방식: 파일을 그대로 반환한다.
- MVC와 템플릿 엔진 방식: model, view, controller로 쪼개서 뷰를 템플릿 엔진으로 html 코드로 렌더링하여 반환한다.
- API 방식: 객체를 반환하는 것. HTTPMessageConverter를 통해 JSON으로 렌더링해서 반환한다.

2. @ResponseBody가 스프링 컨트롤러 메서드에 적용된 경우, 스프링은 해당 메서드가 반환하는 객체를 JSON (또는 XML, 하지만 거의 JSON 사용)과 같은 형식으로 변환하여 HTTP 응답 본문(body)에 담아 클라이언트에게 전송한다.

3. 스프링은 Jackson 라이브러리와 같은 JSON 변환 라이브러리를 사용하여 객체를 JSON 형식으로 변환한다. 따라서 스프링 컨트롤러에서 객체를 반환할 때 @ResponseBody를 사용하면 해당 객체가 JSON으로 변환되어 클라이언트로 전송된다.

## 24. 1. 10

## Vue.js

1.  데이터 바인딩은 데이터와 화면 간의 동기화를 쉽게 관리할 수 있도록 해주는 기능이다.
    Vue.js의 데이터 바인딩은 데이터를 화면에 표시하고, 사용자 입력 또는 데이터 변경에 따라 화면을 업데이트하는 과정을 자동화하는 데 도움을 준다. 이를 통해 애플리케이션의 상태와 UI를 일관되게 유지하고 사용자 경험을 향상시킬 수 있다.

2.  Vue.js에서 데이터 바인딩은 크게 단방향 바인딩과 양방향 바인딩으로 나뉜다.

- 단방향 바인딩 (One-Way Binding):
  단방향 바인딩은 데이터의 변경이 화면에 반영되는 방향이 한쪽으로만 진행된다.
  즉, 데이터를 화면에 표시하는 것은 가능하지만 화면에서의 변경은 데이터에 영향을 주지 않는다.
  주로 {{ }} 또는 v-bind 디렉티브를 사용한다.
  사용자 입력 등으로 데이터를 변경하려면 JS 코드를 통해 데이터를 업데이트해야 한다.

- 양방향 바인딩 (Two-Way Binding):
  양방향 바인딩은 데이터와 화면 간의 변경이 양쪽으로 동시에 이루어진다. 데이터 변경에 따라 화면이 업데이트되고, 화면에서의 변경도 데이터에 반영된다.
  주로 v-model 디렉티브를 사용하여 사용자 입력과 데이터를 양방향으로 바인딩하는 데에 적용된다.
  사용자가 입력 필드 등에 값을 입력하면 데이터가 자동으로 업데이트되며, 데이터를 변경하면 화면에 반영된다.

3. 단방향/양방향 데이터바인딩 예시

- 단방향 바인딩 (One-Way Binding)
  가정: 인터넷 게시판에서 게시물 목록을 보여주는 경우
  단방향 바인딩을 사용하면 서버에서 게시물 목록 데이터를 가져와서 화면에 출력한다.
  사용자는 게시물 목록을 화면에서 볼 뿐이며, 화면에서 게시물을 직접 수정할 수 없다.
  데이터 변경이 필요한 경우, 관리자 또는 글쓴이가 서버에서 게시물을 수정하고, 수정된 데이터가 화면에 다시 출력된다.

양방향 바인딩 (Two-Way Binding)
가정: 인터넷 게시판에서 게시물 목록을 보여주고, 사용자가 게시물을 직접 수정할 수 있는 경우
양방향 바인딩을 사용하면 서버에서 게시물 목록 데이터를 가져와서 화면에 출력한다. 동시에 사용자가 화면에서 게시물을 클릭하고 수정할 수 있다다.
사용자가 화면에서 게시물을 수정하면 해당 변경 사항이 자동으로 데이터에 반영됩니다.
즉, 게시물 목록을 양방향으로 바인딩했으므로 화면과 데이터 간에 동기화가 이루어진다.
데이터 변경이 필요한 경우, 사용자가 화면에서 게시물을 수정하면 해당 변경 사항이 서버로 전달되어 저장된다.
이로써 다른 사용자가 동일한 게시물을 업데이트한 경우 모든 사용자에게 변경 내용이 반영된다.
양방향 바인딩을 사용하면 사용자와 데이터 간의 실시간 상호 작용이 가능하다.

4. prefetch, lazyload, 비동기 컴포넌트
   Prefetch (사전 로딩)
   설명: Prefetch는 사용자가 앱을 실행하거나 특정 페이지로 이동하기 전에 필요한 리소스를 미리 로드하는 기술이다.
   Vue Router에서 사용할 수 있다.
   예를 들어, 사용자가 다음 페이지로 이동할 때 해당 페이지의 리소스를 미리 로드하여 페이지 로딩 시간을 단축시킬 수 있다.

장점:
사용자 경험 향상: 페이지 이동 시 로딩 시간 감소로 빠른 응답성을 제공
미리 로드된 리소스는 브라우저 캐시에 저장되므로 나중에 사용될 때 재로드할 필요가 없어 네트워크 대역폭을 절약

단점:
미리 로드할 리소스가 많은 경우 초기 로딩 시간이 증가
필요하지 않은 리소스를 사전 로드하면 리소스 낭비가 발생

---

Lazy Loading (지연 로딩)
설명: Lazy Loading은 앱이나 웹 페이지의 초기 로딩 시 모든 컴포넌트를 로드하는 대신, 사용자가 접근하려는 컴포넌트만 필요할 때 동적으로 로드하는 기술이다. 이로써 초기 페이지 로딩 시간을 줄이고 앱의 성능을 향상시킬 수 있다.

장점:
초기 로딩 시간 감소: 사용자가 접근하지 않는 컴포넌트를 로드하지 않아 초기 로딩 시간을 단축
성능 향상: 불필요한 리소스 로딩을 방지하여 앱의 성능을 최적화

단점:
사용자가 처음 접근하는 페이지의 컴포넌트를 로딩할 때 약간의 지연이 발생
코드 스플리팅 및 관리가 필요하며, 개발자가 어떤 컴포넌트를 어떻게 로드할지 고려해야 함

---

비동기 컴포넌트 (Asynchronous Components)
설명: 비동기 컴포넌트는 Vue.js에서 컴포넌트를 동적으로 로드하는 방법이다.
주로 import() 함수를 사용하여 비동기적으로 컴포넌트를 로드하고, 이를 Vue Router와 함께 사용할 수 있다.

장점:
필요한 컴포넌트만 로드하여 초기 로딩 시간을 최적화
코드 스플리팅을 통해 번들 크기를 줄이고 앱의 성능을 향상
더 나은 사용자 경험을 제공

단점:
비동기 컴포넌트를 사용하려면 추가 설정 및 코드 작성이 필요하며, 초기 학습 곡선이 존재
코드 스플리팅 및 컴포넌트 로딩 관리가 필요

5. prefetch와 LazyLoading

- 차이점
  Prefetch는 사용자가 이동할 페이지의 리소스를 미리 로드하여 초기 로딩 시간을 단축시키고 사용자 경험을 향상시키는 것에 중점을 둔다.

Lazy Loading은 초기 페이지 로딩 시 필요한 컴포넌트만 로드하고, 사용자가 특정 페이지로 이동할 때 해당 페이지의 컴포넌트를 동적으로 로드하여 초기 로딩 시간을 최적화하고 번들 크기를 줄이는 데 사용된다.

- 공통점
  비동기 컴포넌트 관련 개념이다.

## 24. 1. 11

## Vue.js

1. optional<Member>: Optional<Member>는 값의 존재 여부를 명시적으로 나타낸다.
   즉, 값이 있을 때는 Optional 객체 안에 실제 Member 객체가 포함되고, 값이 없을 때는 Optional 객체 자체가 비어있는 상태이다. 이렇게 함으로써 클라이언트 코드에서 회원 객체가 존재하지 않을 경우에 대한 처리를 명확하게 할 수 있다.

2. 일반 Member: 일반 Member 객체는 단순히 회원 정보를 나타내는 객체로, 값이 없을 때를 구분하지 않는다. 만약 메소드에서 null을 반환하거나 회원 객체를 찾지 못한 경우, 클라이언트 코드에서 null 처리를 해야 한다. 이렇게 하지 않으면 NullPointerException 등의 예외가 발생할 수 있다.

## SpringBoot

1. 일반적인 애플리케이션의 구조는 컨트롤러, 서비스, 도메인, 리포지토리(+DB)로 이루어진다.

2. 메모리 구현체(memory implementation 또는 memory backend)는 데이터를 저장하고 관리하기 위한 메모리 기반의 데이터 저장소다.

3. isEqualto()는 두 객체의 타입이 동일해야 정상적으로 이루어진다.

4. Optional<클래스>의 인스턴스인 instance를 Optional이 아닌 클래스의 객체로 만들려면 .get()을 붙이면 기존 클래스의 객체로 쓸 수 있게된다.

5. orElse() 메서드를 사용하면 Optional 객체가 비어있는 경우에는 지정한 대체값을 반환하며, 비어있지 않은 경우에는 Optional 객체 내부의 값을 반환한다.

6. @AfterEach : 한번에 여러 테스트를 실행하면 메모리 DB에 직전 테스트의 결과가 남을 수 있다. 이렇게 되면

다음 이전 테스트 때문에 다음 테스트가 실패할 가능성이 있다. `@AfterEach` 를 사용하면 각 테스트가 종료될 때 마다 이 기능을 실행한다. 여기서는 메모리 DB에 저장된 데이터를 삭제한다.

7. 테스트는 각각 독립적으로 실행되어야 한다. 테스트 순서에 의존관계가 있는 것은 좋은 테스트가 아니다. 그래서 Junit의 테스트 케이스의 순서는 무작위다. 왜냐하면 개별 테스트 메서드 간에는 의존성이 없어야 하기 때문이다.

## 2024. 1. 14

## Vue.js

1. 문자열 데이터 바인딩: raw html, text, number등을 바인딩할 수 있다.

2. 클래스 바인딩: 클래스 바인딩 할 때 주의할 점은 반드시 적용해야 하는 클래스는 기존html에서 
   사용하던 방식처럼 class 속성에 클래스명을 입력하면 되고, 조건에 따라 바인딩할 클래스​​의 경우에는
   v-bind:class를 이용하여 추가적으로 정의해서 사용할 수 있다는 것이다.
   다른 속성의 경우 하나의 속성만을 이용해서 바인딩 해야 하지만 클래스의 경우는 기본 클래스와 데이터 바인딩
   처리를 하는 클래스를 공존해서 사용할 수 있다.

3. 인라인 스타일 바인딩: 데이터를 오브젝트로 선언해서 바인딩할 수 있다. (배열로도 바인딩 할 수 있다.)

4. 리스트 랜더링(v-for)은 다중 데이터 및 반복적인 객체를 처리할 때 사용한다.

5. 리스트 랜더링 할 때 효율적으로 업데이트를 관리하기 위해서 각 항목에 고유한 키를 부여한다.

6. style scoped 속성을 사용하면 해당 스타일이 특정 컴포넌트 내에서만 유효하도록 지정한다.

7. v-if와 v-show는 조건에 따라 랜더링하는 방식이다. v-if는 조건을 만족하면 html 블록이 생성되고, 만족하지 않으면 html 블록은 삭제된다. 하지만 v-show는 조건 만족 여부와 상관없이 무조건 html 블록이 생성되며, 조건을 만족하면 css의 display를 이용해서 화면에 보이게 되고, 조건을 만족하지 않으면 숨긴다. 즉, 무조건 랜더링은 되는 것이다.

8. 따라서 실무에서는 v-if와 v-show을 사용할 때는 해당 html 블록이 화면 내에서 자주 toggle이 일어나면 v-show을 사용하고, toggle이 일어나는 빈도가 작다면 v-if를 사용하는 것이 좋다.

9. v-on 또는 @로 이벤트를 처리할 수 있다. 가장 대표적인 예시로는 @click이 있다.

10. change 이벤트가 가장 많이 사용되는 Html 태그는 select다.
    사용자가 select에서 옵션을 바꿀 때마다 change가 발생한다.

11. key 이벤트란, 사용자가 키보드 자판을 입력할 때 발생하는 이벤트다.

12. computed는 기존에 정의된 데이터 값을 기반으로 새로운 데이터 값을 활용하기 위해 사용된다면, watch는 watch에 정의된 데이터 값 하나만을 감시하기 위한 용도로 사용된다.

## 2024. 1. 18

## SpringBoot

1. 스프링의 의존관계를 등록하는 방법에는 2개가 있다.
   a. 컴포넌트 스캔과 자동 의존관계 설정
   b. 자바 코드로 직접 스프링빈 등록하기

2. 인터페이스는 2개 이상의 클래스를 상속(extends)할 수 있다.

3. 생성자에 @Autowired 가 있으면 스프링이 연관된 객체를 스프링 컨테이너에서 찾아서 주입해준다. (생성자에 autowired를 작성하면 멤버서비스를 스프링이 스프링 컨테이너에 있는 멤버서비스를 가져다가 연결을 시켜준다.)
   참고로 생성자가 1개만 있으면 @Autowired 는 생략할 수 있다.

4. Controller는 스프링이 제공하는 컨트롤러여서 스프링 빈으로 자동 등록된다.
   @Controller를 작성하면 자동 등록된다.

5. 컴포넌트 스캔이란, 스프링이 스프링 빈으로 등록될 준비 된 클래스들 스캔해 빈으로 등록해주는 과정이다.
   @Controller, @Service, @Repository 어노테이션을 클래스 위에 붙임으로서 스프링 빈으로 등록할 수 있다.
   또는 @Component 를 작성해도 되긴 하는데 가독성을 위해 보통 전자처럼 나누어서 작성한다.

6. 스프링은 스프링 컨테이너에 스프링 빈을 등록할 때, 기본으로 싱글톤으로 등록한다.

7. 자바 코드로 스프링 빈을 등록하려면 클래스 위에 @Configuration을 붙이고,
   그다음 스프링 빈에 등록할 클래스들을 작성하고 @Bean을 위에 덧붙이면 완성이다.
   하지만 컨트롤러는 직접 등록할 수 없다.

8. 스프링 빈(Spring Bean)은 스프링 프레임워크에서 관리하는 객체다.
   스프링은 빈을 생성하고, 관리하며, 주입하며, 소멸하는 라이프사이클을 관리한다.
   Bean은 스프링 컨테이너에 의해 생성되고 관리되므로 개발자가 직접 객체를 생성하고 관리할 필요가 없어진다.

9. 실무에서는 주로 정형화된 컨트롤러, 서비스, 리포지토리 같은 코드는 컴포넌트 스캔을 사용한다.
   그리고 정형화 되지 않거나, 상황에 따라 구현 클래스를 변경해야 하면 설정을 통해 스프링 빈으로 등록한다.

10. hello.hellospring 패키지를 포함해서 이 하위 폴더들은 자동으로 스프링이 다 뒤져서 스프링빈으로 등록한다. 만약 동일 패키지가 아니거나 하위 패키지가 아닌 애들은 스프링빈으로 컴포넌트 스캔을 하지 않는다.

## 2024. 1. 18

## SpringBoot

1. DataSource: DataSource는 데이터베이스와의 연결을 관리하고, 애플리케이션이 데이터베이스에 접근할 수 있도록 하는 객체이다. 주로 커넥션 풀링을 추상화하고, DB연결을 도와준다. JDBC 사용시 꼭 주입해야 한다.

2. Connection Pool: 웹 컨테이너(WAS)가 실행되면서 DB와 미리 connection(연결)을 해놓은 객체들을 pool에 저장해두었다가. 클라이언트 요청이 오면 connection을 빌려주고, 처리가 끝나면 다시 connection을 반납받아 pool에 저장하는 방식

3. JdbcTemplate은 JDBC 코어 패키지의 중앙 클래스로 JDBC의 사용을 단순화하고 일반적인 오류를 방지하는데 도움이 된다. 개발자가 JDBC를 직접 사용할 때 발생하는 다음과 같은 반복 작업을 대신 처리해준다.

a.커넥션 획득
b.statement를 준비하고 실행
c.결과를 반복하도록 루프를 실행
d.커넥션 종료, statement 및 resultset 종료
e.트랜잭션을 다루기 위한 커넥션 동기화
f.예외 발생 시 스프링 예외 변환기 실행

4. 메모리 형태의 레포지토리를 jdbc 파일로 옮기는 과정은 OCP 원칙을 따른다.

5. 스프링 통합 테스트란, 스프링을 실행하여 테스트 하는 것이다.

- @SpringBootTest : 스프링 컨테이너와 테스트를 함께 실행한다.
- @Transactional : 테스트 케이스에 이 애노테이션이 있으면, 테스트 시작 전에 트랜잭션을 시작하고, 테스트 완료 후에 항상 롤백한다. 이렇게 하면 DB에 데이터가 남지 않으므로 다음 테스트에 영향을 주지 않는다.

## 2024. 1. 19

## SpringBoot

1. JPA는 자바 진영에서 데이터를 영구적으로 저장하기 위한 표준 인터페이스를 제공하는 API다. 구현은 여러 업체들이 한다. 업체들 중 Hibernate를 가장 많이 쓴다.
   JPA는 데이터베이스와의 상호 작용을 객체지향적인 방식으로 다룰 수 있게 해주며, 데이터베이스에 대한 복잡한 SQL 쿼리 및 트랜잭션 처리를 개발자 대신에 처리해준다.

2. JPA를 사용하면, SQL과 데이터 중심의 설계에서 객체 중심의 설계로 패러다임을 전환을 할 수 있다.
   기존의 반복 코드는 물론이고, 기본적인 SQL도 JPA가 직접 만들어서 실행해준다.

3. @Identity: 해당 클래스가 JPA 아이덴티티임을 나타내는 어노테이션
   @Id: 해당 필드(id)가 primary key임을 나타냄
   @GeneratedValue(strategy = GenerationType.IDENTITY) : 주키(PK)의 생성 전략을 지정하는 어노테이션.

4. EntityManager: EntityManager는 JPA에서 엔터티를 관리하는 핵심 인터페이스다. 엔터티 매니저는 영속성 컨텍스트를 관리하고 엔터티의 상태를 추적한다. JPA는 EntityManager라는 걸로 모든 게 동작한다. 주로 레포지토리(JpaMemberRepository)에서 주입받으며, em이라는 이름으로 자주 사용한다.

5. @Entity: @Entity 어노테이션은 엔터티 클래스를 나타내며, 이 클래스의 객체가 JPA에서 관리되는 엔터티라는 것을 나타낸다.

6. JpaRepository에 들어가보면 save(), findAll(), findById(), delete() 등의 메소드가 구현되어있다.

7. 스프링 데이터 JPA 제공 기능

- 인터페이스를 통한 기본적인 CRUD
  `findByName()` , `findByEmail()` 처럼 메서드 이름 만으로 조회 기능 제공
- 페이징 기능 자동 제공

8. 실무에서는 JPA와 스프링 데이터 JPA를 기본으로 사용하고, 복잡한 동적 쿼리는 Querydsl이라는 라이브러리를 사용하면 된다. Querydsl을 사용하면 쿼리도 자바 코드로 안전하게 작성할 수 있고, 동적 쿼리도 편리하게 작성할 수 있다. 이 조합으로 해결하기 어려운 쿼리는 JPA가 제공하는 네이티브 쿼리를 사용하거나, 앞서 학습한 스프링 JdbcTemplate를 사용하면 된다.

9. AOP는 공통된 기능을 재사용하는 기법으로써, 핵심 관심 사항(core concern)과 공통 관심 사항 또는 부가기능 (cross-cutting concern)을 분리하는 기술이다.

10. 업무(Biz) 로직을 포함하는 기능을 핵심 기능,핵심기능을 도와주는 부가적인 기능(로깅,보안 등)을 부가기능이라고 한다.

11. AOP의 장점:
    회원가입, 회원 조회등 핵심 관심사항과 시간을 측정하는 공통 관심 사항을 분리한다.
    시간을 측정하는 로직을 별도의 공통 로직으로 만들었다.
    핵심 관심 사항을 깔끔하게 유지할 수 있다.
    변경이 필요하면 이 로직만 변경하면 된다.
    원하는 적용 대상을 선택할 수 있다.

## 2024.01.31

## Spring

1. @RequestBody, @RequestParam, @PathVariable 등은 모두 HTTP 요청에서 특정 데이터를 추출하는 역할을 수행하는 Spring Annotation이다.
   그러나 각각 추출하는 데이터의 위치와 방식은 다르다.

@RequestParam: HTTP 요청 파라미터에서 데이터를 추출한다. 쿼리 스트링(query string, URL 뒤에 ?key=value 형태로 붙는 부분)에서 데이터를 가져온다.
@PathVariable: HTTP 요청 URL의 경로 부분에서 데이터를 추출한다. URL 템플릿에 지정된 변수 부분을 가져온다.
@RequestBody, @ResponseBody: HTTP 요청 본문(Body)에서 데이터를 추출한다. 주로 POST, PUT과 같은 메서드에서 JSON 형태의 복잡한 데이터를 주고받을 때 사용한다.

2. @RequestBody를 사용할 때는 생성자와 클래스(안에 생성자, getter, setter 필수)를 만들어줘야 제대로 작동한다.

3. 객체를 JSON으로 변환하는 과정은 다음과 같다. 스프링의 @RestController 어노테이션을 사용한 컨트롤러는 반환하는 클래스 객체를 'Jackson' 라이브러리를 통해 JSON으로 변환하여, 이를 HTTP 응답 본문에 직접 쓰게 되어, 클래스를 반환하는 것이 JSON을 반환하는 것으로 처리된다.

4. @RequestBody 어노테이션은 HTTP 요청의 본문(body)을 처리하는 데 사용된다. 본문은 HTTP 요청의 페이로드 데이터를 나타내며, GET보다는 주로 POST 또는 PUT 요청과 함께 전송된다.

5. Content-Type은 HTTP 헤더에서 사용되며, 보내는 콘텐츠의 타입을 알려준다.

6. @Entity 어노테이션이 붙어 있으면 JPA가 그 클래스를 데이터베이스 테이블과 연결되는 엔티티로 인식한다.

7. Repository 클래스는 데이터베이스와의 상호작용을 담당하는 인터페이스 또는 클래스다.
   주로 Spring Data JPA와 함께 사용(extends JpaRepository)되며, 엔터티에 대한 CRUD 작업을 수행합니다.
   데이터베이스 조작을 추상화하고, JPA를 사용하여 엔터티에 접근합니다.

8. JpaRepository를 상속하는 Repository 인터페이스(또는 클래스)는 기본제공함수를 통해 Entity를 CRUD 할 수 있다.

9. @Transactional은 Service의 메소드에 붙여야한다.
   @Transactional 어노테이션은 트랜잭션 범위에서 실행되는 코드를 정의하는 데 사용된다. 이 어노테이션을 메서드에 붙이면, 그 메서드가 실행되는 동안 수행되는 모든 데이터베이스 작업이 단일 트랜잭션으로 묶인다. 만약 어떤 문제가 발생하여 예외가 발생하면, 해당 트랜잭션은 롤백되며, 이전 상태로 복원된다. 이를 Service 계층에 적용하는 이유는, Service 계층이 여러 Repository를 조합하여 복잡한 비즈니스 로직을 처리하는 역할을 하기 때문이다.

## 2024.2.1

## Spring

1. GET/DELETE 메소드를 사용할 때는 {}는 response의 본문이고,
   POST/PUT 메소드를 사용할 때는 {}는 request의 본문이다.

2. @RequestBody의 역할은JSON 형태의 데이터(RequestBody)를 자바 객체로 변환하는 것이다.

3. 보통 @Requestbody(전달받을 데이터)는 따로 클래스를 만들어서 사용하며,
   사용하는 이유는 데이터를 효율적으로 관리하기 위함이다.

4. 빌더 패턴(Builder Pattern)은 복잡한 객체의 생성 과정과 표현 방법을 분리하여 다양한 구성의 인스턴스를 만드는 생성 패턴이다. 생성자에 들어갈 매개 변수를 메서드로 하나하나 받아들이고 마지막에 통합 빌드해서 객체를 생성하는 방식이다. 빌더 패턴은 생성해야 되는 객체가 Optional한 속성을 많이 가질 때 빛을 발휘한다.

5. Spring 프레임워크에서 Repository 인터페이스는 일반적으로 데이터베이스와의 상호 작용을 담당한다. 이 인터페이스는 데이터베이스로부터 데이터를 가져오고, 데이터를 저장하고, 데이터를 업데이트하고, 데이터를 삭제하는 등의 기능을 제공한다.

## 2024.2.1

## Spring

1. Entity, Repository, Service, API(Controller)의 작업 순서는 유동적이지만, 보통 아래와 같은 순서대로 작업한다.

a. Entity 및 Repository 작성: 데이터베이스와의 상호작용을 위한 엔터티 및 리포지토리를 먼저 작성합니다.
b. Service 작성: 데이터베이스와의 상호작용을 통해 비즈니스 로직을 처리하는 서비스를 작성합니다.
c. Controller 작성: 클라이언트의 요청을 받아 서비스를 호출하고 응답을 반환하는 컨트롤러를 작성합니다.

2. 검증기능에서 orElseThrow()를 자주 쓴다.

3. /review/123와 같은 URL이 있을 때, 123은 reviewId 변수에 매핑되어 해당 메서드에 전달된다.

4. 읽기만 하는 생성이나 수정 삭제 없는 메소드에서는 Transactional은 필수가 아니다. 또는 readOnly = true로 설정해줘도 되기는 하다.

## 알고리즘

1. new 키워드를 사용하여 배열을 만들면 메모리 상에 새로운 배열 객체가 동적으로 할당된다. 이때 할당된 메모리는 Heap 영역에 위치하게 된다.

2. 정적으로 할당(Static Allocation):
   컴파일 시간에 메모리가 할당되며, 프로그램이 실행되기 전에 크기가 결정됨
   정적으로 할당된 메모리는 프로그램의 생명 주기 동안 일정함

동적으로 할당(Dynamic Allocation):
런타임 시간에 메모리가 할당되며, 프로그램이 실행 중에 크기가 동적으로 결정됨
동적으로 할당된 메모리는 프로그램이 실행 중일 때만 존재하며, 사용이 끝나면 명시적으로 해제해야 함

3. i <= count로 설정하는 것은 피하자. 배열의 범위를 벗어나지 않도록 안전하게 코드를 작성하기 위해서는 i < count를 유지하고, num2를 포함하려면 count를 num2 - num1 + 1로 설정하는 것이 좋다.

4. length는 1부터 시작한다.
   배열 또는 String의 length, length()는 1부터 시작한다.
   0부터 시작하는 인덱스와 헷갈린 것이다.

5. [length - i - 1] 을 활용하면 Array의 인덱스를 뒤집을 수 있다.

6. Collections.reverse() 함수를 사용하면 List를 쉽게 뒤집을 수 있다. 단, Array가 아닌 List 전용이다. 따라서 사용 이전에 자료형이 List인지 확인하자. 또한 Collections.reverse()를 사용하는 것이 속도도 더 빠르다.
