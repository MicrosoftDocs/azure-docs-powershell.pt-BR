---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272248"
---
# <span data-ttu-id="811ba-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="811ba-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="811ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="811ba-102">SYNOPSIS</span></span>
<span data-ttu-id="811ba-103">Obter recurso de escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="811ba-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="811ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="811ba-104">SYNTAX</span></span>

### <span data-ttu-id="811ba-105">ByScopeParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="811ba-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="811ba-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="811ba-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="811ba-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="811ba-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="811ba-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="811ba-108">DESCRIPTION</span></span>
<span data-ttu-id="811ba-109">Obter ou listar um recurso escopo de link privado, o recurso em escopo pode ser espaço de trabalho de análise de log ou componente Application insights</span><span class="sxs-lookup"><span data-stu-id="811ba-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="811ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="811ba-110">EXAMPLES</span></span>

### <span data-ttu-id="811ba-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="811ba-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="811ba-112">Lista de recursos com escopo em escopo de link privado "scope_name"</span><span class="sxs-lookup"><span data-stu-id="811ba-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="811ba-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="811ba-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="811ba-114">Obter recurso de escopo no escopo do link privado "scope_name" com o nome "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="811ba-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="811ba-115">OS</span><span class="sxs-lookup"><span data-stu-id="811ba-115">PARAMETERS</span></span>

### <span data-ttu-id="811ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811ba-116">-DefaultProfile</span></span>
<span data-ttu-id="811ba-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="811ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="811ba-118">-InputObject</span></span>
<span data-ttu-id="811ba-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="811ba-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="811ba-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="811ba-120">-Name</span></span>
<span data-ttu-id="811ba-121">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="811ba-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="811ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="811ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="811ba-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="811ba-123">Resource Group Name</span></span>

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

### <span data-ttu-id="811ba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="811ba-124">-ResourceId</span></span>
<span data-ttu-id="811ba-125">ID do recurso</span><span class="sxs-lookup"><span data-stu-id="811ba-125">Resource Id</span></span>

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

### <span data-ttu-id="811ba-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="811ba-126">-ScopeName</span></span>
<span data-ttu-id="811ba-127">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="811ba-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="811ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811ba-128">CommonParameters</span></span>
<span data-ttu-id="811ba-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811ba-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="811ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811ba-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="811ba-131">INPUTS</span></span>

### <span data-ttu-id="811ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="811ba-132">System.String</span></span>

## <span data-ttu-id="811ba-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="811ba-133">OUTPUTS</span></span>

### <span data-ttu-id="811ba-134">icrosoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="811ba-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="811ba-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="811ba-135">NOTES</span></span>

## <span data-ttu-id="811ba-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="811ba-136">RELATED LINKS</span></span>
