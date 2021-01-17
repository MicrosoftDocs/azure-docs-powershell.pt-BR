---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434232"
---
# <span data-ttu-id="63e0c-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e0c-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="63e0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="63e0c-103">Remove uma extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e0c-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="63e0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63e0c-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e0c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="63e0c-106">O cmdlet **Remove-AzVmssDiagnosticsExtension** remove uma extensão de diagnóstico do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="63e0c-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="63e0c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="63e0c-108">Exemplo 1: remover uma extensão de diagnóstico do VMSS</span><span class="sxs-lookup"><span data-stu-id="63e0c-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="63e0c-109">Esse comando Remove a extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e0c-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="63e0c-110">OS</span><span class="sxs-lookup"><span data-stu-id="63e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="63e0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e0c-111">-DefaultProfile</span></span>
<span data-ttu-id="63e0c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63e0c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e0c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="63e0c-113">-Name</span></span>
<span data-ttu-id="63e0c-114">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="63e0c-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e0c-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63e0c-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="63e0c-116">Especifica o VMSS a partir do qual a extensão deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="63e0c-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="63e0c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63e0c-117">-Confirm</span></span>
<span data-ttu-id="63e0c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e0c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e0c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e0c-119">-WhatIf</span></span>
<span data-ttu-id="63e0c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63e0c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e0c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63e0c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e0c-122">CommonParameters</span></span>
<span data-ttu-id="63e0c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e0c-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63e0c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e0c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63e0c-125">INPUTS</span></span>

### <span data-ttu-id="63e0c-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63e0c-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="63e0c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="63e0c-127">System.String</span></span>

## <span data-ttu-id="63e0c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63e0c-128">OUTPUTS</span></span>

### <span data-ttu-id="63e0c-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63e0c-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="63e0c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63e0c-130">NOTES</span></span>

## <span data-ttu-id="63e0c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e0c-131">RELATED LINKS</span></span>

[<span data-ttu-id="63e0c-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e0c-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="63e0c-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63e0c-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="63e0c-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="63e0c-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


