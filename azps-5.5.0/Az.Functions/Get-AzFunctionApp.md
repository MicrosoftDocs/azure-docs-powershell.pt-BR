---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126943"
---
# <span data-ttu-id="e0443-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e0443-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="e0443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0443-102">SYNOPSIS</span></span>
<span data-ttu-id="e0443-103">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0443-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="e0443-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0443-104">SYNTAX</span></span>

### <span data-ttu-id="e0443-105">GetAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0443-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0443-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="e0443-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0443-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e0443-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0443-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0443-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e0443-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0443-109">DESCRIPTION</span></span>
<span data-ttu-id="e0443-110">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0443-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="e0443-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0443-111">EXAMPLES</span></span>

### <span data-ttu-id="e0443-112">Exemplo 1: Obter todos os aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="e0443-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="e0443-113">Exemplo 2: Obter aplicativos de função por nome.</span><span class="sxs-lookup"><span data-stu-id="e0443-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="e0443-114">Exemplo 3: Obter aplicativos de função por nome de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0443-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="e0443-115">Exemplo 4: Obter aplicativos de função para determinadas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="e0443-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="e0443-116">Exemplo 5: Obter aplicativos de função por local.</span><span class="sxs-lookup"><span data-stu-id="e0443-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="e0443-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0443-117">PARAMETERS</span></span>

### <span data-ttu-id="e0443-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0443-118">-DefaultProfile</span></span>
<span data-ttu-id="e0443-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0443-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0443-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="e0443-120">-IncludeSlot</span></span>
<span data-ttu-id="e0443-121">Use para especificar se você deve incluir slots de implantação nos resultados.</span><span class="sxs-lookup"><span data-stu-id="e0443-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="e0443-122">-Local</span><span class="sxs-lookup"><span data-stu-id="e0443-122">-Location</span></span>
<span data-ttu-id="e0443-123">O local do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="e0443-123">The location of the function app.</span></span>

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

### <span data-ttu-id="e0443-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0443-124">-Name</span></span>
<span data-ttu-id="e0443-125">O nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="e0443-125">The name of the function app.</span></span>

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

### <span data-ttu-id="e0443-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0443-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0443-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0443-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0443-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0443-128">-SubscriptionId</span></span>
<span data-ttu-id="e0443-129">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0443-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e0443-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0443-130">CommonParameters</span></span>
<span data-ttu-id="e0443-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0443-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0443-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0443-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0443-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0443-133">INPUTS</span></span>

## <span data-ttu-id="e0443-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0443-134">OUTPUTS</span></span>

### <span data-ttu-id="e0443-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="e0443-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="e0443-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e0443-136">NOTES</span></span>

<span data-ttu-id="e0443-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="e0443-137">ALIASES</span></span>

## <span data-ttu-id="e0443-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0443-138">RELATED LINKS</span></span>

