
<h2> Clean Architecture</h2>

<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/img/CleanArchitecture.jpg">
<h6>출처 : https://blog.cleancoder.com/</h6>
</div>

<br>
<h4>원 안쪽으로 향해서만 의존하며 , 바깥쪽 원은 안쪽 원에 영향을 주면 안된다.</h4>
<h6>
 - Entity : 데이터 구조, 함수 집합, 핵심 업무 규칙을 캡슐화, 가장 변하지 않고 영향을 받지않는다.
<br><br> - Use Cases : 비즈니스 규칙, 업무 규칙, 데이터의 흐름을 정의 
<br><br> - Interface Adapters : mvp의 presenter, mvvm 의 viewmodel 등, 순수한 비즈니스 로직
<br><br> - Frameworks & Drivers : 프레임워크,데이터베이스,UI 등
</h6> 
<br>

<h4>장점</h4>
<h5>
 - 이해/개발/유지/배포를 더욱 쉽게 -> 더욱 유연하고 부드럽게
</h5>
<h6>
 - 각 계층을 명확하게 분리되어 테스트와 유지 보수가 용이해짐
<br><br> - 인터페이스에 대한 의존성이 없어져 인터페이스가 바뀌더라도 클라이언트는 영향이 없음
<br><br> - 기조 계층형 아키텍처가 가지던 데이터베이스에 대한 의존성이 없어지면서 데이터베이스 없이도 다른 부분을 개발 가능
</h6> 
<br>


<div align="center">
<h4>안드로이드 + 클린아키텍처 구조</h4>
<img src="https://github.com/kimTH65/cs/blob/main/img/cleanAnd.png">
<h6>출처 : https://qiita.com/koutalou/items/07a4f9cf51a2d13e4cdc</h6>
 </div>

