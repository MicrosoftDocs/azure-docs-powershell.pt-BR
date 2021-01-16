---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259613"
---
# <span data-ttu-id="8ef36-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8ef36-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="8ef36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ef36-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef36-103">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef36-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="8ef36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ef36-104">SYNTAX</span></span>

### <span data-ttu-id="8ef36-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ef36-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef36-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef36-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef36-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef36-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ef36-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ef36-108">DESCRIPTION</span></span>
<span data-ttu-id="8ef36-109">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef36-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="8ef36-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ef36-110">EXAMPLES</span></span>

### <span data-ttu-id="8ef36-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ef36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8ef36-112">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8ef36-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8ef36-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8ef36-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="8ef36-114">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8ef36-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8ef36-115">OS</span><span class="sxs-lookup"><span data-stu-id="8ef36-115">PARAMETERS</span></span>

### <span data-ttu-id="8ef36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef36-116">-DefaultProfile</span></span>
<span data-ttu-id="8ef36-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8ef36-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ef36-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ef36-118">-InputObject</span></span>
<span data-ttu-id="8ef36-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8ef36-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8ef36-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ef36-120">-Name</span></span>
<span data-ttu-id="8ef36-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8ef36-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="8ef36-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ef36-122">-PassThru</span></span>
<span data-ttu-id="8ef36-123">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="8ef36-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8ef36-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8ef36-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ef36-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef36-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ef36-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ef36-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ef36-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef36-127">-ResourceId</span></span>
<span data-ttu-id="8ef36-128">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ef36-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="8ef36-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ef36-129">-Confirm</span></span>
<span data-ttu-id="8ef36-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ef36-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef36-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef36-131">-WhatIf</span></span>
<span data-ttu-id="8ef36-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ef36-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ef36-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ef36-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef36-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef36-134">CommonParameters</span></span>
<span data-ttu-id="8ef36-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef36-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef36-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef36-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef36-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ef36-137">INPUTS</span></span>

### <span data-ttu-id="8ef36-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ef36-138">System.String</span></span>

### <span data-ttu-id="8ef36-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8ef36-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8ef36-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ef36-140">OUTPUTS</span></span>

### <span data-ttu-id="8ef36-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ef36-141">System.Boolean</span></span>

## <span data-ttu-id="8ef36-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ef36-142">NOTES</span></span>

## <span data-ttu-id="8ef36-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ef36-143">RELATED LINKS</span></span>
