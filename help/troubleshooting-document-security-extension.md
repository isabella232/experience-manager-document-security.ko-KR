---
title: Microsoft Office용 AEM Document Security 확장 문제 해결
description: AEM Document Security Extension for Microsoft Office를 설치, 구성 또는 사용하는 데 문제가 있는 경우 이 문서에 나열된 지침을 따르십시오.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
translation-type: tm+mt
source-git-commit: ac26ec61f62d7a3db2429c8a9d3f68b82ba8f77a
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Microsoft Office용 AEM Document Security 확장 문제 해결{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## 설치 및 구성 문제 해결 {#troubleshootinginstallationandconfiguration}

Microsoft Office용 AEM Document Security Extension을 설치하고 구성하는 데 문제가 있는 경우 [설치](installing-configuring-aemdsext.md) 집필의 - 설치 전에 에 나열된 지침을 주의 깊게 따르십시오.

설명서에 따라 모든 것을 설치 및 구성한 경우 다음 섹션에서 사용 중인 문제와 유사한 문제를 검토하십시오.

### Document Security Extension을 Microsoft Office 응용 프로그램 {#document-security-extension-fails-to-load-for-microsoft-office-applications}에 대해 로드하지 못했습니다.

Windows 레지스트리의 LoadBehavior 속성은 문서 보안 플러그인의 런타임 동작을 지정합니다. LoadBehavior 속성이 3으로 설정된 경우 모든 플러그인이 자동으로 로드됩니다. Document Security Extension for Microsoft office를 설치하기 전에 LoadBehavior 속성 값이 3으로 설정되어 있는지 확인하십시오.

1. Windows 레지스트리를 변경하기 전에 백업하십시오. 자세한 지침은 [Windows 레지스트리 수정 방법](https://support.microsoft.com/en-us/kb/136393)을 참조하십시오.
1. 레지스트리 편집기에서 toHKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin 또는 HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM으로 이동합니다.
1. **LoadBehavior** 속성 값을 3으로 설정합니다.

1. 레지스트리 편집기를 닫습니다.

LoadBehavior에 대한 자세한 내용은 [VSTO 추가 기능에 대한 레지스트리 항목](https://msdn.microsoft.com/en-us/library/bb386106.aspx#LoadBehavior) 문서를 참조하십시오.

## 관리 작업 문제 해결 {#admintasks}

이 섹션에서는 설치된 AEM Document Security Extension의 가능한 문제를 설명합니다.

### Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension} 설치 시 Microsoft Office 응용 프로그램이 원활하게 시작되지 않습니다.

Document Security Extension이 설치되고 온-액세스 검색을 사용하는 McAfee VirusScan이 활성화된 시스템에서 Office 응용 프로그램이 원활하게 시작되게 하려면 McAfee VirusScan 콘솔에서 [버퍼 오버플로 방지] 옵션을 비활성화하십시오.
