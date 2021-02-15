---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111744"
---
# <span data-ttu-id="13722-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="13722-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="13722-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13722-102">SYNOPSIS</span></span>
<span data-ttu-id="13722-103">excluir para o recurso com escopo de link particular</span><span class="sxs-lookup"><span data-stu-id="13722-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="13722-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13722-104">SYNTAX</span></span>

### <span data-ttu-id="13722-105">ByScopeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13722-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13722-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13722-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13722-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13722-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13722-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="13722-108">DESCRIPTION</span></span>
<span data-ttu-id="13722-109">excluir para o recurso com escopo de link particular</span><span class="sxs-lookup"><span data-stu-id="13722-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="13722-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13722-110">EXAMPLES</span></span>

### <span data-ttu-id="13722-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13722-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="13722-112">excluir recurso com escopo de link particular</span><span class="sxs-lookup"><span data-stu-id="13722-112">delete private link scoped resource</span></span>

## <span data-ttu-id="13722-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13722-113">PARAMETERS</span></span>

### <span data-ttu-id="13722-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13722-114">-DefaultProfile</span></span>
<span data-ttu-id="13722-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13722-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13722-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13722-116">-InputObject</span></span>
<span data-ttu-id="13722-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="13722-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="13722-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="13722-118">-Name</span></span>
<span data-ttu-id="13722-119">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="13722-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="13722-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13722-120">-ResourceGroupName</span></span>
<span data-ttu-id="13722-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="13722-121">Resource Group Name</span></span>

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

### <span data-ttu-id="13722-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13722-122">-ResourceId</span></span>
<span data-ttu-id="13722-123">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="13722-123">Resource Id</span></span>

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

### <span data-ttu-id="13722-124">-Nomedo Escopo</span><span class="sxs-lookup"><span data-stu-id="13722-124">-ScopeName</span></span>
<span data-ttu-id="13722-125">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="13722-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="13722-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="13722-126">-Confirm</span></span>
<span data-ttu-id="13722-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13722-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13722-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13722-128">-WhatIf</span></span>
<span data-ttu-id="13722-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="13722-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13722-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13722-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13722-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13722-131">CommonParameters</span></span>
<span data-ttu-id="13722-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13722-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13722-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13722-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13722-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="13722-134">INPUTS</span></span>

### <span data-ttu-id="13722-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="13722-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="13722-136">System.String</span><span class="sxs-lookup"><span data-stu-id="13722-136">System.String</span></span>

## <span data-ttu-id="13722-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="13722-137">OUTPUTS</span></span>

### <span data-ttu-id="13722-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13722-138">System.Boolean</span></span>

## <span data-ttu-id="13722-139">Notas</span><span class="sxs-lookup"><span data-stu-id="13722-139">NOTES</span></span>

## <span data-ttu-id="13722-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13722-140">RELATED LINKS</span></span>
