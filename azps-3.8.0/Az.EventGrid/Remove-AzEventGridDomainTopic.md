---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 2ca0c66490a95646ec3caa01b394b6210d472370
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941432"
---
# <span data-ttu-id="34344-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="34344-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="34344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34344-102">SYNOPSIS</span></span>
<span data-ttu-id="34344-103">Remove um tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="34344-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="34344-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34344-104">SYNTAX</span></span>

### <span data-ttu-id="34344-105">DomainTopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="34344-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34344-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="34344-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34344-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34344-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34344-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34344-108">DESCRIPTION</span></span>
<span data-ttu-id="34344-109">Remove um tópico de domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="34344-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="34344-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34344-110">EXAMPLES</span></span>

### <span data-ttu-id="34344-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34344-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="34344-112">Remove o tópico de domínio da grade de eventos \` tópico1 \` em Domain \` domain1 \` no grupo de MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="34344-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="34344-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="34344-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="34344-114">Remove o tópico de domínio da grade de eventos \` tópico1 \` em Domain \` domain1 \` no grupo de MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="34344-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="34344-115">OS</span><span class="sxs-lookup"><span data-stu-id="34344-115">PARAMETERS</span></span>

### <span data-ttu-id="34344-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34344-116">-DefaultProfile</span></span>
<span data-ttu-id="34344-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34344-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34344-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="34344-118">-DomainName</span></span>
<span data-ttu-id="34344-119">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="34344-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34344-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34344-120">-InputObject</span></span>
<span data-ttu-id="34344-121">Objeto de tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="34344-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34344-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="34344-122">-Name</span></span>
<span data-ttu-id="34344-123">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="34344-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34344-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34344-124">-PassThru</span></span>
<span data-ttu-id="34344-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="34344-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34344-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34344-126">-ResourceGroupName</span></span>
<span data-ttu-id="34344-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34344-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34344-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34344-128">-ResourceId</span></span>
<span data-ttu-id="34344-129">Identificador de recurso que representa o tópico do domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="34344-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34344-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34344-130">-Confirm</span></span>
<span data-ttu-id="34344-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34344-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34344-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34344-132">-WhatIf</span></span>
<span data-ttu-id="34344-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34344-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34344-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34344-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34344-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34344-135">CommonParameters</span></span>
<span data-ttu-id="34344-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34344-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34344-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34344-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34344-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34344-138">INPUTS</span></span>

### <span data-ttu-id="34344-139">System. String</span><span class="sxs-lookup"><span data-stu-id="34344-139">System.String</span></span>

### <span data-ttu-id="34344-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="34344-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="34344-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34344-141">OUTPUTS</span></span>

### <span data-ttu-id="34344-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34344-142">System.Boolean</span></span>

## <span data-ttu-id="34344-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34344-143">NOTES</span></span>

## <span data-ttu-id="34344-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34344-144">RELATED LINKS</span></span>
