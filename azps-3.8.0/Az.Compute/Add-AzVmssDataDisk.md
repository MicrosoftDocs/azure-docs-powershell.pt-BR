---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944906"
---
# <span data-ttu-id="d559e-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d559e-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="d559e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d559e-102">SYNOPSIS</span></span>
<span data-ttu-id="d559e-103">Adiciona um disco de dados ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="d559e-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="d559e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d559e-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d559e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d559e-105">DESCRIPTION</span></span>
<span data-ttu-id="d559e-106">O cmdlet **Add-AzVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="d559e-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d559e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d559e-107">EXAMPLES</span></span>

### <span data-ttu-id="d559e-108">Exemplo 1: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="d559e-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="d559e-109">Esse comando adiciona um disco de dados vazio ao objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d559e-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="d559e-110">OS</span><span class="sxs-lookup"><span data-stu-id="d559e-110">PARAMETERS</span></span>

### <span data-ttu-id="d559e-111">-Cache</span><span class="sxs-lookup"><span data-stu-id="d559e-111">-Caching</span></span>
<span data-ttu-id="d559e-112">Especifica o tipo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="d559e-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="d559e-113">-CreateOption</span></span>
<span data-ttu-id="d559e-114">Especifica a opção criar do disco.</span><span class="sxs-lookup"><span data-stu-id="d559e-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d559e-115">-DefaultProfile</span></span>
<span data-ttu-id="d559e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d559e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d559e-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d559e-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d559e-118">Especifica a ID do recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d559e-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d559e-119">Só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d559e-119">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="d559e-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="d559e-121">Especifica o Read-Write IOPS para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d559e-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="d559e-122">Deve ser usado somente quando o StorageAccountType está UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="d559e-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="d559e-123">Se não for especificado, um valor padrão será atribuído com base no diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="d559e-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="d559e-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="d559e-125">Especifica a largura de banda em MB por segundo para o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d559e-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="d559e-126">Deve ser usado somente quando o StorageAccountType está UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="d559e-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="d559e-127">Se não for especificado, um valor padrão será atribuído com base no diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="d559e-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d559e-128">-DiskSizeGB</span></span>
<span data-ttu-id="d559e-129">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="d559e-129">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="d559e-130">-Lun</span></span>
<span data-ttu-id="d559e-131">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="d559e-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="d559e-132">-Name</span></span>
<span data-ttu-id="d559e-133">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="d559e-133">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d559e-134">-StorageAccountType</span></span>
<span data-ttu-id="d559e-135">Especifica o tipo de conta de armazenamento do disco.</span><span class="sxs-lookup"><span data-stu-id="d559e-135">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d559e-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d559e-137">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d559e-137">Specify the VMSS object.</span></span>
<span data-ttu-id="d559e-138">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="d559e-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d559e-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d559e-139">-WriteAccelerator</span></span>
<span data-ttu-id="d559e-140">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="d559e-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d559e-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d559e-141">-Confirm</span></span>
<span data-ttu-id="d559e-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d559e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d559e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d559e-143">-WhatIf</span></span>
<span data-ttu-id="d559e-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d559e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d559e-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d559e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d559e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d559e-146">CommonParameters</span></span>
<span data-ttu-id="d559e-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d559e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d559e-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d559e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d559e-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d559e-149">INPUTS</span></span>

### <span data-ttu-id="d559e-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d559e-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d559e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d559e-151">System.String</span></span>

### <span data-ttu-id="d559e-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d559e-152">System.Int32</span></span>

### <span data-ttu-id="d559e-153">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d559e-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d559e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d559e-154">OUTPUTS</span></span>

### <span data-ttu-id="d559e-155">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d559e-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d559e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d559e-156">NOTES</span></span>

## <span data-ttu-id="d559e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d559e-157">RELATED LINKS</span></span>
