---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893202"
---
# <span data-ttu-id="bfc30-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bfc30-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="bfc30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc30-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc30-103">A operação para obter a extensão.</span><span class="sxs-lookup"><span data-stu-id="bfc30-103">The operation to get the extension.</span></span>

## <span data-ttu-id="bfc30-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfc30-104">SYNTAX</span></span>

### <span data-ttu-id="bfc30-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bfc30-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfc30-106">Obter</span><span class="sxs-lookup"><span data-stu-id="bfc30-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bfc30-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfc30-107">DESCRIPTION</span></span>
<span data-ttu-id="bfc30-108">A operação para obter a extensão.</span><span class="sxs-lookup"><span data-stu-id="bfc30-108">The operation to get the extension.</span></span>

## <span data-ttu-id="bfc30-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc30-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc30-110">Exemplo 1: Listar todas as extensões de um computador</span><span class="sxs-lookup"><span data-stu-id="bfc30-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="bfc30-111">Lista todas as extensões de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="bfc30-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="bfc30-112">Exemplo 2: Obter uma extensão específica em um computador</span><span class="sxs-lookup"><span data-stu-id="bfc30-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="bfc30-113">Obtém uma extensão específica em um computador.</span><span class="sxs-lookup"><span data-stu-id="bfc30-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="bfc30-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfc30-114">PARAMETERS</span></span>

### <span data-ttu-id="bfc30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc30-115">-DefaultProfile</span></span>
<span data-ttu-id="bfc30-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc30-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="bfc30-117">-Expand</span></span>
<span data-ttu-id="bfc30-118">A expressão expandir a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="bfc30-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc30-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="bfc30-119">-MachineName</span></span>
<span data-ttu-id="bfc30-120">O nome do computador que contém a extensão.</span><span class="sxs-lookup"><span data-stu-id="bfc30-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc30-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc30-121">-Name</span></span>
<span data-ttu-id="bfc30-122">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="bfc30-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="bfc30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc30-123">-ResourceGroupName</span></span>
<span data-ttu-id="bfc30-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfc30-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc30-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfc30-125">-SubscriptionId</span></span>
<span data-ttu-id="bfc30-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc30-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bfc30-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="bfc30-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bfc30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc30-128">CommonParameters</span></span>
<span data-ttu-id="bfc30-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc30-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfc30-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc30-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfc30-131">INPUTS</span></span>

## <span data-ttu-id="bfc30-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfc30-132">OUTPUTS</span></span>

### <span data-ttu-id="bfc30-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bfc30-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="bfc30-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfc30-134">NOTES</span></span>

<span data-ttu-id="bfc30-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bfc30-135">ALIASES</span></span>

## <span data-ttu-id="bfc30-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc30-136">RELATED LINKS</span></span>

