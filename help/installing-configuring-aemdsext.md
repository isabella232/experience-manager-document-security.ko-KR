---
title: Microsoft Office용 AEM Document Security Extension 설치 및 구성
description: 이 문서에서는 Microsoft Office용 Adobe Experience Manager Document Security Extension 6.2의 설치 및 구성에 대해 설명합니다.
uuid: 9d7eb6bb-4780-4d82-8657-7c6c6d523af0
content-type: reference
topic-tags: installing
discoiquuid: f1cdf344-efe4-4cb5-9fc3-47ee4ba5faf4
translation-type: tm+mt
source-git-commit: ac385c538cdd7d3bb4772b92ee7a94b003595f56
workflow-type: tm+mt
source-wordcount: '2796'
ht-degree: 0%

---


# Microsoft Office용 AEM Document Security Extension 설치 및 구성{#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

이 문서에서는 Adobe Experience Manager Document Security Extension for Microsoft Office 설치 및 구성에 대해 설명합니다.

이 문서에는 다음 작업에 대한 정보가 포함되어 있습니다.

* Document Security Extension for Microsoft Office 설치
* AEM 6.0 Forms 이상용 LiveCycle Rights Management ES2 또는 Document Security Add-on을 가리키도록 설치 프로그램을 미리 구성할 수 있습니다.
* 기본 정책의 자동 응용 프로그램 구성

## 설치하기 전에 {#before-you-install}

Document Security Extension for Microsoft Office를 설치하기 전에 다음을 확인하십시오.

* [릴리스 노트](document-security-extension-release-notes.md)를 읽었습니다.
* Microsoft Office가 활성화됩니다. Microsoft Office 응용 프로그램을 열 때 활성화 대화 상자가 나타나지 않습니다.
* Microsoft Windows 및 Microsoft Office용 최신 서비스 팩이 설치되어 있습니다.
* 지원되지 않는 언어로 Document Security for Microsoft Office를 설치하는 경우 Office 응용 프로그램을 최소 한 번 여십시오.

>[!NOTE]
>
>이름에 더블바이트 문자가 포함된 폴더에 소프트웨어를 설치하지 마십시오. 이렇게 하면 AEM Document Security 메뉴가 Microsoft Office에 표시되지 않습니다.

>[!NOTE]
>
>64비트 운영 체제에서 32비트 버전의 Document Security 확장을 설치하는 것은 지원되지만 반대 방법은 지원되지 않습니다. 32비트 운영 체제에서는 64비트 버전의 Document Security Extension for Microsoft Office를 설치할 수 없습니다.

### McAfee VirusScan 및 {#disable-mcafee-virusscan} 비활성화

Document Security Extension이 설치되고 온-액세스 검색을 사용하는 McAfee VirusScan이 활성화된 시스템에서 Office 응용 프로그램이 원활하게 시작되게 하려면 McAfee VirusScan 콘솔에서 [버퍼 오버플로 방지] 옵션을 비활성화하십시오.

### 타사 플러그인 제거 {#uninstall-third-party-plug-ins}

AEM Document Security Extension for Microsoft Office는 Microsoft Office 응용 프로그램용 타사 플러그인을 지원하지 않습니다. 이 확장은 타사 플러그인과 충돌하므로 Document Security for Microsoft Office를 설치하기 전에 Microsoft Office용 Adobe이 아닌 플러그인을 제거합니다. Adobe에서는 타사 플러그인이 설치된 Document Security for Microsoft Office 응용 프로그램에 대한 지원을 제공하지 않습니다.

## 시스템 요구 사항 {#system-requirements}

### Document Security Extension Client {#document-security-extension-client}

Document Security Extension을 설치할 최소 구성:

* 32비트 또는 64비트 버전의 Microsoft Windows 7 또는 Windows 10은 영어, 프랑스어, 독일어, 일본어, 이탈리아어, 스페인어, 포르투갈어(브라질), 한국어, 중국어 간체 또는 중국어 번체로 제공됩니다.
   **참고:** *Microsoft Office용 문서 보안 익스텐션은 Microsoft Surface 장치에서도 작동될 예정입니다.*

* 32비트 또는 64비트 버전의 Office 365의 일부로 영어, 프랑스어, 독일어, 일본어, 이탈리아어, 스페인어, 포르투갈어(브라질), 한국어, 중국어 간체 또는 중국어 번체로 설치된 Microsoft Office 2013, 2016, 2019 및 Microsoft Office 데스크탑 애플리케이션

   **참고**: *AEM Document Security Extension for Microsoft Office는 Microsoft Office 응용 프로그램용 타사 플러그인을 지원하지 않습니다. 이 확장은 타사 플러그인과 충돌할 수 있으므로 Document Security Extension for Microsoft Office를 설치하기 전에 Adobe이 아닌 Microsoft Office 응용 프로그램용 플러그인을 제거해야 합니다. Adobe에서는 타사 플러그인이 설치된 Document Security Extensions for Microsoft Office 응용 프로그램에 대한 지원을 제공하지 않습니다.*

* 1.3GHz 프로세서 이상
* 2GB RAM
* 100MB의 하드 디스크 여유 공간

### 문서 보안 {#document-security}

Document Security Extension을 사용하려면 AEM 6.0 양식용 Adobe LiveCycle Rights Management ES2 이상 또는 Document Security Add-on에 연결할 수 있는지 확인하십시오.

## Microsoft Office용 Document Security Extension 설치 {#installing-document-security-extension-for-microsoft-office}

[다운로드 페이지](download-installer.md)에서 설치 프로그램을 다운로드할 수 있습니다. 설치 프로그램 실행 파일을 직접 사용자 정의할 수는 없지만 대화형으로 또는 자동 설치 모드에서 설치할 수 있습니다. 소프트웨어를 설치하려면 관리자로 Windows에 로그인합니다.

개별 설치 프로그램은 32비트 및 64비트 버전의 Microsoft Office에서 사용할 수 있습니다. 32비트 버전의 Microsoft Office의 경우 DocumentSecurityExtensionforMicrosoftOffice.exe를 다운로드합니다. 64비트 버전의 Microsoft Office의 경우 DocumentSecurityExtensionforMicrosoftOffice64.exe를 다운로드합니다.

>[!NOTE]
>
>이 문서에서는 32비트 설치 프로그램 파일(DocumentSecurityExtensionforMicrosoftOffice.exe)을 사용하여 다양한 명령 및 옵션을 설명합니다. 64비트 버전의 Microsoft Office를 사용하는 경우 64비트 설치 프로그램 파일(DocumentSecurityExtensionforMicrosoftOffice64.exe)을 사용하여 이 문서에 나열된 작업을 수행합니다.

### 자동 모드 {#install-in-silent-mode}에 설치

WinZip과 같은 파일 추출 유틸리티를 사용하여 설치 프로그램 파일에서 `DocumentSecurityExtensionforMicrosoftOffice.exe`을 추출합니다. 명령 프롬프트를 열고 설정 파일이 포함된 폴더로 가서 다음 텍스트를 입력합니다.

`DocumentSecurityExtensionforMicrosoftOffice.exe -s -a -s -v" /qn"`

설치 프로그램은 사용자 정의에 사용할 수 있는 MSI 파일로도 제공됩니다.

### 자동 모드 {#install-an-msi-file-in-silent-mode}에 MSI 파일 설치

1. WinZip과 같은 파일 추출 유틸리티를 사용하여 ZIP 파일에서 `DocumentSecurityExtensionforMicrosoftOffice.msi` 파일을 추출합니다.

1. 명령 프롬프트를 열고 MSI 파일이 포함된 폴더로 이동한 다음 다음 텍스트를 입력합니다.

   `msiexec /I DocumentSecurityExtensionforMicrosoftOffice.msi /qn`

## 설치 프로그램을 미리 구성하여 Document Security {#preconfiguring-the-installer-to-connect-to-document-security} 연결

Document Security Extension for Microsoft Office 설치 프로그램을 미리 구성하여 LiveCycle 또는 AEM 서버를 지정할 수 있으므로 Document Security Extension for Microsoft Office를 설치한 사용자는 연결을 구성하지 않고 해당 기능을 사용할 수 있습니다. 따라서 구성 없이 보호된 문서를 열 수 있습니다. 그러나 특정 서버를 사용하도록 클라이언트를 구성해야 새 문서를 보호할 수 있습니다.

다음 단계에서는 MSI 파일을 만들고 구성하는 방법에 대해 설명합니다. 이 MSI 파일에는 기업 내 설치된 LiveCycle 또는 AEM 서버에 Document Security Extension for Microsoft Office 설치 프로그램을 미리 구성하는 데 필요한 레지스트리 값이 포함되어 있습니다.

### 설치 프로그램 {#prerequisites-for-customizing-the-installer} 사용자 지정을 위한 사전 요구 사항

Orca 데이터베이스 편집기를 사용하여 설치 프로그램을 사용자 정의합니다. 다음 단계에서는 Orca 데이터베이스 편집기를 사용하여 MSI 설치 파일 사본을 수정하여 사용자 정의 MSI 파일을 만드는 방법을 설명합니다. Orca는 Windows Server 2008 및 .NET Framework 3.5용 Windows SDK의 일부로 사용할 수 있습니다. Orca를 사용하여 Microsoft Windows® 설치 프로그램 파일을 편집하는 방법에 대한 자세한 내용은 [Microsoft 지원](http://support.microsoft.com/kb/255905/EN-US/)을 참조하십시오.

>[!NOTE]
>
>사용자 정의 MSI 파일을 만들기 전에 모든 설치 프로그램 파일을 전체 백업하는 것이 좋습니다.

#### Orca {#install-orca} 설치

1. [Microsoft 다운로드 센터](http://www.microsoft.com/download/en/details.aspx?displaylang=en&amp;id=11310)에서 Windows Server 2008 및 .NET Framework 3.5용 Windows SDK를 다운로드합니다.
1. \Microsoft SDK\bin 폴더에서 Orca.msi 파일을 두 번 클릭합니다.

   설치 프로그램 파일의 MSI 변형이 필요합니다. 최신 버전의 MSI 설치 프로그램을 받으려면 Adobe 지원에 문의하십시오.

   >[!NOTE]
   >
   >설치 관리자를 실행하기 전에 항상 DocumentSecurityExtensionforMicrosoftOffice.msi 파일을 닫으십시오. Orca가 MSI 파일을 사용하고 있는 경우 설치 프로그램을 실행할 수 없습니다.

### MSI 파일 {#create-and-configure-the-msi-file} 만들기 및 구성

1. **[!UICONTROL 시작 > 프로그램 > Orca]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 파일 > 열기]**&#x200B;를 클릭한 다음 `DocumentSecurityExtensionforMicrosoftOffice.msi` 파일을 찾습니다.

1. 표의 왼쪽 목록에서 속성을 선택합니다.

1. 기업 Rights Management 또는 Document Security 설치에 해당하는 다음 키 이름 값을 편집합니다.

<table>
 <tbody>
  <tr>
   <td><p><strong></strong><strong></strong><strong>키 이름</strong></p> </td>
   <td><p><strong>설명</strong></p> </td>
   <td><p><strong>키 </strong><strong></strong><strong>값 기본값</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_NAME</code></p> </td>
   <td><p>표시 이름.</p> </td>
   <td><p>기본 서버</p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_URL</code></p> </td>
   <td><p>호스트 서버 URL.</p> </td>
   <td><p>https://default.corp.com:1234</p> </td>
  </tr>
 </tbody>
</table>

1. 표의 왼쪽 목록에서 레지스트리를 선택합니다.

1. 다음 키 이름 값을 편집합니다.

   | **키 이름** | **설명** | **키 값 기본값** |
   |---|---|---|
   | `IsDefault` | 기본 APS 서버. | 기본 서버 |

1. 원본 MSI 설치 프로그램이 포함된 디렉토리에 수정된 파일을 저장합니다.

   >[!NOTE]
   >
   >원본 MSI 파일(예: `DocumentSecurityExtensionforMicrosoftOffice.msi`)과 동일한 파일 이름을 사용하는 것이 일반적인 방법입니다.

## 기본 정책 {#configuring-automatic-application-of-a-default-policy}의 자동 응용 프로그램 구성

구성의 일부로 기본 정책의 자동 응용 프로그램을 구성하여 Document Security Extension for Microsoft Office에서 저장되는 모든 문서를 보호할 수 있습니다.

다음 옵션 중 하나를 지정할 수 있습니다.

* Protect 기본 정책을 사용하여 모든 문서.
* 서버에 연결할 수 없는 경우 사용자가 보호되지 않은 형식으로 파일을 선택적으로 저장할 수 있도록 합니다. 이러한 유연성을 통해 사용자가 네트워크 연결이 끊어진 상태에서 문서를 만드는 경우(예: 비행기 탑승 중) 문제를 해결할 수 있습니다.

정책 자동 적용 기능을 활성화하면 다음과 같은 경우 문서가 기본 정책으로 보호됩니다.

* 사용자가 새로 만든 문서를 편집하고 저장합니다.
* 사용자가 보호되지 않은 문서를 편집하고 저장합니다.
* 사용자가 기본 문서를 열고 편집한 다음 문서를 저장하는 응용 프로그램을 엽니다

### MSI 파일에서 정책 자동 적용 기능 구성  {#configure-the-auto-apply-policy-feature-in-the-msi-file}

시작하기 전에 이 문서의 초반부에서 설명한 대로 설치 프로그램이 LiveCycle 또는 AEM 양식 서버를 가리키도록 사전 구성합니다.

1. **[!UICONTROL 시작 > 프로그램 > Orca]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 파일 > 열기]**&#x200B;를 클릭한 다음 `DocumentSecurityExtensionforMicrosoftOffice.msi` 파일을 찾습니다.

1. 표의 왼쪽 목록에서 속성을 선택합니다.

1. 기업 Rights Management 또는 Document Security 설치에 해당하는 다음 키 이름 값을 편집합니다.

<table>
 <tbody>
  <tr>
   <td><p><strong>키 이름</strong></p> </td>
   <td><p><strong>설명</strong></p> </td>
   <td><p><strong>키 </strong><strong></strong><strong>값 기본값</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_IS_AUTO_ APPLY</code></p> </td>
   <td><p>정책 자동 적용 기능을 활성화하거나 비활성화합니다.</p> <p><code>1</code>: 사용</p> <p>0:비활성화</p> </td>
   <td><p>0</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_POLICY_I D</code></p> </td>
   <td><p>새 문서를 저장할 때 사용할 정책 GUID. 정책 자동 적용 기능에 적용됩니다.</p> </td>
   <td><p>RM 서버에 표시되는 16진수 정책 ID</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_U RL</code></p> </td>
   <td><p>서버 URL.</p> </td>
   <td><p>default.corp.com</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_P ORT_NO</code></p> </td>
   <td><p>서버 포트 번호입니다.</p> </td>
   <td><p>1234년</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE</code></p> </td>
   <td><p>클라이언트가 처음 저장 시 문서를 보호하기 위해 서버에 접속할 수 없는 경우 Document Security 보호 없이 문서를 작성할 수 있는지 여부를 결정합니다.</p> <p>1:보호되지 않은 저장 허용 </p> <p>0:클라이언트가 문서를 저장할 수 있도록 서버에 연결할 수 없는 경우 새 문서를 만들 수 없도록 합니다.</p> </td>
   <td><p>0</p> </td>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>`AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE` 이 옵션은 고객에게 모든 문서를 보호하도록 강요하지 않고 보호하도록 상기시키려는 경우에 유용합니다. 또한 네트워크 연결이 끊어진 상태에서 사용자가 문서를 작성한다는 사실을 알고 있을 때도 유용합니다. 문서를 만들고 저장할 수 없도록 설정할 수 있습니다.

1. 원본 MSI 파일이 포함된 같은 디렉토리에 수정된 파일을 저장합니다.

   >[!NOTE]
   >
   >원본 MSI 파일(예: `DocumentSecurityExtensionforMicrosoftOffice.msi`)과 동일한 파일 이름을 사용하는 것이 일반적인 방법입니다.

## 새 문서 {#enabling-automatic-protection-of-new-documents} 자동 보호 사용

관리자는 사용자가 저장하는 모든 문서를 자동으로 보호하는 기능을 활성화할 수 있습니다. 관리자는 Document Security Extension for Microsoft Office의 설치 프로그램에 정책 자동 적용 기능을 구성합니다.

정책 자동 적용을 사용하는 경우 사용자가 저장하는 모든 문서는 기본 정책으로 보호됩니다. 이 작업은 다음과 같은 경우에 적용됩니다.

* 사용자가 새 문서를 만들고 편집하고 저장하는 경우
* 사용자가 보호되지 않은 문서를 열고 편집하고 저장할 때

정책 자동 적용 구성에 대한 자세한 내용은 [기본 정책](installing-configuring-aemdsext.md#p-configuring-automatic-application-of-a-default-policy-p)의 자동 응용 프로그램 구성을 참조하십시오.

## 리본 없는 사용자 인터페이스 사용 {#enable-ribbon-less-user-interface}

Windows 레지스트리에서 설정을 수정하여 리본이 없는 사용자 인터페이스를 활성화/비활성화할 수 있습니다. 레지스트리를 업데이트하고 리본이 없는 사용자 인터페이스를 활성화하려면 다음 단계를 수행하십시오.

1. Windows 레지스트리를 변경하기 전에 백업하십시오. 자세한 지침은 [Windows 레지스트리 수정 방법](https://support.microsoft.com/en-us/kb/136393)을 참조하십시오.
1. 레지스트리 편집기에서 HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 또는 HKEY_LOCAL_MACHINE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0으로 이동합니다.
1. **HidePluginUI**&#x200B;이라는 새 Dword(32비트) 값을 만듭니다.

1. 리본 없는 사용자 인터페이스를 사용하려면 **HidePluginUI **속성의 값을 1로 설정합니다.

1. 레지스트리 편집기를 닫습니다.

## Microsoft Excel {#enable-watermark-for-printing-in-microsoft-excel}에서 인쇄를 위한 워터마크 사용

Windows 레지스트리 설정을 변경하여 동적 워터마크와 기존 머리말 및 꼬리말이 함께 표시되도록 할 수 있습니다. 레지스트리 설정을 사용하면 인쇄 중에만 워터마크를 사용할 수 있습니다. 인쇄 중에 레지스트리를 업데이트하고 워터마크를 활성화하려면 다음 단계를 수행하십시오.

1. Windows 레지스트리를 변경하기 전에 백업하십시오. 자세한 지침은 [Windows 레지스트리 수정 방법](https://support.microsoft.com/en-us/kb/136393)을 참조하십시오.
1. 레지스트리 편집기에서 HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 또는 HKEY_LOCAL_MACHINE\WOW6432NODE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0으로 이동합니다.
1. 새 레지스트리 키 **WatermarkMode**&#x200B;를 만듭니다.
1. WatermarkMode 레지스트리 키에서 DWORD **WatermarkMode**&#x200B;를 만들고 DWORD **WatermarkMode**&#x200B;의 값을 **1**&#x200B;로 설정합니다.

1. 레지스트리 편집기를 닫습니다.

>[!NOTE]
>
>Windows 탐색기에서 파일 메뉴 또는 컨텍스트 메뉴를 사용하여 Microsoft Excel 문서를 만들 수 있습니다. 명시된 방법으로 만든 문서의 경우 인쇄 날짜를 검색하거나 변경할 수 없습니다. Microsoft Excel의 제한 사항입니다. AEM Document Security 워터마크는 문서의 인쇄 날짜에 따라 다릅니다. 따라서 이러한 문서의 경우 워터마크는 이전 날짜로 되돌려집니다. 머리말 및 꼬리말도 유지되지 않습니다.

## {#coverpage} 문서에 사용자 정의 표지 페이지 추가

AEM Document Security for Microsoft Office 플러그인이 설치되어 있지 않은 컴퓨터에서 보호된 문서를 열 수 있습니다. 이러한 시스템은 문서를 열 수 없습니다. 이러한 컴퓨터에서는 AEM Document Security for Microsoft Office 플러그인 다운로드 지침 및 기타 정보가 포함된 표지 페이지를 표시할 수 있습니다.

### 표지 페이지를 구성하기 전에 {#before-you-configure-a-cover-page}

* CommonResources.dll 파일을 백업합니다. 기본 경로는 다음과 같습니다.

   * **(32비트 컴퓨터의 32비트 사무실)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(64비트 컴퓨터의 32비트 office용)** C:\Program Files (x86)\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(64비트 컴퓨터의 64비트 office용)** C:\Program Files\Adobe\Adobe Experience Manager Forms\Document Security Extension

* Microsoft Visual Studio 2008 이상이 설치되어 있는지 확인합니다. 다른 유틸리티를 사용하여 DLL 파일을 편집할 수도 있습니다.
* templates.zip 아카이브 추출 보관 파일에는 표지 페이지의 .xlsx, .docx 및 .pptx 템플릿이 포함되어 있습니다. .xlsx, .docx 및 .pptx 파일 유형에 대해 제공된 템플릿만 사용합니다. 다른 파일 유형에 대해 고유한 템플릿을 만들 수 있습니다. 사용자 정의 메시지와 지침을 포함하도록 템플릿을 사용자 정의할 수 있습니다. template.zip은 다음 위치에서 찾을 수 있습니다.

[파일 가져오기](assets/templates.zip)

### CommonResources.dll 파일 {#structure-of-the-commonresources-dll-file} 구조

CommonResources.dll 파일에는 리소스 템플릿에 대한 정보가 포함되어 있습니다. 여기에는 두 개의 이름 식별자 TEMPLATE_FILE과 RT_MANIFEST가 포함되어 있습니다. 사용자 지정 표지 페이지를 활성화하려면 TEMPLATE_FILE 이름 식별자가 수정되었습니다. TEMPLATE_FILE 이름 식별자에는 6개의 리소스가 있습니다.

<table>
 <tbody>
  <tr>
   <td><p><strong>리소스</strong></p> </td>
   <td><p><strong>표시 </strong></p> </td>
  </tr>
  <tr>
   <td><p>101년 </p> </td>
   <td><p>.xls</p> </td>
  </tr>
  <tr>
   <td><p>102년</p> </td>
   <td><p>.doc</p> </td>
  </tr>
  <tr>
   <td><p>103년 </p> </td>
   <td><p>.ppt</p> </td>
  </tr>
  <tr>
   <td><p>104년 </p> </td>
   <td><p>.xlsx</p> </td>
  </tr>
  <tr>
   <td><p>105년</p> </td>
   <td><p>.docx</p> </td>
  </tr>
  <tr>
   <td><p>106년</p> </td>
   <td><p>.pptx</p> </td>
  </tr>
 </tbody>
</table>

#### 템플릿을 표지 페이지 {#configure-the-template-as-a-cover-page}로 구성합니다.

1. Microsoft Visual Studio를 엽니다. 편집할 CommonResources.dll 파일을 찾아 엽니다.

   >[!NOTE]
   >
   >파일이 솔루션 탐색기 창에 나타나지 않으면 [다음으로 열기] 옵션을 사용하여 파일을 다시 엽니다. 리소스 편집기를 편집기로 선택합니다.

1. 솔루션 탐색기 창에서 TEMPLATE_FILE 디렉토리를 확장하고 리소스 101을 삭제합니다.

1. 리소스를 추가합니다.

   1. 솔루션 탐색기에서 프로젝트를 선택하고 프로젝트 메뉴에서 속성을 클릭합니다.
   1. 리소스 탭을 선택합니다.
   1. 리소스 디자이너 도구 모음에서 리소스 추가를 가리킨 다음 화살표를 클릭합니다. 리소스 유형에 대해 TEMPLATE_FILE을 선택하고 가져오기를 클릭합니다.
   1. 기존 파일을 리소스에 추가 대화 상자에서 Resource.xlsx 파일을 찾은 다음 열기를 클릭합니다. 파일이 TEMPLATE_FILE 디렉토리에 추가됩니다.

   >[!NOTE]
   >
   >언어 설정이 올바른지 확인하십시오. 중립 언어로 리소스를 삭제합니다.

1. 모든 리소스 유형에 대해 2단계와 3단계를 반복합니다.

   >[!NOTE]
   >
   >리소스 유형을 임의 순서로 삭제하고 추가하지 마십시오. 101 후 102 등을 구성합니다.

### Microsoft Office용 AEM Document Security 확장 프로그램 설치 프로그램으로 사용자 정의 CommonResources.dll 파일 패키지 {#package-custom-commonresources-dll-file-with-the-installer-of-aem-document-security-extension-for-microsoft-office}

CommonResources.dll 파일을 사용자 지정하여 사용자 정의 표지 페이지를 추가할 수 있습니다. 파일을 사용자 정의한 후 원본 파일을 모든 워크스테이션에서 사용자 정의 파일로 직접 바꾸거나 자동화된 방법을 선택하여 파일을 대체할 수 있습니다.

큰 환경에서는 기본 `CommonResources.dll file`을 사용자 지정 `CommonResources.dll` 파일로 수동으로 교체하는 것이 어렵고 지루합니다. 자동 압축 해제 및 패키징 도구(예: WinZip 자동 압축 풀기)를 사용하여 사용자 정의 CommonResources.dll 파일을 AEM Document Security Extension for Microsoft Office 설치 프로그램으로 패키지화할 수 있습니다. 나중에 사용자 정의 설치 프로그램을 모든 워크스테이션에 배포할 수 있습니다. 이 방법을 사용하면 기본 `CommonResources.dll` 파일을 사용자 정의 파일로 바꾸는 데 필요한 시간이 줄어듭니다. 또한 모든 워크스테이션에 필요한 CommonResources.dll 파일이 있는지 확인합니다. 자동 압축 해제 및 패키징 툴은 파일을 자동으로 교체하는 다양한 방법 중 하나입니다. 환경에 적합한 방법을 선택할 수 있습니다.

다음 단계를 수행하여 AEM Document Security extension for Microsoft Office 설치 프로그램을 사용하여 사용자 정의 `CommonResources.dll` 파일을 패키지화할 수 있습니다.

1. 자체 추출기 및 패키저 도구를 설치합니다. 예: WinZip 자체 추출기.
1. 새 폴더를 만듭니다. 예: YOUR_FOLDER_NAME
1. AEM Document 보안 확장 프로그램의 원래 설치 프로그램과 사용자 정의 CommonResources.dll 파일을 새로 만든 폴더에 배치합니다.
1. 폴더에 일괄 처리 파일을 만듭니다. 예: YOUR_FOLDER_NAME\Installer.bat
1. 편집할 배치 파일을 열고 일괄 처리 파일에 다음 코드를 추가합니다.

   ```shell
    @echo off
   
    setlocal EnableDelayedExpansion
   
    msiexec /i YOUR_FOLDER_NAME\MSI_NAME.exe
   
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\HARDWARE\DESCRIPTION\System\CentralProcessor\0" /v "Identifier"') DO set "IDENTIFIER=%%B"
   
    set IDENTIFIER= %IDENTIFIER: =%
   
    if not %IDENTIFIER:x86=%==%IDENTIFIER% (
   
    REM Fetching install path for 32 bit machine.
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
    ) else (
   
        REM Fetching install path for 64 bit machine.
   
            FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Wow6432Node\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
        )
   
    COPY "YOUR_FOLDER_NAME\CommonResources.dll" "%INSTALLPATH%"
   
    endlocal
   ```

   LiveCycle Rights Management ES4 및 11.0.0 버전 외에 JEE에서 다른 버전의 LiveCycle 또는 AEM Forms을 사용하는 경우 레지스트리 키의 경로를 다음과 같이 바꿉니다.

   * (Livecycle Rights Management ES2 및 버전 9.0):*HKLM\SOFTWARE\Adobe/LiveCycle* *Rights Management ES2\9.0 *
   * (Livecycle Rights Management ES3 및 버전 10.0)
   * (Livecycle Rights Management ES4 및 버전 11.0) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0
   * (AEM 6.0 Forms(JEE 이상 버전) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0

1. 위의 코드에서 YOUR_FOLDER_NAME의 모든 인스턴스를 2단계에서 만든 폴더의 이름으로 바꿉니다.
1. **(AEM Document Security extension for Microsoft Office 설치 프로그램(.exe 확장자만)** 다음 코드 줄을 바꿉니다.

   `msiexec /i YOUR_FOLDER_NAME\MSI_NAME.msi`
with

   `START /w YOUR_FOLDER_NAME\APPLICATION_NAME.exe`

1. 배치 파일을 저장하고 닫습니다.
1. 자체 추출기 및 패키저 도구를 사용하여 사용자 정의 CommonResources.dll 파일, Microsoft Office용 AEM Document Security 확장 프로그램의 원래 설치 프로그램 및 일괄 처리 파일이 포함된 폴더를 패키지화할 수 있습니다.

   >[!NOTE]
   >
   >자동 압축 해제 패키지가 관리자로 실행되도록 설정되고 자동으로 실행되는지 확인
   >추출 완료 시 배치 파일을 실행합니다.

이제 AEM Document Security extension for Microsoft Office의 자동 압축 해제 설치 프로그램은 사용자 정의 CommonResources.dll 파일을 패키징하고 배포할 수 있습니다.
