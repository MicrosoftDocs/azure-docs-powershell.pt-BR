---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 83f4fae326920b24d272ae87341c20702a2bf8fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892120"
---
# <span data-ttu-id="d851a-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d851a-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="d851a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d851a-102">SYNOPSIS</span></span>
<span data-ttu-id="d851a-103">excluir para o recurso de escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d851a-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="d851a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d851a-104">SYNTAX</span></span>

### <span data-ttu-id="d851a-105">ByScopeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d851a-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d851a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d851a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d851a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d851a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d851a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d851a-108">DESCRIPTION</span></span>
<span data-ttu-id="d851a-109">excluir para o recurso de escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d851a-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="d851a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d851a-110">EXAMPLES</span></span>

### <span data-ttu-id="d851a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d851a-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="d851a-112">excluir recurso com escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d851a-112">delete private link scoped resource</span></span>

## <span data-ttu-id="d851a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d851a-113">PARAMETERS</span></span>

### <span data-ttu-id="d851a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d851a-114">-DefaultProfile</span></span>
<span data-ttu-id="d851a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d851a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d851a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d851a-116">-InputObject</span></span>
<span data-ttu-id="d851a-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d851a-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d851a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d851a-118">-Name</span></span>
<span data-ttu-id="d851a-119">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="d851a-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d851a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d851a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d851a-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d851a-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d851a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d851a-122">-ResourceId</span></span>
<span data-ttu-id="d851a-123">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="d851a-123">Resource Id</span></span>

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

### <span data-ttu-id="d851a-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="d851a-124">-ScopeName</span></span>
<span data-ttu-id="d851a-125">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d851a-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d851a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d851a-126">-Confirm</span></span>
<span data-ttu-id="d851a-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d851a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d851a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d851a-128">-WhatIf</span></span>
<span data-ttu-id="d851a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d851a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d851a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d851a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d851a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d851a-131">CommonParameters</span></span>
<span data-ttu-id="d851a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d851a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d851a-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d851a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d851a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d851a-134">INPUTS</span></span>

### <span data-ttu-id="d851a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d851a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="d851a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d851a-136">System.String</span></span>

## <span data-ttu-id="d851a-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d851a-137">OUTPUTS</span></span>

### <span data-ttu-id="d851a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d851a-138">System.Boolean</span></span>

## <span data-ttu-id="d851a-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="d851a-139">NOTES</span></span>

## <span data-ttu-id="d851a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d851a-140">RELATED LINKS</span></span>
