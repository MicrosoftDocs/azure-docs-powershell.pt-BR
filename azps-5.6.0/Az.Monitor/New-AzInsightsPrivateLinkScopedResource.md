---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892840"
---
# <span data-ttu-id="e42f5-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="e42f5-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="e42f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e42f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e42f5-103">criar para o recurso de escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="e42f5-103">create for private link scoped resource</span></span>

## <span data-ttu-id="e42f5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e42f5-104">SYNTAX</span></span>

### <span data-ttu-id="e42f5-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e42f5-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e42f5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42f5-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e42f5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e42f5-107">DESCRIPTION</span></span>
<span data-ttu-id="e42f5-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span><span class="sxs-lookup"><span data-stu-id="e42f5-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="e42f5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e42f5-109">EXAMPLES</span></span>

### <span data-ttu-id="e42f5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e42f5-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="e42f5-111">criar recurso com escopo "scoped_resource_name" vinculado ao componente de insights do aplicativo "ai_name"</span><span class="sxs-lookup"><span data-stu-id="e42f5-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="e42f5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e42f5-112">PARAMETERS</span></span>

### <span data-ttu-id="e42f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42f5-113">-DefaultProfile</span></span>
<span data-ttu-id="e42f5-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e42f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42f5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e42f5-115">-InputObject</span></span>
<span data-ttu-id="e42f5-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e42f5-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="e42f5-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="e42f5-117">-LinkedResourceId</span></span>
<span data-ttu-id="e42f5-118">ID de recurso LA/AI para Link</span><span class="sxs-lookup"><span data-stu-id="e42f5-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42f5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e42f5-119">-Name</span></span>
<span data-ttu-id="e42f5-120">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="e42f5-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e42f5-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e42f5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e42f5-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="e42f5-123">-ScopeName</span></span>
<span data-ttu-id="e42f5-124">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="e42f5-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="e42f5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e42f5-125">-Confirm</span></span>
<span data-ttu-id="e42f5-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e42f5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42f5-127">-WhatIf</span></span>
<span data-ttu-id="e42f5-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e42f5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42f5-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e42f5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42f5-130">CommonParameters</span></span>
<span data-ttu-id="e42f5-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42f5-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e42f5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42f5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e42f5-133">INPUTS</span></span>

### <span data-ttu-id="e42f5-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e42f5-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e42f5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e42f5-135">System.String</span></span>

## <span data-ttu-id="e42f5-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e42f5-136">OUTPUTS</span></span>

### <span data-ttu-id="e42f5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="e42f5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="e42f5-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="e42f5-138">NOTES</span></span>

## <span data-ttu-id="e42f5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e42f5-139">RELATED LINKS</span></span>
