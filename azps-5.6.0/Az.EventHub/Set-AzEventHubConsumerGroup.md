---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: 844b8a08a54409e4eb10cde9f063b65cb5587bae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892795"
---
# <span data-ttu-id="92c3c-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="92c3c-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="92c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="92c3c-103">Atualiza o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="92c3c-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="92c3c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92c3c-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92c3c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="92c3c-106">O cmdlet Set-AzEventHubConsumerGroup atualiza o grupo de consumidores de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="92c3c-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="92c3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="92c3c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92c3c-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="92c3c-109">Define os metadados do usuário do grupo de consumidores \` MyConsumerGroupName \` como "Testing".</span><span class="sxs-lookup"><span data-stu-id="92c3c-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="92c3c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="92c3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c3c-111">-DefaultProfile</span></span>
<span data-ttu-id="92c3c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92c3c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92c3c-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="92c3c-113">-EventHub</span></span>
<span data-ttu-id="92c3c-114">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="92c3c-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="92c3c-115">-Name</span></span>
<span data-ttu-id="92c3c-116">Nome do ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="92c3c-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="92c3c-117">-Namespace</span></span>
<span data-ttu-id="92c3c-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="92c3c-118">Namespace Name</span></span>

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

### <span data-ttu-id="92c3c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c3c-119">-ResourceGroupName</span></span>
<span data-ttu-id="92c3c-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="92c3c-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="92c3c-121">-UserMetadata</span></span>
<span data-ttu-id="92c3c-122">Metadados do Usuário para ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="92c3c-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92c3c-123">-Confirm</span></span>
<span data-ttu-id="92c3c-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c3c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c3c-125">-WhatIf</span></span>
<span data-ttu-id="92c3c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92c3c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c3c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92c3c-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c3c-128">CommonParameters</span></span>
<span data-ttu-id="92c3c-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c3c-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c3c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c3c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92c3c-131">INPUTS</span></span>

### <span data-ttu-id="92c3c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="92c3c-132">System.String</span></span>

## <span data-ttu-id="92c3c-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92c3c-133">OUTPUTS</span></span>

### <span data-ttu-id="92c3c-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="92c3c-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="92c3c-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="92c3c-135">NOTES</span></span>

## <span data-ttu-id="92c3c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92c3c-136">RELATED LINKS</span></span>
