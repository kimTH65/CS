
# SOLID (Object Oriented Design) - 객체지향 5대 원칙


<h2> SRP(단일 책임 원칙)</h2>

<h6>
<br> Single Responsiblity Principle, 하나의 클래스는 하나의 책임(기능)을 가져야 한다.
<br><br>&emsp;&emsp;&emsp;&emsp; Why? 여러가지 기능이 많아지면 응집도가 높아지며, 유지보수에 비용이 증가된다. 변화에 대한 적응성 획득
</h6>

<br>
<br>

<h2> OCP(개방-폐쇠 원칙)</h2>

<h6>
<br> Open-Closed Principle, 기존 코드를 변경하지 않고 기능을 수정하거나 추가할 수 있도록 설계해야 한다, interface 자주사용
<br><br>&emsp;&emsp;&emsp;&emsp; Why? 코드 수정을 최소화하여 결합도를 줄이고 응집도는 높임.
</h6>

<br>
<br>

<h2> LSP(리스코프 치환 원칙)</h2>

<h6>
<br> Liskov Substitution Principle, 자식클래스는 부모클래스와 언제나 호환될 수 있어야한다.
<br><br>&emsp;&emsp;&emsp;&emsp; Why? 다형성을 통한 확장의 원리인 OCP 제공, 다형성을 통한 확장성 획득
</h6>

<br>
<br>

<h2> DIP(의존 역전 원칙)</h2>

<h6>
<br> Dependency Inversion Principle, 객체가 구현체에 의존하지 않고, 인터페이스(추상 클래스)를 통해 인스턴스를 할당받게 함
<br><br>&emsp;&emsp;&emsp;&emsp; Why? 복잡한 컴포넌트간 커뮤니케이션 관계를 단순화 하기 위함
</h6>

<br>
<br>

<h2> ISP(인터페이스 분리 원칙)</h2>

<h6>
<br> Interface Segregation Principle, 한 클래스는 자신이 사용하지 않는 인터페이스를 구현하지 않아야 한다.
<br><br>&emsp;&emsp;&emsp;&emsp; Why? 인터페이스 분리를 통해 의존성을 낮추고 변화에 대한 적응성 획득
</h6>

<br>
<br>

