---
title: Consultar a saída de cmdlets do Azure PowerShell
description: Como consultar recursos no Azure e formatar os resultados.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 664829721843020745cf24a913e1d09a4e68a3da
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243677"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Consultar a saída de cmdlets do Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

A consulta no PowerShell pode ser concluída usando cmdlets internos. No PowerShell, os nomes de cmdlet assumem a forma de **_Verbo-Substantivo_**. Os cmdlets que usam o verbo **_Get_** são os cmdlets de consulta. Os substantivos do cmdlet são os tipos de recursos do Azure que são influenciados pelos verbos do cmdlet.

## <a name="select-simple-properties"></a>Selecionar propriedades simples

O Azure PowerShell tem formatação padrão definidos para cada cmdlet. As propriedades mais comuns para cada tipo de recurso são automaticamente exibidas em um formato de tabela ou de lista. Para saber mais sobre formatação de saída, veja [Formatação de resultados da consulta](formatting-output.md).

Use o cmdlet `Get-AzureRmVM` para consultar uma lista de máquinas virtuais em sua conta.

```azurepowershell-interactive
Get-AzureRmVM
```

A saída padrão é formatada automaticamente como uma tabela.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

O cmdlet `Select-Object` pode ser usado para selecionar as propriedades específicas que são interessantes para você.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Selecionar propriedades aninhadas complexas

Se a propriedade que você deseja selecionar estiver aninhada profundamente na saída JSON, será necessário fornecer o caminho completo para a propriedade aninhada. O exemplo a seguir mostra como selecionar o nome da VM e o tipo do SO do cmdlet `Get-AzureRmVM`.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Filtrar resultados com o cmdlet Where-Object

O cmdlet `Where-Object` permite filtrar o resultados com base em qualquer valor de propriedade. No exemplo a seguir, o filtro seleciona apenas as VMs com o texto "RGD" em seu nome.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Com o exemplo a seguir, os resultados retornarão as VMs com o vmSize 'Standard_DS1_V2'.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
