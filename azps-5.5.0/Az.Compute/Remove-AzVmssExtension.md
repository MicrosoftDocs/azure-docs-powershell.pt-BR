---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112102"
---
# <span data-ttu-id="ff713-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ff713-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="ff713-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff713-102">SYNOPSIS</span></span>
<span data-ttu-id="ff713-103">Remove uma extensão do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff713-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="ff713-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff713-104">SYNTAX</span></span>

### <span data-ttu-id="ff713-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff713-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff713-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff713-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff713-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff713-107">DESCRIPTION</span></span>
<span data-ttu-id="ff713-108">O cmdlet **Remove-AzVmssExtension** remove uma extensão do VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="ff713-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ff713-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff713-109">EXAMPLES</span></span>

### <span data-ttu-id="ff713-110">Exemplo 1: Remover uma extensão VMSS</span><span class="sxs-lookup"><span data-stu-id="ff713-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="ff713-111">Esse comando remove a extensão de um VMSS e atualiza o VMSS após a modificação.</span><span class="sxs-lookup"><span data-stu-id="ff713-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="ff713-112">Exemplo 2: remover uma instância de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="ff713-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="ff713-113">Esse comando remove a ID de especificação de extensão do VMSS que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="ff713-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="ff713-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff713-114">PARAMETERS</span></span>

### <span data-ttu-id="ff713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff713-115">-DefaultProfile</span></span>
<span data-ttu-id="ff713-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ff713-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff713-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ff713-117">-Id</span></span>
<span data-ttu-id="ff713-118">Especifica a ID da extensão que este cmdlet remove do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff713-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ff713-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff713-119">-Name</span></span>
<span data-ttu-id="ff713-120">Especifica o nome da extensão que este cmdlet remove do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff713-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ff713-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff713-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ff713-122">Especifica o VMSS do qual remover a extensão.</span><span class="sxs-lookup"><span data-stu-id="ff713-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="ff713-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ff713-123">-Confirm</span></span>
<span data-ttu-id="ff713-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff713-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff713-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff713-125">-WhatIf</span></span>
<span data-ttu-id="ff713-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ff713-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff713-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff713-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff713-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff713-128">CommonParameters</span></span>
<span data-ttu-id="ff713-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff713-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff713-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff713-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff713-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff713-131">INPUTS</span></span>

### <span data-ttu-id="ff713-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff713-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ff713-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ff713-133">System.String</span></span>

## <span data-ttu-id="ff713-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff713-134">OUTPUTS</span></span>

### <span data-ttu-id="ff713-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff713-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ff713-136">Notas</span><span class="sxs-lookup"><span data-stu-id="ff713-136">NOTES</span></span>

## <span data-ttu-id="ff713-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff713-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff713-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ff713-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
