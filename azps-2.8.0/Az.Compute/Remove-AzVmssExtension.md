---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 676584e1e6814a05ba1ab49bb7c751218a16d361
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597275"
---
# <span data-ttu-id="e7c79-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e7c79-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="e7c79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7c79-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c79-103">Remove uma extensão da VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7c79-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="e7c79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7c79-104">SYNTAX</span></span>

### <span data-ttu-id="e7c79-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c79-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7c79-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7c79-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c79-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7c79-107">DESCRIPTION</span></span>
<span data-ttu-id="e7c79-108">O cmdlet **Remove-AzVmssExtension** remove uma extensão do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="e7c79-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e7c79-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7c79-109">EXAMPLES</span></span>

### <span data-ttu-id="e7c79-110">Exemplo 1: remover uma extensão VMSS</span><span class="sxs-lookup"><span data-stu-id="e7c79-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="e7c79-111">Esse comando Remove a extensão de um VMSS e atualiza o VMSS após a modificação.</span><span class="sxs-lookup"><span data-stu-id="e7c79-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="e7c79-112">Exemplo 2: remover uma instância de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="e7c79-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="e7c79-113">Esse comando Remove a ID de extensão de nome da VMSS que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="e7c79-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="e7c79-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7c79-114">PARAMETERS</span></span>

### <span data-ttu-id="e7c79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c79-115">-DefaultProfile</span></span>
<span data-ttu-id="e7c79-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c79-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e7c79-117">-Id</span></span>
<span data-ttu-id="e7c79-118">Especifica a ID da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7c79-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c79-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7c79-119">-Name</span></span>
<span data-ttu-id="e7c79-120">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7c79-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c79-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7c79-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7c79-122">Especifica o VMSS do qual a extensão será removida.</span><span class="sxs-lookup"><span data-stu-id="e7c79-122">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c79-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7c79-123">-Confirm</span></span>
<span data-ttu-id="e7c79-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c79-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c79-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c79-125">-WhatIf</span></span>
<span data-ttu-id="e7c79-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7c79-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7c79-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7c79-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c79-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c79-128">CommonParameters</span></span>
<span data-ttu-id="e7c79-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c79-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c79-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7c79-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c79-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7c79-131">INPUTS</span></span>

### <span data-ttu-id="e7c79-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7c79-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e7c79-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c79-133">System.String</span></span>

## <span data-ttu-id="e7c79-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7c79-134">OUTPUTS</span></span>

### <span data-ttu-id="e7c79-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7c79-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e7c79-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7c79-136">NOTES</span></span>

## <span data-ttu-id="e7c79-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7c79-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7c79-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e7c79-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
