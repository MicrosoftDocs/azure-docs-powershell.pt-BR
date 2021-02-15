---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112106"
---
# <span data-ttu-id="91763-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="91763-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="91763-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91763-102">SYNOPSIS</span></span>
<span data-ttu-id="91763-103">Remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91763-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="91763-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91763-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91763-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="91763-105">DESCRIPTION</span></span>
<span data-ttu-id="91763-106">O **cmdlet Remove-AzVMNetworkInterface** remove uma interface de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91763-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="91763-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91763-107">EXAMPLES</span></span>

## <span data-ttu-id="91763-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91763-108">PARAMETERS</span></span>

### <span data-ttu-id="91763-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91763-109">-DefaultProfile</span></span>
<span data-ttu-id="91763-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="91763-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91763-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="91763-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="91763-112">Especifica uma matriz de IDs de interface de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="91763-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91763-113">-VM</span><span class="sxs-lookup"><span data-stu-id="91763-113">-VM</span></span>
<span data-ttu-id="91763-114">Especifica a máquina virtual da qual este cmdlet remove uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="91763-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="91763-115">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="91763-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="91763-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91763-116">-Confirm</span></span>
<span data-ttu-id="91763-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91763-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91763-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91763-118">-WhatIf</span></span>
<span data-ttu-id="91763-119">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91763-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91763-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91763-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91763-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91763-121">CommonParameters</span></span>
<span data-ttu-id="91763-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91763-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91763-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91763-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91763-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="91763-124">INPUTS</span></span>

### <span data-ttu-id="91763-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="91763-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="91763-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="91763-126">OUTPUTS</span></span>

### <span data-ttu-id="91763-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="91763-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="91763-128">Notas</span><span class="sxs-lookup"><span data-stu-id="91763-128">NOTES</span></span>

## <span data-ttu-id="91763-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91763-129">RELATED LINKS</span></span>

[<span data-ttu-id="91763-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="91763-130">Get-AzVM</span></span>](./Get-AzVM.md)


