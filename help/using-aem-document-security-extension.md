---
title: AEM Document Security Extension for Microsoft Office 사용
description: 배포 범위에 관계없이 받는 사람이 정책으로 보호된 파일을 사용하는 방법을 제어할 수 있습니다. 이 문서에서는 파일을 보호하는 방법과 보호된 파일을 사용하여 작업하는 방법에 대해 설명합니다.
uuid: db4abbc8-eb21-4f4a-9950-224ada95ce66
content-type: reference
topic-tags: using
discoiquuid: f4c2460c-174f-4e4d-b804-1eb051d2781e
translation-type: tm+mt
source-git-commit: 21288f7f1c8f786d3c4c363986226038bdb03e26
workflow-type: tm+mt
source-wordcount: '6270'
ht-degree: 0%

---


# AEM Document Security Extension for Microsoft Office 사용{#using-aem-document-security-extension-for-microsoft-office}

## AEM Document Security Extension {#usingaemdocumentsecurityextensiontoprotectfiles}을(를) 사용하는 Protect 파일

배포 범위에 관계없이 받는 사람이 정책으로 보호된 파일을 사용하는 방법을 제어할 수 있습니다.

Document Security Extension for Microsoft Office를 사용하여 다음 작업을 수행할 수 있습니다.

* Document Security에 연결 구성
* 파일에 정책 적용
* Document Security 웹 페이지를 열어 사용자 정책 만들기 및 관리
* 파일에서 정책 보호 제거
* 파일에 적용되는 정책 변경
* Document Security 웹 페이지를 열어 파일에 대한 액세스 폐지 또는 파일 정책 변경
* Document Security 웹 페이지를 열어 파일 감사 기록 보기

### Document Security 서버 {#connect-to-a-document-security-server}에 연결

파일에 정책을 적용하려면 Document Security에 대한 연결 설정을 구성해야 합니다. Document Security Extension for Microsoft Office 설치 방법에 따라 기본 연결 설정이 이미 적용되어 있을 수 있습니다. 하나 이상의 Document Security 인스턴스에 대한 연결 설정을 추가할 수 있습니다. 서버 정보는 Document Security 관리자로부터 얻을 수 있습니다.

파일을 보호하거나 보호된 파일을 관리하는 데 사용할 서버를 기본 서버로 설정해야 합니다. 새 파일에 정책을 적용하거나 Document Security 웹 페이지를 열면 Document Security Extension for Microsoft Office가 기본 서버에 연결됩니다. 두 개 이상의 Document Security 인스턴스를 사용하여 파일을 보호하는 경우 서버 간에 전환할 때 기본 서버 설정을 변경해야 합니다. 파일을 열 권한이 있으면 Document Security의 모든 인스턴스에서 보호된 파일을 열 수 있습니다.

Document Security 서버가 인증서 기반 인증을 사용하는 경우 로컬 컴퓨터에서 받은 인증서를 설치해야 합니다. 인증서 인증을 선택하고 인증에 사용할 인증서를 제공해야 합니다.

하나의 Microsoft Office 응용 프로그램에서 Document Security 인스턴스에 대한 연결 설정을 구성하면 모든 Word, Excel 및 PowerPoint에 대해 설정이 구성됩니다.

#### 클라이언트측 인증서 {#install-the-client-side-certificate} 설치

인증서 인증 또는 양방향 인증을 통해 Document Security 웹 페이지에 액세스해야 하는 경우 로컬 컴퓨터에 설치해야 하는 인증서를 받게 됩니다. 인증서 파일(.PFX 또는 .P12 파일) 및 인증서 파일의 암호를 받습니다.

1. 로컬 컴퓨터에 인증서 파일을 저장합니다.
1. 인증서 파일을 두 번 클릭하여 인증서 가져오기 마법사를 열고 **다음**&#x200B;을 클릭합니다.
1. 인증서 파일이 파일 이름 상자에 나열되면 **다음**&#x200B;을 클릭합니다. 다른 인증서를 찾으려면 **찾아보기**&#x200B;를 클릭합니다.
1. 받은 암호를 입력하고 **다음**&#x200B;을 클릭합니다.
1. 인증서 저장소 대화 상자에서 [다음 저장소에 모든 인증서 배치]를 선택하고 **찾아보기**&#x200B;를 클릭합니다.
1. 인증서 저장소 선택 대화 상자에서 [개인]을 선택하고 **확인**&#x200B;을 클릭한 다음 **다음**&#x200B;을 클릭한 다음 **완료**&#x200B;를 클릭합니다.

#### 연결 설정 구성 {#configure-connection-settings}

1. Document Security Extension for Microsoft Office 2010 및 Office 2013의 **Document Security** 탭에서 **서버 선택**&#x200B;을 선택합니다.
1. **새로 만들기**&#x200B;를 클릭하여 새 연결 설정을 만들거나 기존 연결을 선택하고 **편집**&#x200B;을 클릭합니다.
1. **이름** 상자에 연결 이름을 입력합니다. 어떤 이름이든 사용할 수 있습니다.
1. **서버 주소** 상자에 서버 주소를 입력합니다.
1. **포트** 상자에 서버 포트를 입력합니다.
1. (선택 사항) 사용자 이름과 암호를 저장하려면 **이 컴퓨터에 암호 저장**&#x200B;을 선택하고 해당 상자에 사용자 이름과 암호를 입력합니다. 다른 사람이 컴퓨터에 액세스할 수 있는 경우에는 이 옵션을 선택하지 않는 것이 좋습니다.
1. **이 서버에 연결**&#x200B;을 클릭합니다. Document Security Extension for Microsoft Office에서 지정한 서버에 연결을 시도합니다. 지정된 인증 유형에 따라 다음 중 하나를 수행합니다.

   **사용자 이름 및 암호**

   Document Security 관리자로부터 받은 사용자 이름과 암호를 입력합니다.

   **인증서 인증**

   개인 인증서 저장소에서 받고 설치한 인증서를 선택하려면 이 옵션을 선택합니다.

   Document Security에 하나의 인증 유형만 구성된 경우 해당 옵션만 표시됩니다.

>[!NOTE]
>
>서버에 연결할 수 없는 경우 Internet Explorer에서 Document Security 웹 페이지를 열어 보십시오. Internet Explorer를 사용하여 서버에 연결할 수 없거나 대화 상자에 서버 인증서에 대한 경고가 표시되는 경우 Document Security Extension for Microsoft Office는 서버에 연결할 수 없습니다. 도움이 필요하면 서버 관리자에게 문의하십시오.

>[!NOTE]
>
>Document Security에 연결할 수 없는 경우 &quot;사용자 이름 및 암호가 잘못되었습니다. 구성 설정을 확인한 후 다시 시도하십시오.&quot;라는 메시지가 나타납니다. 다른 이유로 연결할 수 없는 경우 이 메시지가 나타날 수 있습니다. 서버에 처음 연결하는 경우 서버 이름과 포트를 올바로 설정했는지 확인하십시오.

#### 기본 서버 {#specify-the-default-server} 지정

1. 다음을 수행합니다.

   * **Document Security** 탭의 Document Security Extension for Microsoft Office 2010 및 Office 2013에서 **서버 선택**&#x200B;을 선택합니다.

1. 기본값으로 지정할 서버를 선택하고 **기본값 설정**&#x200B;을 클릭합니다. 기본 서버 옆에 별표가 나타납니다.

### 타사 인증 공급자 사용 {#using-third-party-authentication-providers}

AEM Forms Document Security에서 타사 인증 공급자를 사용할 수 있습니다. 이러한 인증 공급자를 사용하면 보호된 문서에 추가 액세스 레이어를 추가할 수 있습니다. AEM Forms Document Security는 다음과 같은 확장 인증 워크플로우를 지원합니다.

* 기본 AEM Forms URL을 사용한 확장 인증
* 사용자 정의 URL을 사용한 확장 인증
* JEE 서버의 AEM Forms에 구성된 타사 ID 공급자가 포함된 기본 확장 인증 워크플로
* JEE 서버의 AEM Forms에 구성된 타사 ID 공급자를 통한 사용자 정의 확장 인증 워크플로
* SAML 인증 목록을 위한 사용자 정의 페이지를 사용한 확장 인증

#### 기본 AEM Forms URL {#extended-authentication-using-default-aem-forms-url}을(를) 사용한 확장 인증

확장 인증에 기본 AEM Forms URL을 사용할 수 있습니다. 기본 랜딩 페이지에는 Adobe 브랜딩이 포함되어 있습니다. 또한 기본 AEM Forms 설정은 확장 인증을 위해 기본 AEM Forms URL을 사용하는 데 사용됩니다.

기본 Adobe 랜딩 URL을 사용하여 확장 인증을 활성화하려면 다음 단계를 수행하십시오.

1. AEM Forms 관리자 UI를 엽니다.
1. 서비스 > Document Security > 구성 > 서버 구성으로 이동합니다.
1. 확장 인증 허용 옵션을 활성화합니다.
1. 기본 URL 확장 인증 랜딩 URL을 지정합니다. 기본 URL은 http://localhost:8080/edc/extendedauthentication/welcome.jsp입니다.

   **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >URL에 정규화된 호스트 이름을 사용합니다. HTTPS 프로토콜을 사용하는 것이 좋습니다.

   이제 AEM Forms 문서 보안은 기본 AEM Forms 랜딩 URL의 확장 인증을 사용하도록 구성되어 있습니다.

   ![](assets/third-party-authentication.png)

#### 사용자 지정 랜딩 URL {#extended-authentication-with-a-custom-landing-url}이(가) 있는 확장 인증

확장 인증에 사용자 정의 URL을 사용할 수 있습니다. 사용자 정의 브랜딩을 사용하여 사용자 정의 인증 페이지를 표시할 수 있는 유연성을 제공합니다. 예를 들어 조직의 브랜딩을 예로 들 수 있습니다.

사용자 정의 인증 페이지를 전쟁 파일로 패키지하여 War 파일을 AEM Forms 서버에 배포할 수 있습니다. 전쟁 파일에는 사용자 자격 증명을 수락하고 AEM Forms 서버에 대해 인증할 수 있는 전체 논리가 포함되어 있습니다. AEM Forms Document Security에는 사용자 정의 인증 페이지에 대한 다음과 같은 요구 사항이 있습니다.

* 인증 페이지에서는 사용자 이름을 j_username 및 암호로 보내야 합니다. 또한 페이지는 source_url 및 login_url을 숨겨진 매개 변수로 보내야 합니다.
* 인증이 완료되면 페이지가 자동으로 닫힙니다.

사용자 지정 랜딩 URL을 사용하여 확장 인증을 활성화하려면 다음 단계를 수행합니다.

1. 사용자 정의 인증 전쟁 파일을 AEM Forms 서버에 배포합니다.
1. AEM Forms 관리자 UI를 엽니다.
1. 서비스 > Document Security > 구성 > 서버 구성으로 이동합니다.
1. 확장 인증 허용 옵션을 활성화하고 사용자 지정 확장 인증 랜딩 URL을 지정합니다.
1. *&lt;node name=&quot;AllowedUrls&quot;>* 입력 후 SSO 노드 아래의 config.xml 파일에 다음 항목을 추가합니다.

   >[!NOTE]
   >
   >&lt;entry>!!discoqbr!!&lt;entry>!!discoqbr!!&lt;entry>!!discoqbr!!

   config.xml 파일 업데이트에 대한 단계별 자세한 내용은 [문서 보안 구성 파일](https://helpx.adobe.com/aem-forms/6-3/admin-help/configuring-client-server-options.html#manually_editing_the_document_security_configuration_file) 수동 편집을 참조하십시오.

   이제 AEM Forms 문서 보안은 사용자 정의 랜딩 URL과 함께 확장 인증을 사용하도록 구성됩니다

#### AEM Forms 서버 {#default-extended-authentication-workflow-with-third-party-identity-providers-configured-on-aem-forms-server}에 구성된 타사 ID 공급자가 구성된 기본 확장 인증 워크플로

확장 인증은 AEM Forms 서버에서 사용할 수 있는 서로 다른 유형의 인증을 사용할 수 있습니다. 예를 들어 SAML, [더 많은 예]는

참고:SAML 공급자가 AEM Forms 서버에 구성된 경우 랜딩 URL을 표시하기 전에 SAML 인증을 위해 구성된 모든 ID 공급자가 포함된 페이지가 표시됩니다.

Acrobat에서 보호된 문서를 열면 다음 화면이 표시됩니다.

#### SAML 공급자가 AEM Forms 서버 {#custom-extended-authentication-workflow-when-saml-providers-are-configured-on-aem-forms-server}에 구성된 경우 사용자 지정 확장 인증 워크플로

SAML 공급자가 AEM Forms 서버에 구성된 경우 랜딩 URL을 표시하기 전에 SAML 인증을 위해 구성된 모든 ID 공급자가 포함된 페이지가 표시됩니다.

AEM Forms 서버에 SAML 공급자가 구성된 경우 사용자 지정 확장 인증 워크플로우를 구성할 수 있는 요구 사항은 다음과 같습니다.

* SAML 인증이 AEM Forms 서버에 구성되어 있습니다.
* 사용자 정의 인증 페이지와 사용자 자격 증명을 수락하고 AEM Forms 서버에 대해 인증할 수 있는 전체 논리가 포함된 사용자 정의 전쟁은 AEM Forms 서버에 배포됩니다.

#### SAML 인증 목록 {#using-custom-page-for-listing-saml-authentications}에 사용자 지정 페이지 사용

AEM Forms 서버에 구성된 모든 인증 공급자를 포함하도록 사용자 정의 페이지를 표시할 수도 있습니다. 이러한 페이지를 만들려면 다음 단계를 수행합니다.

1. 사용자 정의 인증 페이지를 전쟁 파일로 패키지하여 War 파일을 AEM Forms 서버에 배포합니다. 전쟁 파일에는 사용자 자격 증명을 수락하고 AEM Forms 서버에 대해 인증할 수 있는 전체 논리가 포함되어 있습니다.
1. AEM Forms 관리자 UI를 열고 **[!UICONTROL 설정]** **[!UICONTROL 사용자 관리]** > **[!UICONTROL 구성]** > **[!UICONTROL SAML 서비스 공급자 설정]**&#x200B;으로 이동합니다.
1. 사용자 지정 속성 필드에 다음을 추가하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   *saml.sp.discovery.url=/demoJSP/saml_discovery.jsp*

   이제 구성된 모든 인증 공급자가 포함된 사용자 정의 페이지를 표시하도록 AEM Forms 문서 보안이 구성되었습니다.

### 사용자 계정 {#obtaining-a-user-account} 얻기

Document Security 계정이 없는 경우 다음과 같은 이벤트가 발생하면 등록 프로세스를 시작할 수 있습니다.

* 정책으로 보호된 파일을 보내려는 Document Security 사용자가 정책에 자신을 추가하는 경우
* Document Security 관리자가 계정을 만듭니다.

계정을 등록 및 활성화한 후 정책을 통해 사용할 수 있도록 권한이 부여된 정책으로 보호된 파일을 사용할 수 있습니다.

>[!NOTE]
정책으로 보호된 파일을 받았는데 Document Security 계정이 없거나 등록하라는 초대를 받은 경우 파일을 보낸 사람에게 문의하여 지원을 받으십시오.

Document Security에서 전자 메일 등록 초대를 받은 경우 전자 메일에 있는 URL을 사용하여 온라인 등록 페이지를 열어 등록할 수 있습니다. 등록한 후 계정 활성화에 대한 두 번째 알림을 받게 됩니다.

#### 외부 사용자 계정 {#obtain-an-external-user-account} 얻기

1. Document Security 등록 이메일을 엽니다. 메시지에 포함된 URL은 Document Security 외부 사용자 등록 페이지에 대한 링크입니다. 등록 메시지를 받지 못한 경우 파일을 보낸 사람에게 문의하여 지원을 받으십시오.
1. URL을 클릭하거나 URL을 복사하여 브라우저에 붙여넣습니다.
1. 해당 상자에 이름, 조직 및 암호를 입력합니다. 암호는 8자의 조합으로 사용할 수 있습니다.

   >[!NOTE]
   기억하기 쉬운 암호를 선택해야 합니다.잊어버린 암호를 찾을 수 있는 방법이 없습니다.

1. **등록**&#x200B;을 클릭합니다. 정품 인증 이메일 메시지가 이메일을 확인하라는 메시지가 표시됩니다.
1. Document Security 등록 확인 이메일을 엽니다.
1. 메시지에 나타나는 URL을 클릭합니다.
1. 로그인 페이지에 대한 링크를 클릭합니다.
1. **사용자 이름** 상자에 Document Security에 등록한 이메일 주소를 입력합니다. 이 전자 메일 주소는 기본 Document Security 사용자 이름입니다.
1. **암호** 상자에 등록할 때 만든 암호를 입력합니다.
1. **로그인**&#x200B;을 클릭합니다.

### 정책 만들기 및 관리 {#creating-and-managing-policies}

Document Security 관리자로부터 권한을 받은 경우 Document Security 웹 페이지의 정책 페이지에서 자신의 파일에 적용할 정책을 만들 수 있습니다.

Document Security 웹 페이지에서 정책을 만드는 데 사용할 수 있는 정책 설정 중 일부는 Word, Excel 및 PowerPoint 파일에는 지원되지 않습니다. 다음 표에서는 정책 권한이 Word, Excel 및 PowerPoint 기능에 매핑되는 방법을 설명합니다.

<table>
 <thead>
  <tr>
   <th><p>권한</p></th>
   <th><p>Word, Excel 및 PowerPoint 지원</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>인쇄 &gt; 허용되지 않음</p></td>
   <td><p>파일을 인쇄할 수 없습니다.</p></td>
  </tr>
  <tr>
   <td><p>인쇄 &gt; 허용됨</p></td>
   <td><p>파일을 인쇄할 수 있습니다.</p><p><strong>참고</strong>: <i>정책에서 복사 권한을 제공하지만 인쇄 권한은 제공하지 않는 경우 다른 파일에 복사한 콘텐트를 인쇄할 수 있습니다.</i></p></td>
  </tr>
  <tr>
   <td><p>인쇄 &gt; 저해상도 전용</p></td>
   <td><p>해당 없음.</p></td>
  </tr>
  <tr>
   <td><p>변경 &gt; 모두</p></td>
   <td><p>파일을 변경할 수 있습니다.</p><p>이 권한이 부여되지 않으면 보호된 Word 및 Excel 파일을 수정할 수 없습니다. PowerPoint 파일을 수정할 수는 있지만 변경 내용을 저장하거나 수정된 파일의 슬라이드 쇼를 볼 수는 없습니다.</p></td>
  </tr>
  <tr>
   <td><p>변경 &gt; 허용되지 않음</p></td>
   <td><p>사용자는 보호된 파일을 수정할 수 없습니다.</p></td>
  </tr>
  <tr>
   <td><p>변경 &gt; 페이지 변경</p></td>
   <td><p>해당 없음.</p><p>페이지 삽입, 삭제 및 회전 포함</p></td>
  </tr>
  <tr>
   <td><p>변경 &gt; Fill &amp; Sign</p></td>
   <td><p>해당 없음.</p></td>
  </tr>
  <tr>
   <td><p>오프라인</p></td>
   <td><p>파일을 오프라인으로 열 수 있습니다.</p></td>
  </tr>
  <tr>
   <td><p>복사</p></td>
   <td><p>파일 내용을 다른 파일로 복사할 수 있습니다.</p></td>
  </tr>
  <tr>
   <td><p>화면 Reader </p></td>
   <td><p>시각 장애인을 위한 화면 판독기(장치)는 파일 내용을 읽을 수 있습니다.</p></td>
  </tr>
  <tr>
   <td><p>권한 유효성</p></td>
   <td><p>지원됨.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>일반 설정</p></th>
   <th><p>Word, Excel 및 PowerPoint 지원</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>유효 기간</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>문서 감사</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>자동 오프라인 제공 기간</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>외부 인증 공급자</p></td>
   <td><p>지원됨.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>고급 설정</p></th>
   <th><p>Word, Excel 및 PowerPoint 지원</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>동적 워터마크</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>인증 플러그인</p></td>
   <td><p>해당 없음.</p></td>
  </tr>
  <tr>
   <td><p>암호화 알고리즘 및 키 길이 </p></td>
   <td><p>모든 옵션이 지원됩니다.</p></td>
  </tr>
  <tr>
   <td><p>문서 제한</p></td>
   <td><p>정책의 설정에 관계없이 모든 파일 내용이 항상 암호화됩니다.</p></td>
  </tr>
  <tr>
   <td><p>액세스 거부 오류 메시지</p></td>
   <td><p>지원됨.</p></td>
  </tr>
 </tbody>
</table>

정책 만들기 및 관리에 대한 자세한 내용은 [Document Security 최종 사용자 도움말](http://help.adobe.com/en_US/AEMForms/6.1/RMHelp/)을 참조하십시오.

### 정책 적용 {#applying-policies}

만든 정책과 액세스 권한이 있는 정책 집합에 포함된 정책을 포함하여 사용 가능한 정책을 파일에 적용할 수 있습니다. 정책을 적용하기 전에 파일을 저장해야 합니다.

정책을 적용하면 자주 사용하는 정책을 쉽게 적용할 수 있도록 AEM Document Security 메뉴의 최근 사용 목록에 추가됩니다. Document Security 인스턴스를 두 개 이상 사용하는 경우 최근 사용 목록에는 현재 연결되어 있는 서버 또는 기본 서버에 대한 정책만 표시됩니다(Document Security 인스턴스에 아직 로그인하지 않은 경우).

>[!NOTE]
Word 문서 파일(.doc, Microsoft Office 2010 및 2013의 .docx 및 .docm), Excel 통합 문서 파일(.xls, .xlsx 및 .xlsm(Microsoft Office 2010 및 2013의 경우) 및 PowerPoint 프레젠테이션 파일(.ppt, .pptx 및 .pptm(Microsoft Office 2010 및 2013의 경우). Word 템플릿 파일(.dot), Excel 템플릿 파일(.xlt) 및 PowerPoint 디자인 템플릿 파일(.pot)에는 정책을 적용할 수 없습니다.

#### 정책 적용 {#apply-a-policy}

1. Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **보안 > 정책 선택**&#x200B;을 선택합니다.

   서버에서 인증 방법으로 사용자 이름과 암호를 선택하고 Document Security에 대한 로그인 정보를 아직 입력하지 않은 경우 사용자 이름과 암호를 입력하라는 대화 상자가 표시됩니다.

1. 목록에서 정책을 선택하고 **적용**&#x200B;을 클릭합니다.
1. 파일을 저장합니다.

#### 최근에 사용한 정책 {#apply-a-recently-used-policy} 적용

1. Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **Secure > ***[정책 이름]*&#x200B;을 선택합니다.
1. 파일을 저장합니다.

## 정책으로 보호된 파일 작업 {#usingaemdocumentsecurityextensionpolicyprotectedfiles}

정책으로 보호된 파일에는 파일 게시자가 소유하고 Document Security로 보호되는 지적 재산이 포함됩니다.

정책으로 보호된 파일은 파일 게시자의 조직에 내외부 파일이든 사용할 수 있습니다. 정책으로 보호된 파일을 열려면 사용자로 초대된 후 연결된 LDAP 또는 Active Directory 목록에 포함되거나 JEE에 LiveCycle 또는 AEM 양식에 대한 로컬 사용자로 추가되거나 Document Security에 등록하여 Document Security에서 인식되어야 합니다.

정책으로 보호된 파일을 받았는데 Document Security 계정이 없거나 등록하라는 초대를 받은 경우 파일을 보낸 사람에게 문의하여 지원을 받으십시오.

### Microsoft Office {#working-with-policy-protected-files-in-microsoft-office}에서 정책으로 보호된 파일로 작업

Document Security Extension for Microsoft Office에서는 파일 게시자의 지적 재산을 보호하기 위해 특정 Word, Excel 및 PowerPoint 기능을 제한합니다. 파일을 변경할 권한이 없으면 파일에 수정 내용을 저장할 수 없습니다.

정책으로 보호된 파일로 작업하는 경우 일부 제품 기능을 사용할 수 없거나 정상적으로 작동하지 않을 수 있습니다. 보호되지 않은 파일도 열려 있는 경우, 복사 또는 내보내기 권한이 없는 정책으로 보호된 파일에서 내용을 가져오거나 복사할 수 있도록 허용하는 파일을 제외하고 보호되지 않은 파일에 대해 대부분의 기능이 활성화됩니다.

>[!NOTE]
Document Security Extension에서 지원되는 Office 응용 프로그램을 사용할 때는 Windows DEP 설정을 비활성화하는 것이 좋습니다. 또한 Document Security Extension이 설치되고 온-액세스 검색을 사용하는 McAfee VirusScan이 활성화된 시스템에서 Office 응용 프로그램이 원활하게 시작되게 하려면 McAfee VirusScan 콘솔에서 [버퍼 오버플로 방지] 옵션을 비활성화하십시오.

기능을 사용할 수 없는 경우 메뉴의 명령 이름과 관련 도구 모음 단추를 사용할 수 없습니다. Document Security Extension for Microsoft Office에서 마우스 포인터를 명령이나 버튼 위에 두면 Document Security에서 해당 명령을 사용할 수 없다는 도구 설명이 표시됩니다.

### 정책으로 보호된 파일 열기 {#opening-policy-protected-files}

정책으로 보호된 파일은 다른 파일을 열 때 사용하는 것과 동일한 방법으로 열 수 있습니다. Document Security에 아직 로그인하지 않은 경우 인터넷에 연결되어 있지 않고 파일을 오프라인으로 열 수 있는 경우가 아니면 로그인하라는 메시지가 표시됩니다. 로그인 프로세스를 취소하면 액세스가 거부됩니다.

파일을 열 수 있는 권한이 없는 경우 액세스가 거부되었다는 메시지가 표시됩니다. 파일 액세스 권한이 폐지된 경우 업데이트된 버전의 파일(있는 경우)로 이동될 수도 있습니다. 정책으로 보호된 파일을 열 수 없는 경우 추가 지원이 필요하면 파일 게시자에게 문의하십시오.

보호된 파일이 열려 있는 경우 제목 표시줄의 파일 이름 다음에 나오는 텍스트는 AEM Document Security로 파일이 보호되었다는 것을 나타냅니다.

SharePoint Server의 Document Security Extension for Microsoft Office에서 보호된 문서를 열 때 Microsoft Word, Microsoft Excel 또는 Microsoft PowerPoint와 같은 파일 형식과 관련된 Microsoft Office 프로그램이 열려 있는지 확인합니다. 관련 응용 프로그램을 열지 않고 파일을 열려고 하면 문서가 열리지 않고 해당 플러그인을 설치해야 한다는 오류 메시지가 표시됩니다. 필요한 응용 프로그램을 여는 것 외에도 캐시 폴더를 지운 후에 SharePoint Server의 Document Security Extension for Microsoft Office에서 보호된 문서를 여는 것이 좋습니다. 또한 SharePoint Server에서 보호된 문서를 열면 적용된 정책에 상관없이 문서에 대한 모든 권한이 비활성화됩니다.

Document Security에 구현된 인증 방법에 따라 보호된 문서를 열 때 인증 방법을 선택하라는 메시지가 표시될 수 있습니다. Document Security에서 두 개 이상의 인증 방법을 지원하는 경우 인증 옵션이 표시됩니다. 예를 들어 Document Security 서버가 사용자 이름/암호 및 인증서 인증을 모두 제공하는 경우 적절한 인증 방법을 선택할 수 있습니다. 인증서 기반 인증을 사용하는 경우 수신하여 설치한 인증서를 사용하라는 메시지가 표시됩니다.

보호된 파일을 열 때의 사용자 환경은 서버의 상호 인증 구성에 따라 다릅니다. 유효한 클라이언트 인증서를 하나만 설치하면 인증 대화 상자가 나타나지 않고 파일이 열립니다. 그러나 한 컴퓨터에 여러 클라이언트 인증서가 설치되어 있는 경우 인증 대화 상자가 나타납니다. 보호된 파일을 열려면 유효한 인증서를 선택해야 합니다.

### {#removing-policy-protection-from-a-file} 파일에서 정책 보호 제거

허용되는 경우 보호된 파일에서 정책 보호를 제거할 수 있습니다. 이렇게 하면 파일이 더 이상 Document Security로 보호되지 않습니다.

1. Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **제거**&#x200B;를 선택합니다.

   Document Security에 대한 로그인 정보를 아직 입력하지 않은 경우 사용자 이름과 암호를 입력하라는 대화 상자가 표시됩니다.

>[!NOTE]
보호된 파일에서 정책을 제거할 수 없는 경우 Document Security 관리자에게 문의하십시오.

### 보안 설정 보기 {#viewing-security-settings}

현재 파일의 인쇄, 복사, 변경 및 오프라인 액세스 권한과 파일 유효 기간을 볼 수 있습니다.

Document Security Extension for Microsoft Office 2010의 Document Security 탭의 보안 상태 그룹에 파일에 대한 권한이 표시됩니다.

다음을 수행합니다.

* Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security 탭**&#x200B;의 **보안 상태** 그룹에서 항목을 클릭합니다.

### 정책 자동 적용을 사용하는 경우 문서 저장 {#saving-documents-when-auto-apply-policy-is-enabled}

관리자가 정책 자동 적용 기능을 활성화한 경우 사용자가 만들거나 편집하는 모든 문서는 문서를 저장할 때 자동으로 보호됩니다.

정책 자동 적용을 사용하는 경우 Document Security Extension for Microsoft Office에서 Document Security 서버에 로그인하라는 메시지가 표시됩니다. 서버에서 인증하려면 사용자 이름과 암호를 제공해야 합니다. 올바른 로그인 자격 증명을 제공하면 문서가 저장되고 보호됩니다.

>[!NOTE]
Document Security에 로그인할 수 없는 경우 문서가 저장되거나 저장되지 않을 수 있습니다. 이는 관리자가 정책 자동 적용을 구성한 방식에 따라 달라집니다. 이 상황에서 문서를 처리하는 방법에 대해 관리자에게 문의하십시오.

### 오프라인 액세스 {#synchronizing-for-offline-access} 동기화

정책을 사용하면 Document Security에 연결되지 않은 오프라인 상태에서도 파일을 열 수 있습니다. 오프라인으로 작업하려면 Document Security에 로그인하여 서버에 자격 증명을 설정해 두어야 합니다. 오프라인으로 파일 작업을 하려면 연결을 끊기 전에 파일의 정책 설정이 서버의 최신 내용을 포함하도록 Document Security와 동기화하는 것이 좋습니다. 또한 파일을 오프라인으로 열기 전에 온라인으로 한 번 여는 것이 좋습니다. 파일을 온라인으로 한 번 열지 않거나 서버와 동기화하지 않아도 정책으로 보호된 파일을 오프라인 상태에서 사용할 수 있습니다. 그러나 오프라인 제공 기간은 만료되지 않아야 하며 마지막으로 서버와 수동 또는 자동으로 동기화한 이후 파일에 대한 정책 설정이 변경되지 않아야 합니다.

다음을 수행합니다.

* Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **오프라인 동기화**&#x200B;를 선택합니다.

   ***참고**:사용자에게 문서에 대한 오프라인 사용 권한이 없는 경우에도 오프라인 동기화 버튼을 사용할 수 있습니다. 그러나 단추를 선택하더라도 아무 작업도 수행되지 않습니다.*

### 동적 워터마크 작업 중 {#working-with-dynamic-watermarks}

Document Security Extension for Microsoft Office에서는 정책으로 보호된 문서에 동적 텍스트 기반 워터마크를 포함할 수 있습니다. 동적 워터마크에는 날짜, 시간, 사용자 이름 또는 정책 이름과 같이 변경될 수 있는 정보가 포함될 수 있습니다. 사용자가 정책으로 보호된 파일을 인쇄하고 해당 파일에 동적 워터마크 및 인쇄 권한이 있으면 워터마크가 출력됩니다.

Document Security Extension은 PDF 기반 워터마크, 워터마크의 여러 요소, 텍스트 서식 지정 옵션 및 페이지 범위와 같은 다양한 워터마크 기능을 지원하지 않습니다.

Document Security 웹 페이지를 사용하여 동적 워터마크를 만듭니다. 정책으로 보호된 문서에서 동적 워터마크를 만들고 포함하는 방법에 대한 자세한 내용은 [Document Security 최종 사용자 도움말](http://www.adobe.com/go/learn_lc_euRightsMgmt_11)을 참조하십시오.

Document Security Extension for Microsoft Office에서는 다음과 같은 워터마크 기능을 지원합니다.

<table>
 <thead>
  <tr>
   <th><p>Document Security 워터마크 옵션</p></th>
   <th><p>Word, Excel 및 PowerPoint 지원</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>정책 이름</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>워터마크 이름</p></td>
   <td><p>지원됨.</p></td>
  </tr>
  <tr>
   <td><p>배경으로 사용</p></td>
   <td><p>동적 워터마크의 표시 동작은 [배경으로 사용]을 선택하는지 여부와 관계없이 동일합니다.</p><p>Word 2010 및 2013의 동적 워터마크는 인쇄 레이아웃 및 인쇄 미리 보기 보기에서만 나타납니다. </p><p>Excel 2010 및 2013에서도 인쇄 미리 보기 및 페이지 레이아웃 보기에 표시됩니다.</p></td>
  </tr>
  <tr>
   <td><p>세로 위치</p></td>
   <td><p>지원됨</p></td>
  </tr>
  <tr>
   <td><p>가로 위치</p></td>
   <td><p>지원됨</p><p>Excel 2010 및 2013에서는 포인트를 사용하여 워터마크의 가로 위치를 조정할 수 없습니다.</p></td>
  </tr>
  <tr>
   <td><p>비율 조정</p></td>
   <td><p>지원됨</p></td>
  </tr>
  <tr>
   <td><p>위치</p></td>
   <td><p>지원됨</p></td>
  </tr>
  <tr>
   <td><p>불투명도</p></td>
   <td><p>지원됨</p></td>
  </tr>
 </tbody>
</table>

### Document Security 웹 페이지 열기 {#opening-the-document-security-web-pages}

Document Security 웹 페이지를 열어 사용자 정책을 만들고 업데이트할 수 있으며 정책으로 보호된 파일의 상태 및 감사 정보를 볼 수 있습니다. Document Security 웹 페이지를 사용하여 정책을 변경하거나 정책으로 보호된 파일에 대한 액세스를 폐지할 수도 있습니다.

Document Security 웹 페이지를 열려면 Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **정책 만들기 및 관리**&#x200B;를 선택합니다. 로그인 정보를 아직 입력하지 않은 경우 브라우저가 서버 로그인 페이지에 열립니다.

### 정책 변경 중 {#changing-policies}

일반적으로 Document Security 관리자 또는 파일 게시자인 권한이 있으면 나중에 다른 정책을 파일에 적용하거나 현재 적용된 정책의 설정을 변경할 수 있습니다.

정책 설정을 변경하려면 Document Security 웹 페이지를 사용합니다.

1. 다음을 수행합니다.

   * Document Security Extension for Microsoft Office 2010 또는 2013의 **Document Security** 탭에서 **보안 > 보안 변경**&#x200B;을 선택합니다.

1. 목록에서 정책을 선택하고 **적용**&#x200B;을 클릭합니다.

### 파일 액세스 권한 취소 중 {#revoking-file-access-privileges}

보호된 파일을 여는 기능을 취소할 수 있습니다. 파일에 대한 액세스 권한을 해지할 때 파일을 열려는 모든 사람에게 나타나는 메시지와 파일을 수정된 사본으로 바꾸는 경우 업데이트된 버전의 파일로 연결되는 URL을 지정할 수도 있습니다.

1. 다음을 수행합니다.

   * Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **취소**&#x200B;를 선택합니다.

   Document Security 웹 페이지가 문서 폐지 페이지에 열립니다.

1. 표시할 메시지를 지정하고, 가능한 경우 업데이트된 버전의 URL을 지정한 다음 **확인**&#x200B;을 클릭합니다.

파일 액세스 권한 취소에 대한 자세한 내용은 [Document Security 최종 사용자 도움말](http://help.adobe.com/en_US/AEMForms/6.1/RMHelp/)을 참조하십시오.

액세스 권한은 Document Security 웹 페이지에서 복구할 수 있습니다.

### 파일 감사 기록 보기 {#viewing-the-file-audit-history}

Document Security는 정책으로 보호된 파일에 대한 감사 기록을 저장하여 사용자가 파일에 수행하는 작업을 감사할 수 있습니다.

Word, Excel 및 PowerPoint 파일에 대해 감사되는 이벤트는 다음과 같습니다.

**파일에 적용된 새** 문서 정책 보호

**열린** 문서 파일 보기

**문서** 파일 닫기

**파일** 에 대해 제거된 DocumentAccess 권한 취소

**파일에** 반환된 DocumentAccess 권한 취소

**Modify** DocumentFile 변경 및 로컬에 저장

**고해상도** 파일 인쇄인쇄됨

**Change Security** Handler파일에서 정책 보호 제거됨

**문서의 정책** 전환Document Security 웹 페이지에서 파일에 적용한 새 정책

### {#view-the-audit-history-for-a-file} 파일의 감사 기록 보기

Document Security Extension for Microsoft Office 2010 및 2013의 **Document Security** 탭에서 **감사 내역**&#x200B;을 선택합니다.

Document Security 웹 페이지가 [이벤트] 페이지에 열리고 현재 파일에 대해 감사된 이벤트가 표시됩니다.

### Microsoft Office 제한 기능 {#microsoft-office-restricted-features}

정책으로 보호된 파일이 열려 있으면 지적 재산을 보호하기 위해 일부 Microsoft Office 기능을 사용할 수 없습니다. 사용할 수 없는 기능 목록은 현재 사용자에게 부여된 권한에 따라 다릅니다. 일부 기능은 보호된 파일에만 사용할 수 없으며, 보호된 세션에 있는 경우 모든 파일에는 사용할 수 없는 기능도 있습니다. 일반적으로 보호된 세션은 정책으로 보호된 파일을 열 때부터 응용 프로그램을 닫거나 세션이 만료될 때까지 계속됩니다.

대부분의 정책은 파일 게시자에게 전체 권한을 부여합니다. 다른 사용자는 추가 기능 제한 사항을 알 수 있습니다.

명령을 사용할 수 없는 경우 메뉴의 명령 이름과 관련 도구 모음 단추가 흐리게 표시됩니다.

>[!NOTE]
포함된 파일에 대한 링크가 포함된 파일에 정책을 적용하면 해당 정책이 연결된 파일에 적용되지 않습니다. Document Security for Microsoft Office에서는 연결된 파일로 보호 기능이 확장되지 않습니다.

* 정책으로 보호된 Word, Excel 및 PowerPoint 파일은 Internet Explorer 브라우저 창에서 열 수 없도록 차단됩니다.
* 변경 권한만 부여된 사용자는 Windows 클립보드를 사용하여 다른 응용 프로그램의 파일에 콘텐트를 복사할 수 없습니다. 사용자는 Microsoft Office 클립보드 옵션을 사용하여 내용을 파일에 복사할 수 있습니다.
* Microsoft Office에서 정책으로 보호된 파일을 열면 응용 프로그램을 닫거나 세션이 만료될 때까지 인쇄 화면 키를 사용할 수 없습니다.
* Document Security for Microsoft Office에서는 WebDAV(Web-based Distributed Authoring and Versioning)를 지원하지 않습니다. 대부분의 경우 WebDAV 폴더에서 정책으로 보호된 파일을 열 수 없습니다. 정책으로 보호된 파일을 열 수 있는 경우에는 파일을 저장, 인쇄, 변경 또는 복사할 수 있는 권한이 없습니다.

정책으로 보호된 파일에 적용되는 일반 보안에는 다음 제한 사항이 포함됩니다.

보호된 세션 중에 Word, Excel 및 PowerPoint에서 많은 일반적인 기능이 제한될 수 있습니다.

정책으로 보호된 파일 중 사용자가 변경을 허용하지 않는 파일이 열려 있으면 어떤 식으로든 파일을 변경하는 명령을 사용할 수 없습니다. 새 문서를 열거나 만들고 응용 프로그램 환경 설정을 변경하는 명령만 사용할 수 있습니다.

#### Word 2010 및 Word 2013 제한 사항 {#word-2010-and-word-2013-restrictions}

정책으로 보호된 파일을 Word에서 열면 Word를 닫았다가 다시 시작해야 자동 파일 복구 정보를 저장할 수 있습니다. 또한 아래 나열된 기능은 설명된 상황에서 제한됩니다.

**파일 > 새로 만들기 > 기존** 에서 새로 만들기 사용 가능하지만 정책으로 보호된 파일이 열려 있는 동안에는 이 명령을 사용하여 만든 파일을 저장할 수 없습니다. 새 파일의 콘텐트를 다른 파일로 복사할 수 없습니다.

**[파일] > [** 저장]은 [변경] 권한을 통해 제한됩니다.

**[파일] > [** 다른 이름으로 저장] 옵션은 [변경] 권한을 통해 제한됩니다.

**파일 >** 인쇄모두 옵션은 인쇄 권한을 통해 제한됩니다. 정책에서 고해상도 인쇄를 허용하지 않으면 사용할 수 없습니다.

**보호된 세션 중에는 파일 > 저장 및** 모두 전송 옵션을 사용할 수 없습니다.

**[파일] > [정보] > [Protect 문서] > [암호로 암호화], [디지털 서명 추가], [최종본으로 표시], [사용자별로 권한** 제한]보호된 세션 중에는 사용할 수 없습니다.

**파일 >** 워크플로보호된 세션 중에는 사용할 수 없습니다.

***참고&#x200B;**:2010 Microsoft Office 시스템 버전의 Word, Excel 및 PowerPoint에서 워크플로우를 시작하는 기능은 Office Professional Plus 2010, Office Enterprise 2010 및 Office Ultimate 2010 제품군과 독립형 2010 Office 릴리스에서만 사용할 수 있습니다 이 프로그램들.*

**보호된 세션** 중에 블로그 게시물 > 게시사용할 수 없음

**파일 > 서버 > 파일 서버 작업** 메뉴보호된 세션 중에는 사용할 수 없습니다.

**[홈] > [클립보드] >** [복사] 권한을 통해 제한됨. 복사가 허용되지 않으면 복사한 콘텐트를 다른 어떤 파일이나 Office 클립보드에도 붙여넣을 수 없습니다. 사용자에게 변경 권한이 있는 경우 콘텐트를 보호된 파일 내에서 복사할 수 있습니다.

**홈 > 클립보드 >** 붙여넣기변경 권한을 통해 제한됨.

**[홈] > [클립보드] > [** 특수 붙여넣기]는 변경 권한을 통해 제한됩니다.

**삽입 > 텍스트 >** 객체보호된 세션 중에 사용할 수 없는 객체입니다. 정책으로 보호된 파일은 언제든지 삽입할 수 없습니다.

**메일** 보내기이 탭의 대부분의 옵션은 보호된 세션 중에 사용할 수 없습니다.

**검토 > 언어 교정 >** 연구 복사 권한을 통해 제한됨 복사가 허용되지 않으면 사용할 수 없습니다.

**검토 > 언어 교정 >** 동의어 사전 복사 권한을 통해 제한됩니다. 복사가 허용되지 않으면 사용할 수 없습니다.

**[검토] > [언어] > [번역] > [** 문서 번역](복사 사용)을 선택합니다.

**[검토] > [언어] > [번역] > [선택한** 텍스트 번역](복사 사용)을 선택합니다.

**검토 > 언어 > 번역 > Mini** Translator 복사 권한이 있는 사용.

**검토 > 비교 >** 비교보호된 세션 중에 사용할 수 없음 정책으로 보호된 파일은 항상 비교할 수 없습니다.

**검토 > Protect > 작성자** 차단 보호된 세션 중에는 사용할 수 없습니다.

**검토 > Protect >** 편집 제한보호된 세션 중에는 사용할 수 없습니다.

**보기 >** 매크로일부 매크로는 복사 권한을 통해 제한되며 복사가 허용되지 않으면 매크로를 사용할 수 없습니다.

**추가** 기능보호된 세션 중에는 추가하거나 제거할 수 없습니다.

**온라인** 공동 작업보호된 세션 중에는 사용할 수 없습니다.

**및** 하위 문서하위 문서는 마스터 문서 내에서 열 때 마스터 문서 정책의 적용을 받습니다. 별도로 여는 경우에는 하위 문서를 인쇄, 복사 또는 수정할 수 없습니다.

**다시** 요약보호된 세션 중에 사용할 수 없습니다.

**프레임(및 모든 관련 명령)** 보호된 세션 중에는 사용할 수 없습니다.

**문서** 패널보호된 세션 중에는 사용할 수 없습니다.

**개발자 > 문서** 템플릿보호된 세션 중에 사용할 수 없습니다. 이 명령에 액세스하려면 파일 > 옵션 > 사용자 지정 > 개발자 탭 > 템플릿 > 문서 템플릿을 선택합니다.

**개요 > 기본 문서 > 하위 문서 만들기, 하위 문서 삽입** 보호된 세션 중에는 사용할 수 없습니다.

#### Excel 2010 및 Excel 2013 제한 사항 {#excel-2010-and-excel-2013-restrictions}

아래 나열된 기능은 설명된 상황에서 제한됩니다.

**[파일] > [새로 만들기] > [** 기존 파일에서 새로 만들기]를 선택합니다. 그러나 보호된 세션 중에 이 명령을 사용하여 만든 파일은 저장할 수 없습니다. 새 파일의 콘텐트를 다른 파일로 복사할 수 없습니다.

**[파일] > [저장], [** 다른 이름으로 저장] 권한은 변경 권한을 기준으로 제한됩니다.

**[파일] > [다른 이름으로 저장] > [** PDF]보호된 세션 동안 사용할 수 없습니다.

**파일 >** 인쇄 권한을 통해 제한됨 정책에서 고해상도 인쇄를 허용하지 않으면 사용할 수 없습니다.

**보호된 세션 중에 파일 > 정보 > Protect** DocumentUnavailable.

**보호된 세션 중에는 파일 > 정보 > Protect** 통합 문서를 사용할 수 없습니다.

**보호된 세션 중에 파일 > 저장** 및 보내기사용할 수 없음

**파일 > 옵션 > 추가** 기능보호된 세션 중에는 추가하거나 제거할 수 없습니다.

**파일 >** 워크플로보호된 세션 중에는 사용할 수 없습니다.

***참고&#x200B;**:2010 Microsoft Office 시스템 버전의 Word, Excel 및 PowerPoint에서 워크플로우를 시작하는 기능은 Office Professional Plus 2010, Office Enterprise 2010 및 Office Ultimate 2010 제품군과 독립형 2010 Office 릴리스에서만 사용할 수 있습니다 이 프로그램들.*

**파일 > 서버 > 파일 서버 작업** 메뉴보호된 세션 중에는 사용할 수 없습니다.

**[홈] > [클립보드] >** [복사] 권한을 통해 제한됨. 복사가 허용되지 않으면 복사한 콘텐트를 다른 어떤 파일이나 Microsoft Office 클립보드에도 붙여넣을 수 없습니다. 사용자에게 변경 권한이 있는 경우 콘텐트를 보호된 파일 내에서 복사할 수 있습니다.

**홈 > 클립보드 >** 붙여넣기변경 권한을 통해 제한됨.

**[홈] > [클립보드] > [** 특수 붙여넣기]는 변경 권한을 통해 제한됩니다.

**홈 > 셀 > 서식 > 시트 이동 또** 는 복사를 보호된 세션 중에 사용할 수 없습니다.

**보호된 세션 중에는 홈 > 셀 > 삽입 > 시트** 삽입을 사용할 수 없습니다.

**홈 > 셀 > 삭제 > 시트** 삭제보호된 세션 중에는 사용할 수 없습니다.

**홈 > 편집 > 채우기 >** 워크시트 전체 변경 권한을 통해 제한됩니다.

**삽입 > 표 >** 테이블변경 권한을 통해 제한됨

**[삽입] > [표] > [** 피벗 테이블]정책으로 보호된 파일은 만들기 마법사에서 선택할 수 없습니다.

**삽입 > 텍스트 >** 객체보호된 세션 중에 사용할 수 없는 객체입니다. 정책으로 보호된 파일은 언제든지 삽입할 수 없습니다.

**[삽입] > [텍스트] > [머리글 및** 바닥글]변경 권한을 통해 제한됩니다. 정책으로 보호된 문서에서는 사용할 수 없습니다.

**정책으로 보호된 파일** 에서 데이터 > 외부 데이터 가져오기를 가져올 수 없습니다.

**데이터 > 개요 >** 부분합은 변경 권한을 통해 제한됩니다.

**데이터 > 데이터 도구 > 데이터** 유효성 검사변경 권한을 통해 제한됩니다.

**검토 > 언어 교정 >** 연구 복사 권한을 통해 제한됨

**검토 > 언어 교정 >** 동의어 사전 복사 권한을 통해 제한됩니다.

**[검토] > [언어] > [** 번역]복사 권한을 통해 제한됩니다.

**검토 > 변경 내용 > Protect** Sheet보호된 세션 중에 사용할 수 없음

**검토 > 변경 내용 > Protect** 통합 문서보호된 세션 중에는 사용할 수 없습니다.

**검토 > 변경 내용 >** 통합 문서 공유보호된 세션 중에는 사용할 수 없습니다.

**검토 > 변경 내용 > Protect 및** 통합 문서 공유보호된 세션 중에는 사용할 수 없습니다.

**검토 > 변경 내용 > 사용자가 범위 편집** 허용보호된 세션 중에는 사용할 수 없습니다.

**동적 워터마크가 포함된 정책으로 보호된 파일에 대해 검토 > 변경 내용** 추적 > 변경 내용 강조 표시를 사용할 수 없습니다.

**보기 >** 매크로변경 권한을 통해 제한됩니다.

**보기 > 작업 공간** 저장 명령이 작동하지 않습니다.

**개발자 > XML > 확장** 팩일부 매크로는 복사 권한을 통해 제한되며 복사가 허용되지 않으면 매크로를 사용할 수 없습니다.

**수식 > 공식 감사 >** 오류 검사변경 권한을 통해 제한됨 변경이 허용되지 않으면 사용할 수 없습니다.

**온라인** 공동 작업보호된 세션 중에는 사용할 수 없습니다.

**자동 복구 저장 정보** 는 보호된 세션 중에 사용할 수 없습니다.

***참고&#x200B;**:정책으로 보호된 파일에서 변경할 권한이 없는 셀을 변경하려고 하면 시트 보호 해제 명령을 사용하여 파일에서 보호를 제거해야 한다는 잘못된 경고 메시지가 Excel에 표시됩니다. 시트 보호 해제 명령을 사용하면 파일에서 정책 보호가 제거되지 않습니다.*

#### PowerPoint 2010 및 PowerPoint 2013 제한 사항 {#powerpoint-2010-and-powerpoint-2013-restrictions}

아래 나열된 기능은 설명된 상황에서 제한됩니다.

**[파일] > [새로 만들기] > [** 기존 파일에서 새로 만들기]를 선택합니다. 그러나 보호된 세션 중에 이 명령을 사용하여 만든 파일은 저장할 수 없습니다. 새 파일의 콘텐트를 다른 파일로 복사할 수 없습니다.

**[파일] > [** 저장]은 [변경] 권한을 통해 제한됩니다.

**[파일] > [** 다른 이름으로 저장] 옵션은 [변경] 권한을 통해 제한됩니다.

**파일 >** 인쇄모두 옵션은 인쇄 권한을 통해 제한됩니다. 정책에서 고해상도 인쇄를 허용하지 않으면 사용할 수 없습니다.

**보호된 세션 중에 파일 > 저장** 및 보내기사용할 수 없음

**[파일] > [정보] > [Protect 프레젠테이션] > [암호로 암호화], [디지털 서명 추가], [최종본으로 표시], [사용자별로 권한** 제한]보호된 세션 중에는 사용할 수 없습니다.

**파일 > PowerPoint 옵션 > 자동 복구** 저장 정보 보호된 세션 중에는 사용할 수 없습니다.

**파일 > 서버 > 파일 서버 작업** 메뉴보호된 세션 중에는 사용할 수 없습니다.

**[홈] > [클립보드] >** [복사] 권한을 통해 제한됨. 복사가 허용되지 않으면 복사한 콘텐트를 문서 내, 다른 파일 또는 Office 클립보드로 붙여넣을 수 없습니다. 사용자에게 변경 권한이 있는 경우 콘텐트를 보호된 파일 내에서 복사할 수 있습니다.

**홈 > 클립보드 >** 붙여넣기변경 권한을 통해 제한됨. 복사가 허용되지 않으면 복사한 콘텐트를 문서에 붙여넣을 수 없습니다.

**[홈] > [클립보드] > [** 특수 붙여넣기]는 변경 권한을 통해 제한됩니다.

**[홈] > [슬라이드] > [새 슬라이드] > [슬라이드 개요], [슬라이드** 재사용]보호된 세션 중에는 사용할 수 없습니다.

**삽입 > 텍스트 >** 객체보호된 세션 중에 사용할 수 없는 객체입니다. 정책으로 보호된 파일은 언제든지 삽입할 수 없습니다.

**동적 워터마크가 포함된 정책으로 보호된 파일에는 디자인 > 배경 > 배경 스타일, 배경** 그래픽 숨기기, 배경 서식 지정을 사용할 수 없습니다.

**[슬라이드 쇼] > [설정] > [슬라이드** 쇼 기록]변경 권한을 통해 제한됩니다.

**검토 > 언어 교정 >** 동의어 사전 복사 권한을 통해 제한됩니다.

**[검토] > [언어] > [** 번역]복사 권한을 통해 제한됩니다.

**검토 > 언어 > 번역 > Mini** Translator 복사 권한이 있는 사용.

**보기 > 프레젠테이션 보기 > 슬라이드** 쇼 변경 권한을 통해 제한됨 변경이 허용되지 않으면 파일을 수정한 경우 슬라이드 쇼를 볼 수 없습니다.

**보기 >** 매크로일부 매크로는 복사 권한을 통해 제한되며 복사가 허용되지 않으면 매크로를 사용할 수 없습니다.

**추가** 기능보호된 세션 중에는 추가하거나 제거할 수 없습니다.

**온라인** 공동 작업보호된 세션 중에는 사용할 수 없습니다.

## 타사 인증 공급자 사용 {#use-third-party-authentication-providers}

AEM Forms Document Security에서 타사 인증 공급자를 사용할 수 있습니다. 이러한 인증 공급자를 사용하면 보호된 문서에 추가 액세스 레이어를 추가할 수 있습니다. AEM Forms Document Security는 다음과 같은 확장 인증 워크플로우를 지원합니다.

* 기본 AEM Forms URL을 사용한 확장 인증
* 사용자 정의 URL을 사용한 확장 인증
* JEE 서버의 AEM Forms에 구성된 타사 ID 공급자가 포함된 기본 확장 인증 워크플로
* JEE 서버의 AEM Forms에 구성된 타사 ID 공급자를 통한 사용자 정의 확장 인증 워크플로
* SAML 인증 목록을 위한 사용자 정의 페이지를 사용한 확장 인증

확장 인증 워크플로우를 구성하는 자세한 방법은 [확장 인증 시나리오](http://blogs.adobe.com/livecycle/2011/12/extended-authentication-scenarios.html) 문서를 참조하십시오.

## 용어 설명 {#glossary}

JEE 용어에 대한 LiveCycle 및 AEM 양식에 대한 자세한 내용은 [용어집](http://www.adobe.com/go/learn_aemforms_designer_65)을 참조하십시오.
