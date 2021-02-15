---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112104"
---
# <span data-ttu-id="ea7b3-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea7b3-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="ea7b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7b3-103">Remove uma extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="ea7b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea7b3-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7b3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7b3-106">O cmdlet **Remove-AzVmssDiagnosticsExtension** remove uma extensão de diagnóstico do VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="ea7b3-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ea7b3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea7b3-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7b3-108">Exemplo 1: Remover uma extensão de diagnóstico do VMSS</span><span class="sxs-lookup"><span data-stu-id="ea7b3-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="ea7b3-109">Esse comando remove a extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="ea7b3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea7b3-110">PARAMETERS</span></span>

### <span data-ttu-id="ea7b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7b3-111">-DefaultProfile</span></span>
<span data-ttu-id="ea7b3-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7b3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea7b3-113">-Name</span></span>
<span data-ttu-id="ea7b3-114">Especifica o nome da extensão que este cmdlet remove do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ea7b3-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ea7b3-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ea7b3-116">Especifica o VMSS do qual remover a extensão.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="ea7b3-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ea7b3-117">-Confirm</span></span>
<span data-ttu-id="ea7b3-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7b3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7b3-119">-WhatIf</span></span>
<span data-ttu-id="ea7b3-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7b3-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7b3-122">CommonParameters</span></span>
<span data-ttu-id="ea7b3-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7b3-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea7b3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7b3-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="ea7b3-125">INPUTS</span></span>

### <span data-ttu-id="ea7b3-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ea7b3-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ea7b3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ea7b3-127">System.String</span></span>

## <span data-ttu-id="ea7b3-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ea7b3-128">OUTPUTS</span></span>

### <span data-ttu-id="ea7b3-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ea7b3-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ea7b3-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ea7b3-130">NOTES</span></span>

## <span data-ttu-id="ea7b3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea7b3-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea7b3-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea7b3-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="ea7b3-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea7b3-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="ea7b3-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ea7b3-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


