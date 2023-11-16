
<h2> Clean Architecture</h2>

<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/img/CleanArchitecture.jpg">
<h6>출처 : https://blog.cleancoder.com/</h6>
</div>

<br>
<h4>원 안쪽으로 향해서만 의존하며 , 바깥쪽 원은 안쪽 원에 영향을 주면 안된다.<br>
(円の内側に向かってのみ依存し、外側の円は内側の円に影響を与えてはならない。)
</h4>
<h6>
<a>　　</a>- Entity : 데이터 구조, 함수 집합, 핵심 업무 규칙을 캡슐화, 가장 변하지 않고 영향을 받지않는다.<br>
<a>　　　　　　</a>(データ構造、関数集合、コアワークルールをカプセル化、最も変わらず影響を受けない)
<br><br>
<a>　　</a>- Use Cases : 비즈니스 규칙, 업무 규칙, 데이터의 흐름을 정의<br>
<a>　　　　　　　　</a>(ビジネスルール、業務ルール、データの流れを定義)
<br><br> 
<a>　　</a>- Interface Adapters : mvp의 presenter, mvvm 의 viewmodel 등, 순수한 비즈니스 로직<br>
<a>　　　　　　　　　　　　</a>(mvp の presenter, mvvm の view model など、純粋なビジネスロジック)
<br><br> 
<a>　　</a>- Frameworks & Drivers : 프레임워크,데이터베이스,UI 등<br>
<a>　　　　　　　　　　　　　</a> &nbsp(フレームワーク、データベース、UI など)
</h6> 
<br>

<h4>장점(長所)</h4>
<h5>
 - 이해/개발/유지/배포를 더욱 쉽게 -> 더욱 유연하고 부드럽게<br>
<a>　</a>(理解/開発/維持/配布をより簡単に -> より柔軟でスムーズに)
</h5>
<h6>
 - 각 계층을 명확하게 분리되어 테스트와 유지 보수가 용이해짐<br>
<a>　</a>(各階層を明確に分離し、テストとメンテナンスが容易になる)
<br><br> - 인터페이스에 대한 의존성이 없어져 인터페이스가 바뀌더라도 클라이언트는 영향이 없음<br>
<a>　</a>(インターフェイスへの依存性がなくなり、インターフェイスが変わってもクライアントは影響なし)
<br><br> - 기조 계층형 아키텍처가 가지던 데이터베이스에 대한 의존성이 없어지면서 데이터베이스 없이도 다른 부분을 개발 가능<br><a>　</a>(基調階層型アーキテクチャが持っていたデータベースへの依存性がなくなり、データベースなしでも他の部分を開発可能)
</h6> 
<br>


<div align="center">
<h4>안드로이드 + 클린아키텍처 구조<br>
(アンドロイド+クリーンアーキテクチャ構造)
</h4>
<img src="https://github.com/kimTH65/cs/blob/main/img/cleanAnd.png">
<h6>출처 : https://qiita.com/koutalou/items/07a4f9cf51a2d13e4cdc</h6>
 </div>

