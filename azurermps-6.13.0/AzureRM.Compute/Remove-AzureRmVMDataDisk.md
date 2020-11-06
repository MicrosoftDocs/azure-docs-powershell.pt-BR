---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: e0f8b1d4e47cfe488fcba02228bd35c09f4d3ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426414"
---
# <span data-ttu-id="757ea-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="757ea-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="757ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="757ea-102">SYNOPSIS</span></span>
<span data-ttu-id="757ea-103">Remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="757ea-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="757ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="757ea-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="757ea-105">DESCRIPTION</span></span>
<span data-ttu-id="757ea-106">O cmdlet **Remove-AzureRmVMDataDisk** remove um disco de dados de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="757ea-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="757ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="757ea-107">EXAMPLES</span></span>

### <span data-ttu-id="757ea-108">Exemplo 1: remover um disco de dados de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="757ea-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="757ea-109">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="757ea-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="757ea-110">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="757ea-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="757ea-111">O segundo comando Remove o disco de dados denominado Disk3 da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="757ea-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="757ea-112">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="757ea-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="757ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="757ea-113">PARAMETERS</span></span>

### <span data-ttu-id="757ea-114">-Datadisknames</span><span class="sxs-lookup"><span data-stu-id="757ea-114">-DataDiskNames</span></span>
<span data-ttu-id="757ea-115">Especifica os nomes de um ou mais discos de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="757ea-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="757ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757ea-116">-DefaultProfile</span></span>
<span data-ttu-id="757ea-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="757ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757ea-118">-VM</span><span class="sxs-lookup"><span data-stu-id="757ea-118">-VM</span></span>
<span data-ttu-id="757ea-119">Especifica o objeto da máquina virtual local do qual remover um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="757ea-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="757ea-120">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="757ea-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="757ea-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="757ea-121">-Confirm</span></span>
<span data-ttu-id="757ea-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757ea-123">-WhatIf</span></span>
<span data-ttu-id="757ea-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="757ea-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="757ea-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="757ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757ea-126">CommonParameters</span></span>
<span data-ttu-id="757ea-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757ea-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757ea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757ea-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="757ea-129">INPUTS</span></span>

### <span data-ttu-id="757ea-130">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="757ea-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="757ea-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="757ea-131">OUTPUTS</span></span>

### <span data-ttu-id="757ea-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="757ea-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="757ea-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="757ea-133">NOTES</span></span>

## <span data-ttu-id="757ea-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="757ea-134">RELATED LINKS</span></span>

[<span data-ttu-id="757ea-135">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="757ea-135">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="757ea-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="757ea-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


