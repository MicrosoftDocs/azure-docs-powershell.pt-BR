---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427787"
---
# Get-AzureRmServiceBusTopic

## Sinopse
Retorna uma descrição para o tópico de barramento de serviço especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmServiceBusTopic** retorna uma descrição de tópico para o namespace de barramento de serviço especificado.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

Retorna a descrição do tópico especificado para o namespace de barramento de serviço fornecido.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do tópico.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Nome do namespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### -Resource
 System. String
 

### -NamespaceName
 System. String
 

### -Topicname
 System. String

## EXIBE

### Microsoft. Azure. Commands. ServiceBus. Models. Topicattributes
Nome: local do SB-Topic_exampl1: identificação do oeste dos EUA:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 tipo: Microsoft. ServiceBus/tópico AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: FilteringMessagesBeforePublishing IsAnonymousAccessible: false MaxSizeInMegabytes: false Isexpress: false RequiresDuplicateDetection: sizeInBytes: false SubscriptionCount: 0 status: active SupportOrdering: 1 UpdatedAt:: 1/20/2017 3:16:43 AM 16384

## INFORMA

## LINKS RELACIONADOS

