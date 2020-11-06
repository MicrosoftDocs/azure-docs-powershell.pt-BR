---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430934"
---
# <span data-ttu-id="ffc57-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ffc57-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="ffc57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffc57-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc57-103">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="ffc57-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffc57-104">SYNTAX</span></span>

### <span data-ttu-id="ffc57-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffc57-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc57-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc57-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc57-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc57-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc57-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffc57-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc57-109">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="ffc57-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="ffc57-110">Isso pode ser usado para substituir as marcas de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="ffc57-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="ffc57-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffc57-111">EXAMPLES</span></span>

### <span data-ttu-id="ffc57-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ffc57-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="ffc57-113">Define as propriedades do tópico da grade de eventos \` tópico1 \` no grupo de MyResourceGroupName de recursos \` \` para substituir as marcas por "departamento" e "ambiente" especificado.</span><span class="sxs-lookup"><span data-stu-id="ffc57-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="ffc57-114">OS</span><span class="sxs-lookup"><span data-stu-id="ffc57-114">PARAMETERS</span></span>

### <span data-ttu-id="ffc57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc57-115">-DefaultProfile</span></span>
<span data-ttu-id="ffc57-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ffc57-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffc57-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc57-117">-InputObject</span></span>
<span data-ttu-id="ffc57-118">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ffc57-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ffc57-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffc57-119">-Name</span></span>
<span data-ttu-id="ffc57-120">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ffc57-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ffc57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc57-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffc57-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffc57-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ffc57-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc57-123">-ResourceId</span></span>
<span data-ttu-id="ffc57-124">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="ffc57-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="ffc57-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="ffc57-125">-Tag</span></span>
<span data-ttu-id="ffc57-126">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffc57-126">Hashtables which represents resource Tag.</span></span>

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc57-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffc57-127">-Confirm</span></span>
<span data-ttu-id="ffc57-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffc57-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc57-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc57-129">-WhatIf</span></span>
<span data-ttu-id="ffc57-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffc57-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc57-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffc57-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc57-132">CommonParameters</span></span>
<span data-ttu-id="ffc57-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc57-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc57-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc57-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffc57-135">INPUTS</span></span>

### <span data-ttu-id="ffc57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ffc57-136">System.String</span></span>

### <span data-ttu-id="ffc57-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ffc57-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="ffc57-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffc57-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ffc57-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffc57-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ffc57-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffc57-140">OUTPUTS</span></span>

### <span data-ttu-id="ffc57-141">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ffc57-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ffc57-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffc57-142">NOTES</span></span>

## <span data-ttu-id="ffc57-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffc57-143">RELATED LINKS</span></span>