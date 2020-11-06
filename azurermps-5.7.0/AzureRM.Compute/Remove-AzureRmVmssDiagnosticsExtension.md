---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429895"
---
# <span data-ttu-id="4357b-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4357b-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="4357b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4357b-102">SYNOPSIS</span></span>
<span data-ttu-id="4357b-103">Remove uma extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4357b-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4357b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4357b-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4357b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4357b-105">DESCRIPTION</span></span>
<span data-ttu-id="4357b-106">O cmdlet **Remove-AzureRmVmssDiagnosticsExtension** remove uma extensão de diagnóstico do conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4357b-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4357b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4357b-107">EXAMPLES</span></span>

### <span data-ttu-id="4357b-108">Exemplo 1: remover uma extensão de diagnóstico do VMSS</span><span class="sxs-lookup"><span data-stu-id="4357b-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="4357b-109">Esse comando Remove a extensão de diagnóstico do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4357b-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="4357b-110">OS</span><span class="sxs-lookup"><span data-stu-id="4357b-110">PARAMETERS</span></span>

### <span data-ttu-id="4357b-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="4357b-111">-Name</span></span>
<span data-ttu-id="4357b-112">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="4357b-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4357b-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4357b-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4357b-114">Especifica o VMSS a partir do qual a extensão deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="4357b-114">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4357b-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4357b-115">-Confirm</span></span>
<span data-ttu-id="4357b-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4357b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4357b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4357b-117">-WhatIf</span></span>
<span data-ttu-id="4357b-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4357b-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4357b-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4357b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4357b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4357b-120">CommonParameters</span></span>
<span data-ttu-id="4357b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4357b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4357b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4357b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4357b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4357b-123">INPUTS</span></span>

### <span data-ttu-id="4357b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4357b-124">None</span></span>
<span data-ttu-id="4357b-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4357b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4357b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4357b-126">OUTPUTS</span></span>

###  
<span data-ttu-id="4357b-127">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4357b-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4357b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4357b-128">NOTES</span></span>

## <span data-ttu-id="4357b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4357b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4357b-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4357b-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="4357b-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4357b-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="4357b-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4357b-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


