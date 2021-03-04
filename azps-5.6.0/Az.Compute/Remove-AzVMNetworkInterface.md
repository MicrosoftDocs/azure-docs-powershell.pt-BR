---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 247a066da4d6a8a84587e451850954df40ba7be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892533"
---
# <span data-ttu-id="c9570-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c9570-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="c9570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9570-102">SYNOPSIS</span></span>
<span data-ttu-id="c9570-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9570-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c9570-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c9570-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9570-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c9570-105">DESCRIPTION</span></span>
<span data-ttu-id="c9570-106">O cmdlet **Remove-AzVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9570-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="c9570-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9570-107">EXAMPLES</span></span>

## <span data-ttu-id="c9570-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c9570-108">PARAMETERS</span></span>

### <span data-ttu-id="c9570-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9570-109">-DefaultProfile</span></span>
<span data-ttu-id="c9570-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c9570-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9570-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="c9570-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="c9570-112">Especifica uma matriz de IDs de interface de rede que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="c9570-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9570-113">-VM</span><span class="sxs-lookup"><span data-stu-id="c9570-113">-VM</span></span>
<span data-ttu-id="c9570-114">Especifica a máquina virtual da qual esse cmdlet remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c9570-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="c9570-115">Para obter um objeto de máquina virtual, use Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9570-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="c9570-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9570-116">-Confirm</span></span>
<span data-ttu-id="c9570-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9570-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9570-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9570-118">-WhatIf</span></span>
<span data-ttu-id="c9570-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9570-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9570-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9570-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9570-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9570-121">CommonParameters</span></span>
<span data-ttu-id="c9570-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9570-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9570-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9570-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9570-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9570-124">INPUTS</span></span>

### <span data-ttu-id="c9570-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9570-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9570-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c9570-126">OUTPUTS</span></span>

### <span data-ttu-id="c9570-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9570-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9570-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="c9570-128">NOTES</span></span>

## <span data-ttu-id="c9570-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9570-129">RELATED LINKS</span></span>

[<span data-ttu-id="c9570-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c9570-130">Get-AzVM</span></span>](./Get-AzVM.md)


