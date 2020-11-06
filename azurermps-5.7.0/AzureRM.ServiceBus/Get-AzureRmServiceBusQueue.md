---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428763"
---
# Get-AzureRmServiceBusQueue

## Sinopse
Retorna uma descrição para a fila de barramento de serviço especificada.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmServiceBusQueue** retorna uma descrição da fila de barramento de serviço especificada.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

Retorna a descrição da fila.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome da fila.

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Nome do namespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
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
 

### -QueueName
 System. String 

## EXIBE

### Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes

## INFORMA

## LINKS RELACIONADOS

