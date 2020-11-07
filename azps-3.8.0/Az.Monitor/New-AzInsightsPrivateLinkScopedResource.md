---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940412"
---
# <span data-ttu-id="5e29e-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5e29e-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5e29e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e29e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e29e-103">criar para recurso de escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="5e29e-103">create for private link scoped resource</span></span>

## <span data-ttu-id="5e29e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e29e-104">SYNTAX</span></span>

### <span data-ttu-id="5e29e-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e29e-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e29e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e29e-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e29e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e29e-107">DESCRIPTION</span></span>
<span data-ttu-id="5e29e-108">criar para recurso de escopo de link privado, o recurso em escopo pode ser espaço de trabalho de análise de log ou componente Application insights</span><span class="sxs-lookup"><span data-stu-id="5e29e-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="5e29e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e29e-109">EXAMPLES</span></span>

### <span data-ttu-id="5e29e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e29e-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="5e29e-111">criar recurso de escopo "scoped_resource_name" vinculado ao componente Application insights "ai_name"</span><span class="sxs-lookup"><span data-stu-id="5e29e-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="5e29e-112">OS</span><span class="sxs-lookup"><span data-stu-id="5e29e-112">PARAMETERS</span></span>

### <span data-ttu-id="5e29e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e29e-113">-DefaultProfile</span></span>
<span data-ttu-id="5e29e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e29e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e29e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e29e-115">-InputObject</span></span>
<span data-ttu-id="5e29e-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5e29e-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="5e29e-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="5e29e-117">-LinkedResourceId</span></span>
<span data-ttu-id="5e29e-118">ID do recurso LA/AI para vincular</span><span class="sxs-lookup"><span data-stu-id="5e29e-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="5e29e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e29e-119">-Name</span></span>
<span data-ttu-id="5e29e-120">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="5e29e-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="5e29e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e29e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e29e-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5e29e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5e29e-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="5e29e-123">-ScopeName</span></span>
<span data-ttu-id="5e29e-124">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="5e29e-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="5e29e-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e29e-125">-Confirm</span></span>
<span data-ttu-id="5e29e-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e29e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e29e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e29e-127">-WhatIf</span></span>
<span data-ttu-id="5e29e-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e29e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e29e-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e29e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e29e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e29e-130">CommonParameters</span></span>
<span data-ttu-id="5e29e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e29e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e29e-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e29e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e29e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e29e-133">INPUTS</span></span>

### <span data-ttu-id="5e29e-134">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5e29e-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="5e29e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5e29e-135">System.String</span></span>

## <span data-ttu-id="5e29e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e29e-136">OUTPUTS</span></span>

### <span data-ttu-id="5e29e-137">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5e29e-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5e29e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e29e-138">NOTES</span></span>

## <span data-ttu-id="5e29e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e29e-139">RELATED LINKS</span></span>
