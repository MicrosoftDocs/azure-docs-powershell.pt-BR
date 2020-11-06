---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: edf0ab0784288f6a700dc82a77a66846a5806826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597454"
---
# <span data-ttu-id="6ed50-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ed50-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="6ed50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ed50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed50-103">Obtém informações sobre a extensão VMAccess.</span><span class="sxs-lookup"><span data-stu-id="6ed50-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="6ed50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ed50-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ed50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ed50-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed50-106">O cmdlet **Get-AzVMAccessExtension** Obtém informações sobre a extensão da máquina virtual do VMAccess (acesso à máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="6ed50-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="6ed50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ed50-107">EXAMPLES</span></span>

### <span data-ttu-id="6ed50-108">Exemplo 1: obter a extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="6ed50-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="6ed50-109">Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual nomeada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6ed50-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6ed50-110">Exemplo 2: obter o modo de exibição de instância da extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="6ed50-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="6ed50-111">Esse comando obtém o modo de exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6ed50-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="6ed50-112">OS</span><span class="sxs-lookup"><span data-stu-id="6ed50-112">PARAMETERS</span></span>

### <span data-ttu-id="6ed50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed50-113">-DefaultProfile</span></span>
<span data-ttu-id="6ed50-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ed50-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ed50-115">-Name</span></span>
<span data-ttu-id="6ed50-116">Especifica o nome da extensão obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed50-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6ed50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed50-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ed50-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed50-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6ed50-119">-Status</span><span class="sxs-lookup"><span data-stu-id="6ed50-119">-Status</span></span>
<span data-ttu-id="6ed50-120">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão.</span><span class="sxs-lookup"><span data-stu-id="6ed50-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="6ed50-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ed50-121">-VMName</span></span>
<span data-ttu-id="6ed50-122">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ed50-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6ed50-123">Este cmdlet obtém informações sobre VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6ed50-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ed50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed50-124">CommonParameters</span></span>
<span data-ttu-id="6ed50-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ed50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed50-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ed50-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed50-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ed50-127">INPUTS</span></span>

### <span data-ttu-id="6ed50-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6ed50-128">System.String</span></span>

### <span data-ttu-id="6ed50-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ed50-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ed50-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ed50-130">OUTPUTS</span></span>

### <span data-ttu-id="6ed50-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="6ed50-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="6ed50-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ed50-132">NOTES</span></span>

## <span data-ttu-id="6ed50-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ed50-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ed50-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ed50-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="6ed50-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ed50-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="6ed50-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6ed50-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


