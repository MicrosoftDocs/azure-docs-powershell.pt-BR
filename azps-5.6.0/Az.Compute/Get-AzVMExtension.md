---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 33be258858a6ace456b7aa3c5b25594a373ccfd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893381"
---
# <span data-ttu-id="ec841-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ec841-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="ec841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec841-102">SYNOPSIS</span></span>
<span data-ttu-id="ec841-103">Obtém propriedades de Extensões de Máquina Virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec841-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="ec841-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec841-104">SYNTAX</span></span>

### <span data-ttu-id="ec841-105">GetExtensionParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec841-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec841-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec841-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec841-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec841-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec841-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec841-108">DESCRIPTION</span></span>
<span data-ttu-id="ec841-109">O cmdlet **Get-AzVMExtension** obtém propriedades de Extensões de Máquina Virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec841-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="ec841-110">Especifique o nome de uma extensão para a qual obter propriedades.</span><span class="sxs-lookup"><span data-stu-id="ec841-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="ec841-111">Para obter apenas a exibição de instância de uma extensão, especifique o parâmetro Status.</span><span class="sxs-lookup"><span data-stu-id="ec841-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="ec841-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec841-112">EXAMPLES</span></span>

### <span data-ttu-id="ec841-113">Exemplo 1: Obter propriedades de uma extensão</span><span class="sxs-lookup"><span data-stu-id="ec841-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="ec841-114">Este comando obtém propriedades para a extensão chamada CustomScriptExtension na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec841-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="ec841-115">Exemplo 2: Obter exibição de instância de uma extensão</span><span class="sxs-lookup"><span data-stu-id="ec841-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="ec841-116">Este comando obtém a exibição de instância para a extensão chamada CustomScriptExtension na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec841-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="ec841-117">Exemplo 3: Obter todas as extensões instaladas em uma VM</span><span class="sxs-lookup"><span data-stu-id="ec841-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="ec841-118">Exemplo 4: Obter propriedades de uma extensão usando o parâmetro VM</span><span class="sxs-lookup"><span data-stu-id="ec841-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="ec841-119">Este comando obtém a lista de extensões instaladas na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec841-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ec841-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec841-120">PARAMETERS</span></span>

### <span data-ttu-id="ec841-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec841-121">-DefaultProfile</span></span>
<span data-ttu-id="ec841-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ec841-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ec841-123">-Name</span></span>
<span data-ttu-id="ec841-124">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="ec841-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="ec841-125">Este cmdlet obtém propriedades para a extensão especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec841-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec841-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec841-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec841-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec841-128">-ResourceId</span></span>
<span data-ttu-id="ec841-129">ID do recurso especificando o objeto da máquina virtual em que a extensão está.</span><span class="sxs-lookup"><span data-stu-id="ec841-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-130">-Status</span><span class="sxs-lookup"><span data-stu-id="ec841-130">-Status</span></span>
<span data-ttu-id="ec841-131">Indica que esse cmdlet obtém apenas a exibição de instância de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="ec841-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="ec841-132">-VMName</span></span>
<span data-ttu-id="ec841-133">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec841-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ec841-134">Este cmdlet obtém propriedades de uma extensão da máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec841-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="ec841-135">-VMObject</span></span>
<span data-ttu-id="ec841-136">Especifica o objeto da máquina virtual em que a extensão está.</span><span class="sxs-lookup"><span data-stu-id="ec841-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec841-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec841-137">CommonParameters</span></span>
<span data-ttu-id="ec841-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec841-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec841-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec841-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec841-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec841-140">INPUTS</span></span>

### <span data-ttu-id="ec841-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ec841-141">System.String</span></span>

### <span data-ttu-id="ec841-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec841-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec841-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec841-143">OUTPUTS</span></span>

### <span data-ttu-id="ec841-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ec841-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="ec841-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec841-145">NOTES</span></span>

## <span data-ttu-id="ec841-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec841-146">RELATED LINKS</span></span>

[<span data-ttu-id="ec841-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ec841-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="ec841-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ec841-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


