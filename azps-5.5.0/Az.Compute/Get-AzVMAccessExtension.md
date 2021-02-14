---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111150"
---
# <span data-ttu-id="83407-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="83407-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="83407-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83407-102">SYNOPSIS</span></span>
<span data-ttu-id="83407-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="83407-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="83407-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83407-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83407-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="83407-105">DESCRIPTION</span></span>
<span data-ttu-id="83407-106">O cmdlet **Get-AzVMAccessExtension obtém** informações sobre a Extensão de Máquina Virtual (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="83407-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="83407-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83407-107">EXAMPLES</span></span>

### <span data-ttu-id="83407-108">Exemplo 1: Obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="83407-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="83407-109">Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="83407-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="83407-110">Exemplo 2: Obter a exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="83407-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="83407-111">Esse comando obtém a exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="83407-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="83407-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83407-112">PARAMETERS</span></span>

### <span data-ttu-id="83407-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83407-113">-DefaultProfile</span></span>
<span data-ttu-id="83407-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="83407-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83407-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="83407-115">-Name</span></span>
<span data-ttu-id="83407-116">Especifica o nome da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="83407-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83407-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83407-117">-ResourceGroupName</span></span>
<span data-ttu-id="83407-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83407-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="83407-119">-Status</span><span class="sxs-lookup"><span data-stu-id="83407-119">-Status</span></span>
<span data-ttu-id="83407-120">Indica que esse cmdlet obtém apenas a exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="83407-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="83407-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="83407-121">-VMName</span></span>
<span data-ttu-id="83407-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="83407-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="83407-123">Este cmdlet obtém informações sobre o VMAccess para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="83407-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="83407-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83407-124">CommonParameters</span></span>
<span data-ttu-id="83407-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83407-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83407-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83407-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83407-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="83407-127">INPUTS</span></span>

### <span data-ttu-id="83407-128">System.String</span><span class="sxs-lookup"><span data-stu-id="83407-128">System.String</span></span>

### <span data-ttu-id="83407-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="83407-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="83407-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="83407-130">OUTPUTS</span></span>

### <span data-ttu-id="83407-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="83407-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="83407-132">Notas</span><span class="sxs-lookup"><span data-stu-id="83407-132">NOTES</span></span>

## <span data-ttu-id="83407-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83407-133">RELATED LINKS</span></span>

[<span data-ttu-id="83407-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="83407-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="83407-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="83407-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="83407-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="83407-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


