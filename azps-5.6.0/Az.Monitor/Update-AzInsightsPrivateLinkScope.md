---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887106"
---
# <span data-ttu-id="180b0-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="180b0-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="180b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="180b0-102">SYNOPSIS</span></span>
<span data-ttu-id="180b0-103">Atualização para escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="180b0-103">Update for private link scope</span></span>

## <span data-ttu-id="180b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="180b0-104">SYNTAX</span></span>

### <span data-ttu-id="180b0-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="180b0-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="180b0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="180b0-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="180b0-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="180b0-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="180b0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="180b0-108">DESCRIPTION</span></span>
<span data-ttu-id="180b0-109">Atualização para escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="180b0-109">Update for private link scope</span></span>

## <span data-ttu-id="180b0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="180b0-110">EXAMPLES</span></span>

### <span data-ttu-id="180b0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="180b0-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="180b0-112">atualizar escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name" para usar a marca "key:value"</span><span class="sxs-lookup"><span data-stu-id="180b0-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="180b0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="180b0-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="180b0-114">atualizar escopo de link privado com id de recurso para usar a marca "key:value"</span><span class="sxs-lookup"><span data-stu-id="180b0-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="180b0-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="180b0-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="180b0-116">atualizar escopo de link privado com objeto de escopo de link privado de entrada para usar a marca "key:value"</span><span class="sxs-lookup"><span data-stu-id="180b0-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="180b0-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="180b0-117">PARAMETERS</span></span>

### <span data-ttu-id="180b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180b0-118">-DefaultProfile</span></span>
<span data-ttu-id="180b0-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="180b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="180b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="180b0-120">-InputObject</span></span>
<span data-ttu-id="180b0-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="180b0-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="180b0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="180b0-122">-Name</span></span>
<span data-ttu-id="180b0-123">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="180b0-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="180b0-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="180b0-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180b0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="180b0-126">-ResourceId</span></span>
<span data-ttu-id="180b0-127">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="180b0-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180b0-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="180b0-128">-Tags</span></span>
<span data-ttu-id="180b0-129">Tags</span><span class="sxs-lookup"><span data-stu-id="180b0-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180b0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="180b0-130">-Confirm</span></span>
<span data-ttu-id="180b0-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="180b0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="180b0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="180b0-132">-WhatIf</span></span>
<span data-ttu-id="180b0-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="180b0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="180b0-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="180b0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="180b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180b0-135">CommonParameters</span></span>
<span data-ttu-id="180b0-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180b0-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="180b0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180b0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="180b0-138">INPUTS</span></span>

### <span data-ttu-id="180b0-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="180b0-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="180b0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="180b0-140">System.String</span></span>

## <span data-ttu-id="180b0-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="180b0-141">OUTPUTS</span></span>

### <span data-ttu-id="180b0-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="180b0-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="180b0-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="180b0-143">NOTES</span></span>

## <span data-ttu-id="180b0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="180b0-144">RELATED LINKS</span></span>
