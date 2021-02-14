---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111106"
---
# <span data-ttu-id="cf31a-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cf31a-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="cf31a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf31a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf31a-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf31a-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="cf31a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf31a-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf31a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf31a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf31a-106">O **cmdlet Remove-AzVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf31a-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="cf31a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cf31a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf31a-108">Exemplo 1: Remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cf31a-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="cf31a-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="cf31a-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="cf31a-110">O comando armazena a máquina virtual na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="cf31a-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cf31a-111">O segundo comando remove o disco de dados chamado Disco3 da máquina virtual armazenada no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cf31a-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="cf31a-112">O comando final atualiza o estado da máquina virtual armazenada $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cf31a-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="cf31a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf31a-113">PARAMETERS</span></span>

### <span data-ttu-id="cf31a-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="cf31a-114">-DataDiskNames</span></span>
<span data-ttu-id="cf31a-115">Especifica os nomes de um ou mais discos de dados que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="cf31a-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cf31a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf31a-116">-DefaultProfile</span></span>
<span data-ttu-id="cf31a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cf31a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf31a-118">-VM</span><span class="sxs-lookup"><span data-stu-id="cf31a-118">-VM</span></span>
<span data-ttu-id="cf31a-119">Especifica o objeto de máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="cf31a-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="cf31a-120">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="cf31a-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="cf31a-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cf31a-121">-Confirm</span></span>
<span data-ttu-id="cf31a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf31a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf31a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf31a-123">-WhatIf</span></span>
<span data-ttu-id="cf31a-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cf31a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf31a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf31a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf31a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf31a-126">CommonParameters</span></span>
<span data-ttu-id="cf31a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf31a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf31a-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf31a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf31a-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="cf31a-129">INPUTS</span></span>

### <span data-ttu-id="cf31a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cf31a-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cf31a-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="cf31a-131">OUTPUTS</span></span>

### <span data-ttu-id="cf31a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cf31a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cf31a-133">Notas</span><span class="sxs-lookup"><span data-stu-id="cf31a-133">NOTES</span></span>

## <span data-ttu-id="cf31a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf31a-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf31a-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cf31a-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="cf31a-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cf31a-136">Get-AzVM</span></span>](./Get-AzVM.md)


