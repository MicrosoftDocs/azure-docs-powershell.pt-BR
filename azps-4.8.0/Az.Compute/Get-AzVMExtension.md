---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948419"
---
# <span data-ttu-id="02d8f-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="02d8f-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="02d8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="02d8f-103">Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02d8f-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="02d8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d8f-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="02d8f-106">O cmdlet **Get-AzVMExtension** Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02d8f-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="02d8f-107">Especifique o nome de uma extensão para a qual obter as propriedades.</span><span class="sxs-lookup"><span data-stu-id="02d8f-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="02d8f-108">Para obter apenas o modo de exibição de instância de uma extensão, especifique o parâmetro status.</span><span class="sxs-lookup"><span data-stu-id="02d8f-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="02d8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="02d8f-110">Exemplo 1: obter propriedades de uma extensão</span><span class="sxs-lookup"><span data-stu-id="02d8f-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="02d8f-111">Este comando obtém as propriedades da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="02d8f-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="02d8f-112">Exemplo 2: obter o modo de exibição de instância de uma extensão</span><span class="sxs-lookup"><span data-stu-id="02d8f-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="02d8f-113">Esse comando obtém o modo de exibição de instância da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="02d8f-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="02d8f-114">Exemplo 3: obter todas as extensões instaladas em uma VM</span><span class="sxs-lookup"><span data-stu-id="02d8f-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="02d8f-115">Este comando obtém a lista de extensões instaladas na máquina virtual nomeada VirtualMachine22 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02d8f-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="02d8f-116">OS</span><span class="sxs-lookup"><span data-stu-id="02d8f-116">PARAMETERS</span></span>

### <span data-ttu-id="02d8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d8f-117">-DefaultProfile</span></span>
<span data-ttu-id="02d8f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02d8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d8f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d8f-119">-Name</span></span>
<span data-ttu-id="02d8f-120">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="02d8f-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="02d8f-121">Esse cmdlet obtém as propriedades da extensão que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="02d8f-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="02d8f-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02d8f-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d8f-124">-Status</span><span class="sxs-lookup"><span data-stu-id="02d8f-124">-Status</span></span>
<span data-ttu-id="02d8f-125">Indica que esse cmdlet obtém apenas o modo de exibição de instância de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="02d8f-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="02d8f-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="02d8f-126">-VMName</span></span>
<span data-ttu-id="02d8f-127">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02d8f-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="02d8f-128">Esse cmdlet obtém as propriedades de uma extensão da máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="02d8f-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d8f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d8f-129">CommonParameters</span></span>
<span data-ttu-id="02d8f-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d8f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d8f-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02d8f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d8f-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d8f-132">INPUTS</span></span>

### <span data-ttu-id="02d8f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="02d8f-133">System.String</span></span>

### <span data-ttu-id="02d8f-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="02d8f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="02d8f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d8f-135">OUTPUTS</span></span>

### <span data-ttu-id="02d8f-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="02d8f-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="02d8f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d8f-137">NOTES</span></span>

## <span data-ttu-id="02d8f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d8f-138">RELATED LINKS</span></span>

[<span data-ttu-id="02d8f-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="02d8f-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="02d8f-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="02d8f-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


