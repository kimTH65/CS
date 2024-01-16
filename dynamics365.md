<h1>dynamics365</h1>
CRM(Customer Relationship Management) : <br>
회사의 고객 관련 정보를 관리,추적,저장하도록 지원하는 일련의 데이터 기반 소프트웨어가 통합된 솔루션 (고객 관계 관리 시스템) <br><br>

dynamics365（CRM） URL：
https://dynamics.microsoft.com/ja-jp/dynamics-365-free-trial/<br>

dynamics365 sals : 동료 데이터, 고객 데이터, 상황별 고객 데이터를 모두 통합해주는 엔터프라이즈 협업 허브를 통해 가상 공간의 참여 활동을 조정<br>

Dynamics365のSales開発者ガイド: https://learn.microsoft.com/ja-jp/dynamics365/sales/developer/developer-guide<br>

https://kageura.hatenadiary.jp/entry/2015/04/17/190000<br>

https://learn.microsoft.com/ja-jp/power-apps/developer/data-platform/register-plug-in
<hr>
<h3>Entity</h3>

 - Dynamics365のentityはMicrosoft Dataverseを利用している 
 - Microsoft Dataverseは普通DBと違い、開発者がデータと対話することがでできるようにする Web サービス 
 - 開発者向けドキュメントでは、場合によって、Power Appsユーザーインターフェイスとは異なる用語を使用
 
![image](https://github.com/kimTH65/cs/assets/59690816/d886091e-1731-41b9-8786-cfcb178c2e62)

<hr>
<h3>Script를 사용하는 부분</h3> 

 - 참고 : https://www.youtube.com/watch?v=tUdL5YZA29A
 - Workflows -> 프로세스 자동 기능에서 사용
 - WebPage, Form -> JavaSciprt를 삽입하여 필드 유효성 검사, 연산, 이벤트 핸들링 등을 구현
 - Plugins -> 데이터의 변경사항 감지하고 이에 대해 반응, C#이나 .NET을 이용해 플러그인 작성
 - Custom Action -> 사용자 정의 기능 추가하기 위해 REST나 SOAP를 사용하여 실행가능한 액션을정의
 - Web Resources -> 웹 자원을 저장하는데 사용
 - Processes -> 비즈니스 프로세스 흐름을 정의
 - Power Apps -> 사용자 정의 기능 추가 

<hr>

 - nuget패키지
 - ソリューション : カスタマイザーと開発者が Dynamics 365 for Customer Engagement を拡張する単体ソフトウェアを作成、パッケージ化、および保守する方法です。
 - フロー : データを一貫して入力し、顧客と作業するたびに同じステップを実行するように確認することができます。

플러그인 완료