---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111147"
---
# <span data-ttu-id="a7f9d-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a7f9d-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="a7f9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f9d-103">Obtém informações sobre uma extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="a7f9d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7f9d-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f9d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f9d-106">O cmdlet **Get-AzVMCustomScriptExtension obtém** informações sobre uma Extensão de Máquina Virtual de script personalizado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="a7f9d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f9d-108">Exemplo 1: Obter uma extensão de script personalizada</span><span class="sxs-lookup"><span data-stu-id="a7f9d-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="a7f9d-109">Esse comando obtém a extensão de script personalizada chamada ContosoCustomScript para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="a7f9d-110">Exemplo 2: Obter a exibição de instância de uma extensão de script personalizada</span><span class="sxs-lookup"><span data-stu-id="a7f9d-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="a7f9d-111">Esse comando obtém a exibição de instância da extensão de script personalizada chamada ContosoCustomScript para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="a7f9d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f9d-112">PARAMETERS</span></span>

### <span data-ttu-id="a7f9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f9d-113">-DefaultProfile</span></span>
<span data-ttu-id="a7f9d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f9d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7f9d-115">-Name</span></span>
<span data-ttu-id="a7f9d-116">Especifica o nome da extensão de script personalizada sobre a qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f9d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f9d-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7f9d-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a7f9d-119">-Status</span><span class="sxs-lookup"><span data-stu-id="a7f9d-119">-Status</span></span>
<span data-ttu-id="a7f9d-120">Indica que esse cmdlet obtém a exibição de instância da extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="a7f9d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="a7f9d-121">-VMName</span></span>
<span data-ttu-id="a7f9d-122">Especifica o nome de uma máquina virtual para a qual este cmdlet obtém a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="a7f9d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f9d-123">CommonParameters</span></span>
<span data-ttu-id="a7f9d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f9d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f9d-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7f9d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f9d-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7f9d-126">INPUTS</span></span>

### <span data-ttu-id="a7f9d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a7f9d-127">System.String</span></span>

### <span data-ttu-id="a7f9d-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7f9d-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7f9d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7f9d-129">OUTPUTS</span></span>

### <span data-ttu-id="a7f9d-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a7f9d-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="a7f9d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="a7f9d-131">NOTES</span></span>

## <span data-ttu-id="a7f9d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7f9d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7f9d-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a7f9d-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="a7f9d-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a7f9d-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="a7f9d-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a7f9d-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


