---
title: Consulta de recursos do Azure e formatação de resultados | Microsoft Docs
description: Como consultar recursos no Azure e formatar os resultados.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: eb359710efde6b5969ac721e395725a0ce87fddd
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024589"
---
# <a name="querying-for-azure-resources"></a>Consultar recursos do Azure

A consulta no PowerShell pode ser concluída usando cmdlets internos. No PowerShell, os nomes de cmdlet assumem a forma de  **_Verbo-Substantivo_**. Os cmdlets que usam o verbo **_Get_** são os cmdlets de consulta. Os substantivos do cmdlet são os tipos de recursos do Azure que são influenciados pelos verbos do cmdlet.

## <a name="selecting-simple-properties"></a>Seleção de propriedades simples

O Azure PowerShell tem formatação padrão definidos para cada cmdlet. As propriedades mais comuns para cada tipo de recurso são automaticamente exibidas em um formato de tabela ou de lista. Para saber mais sobre formatação de saída, veja [Formatação de resultados da consulta](formatting-output.md).

Use o cmdlet `Get-AzureRmVM` para consultar uma lista de máquinas virtuais em sua conta.

```powershell
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

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Seleção de propriedades aninhadas complexas

Se a propriedade que você deseja selecionar estiver aninhada profundamente na saída JSON, será necessário fornecer o caminho completo para a propriedade aninhada. O exemplo a seguir mostra como selecionar o nome da VM e o tipo do SO do cmdlet `Get-AzureRmVM`.

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Filtrar resultados usando o cmdlet Where-Object

O cmdlet `Where-Object` permite filtrar o resultados com base em qualquer valor de propriedade. No exemplo a seguir, o filtro seleciona apenas as VMs com o texto "RGD" em seu nome.

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Com o exemplo a seguir, os resultados retornarão as VMs com o vmSize 'Standard_DS1_V2'.

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
