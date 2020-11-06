---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431052"
---
# <span data-ttu-id="49f82-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="49f82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49f82-102">SYNOPSIS</span></span>
<span data-ttu-id="49f82-103">Remove o VMSS ou uma máquina virtual que está dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="49f82-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49f82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49f82-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f82-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49f82-105">DESCRIPTION</span></span>
<span data-ttu-id="49f82-106">O cmdlet **Remove-AzureRmVmss** remove o VMSS (conjunto de escala da máquina virtual) do Azure.</span><span class="sxs-lookup"><span data-stu-id="49f82-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="49f82-107">Esse cmdlet também pode ser usado para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="49f82-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="49f82-108">Você pode usar o parâmetro *InstanceId* para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="49f82-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="49f82-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49f82-109">EXAMPLES</span></span>

### <span data-ttu-id="49f82-110">Exemplo 1: remover um VMSS</span><span class="sxs-lookup"><span data-stu-id="49f82-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="49f82-111">Esse comando Remove a VMSS chamada VMScaleSet001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="49f82-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="49f82-112">Exemplo 2: remover uma máquina virtual de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="49f82-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="49f82-113">Esse comando Remove a máquina virtual com a ID de instância 3 da VMSS chamada VMScaleSet002 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="49f82-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="49f82-114">OS</span><span class="sxs-lookup"><span data-stu-id="49f82-114">PARAMETERS</span></span>

### <span data-ttu-id="49f82-115">-Force</span><span class="sxs-lookup"><span data-stu-id="49f82-115">-Force</span></span>
<span data-ttu-id="49f82-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="49f82-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f82-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="49f82-117">-InstanceId</span></span>
<span data-ttu-id="49f82-118">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="49f82-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="49f82-119">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="49f82-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="49f82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f82-120">-ResourceGroupName</span></span>
<span data-ttu-id="49f82-121">Especifica o nome do grupo de recursos ao qual o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="49f82-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="49f82-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="49f82-122">-VMScaleSetName</span></span>
<span data-ttu-id="49f82-123">Especifica o nome do VMSS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="49f82-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="49f82-124">Se você especificar o parâmetro *InstanceId* , o cmdlet removerá a máquina virtual especificada do VMSS nomeado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49f82-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="49f82-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49f82-125">-Confirm</span></span>
<span data-ttu-id="49f82-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f82-126">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="49f82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f82-127">-WhatIf</span></span>
<span data-ttu-id="49f82-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49f82-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49f82-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49f82-129">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="49f82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f82-130">CommonParameters</span></span>
<span data-ttu-id="49f82-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f82-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f82-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f82-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49f82-133">INPUTS</span></span>

### <span data-ttu-id="49f82-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="49f82-134">None</span></span>
<span data-ttu-id="49f82-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="49f82-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49f82-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49f82-136">OUTPUTS</span></span>

## <span data-ttu-id="49f82-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49f82-137">NOTES</span></span>

## <span data-ttu-id="49f82-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49f82-138">RELATED LINKS</span></span>

[<span data-ttu-id="49f82-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="49f82-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="49f82-141">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="49f82-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="49f82-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="49f82-144">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="49f82-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49f82-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


