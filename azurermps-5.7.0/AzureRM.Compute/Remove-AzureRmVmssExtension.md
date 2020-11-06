---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429847"
---
# <span data-ttu-id="3d92e-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3d92e-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="3d92e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d92e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d92e-103">Remove uma extensão da VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d92e-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d92e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d92e-104">SYNTAX</span></span>

### <span data-ttu-id="3d92e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d92e-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d92e-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d92e-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d92e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d92e-107">DESCRIPTION</span></span>
<span data-ttu-id="3d92e-108">O cmdlet **Remove-AzureRmVmssExtension** remove uma extensão do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="3d92e-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3d92e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d92e-109">EXAMPLES</span></span>

## <span data-ttu-id="3d92e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d92e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d92e-111">-ID</span><span class="sxs-lookup"><span data-stu-id="3d92e-111">-Id</span></span>
<span data-ttu-id="3d92e-112">Especifica a ID da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d92e-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d92e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d92e-113">-Name</span></span>
<span data-ttu-id="3d92e-114">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="3d92e-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d92e-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d92e-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3d92e-116">Especifica o VMSS do qual a extensão será removida.</span><span class="sxs-lookup"><span data-stu-id="3d92e-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="3d92e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d92e-117">-Confirm</span></span>
<span data-ttu-id="3d92e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d92e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d92e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d92e-119">-WhatIf</span></span>
<span data-ttu-id="3d92e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d92e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d92e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d92e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d92e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d92e-122">CommonParameters</span></span>
<span data-ttu-id="3d92e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d92e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d92e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d92e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d92e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d92e-125">INPUTS</span></span>

### <span data-ttu-id="3d92e-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3d92e-126">None</span></span>
<span data-ttu-id="3d92e-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3d92e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d92e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d92e-128">OUTPUTS</span></span>

### <span data-ttu-id="3d92e-129">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3d92e-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3d92e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d92e-130">NOTES</span></span>

## <span data-ttu-id="3d92e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d92e-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d92e-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3d92e-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
