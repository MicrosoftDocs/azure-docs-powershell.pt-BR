---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118665"
---
# <span data-ttu-id="fc96f-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fc96f-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="fc96f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc96f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc96f-103">Atualiza a descrição de uma fila de Service Bus no namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="fc96f-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc96f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc96f-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc96f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc96f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc96f-106">O cmdlet **Set-AzServiceBusQueue** atualiza a descrição da fila de Barra de Serviços no namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="fc96f-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc96f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc96f-107">EXAMPLES</span></span>

### <span data-ttu-id="fc96f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc96f-108">Example 1</span></span>
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

<span data-ttu-id="fc96f-109">Atualiza a fila especificada com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="fc96f-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="fc96f-110">Este exemplo atualiza a **propriedade DeadLetteringOnMessageExpiration** como verdadeira **e a SupportOrdering** como **verdadeira.** </span><span class="sxs-lookup"><span data-stu-id="fc96f-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="fc96f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc96f-111">PARAMETERS</span></span>

### <span data-ttu-id="fc96f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc96f-112">-DefaultProfile</span></span>
<span data-ttu-id="fc96f-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fc96f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc96f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc96f-114">-InputObject</span></span>
<span data-ttu-id="fc96f-115">Definição de ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fc96f-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="fc96f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc96f-116">-Name</span></span>
<span data-ttu-id="fc96f-117">Nome da Fila.</span><span class="sxs-lookup"><span data-stu-id="fc96f-117">Queue Name.</span></span>

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

### <span data-ttu-id="fc96f-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc96f-118">-Namespace</span></span>
<span data-ttu-id="fc96f-119">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="fc96f-119">Namespace Name.</span></span>

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

### <span data-ttu-id="fc96f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc96f-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc96f-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fc96f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fc96f-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fc96f-122">-Confirm</span></span>
<span data-ttu-id="fc96f-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc96f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc96f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc96f-124">-WhatIf</span></span>
<span data-ttu-id="fc96f-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fc96f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc96f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc96f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc96f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc96f-127">CommonParameters</span></span>
<span data-ttu-id="fc96f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc96f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc96f-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc96f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc96f-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="fc96f-130">INPUTS</span></span>

### <span data-ttu-id="fc96f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fc96f-131">System.String</span></span>

### <span data-ttu-id="fc96f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fc96f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fc96f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="fc96f-133">OUTPUTS</span></span>

### <span data-ttu-id="fc96f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fc96f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fc96f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="fc96f-135">NOTES</span></span>

## <span data-ttu-id="fc96f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc96f-136">RELATED LINKS</span></span>
