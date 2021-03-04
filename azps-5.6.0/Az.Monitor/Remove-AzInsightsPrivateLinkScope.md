---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889452"
---
# <span data-ttu-id="d359b-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d359b-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d359b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d359b-102">SYNOPSIS</span></span>
<span data-ttu-id="d359b-103">excluir escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d359b-103">delete private link scope</span></span>

## <span data-ttu-id="d359b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d359b-104">SYNTAX</span></span>

### <span data-ttu-id="d359b-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d359b-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d359b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d359b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d359b-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d359b-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d359b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d359b-108">DESCRIPTION</span></span>
<span data-ttu-id="d359b-109">excluir escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d359b-109">delete private link scope</span></span>

## <span data-ttu-id="d359b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d359b-110">EXAMPLES</span></span>

### <span data-ttu-id="d359b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d359b-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="d359b-112">excluir escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="d359b-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="d359b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d359b-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="d359b-114">excluir escopo de link privado com id de recurso</span><span class="sxs-lookup"><span data-stu-id="d359b-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="d359b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d359b-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="d359b-116">excluir escopo de link privado com objeto de escopo de link privado de entrada</span><span class="sxs-lookup"><span data-stu-id="d359b-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="d359b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d359b-117">PARAMETERS</span></span>

### <span data-ttu-id="d359b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d359b-118">-DefaultProfile</span></span>
<span data-ttu-id="d359b-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d359b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d359b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d359b-120">-InputObject</span></span>
<span data-ttu-id="d359b-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d359b-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d359b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d359b-122">-Name</span></span>
<span data-ttu-id="d359b-123">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d359b-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d359b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d359b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d359b-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d359b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="d359b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d359b-126">-ResourceId</span></span>
<span data-ttu-id="d359b-127">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="d359b-127">Resource Id</span></span>

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

### <span data-ttu-id="d359b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d359b-128">-Confirm</span></span>
<span data-ttu-id="d359b-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d359b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d359b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d359b-130">-WhatIf</span></span>
<span data-ttu-id="d359b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d359b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d359b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d359b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d359b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d359b-133">CommonParameters</span></span>
<span data-ttu-id="d359b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d359b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d359b-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d359b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d359b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d359b-136">INPUTS</span></span>

### <span data-ttu-id="d359b-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d359b-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="d359b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d359b-138">System.String</span></span>

## <span data-ttu-id="d359b-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d359b-139">OUTPUTS</span></span>

### <span data-ttu-id="d359b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d359b-140">System.Boolean</span></span>

## <span data-ttu-id="d359b-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="d359b-141">NOTES</span></span>

## <span data-ttu-id="d359b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d359b-142">RELATED LINKS</span></span>
