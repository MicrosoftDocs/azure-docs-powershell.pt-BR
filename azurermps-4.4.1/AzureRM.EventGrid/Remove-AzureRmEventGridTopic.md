---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610802"
---
# <span data-ttu-id="7e97c-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7e97c-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="7e97c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e97c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e97c-103">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e97c-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e97c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e97c-104">SYNTAX</span></span>

### <span data-ttu-id="7e97c-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e97c-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e97c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e97c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e97c-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e97c-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e97c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e97c-108">DESCRIPTION</span></span>
<span data-ttu-id="7e97c-109">Remove um tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e97c-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7e97c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e97c-110">EXAMPLES</span></span>

### <span data-ttu-id="7e97c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e97c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="7e97c-112">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e97c-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7e97c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7e97c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="7e97c-114">Remove o tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e97c-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7e97c-115">OS</span><span class="sxs-lookup"><span data-stu-id="7e97c-115">PARAMETERS</span></span>

### <span data-ttu-id="7e97c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e97c-116">-InputObject</span></span>
<span data-ttu-id="7e97c-117">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7e97c-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7e97c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e97c-118">-Name</span></span>
<span data-ttu-id="7e97c-119">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7e97c-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="7e97c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e97c-120">-PassThru</span></span>
<span data-ttu-id="7e97c-121">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="7e97c-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7e97c-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7e97c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e97c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e97c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e97c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e97c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e97c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e97c-125">-ResourceId</span></span>
<span data-ttu-id="7e97c-126">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e97c-126">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="7e97c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e97c-127">-Confirm</span></span>
<span data-ttu-id="7e97c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e97c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e97c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e97c-129">-WhatIf</span></span>
<span data-ttu-id="7e97c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e97c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e97c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e97c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e97c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e97c-132">-DefaultProfile</span></span>
<span data-ttu-id="7e97c-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e97c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e97c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e97c-134">CommonParameters</span></span>
<span data-ttu-id="7e97c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e97c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e97c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e97c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e97c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e97c-137">INPUTS</span></span>

### <span data-ttu-id="7e97c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7e97c-138">System.String</span></span>
<span data-ttu-id="7e97c-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e97c-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7e97c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e97c-140">OUTPUTS</span></span>

### <span data-ttu-id="7e97c-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="7e97c-141">System.Object</span></span>

## <span data-ttu-id="7e97c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e97c-142">NOTES</span></span>

## <span data-ttu-id="7e97c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e97c-143">RELATED LINKS</span></span>

