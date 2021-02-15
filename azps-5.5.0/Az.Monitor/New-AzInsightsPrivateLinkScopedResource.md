---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114761"
---
# <span data-ttu-id="f3bfe-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f3bfe-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f3bfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bfe-103">criar para o recurso de vinculação privada com escopo</span><span class="sxs-lookup"><span data-stu-id="f3bfe-103">create for private link scoped resource</span></span>

## <span data-ttu-id="f3bfe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3bfe-104">SYNTAX</span></span>

### <span data-ttu-id="f3bfe-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f3bfe-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3bfe-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3bfe-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3bfe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3bfe-107">DESCRIPTION</span></span>
<span data-ttu-id="f3bfe-108">criar para um recurso com escopo de link privado, o recurso com escopo pode ser o espaço de trabalho do Log Analytics ou o componente Informações do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f3bfe-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f3bfe-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3bfe-109">EXAMPLES</span></span>

### <span data-ttu-id="f3bfe-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3bfe-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f3bfe-111">criar recurso com escopo "scoped_resource_name" vinculado ao componente de informações do aplicativo "ai_name"</span><span class="sxs-lookup"><span data-stu-id="f3bfe-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="f3bfe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3bfe-112">PARAMETERS</span></span>

### <span data-ttu-id="f3bfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bfe-113">-DefaultProfile</span></span>
<span data-ttu-id="f3bfe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3bfe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3bfe-115">-InputObject</span></span>
<span data-ttu-id="f3bfe-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f3bfe-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="f3bfe-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="f3bfe-117">-LinkedResourceId</span></span>
<span data-ttu-id="f3bfe-118">ID de Recurso LA/AI para Vincular</span><span class="sxs-lookup"><span data-stu-id="f3bfe-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="f3bfe-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3bfe-119">-Name</span></span>
<span data-ttu-id="f3bfe-120">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="f3bfe-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="f3bfe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bfe-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3bfe-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f3bfe-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f3bfe-123">-Nomedo Escopo</span><span class="sxs-lookup"><span data-stu-id="f3bfe-123">-ScopeName</span></span>
<span data-ttu-id="f3bfe-124">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="f3bfe-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="f3bfe-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f3bfe-125">-Confirm</span></span>
<span data-ttu-id="f3bfe-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3bfe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bfe-127">-WhatIf</span></span>
<span data-ttu-id="f3bfe-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3bfe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3bfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bfe-130">CommonParameters</span></span>
<span data-ttu-id="f3bfe-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bfe-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3bfe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bfe-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f3bfe-133">INPUTS</span></span>

### <span data-ttu-id="f3bfe-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f3bfe-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="f3bfe-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f3bfe-135">System.String</span></span>

## <span data-ttu-id="f3bfe-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="f3bfe-136">OUTPUTS</span></span>

### <span data-ttu-id="f3bfe-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f3bfe-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f3bfe-138">Notas</span><span class="sxs-lookup"><span data-stu-id="f3bfe-138">NOTES</span></span>

## <span data-ttu-id="f3bfe-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3bfe-139">RELATED LINKS</span></span>
