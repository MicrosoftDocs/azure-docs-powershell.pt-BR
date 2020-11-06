---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431050"
---
# <span data-ttu-id="52f04-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="52f04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52f04-102">SYNOPSIS</span></span>
<span data-ttu-id="52f04-103">Define ações específicas em um VMSS especificado.</span><span class="sxs-lookup"><span data-stu-id="52f04-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52f04-104">SYNTAX</span></span>

### <span data-ttu-id="52f04-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="52f04-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52f04-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="52f04-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52f04-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52f04-107">DESCRIPTION</span></span>
<span data-ttu-id="52f04-108">O cmdlet **set-AzureRmVmss** define ações específicas no conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="52f04-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="52f04-109">A única ação aceita por este cmdlet é a reimagem.</span><span class="sxs-lookup"><span data-stu-id="52f04-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="52f04-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52f04-110">EXAMPLES</span></span>

### <span data-ttu-id="52f04-111">Exemplo 1: reimagem de um VMSS</span><span class="sxs-lookup"><span data-stu-id="52f04-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="52f04-112">Esse comando faz a nova imagem do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="52f04-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="52f04-113">OS</span><span class="sxs-lookup"><span data-stu-id="52f04-113">PARAMETERS</span></span>

### <span data-ttu-id="52f04-114">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="52f04-114">-Reimage</span></span>
<span data-ttu-id="52f04-115">Indica que o cmdlet reimagemia o VMSS.</span><span class="sxs-lookup"><span data-stu-id="52f04-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f04-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="52f04-116">-ReimageAll</span></span>
<span data-ttu-id="52f04-117">Indica que o cmdlet reimagemia todos os discos no VMSS.</span><span class="sxs-lookup"><span data-stu-id="52f04-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f04-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f04-118">-ResourceGroupName</span></span>
<span data-ttu-id="52f04-119">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="52f04-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f04-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="52f04-120">-VMScaleSetName</span></span>
<span data-ttu-id="52f04-121">Especifica o nome do VMSS para o qual esse cmdlet define ações.</span><span class="sxs-lookup"><span data-stu-id="52f04-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f04-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52f04-122">-Confirm</span></span>
<span data-ttu-id="52f04-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f04-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f04-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f04-124">-WhatIf</span></span>
<span data-ttu-id="52f04-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52f04-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52f04-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52f04-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f04-127">CommonParameters</span></span>
<span data-ttu-id="52f04-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f04-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f04-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f04-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52f04-130">INPUTS</span></span>

### <span data-ttu-id="52f04-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="52f04-131">None</span></span>
<span data-ttu-id="52f04-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="52f04-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52f04-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52f04-133">OUTPUTS</span></span>

### <span data-ttu-id="52f04-134">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="52f04-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="52f04-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52f04-135">NOTES</span></span>

## <span data-ttu-id="52f04-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52f04-136">RELATED LINKS</span></span>

[<span data-ttu-id="52f04-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="52f04-138">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="52f04-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="52f04-140">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="52f04-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="52f04-142">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="52f04-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52f04-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


