---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430130"
---
# <span data-ttu-id="a7ecc-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a7ecc-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="a7ecc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ecc-103">A operação para obter a extensão.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-103">The operation to get the extension.</span></span>

## <span data-ttu-id="a7ecc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7ecc-104">SYNTAX</span></span>

### <span data-ttu-id="a7ecc-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7ecc-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7ecc-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a7ecc-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a7ecc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7ecc-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ecc-108">A operação para obter a extensão.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-108">The operation to get the extension.</span></span>

## <span data-ttu-id="a7ecc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7ecc-109">EXAMPLES</span></span>

### <span data-ttu-id="a7ecc-110">Exemplo 1: listar todas as extensões de um computador</span><span class="sxs-lookup"><span data-stu-id="a7ecc-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="a7ecc-111">Lista todas as extensões de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="a7ecc-112">Exemplo 2: obter uma extensão específica em um computador</span><span class="sxs-lookup"><span data-stu-id="a7ecc-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="a7ecc-113">Obtém uma extensão específica em um computador.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="a7ecc-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="a7ecc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ecc-115">-DefaultProfile</span></span>
<span data-ttu-id="a7ecc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ecc-117">-Expandir</span><span class="sxs-lookup"><span data-stu-id="a7ecc-117">-Expand</span></span>
<span data-ttu-id="a7ecc-118">A expressão de expansão a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="a7ecc-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="a7ecc-119">-MachineName</span></span>
<span data-ttu-id="a7ecc-120">O nome da máquina que contém a extensão.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="a7ecc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7ecc-121">-Name</span></span>
<span data-ttu-id="a7ecc-122">O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="a7ecc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ecc-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7ecc-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7ecc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7ecc-125">-SubscriptionId</span></span>
<span data-ttu-id="a7ecc-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a7ecc-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a7ecc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ecc-128">CommonParameters</span></span>
<span data-ttu-id="a7ecc-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ecc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ecc-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7ecc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ecc-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7ecc-131">INPUTS</span></span>

## <span data-ttu-id="a7ecc-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7ecc-132">OUTPUTS</span></span>

### <span data-ttu-id="a7ecc-133">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a7ecc-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="a7ecc-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7ecc-134">NOTES</span></span>

<span data-ttu-id="a7ecc-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a7ecc-135">ALIASES</span></span>

## <span data-ttu-id="a7ecc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7ecc-136">RELATED LINKS</span></span>

