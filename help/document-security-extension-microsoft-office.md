---
title: AEM Document Security Extension for Microsoft Office 소개
description: Document Security Extension for Microsoft Office를 사용하면 미리 정의된 기밀 설정을 Microsoft Office 파일에 적용할 수 있습니다.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
translation-type: tm+mt
source-git-commit: 19de0b62ac493c7507581abb607b008c64f77597
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---


# AEM Document Security Extension for Microsoft Office 소개{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office에서는 권한이 부여된 사람만이 지적 재산이 포함된 Word, Excel 및 PowerPoint 파일을 사용할 수 있습니다. Document Security Extension for Microsoft Office를 사용하면 미리 정의된 기밀 설정을 파일에 적용할 수 있습니다.

Document Security Extension for Microsoft Office는 Adobe Experience Manager Forms용 LiveCycle Rights Management 및 Document Security 추가 기능을 확장하여 Word, Excel 및 PowerPoint 파일을 보호하고 이 소프트웨어를 설치한 권한이 있는 사용자가 정책으로 보호된 파일을 정책에 설정된 기밀 설정에 따라 사용할 수 있도록 합니다.

## Document Security가 지적 재산 {#how-document-security-protects-intellectual-property}을 보호하는 방법

Document Security에서는 권한이 부여된 사람만이 지적 재산이 포함된 파일을 사용할 수 있습니다. Document Security를 사용하면 기밀 정책을 사용하여 파일을 보호할 수 있습니다. *정책*&#x200B;은 기밀 설정과 권한이 있는 사용자 목록이 포함된 정보 모음입니다. 정책에서 지정하는 설정에 따라 정책을 적용하는 파일을 받는 사람이 사용할 수 있는 방법이 결정됩니다. 예를 들어 받는 사람이 텍스트를 인쇄 또는 복사하거나 변경 내용을 저장할 수 있는지 여부를 지정할 수 있습니다.

Document Security 관리자와 사용자는 정책을 만듭니다. 관리자는 권한이 있는 모든 사용자가 사용할 수 있는 조직 정책을 만듭니다. 관리자 또는 정책 집합 코디네이터는 사용자 하위 집합에서 사용할 수 있는 *정책 집합*&#x200B;이라는 정책 그룹도 만들 수 있습니다. 사용자는 자신만이 사용할 수 있는 고유한 정책을 만들 수 있습니다. 관리자, 정책 집합 코디네이터 및 사용자는 Document Security 웹 페이지를 사용하여 정책을 만듭니다.

정책은 Document Security에 저장되지만 Word, Excel 또는 PowerPoint를 통해 파일에 적용할 수 있습니다. 파일에 정책을 적용하면 파일에 포함된 정보가 정책에 지정된 기밀 설정으로 보호됩니다. 정책으로 보호된 파일을 배포하는 경우 정책으로 권한이 부여된 받는 사람만 파일 내용에 액세스할 수 있습니다.

정책을 사용하여 파일을 보호하면 파일을 배포한 후에도 해당 파일을 지속적으로 제어할 수 있습니다. 이벤트를 감사하여 받는 사람이 파일을 사용하는 시기와 방법을 추적하고, 정책을 변경하고, 사용자가 파일에 계속 액세스하지 못하도록 방지하고 파일에 첨부된 정책을 변경할 수 있습니다.

## 정책 작동 방식 {#how-policies-work}

정책에는 권한이 있는 사용자에 대한 정보와 지적 재산권에 적용할 기밀 설정이 포함되어 있습니다. 사용자는 연결된 LDAP 또는 Active Directory 목록에 포함되어 Document Security에서 인식되는 모든 사용자가 해당될 수 있습니다. 또한 Document Security에 등록하도록 초대를 받았거나 관리자가 계정을 만든 사람일 수도 있습니다.

정책의 기밀 설정에 따라 받는 사람이 정책으로 보호된 파일을 사용할 수 있는 방법이 결정됩니다. 예를 들어 정책을 통해 받는 사람이 파일을 인쇄하거나 다른 파일에 컨텐츠를 복사하거나 보호된 파일에 변경 사항을 저장할 수 있는지 여부를 지정할 수 있습니다. 정책에 따라 다양한 사용자에 대해 서로 다른 기밀 설정을 지정할 수도 있습니다.

파일에 정책을 적용하면 파일에 포함된 정보가 정책에 지정된 기밀 설정으로 보호됩니다. 파일을 배포하면 Document Security에서 파일을 열려고 시도한 받는 사람을 인증하고 정책에 지정된 권한에 따라 액세스 권한을 부여합니다.

정책을 파일에 적용한 후 언제든지 정책의 기밀 설정을 변경할 수 있으므로 권한이 있는 사용자를 추가 또는 제거하거나 사용자가 파일을 받은 후 사용자에 대한 권한을 변경할 수 있습니다. 파일에 적용된 정책은 변경할 수 있으며 파일 사본이 있는 사람은 더 이상 파일을 열 수 없도록 파일에 대한 액세스를 폐지할 수 있습니다.

정책에서 오프라인 액세스를 허용하는 경우 받는 사람은 정책에 지정된 기간 동안 인터넷이나 네트워크에 연결하지 않고 오프라인으로 정책으로 보호된 파일을 사용할 수도 있습니다.

## 정책으로 보호된 파일의 작동 방식 {#how-policy-protected-files-work}

사용자가 정책으로 보호된 Word, Excel 및 PowerPoint 파일을 열고 사용하려면 정책을 통해 해당 사용자를 받는 사람으로 포함하거나 익명 액세스를 허용해야 하며 사용자는 Document Security Extension for Microsoft Office를 설치해야 합니다. Document Security Extension for Microsoft Office를 사용하지 않는 사람에게 정책으로 보호된 파일을 주려면 소프트웨어 사본을 주거나 웹 사이트에서 소프트웨어를 다운로드하는 방법을 알려 줍니다. 설치 프로그램이 없는 경우 [다운로드 페이지](https://www.adobe.com/products/livecycle/rightsmanagement/extension/downloads.html)에서 다운로드할 수 있습니다.

사용자가 정책으로 보호된 파일을 열려고 하면 Document Security Extension for Microsoft Office는 Document Security에 연결하여 사용자를 인증합니다. Document Security가 파일 사용을 감사하도록 구성된 경우 사용자에게 파일 사용이 현재 감사 중임을 나타내는 알림이 표시됩니다. Document Security는 사용자에게 부여할 파일 권한을 결정하며 다음 조건에서 사용자가 정책 설정에 따라 파일을 사용할 수 있습니다.

* 정책에 지정된 유효 기간에 사용할 수 있습니다.
* 관리자나 정책을 적용한 사람이 파일에 대한 액세스를 폐지하거나 정책을 변경할 때까지 사용할 수 있습니다.

   정책을 적용한 사람이 정책을 변경하거나 파일에 대한 액세스를 폐지하면 사용자가 파일을 이미 가지고 있어도 파일에 대한 사용자의 권한이 변경되거나 제거됩니다. 파일 자체가 폐지된 경우 업데이트된 사본을 얻기 위해 사용자에게 URL을 제공할 수 있습니다.

   정책에서 오프라인 액세스를 허용하는 경우 정책에 지정된 오프라인 제공 기간 동안 인터넷 또는 네트워크에 연결하지 않고 오프라인으로 정책으로 보호된 파일을 열 수 있습니다. 오프라인 제공 기간이 끝나면 사용자는 온라인 상태로 전환하여 Document Security와 동기화해야 합니다. 그러면 제공 기간이 새로 시작됩니다.

   정책이 파일을 저장할 수 있도록 허용하고 사용자가 정책으로 보호된 파일의 사본을 저장하면 저장된 파일에 정책이 자동으로 적용되고 적용됩니다. 새 파일을 열려는 시도와 같은 이벤트도 원본 파일과 동일하게 감사 및 기록됩니다.

## Document Security를 사용하여 파일 {#using-document-security-to-protect-your-files} 보호

정책을 사용하여 다양한 상황에서 파일을 보호할 수 있습니다.

예를 들어 제조업체는 새 제품에 부품을 제공할 공급업체의 입찰을 수락합니다. 제조업체는 입찰자에게 최종 제출에 필요한 독점 정보를 제공해야 합니다. 제조업체는 Document Security를 사용하여 입찰자가 파일을 열고 정보를 볼 수 있는 정책으로 파일을 보호합니다. 그러나 입찰자는 파일을 변경, 인쇄 또는 복사할 수 없으며 권한이 없는 사람은 파일을 열 수 없습니다.

제조업체는 입찰 중 하나를 수락하면 정책을 업데이트하여 낙찰된 입찰자에게 변경 내용을 로컬로 인쇄, 복사 및 저장할 수 있는 권한을 주고 낙찰되지 않은 입찰자가 더 이상 파일을 열 수 있는 권한이 없도록 해당 입찰자를 제거합니다.

제조업체 엔지니어는 낙찰된 입찰자와 함께 작업하는 동안 파일의 디자인 사양을 일부 변경합니다. 제조업체는 새 사양을 게시하기 위해 일부 파일에 대한 액세스를 폐지하고 새 버전을 게시합니다. 낙찰된 입찰자의 엔지니어가 파일을 열려고 하면 파일에 대한 액세스가 폐지되었다는 메시지가 표시됩니다. 이 메시지에는 새 버전의 파일을 다운로드할 수 있는 URL이 포함되어 있습니다.

## 추가 정보 {#additional-information}

이 표의 리소스를 통해 AEM Document Security에 대한 자세한 내용을 살펴볼 수 있습니다.

<table >
 <tbody>
  <tr>
   <th><p>자세한 내용은</p> </th>
   <th><p>자세한 내용은</p> </th>
  </tr>
  <tr>
   <td><p>AEM 양식 관리자 도움말</p> </td>
   <td><p><a href="http://www.adobe.com/go/learn_aemforms_admin_65">Administrator </a> Helper는 Document Security 관리 페이지에서 페이지의 오른쪽 상단에 있는 도움말 링크를 클릭합니다.</p> </td>
  </tr>
  <tr>
   <td><p>이 제품 버전에 대한 패치 업데이트, 기술 정보 및 추가 정보</p> </td>
   <td><p><a href="https://helpx.adobe.com/kr/marketing-cloud/contact-support.html">Marketing Cloud 기술 지원</a></p> </td>
  </tr>
 </tbody>
</table>

