---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889297"
---
# <span data-ttu-id="d839a-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d839a-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="d839a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d839a-102">SYNOPSIS</span></span>
<span data-ttu-id="d839a-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d839a-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="d839a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d839a-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d839a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d839a-105">DESCRIPTION</span></span>
<span data-ttu-id="d839a-106">O cmdlet **Remove-AzVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d839a-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="d839a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d839a-107">EXAMPLES</span></span>

### <span data-ttu-id="d839a-108">Exemplo 1: Remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d839a-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d839a-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="d839a-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="d839a-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d839a-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d839a-111">O segundo comando remove o disco de dados chamado Disk3 da máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d839a-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d839a-112">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d839a-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="d839a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d839a-113">PARAMETERS</span></span>

### <span data-ttu-id="d839a-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="d839a-114">-DataDiskNames</span></span>
<span data-ttu-id="d839a-115">Especifica os nomes de um ou mais discos de dados que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d839a-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d839a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d839a-116">-DefaultProfile</span></span>
<span data-ttu-id="d839a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d839a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d839a-118">-VM</span><span class="sxs-lookup"><span data-stu-id="d839a-118">-VM</span></span>
<span data-ttu-id="d839a-119">Especifica o objeto da máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="d839a-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="d839a-120">Para obter um objeto de máquina virtual, use Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d839a-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d839a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d839a-121">-Confirm</span></span>
<span data-ttu-id="d839a-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d839a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d839a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d839a-123">-WhatIf</span></span>
<span data-ttu-id="d839a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d839a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d839a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d839a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d839a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d839a-126">CommonParameters</span></span>
<span data-ttu-id="d839a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d839a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d839a-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d839a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d839a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d839a-129">INPUTS</span></span>

### <span data-ttu-id="d839a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d839a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d839a-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d839a-131">OUTPUTS</span></span>

### <span data-ttu-id="d839a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d839a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d839a-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="d839a-133">NOTES</span></span>

## <span data-ttu-id="d839a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d839a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d839a-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d839a-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="d839a-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d839a-136">Get-AzVM</span></span>](./Get-AzVM.md)


