---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: f89260b083d07ca717e1e302c2fb0bb747005d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889016"
---
# <span data-ttu-id="6fdc6-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6fdc6-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="6fdc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdc6-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="6fdc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6fdc6-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fdc6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6fdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdc6-106">O cmdlet **Get-AzVMAccessExtension** obtém informações sobre a Extensão de Máquina Virtual (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="6fdc6-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="6fdc6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdc6-108">Exemplo 1: Obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="6fdc6-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="6fdc6-109">Este comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6fdc6-110">Exemplo 2: Obter a exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="6fdc6-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="6fdc6-111">Este comando obtém a exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="6fdc6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-112">PARAMETERS</span></span>

### <span data-ttu-id="6fdc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdc6-113">-DefaultProfile</span></span>
<span data-ttu-id="6fdc6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fdc6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6fdc6-115">-Name</span></span>
<span data-ttu-id="6fdc6-116">Especifica o nome da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6fdc6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdc6-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fdc6-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6fdc6-119">-Status</span><span class="sxs-lookup"><span data-stu-id="6fdc6-119">-Status</span></span>
<span data-ttu-id="6fdc6-120">Indica que esse cmdlet obtém apenas a exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="6fdc6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6fdc6-121">-VMName</span></span>
<span data-ttu-id="6fdc6-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6fdc6-123">Este cmdlet obtém informações sobre VMAccess para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6fdc6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdc6-124">CommonParameters</span></span>
<span data-ttu-id="6fdc6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdc6-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fdc6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdc6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-127">INPUTS</span></span>

### <span data-ttu-id="6fdc6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6fdc6-128">System.String</span></span>

### <span data-ttu-id="6fdc6-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6fdc6-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6fdc6-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-130">OUTPUTS</span></span>

### <span data-ttu-id="6fdc6-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="6fdc6-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="6fdc6-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="6fdc6-132">NOTES</span></span>

## <span data-ttu-id="6fdc6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fdc6-133">RELATED LINKS</span></span>

[<span data-ttu-id="6fdc6-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6fdc6-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="6fdc6-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6fdc6-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="6fdc6-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6fdc6-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


