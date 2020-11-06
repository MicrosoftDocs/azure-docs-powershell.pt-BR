---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602544"
---
# <span data-ttu-id="696d3-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="696d3-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="696d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="696d3-102">SYNOPSIS</span></span>
<span data-ttu-id="696d3-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="696d3-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="696d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="696d3-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="696d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="696d3-105">DESCRIPTION</span></span>
<span data-ttu-id="696d3-106">O cmdlet **Remove-AzureRmVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="696d3-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="696d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="696d3-107">EXAMPLES</span></span>

### <span data-ttu-id="696d3-108">Exemplo 1: remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="696d3-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="696d3-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="696d3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="696d3-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="696d3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="696d3-111">O segundo comando Remove o disco de dados denominado Disk3 da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="696d3-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="696d3-112">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="696d3-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="696d3-113">OS</span><span class="sxs-lookup"><span data-stu-id="696d3-113">PARAMETERS</span></span>

### <span data-ttu-id="696d3-114">-Datadisknames</span><span class="sxs-lookup"><span data-stu-id="696d3-114">-DataDiskNames</span></span>
<span data-ttu-id="696d3-115">Especifica os nomes de um ou mais discos de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="696d3-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696d3-116">-VM</span><span class="sxs-lookup"><span data-stu-id="696d3-116">-VM</span></span>
<span data-ttu-id="696d3-117">Especifica o objeto da máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="696d3-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="696d3-118">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="696d3-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696d3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="696d3-119">-Confirm</span></span>
<span data-ttu-id="696d3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="696d3-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696d3-121">-WhatIf</span></span>
<span data-ttu-id="696d3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="696d3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="696d3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="696d3-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696d3-124">CommonParameters</span></span>
<span data-ttu-id="696d3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696d3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696d3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="696d3-127">INPUTS</span></span>

### <span data-ttu-id="696d3-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="696d3-128">None</span></span>
<span data-ttu-id="696d3-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="696d3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="696d3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="696d3-130">OUTPUTS</span></span>

## <span data-ttu-id="696d3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="696d3-131">NOTES</span></span>

## <span data-ttu-id="696d3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="696d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="696d3-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="696d3-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="696d3-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="696d3-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


