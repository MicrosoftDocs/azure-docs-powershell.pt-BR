---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440553"
---
# <span data-ttu-id="2d4dd-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2d4dd-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="2d4dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4dd-103">Atualiza a descrição de uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d4dd-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d4dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4dd-106">O cmdlet **set-AzureRmServiceBusQueue** atualiza a descrição da fila de barramento do serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2d4dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4dd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d4dd-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="2d4dd-109">Atualiza a fila especificada com uma nova descrição no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="2d4dd-110">Este exemplo atualiza a propriedade **DeadLetteringOnMessageExpiration** para **true** e **SupportOrdering** para **true**.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="2d4dd-111">OS</span><span class="sxs-lookup"><span data-stu-id="2d4dd-111">PARAMETERS</span></span>

### <span data-ttu-id="2d4dd-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d4dd-112">-Confirm</span></span>
<span data-ttu-id="2d4dd-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4dd-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4dd-114">-WhatIf</span></span>
<span data-ttu-id="2d4dd-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4dd-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4dd-117">-DefaultProfile</span></span>
<span data-ttu-id="2d4dd-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d4dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d4dd-119">-InputObject</span></span>
<span data-ttu-id="2d4dd-120">Definição do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4dd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d4dd-121">-Name</span></span>
<span data-ttu-id="2d4dd-122">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-122">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4dd-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2d4dd-123">-Namespace</span></span>
<span data-ttu-id="2d4dd-124">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-124">Namespace Name.</span></span>

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

### <span data-ttu-id="2d4dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d4dd-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2d4dd-126">The name of the resource group</span></span>

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

### <span data-ttu-id="2d4dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4dd-127">CommonParameters</span></span>
<span data-ttu-id="2d4dd-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4dd-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4dd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4dd-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d4dd-130">INPUTS</span></span>

### <span data-ttu-id="2d4dd-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="2d4dd-131">-ResourceGroup</span></span>
 <span data-ttu-id="2d4dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d4dd-132">System.String</span></span>

### <span data-ttu-id="2d4dd-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2d4dd-133">-NamespaceName</span></span>
 <span data-ttu-id="2d4dd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d4dd-134">System.String</span></span>

### <span data-ttu-id="2d4dd-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="2d4dd-135">-QueueName</span></span>
 <span data-ttu-id="2d4dd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2d4dd-136">System.String</span></span>

### <span data-ttu-id="2d4dd-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="2d4dd-137">-QueueObj</span></span>
 <span data-ttu-id="2d4dd-138">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="2d4dd-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="2d4dd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d4dd-139">OUTPUTS</span></span>

### <span data-ttu-id="2d4dd-140">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="2d4dd-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="2d4dd-141">Nome: local do SB-Queue_exampl1: West US LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:34 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails RequiresDuplicateDetection: false RequiresSession: false SizeInBytes: status: active SupportOrdering: false UpdatedAt: false PM 1/20/2017 6:16:18</span><span class="sxs-lookup"><span data-stu-id="2d4dd-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="2d4dd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d4dd-142">NOTES</span></span>

## <span data-ttu-id="2d4dd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d4dd-143">RELATED LINKS</span></span>

