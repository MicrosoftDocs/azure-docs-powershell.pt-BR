---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: c97567c2832d82ec739b62bfe8bb6c08e173f9e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893203"
---
# <span data-ttu-id="84bdf-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="84bdf-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="84bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="84bdf-103">Recupera informações sobre o exibição de modelo ou a exibição de instância de uma máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="84bdf-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="84bdf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="84bdf-104">SYNTAX</span></span>

### <span data-ttu-id="84bdf-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="84bdf-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="84bdf-106">Obter</span><span class="sxs-lookup"><span data-stu-id="84bdf-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="84bdf-107">Listar</span><span class="sxs-lookup"><span data-stu-id="84bdf-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="84bdf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="84bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="84bdf-109">Recupera informações sobre o exibição de modelo ou a exibição de instância de uma máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="84bdf-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="84bdf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="84bdf-111">Exemplo 1: Listar todos os dispositivos conectados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="84bdf-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="84bdf-112">Lista todos os dispositivos conectados em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="84bdf-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="84bdf-113">Se a assinatura não for especificada, ela usará a assinatura do contexto atual do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="84bdf-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="84bdf-114">Exemplo 2: Listar todos os dispositivos conectados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="84bdf-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="84bdf-115">Listar todos os dispositivos conectados em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84bdf-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="84bdf-116">Exemplo 3: Obter uma máquina conectada em um grupo de recursos pelo nome</span><span class="sxs-lookup"><span data-stu-id="84bdf-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="84bdf-117">Obter uma máquina conectada em um grupo de recursos pelo nome.</span><span class="sxs-lookup"><span data-stu-id="84bdf-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="84bdf-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="84bdf-118">PARAMETERS</span></span>

### <span data-ttu-id="84bdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bdf-119">-DefaultProfile</span></span>
<span data-ttu-id="84bdf-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84bdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84bdf-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="84bdf-121">-Expand</span></span>
<span data-ttu-id="84bdf-122">A expressão expandir a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="84bdf-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bdf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="84bdf-123">-Name</span></span>
<span data-ttu-id="84bdf-124">O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="84bdf-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="84bdf-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84bdf-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bdf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84bdf-127">-SubscriptionId</span></span>
<span data-ttu-id="84bdf-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84bdf-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="84bdf-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="84bdf-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84bdf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bdf-130">CommonParameters</span></span>
<span data-ttu-id="84bdf-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bdf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bdf-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84bdf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bdf-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84bdf-133">INPUTS</span></span>

## <span data-ttu-id="84bdf-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="84bdf-134">OUTPUTS</span></span>

### <span data-ttu-id="84bdf-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span><span class="sxs-lookup"><span data-stu-id="84bdf-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="84bdf-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="84bdf-136">NOTES</span></span>

<span data-ttu-id="84bdf-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="84bdf-137">ALIASES</span></span>

## <span data-ttu-id="84bdf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84bdf-138">RELATED LINKS</span></span>

