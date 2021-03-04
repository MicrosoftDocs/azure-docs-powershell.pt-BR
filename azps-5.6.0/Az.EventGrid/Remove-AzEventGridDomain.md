---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886976"
---
# <span data-ttu-id="3a76b-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a76b-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="3a76b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a76b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a76b-103">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a76b-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3a76b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a76b-104">SYNTAX</span></span>

### <span data-ttu-id="3a76b-105">DomainNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a76b-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a76b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a76b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a76b-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a76b-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a76b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a76b-108">DESCRIPTION</span></span>
<span data-ttu-id="3a76b-109">Remove um domínio da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a76b-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3a76b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a76b-110">EXAMPLES</span></span>

### <span data-ttu-id="3a76b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a76b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="3a76b-112">Remove o Domínio de Domínio da Grade \` de Eventos1 \` no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3a76b-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3a76b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3a76b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="3a76b-114">Remove o Domínio de Domínio da Grade \` de Eventos1 \` no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3a76b-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3a76b-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a76b-115">PARAMETERS</span></span>

### <span data-ttu-id="3a76b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a76b-116">-DefaultProfile</span></span>
<span data-ttu-id="3a76b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a76b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a76b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a76b-118">-InputObject</span></span>
<span data-ttu-id="3a76b-119">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="3a76b-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a76b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3a76b-120">-Name</span></span>
<span data-ttu-id="3a76b-121">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3a76b-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a76b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a76b-122">-PassThru</span></span>
<span data-ttu-id="3a76b-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3a76b-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a76b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a76b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a76b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a76b-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a76b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a76b-126">-ResourceId</span></span>
<span data-ttu-id="3a76b-127">Identificador de Recurso que representa o Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="3a76b-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="3a76b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a76b-128">-Confirm</span></span>
<span data-ttu-id="3a76b-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a76b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a76b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a76b-130">-WhatIf</span></span>
<span data-ttu-id="3a76b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a76b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a76b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a76b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a76b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a76b-133">CommonParameters</span></span>
<span data-ttu-id="3a76b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a76b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a76b-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a76b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a76b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a76b-136">INPUTS</span></span>

### <span data-ttu-id="3a76b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3a76b-137">System.String</span></span>

### <span data-ttu-id="3a76b-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="3a76b-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="3a76b-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a76b-139">OUTPUTS</span></span>

### <span data-ttu-id="3a76b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a76b-140">System.Boolean</span></span>

## <span data-ttu-id="3a76b-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a76b-141">NOTES</span></span>

## <span data-ttu-id="3a76b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a76b-142">RELATED LINKS</span></span>
