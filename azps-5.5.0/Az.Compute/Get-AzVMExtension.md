---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117860"
---
# <span data-ttu-id="55642-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="55642-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="55642-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55642-102">SYNOPSIS</span></span>
<span data-ttu-id="55642-103">Obtém propriedades das Extensões de Máquina Virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55642-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="55642-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55642-104">SYNTAX</span></span>

### <span data-ttu-id="55642-105">GetExtensionParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55642-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55642-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="55642-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55642-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55642-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55642-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="55642-108">DESCRIPTION</span></span>
<span data-ttu-id="55642-109">O **cmdlet Get-AzVMExtension** obtém propriedades de Extensões de Máquina Virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55642-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="55642-110">Especifique o nome de uma extensão para a qual obter propriedades.</span><span class="sxs-lookup"><span data-stu-id="55642-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="55642-111">Para obter apenas a exibição de instância de uma extensão, especifique o parâmetro Status.</span><span class="sxs-lookup"><span data-stu-id="55642-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="55642-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55642-112">EXAMPLES</span></span>

### <span data-ttu-id="55642-113">Exemplo 1: Obter propriedades de uma extensão</span><span class="sxs-lookup"><span data-stu-id="55642-113">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="55642-114">Esse comando obtém propriedades para a extensão chamada CustomScriptExtension na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="55642-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="55642-115">Exemplo 2: Obter a exibição de instância de uma extensão</span><span class="sxs-lookup"><span data-stu-id="55642-115">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="55642-116">Esse comando obtém a exibição de instância da extensão chamada CustomScriptExtension na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="55642-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="55642-117">Exemplo 3: Instalar todas as extensões em um VM</span><span class="sxs-lookup"><span data-stu-id="55642-117">Example 3: Get all extensions installed on a VM</span></span>
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

### <span data-ttu-id="55642-118">Exemplo 4: Obter propriedades de uma extensão usando o parâmetro VM</span><span class="sxs-lookup"><span data-stu-id="55642-118">Example 4: Get properties of an extension using the VM parameter</span></span>
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

<span data-ttu-id="55642-119">Esse comando obtém a lista de extensões instalada na máquina virtual chamada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="55642-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="55642-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55642-120">PARAMETERS</span></span>

### <span data-ttu-id="55642-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55642-121">-DefaultProfile</span></span>
<span data-ttu-id="55642-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="55642-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55642-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="55642-123">-Name</span></span>
<span data-ttu-id="55642-124">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="55642-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="55642-125">Este cmdlet obtém propriedades para a extensão especificada por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="55642-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="55642-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55642-126">-ResourceGroupName</span></span>
<span data-ttu-id="55642-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55642-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="55642-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55642-128">-ResourceId</span></span>
<span data-ttu-id="55642-129">ID do Recurso especificando o objeto de máquina virtual em que a extensão está.</span><span class="sxs-lookup"><span data-stu-id="55642-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="55642-130">-Status</span><span class="sxs-lookup"><span data-stu-id="55642-130">-Status</span></span>
<span data-ttu-id="55642-131">Indica que esse cmdlet obtém apenas a exibição de instância de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="55642-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="55642-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="55642-132">-VMName</span></span>
<span data-ttu-id="55642-133">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="55642-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="55642-134">Este cmdlet obtém propriedades de uma extensão da máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="55642-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="55642-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="55642-135">-VMObject</span></span>
<span data-ttu-id="55642-136">Especifica o objeto de máquina virtual em que a extensão está.</span><span class="sxs-lookup"><span data-stu-id="55642-136">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="55642-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55642-137">CommonParameters</span></span>
<span data-ttu-id="55642-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55642-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55642-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55642-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55642-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="55642-140">INPUTS</span></span>

### <span data-ttu-id="55642-141">System.String</span><span class="sxs-lookup"><span data-stu-id="55642-141">System.String</span></span>

### <span data-ttu-id="55642-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55642-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55642-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="55642-143">OUTPUTS</span></span>

### <span data-ttu-id="55642-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="55642-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="55642-145">Notas</span><span class="sxs-lookup"><span data-stu-id="55642-145">NOTES</span></span>

## <span data-ttu-id="55642-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55642-146">RELATED LINKS</span></span>

[<span data-ttu-id="55642-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="55642-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="55642-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="55642-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


