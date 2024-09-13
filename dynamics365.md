<h1>dynamics365</h1>

<h3>사용경험</h3>

 - security roles, solution, entity, form, view, Ribbon, fetch xml, Azure, Power AutoMate, Script, Plugin ...
 - 외부패치설계/계발, 에러처리
 
<h3>Memo</h3>

 - CRM(Customer Relationship Management) : 고객 관계 관리 시스템 <br>
 - https://dynamics.microsoft.com/ja-jp/dynamics-365-free-trial/<br>
 - Dynamics365のSales개발자 가이드: https://learn.microsoft.com/ja-jp/dynamics365/sales/developer/developer-guide<br>
 - https://kageura.hatenadiary.jp/entry/2015/04/17/190000<br>
 - https://learn.microsoft.com/ja-jp/power-apps/developer/data-platform/register-plug-in
 - 플러그인을 Visual Studio에서 사용 시 nuget패키지를 이용하여 관련 라이브러리를 설치
 - Back = 워크플로우/플러그인, Front = 비즈니스룰/스크립트
 - Power automate로 엑셀 이름 바꾸기 : https://www.youtube.com/watch?v=-Z1_43SWboM
 - Power automate json으로 insert, update
 - crm-설정-개인설정-전자메일탭에서 타인메일송신허가설정가능
 - setNotification, setFormNotification다름
 - https://community.powerplatform.com/forums/thread/details/?threadid=79ad26b5-af2f-420d-a5d9-ba96694d483b
 - power automate에서 excel스크립크 실행 가능
 - 어플종류는 모델,캔버스 두가지가 존재
 - executionContext.getEventArgs().preventDefault();
 - tabs.set : 텝을 기준으로 액션 설정 가능, 비즈니스룰에서도 탭을 트리거로 설정가능
 - 모델기반 앱 에서도 캔버스 사용가능
 - 캔버스페이지에 Flow사용
<h3>Entity</h3>

 - Dynamics365のentityはMicrosoft Dataverseを利用している 
 - Microsoft Dataverseは普通DBと違い、開発者がデータと対話することがでできるようにする Web サービス 
 - 開発者向けドキュメントでは、場合によって、Power Appsユーザーインターフェイスとは異なる用語を使用
 
![image](https://github.com/kimTH65/cs/assets/59690816/d886091e-1731-41b9-8786-cfcb178c2e62)



<hr>
<h3>Plugin Memo(C#) - Back_End</h3>

```
// Obtain the tracing service
ITracingService tracingService =
(ITracingService)serviceProvider.GetService(typeof(ITracingService));

// Obtain the execution context from the service provider.  
IPluginExecutionContext context = (IPluginExecutionContext)
    serviceProvider.GetService(typeof(IPluginExecutionContext));

// The InputParameters collection contains all the data passed in the message request.  
if (context.InputParameters.Contains("Target") &&
    context.InputParameters["Target"] is Entity)
{
    // Obtain the target entity from the input parameters.  
    Entity entity = (Entity)context.InputParameters["Target"];

    // Obtain the IOrganizationService instance which you will need for  
    // web service calls.  
    IOrganizationServiceFactory serviceFactory =
        (IOrganizationServiceFactory)serviceProvider.GetService(typeof(IOrganizationServiceFactory));
    IOrganizationService service = serviceFactory.CreateOrganizationService(context.UserId);

    try
    {
        // Plug-in business logic goes here.  
    }

    catch (FaultException<OrganizationServiceFault> ex)
    {
        throw new InvalidPluginExecutionException("An error occurred in FollowUpPlugin.", ex);
    }

    catch (Exception ex)
    {
        tracingService.Trace("FollowUpPlugin: {0}", ex.ToString());
        throw;
    }
 executionContext.getEventArgs().preventDefault();
}
}
```

<hr>
<h3>Java Script Memo - Front_End</h3>

```
function test(ExecutionContext) {
    //콘텍스트 습득
    var executionContext = ExecutionContext.getFormContext();

    //현재열린 텝 확인 로직
    var currentTab = ""
    executionContext.ui.tabs.forEach(tab => {
        if (tab.getDisplayState() === "expanded") {
            currentTab = tab.getName();
        }
    )
    ExecutionContext.ui.getEventArgs().preventDefault();//저장방지

}

```
<hr>
<h3> fetch xml (c#)</h3>

 - MetaData를 이용해서 속성정보 획득가능
 - 멀티쓰레드, sendmail -> mail box
 - group by, aggregate 사용시 row 길이가 50000 까지 정해져 있음 -> dynamics의 config 테이블 설정 해서 limit 수정가능
 - select는 시간이 별로 안걸림 , delete update create가 시간이 많이 걸림
 - 메일이 보내지지 않을경우 dynamics 메일 박스 체크

<hr>
<h3> 자격증 취득 메모</h3>
mb-910<br>
https://www.examtopics.com/exams/microsoft/mb-910/view/6/<br>
https://learn.microsoft.com/en-us/credentials/certifications/d365-fundamentals-customer-engagement-apps-crm/?practice-assessment-type=certification<br>
Dynamics 365 Customer Insights :  프로필을 통합하고 대상 고객의 경험을 조정합니다<br>
Dynamics 365 Sales :  전체 판매 주문 수명 주기 동안 사용자를 효율적으로 지원<br>
Dynamics 365 Customer Service :  전체 고객 지원 수명 주기 동안 에이전트의 사례 관리를 지원<br>
Dynamics 365 Field Service :  고객에게 온사이트 서비스를 제공하고 모바일 인력을 관리하는 데 필요한 도구를 제공<br><br>

Leads : 잠재 고객<br>
quotes : 견적<br>
invoice : 송장<br>
Opportunity : 기회,상담<br>
EntitleMent : 권한<br>
queue : 대기열<br>
Service level agreements(SLA) : 서비스 수준 계약(SLA),서비스 회사와 서비스 고객 간의 계약 <br>


