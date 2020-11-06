---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426973"
---
# <span data-ttu-id="f17a3-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f17a3-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="f17a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f17a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f17a3-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f17a3-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f17a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f17a3-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f17a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f17a3-105">DESCRIPTION</span></span>
<span data-ttu-id="f17a3-106">O cmdlet **Remove-AzureRmVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f17a3-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="f17a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f17a3-107">EXAMPLES</span></span>

### <span data-ttu-id="f17a3-108">Exemplo 1: remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f17a3-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="f17a3-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="f17a3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="f17a3-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f17a3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f17a3-111">O segundo comando Remove o disco de dados denominado Disk3 da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f17a3-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="f17a3-112">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f17a3-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="f17a3-113">OS</span><span class="sxs-lookup"><span data-stu-id="f17a3-113">PARAMETERS</span></span>

### <span data-ttu-id="f17a3-114">-Datadisknames</span><span class="sxs-lookup"><span data-stu-id="f17a3-114">-DataDiskNames</span></span>
<span data-ttu-id="f17a3-115">Especifica os nomes de um ou mais discos de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f17a3-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f17a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17a3-116">-DefaultProfile</span></span>
<span data-ttu-id="f17a3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f17a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17a3-118">-VM</span><span class="sxs-lookup"><span data-stu-id="f17a3-118">-VM</span></span>
<span data-ttu-id="f17a3-119">Especifica o objeto da máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="f17a3-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="f17a3-120">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f17a3-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="f17a3-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f17a3-121">-Confirm</span></span>
<span data-ttu-id="f17a3-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f17a3-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="f17a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f17a3-123">-WhatIf</span></span>
<span data-ttu-id="f17a3-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f17a3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f17a3-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f17a3-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="f17a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17a3-126">CommonParameters</span></span>
<span data-ttu-id="f17a3-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17a3-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17a3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17a3-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f17a3-129">INPUTS</span></span>

## <span data-ttu-id="f17a3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f17a3-130">OUTPUTS</span></span>

## <span data-ttu-id="f17a3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f17a3-131">NOTES</span></span>

## <span data-ttu-id="f17a3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f17a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="f17a3-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f17a3-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="f17a3-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f17a3-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


