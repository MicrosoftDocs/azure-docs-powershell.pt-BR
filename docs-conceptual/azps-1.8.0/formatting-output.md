---
title: Formatar saída de cmdlet do Azure PowerShell
description: Como formatar a saída de cmdlet do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: e5c9a9df830f6d866d171107472ff94166442be9
ms.sourcegitcommit: 1b3de64d816c8c7116ddd4ca8cef2cfbaddb472f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65729686"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="01155-103">Formatar saída de cmdlet do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="01155-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="01155-104">Por padrão, cada cmdlet do Azure PowerShell formata a saída para ser fácil de ler.</span><span class="sxs-lookup"><span data-stu-id="01155-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="01155-105">O PowerShell permite converter ou formater a saída do cmdlet através do redirecionamento para um dos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="01155-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="01155-106">Formatação</span><span class="sxs-lookup"><span data-stu-id="01155-106">Formatting</span></span>      | <span data-ttu-id="01155-107">Conversão</span><span class="sxs-lookup"><span data-stu-id="01155-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="01155-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="01155-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="01155-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="01155-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="01155-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="01155-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="01155-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="01155-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="01155-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="01155-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="01155-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="01155-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="01155-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="01155-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="01155-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="01155-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="01155-116">A formatação é usada para a exibição em um terminal do PowerShell e a conversão é usada para gerar dados a serem consumidos por outros scripts ou programas.</span><span class="sxs-lookup"><span data-stu-id="01155-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="01155-117">Formato de saída da tabela</span><span class="sxs-lookup"><span data-stu-id="01155-117">Table output format</span></span>

<span data-ttu-id="01155-118">Por padrão, os cmdlets do Azure PowerShell são produzidos no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="01155-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="01155-119">Esse formato não exibe todas as informações do recurso solicitado:</span><span class="sxs-lookup"><span data-stu-id="01155-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="01155-120">A quantidade de dados exibidos por `Format-Table` pode ser afetada pela largura da janela da sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01155-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="01155-121">Para restringir a saída às propriedades específicas e ordená-las, os nomes da propriedade podem ser fornecidos como argumentos para `Format-Table`:</span><span class="sxs-lookup"><span data-stu-id="01155-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="01155-122">Formato de saída de lista</span><span class="sxs-lookup"><span data-stu-id="01155-122">List output format</span></span>

<span data-ttu-id="01155-123">O formato de saída de lista gera duas colunas e os nomes da propriedade são seguidos pelo valor.</span><span class="sxs-lookup"><span data-stu-id="01155-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="01155-124">Para os objetos complexos, o tipo do objeto é exibido.</span><span class="sxs-lookup"><span data-stu-id="01155-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="01155-125">A saída a seguir tem alguns campos removidos.</span><span class="sxs-lookup"><span data-stu-id="01155-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="01155-126">Como `Format-Table`, os nomes da propriedade podem ser fornecidos para ordenar e restringir a saída:</span><span class="sxs-lookup"><span data-stu-id="01155-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="01155-127">Formato de saída largo</span><span class="sxs-lookup"><span data-stu-id="01155-127">Wide output format</span></span>

<span data-ttu-id="01155-128">O formato de saída largo produz apenas um nome da propriedade por consulta.</span><span class="sxs-lookup"><span data-stu-id="01155-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="01155-129">A propriedade exibida pode ser controlada fornecendo-se uma propriedade como argumento.</span><span class="sxs-lookup"><span data-stu-id="01155-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="01155-130">Formato de saída personalizado</span><span class="sxs-lookup"><span data-stu-id="01155-130">Custom output format</span></span>

<span data-ttu-id="01155-131">O tipo de saída `Custom-Format` destina-se a formatar objetos personalizados.</span><span class="sxs-lookup"><span data-stu-id="01155-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="01155-132">Sem nenhum argumento, ele se comporta como `Format-List`, mas exibe os nomes da propriedade das classes personalizadas.</span><span class="sxs-lookup"><span data-stu-id="01155-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="01155-133">A saída a seguir tem alguns campos removidos.</span><span class="sxs-lookup"><span data-stu-id="01155-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="01155-134">Fornecer nomes de propriedade como argumentos para `Custom-Format` exibe os pares de propriedade/valor para objetos personalizados definidos como valores:</span><span class="sxs-lookup"><span data-stu-id="01155-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="01155-135">A saída a seguir tem alguns campos removidos.</span><span class="sxs-lookup"><span data-stu-id="01155-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="01155-136">Conversão para outros formatos de dados</span><span class="sxs-lookup"><span data-stu-id="01155-136">Conversion to other data formats</span></span>

<span data-ttu-id="01155-137">A família de cmdlets `ConvertTo-*` permite converter os resultados dos cmdlets do Azure PowerShell em formatos legíveis por máquina.</span><span class="sxs-lookup"><span data-stu-id="01155-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="01155-138">Para obter apenas algumas propriedades dos resultados do Azure PowerShell, use o comando `Select-Object` em um pipe antes de fazer a conversão.</span><span class="sxs-lookup"><span data-stu-id="01155-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="01155-139">Os exemplos a seguir demonstram os diferentes tipos de saída que cada conversão produz.</span><span class="sxs-lookup"><span data-stu-id="01155-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="01155-140">Conversão para CSV</span><span class="sxs-lookup"><span data-stu-id="01155-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="01155-141">Conversão para JSON</span><span class="sxs-lookup"><span data-stu-id="01155-141">Conversion to JSON</span></span>

<span data-ttu-id="01155-142">A saída JSON não expande todas as propriedades por padrão.</span><span class="sxs-lookup"><span data-stu-id="01155-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="01155-143">Para alterar a profundidade das propriedades expandidas, use o argumento `-Depth`.</span><span class="sxs-lookup"><span data-stu-id="01155-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="01155-144">Por padrão, a profundidade de expansão é `2`.</span><span class="sxs-lookup"><span data-stu-id="01155-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="01155-145">A saída a seguir tem alguns campos removidos.</span><span class="sxs-lookup"><span data-stu-id="01155-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="01155-146">Conversão para XML</span><span class="sxs-lookup"><span data-stu-id="01155-146">Conversion to XML</span></span>

<span data-ttu-id="01155-147">O cmdlet `ConvertTo-XML` converte o objeto de resposta do Azure PowerShell em um objeto XML puro, que pode ser tratado como qualquer outro objeto XML dentro do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01155-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="01155-148">Conversão para HTML</span><span class="sxs-lookup"><span data-stu-id="01155-148">Conversion to HTML</span></span>

<span data-ttu-id="01155-149">Converter um objeto para HTML produz uma saída que será apresentada como uma tabela HTML.</span><span class="sxs-lookup"><span data-stu-id="01155-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="01155-150">A renderização do HTML dependerá do comportamento do navegador para renderizar as tabelas que não têm nenhuma informação da largura.</span><span class="sxs-lookup"><span data-stu-id="01155-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="01155-151">Nenhum objeto de classe personalizada é expandido.</span><span class="sxs-lookup"><span data-stu-id="01155-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
