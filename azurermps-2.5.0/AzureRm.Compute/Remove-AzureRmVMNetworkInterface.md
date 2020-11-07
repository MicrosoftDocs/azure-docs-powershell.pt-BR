---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785974"
---
# <span data-ttu-id="48b6b-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="48b6b-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="48b6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="48b6b-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48b6b-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48b6b-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="48b6b-106">O cmdlet **Remove-AzureRmVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48b6b-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="48b6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="48b6b-108">1:</span><span class="sxs-lookup"><span data-stu-id="48b6b-108">1:</span></span>
```

```

## <span data-ttu-id="48b6b-109">OS</span><span class="sxs-lookup"><span data-stu-id="48b6b-109">PARAMETERS</span></span>

### <span data-ttu-id="48b6b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b6b-110">-DefaultProfile</span></span>
<span data-ttu-id="48b6b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48b6b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b6b-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="48b6b-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="48b6b-113">Especifica uma matriz de IDs de interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="48b6b-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="48b6b-114">-VM</span><span class="sxs-lookup"><span data-stu-id="48b6b-114">-VM</span></span>
<span data-ttu-id="48b6b-115">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="48b6b-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="48b6b-116">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="48b6b-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="48b6b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48b6b-117">-Confirm</span></span>
<span data-ttu-id="48b6b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b6b-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="48b6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b6b-119">-WhatIf</span></span>
<span data-ttu-id="48b6b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48b6b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48b6b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48b6b-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="48b6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b6b-122">CommonParameters</span></span>
<span data-ttu-id="48b6b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b6b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b6b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b6b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48b6b-125">INPUTS</span></span>

### <span data-ttu-id="48b6b-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="48b6b-126">PSVirtualMachine</span></span>
<span data-ttu-id="48b6b-127">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="48b6b-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="48b6b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48b6b-128">OUTPUTS</span></span>

### <span data-ttu-id="48b6b-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="48b6b-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="48b6b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48b6b-130">NOTES</span></span>

## <span data-ttu-id="48b6b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48b6b-131">RELATED LINKS</span></span>

[<span data-ttu-id="48b6b-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b6b-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


