---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 307dccf0d5bb137ba83a6acf3a9b5db0b4606f7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893383"
---
# <span data-ttu-id="63aa9-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63aa9-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="63aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="63aa9-103">Obtém as configurações da extensão DSC em uma máquina virtual específica.</span><span class="sxs-lookup"><span data-stu-id="63aa9-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="63aa9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63aa9-104">SYNTAX</span></span>

### <span data-ttu-id="63aa9-105">GetDscExtension (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63aa9-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63aa9-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="63aa9-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63aa9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63aa9-107">DESCRIPTION</span></span>
<span data-ttu-id="63aa9-108">O cmdlet **Get-AzVMDscExtension** obtém as configurações da extensão DSC (Configuração de Estado Desejado) em uma máquina virtual específica.</span><span class="sxs-lookup"><span data-stu-id="63aa9-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="63aa9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63aa9-109">EXAMPLES</span></span>

### <span data-ttu-id="63aa9-110">Exemplo 1: Obter as configurações de uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="63aa9-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="63aa9-111">Este comando obtém as configurações da extensão chamada DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="63aa9-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="63aa9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63aa9-112">PARAMETERS</span></span>

### <span data-ttu-id="63aa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63aa9-113">-DefaultProfile</span></span>
<span data-ttu-id="63aa9-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="63aa9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63aa9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63aa9-115">-Name</span></span>
<span data-ttu-id="63aa9-116">Especifica o nome do recurso Gerenciador de Recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="63aa9-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="63aa9-117">O Set-AzVMDscExtension cmdlet define esse nome como Microsoft.Powershell.DSC, que é o mesmo valor usado por **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="63aa9-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="63aa9-118">Especifique esse parâmetro somente se você alterou o nome padrão no cmdlet **Set-AzVMDscExtension** ou usou um nome de recurso diferente em um modelo do Gerenciador de Recursos.</span><span class="sxs-lookup"><span data-stu-id="63aa9-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63aa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63aa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="63aa9-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="63aa9-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63aa9-121">-Status</span><span class="sxs-lookup"><span data-stu-id="63aa9-121">-Status</span></span>
<span data-ttu-id="63aa9-122">Indica que esse cmdlet obtém a exibição de instância da extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="63aa9-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63aa9-123">-VM</span><span class="sxs-lookup"><span data-stu-id="63aa9-123">-VM</span></span>
<span data-ttu-id="63aa9-124">Especifica o objeto da máquina virtual em que a extensão está.</span><span class="sxs-lookup"><span data-stu-id="63aa9-124">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="63aa9-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="63aa9-125">-VMName</span></span>
<span data-ttu-id="63aa9-126">Especifica o nome de uma máquina virtual para a qual este cmdlet obtém a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="63aa9-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63aa9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63aa9-127">CommonParameters</span></span>
<span data-ttu-id="63aa9-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63aa9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63aa9-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63aa9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63aa9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63aa9-130">INPUTS</span></span>

### <span data-ttu-id="63aa9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="63aa9-131">System.String</span></span>

### <span data-ttu-id="63aa9-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63aa9-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63aa9-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63aa9-133">OUTPUTS</span></span>

### <span data-ttu-id="63aa9-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="63aa9-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="63aa9-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="63aa9-135">NOTES</span></span>

## <span data-ttu-id="63aa9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63aa9-136">RELATED LINKS</span></span>

[<span data-ttu-id="63aa9-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63aa9-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="63aa9-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="63aa9-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


