---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115429"
---
# <span data-ttu-id="3f4ae-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="3f4ae-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="3f4ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4ae-103">Obter os planos de aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="3f4ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f4ae-104">SYNTAX</span></span>

### <span data-ttu-id="3f4ae-105">GetAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f4ae-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f4ae-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="3f4ae-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4ae-107">ByName</span><span class="sxs-lookup"><span data-stu-id="3f4ae-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f4ae-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4ae-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f4ae-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f4ae-109">DESCRIPTION</span></span>
<span data-ttu-id="3f4ae-110">Obter os planos de aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="3f4ae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f4ae-111">EXAMPLES</span></span>

### <span data-ttu-id="3f4ae-112">Exemplo 1: obter todos os planos de aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="3f4ae-113">Esse comando obtém todos os planos do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="3f4ae-114">Exemplo 2: obter planos de aplicativo de função por nome de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="3f4ae-115">Esse comando obtém planos de aplicativo de função por nome de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="3f4ae-116">Exemplo 3: obter planos de aplicativo de função para as assinaturas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="3f4ae-117">Esse comando obtém planos de aplicativo de função para as assinaturas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="3f4ae-118">Exemplo 4: obter planos de aplicativo de função por localização.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="3f4ae-119">Esse comando obtém planos de aplicativo de função por localização.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="3f4ae-120">OS</span><span class="sxs-lookup"><span data-stu-id="3f4ae-120">PARAMETERS</span></span>

### <span data-ttu-id="3f4ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4ae-121">-DefaultProfile</span></span>
<span data-ttu-id="3f4ae-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4ae-123">-Local</span><span class="sxs-lookup"><span data-stu-id="3f4ae-123">-Location</span></span>
<span data-ttu-id="3f4ae-124">O local do plano do aplicativo função.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="3f4ae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f4ae-125">-Name</span></span>
<span data-ttu-id="3f4ae-126">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-126">The service plan name.</span></span>

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

### <span data-ttu-id="3f4ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f4ae-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f4ae-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f4ae-129">-SubscriptionId</span></span>
<span data-ttu-id="3f4ae-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="3f4ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4ae-131">CommonParameters</span></span>
<span data-ttu-id="3f4ae-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4ae-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f4ae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4ae-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f4ae-134">INPUTS</span></span>

## <span data-ttu-id="3f4ae-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f4ae-135">OUTPUTS</span></span>

### <span data-ttu-id="3f4ae-136">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3f4ae-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="3f4ae-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f4ae-137">NOTES</span></span>

<span data-ttu-id="3f4ae-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3f4ae-138">ALIASES</span></span>

## <span data-ttu-id="3f4ae-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f4ae-139">RELATED LINKS</span></span>

