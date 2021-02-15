---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113836"
---
# <span data-ttu-id="eccb4-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="eccb4-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="eccb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eccb4-102">SYNOPSIS</span></span>
<span data-ttu-id="eccb4-103">Remove um Tópico de Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eccb4-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="eccb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eccb4-104">SYNTAX</span></span>

### <span data-ttu-id="eccb4-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eccb4-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eccb4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eccb4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eccb4-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eccb4-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eccb4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="eccb4-108">DESCRIPTION</span></span>
<span data-ttu-id="eccb4-109">Remove um Tópico de Grade do Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eccb4-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="eccb4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eccb4-110">EXAMPLES</span></span>

### <span data-ttu-id="eccb4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eccb4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="eccb4-112">Remove o tópico da Grade do \` Evento1 \` no grupo de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="eccb4-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="eccb4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eccb4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="eccb4-114">Remove o tópico da Grade do \` Evento1 \` no grupo de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="eccb4-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="eccb4-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eccb4-115">PARAMETERS</span></span>

### <span data-ttu-id="eccb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccb4-116">-DefaultProfile</span></span>
<span data-ttu-id="eccb4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="eccb4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eccb4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eccb4-118">-InputObject</span></span>
<span data-ttu-id="eccb4-119">Objeto De Tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="eccb4-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="eccb4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eccb4-120">-Name</span></span>
<span data-ttu-id="eccb4-121">Nome do tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="eccb4-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="eccb4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eccb4-122">-PassThru</span></span>
<span data-ttu-id="eccb4-123">Retorna o status da operação Remover.</span><span class="sxs-lookup"><span data-stu-id="eccb4-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="eccb4-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="eccb4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eccb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eccb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="eccb4-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eccb4-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="eccb4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eccb4-127">-ResourceId</span></span>
<span data-ttu-id="eccb4-128">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="eccb4-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="eccb4-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eccb4-129">-Confirm</span></span>
<span data-ttu-id="eccb4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eccb4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eccb4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eccb4-131">-WhatIf</span></span>
<span data-ttu-id="eccb4-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eccb4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eccb4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eccb4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eccb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccb4-134">CommonParameters</span></span>
<span data-ttu-id="eccb4-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eccb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccb4-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eccb4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccb4-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="eccb4-137">INPUTS</span></span>

### <span data-ttu-id="eccb4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="eccb4-138">System.String</span></span>

### <span data-ttu-id="eccb4-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="eccb4-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="eccb4-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="eccb4-140">OUTPUTS</span></span>

### <span data-ttu-id="eccb4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eccb4-141">System.Boolean</span></span>

## <span data-ttu-id="eccb4-142">Notas</span><span class="sxs-lookup"><span data-stu-id="eccb4-142">NOTES</span></span>

## <span data-ttu-id="eccb4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eccb4-143">RELATED LINKS</span></span>
