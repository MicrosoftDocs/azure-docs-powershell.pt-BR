---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776904"
---
# <span data-ttu-id="11162-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="11162-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="11162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11162-102">SYNOPSIS</span></span>
<span data-ttu-id="11162-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11162-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="11162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11162-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11162-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11162-105">DESCRIPTION</span></span>
<span data-ttu-id="11162-106">O cmdlet **Remove-AzVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11162-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="11162-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11162-107">EXAMPLES</span></span>

### <span data-ttu-id="11162-108">1:</span><span class="sxs-lookup"><span data-stu-id="11162-108">1:</span></span>
```

```

## <span data-ttu-id="11162-109">OS</span><span class="sxs-lookup"><span data-stu-id="11162-109">PARAMETERS</span></span>

### <span data-ttu-id="11162-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11162-110">-DefaultProfile</span></span>
<span data-ttu-id="11162-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11162-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11162-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="11162-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="11162-113">Especifica uma matriz de IDs de interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="11162-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="11162-114">-VM</span><span class="sxs-lookup"><span data-stu-id="11162-114">-VM</span></span>
<span data-ttu-id="11162-115">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="11162-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="11162-116">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="11162-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="11162-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11162-117">-Confirm</span></span>
<span data-ttu-id="11162-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11162-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="11162-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11162-119">-WhatIf</span></span>
<span data-ttu-id="11162-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11162-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11162-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11162-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="11162-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11162-122">CommonParameters</span></span>
<span data-ttu-id="11162-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11162-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11162-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11162-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11162-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11162-125">INPUTS</span></span>

### <span data-ttu-id="11162-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11162-126">PSVirtualMachine</span></span>
<span data-ttu-id="11162-127">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="11162-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="11162-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11162-128">OUTPUTS</span></span>

### <span data-ttu-id="11162-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="11162-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="11162-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11162-130">NOTES</span></span>

## <span data-ttu-id="11162-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11162-131">RELATED LINKS</span></span>

[<span data-ttu-id="11162-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="11162-132">Get-AzVM</span></span>](./Get-AzVM.md)


