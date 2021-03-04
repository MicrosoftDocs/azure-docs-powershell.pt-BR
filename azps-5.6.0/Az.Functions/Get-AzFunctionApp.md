---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: ee678b905eba891543399c9130a8ef034daf2a16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887523"
---
# <span data-ttu-id="ca416-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="ca416-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="ca416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca416-102">SYNOPSIS</span></span>
<span data-ttu-id="ca416-103">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca416-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="ca416-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca416-104">SYNTAX</span></span>

### <span data-ttu-id="ca416-105">GetAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca416-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca416-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="ca416-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca416-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ca416-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca416-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca416-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ca416-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca416-109">DESCRIPTION</span></span>
<span data-ttu-id="ca416-110">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca416-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="ca416-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca416-111">EXAMPLES</span></span>

### <span data-ttu-id="ca416-112">Exemplo 1: Obter todos os aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="ca416-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="ca416-113">Exemplo 2: Obter aplicativos de função pelo nome.</span><span class="sxs-lookup"><span data-stu-id="ca416-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="ca416-114">Exemplo 3: Obter aplicativos de função pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca416-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="ca416-115">Exemplo 4: Obter aplicativos de função para as assinaturas determinadas.</span><span class="sxs-lookup"><span data-stu-id="ca416-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="ca416-116">Exemplo 5: Obter aplicativos de função por local.</span><span class="sxs-lookup"><span data-stu-id="ca416-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="ca416-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca416-117">PARAMETERS</span></span>

### <span data-ttu-id="ca416-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca416-118">-DefaultProfile</span></span>
<span data-ttu-id="ca416-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca416-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca416-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="ca416-120">-IncludeSlot</span></span>
<span data-ttu-id="ca416-121">Use para especificar se devem incluir slots de implantação nos resultados.</span><span class="sxs-lookup"><span data-stu-id="ca416-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca416-122">-Location</span><span class="sxs-lookup"><span data-stu-id="ca416-122">-Location</span></span>
<span data-ttu-id="ca416-123">O local do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="ca416-123">The location of the function app.</span></span>

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

### <span data-ttu-id="ca416-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ca416-124">-Name</span></span>
<span data-ttu-id="ca416-125">O nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="ca416-125">The name of the function app.</span></span>

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

### <span data-ttu-id="ca416-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca416-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca416-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca416-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca416-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca416-128">-SubscriptionId</span></span>
<span data-ttu-id="ca416-129">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca416-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="ca416-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca416-130">CommonParameters</span></span>
<span data-ttu-id="ca416-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca416-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca416-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca416-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca416-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca416-133">INPUTS</span></span>

## <span data-ttu-id="ca416-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca416-134">OUTPUTS</span></span>

### <span data-ttu-id="ca416-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="ca416-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="ca416-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca416-136">NOTES</span></span>

<span data-ttu-id="ca416-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ca416-137">ALIASES</span></span>

## <span data-ttu-id="ca416-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca416-138">RELATED LINKS</span></span>

