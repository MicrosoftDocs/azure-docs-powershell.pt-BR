---
title: Consulta de recursos do Azure e formatação de resultados | Microsoft Docs
description: Como consultar recursos no Azure e formatar os resultados.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9a7627a25f9bbd196b1d615229e45a6e1ce7a7d9
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258393"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="df1e1-103">Consultar recursos do Azure</span><span class="sxs-lookup"><span data-stu-id="df1e1-103">Querying for Azure resources</span></span>

<span data-ttu-id="df1e1-104">A consulta no PowerShell pode ser concluída usando cmdlets internos.</span><span class="sxs-lookup"><span data-stu-id="df1e1-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="df1e1-105">No PowerShell, os nomes de cmdlet assumem a forma de  **_Verbo-Substantivo_**.</span><span class="sxs-lookup"><span data-stu-id="df1e1-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="df1e1-106">Os cmdlets que usam o verbo **_Get_** são os cmdlets de consulta.</span><span class="sxs-lookup"><span data-stu-id="df1e1-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="df1e1-107">Os substantivos do cmdlet são os tipos de recursos do Azure que são influenciados pelos verbos do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1e1-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="df1e1-108">Seleção de propriedades simples</span><span class="sxs-lookup"><span data-stu-id="df1e1-108">Selecting simple properties</span></span>

<span data-ttu-id="df1e1-109">O Azure PowerShell tem formatação padrão definidos para cada cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1e1-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="df1e1-110">As propriedades mais comuns para cada tipo de recurso são automaticamente exibidas em um formato de tabela ou de lista.</span><span class="sxs-lookup"><span data-stu-id="df1e1-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="df1e1-111">Para saber mais sobre formatação de saída, veja [Formatação de resultados da consulta](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="df1e1-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="df1e1-112">Use o cmdlet `Get-AzureRmVM` para consultar uma lista de máquinas virtuais em sua conta.</span><span class="sxs-lookup"><span data-stu-id="df1e1-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="df1e1-113">A saída padrão é formatada automaticamente como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="df1e1-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="df1e1-114">O cmdlet `Select-Object` pode ser usado para selecionar as propriedades específicas que são interessantes para você.</span><span class="sxs-lookup"><span data-stu-id="df1e1-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="df1e1-115">Seleção de propriedades aninhadas complexas</span><span class="sxs-lookup"><span data-stu-id="df1e1-115">Selecting complex nested properties</span></span>

<span data-ttu-id="df1e1-116">Se a propriedade que você deseja selecionar estiver aninhada profundamente na saída JSON, será necessário fornecer o caminho completo para a propriedade aninhada.</span><span class="sxs-lookup"><span data-stu-id="df1e1-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="df1e1-117">O exemplo a seguir mostra como selecionar o nome da VM e o tipo do SO do cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="df1e1-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="df1e1-118">Filtrar resultados usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="df1e1-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="df1e1-119">O cmdlet `Where-Object` permite filtrar o resultados com base em qualquer valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df1e1-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="df1e1-120">No exemplo a seguir, o filtro seleciona apenas as VMs com o texto "RGD" em seu nome.</span><span class="sxs-lookup"><span data-stu-id="df1e1-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="df1e1-121">Com o exemplo a seguir, os resultados retornarão as VMs com o vmSize 'Standard_DS1_V2'.</span><span class="sxs-lookup"><span data-stu-id="df1e1-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
