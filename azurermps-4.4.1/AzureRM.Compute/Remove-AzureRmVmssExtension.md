---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426955"
---
# <span data-ttu-id="ea25d-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ea25d-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="ea25d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea25d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea25d-103">Remove uma extensão da VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea25d-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea25d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea25d-104">SYNTAX</span></span>

### <span data-ttu-id="ea25d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea25d-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea25d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea25d-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea25d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea25d-107">DESCRIPTION</span></span>
<span data-ttu-id="ea25d-108">O cmdlet **Remove-AzureRmVmssExtension** remove uma extensão do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="ea25d-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ea25d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea25d-109">EXAMPLES</span></span>

## <span data-ttu-id="ea25d-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea25d-110">PARAMETERS</span></span>

### <span data-ttu-id="ea25d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea25d-111">-DefaultProfile</span></span>
<span data-ttu-id="ea25d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea25d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea25d-113">-ID</span><span class="sxs-lookup"><span data-stu-id="ea25d-113">-Id</span></span>
<span data-ttu-id="ea25d-114">Especifica a ID da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea25d-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ea25d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea25d-115">-Name</span></span>
<span data-ttu-id="ea25d-116">Especifica o nome da extensão que esse cmdlet Remove da VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea25d-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="ea25d-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ea25d-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ea25d-118">Especifica o VMSS do qual a extensão será removida.</span><span class="sxs-lookup"><span data-stu-id="ea25d-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="ea25d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea25d-119">-Confirm</span></span>
<span data-ttu-id="ea25d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea25d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea25d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea25d-121">-WhatIf</span></span>
<span data-ttu-id="ea25d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea25d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea25d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea25d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea25d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea25d-124">CommonParameters</span></span>
<span data-ttu-id="ea25d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea25d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea25d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea25d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea25d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea25d-127">INPUTS</span></span>

## <span data-ttu-id="ea25d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea25d-128">OUTPUTS</span></span>

### <span data-ttu-id="ea25d-129">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ea25d-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ea25d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea25d-130">NOTES</span></span>

## <span data-ttu-id="ea25d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea25d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea25d-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ea25d-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
