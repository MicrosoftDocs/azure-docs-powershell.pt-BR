---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: df4a3676d86027c4b2e8627e8eae87dcb84644c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601377"
---
# <span data-ttu-id="9d86f-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="9d86f-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="9d86f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d86f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d86f-103">Adiciona um disco de dados ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d86f-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="9d86f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d86f-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d86f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d86f-105">DESCRIPTION</span></span>
<span data-ttu-id="9d86f-106">O cmdlet **Add-AzVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="9d86f-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9d86f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d86f-107">EXAMPLES</span></span>

### <span data-ttu-id="9d86f-108">Exemplo 1: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="9d86f-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="9d86f-109">Esse comando adiciona um disco de dados vazio ao objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d86f-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="9d86f-110">OS</span><span class="sxs-lookup"><span data-stu-id="9d86f-110">PARAMETERS</span></span>

### <span data-ttu-id="9d86f-111">-Cache</span><span class="sxs-lookup"><span data-stu-id="9d86f-111">-Caching</span></span>
<span data-ttu-id="9d86f-112">Especifica o tipo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="9d86f-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="9d86f-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="9d86f-113">-CreateOption</span></span>
<span data-ttu-id="9d86f-114">Especifica a opção criar do disco.</span><span class="sxs-lookup"><span data-stu-id="9d86f-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="9d86f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d86f-115">-DefaultProfile</span></span>
<span data-ttu-id="9d86f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d86f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d86f-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9d86f-117">-DiskSizeGB</span></span>
<span data-ttu-id="9d86f-118">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="9d86f-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="9d86f-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="9d86f-119">-Lun</span></span>
<span data-ttu-id="9d86f-120">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="9d86f-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="9d86f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d86f-121">-Name</span></span>
<span data-ttu-id="9d86f-122">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="9d86f-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="9d86f-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9d86f-123">-StorageAccountType</span></span>
<span data-ttu-id="9d86f-124">Especifica o tipo de conta de armazenamento do disco.</span><span class="sxs-lookup"><span data-stu-id="9d86f-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="9d86f-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d86f-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9d86f-126">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9d86f-126">Specify the VMSS object.</span></span>
<span data-ttu-id="9d86f-127">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="9d86f-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9d86f-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9d86f-128">-WriteAccelerator</span></span>
<span data-ttu-id="9d86f-129">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9d86f-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="9d86f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d86f-130">-Confirm</span></span>
<span data-ttu-id="9d86f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d86f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d86f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d86f-132">-WhatIf</span></span>
<span data-ttu-id="9d86f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d86f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d86f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d86f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d86f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d86f-135">CommonParameters</span></span>
<span data-ttu-id="9d86f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d86f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d86f-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d86f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d86f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d86f-138">INPUTS</span></span>

### <span data-ttu-id="9d86f-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d86f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9d86f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9d86f-140">System.String</span></span>

### <span data-ttu-id="9d86f-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9d86f-141">System.Int32</span></span>

### <span data-ttu-id="9d86f-142">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9d86f-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="9d86f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d86f-143">OUTPUTS</span></span>

### <span data-ttu-id="9d86f-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d86f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9d86f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d86f-145">NOTES</span></span>

## <span data-ttu-id="9d86f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d86f-146">RELATED LINKS</span></span>
