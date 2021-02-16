---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117671"
---
# <span data-ttu-id="3bec7-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3bec7-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="3bec7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bec7-102">SYNOPSIS</span></span>
<span data-ttu-id="3bec7-103">Remove um domínio de grade de evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3bec7-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3bec7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bec7-104">SYNTAX</span></span>

### <span data-ttu-id="3bec7-105">DomainNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3bec7-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bec7-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bec7-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bec7-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bec7-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bec7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bec7-108">DESCRIPTION</span></span>
<span data-ttu-id="3bec7-109">Remove um domínio de grade de evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3bec7-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="3bec7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bec7-110">EXAMPLES</span></span>

### <span data-ttu-id="3bec7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3bec7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="3bec7-112">Remove o Domínio de Domínio da Grade do Evento1 no grupo \` de recursos \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="3bec7-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3bec7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3bec7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="3bec7-114">Remove o Domínio de Domínio da Grade do Evento1 no grupo \` de recursos \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="3bec7-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3bec7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bec7-115">PARAMETERS</span></span>

### <span data-ttu-id="3bec7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bec7-116">-DefaultProfile</span></span>
<span data-ttu-id="3bec7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bec7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bec7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bec7-118">-InputObject</span></span>
<span data-ttu-id="3bec7-119">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="3bec7-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="3bec7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bec7-120">-Name</span></span>
<span data-ttu-id="3bec7-121">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="3bec7-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="3bec7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bec7-122">-PassThru</span></span>
<span data-ttu-id="3bec7-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3bec7-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3bec7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bec7-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bec7-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3bec7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="3bec7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bec7-126">-ResourceId</span></span>
<span data-ttu-id="3bec7-127">Identificador de Recurso representando o Domínio da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="3bec7-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="3bec7-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3bec7-128">-Confirm</span></span>
<span data-ttu-id="3bec7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bec7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bec7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bec7-130">-WhatIf</span></span>
<span data-ttu-id="3bec7-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3bec7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bec7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3bec7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bec7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bec7-133">CommonParameters</span></span>
<span data-ttu-id="3bec7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bec7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bec7-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bec7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bec7-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3bec7-136">INPUTS</span></span>

### <span data-ttu-id="3bec7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3bec7-137">System.String</span></span>

### <span data-ttu-id="3bec7-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="3bec7-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="3bec7-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="3bec7-139">OUTPUTS</span></span>

### <span data-ttu-id="3bec7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bec7-140">System.Boolean</span></span>

## <span data-ttu-id="3bec7-141">Notas</span><span class="sxs-lookup"><span data-stu-id="3bec7-141">NOTES</span></span>

## <span data-ttu-id="3bec7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bec7-142">RELATED LINKS</span></span>
