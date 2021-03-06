---
title: '&lt;netMsmqBinding&gt;'
ms.date: 03/30/2017
ms.assetid: a68b44d7-7799-43a3-9e63-f07c782810a6
ms.openlocfilehash: 05ab1b064f6dd7bb28d1d118ec8c4249da5a75e1
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44087592"
---
# <a name="ltnetmsmqbindinggt"></a>&lt;netMsmqBinding&gt;
시스템 간 통신에 적합한 대기 중인 바인딩을 정의합니다.  
  
 \<system.ServiceModel>  
\<바인딩 >  
\<netMsmqBinding>  
  
## <a name="syntax"></a>구문  
  
```xml  
<netMsmqBinding>  
    <binding   
       closeTimeout="TimeSpan"   
       customDeadLetterQueue="Uri"  
       deadLetterQueue="Uri"  
       durable="Boolean"  
       exactlyOnce="Boolean"   
       maxBufferPoolSize="Integer"  
       maxReceivedMessageSize"Integer"  
       maxRetryCycles="Integer"   
       name="string"   
       openTimeout="TimeSpan"   
       poisonMessageHandling="Disabled/EnabledIfSupported"   
       queueTransferProtocol="Native/Srmp/SrmpSecure"  
       receiveErrorHandling="Drop/Fault/Move/Reject"  
       receiveTimeout="TimeSpan"   
       receiveRetryCount="Integer"  
       rejectAfterLastRetry="Boolean"   
       retryCycleDelay="TimeSpan"    
       sendTimeout="TimeSpan"   
       timeToLive="TimeSpan"    
       useActiveDirectory="Boolean"  
       useMsmqTracing="Boolean  
       useSourceJournal="Boolean"  
          <security>  
                  <message    
                        algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            clientCredentialType="None/Windows/UserName/Certificate/InfoCard "/>  
                  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"  
            msmqEncryptionAlgorithm="RC4Stream/AES"  
            msmqProtectionLevel="None/Sign/EncryptAndSign"  
            msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
          </security>  
       <readerQuotas             maxArrayLength="Integer"            maxBytesPerRead="Integer"            maxDepth="Integer"             maxNameTableCharCount="Integer"                     maxStringContentLength="Integer" />   </binding></netMsmqBinding>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|`closeTimeout`|닫기 작업을 완료하기 위해 제공된 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다. 이 값은 <xref:System.TimeSpan.Zero>보다 크거나 같아야 합니다. 기본값은 00:01:00입니다.|  
|`customDeadLetterQueue`|응용 프로그램별 배달 못 한 편지 큐의 위치를 포함하는 URI입니다. 이 큐에는 만료되었거나 전송 또는 배달하지 못한 메시지가 보관됩니다.<br /><br /> 배달 못 한 편지 큐는 송신 응용 프로그램의 큐 관리자에서 관리하는 큐로, 배달하지 못한 만료된 메시지가 보관됩니다.<br /><br /> <xref:System.ServiceModel.MsmqBindingBase.CustomDeadLetterQueue%2A>로 지정된 URI는 net.msmq 체계를 사용해야 합니다.|  
|`deadLetterQueue`|배달 못 한 편지 큐가 있는 경우 큐의 형식을 지정하는 <xref:System.ServiceModel.MsmqBindingBase.DeadLetterQueue%2A> 값입니다.<br /><br /> 배달 못 한 편지 큐는 응용 프로그램에 배달하지 못한 메시지가 전송되는 위치입니다.<br /><br /> `exactlyOnce` 보증을 요구하는 메시지(`exactlyOnce` 특성이 `true`로 설정)의 경우 이 특성은 기본적으로 MSMQ의 시스템 전체 트랜잭션 배달 못 한 편지 큐로 설정됩니다.<br /><br /> 보증이 필요하지 않은 메시지의 경우 이 특성은 기본적으로 `null`로 설정됩니다.|  
|`durable`|큐의 메시지가 지속적인지 또는 일시적인지를 나타내는 부울 값입니다. 지속적 메시지는 큐 관리자가 중단되더라도 남아 있지만, 일시적 메시지는 손실됩니다. 응용 프로그램에서 더 낮은 대기 시간을 요구하며 어느 정도의 메시지 손실을 허용할 수 있다면 일시적 메시지가 유용합니다. `exactlyOnce` 특성을 `true`로 설정하면 메시지는 지속적이어야 합니다. 기본값은 `true`입니다.|  
|`exactlyOnce`|이 바인딩에서 처리하는 각 메시지가 한 번만 배달되는지 여부를 나타내는 부울 값입니다. 배달이 실패하면 발신자는 알림을 받습니다. `durable`이 `false`이면 이 특성은 무시되고 배달 보증 없이 메시지가 전송됩니다. 기본값은 `true`입니다. 자세한 내용은 <xref:System.ServiceModel.MsmqBindingBase.ExactlyOnce%2A>을 참조하세요.|  
|`maxBufferPoolSize`|이 바인딩의 최대 버퍼 풀 크기를 지정하는 정수입니다. 기본값은 8입니다.|  
|`maxReceivedMessageSize`|이 바인딩에 의해 처리되는 최대 메시지 크기(헤더 포함)(바이트)를 정의하는 양의 정수입니다. 이 한도를 초과하는 메시지를 보낸 사람은 SOAP 오류를 받습니다. 수신자는 메시지를 삭제하고 추적 로그에 이벤트 항목을 만듭니다. 기본값은 65536입니다. 이 메시지 크기 제한은 DoS(서비스 거부) 공격에 대한 노출을 막기 위한 것입니다.|  
|`maxRetryCycles`|포이즌 메시지 검색 기능에 사용되는 재시도 주기 수를 나타내는 정수입니다. 모든 주기의 모든 배달 시도가 실패할 경우 메시지는 포이즌 메시지가 됩니다. 기본값은 3입니다. 자세한 내용은 <xref:System.ServiceModel.MsmqBindingBase.MaxRetryCycles%2A>을 참조하세요.|  
|`name`|필수 특성입니다. 바인딩의 구성 이름을 포함하는 문자열입니다. 이 값은 바인딩의 ID로 사용되므로 고유해야 합니다. [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)]부터는 바인딩 및 동작에 이름이 필요하지 않습니다. 기본 구성 및 이름 없는 바인딩 및 동작에 대 한 자세한 내용은 참조 하세요. [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) 하 고 [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)합니다.|  
|`openTimeout`|열기 작업을 완료하기 위해 제공된 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다. 이 값은 <xref:System.TimeSpan.Zero>보다 크거나 같아야 합니다. 기본값은 00:01:00입니다.|  
|`QueueTransferProtocol`|이 바인딩에서 사용하는 대기 중인 통신 채널 전송을 지정하는 유효한 <xref:System.ServiceModel.QueueTransferProtocol> 값입니다. SRMP(SOAP Reliable Messaging Protocol) 사용 시 MSMQ는 Active Directory 주소 지정을 지원하지 않습니다. 따라서이 특성 설정 하지 해야 `Srmp` 또는 `Srmps` 때 합니다 `useActiveDirectory` 특성이로 설정 된 `true`합니다.|  
|`receiveErrorHandling`|포이즌 메시지 및 디스패치할 수 없는 메시지의 처리 방법을 지정하는 <xref:System.ServiceModel.ReceiveErrorHandling> 값입니다.|  
|`receiveRetryCount`|메시지를 재시도 큐로 전송하기 전에 큐 관리자가 메시지 전송을 시도하는 최대 횟수를 지정하는 정수입니다.|  
|`receiveTimeout`|받기 작업을 완료하기 위해 제공된 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다. 이 값은 <xref:System.TimeSpan.Zero>보다 크거나 같아야 합니다. 기본값은 00:10:00입니다.|  
|`retryCycleDelay`|전달하지 못한 메시지를 즉시 다시 전달하려고 시도할 때 재시도 주기 사이의 지연 시간을 지정하는 TimeSpan 값입니다. 실제 대기 시간이 더 길 수 있으므로 이 값은 최소 대기 시간만 정의합니다. 기본값은 00:10:00입니다. 자세한 내용은 <xref:System.ServiceModel.MsmqBindingBase.RetryCycleDelay%2A>을 참조하세요.|  
|`sendTimeout`|보내기 작업을 완료하기 위해 제공된 시간 간격을 지정하는 <xref:System.TimeSpan> 값입니다. 이 값은 <xref:System.TimeSpan.Zero>보다 크거나 같아야 합니다. 기본값은 00:01:00입니다.|  
|`timeToLive`|메시지가 만료되어 배달 못 한 큐에 추가되기 전에 메시지가 유효한 기간을 지정하는 TimeSpan 값입니다. 기본값은 1.00:00:00입니다.<br /><br /> 이 특성은 시간을 다투는 메시지가 수신 응용 프로그램에서 처리되기 전에 무효화되지 않도록 하기 위해 설정됩니다. 지정된 시간 간격 내에 수신 응용 프로그램에서 사용하지 않은 큐의 메시지는 만료된 것으로 간주됩니다. 만료된 메시지는 배달 못한 편지 큐라는 특수 큐로 보내집니다. 배달 못 한 편지 큐의 위치는 보증에 따라 `DeadLetterQueue` 특성으로 설정되거나 해당 기본값으로 설정됩니다.|  
|`usingActiveDirectory`|Active Directory를 사용하여 큐 주소를 변환해야 하는지 여부를 지정하는 부울 값입니다.<br /><br /> MSMQ 큐 주소는 경로 이름이나 직접 형식 이름으로 구성될 수 있습니다. 직접 형식 이름을 사용할 경우 MSMQ는 DNS, NetBIOS 또는 IP를 사용하여 컴퓨터 이름을 확인합니다. 경로 이름을 사용할 경우 MSMQ는 Active Directory를 사용하여 컴퓨터 이름을 확인합니다.<br /><br /> 기본적으로 Windows Communication Foundation (WCF) 전송 변환 직접 형식 이름에는 메시지 큐의 URI를 대기 합니다. `UseActiveDirectory` 속성을 true로 설정하면 대기 중 전송이 DNS, NetBIOS 또는 IP 대신 Active Directory를 사용하여 컴퓨터 이름을 확인하도록 응용 프로그램에서 지정할 수 있습니다.|  
|`useMsmqTracing`|이 바인딩이 처리하는 메시지를 추적할지 여부를 지정하는 부울 값입니다. 기본값은 `false`입니다. 추적 기능을 사용하면 메시지가 메시지 큐 컴퓨터에 들어가거나 나올 때마다 보고서 메시지가 만들어진 후 보고서 큐로 보내집니다.|  
|`useSourceJournal`|이 바인딩에서 처리하는 메시지의 복사본을 소스 업무 일지에 저장할지 여부를 지정하는 부울 값입니다. 기본값은 `false`입니다.<br /><br /> 대기 중 응용 프로그램에서 컴퓨터의 나가는 큐를 떠난 메시지의 레코드를 보존해야 할 경우 메시지를 업무 일지 큐에 복사할 수 있습니다. 메시지가 보내는 큐를 떠난 후 대상 컴퓨터에 수신되었다는 승인을 받으면 해당 메시지의 복사본이 보낸 컴퓨터의 시스템 업무 일지 큐에 보관됩니다.|  
  
### <a name="child-elements"></a>자식 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<readerQuotas>](https://msdn.microsoft.com/library/3e5e42ff-cef8-478f-bf14-034449239bfd)|이 바인딩으로 구성된 엔드포인트에서 처리할 수 있는 SOAP 메시지의 복잡성에 대한 제약 조건을 정의합니다. 이 요소는 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement> 형식입니다.|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|바인딩에 대한 보안 설정을 정의합니다. 이 요소는 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement> 형식입니다.|  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<bindings>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|이 요소는 표준 및 사용자 지정 바인딩의 컬렉션을 보유합니다.|  
  
## <a name="remarks"></a>설명  
 `netMsmqBinding` 바인딩은 MSMQ(Microsoft Message Queuing)를 전송으로 활용하면서 큐에 대한 지원을 제공하며, 느슨하게 결합된 응용 프로그램, 실패 격리, 로드 조정 및 연결이 끊긴 작업을 지원할 수 있도록 합니다. 이러한 기능 설명은 참조 하세요 [WCF의 큐](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)합니다.  
  
## <a name="example"></a>예제  
  
```xml  
<configuration>  
<system.ServiceModel>  
    <bindings>  
           <netMsmqBinding>  
                <binding   
                         closeTimeout="00:00:10"   
                         openTimeout="00:00:20"   
                         receiveTimeout="00:00:30"  
                         sendTimeout="00:00:40"  
                         deadLetterQueue="net.msmq://localhost/blah"   
                         durable="true"   
                         exactlyOnce="true"   
                         maxReceivedMessageSize="1000"  
                         maxRetries="11"  
                         maxRetryCycles="12"   
                         poisonMessageHandling="Disabled"   
                         rejectAfterLastRetry="false"   
                         retryCycleDelay="00:05:55"   
                         timeToLive="00:11:11"   
                         sourceJournal="true"  
                         useMsmqTracing="true"  
                         useActiveDirectory="true">  
                         <security>  
                             <message clientCredentialType="Windows" />  
                         </security>  
            </netMsmqBinding>  
    </bindings>  
</system.ServiceModel>  
</configuration>  
```  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.ServiceModel.NetMsmqBinding>  
 <xref:System.ServiceModel.Configuration.NetMsmqBindingElement>  
 [\<binding>](../../../../../docs/framework/misc/binding.md)  
 [바인딩](../../../../../docs/framework/wcf/bindings.md)  
 [시스템 제공 바인딩 구성](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [바인딩을 사용 하 여 Windows Communication Foundation 서비스 및 클라이언트 구성](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [WCF의 큐](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
