---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258162"
---
# <span data-ttu-id="c9ab1-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="c9ab1-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="c9ab1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ab1-103">Recupera informações sobre o modo de exibição de modelo ou o modo de exibição de instância de um computador híbrido.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="c9ab1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9ab1-104">SYNTAX</span></span>

### <span data-ttu-id="c9ab1-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9ab1-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9ab1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c9ab1-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9ab1-107">Programação</span><span class="sxs-lookup"><span data-stu-id="c9ab1-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9ab1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="c9ab1-109">Recupera informações sobre o modo de exibição de modelo ou o modo de exibição de instância de um computador híbrido.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="c9ab1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="c9ab1-111">Exemplo 1: listar todas as máquinas conectadas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c9ab1-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="c9ab1-112">Lista todas as máquinas conectadas em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="c9ab1-113">Se a assinatura não for especificada, ela usará a assinatura do contexto atual do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="c9ab1-114">Exemplo 2: listar todas as máquinas conectadas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c9ab1-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="c9ab1-115">Listar todas as máquinas conectadas em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="c9ab1-116">Exemplo 3: obter um computador conectado em um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="c9ab1-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="c9ab1-117">Obtenha um computador conectado em um grupo de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="c9ab1-118">OS</span><span class="sxs-lookup"><span data-stu-id="c9ab1-118">PARAMETERS</span></span>

### <span data-ttu-id="c9ab1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ab1-119">-DefaultProfile</span></span>
<span data-ttu-id="c9ab1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ab1-121">-Expandir</span><span class="sxs-lookup"><span data-stu-id="c9ab1-121">-Expand</span></span>
<span data-ttu-id="c9ab1-122">A expressão de expansão a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-122">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="c9ab1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9ab1-123">-Name</span></span>
<span data-ttu-id="c9ab1-124">O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="c9ab1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ab1-125">-ResourceGroupName</span></span>
<span data-ttu-id="c9ab1-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9ab1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9ab1-127">-SubscriptionId</span></span>
<span data-ttu-id="c9ab1-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9ab1-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9ab1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ab1-130">CommonParameters</span></span>
<span data-ttu-id="c9ab1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ab1-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9ab1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ab1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9ab1-133">INPUTS</span></span>

## <span data-ttu-id="c9ab1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9ab1-134">OUTPUTS</span></span>

### <span data-ttu-id="c9ab1-135">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachine</span><span class="sxs-lookup"><span data-stu-id="c9ab1-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="c9ab1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9ab1-136">NOTES</span></span>

<span data-ttu-id="c9ab1-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c9ab1-137">ALIASES</span></span>

## <span data-ttu-id="c9ab1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9ab1-138">RELATED LINKS</span></span>

