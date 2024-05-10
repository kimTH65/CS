<h1>dynamics365</h1>

<h3>사용경험</h3>

 - 세큐리티 룰, 솔루션, 엔티티, 폼, 뷰
 - xml, 외부연결
 - 폼, 테이블 수정
 - 외부연결, azure, Power AutoMate, Script, Plugin, 외부패치설계/계발

<h3>Memo</h3>

 - CRM(Customer Relationship Management) : 고객 관계 관리 시스템 <br>
 - dynamics365（CRM） URL：
 - https://dynamics.microsoft.com/ja-jp/dynamics-365-free-trial/<br>
 - Dynamics365のSales개발자 가이드: https://learn.microsoft.com/ja-jp/dynamics365/sales/developer/developer-guide<br>
 - https://kageura.hatenadiary.jp/entry/2015/04/17/190000<br>
 - https://learn.microsoft.com/ja-jp/power-apps/developer/data-platform/register-plug-in
 - 플러그인을 Visual Studio에서 사용 시 nuget패키지를 이용하여 관련 라이브러리를 설치
 - Back = 워크플로우/플러그인, Front = 비즈니스룰/스크립트
 - 세큐리티 룰,솔루션,엔티티,폼,뷰
 - xml , 외부연결
 - 폼,테이블 수정
 - 외부연결, azure
 - 
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
<h3> fetch xml</h3>

 - linked-entity
 - group by
 - entity collection
```
```
<hr>

### 사용기술, 작성예정 

 - context,onsave , alert,oncreate,PREVENT SAVE
 - executionContext.getEventArgs().preventDefault();
 - tabs.set : 텝을 기준으로 액션 설정 가능, 비즈니스룰에서도 탭을 트리거로 설정가능

