---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118419"
---
# <span data-ttu-id="5370b-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5370b-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5370b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5370b-102">SYNOPSIS</span></span>
<span data-ttu-id="5370b-103">Obter para o recurso de vinculação privada com escopo</span><span class="sxs-lookup"><span data-stu-id="5370b-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="5370b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5370b-104">SYNTAX</span></span>

### <span data-ttu-id="5370b-105">ByScopeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5370b-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5370b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5370b-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5370b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5370b-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5370b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5370b-108">DESCRIPTION</span></span>
<span data-ttu-id="5370b-109">Obter ou lista para o recurso com escopo de link privado, o recurso com escopo pode ser o espaço de trabalho do Log Analytics ou o componente Informações do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5370b-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="5370b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5370b-110">EXAMPLES</span></span>

### <span data-ttu-id="5370b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5370b-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="5370b-112">Recurso com escopo de lista sob escopo de link privado "scope_name"</span><span class="sxs-lookup"><span data-stu-id="5370b-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="5370b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5370b-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="5370b-114">Obter recurso com escopo no escopo de link privado "scope_name" com o nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="5370b-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="5370b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5370b-115">PARAMETERS</span></span>

### <span data-ttu-id="5370b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5370b-116">-DefaultProfile</span></span>
<span data-ttu-id="5370b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5370b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5370b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5370b-118">-InputObject</span></span>
<span data-ttu-id="5370b-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5370b-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="5370b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5370b-120">-Name</span></span>
<span data-ttu-id="5370b-121">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="5370b-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="5370b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5370b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5370b-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5370b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5370b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5370b-124">-ResourceId</span></span>
<span data-ttu-id="5370b-125">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="5370b-125">Resource Id</span></span>

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

### <span data-ttu-id="5370b-126">-Nomedo Escopo</span><span class="sxs-lookup"><span data-stu-id="5370b-126">-ScopeName</span></span>
<span data-ttu-id="5370b-127">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="5370b-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="5370b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5370b-128">CommonParameters</span></span>
<span data-ttu-id="5370b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5370b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5370b-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5370b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5370b-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="5370b-131">INPUTS</span></span>

### <span data-ttu-id="5370b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5370b-132">System.String</span></span>

## <span data-ttu-id="5370b-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="5370b-133">OUTPUTS</span></span>

### <span data-ttu-id="5370b-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="5370b-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="5370b-135">Notas</span><span class="sxs-lookup"><span data-stu-id="5370b-135">NOTES</span></span>

## <span data-ttu-id="5370b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5370b-136">RELATED LINKS</span></span>
