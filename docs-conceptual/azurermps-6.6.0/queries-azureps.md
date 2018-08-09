---
title: Consultar a saída de cmdlets do Azure PowerShell
description: Como consultar recursos no Azure e formatar os resultados.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: daa39ada5b4e969264b6e8596dc7b090bb196fd5
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653620"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="cb03e-103">Consultar a saída de cmdlets do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb03e-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="cb03e-104">A consulta no PowerShell pode ser concluída usando cmdlets internos.</span><span class="sxs-lookup"><span data-stu-id="cb03e-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="cb03e-105">No PowerShell, os nomes de cmdlet assumem a forma de  **_Verbo-Substantivo_**.</span><span class="sxs-lookup"><span data-stu-id="cb03e-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="cb03e-106">Os cmdlets que usam o verbo **_Get_** são os cmdlets de consulta.</span><span class="sxs-lookup"><span data-stu-id="cb03e-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="cb03e-107">Os substantivos do cmdlet são os tipos de recursos do Azure que são influenciados pelos verbos do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb03e-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="cb03e-108">Selecionar propriedades simples</span><span class="sxs-lookup"><span data-stu-id="cb03e-108">Select simple properties</span></span>

<span data-ttu-id="cb03e-109">O Azure PowerShell tem formatação padrão definidos para cada cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb03e-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="cb03e-110">As propriedades mais comuns para cada tipo de recurso são automaticamente exibidas em um formato de tabela ou de lista.</span><span class="sxs-lookup"><span data-stu-id="cb03e-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="cb03e-111">Para saber mais sobre formatação de saída, veja [Formatação de resultados da consulta](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="cb03e-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="cb03e-112">Use o cmdlet `Get-AzureRmVM` para consultar uma lista de máquinas virtuais em sua conta.</span><span class="sxs-lookup"><span data-stu-id="cb03e-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="cb03e-113">A saída padrão é formatada automaticamente como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="cb03e-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="cb03e-114">O cmdlet `Select-Object` pode ser usado para selecionar as propriedades específicas que são interessantes para você.</span><span class="sxs-lookup"><span data-stu-id="cb03e-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="cb03e-115">Selecionar propriedades aninhadas complexas</span><span class="sxs-lookup"><span data-stu-id="cb03e-115">Select complex nested properties</span></span>

<span data-ttu-id="cb03e-116">Se a propriedade que você deseja selecionar estiver aninhada profundamente na saída JSON, será necessário fornecer o caminho completo para a propriedade aninhada.</span><span class="sxs-lookup"><span data-stu-id="cb03e-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="cb03e-117">O exemplo a seguir mostra como selecionar o nome da VM e o tipo do SO do cmdlet `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="cb03e-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="cb03e-118">Filtrar resultados com o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="cb03e-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="cb03e-119">O cmdlet `Where-Object` permite filtrar o resultados com base em qualquer valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="cb03e-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="cb03e-120">No exemplo a seguir, o filtro seleciona apenas as VMs com o texto "RGD" em seu nome.</span><span class="sxs-lookup"><span data-stu-id="cb03e-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="cb03e-121">Com o exemplo a seguir, os resultados retornarão as VMs com o vmSize 'Standard_DS1_V2'.</span><span class="sxs-lookup"><span data-stu-id="cb03e-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```