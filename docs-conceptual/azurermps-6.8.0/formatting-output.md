---
title: Formatar saída de cmdlet do Azure PowerShell
description: Como formatar a saída de cmdlet do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 833c82903305f99be5ad43f707e22644bb568abe
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117596"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="9b7a2-103">Formatar saída de cmdlet do AzurePowerShell</span><span class="sxs-lookup"><span data-stu-id="9b7a2-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="9b7a2-104">Por padrão, cada cmdlet do Azure PowerShell tem formatação predefinida de saída, facilitando a leitura.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="9b7a2-105">O PowerShell também oferece a flexibilidade para ajustar a saída ou converter a saída do cmdlet em um formato diferente com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="9b7a2-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="9b7a2-106">Formatação</span><span class="sxs-lookup"><span data-stu-id="9b7a2-106">Formatting</span></span>      | <span data-ttu-id="9b7a2-107">Conversão</span><span class="sxs-lookup"><span data-stu-id="9b7a2-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="9b7a2-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="9b7a2-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="9b7a2-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="9b7a2-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="9b7a2-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="9b7a2-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="9b7a2-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="9b7a2-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="9b7a2-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="9b7a2-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="9b7a2-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="9b7a2-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="9b7a2-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="9b7a2-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="9b7a2-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="9b7a2-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="9b7a2-116">Exemplos de formato</span><span class="sxs-lookup"><span data-stu-id="9b7a2-116">Format examples</span></span>

<span data-ttu-id="9b7a2-117">Neste exemplo, obtemos uma lista de máquinas virtuais do Azure em nossa assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-117">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="9b7a2-118">O comando `Get-AzureRmVM` tem como saída padrão um formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="9b7a2-119">Se você quiser limitar as colunas retornadas, use o cmdlet `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="9b7a2-120">No exemplo a seguir, vamos obter a mesma lista de máquinas virtuais mas restringir a saída ao nome da VM, ao grupo de recursos e ao local da VM.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-120">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="9b7a2-121">O parâmetro `-Autosize` dimensiona as colunas de acordo com o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="9b7a2-122">A saída também pode ser formatada em uma lista.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="9b7a2-123">O exemplo a seguir mostra isso usando o cmdlet `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="9b7a2-124">Converter para outros tipos de dados</span><span class="sxs-lookup"><span data-stu-id="9b7a2-124">Convert to other data types</span></span>

<span data-ttu-id="9b7a2-125">O PowerShell também permite colocar a saída do comando e convertê-la em vários formatos de dados.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="9b7a2-126">No exemplo a seguir, o cmdlet `Select-Object` é usado para obter os atributos das máquinas virtuais em nossa assinatura e converter a saída em formato CSV para simplificar a importação para um banco de dados ou uma planilha.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-126">In the following example the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="9b7a2-127">A saída também pode ser convertida no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="9b7a2-128">O exemplo a seguir cria a mesma lista de VMs, mas altera o formato de saída para JSON.</span><span class="sxs-lookup"><span data-stu-id="9b7a2-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
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
