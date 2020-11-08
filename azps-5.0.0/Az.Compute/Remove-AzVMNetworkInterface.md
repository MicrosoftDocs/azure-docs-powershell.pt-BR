---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116580"
---
# <span data-ttu-id="38a81-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38a81-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="38a81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38a81-102">SYNOPSIS</span></span>
<span data-ttu-id="38a81-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38a81-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="38a81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38a81-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38a81-105">DESCRIPTION</span></span>
<span data-ttu-id="38a81-106">O cmdlet **Remove-AzVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38a81-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="38a81-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38a81-107">EXAMPLES</span></span>

## <span data-ttu-id="38a81-108">OS</span><span class="sxs-lookup"><span data-stu-id="38a81-108">PARAMETERS</span></span>

### <span data-ttu-id="38a81-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a81-109">-DefaultProfile</span></span>
<span data-ttu-id="38a81-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38a81-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a81-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="38a81-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="38a81-112">Especifica uma matriz de IDs de interface de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="38a81-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38a81-113">-VM</span><span class="sxs-lookup"><span data-stu-id="38a81-113">-VM</span></span>
<span data-ttu-id="38a81-114">Especifica a máquina virtual a partir da qual esse cmdlet Remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="38a81-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="38a81-115">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="38a81-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="38a81-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38a81-116">-Confirm</span></span>
<span data-ttu-id="38a81-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a81-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a81-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a81-118">-WhatIf</span></span>
<span data-ttu-id="38a81-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38a81-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38a81-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38a81-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a81-121">CommonParameters</span></span>
<span data-ttu-id="38a81-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a81-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a81-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a81-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38a81-124">INPUTS</span></span>

### <span data-ttu-id="38a81-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38a81-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38a81-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38a81-126">OUTPUTS</span></span>

### <span data-ttu-id="38a81-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38a81-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38a81-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38a81-128">NOTES</span></span>

## <span data-ttu-id="38a81-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38a81-129">RELATED LINKS</span></span>

[<span data-ttu-id="38a81-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="38a81-130">Get-AzVM</span></span>](./Get-AzVM.md)


