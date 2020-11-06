---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: d853d5d4659e41c9696ab87c3f9ab8b58c240044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430935"
---
# <span data-ttu-id="1ac2d-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="1ac2d-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="1ac2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ac2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac2d-103">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ac2d-104">SYNTAX</span></span>

### <span data-ttu-id="1ac2d-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ac2d-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac2d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ac2d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac2d-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ac2d-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac2d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ac2d-108">DESCRIPTION</span></span>
<span data-ttu-id="1ac2d-109">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="1ac2d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ac2d-110">EXAMPLES</span></span>

### <span data-ttu-id="1ac2d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ac2d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="1ac2d-112">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="1ac2d-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1ac2d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1ac2d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="1ac2d-114">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="1ac2d-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1ac2d-115">OS</span><span class="sxs-lookup"><span data-stu-id="1ac2d-115">PARAMETERS</span></span>

### <span data-ttu-id="1ac2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac2d-116">-DefaultProfile</span></span>
<span data-ttu-id="1ac2d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1ac2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ac2d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ac2d-118">-InputObject</span></span>
<span data-ttu-id="1ac2d-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="1ac2d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ac2d-120">-Name</span></span>
<span data-ttu-id="1ac2d-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="1ac2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ac2d-122">-PassThru</span></span>
<span data-ttu-id="1ac2d-123">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="1ac2d-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ac2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ac2d-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ac2d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ac2d-127">-ResourceId</span></span>
<span data-ttu-id="1ac2d-128">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="1ac2d-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="1ac2d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ac2d-129">-Confirm</span></span>
<span data-ttu-id="1ac2d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac2d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac2d-131">-WhatIf</span></span>
<span data-ttu-id="1ac2d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac2d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac2d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac2d-134">CommonParameters</span></span>
<span data-ttu-id="1ac2d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac2d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac2d-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac2d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac2d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ac2d-137">INPUTS</span></span>

### <span data-ttu-id="1ac2d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1ac2d-138">System.String</span></span>

### <span data-ttu-id="1ac2d-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1ac2d-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="1ac2d-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ac2d-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1ac2d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ac2d-141">OUTPUTS</span></span>

### <span data-ttu-id="1ac2d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ac2d-142">System.Boolean</span></span>

## <span data-ttu-id="1ac2d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ac2d-143">NOTES</span></span>

## <span data-ttu-id="1ac2d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ac2d-144">RELATED LINKS</span></span>
