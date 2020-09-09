---
title: Consultar a saída de cmdlets do Azure PowerShell
description: Como consultar recursos no Azure e formatar os resultados.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2754df5132ca9d528217fa5caad95b7f59cc8215
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240889"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="72eb7-103">Consultar a saída do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="72eb7-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="72eb7-104">Os resultados de cada cmdlet do Azure PowerShell são um objeto do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72eb7-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="72eb7-105">Mesmo cmdlets que não são explicitamente operações `Get-` podem retornar um valor que pode ser inspecionado para fornecer informações sobre um recurso que foi criado ou modificado.</span><span class="sxs-lookup"><span data-stu-id="72eb7-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="72eb7-106">Embora a maioria dos cmdlets retorne um objeto único, alguns retornam uma matriz que deve ser iterada.</span><span class="sxs-lookup"><span data-stu-id="72eb7-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="72eb7-107">Em quase todos os casos, você consulta a saída do Azure PowerShell com o cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), muitas vezes abreviado como `select`.</span><span class="sxs-lookup"><span data-stu-id="72eb7-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="72eb7-108">A saída pode ser filtrada com [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) ou seu alias `where`.</span><span class="sxs-lookup"><span data-stu-id="72eb7-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="72eb7-109">Selecionar propriedades simples</span><span class="sxs-lookup"><span data-stu-id="72eb7-109">Select simple properties</span></span>

<span data-ttu-id="72eb7-110">No formato de tabela padrão, os cmdlets do Azure PowerShell não exibem todas as suas propriedades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="72eb7-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="72eb7-111">Você pode obter todas as propriedades usando o cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) ou redirecionando a saída para `Select-Object *`:</span><span class="sxs-lookup"><span data-stu-id="72eb7-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="72eb7-112">Assim que souber os nomes das propriedades nas quais está interessado, você pode usar esses nomes de propriedade com `Select-Object` para obtê-los diretamente:</span><span class="sxs-lookup"><span data-stu-id="72eb7-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="72eb7-113">A saída ao usar o `Select-Object` sempre é formatada para exibir as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="72eb7-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="72eb7-114">Para saber mais sobre como usar a formatação como parte da consulta de resultados do cmdlet, confira [Formatar saída de cmdlet do Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="72eb7-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="72eb7-115">Selecionar propriedades aninhadas</span><span class="sxs-lookup"><span data-stu-id="72eb7-115">Select nested properties</span></span>

<span data-ttu-id="72eb7-116">Algumas propriedades na saída do cmdlet do Azure PowerShell usam objetos aninhados, como a propriedade `StorageProfile` da saída `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="72eb7-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="72eb7-117">Para obter um valor de uma propriedade aninhada, forneça um nome de exibição e o caminho completo para o valor que você deseja inspecionar como parte de um argumento de dicionário para `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="72eb7-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="72eb7-118">Cada argumento de dicionário seleciona uma propriedade do objeto.</span><span class="sxs-lookup"><span data-stu-id="72eb7-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="72eb7-119">A propriedade a ser extraída deve ser parte de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="72eb7-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="72eb7-120">Resultados do filtro</span><span class="sxs-lookup"><span data-stu-id="72eb7-120">Filter results</span></span> 

<span data-ttu-id="72eb7-121">O cmdlet `Where-Object` permite filtrar os resultados com base em qualquer valor de propriedade, incluindo propriedades aninhadas.</span><span class="sxs-lookup"><span data-stu-id="72eb7-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="72eb7-122">O próximo exemplo mostra como usar o `Where-Object` para localizar as VMs do Linux em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="72eb7-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="72eb7-123">É possível redirecionar os resultados de `Select-Object` e `Where-Object` entre si.</span><span class="sxs-lookup"><span data-stu-id="72eb7-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="72eb7-124">Para fins de desempenho, sempre é recomendável colocar a operação `Where-Object` antes de `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="72eb7-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
