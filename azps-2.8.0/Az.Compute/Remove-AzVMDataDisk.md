---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 11605529233a6c849a5f164f279b966e769265cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597297"
---
# <span data-ttu-id="86d0a-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86d0a-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="86d0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="86d0a-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="86d0a-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="86d0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86d0a-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="86d0a-106">O cmdlet **Remove-AzVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="86d0a-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="86d0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="86d0a-108">Exemplo 1: remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="86d0a-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="86d0a-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="86d0a-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="86d0a-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="86d0a-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="86d0a-111">O segundo comando Remove o disco de dados denominado Disk3 da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="86d0a-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="86d0a-112">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="86d0a-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="86d0a-113">OS</span><span class="sxs-lookup"><span data-stu-id="86d0a-113">PARAMETERS</span></span>

### <span data-ttu-id="86d0a-114">-Datadisknames</span><span class="sxs-lookup"><span data-stu-id="86d0a-114">-DataDiskNames</span></span>
<span data-ttu-id="86d0a-115">Especifica os nomes de um ou mais discos de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="86d0a-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="86d0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d0a-116">-DefaultProfile</span></span>
<span data-ttu-id="86d0a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86d0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86d0a-118">-VM</span><span class="sxs-lookup"><span data-stu-id="86d0a-118">-VM</span></span>
<span data-ttu-id="86d0a-119">Especifica o objeto da máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="86d0a-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="86d0a-120">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="86d0a-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="86d0a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86d0a-121">-Confirm</span></span>
<span data-ttu-id="86d0a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d0a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d0a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d0a-123">-WhatIf</span></span>
<span data-ttu-id="86d0a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86d0a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86d0a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86d0a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d0a-126">CommonParameters</span></span>
<span data-ttu-id="86d0a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d0a-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86d0a-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d0a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86d0a-129">INPUTS</span></span>

### <span data-ttu-id="86d0a-130">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86d0a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="86d0a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86d0a-131">OUTPUTS</span></span>

### <span data-ttu-id="86d0a-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86d0a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="86d0a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86d0a-133">NOTES</span></span>

## <span data-ttu-id="86d0a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86d0a-134">RELATED LINKS</span></span>

[<span data-ttu-id="86d0a-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86d0a-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="86d0a-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="86d0a-136">Get-AzVM</span></span>](./Get-AzVM.md)


