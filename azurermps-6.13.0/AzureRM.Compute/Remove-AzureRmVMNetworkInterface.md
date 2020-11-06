---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609838"
---
# <span data-ttu-id="5e462-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5e462-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="5e462-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e462-102">SYNOPSIS</span></span>
<span data-ttu-id="5e462-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e462-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e462-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e462-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e462-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e462-105">DESCRIPTION</span></span>
<span data-ttu-id="5e462-106">O cmdlet **Remove-AzureRmVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e462-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="5e462-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e462-107">EXAMPLES</span></span>

## <span data-ttu-id="5e462-108">OS</span><span class="sxs-lookup"><span data-stu-id="5e462-108">PARAMETERS</span></span>

### <span data-ttu-id="5e462-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e462-109">-DefaultProfile</span></span>
<span data-ttu-id="5e462-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e462-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e462-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="5e462-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="5e462-112">Especifica uma matriz de IDs de interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5e462-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e462-113">-VM</span><span class="sxs-lookup"><span data-stu-id="5e462-113">-VM</span></span>
<span data-ttu-id="5e462-114">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5e462-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="5e462-115">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5e462-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="5e462-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e462-116">-Confirm</span></span>
<span data-ttu-id="5e462-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e462-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e462-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e462-118">-WhatIf</span></span>
<span data-ttu-id="5e462-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e462-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e462-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e462-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e462-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e462-121">CommonParameters</span></span>
<span data-ttu-id="5e462-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e462-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e462-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e462-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e462-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e462-124">INPUTS</span></span>

### <span data-ttu-id="5e462-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5e462-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5e462-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e462-126">OUTPUTS</span></span>

### <span data-ttu-id="5e462-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5e462-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5e462-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e462-128">NOTES</span></span>

## <span data-ttu-id="5e462-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e462-129">RELATED LINKS</span></span>

[<span data-ttu-id="5e462-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5e462-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


