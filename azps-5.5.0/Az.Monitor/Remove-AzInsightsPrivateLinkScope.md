---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112945"
---
# <span data-ttu-id="698c7-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="698c7-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="698c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="698c7-102">SYNOPSIS</span></span>
<span data-ttu-id="698c7-103">excluir escopo de link particular</span><span class="sxs-lookup"><span data-stu-id="698c7-103">delete private link scope</span></span>

## <span data-ttu-id="698c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="698c7-104">SYNTAX</span></span>

### <span data-ttu-id="698c7-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="698c7-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698c7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="698c7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698c7-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="698c7-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="698c7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="698c7-108">DESCRIPTION</span></span>
<span data-ttu-id="698c7-109">excluir escopo de link particular</span><span class="sxs-lookup"><span data-stu-id="698c7-109">delete private link scope</span></span>

## <span data-ttu-id="698c7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="698c7-110">EXAMPLES</span></span>

### <span data-ttu-id="698c7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="698c7-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="698c7-112">excluir escopo de link particular com o nome "scope_name" no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="698c7-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="698c7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="698c7-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="698c7-114">excluir escopo de link privado com ID de recurso</span><span class="sxs-lookup"><span data-stu-id="698c7-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="698c7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="698c7-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="698c7-116">excluir escopo de link particular com objeto de escopo de link particular de entrada</span><span class="sxs-lookup"><span data-stu-id="698c7-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="698c7-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="698c7-117">PARAMETERS</span></span>

### <span data-ttu-id="698c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698c7-118">-DefaultProfile</span></span>
<span data-ttu-id="698c7-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="698c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="698c7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="698c7-120">-InputObject</span></span>
<span data-ttu-id="698c7-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="698c7-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="698c7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="698c7-122">-Name</span></span>
<span data-ttu-id="698c7-123">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="698c7-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="698c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="698c7-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="698c7-125">Resource Group Name</span></span>

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

### <span data-ttu-id="698c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="698c7-126">-ResourceId</span></span>
<span data-ttu-id="698c7-127">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="698c7-127">Resource Id</span></span>

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

### <span data-ttu-id="698c7-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="698c7-128">-Confirm</span></span>
<span data-ttu-id="698c7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="698c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="698c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698c7-130">-WhatIf</span></span>
<span data-ttu-id="698c7-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="698c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698c7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="698c7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="698c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698c7-133">CommonParameters</span></span>
<span data-ttu-id="698c7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698c7-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="698c7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698c7-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="698c7-136">INPUTS</span></span>

### <span data-ttu-id="698c7-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="698c7-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="698c7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="698c7-138">System.String</span></span>

## <span data-ttu-id="698c7-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="698c7-139">OUTPUTS</span></span>

### <span data-ttu-id="698c7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="698c7-140">System.Boolean</span></span>

## <span data-ttu-id="698c7-141">Notas</span><span class="sxs-lookup"><span data-stu-id="698c7-141">NOTES</span></span>

## <span data-ttu-id="698c7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="698c7-142">RELATED LINKS</span></span>
