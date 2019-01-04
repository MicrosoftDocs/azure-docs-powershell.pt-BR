---
title: Consultar a saída de cmdlets do Azure PowerShell
description: Como consultar recursos no Azure e formatar os resultados.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: fd0135f981452a2425f4dc8b9c9708d4907eff2a
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594631"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="af0a1-103">Consultar a saída de cmdlets do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="af0a1-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="af0a1-104">A consulta no PowerShell pode ser concluída usando cmdlets internos.</span><span class="sxs-lookup"><span data-stu-id="af0a1-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="af0a1-105">No PowerShell, os nomes de cmdlet assumem a forma de  **_Verbo-Substantivo_**.</span><span class="sxs-lookup"><span data-stu-id="af0a1-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="af0a1-106">Os cmdlets que usam o verbo **_Get_** são os cmdlets de consulta.</span><span class="sxs-lookup"><span data-stu-id="af0a1-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="af0a1-107">Os substantivos do cmdlet são os tipos de recursos do Azure que são influenciados pelos verbos do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af0a1-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="af0a1-108">Selecionar propriedades simples</span><span class="sxs-lookup"><span data-stu-id="af0a1-108">Select simple properties</span></span>

<span data-ttu-id="af0a1-109">O Azure PowerShell tem formatação padrão definidos para cada cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af0a1-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="af0a1-110">As propriedades mais comuns para cada tipo de recurso são automaticamente exibidas em um formato de tabela ou de lista.</span><span class="sxs-lookup"><span data-stu-id="af0a1-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="af0a1-111">Para saber mais sobre formatação de saída, veja [Formatação de resultados da consulta](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="af0a1-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="af0a1-112">Use o cmdlet `Get-AzVM` para consultar uma lista de máquinas virtuais em sua conta.</span><span class="sxs-lookup"><span data-stu-id="af0a1-112">Use the `Get-AzVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzVM
```

<span data-ttu-id="af0a1-113">A saída padrão é formatada automaticamente como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="af0a1-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="af0a1-114">O cmdlet `Select-Object` pode ser usado para selecionar as propriedades específicas que são interessantes para você.</span><span class="sxs-lookup"><span data-stu-id="af0a1-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="af0a1-115">Selecionar propriedades aninhadas complexas</span><span class="sxs-lookup"><span data-stu-id="af0a1-115">Select complex nested properties</span></span>

<span data-ttu-id="af0a1-116">Se a propriedade que você deseja estiver aninhada na saída JSON, será necessário fornecer o caminho completo para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="af0a1-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="af0a1-117">O exemplo a seguir mostra como selecionar o nome da VM e o tipo do SO do cmdlet `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="af0a1-117">The following example shows how to select the VM Name and the OS type from the `Get-AzVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="af0a1-118">Filtrar resultados com o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="af0a1-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="af0a1-119">O cmdlet `Where-Object` permite filtrar o resultados com base em qualquer valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="af0a1-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="af0a1-120">No exemplo a seguir, o filtro seleciona apenas as VMs com o texto "RGD" em seu nome.</span><span class="sxs-lookup"><span data-stu-id="af0a1-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="af0a1-121">Com o exemplo a seguir, os resultados retornarão as VMs com o vmSize 'Standard_DS1_V2'.</span><span class="sxs-lookup"><span data-stu-id="af0a1-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```