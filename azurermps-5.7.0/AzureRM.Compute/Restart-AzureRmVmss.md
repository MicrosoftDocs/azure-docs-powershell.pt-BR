---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440502"
---
# <span data-ttu-id="1f79a-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="1f79a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f79a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f79a-103">Reinicia o VMSS ou uma máquina virtual dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="1f79a-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f79a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f79a-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f79a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f79a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f79a-106">O cmdlet **Restart-AzureRmVmss** reinicia o conjunto de dimensionamento da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1f79a-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="1f79a-107">Esse cmdlet também pode ser usado para reiniciar uma máquina virtual específica dentro do VMSS usando o parâmetro *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="1f79a-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="1f79a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f79a-108">EXAMPLES</span></span>

### <span data-ttu-id="1f79a-109">Exemplo 1: reiniciar o VMSS</span><span class="sxs-lookup"><span data-stu-id="1f79a-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="1f79a-110">Esse comando reinicia o VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="1f79a-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="1f79a-111">Exemplo 2: reiniciar uma máquina virtual específica dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="1f79a-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="1f79a-112">Esse comando reinicia uma máquina virtual com a ID de instância 1 no VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="1f79a-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="1f79a-113">OS</span><span class="sxs-lookup"><span data-stu-id="1f79a-113">PARAMETERS</span></span>

### <span data-ttu-id="1f79a-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1f79a-114">-InstanceId</span></span>
<span data-ttu-id="1f79a-115">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser reiniciadas.</span><span class="sxs-lookup"><span data-stu-id="1f79a-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f79a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f79a-116">-ResourceGroupName</span></span>
<span data-ttu-id="1f79a-117">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="1f79a-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="1f79a-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1f79a-118">-VMScaleSetName</span></span>
<span data-ttu-id="1f79a-119">Especifica o nome do VMSS que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="1f79a-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="1f79a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f79a-120">-Confirm</span></span>
<span data-ttu-id="1f79a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f79a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f79a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f79a-122">-WhatIf</span></span>
<span data-ttu-id="1f79a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f79a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f79a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f79a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f79a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f79a-125">CommonParameters</span></span>
<span data-ttu-id="1f79a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f79a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f79a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f79a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f79a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f79a-128">INPUTS</span></span>

### <span data-ttu-id="1f79a-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1f79a-129">None</span></span>
<span data-ttu-id="1f79a-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1f79a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f79a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f79a-131">OUTPUTS</span></span>

###  
<span data-ttu-id="1f79a-132">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1f79a-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1f79a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f79a-133">NOTES</span></span>

## <span data-ttu-id="1f79a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f79a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f79a-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="1f79a-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="1f79a-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="1f79a-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="1f79a-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="1f79a-140">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="1f79a-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1f79a-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


