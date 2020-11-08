---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112772"
---
# <span data-ttu-id="234a1-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="234a1-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="234a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="234a1-102">SYNOPSIS</span></span>
<span data-ttu-id="234a1-103">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="234a1-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="234a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="234a1-104">SYNTAX</span></span>

### <span data-ttu-id="234a1-105">GetAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="234a1-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="234a1-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="234a1-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="234a1-107">ByName</span><span class="sxs-lookup"><span data-stu-id="234a1-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="234a1-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="234a1-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="234a1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="234a1-109">DESCRIPTION</span></span>
<span data-ttu-id="234a1-110">Obtém aplicativos de função em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="234a1-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="234a1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="234a1-111">EXAMPLES</span></span>

### <span data-ttu-id="234a1-112">Exemplo 1: obter todos os aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="234a1-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="234a1-113">Exemplo 2: obter os aplicativos de função por nome.</span><span class="sxs-lookup"><span data-stu-id="234a1-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="234a1-114">Exemplo 3: obter aplicativos de função por nome de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="234a1-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="234a1-115">Exemplo 4: obter aplicativos de função para as assinaturas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="234a1-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="234a1-116">Exemplo 5: obter os aplicativos de função por localização.</span><span class="sxs-lookup"><span data-stu-id="234a1-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="234a1-117">OS</span><span class="sxs-lookup"><span data-stu-id="234a1-117">PARAMETERS</span></span>

### <span data-ttu-id="234a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234a1-118">-DefaultProfile</span></span>
<span data-ttu-id="234a1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="234a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="234a1-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="234a1-120">-IncludeSlot</span></span>
<span data-ttu-id="234a1-121">Use para especificar se os slots de implantação devem ser incluídos nos resultados.</span><span class="sxs-lookup"><span data-stu-id="234a1-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234a1-122">-Local</span><span class="sxs-lookup"><span data-stu-id="234a1-122">-Location</span></span>
<span data-ttu-id="234a1-123">O local do aplicativo da função.</span><span class="sxs-lookup"><span data-stu-id="234a1-123">The location of the function app.</span></span>

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

### <span data-ttu-id="234a1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="234a1-124">-Name</span></span>
<span data-ttu-id="234a1-125">O nome do aplicativo da função.</span><span class="sxs-lookup"><span data-stu-id="234a1-125">The name of the function app.</span></span>

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

### <span data-ttu-id="234a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="234a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="234a1-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="234a1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="234a1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="234a1-128">-SubscriptionId</span></span>
<span data-ttu-id="234a1-129">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="234a1-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="234a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234a1-130">CommonParameters</span></span>
<span data-ttu-id="234a1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="234a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234a1-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="234a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234a1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="234a1-133">INPUTS</span></span>

## <span data-ttu-id="234a1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="234a1-134">OUTPUTS</span></span>

### <span data-ttu-id="234a1-135">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="234a1-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="234a1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="234a1-136">NOTES</span></span>

<span data-ttu-id="234a1-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="234a1-137">ALIASES</span></span>

## <span data-ttu-id="234a1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="234a1-138">RELATED LINKS</span></span>

