---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426793"
---
# <span data-ttu-id="e1c2e-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e1c2e-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="e1c2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c2e-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1c2e-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c2e-106">O cmdlet **Remove-AzureRmVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="e1c2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1c2e-107">EXAMPLES</span></span>

## <span data-ttu-id="e1c2e-108">OS</span><span class="sxs-lookup"><span data-stu-id="e1c2e-108">PARAMETERS</span></span>

### <span data-ttu-id="e1c2e-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="e1c2e-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="e1c2e-110">Especifica uma matriz de IDs de interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c2e-111">-VM</span><span class="sxs-lookup"><span data-stu-id="e1c2e-111">-VM</span></span>
<span data-ttu-id="e1c2e-112">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="e1c2e-113">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="e1c2e-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1c2e-114">-Confirm</span></span>
<span data-ttu-id="e1c2e-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="e1c2e-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c2e-116">-WhatIf</span></span>
<span data-ttu-id="e1c2e-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c2e-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="e1c2e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c2e-119">CommonParameters</span></span>
<span data-ttu-id="e1c2e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c2e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c2e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c2e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1c2e-122">INPUTS</span></span>

### <span data-ttu-id="e1c2e-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1c2e-123">None</span></span>
<span data-ttu-id="e1c2e-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e1c2e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1c2e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1c2e-125">OUTPUTS</span></span>

## <span data-ttu-id="e1c2e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1c2e-126">NOTES</span></span>

## <span data-ttu-id="e1c2e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1c2e-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1c2e-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e1c2e-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


