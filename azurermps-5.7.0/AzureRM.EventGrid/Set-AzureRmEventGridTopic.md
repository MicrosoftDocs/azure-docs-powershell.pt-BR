---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429800"
---
# <span data-ttu-id="84b18-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="84b18-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="84b18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84b18-102">SYNOPSIS</span></span>
<span data-ttu-id="84b18-103">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="84b18-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84b18-104">SYNTAX</span></span>

### <span data-ttu-id="84b18-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="84b18-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b18-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="84b18-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b18-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84b18-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b18-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84b18-108">DESCRIPTION</span></span>
<span data-ttu-id="84b18-109">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="84b18-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="84b18-110">Isso pode ser usado para substituir as marcas de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="84b18-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="84b18-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84b18-111">EXAMPLES</span></span>

### <span data-ttu-id="84b18-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84b18-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="84b18-113">Define as propriedades do tópico da grade de eventos \` tópico1 \` no grupo de MyResourceGroupName de recursos \` \` para substituir as marcas por "departamento" e "ambiente" especificado.</span><span class="sxs-lookup"><span data-stu-id="84b18-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="84b18-114">OS</span><span class="sxs-lookup"><span data-stu-id="84b18-114">PARAMETERS</span></span>

### <span data-ttu-id="84b18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b18-115">-DefaultProfile</span></span>
<span data-ttu-id="84b18-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="84b18-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b18-117">-InputObject</span></span>
<span data-ttu-id="84b18-118">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="84b18-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="84b18-119">-Name</span></span>
<span data-ttu-id="84b18-120">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="84b18-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b18-121">-ResourceGroupName</span></span>
<span data-ttu-id="84b18-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84b18-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84b18-123">-ResourceId</span></span>
<span data-ttu-id="84b18-124">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="84b18-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="84b18-125">-Tag</span></span>
<span data-ttu-id="84b18-126">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="84b18-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84b18-127">-Confirm</span></span>
<span data-ttu-id="84b18-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b18-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b18-129">-WhatIf</span></span>
<span data-ttu-id="84b18-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84b18-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b18-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84b18-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b18-132">CommonParameters</span></span>
<span data-ttu-id="84b18-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b18-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b18-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b18-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84b18-135">INPUTS</span></span>

### <span data-ttu-id="84b18-136">System. String</span><span class="sxs-lookup"><span data-stu-id="84b18-136">System.String</span></span>
<span data-ttu-id="84b18-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84b18-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84b18-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84b18-138">OUTPUTS</span></span>

### <span data-ttu-id="84b18-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="84b18-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="84b18-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84b18-140">NOTES</span></span>

## <span data-ttu-id="84b18-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84b18-141">RELATED LINKS</span></span>

