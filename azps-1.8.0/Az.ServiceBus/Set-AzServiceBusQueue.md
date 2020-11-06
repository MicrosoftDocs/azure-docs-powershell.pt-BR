---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 4206e29ad56e1d7b48b9d87a66b8a85960c4707e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599141"
---
# <span data-ttu-id="40daf-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="40daf-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="40daf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40daf-102">SYNOPSIS</span></span>
<span data-ttu-id="40daf-103">Atualiza a descrição de uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="40daf-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="40daf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40daf-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40daf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40daf-105">DESCRIPTION</span></span>
<span data-ttu-id="40daf-106">O cmdlet **set-AzServiceBusQueue** atualiza a descrição da fila de barramento do serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="40daf-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="40daf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40daf-107">EXAMPLES</span></span>

### <span data-ttu-id="40daf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40daf-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="40daf-109">Atualiza a fila especificada com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="40daf-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="40daf-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **SupportOrdering** para **true**.</span><span class="sxs-lookup"><span data-stu-id="40daf-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="40daf-111">OS</span><span class="sxs-lookup"><span data-stu-id="40daf-111">PARAMETERS</span></span>

### <span data-ttu-id="40daf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40daf-112">-DefaultProfile</span></span>
<span data-ttu-id="40daf-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40daf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40daf-114">-InputObject</span></span>
<span data-ttu-id="40daf-115">Definição do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="40daf-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="40daf-116">-Name</span></span>
<span data-ttu-id="40daf-117">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="40daf-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40daf-118">-Namespace</span></span>
<span data-ttu-id="40daf-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="40daf-119">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40daf-120">-ResourceGroupName</span></span>
<span data-ttu-id="40daf-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="40daf-121">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40daf-122">-Confirm</span></span>
<span data-ttu-id="40daf-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40daf-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40daf-124">-WhatIf</span></span>
<span data-ttu-id="40daf-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40daf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40daf-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40daf-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40daf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40daf-127">CommonParameters</span></span>
<span data-ttu-id="40daf-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40daf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40daf-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40daf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40daf-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40daf-130">INPUTS</span></span>

### <span data-ttu-id="40daf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="40daf-131">System.String</span></span>

### <span data-ttu-id="40daf-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="40daf-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="40daf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40daf-133">OUTPUTS</span></span>

### <span data-ttu-id="40daf-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="40daf-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="40daf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40daf-135">NOTES</span></span>

## <span data-ttu-id="40daf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40daf-136">RELATED LINKS</span></span>
