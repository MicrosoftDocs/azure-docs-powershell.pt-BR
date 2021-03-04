---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 3960f73d115b881bdffab89c225a9321e19af067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890404"
---
# <span data-ttu-id="e7d63-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e7d63-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="e7d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d63-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d63-103">Remove um tópico de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d63-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e7d63-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7d63-104">SYNTAX</span></span>

### <span data-ttu-id="e7d63-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e7d63-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d63-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d63-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d63-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d63-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d63-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7d63-108">DESCRIPTION</span></span>
<span data-ttu-id="e7d63-109">Remove um tópico de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d63-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e7d63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7d63-110">EXAMPLES</span></span>

### <span data-ttu-id="e7d63-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7d63-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e7d63-112">Remove o tópico De grade de \` eventos1 \` no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e7d63-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e7d63-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e7d63-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="e7d63-114">Remove o tópico De grade de \` eventos1 \` no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e7d63-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e7d63-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7d63-115">PARAMETERS</span></span>

### <span data-ttu-id="e7d63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d63-116">-DefaultProfile</span></span>
<span data-ttu-id="e7d63-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e7d63-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7d63-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7d63-118">-InputObject</span></span>
<span data-ttu-id="e7d63-119">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="e7d63-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d63-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d63-120">-Name</span></span>
<span data-ttu-id="e7d63-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e7d63-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d63-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7d63-122">-PassThru</span></span>
<span data-ttu-id="e7d63-123">Retorna o status da operação Remover.</span><span class="sxs-lookup"><span data-stu-id="e7d63-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e7d63-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e7d63-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d63-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d63-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7d63-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e7d63-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d63-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7d63-127">-ResourceId</span></span>
<span data-ttu-id="e7d63-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="e7d63-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d63-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d63-129">-Confirm</span></span>
<span data-ttu-id="e7d63-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7d63-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d63-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d63-131">-WhatIf</span></span>
<span data-ttu-id="e7d63-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7d63-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d63-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7d63-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d63-134">CommonParameters</span></span>
<span data-ttu-id="e7d63-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d63-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7d63-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d63-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d63-137">INPUTS</span></span>

### <span data-ttu-id="e7d63-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d63-138">System.String</span></span>

### <span data-ttu-id="e7d63-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="e7d63-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e7d63-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7d63-140">OUTPUTS</span></span>

### <span data-ttu-id="e7d63-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7d63-141">System.Boolean</span></span>

## <span data-ttu-id="e7d63-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7d63-142">NOTES</span></span>

## <span data-ttu-id="e7d63-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7d63-143">RELATED LINKS</span></span>
