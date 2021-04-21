TIL - 0325
그래들은 빌딩해주는 애
wrapper가 있는데 라이브러리 관리해줌

빌드 그래들에 프로젝트랑 모듈이랑 나뉨.
프로젝트 전역에 대한 설정 - 프로젝트 빌드 그래들 언어 같은거
모듈의 프로젝트 빌드 그래들이 이제 세부 설정. 

build variants
그럼 빌드 variants 에서 릴리즈 디버그 이외에 유료모델은 거기서 관리가 되는건가?

R이라는 ? 애가 리소스를 관리하는 거

그냥 test는 코드 테스트용
안드test는 db같은 안드로이드 자원을 가져다 쓰면서 진행함.
intent - filter 액티비티가 다른 액티비티를 호출할 때 쓰임! 근데 없어지면 디폴트가 없다고 함.

2주차 질문
1. kotlin eventlog 에서 importantForAccessibility를 no로 하는게 무슨의미인가?
-> 굳이 이미지에 대해 설명하지 않겠따! 라고 하는거

2. val 이랑 int랑 차이? python 에서는val를 안썻음..
    val myFirstDice = Dice(6)
    val diceRoll = myFirstDice.roll()
    val의 의미란? 왜 굳이 integer을 val 형으로 사용할까?

값이라고 칭하는 것. 바뀌지 않도록 var는 바뀔 수 있음.

3. Notice that there is no main() function in your MainActivity. 이래서 객체지향? 프로그래밍이라고 하는건가요?

4. Add unambiguous imports on the fly and Optimize imports on the fly (for current project) are checked 무슨의미..?
자동으로 library..? 같은 걸 import 해주게 하는 것 같긴 한데 맞는건지..?

5. private fun rollDice() {
    val dice = Dice(6)
    val diceRoll = dice.roll()
    val resultTextView: TextView = findViewById(R.id.textView)
    resultTextView.text = diceRoll.toString() <- 이 부분 화면에 띄우는 건가? }

질문 왜 private? 그리고 마지막 2줄.. 뭔지 모르겠으 ㅠㅠ
-> 객체 지향의 주요 특징중 하나 인데 캡슐화를 해가지고..? 내가 공개를 허용하지 않는 변수에 대해서는.. protected or public 접근제한자. 외부에서 접근을 제한하도록..?

먼가 실세계와 비슷하다라고 생각하며 ㄴ된다는데?

6. 혹시 웹 기획 관련해서도 바이블 같은 책.. 한권만! 추천해줄 수 있으신지?
해보고 싶은건 velog.io 같은 걸 해보고 싶은 상황.
각페이지마다 다 기획을 하는 것에 가까움.. 
ux / ui => 웹 개발 클로닝.
그 시장에 가장 잘나가는 애들껄 고대로 다 분석해보고 써보고 이런식으로 장사하는 군 를 접근.. 

라프텔 기획서 같은 경우에는 비즈니스적으로 갈꺼면 철저하게 비즈니스처럼.. 이거 도저히 안될 거 같으면.. 
비전을 좀 맞춰가는 것도 중요함. 내가 아느 사람이니까.. 자금적인 문제도 있고.. 

직원을 볼 때, 가장 잘 봐야할게 자기 성장을 하는가가 가장 중요하고 그리고 말이 통해야 함.
의사소통도 안되는 사람도 있음. 요목조목 말 잘하는 사람을 뽑아라.. !
말이 통하는 친구인가?! 일에 대해서.. 말이 통하는 사람을 찾아라

native 보단 flutter로 본격적으로 

본격적으로 사업이 굴러갈 떄 자신이 한 일을  페이스 조절도 .. ! 
7. 왜 if문 이 아닌.. when문? 이건 뭐지.. 첨봄 자주 쓰이는지?
-> switch를 선언하고 나서..? 각 case 마다 해줘야하는데.. 
kotln에서는 과감이 제외하고 else 처리.. 
unit2 - class 개념 잘 볼 것.

3일차 질문
1. val diceImage: ImageView = findViewById(R.id.imageView) -> 이게 화면 다이스 이미지를 띄우는거? 아니면 
단순히 이미지를 변수에 저장하는 것?

Q1. R.id.imaveView => R class는 빌드툴인 gradle이 생성한 클래스로써 각종 자원에 접근할 수 있는 클래스. 리소스 중에서 layout에 id를 imageView로 설정한 view에 접근할 수 있도록 선언하는 문장입니다

2. 그림은 바뀌는데 contentDescripiton은 뭐가 되는건지 모르겠음? 적힌 거 보면 숫자가 떠야하는데.. 어디에?
// Update the ImageView with the correct drawable resource ID
diceImage.setImageResource(drawableResource)

Q2.의 contentDescription 대한 대답입니다. 
안드로이드에서는 시각장애인들을 위한 기능을 접근성 메뉴를 설정할 수 있습니다. 해당기능을 키고 눌러보시면 tts 음성이 나옵니다

// Update the content description
diceImage.contentDescription = diceRoll.toString()

3. abstract class? class? 무슨 차이? abstract -> override

Q3. 부모클래스로 부터 상속받는 항목을 자식클래스에서 재정의 하는 경우 override라는 키워드를 사용합니다. 
abstract 키워드의 경우 추상클래스로, 추상클래스를 상속받을 때 반드시 구현해야하는 변수, 함수에 사용합니다

4. 왜 여기서는 val 대신 var를 쓰는 건지? 
abstract class Dwelling(private var residents: Int) {
    abstract val buildingMaterial: String
    abstract val capacity: Int
       
    fun hasRoom(): Boolean {
       return residents < capacity
   }
}

Q4. val, var의 경우 읽기 전용 값인지, 읽고 쓰기가 가능한 변수인지 구분할 수 있는 키워드입니다. 
근데 클래스 내에서 val, var의 경우는 조금 특별하게 쓰이는 경우가 있는데, 자바에서 멤버변수를 private로 선언하고 getter, setter 메소드를 선언하는 경우가 있습니다. 
이를 캡슐화라고 하는데, 코틀린에서는 해당 부분을 var, val로 대체하여 사용하기도 합니다. 
해당 클래스에서 private을 사용한것을 봤을 때, 외부로 노출되진 않지만 클래스 내에서 변경될 수 있는 멤버변수라고 생각하시면 됩니다

5주차? 질문
drawable에서
리소스가 자동으로 minimap folder에 할당되는건지?
안드로이드 스튜디오에서 재성성 해준다. 각자 dpi에 따라서

drawable 에서 image asset이랑 vector asset은 무슨 차이인가..?
image 는 안드로이드 프레임워크 내 앱 아이콘 내지 푸쉬 알리미 아이콘
vector cusmotized icons or logos

legacy는 ? -> adaptive는 앱아이콘 자체가 사용자랑 interative 가능한 것. 앱자체가 흔들린다거나 하지만 png 파일로 움직이는 것들은 legacy

재플린 - 디자인 툴? 디자이너가 adobe ai 나 스케치 앱 디자인 툴을 
재플린으로 내보내면 거기서 마진이나 스타일 가이드로 .. 빠르게 찍어냄.

___

TIL - 0421
* kotlin shortcut modifier
    list type에 python 처럼 자동으로 integer 형식을 잡아줄 수 있음.
``` kotlin
val numbers: List<Int> = listOf(1, 2, 3, 4, 5, 6)
val numbers = listOf(1, 2, 3, 4, 5, 6)
```

* mutableList 
    길이를 지정해주지 않아도 계속 adding 가능함.
``` kotlin
val entrees = mutableListOf<String>()
```

* vararg modifier (첨 봤음..)
    > In Kotlin, the vararg modifier allows you to pass a variable number of arguments of the same type into a function or constructor. In that way, you can supply the different vegetables as individual strings instead of a list.

``` kotlin 
class Vegetables(vararg val toppings: String) : Item("Vegetables", 5)
```

* 질문사항
1. vararg 많이 쓰이는지..? 언뜻 보기엔 그냥 List<string>하면 되는거 아닌지?

2. double dollar sgign의 의미는 먼지?

3. 혹시 android studio에서 그냥 따로 kt 파일은 running 할 수 있는지?

4. return this 는 어떻게 되는건지..?\
    > Kotlin provides the keyword this to reference the current object instance. Within the addItem() and addAll() methods, you return the current Order by returning this.