---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426761"
---
# <span data-ttu-id="8b8fa-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="8b8fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8fa-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b8fa-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b8fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b8fa-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8fa-106">O cmdlet **Update-AzureRmVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="8b8fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b8fa-107">EXAMPLES</span></span>

### <span data-ttu-id="8b8fa-108">Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="8b8fa-109">Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local chamado LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="8b8fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="8b8fa-110">PARAMETERS</span></span>

### <span data-ttu-id="8b8fa-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8fa-111">-ResourceGroupName</span></span>
<span data-ttu-id="8b8fa-112">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="8b8fa-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b8fa-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8b8fa-114">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="8b8fa-115">Para obter um objeto VMSS, use o cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="8b8fa-116">Esse objeto da máquina virtual contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8fa-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8b8fa-117">-VMScaleSetName</span></span>
<span data-ttu-id="8b8fa-118">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b8fa-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b8fa-119">-Confirm</span></span>
<span data-ttu-id="8b8fa-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b8fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b8fa-121">-WhatIf</span></span>
<span data-ttu-id="8b8fa-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8b8fa-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b8fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8fa-124">CommonParameters</span></span>
<span data-ttu-id="8b8fa-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8fa-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8fa-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b8fa-127">INPUTS</span></span>

### <span data-ttu-id="8b8fa-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8b8fa-128">None</span></span>
<span data-ttu-id="8b8fa-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8b8fa-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b8fa-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b8fa-130">OUTPUTS</span></span>

## <span data-ttu-id="8b8fa-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b8fa-131">NOTES</span></span>

## <span data-ttu-id="8b8fa-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b8fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b8fa-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="8b8fa-139">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b8fa-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


