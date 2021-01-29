---
title: Microsoft Office용 AEM Document Security - 릴리스 노트
description: AEM Document Security 6.2 Extension for Microsoft Office를 설치하기 전에 릴리스 정보를 참조하십시오.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
translation-type: tm+mt
source-git-commit: 403b800eab086d131beb65a496836158778954ee
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---


# Microsoft Office용 AEM Document Security - 릴리스 노트{#aem-document-security-for-microsoft-office-release-notes}

## Microsoft Office용 AEM Document Security {#whats-new-in-aem-document-security-for-microsoft-office}의 새로운 기능

* **Office 2019** 지원:Document Security Extension for Microsoft Office 2019에 대한 지원이 추가되었습니다. 또한 Office 365의 일부로 설치된 Microsoft Office 2019 데스크탑 응용 프로그램에서도 작동될 예정입니다.

>[!NOTE]
>
>이 문서에서는 Microsoft Office용 Adobe Experience Manager Document Security, Microsoft Office용 Adobe Experience Manager Document Security Extension 및 Document Security Extension for Microsoft Office의 혼용된 방식으로 용어를 사용합니다.

## Microsoft Office용 AEM Document Security Extension 설치 및 구성 {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

이 버전의 Document Security Extension for Microsoft Office는 AEM 양식용 Adobe LiveCycle Rights Management ES2 이상 및 Document Security Add-on과 호환됩니다.

AEM Document Security Extension for Microsoft Office를 설치하기 전에 이 문서의 정보를 검토하십시오. 설치 지침에 대한 자세한 내용은 [Microsoft Office용 AEM Document Security Extension 설치 및 구성](installing-configuring-aemdsext.md) 문서를 참조하십시오.

## 해결된 문제 {#fixed-issues}

* 문자열은 세로로 표시되며 컨텐츠에 잘못된 줄 바꿈이 추가됩니다. (Ref# CQ-4201054)

## 알려진 문제 {#known-issues}

### 타사 플러그인은 지원되지 않음 {#third-party-plug-ins-not-supported}

AEM Document Security Extension for Microsoft Office는 타사 플러그인과 작동하지 않습니다. Document Security Extension for Microsoft Office를 설치하기 전에 Microsoft Office용 타사 플러그인을 제거합니다.

### Microsoft Word, Excel 및 PowerPoint에서 메뉴 옵션이 비활성화됨 {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office는 내장된 보호 기능을 사용하여 문서, 워크시트 및 프레젠테이션을 보호합니다. 일부 Excel, Word 및 PowerPoint 메뉴 옵션이 비활성화됩니다.

### Microsoft Office 2013, 2016 및 2019에 대한 제한 사항 {#restrictions-for-microsoft-office}

Microsoft Office에서는 보호된 세션 중에 다음 옵션을 사용할 수 없습니다.

* Microsoft Office 2016 또는 Microsoft Office 2019

   * 파일 > 다른 이름으로 저장
   * 파일 > 작업 내역
   * 파일 > 공유
   * 파일 > 내보내기
   * 파일 > 게시
   * 파일 > 계정
   * 파일 > 정보 > Protect 문서/통합 문서/프레젠테이션 > 암호로 암호화
   * 파일 > 정보 > Protect 문서 > 디지털 서명 추가
   * 파일 > 정보 > Protect 문서 > 최종본으로 표시
   * 오른쪽 위에 있는 공유 옵션

* Microsoft Office 2013

   * 파일 > 다른 이름으로 저장
   * 파일 > 공유
   * 파일 > 내보내기
   * 파일 > 계정
   * 파일 > 정보 > Protect 문서/통합 문서/프레젠테이션 > 암호로 암호화
   * 파일 > 정보 > Protect 문서 > 디지털 서명 추가
   * 파일 > 정보 > Protect 문서 > 최종본으로 표시

### SharePoint Server {#opening-a-protected-document-from-sharepoint-server}에서 보호된 문서를 여는 중

보호된 문서 열기:Microsoft Word, Microsoft Excel 또는 Microsoft PowerPoint와 같은 파일 형식과 관련된 Microsoft Office 프로그램을 먼저 열지 않고 SharePoint Server의 Document Security Extension for Microsoft Office에서 보호된 문서를 열려고 하면 문서가 열리지 않을 수 있습니다. 해당 플러그인을 설치한다는 오류 메시지가 표시됩니다. 따라서 SharePoint Server의 Document Security Extension for Microsoft Office에서 보호된 문서를 열기 전에 관련 Microsoft Office 프로그램을 여는 것이 좋습니다.

(선택 사항) 캐시 폴더를 지운 후에 SharePoint Server의 Document Security Extension for Microsoft Office에서 보호된 문서를 여는 것이 좋습니다.

SharePoint Server에서 보호된 문서를 열면 적용된 정책에 상관없이 문서에 대한 모든 권한이 비활성화됩니다.

### 프린터를 설치하지 않은 Microsoft Excel 2013, Microsoft Excel 2016 및 Microsoft Excel 2019 파일에 동적 워터마크가 있는 정책을 적용합니다 {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

프린터가 설치되어 있지 않은 컴퓨터에서 동적 워터마크가 있는 정책을 Microsoft Excel 2013, Microsoft Excel 2016 및 Microsoft Excel 2019 파일에 적용한 다음 파일을 저장하면 다음 오류가 표시됩니다.&quot;동적 워터마크를 적용하는 동안 내부 오류가 발생했습니다.&quot; 이 오류는 보호된 파일을 다시 열 때도 나타납니다. 워터마크는 적용되지 않으며 보기 > 페이지 레이아웃에서 볼 수 없습니다.

### 지원되는 Office 응용 프로그램에 대해 Windows 데이터 실행 방지 비활성화 {#disable-windows-data-execution-prevention-for-supported-office-applications}

Document Security Extension for Microsoft Office 응용 프로그램을 사용할 때는 Windows DEP(데이터 실행 방지) 설정을 비활성화하는 것이 좋습니다.

### 공유 Microsoft Office 파일은 Document Security Extension {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}을(를) 사용하여 보호할 수 없습니다.

Document Security Extension을 사용하여 공유 Microsoft Office 파일을 보호하는 경우 오류가 발생하고 공유 파일의 보안이 해제됩니다.

### Document Security Extension for Microsoft Office 및 McAfee VirusScan이 포함된 시스템에서 Office 응용 프로그램 시작 {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Document Security가 설치되고 온-액세스 검색을 사용하는 McAfee VirusScan이 활성화된 시스템에서 Office 응용 프로그램이 원활하게 시작되게 하려면 McAfee VirusScan 콘솔에서 [버퍼 오버플로 방지] 옵션을 비활성화하십시오.

### 지원되지 않는 Microsoft Office 언어인 {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}의 컴퓨터에 Document Security Extension for Microsoft Office 설치

지원되지 않는 언어로 Microsoft Office 응용 프로그램을 사용하는 컴퓨터에 Document Security Extension for Microsoft Office를 설치하기 전에 Office 응용 프로그램을 최소 한 번 여십시오.

### 사용자에게 오프라인 권한이 {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions} 없는 경우에도 [오프라인 동기화] 단추가 활성화됩니다

사용자에게 문서에 대한 오프라인 권한이 없는 경우에도 [오프라인 동기화] 단추를 사용할 수 있습니다. 그러나 단추를 선택하더라도 아무 작업도 수행되지 않습니다.

### Microsoft Office 시험버전 {#no-support-for-trial-versions-of-microsoft-office}은(는) 지원되지 않습니다.

Document Security extension for Microsoft Office는 Microsoft Office 추적 버전을 지원하지 않습니다. 확장 프로그램을 설치하기 전에 Microsoft Office의 라이선스가 부여된 복사본을 설치했으며 이 사본이 활성화되었는지 확인하십시오.

### 보호된 Microsoft Office 파일 {#unable-to-open-a-protected-microsoft-office-files}을(를) 열 수 없습니다.

Microsoft Office의 보호된 보기를 사용하는 경우 Right Management Extension은 원격 위치에서 보호된 Microsoft Excel 파일(XLS, XLSX) 및 보호된 Microsoft PowerPoint(PPT) 파일을 열 수 없습니다.

### 이미지 또는 배경색이 포함된 Microsoft Excel 문서의 셀이 워터마크 {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark} 위에 나타납니다.

Microsoft Excel 문서의 셀에 이미지가 포함되어 있거나 배경색으로 채워져 있는 경우 문서에 동적 워터마크 정책이 적용된 경우 워터마크 맨 위에 해당 셀에 채워진 이미지나 배경색이 나타나고 워터마크를 덮습니다.

### 여러 인증서 {#usability-issue-with-multiple-certificates} 사용 문제

클라이언트 컴퓨터에 인증서가 여러 개 있고 사용자가 인증서 선택 대화 상자를 취소하면 대화 상자가 다시 나타나고 사용자는 대화 상자를 두 번 취소해야 합니다.

### Microsoft PowerPoint에서 보호된 문서 편집 가능 {#microsoft-powerpoint-allows-editing-protected-documents}

보호된 문서를 편집하려고 하면 &quot;이 문서를 수정할 수 없습니다. 변경 내용을 저장할 수 없습니다.&quot; 메시지를 닫은 후에도 텍스트를 추가하거나 문서를 편집할 수 있습니다. 그러나 보호된 문서의 변경 내용은 저장되지 않습니다.

위에 언급된 동작은 PowerPoint 2013, PowerPoint 2016 및 PowerPoint 2019에서 예상한 대로 이루어집니다.
