---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c02c596b1b1eecb8654b07a2392d2336c0b0215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602446"
---
# <span data-ttu-id="c12b9-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c12b9-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="c12b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c12b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c12b9-103">Atualiza a descrição de uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c12b9-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c12b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c12b9-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c12b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c12b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c12b9-106">O cmdlet **set-AzureRmServiceBusQueue** atualiza a descrição da fila de barramento do serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c12b9-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c12b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c12b9-107">EXAMPLES</span></span>

### <span data-ttu-id="c12b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c12b9-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

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

<span data-ttu-id="c12b9-109">Atualiza a fila especificada com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="c12b9-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="c12b9-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **SupportOrdering** para **true**.</span><span class="sxs-lookup"><span data-stu-id="c12b9-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="c12b9-111">OS</span><span class="sxs-lookup"><span data-stu-id="c12b9-111">PARAMETERS</span></span>

### <span data-ttu-id="c12b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12b9-112">-DefaultProfile</span></span>
<span data-ttu-id="c12b9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c12b9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c12b9-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c12b9-114">-InputObject</span></span>
<span data-ttu-id="c12b9-115">Definição do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="c12b9-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="c12b9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c12b9-116">-Name</span></span>
<span data-ttu-id="c12b9-117">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="c12b9-117">Queue Name.</span></span>

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

### <span data-ttu-id="c12b9-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c12b9-118">-Namespace</span></span>
<span data-ttu-id="c12b9-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c12b9-119">Namespace Name.</span></span>

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

### <span data-ttu-id="c12b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c12b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="c12b9-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c12b9-121">The name of the resource group</span></span>

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

### <span data-ttu-id="c12b9-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c12b9-122">-Confirm</span></span>
<span data-ttu-id="c12b9-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c12b9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12b9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12b9-124">-WhatIf</span></span>
<span data-ttu-id="c12b9-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c12b9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12b9-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c12b9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12b9-127">CommonParameters</span></span>
<span data-ttu-id="c12b9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12b9-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c12b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12b9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c12b9-130">INPUTS</span></span>

### <span data-ttu-id="c12b9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c12b9-131">System.String</span></span>

### <span data-ttu-id="c12b9-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c12b9-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c12b9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c12b9-133">OUTPUTS</span></span>

### <span data-ttu-id="c12b9-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="c12b9-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="c12b9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c12b9-135">NOTES</span></span>

## <span data-ttu-id="c12b9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c12b9-136">RELATED LINKS</span></span>
