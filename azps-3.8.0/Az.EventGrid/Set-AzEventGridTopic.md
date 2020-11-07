---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940933"
---
# <span data-ttu-id="7e1b4-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7e1b4-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="7e1b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1b4-103">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="7e1b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e1b4-104">SYNTAX</span></span>

### <span data-ttu-id="7e1b4-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e1b4-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e1b4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e1b4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e1b4-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e1b4-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e1b4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e1b4-108">DESCRIPTION</span></span>
<span data-ttu-id="7e1b4-109">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="7e1b4-110">Isso pode ser usado para substituir as marcas de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="7e1b4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e1b4-111">EXAMPLES</span></span>

### <span data-ttu-id="7e1b4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e1b4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="7e1b4-113">Define as propriedades do tópico da grade de eventos \` tópico1 \` no grupo de MyResourceGroupName de recursos \` \` para substituir as marcas por "departamento" e "ambiente" especificado.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="7e1b4-114">OS</span><span class="sxs-lookup"><span data-stu-id="7e1b4-114">PARAMETERS</span></span>

### <span data-ttu-id="7e1b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1b4-115">-DefaultProfile</span></span>
<span data-ttu-id="7e1b4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7e1b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e1b4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e1b4-117">-InputObject</span></span>
<span data-ttu-id="7e1b4-118">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7e1b4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e1b4-119">-Name</span></span>
<span data-ttu-id="7e1b4-120">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="7e1b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e1b4-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e1b4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e1b4-123">-ResourceId</span></span>
<span data-ttu-id="7e1b4-124">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e1b4-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e1b4-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="7e1b4-125">-Tag</span></span>
<span data-ttu-id="7e1b4-126">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e1b4-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e1b4-127">-Confirm</span></span>
<span data-ttu-id="7e1b4-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e1b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e1b4-129">-WhatIf</span></span>
<span data-ttu-id="7e1b4-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e1b4-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e1b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1b4-132">CommonParameters</span></span>
<span data-ttu-id="7e1b4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1b4-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1b4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1b4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e1b4-135">INPUTS</span></span>

### <span data-ttu-id="7e1b4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7e1b4-136">System.String</span></span>

### <span data-ttu-id="7e1b4-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e1b4-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7e1b4-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e1b4-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e1b4-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e1b4-139">OUTPUTS</span></span>

### <span data-ttu-id="7e1b4-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e1b4-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7e1b4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e1b4-141">NOTES</span></span>

## <span data-ttu-id="7e1b4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e1b4-142">RELATED LINKS</span></span>
