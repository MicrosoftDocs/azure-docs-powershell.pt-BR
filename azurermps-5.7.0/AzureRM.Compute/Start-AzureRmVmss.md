---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431038"
---
# <span data-ttu-id="a9a86-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="a9a86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9a86-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a86-103">Inicia o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9a86-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9a86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9a86-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9a86-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a86-106">O cmdlet **Start-AzureRmVmss** inicia todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a9a86-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="a9a86-107">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a9a86-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="a9a86-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9a86-108">EXAMPLES</span></span>

### <span data-ttu-id="a9a86-109">Exemplo 1: iniciar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="a9a86-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="a9a86-110">Esse comando inicia um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertence à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a9a86-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="a9a86-111">Exemplo 2: iniciar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="a9a86-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a9a86-112">Esse comando inicia todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a9a86-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a9a86-113">OS</span><span class="sxs-lookup"><span data-stu-id="a9a86-113">PARAMETERS</span></span>

### <span data-ttu-id="a9a86-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a9a86-114">-InstanceId</span></span>
<span data-ttu-id="a9a86-115">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="a9a86-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="a9a86-116">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="a9a86-116">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="a9a86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a86-117">-ResourceGroupName</span></span>
<span data-ttu-id="a9a86-118">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9a86-118">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a9a86-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a9a86-119">-VMScaleSetName</span></span>
<span data-ttu-id="a9a86-120">Especifica o nome do VMSS que este cmdlet inicia nas máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a9a86-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="a9a86-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9a86-121">-Confirm</span></span>
<span data-ttu-id="a9a86-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9a86-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a86-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a86-123">-WhatIf</span></span>
<span data-ttu-id="a9a86-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9a86-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9a86-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9a86-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a86-126">CommonParameters</span></span>
<span data-ttu-id="a9a86-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a86-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a86-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a86-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9a86-129">INPUTS</span></span>

### <span data-ttu-id="a9a86-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9a86-130">None</span></span>
<span data-ttu-id="a9a86-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a9a86-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9a86-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9a86-132">OUTPUTS</span></span>

###  
<span data-ttu-id="a9a86-133">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a9a86-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a9a86-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9a86-134">NOTES</span></span>

## <span data-ttu-id="a9a86-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9a86-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9a86-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a9a86-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a9a86-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a9a86-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a9a86-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a9a86-141">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a9a86-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a9a86-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


