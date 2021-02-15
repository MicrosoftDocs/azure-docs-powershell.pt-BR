---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113840"
---
# <span data-ttu-id="0efed-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="0efed-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="0efed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0efed-102">SYNOPSIS</span></span>
<span data-ttu-id="0efed-103">Regenera a chave de acesso compartilhado para um Tópico de Grade de Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0efed-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="0efed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0efed-104">SYNTAX</span></span>

### <span data-ttu-id="0efed-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0efed-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efed-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efed-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efed-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efed-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efed-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0efed-108">DESCRIPTION</span></span>
<span data-ttu-id="0efed-109">Regenera a chave de acesso compartilhado para um Tópico de Grade de Evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0efed-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="0efed-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0efed-110">EXAMPLES</span></span>

### <span data-ttu-id="0efed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0efed-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="0efed-112">Regenerar a chave correspondente à chave1'\ do tópico da Grade do Evento1 no grupo de recursos \' \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0efed-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0efed-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0efed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="0efed-114">Regenerar a chave correspondente à chave1'\ do tópico da Grade do Evento1 no grupo de recursos \' \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0efed-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0efed-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0efed-115">PARAMETERS</span></span>

### <span data-ttu-id="0efed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efed-116">-DefaultProfile</span></span>
<span data-ttu-id="0efed-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0efed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0efed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efed-118">-InputObject</span></span>
<span data-ttu-id="0efed-119">Objeto De Tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0efed-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0efed-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0efed-120">-KeyName</span></span>
<span data-ttu-id="0efed-121">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="0efed-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0efed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efed-122">-ResourceGroupName</span></span>
<span data-ttu-id="0efed-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0efed-123">Resource group name.</span></span>

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

### <span data-ttu-id="0efed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0efed-124">-ResourceId</span></span>
<span data-ttu-id="0efed-125">Identificador de Recurso representando o Tópico da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="0efed-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="0efed-126">-Nomedo Tópico</span><span class="sxs-lookup"><span data-stu-id="0efed-126">-TopicName</span></span>
<span data-ttu-id="0efed-127">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="0efed-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0efed-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0efed-128">-Confirm</span></span>
<span data-ttu-id="0efed-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efed-130">-WhatIf</span></span>
<span data-ttu-id="0efed-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0efed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efed-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0efed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efed-133">CommonParameters</span></span>
<span data-ttu-id="0efed-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efed-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0efed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efed-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="0efed-136">INPUTS</span></span>

### <span data-ttu-id="0efed-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0efed-137">System.String</span></span>

### <span data-ttu-id="0efed-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="0efed-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0efed-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="0efed-139">OUTPUTS</span></span>

### <span data-ttu-id="0efed-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0efed-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="0efed-141">Notas</span><span class="sxs-lookup"><span data-stu-id="0efed-141">NOTES</span></span>

## <span data-ttu-id="0efed-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0efed-142">RELATED LINKS</span></span>
