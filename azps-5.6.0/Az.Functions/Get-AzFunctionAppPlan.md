---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: 786f3e406228eb7929993804a8cef84e7cae109e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887521"
---
# <span data-ttu-id="5d5d5-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="5d5d5-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="5d5d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5d5-103">Obter planos de aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="5d5d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5d5d5-104">SYNTAX</span></span>

### <span data-ttu-id="5d5d5-105">GetAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5d5d5-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d5d5-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="5d5d5-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d5d5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5d5d5-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d5d5-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5d5-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d5d5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5d5d5-109">DESCRIPTION</span></span>
<span data-ttu-id="5d5d5-110">Obter planos de aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="5d5d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-111">EXAMPLES</span></span>

### <span data-ttu-id="5d5d5-112">Exemplo 1: Obter todos os planos do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="5d5d5-113">Este comando obtém todos os planos do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="5d5d5-114">Exemplo 2: Obter planos de aplicativo de função pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="5d5d5-115">Este comando obtém planos de aplicativo de função pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="5d5d5-116">Exemplo 3: Obter planos de aplicativo de função para as assinaturas determinadas.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="5d5d5-117">Este comando obtém planos de aplicativo de função para as assinaturas determinadas.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="5d5d5-118">Exemplo 4: Obter planos de aplicativo de função por local.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="5d5d5-119">Este comando obtém planos de aplicativo de função por local.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="5d5d5-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-120">PARAMETERS</span></span>

### <span data-ttu-id="5d5d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5d5-121">-DefaultProfile</span></span>
<span data-ttu-id="5d5d5-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5d5-123">-Location</span><span class="sxs-lookup"><span data-stu-id="5d5d5-123">-Location</span></span>
<span data-ttu-id="5d5d5-124">O local do plano do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5d5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5d5d5-125">-Name</span></span>
<span data-ttu-id="5d5d5-126">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d5d5-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5d5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d5d5-129">-SubscriptionId</span></span>
<span data-ttu-id="5d5d5-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5d5-131">CommonParameters</span></span>
<span data-ttu-id="5d5d5-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5d5-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d5d5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5d5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-134">INPUTS</span></span>

## <span data-ttu-id="5d5d5-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-135">OUTPUTS</span></span>

### <span data-ttu-id="5d5d5-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5d5d5-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="5d5d5-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="5d5d5-137">NOTES</span></span>

<span data-ttu-id="5d5d5-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5d5d5-138">ALIASES</span></span>

## <span data-ttu-id="5d5d5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d5d5-139">RELATED LINKS</span></span>

