---
title: Formatação de resultados da consulta | Microsoft Docs
description: Como consultar recursos no Azure e formatar os resultados.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9cef703f302651a48381dba70c0be23d4d24df0b
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820860"
---
# <a name="formatting-query-results"></a><span data-ttu-id="4700a-103">Formatação de resultados da consulta</span><span class="sxs-lookup"><span data-stu-id="4700a-103">Formatting query results</span></span>

<span data-ttu-id="4700a-104">Por padrão, cada cmdlet do PowerShell tem formatação predefinida de saída, facilitando a leitura.</span><span class="sxs-lookup"><span data-stu-id="4700a-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="4700a-105">O PowerShell também oferece a flexibilidade para ajustar a saída ou converter a saída do cmdlet em um formato diferente com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4700a-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="4700a-106">Formatação</span><span class="sxs-lookup"><span data-stu-id="4700a-106">Formatting</span></span>      | <span data-ttu-id="4700a-107">Conversão</span><span class="sxs-lookup"><span data-stu-id="4700a-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="4700a-108">Exemplos de formatação</span><span class="sxs-lookup"><span data-stu-id="4700a-108">Formatting examples</span></span>

<span data-ttu-id="4700a-109">Neste exemplo, obtemos uma lista de máquinas virtuais do Azure em nossa assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="4700a-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="4700a-110">O comando Get-AzureRmVM tem como saída padrão um formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="4700a-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="4700a-111">Se você quiser limitar as colunas retornadas, use o cmdlet `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="4700a-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="4700a-112">No exemplo a seguir, vamos obter a mesma lista de máquinas virtuais mas restringir a saída ao nome da VM, ao grupo de recursos e ao local da VM.</span><span class="sxs-lookup"><span data-stu-id="4700a-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="4700a-113">O parâmetro `-Autosize` dimensiona as colunas de acordo com o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="4700a-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="4700a-114">Se você preferir, poderá exibir as informações em um formato de lista.</span><span class="sxs-lookup"><span data-stu-id="4700a-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="4700a-115">O exemplo a seguir mostra isso usando o cmdlet `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="4700a-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="4700a-116">Conversão em outros tipos de dados</span><span class="sxs-lookup"><span data-stu-id="4700a-116">Converting to other data types</span></span>

<span data-ttu-id="4700a-117">O PowerShell também oferece vários formatos de saída que você pode usar para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="4700a-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="4700a-118">No exemplo a seguir, podemos usar o cmdlet `Select-Object` para obter os atributos das máquinas virtuais na nossa assinatura e converter a saída em formato CSV para simplificar a importação para um banco de dados ou uma planilha.</span><span class="sxs-lookup"><span data-stu-id="4700a-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="4700a-119">Você também pode converter a saída em formato JSON.</span><span class="sxs-lookup"><span data-stu-id="4700a-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="4700a-120">O exemplo a seguir cria a mesma lista de VMs, mas altera o formato de saída para JSON.</span><span class="sxs-lookup"><span data-stu-id="4700a-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
