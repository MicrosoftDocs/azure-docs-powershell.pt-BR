---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441101"
---
# <span data-ttu-id="6d003-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="6d003-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="6d003-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d003-102">SYNOPSIS</span></span>
<span data-ttu-id="6d003-103">Defina as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="6d003-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d003-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d003-104">SYNTAX</span></span>

### <span data-ttu-id="6d003-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d003-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d003-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d003-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d003-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d003-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d003-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d003-108">DESCRIPTION</span></span>
<span data-ttu-id="6d003-109">Defina as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="6d003-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="6d003-110">Isso pode ser usado para substituir as marcas de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="6d003-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="6d003-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d003-111">EXAMPLES</span></span>

### <span data-ttu-id="6d003-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d003-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="6d003-113">Define as propriedades do tópico da grade de eventos \` tópico1 \` no grupo de MyResourceGroupName de recursos \` \` para substituir as marcas por "departamento" e "ambiente" especificado.</span><span class="sxs-lookup"><span data-stu-id="6d003-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="6d003-114">OS</span><span class="sxs-lookup"><span data-stu-id="6d003-114">PARAMETERS</span></span>

### <span data-ttu-id="6d003-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d003-115">-InputObject</span></span>
<span data-ttu-id="6d003-116">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6d003-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6d003-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d003-117">-Name</span></span>
<span data-ttu-id="6d003-118">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="6d003-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="6d003-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d003-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d003-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d003-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="6d003-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d003-121">-ResourceId</span></span>
<span data-ttu-id="6d003-122">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d003-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="6d003-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="6d003-123">-Tag</span></span>
<span data-ttu-id="6d003-124">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d003-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="6d003-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d003-125">-Confirm</span></span>
<span data-ttu-id="6d003-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d003-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d003-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d003-127">-WhatIf</span></span>
<span data-ttu-id="6d003-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d003-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d003-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d003-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d003-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d003-130">-DefaultProfile</span></span>
<span data-ttu-id="6d003-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d003-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d003-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d003-132">CommonParameters</span></span>
<span data-ttu-id="6d003-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d003-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d003-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d003-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d003-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d003-135">INPUTS</span></span>

### <span data-ttu-id="6d003-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6d003-136">System.String</span></span>
<span data-ttu-id="6d003-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d003-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6d003-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d003-138">OUTPUTS</span></span>

### <span data-ttu-id="6d003-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="6d003-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="6d003-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d003-140">NOTES</span></span>

## <span data-ttu-id="6d003-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d003-141">RELATED LINKS</span></span>

