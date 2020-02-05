---
title: Consultar a saída de cmdlets do Azure PowerShell
description: Como consultar recursos no Azure e formatar os resultados.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002768"
---
# <a name="query-output-of-azure-powershell"></a>Consultar a saída do Azure PowerShell 

Os resultados de cada cmdlet do Azure PowerShell são um objeto do Azure PowerShell. Mesmo cmdlets que não são explicitamente operações `Get-` podem retornar um valor que pode ser inspecionado para fornecer informações sobre um recurso que foi criado ou modificado. Embora a maioria dos cmdlets retorne um objeto único, alguns retornam uma matriz que deve ser iterada.

Em quase todos os casos, você consulta a saída do Azure PowerShell com o cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), muitas vezes abreviado como `select`. A saída pode ser filtrada com [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) ou seu alias `where`.

## <a name="select-simple-properties"></a>Selecionar propriedades simples

No formato de tabela padrão, os cmdlets do Azure PowerShell não exibem todas as suas propriedades disponíveis. Você pode obter todas as propriedades usando o cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list) ou redirecionando a saída para `Select-Object *`:

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

Assim que souber os nomes das propriedades nas quais está interessado, você pode usar esses nomes de propriedade com `Select-Object` para obtê-los diretamente:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

A saída ao usar o `Select-Object` sempre é formatada para exibir as informações solicitadas. Para saber mais sobre como usar a formatação como parte da consulta de resultados do cmdlet, confira [Formatar saída de cmdlet do Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Selecionar propriedades aninhadas

Algumas propriedades na saída do cmdlet do Azure PowerShell usam objetos aninhados, como a propriedade `StorageProfile` da saída `Get-AzVM`. Para obter um valor de uma propriedade aninhada, forneça um nome de exibição e o caminho completo para o valor que você deseja inspecionar como parte de um argumento de dicionário para `Select-Object`:

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

Cada argumento de dicionário seleciona uma propriedade do objeto. A propriedade a ser extraída deve ser parte de uma expressão.

## <a name="filter-results"></a>Resultados do filtro 

O cmdlet `Where-Object` permite filtrar os resultados com base em qualquer valor de propriedade, incluindo propriedades aninhadas. O próximo exemplo mostra como usar o `Where-Object` para localizar as VMs do Linux em um grupo de recursos.

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

É possível redirecionar os resultados de `Select-Object` e `Where-Object` entre si. Para fins de desempenho, sempre é recomendável colocar a operação `Where-Object` antes de `Select-Object`:

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