---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888891"
---
# <span data-ttu-id="a6e7f-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a6e7f-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a6e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e7f-103">Obter para o recurso de escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a6e7f-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="a6e7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6e7f-104">SYNTAX</span></span>

### <span data-ttu-id="a6e7f-105">ByScopeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6e7f-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e7f-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6e7f-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e7f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6e7f-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6e7f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6e7f-108">DESCRIPTION</span></span>
<span data-ttu-id="a6e7f-109">Obter ou listar o recurso com escopo de link privado, o recurso com escopo pode ser o espaço de trabalho do Log Analytics ou o componente Application Insights</span><span class="sxs-lookup"><span data-stu-id="a6e7f-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="a6e7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-110">EXAMPLES</span></span>

### <span data-ttu-id="a6e7f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6e7f-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="a6e7f-112">Listar recurso com escopo em escopo de link privado "scope_name"</span><span class="sxs-lookup"><span data-stu-id="a6e7f-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="a6e7f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a6e7f-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="a6e7f-114">Obter recurso com escopo em escopo de link privado "scope_name" com o nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="a6e7f-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="a6e7f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-115">PARAMETERS</span></span>

### <span data-ttu-id="a6e7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e7f-116">-DefaultProfile</span></span>
<span data-ttu-id="a6e7f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6e7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6e7f-118">-InputObject</span></span>
<span data-ttu-id="a6e7f-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a6e7f-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e7f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a6e7f-120">-Name</span></span>
<span data-ttu-id="a6e7f-121">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="a6e7f-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e7f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e7f-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6e7f-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a6e7f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a6e7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e7f-124">-ResourceId</span></span>
<span data-ttu-id="a6e7f-125">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="a6e7f-125">Resource Id</span></span>

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

### <span data-ttu-id="a6e7f-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="a6e7f-126">-ScopeName</span></span>
<span data-ttu-id="a6e7f-127">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a6e7f-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a6e7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e7f-128">CommonParameters</span></span>
<span data-ttu-id="a6e7f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e7f-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6e7f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e7f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-131">INPUTS</span></span>

### <span data-ttu-id="a6e7f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a6e7f-132">System.String</span></span>

## <span data-ttu-id="a6e7f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-133">OUTPUTS</span></span>

### <span data-ttu-id="a6e7f-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a6e7f-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a6e7f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6e7f-135">NOTES</span></span>

## <span data-ttu-id="a6e7f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6e7f-136">RELATED LINKS</span></span>
