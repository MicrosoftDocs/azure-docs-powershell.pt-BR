---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440495"
---
# <span data-ttu-id="56552-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="56552-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56552-102">SYNOPSIS</span></span>
<span data-ttu-id="56552-103">Interrompe o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="56552-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56552-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56552-104">SYNTAX</span></span>

### <span data-ttu-id="56552-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="56552-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56552-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="56552-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56552-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56552-107">DESCRIPTION</span></span>
<span data-ttu-id="56552-108">O cmdlet **Stop-AzureRmVmss** interrompe todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56552-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="56552-109">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56552-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="56552-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56552-110">EXAMPLES</span></span>

### <span data-ttu-id="56552-111">Exemplo 1: parar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="56552-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="56552-112">Esse comando interrompe todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="56552-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="56552-113">Exemplo 2: parar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="56552-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="56552-114">Esse comando para o conjunto específico de máquinas virtuais especificado pela matriz de cadeia de caracteres de ID de instância que pertence ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="56552-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="56552-115">OS</span><span class="sxs-lookup"><span data-stu-id="56552-115">PARAMETERS</span></span>

### <span data-ttu-id="56552-116">-Force</span><span class="sxs-lookup"><span data-stu-id="56552-116">-Force</span></span>
<span data-ttu-id="56552-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="56552-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56552-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="56552-118">-InstanceId</span></span>
<span data-ttu-id="56552-119">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias da máquina virtual em que esse cmdlet para.</span><span class="sxs-lookup"><span data-stu-id="56552-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="56552-120">Por exemplo: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="56552-120">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="56552-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56552-121">-ResourceGroupName</span></span>
<span data-ttu-id="56552-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="56552-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="56552-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="56552-123">-StayProvisioned</span></span>
<span data-ttu-id="56552-124">Se especificado, a máquina virtual irá entrar no estado parado.</span><span class="sxs-lookup"><span data-stu-id="56552-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="56552-125">Se não for especificado, a máquina virtual entrará no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="56552-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="56552-126">O usuário ainda é cobrado por VMs no estado parado, mas não para VMs no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="56552-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56552-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56552-127">-VMScaleSetName</span></span>
<span data-ttu-id="56552-128">Especifica o nome do VMSS para o qual esse cmdlet interrompe as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="56552-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="56552-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56552-129">-Confirm</span></span>
<span data-ttu-id="56552-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56552-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56552-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56552-131">-WhatIf</span></span>
<span data-ttu-id="56552-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56552-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56552-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56552-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56552-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56552-134">CommonParameters</span></span>
<span data-ttu-id="56552-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56552-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56552-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56552-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56552-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56552-137">INPUTS</span></span>

### <span data-ttu-id="56552-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="56552-138">None</span></span>
<span data-ttu-id="56552-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="56552-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56552-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56552-140">OUTPUTS</span></span>

## <span data-ttu-id="56552-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56552-141">NOTES</span></span>

## <span data-ttu-id="56552-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56552-142">RELATED LINKS</span></span>

[<span data-ttu-id="56552-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="56552-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="56552-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="56552-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="56552-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="56552-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="56552-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56552-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


