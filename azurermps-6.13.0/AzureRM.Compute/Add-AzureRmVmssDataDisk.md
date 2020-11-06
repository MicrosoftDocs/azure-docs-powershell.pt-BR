---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 0ef680f60f48451e5d5dd9bff730cbfe4ebc9aae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431374"
---
# <span data-ttu-id="7bf49-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="7bf49-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="7bf49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bf49-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf49-103">Adiciona um disco de dados ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="7bf49-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bf49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bf49-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bf49-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf49-106">O cmdlet **Add-AzureRmVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="7bf49-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="7bf49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bf49-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf49-108">Exemplo 1: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="7bf49-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="7bf49-109">Esse comando adiciona um disco de dados vazio ao objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7bf49-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="7bf49-110">OS</span><span class="sxs-lookup"><span data-stu-id="7bf49-110">PARAMETERS</span></span>

### <span data-ttu-id="7bf49-111">-Cache</span><span class="sxs-lookup"><span data-stu-id="7bf49-111">-Caching</span></span>
<span data-ttu-id="7bf49-112">Especifica o tipo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="7bf49-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="7bf49-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="7bf49-113">-CreateOption</span></span>
<span data-ttu-id="7bf49-114">Especifica a opção criar do disco.</span><span class="sxs-lookup"><span data-stu-id="7bf49-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="7bf49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf49-115">-DefaultProfile</span></span>
<span data-ttu-id="7bf49-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf49-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7bf49-117">-DiskSizeGB</span></span>
<span data-ttu-id="7bf49-118">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="7bf49-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7bf49-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="7bf49-119">-Lun</span></span>
<span data-ttu-id="7bf49-120">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="7bf49-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="7bf49-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bf49-121">-Name</span></span>
<span data-ttu-id="7bf49-122">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="7bf49-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="7bf49-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7bf49-123">-StorageAccountType</span></span>
<span data-ttu-id="7bf49-124">Especifica o tipo de conta de armazenamento do disco.</span><span class="sxs-lookup"><span data-stu-id="7bf49-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="7bf49-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bf49-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7bf49-126">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7bf49-126">Specify the VMSS object.</span></span>
<span data-ttu-id="7bf49-127">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="7bf49-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="7bf49-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7bf49-128">-WriteAccelerator</span></span>
<span data-ttu-id="7bf49-129">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.</span><span class="sxs-lookup"><span data-stu-id="7bf49-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="7bf49-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bf49-130">-Confirm</span></span>
<span data-ttu-id="7bf49-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bf49-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf49-132">-WhatIf</span></span>
<span data-ttu-id="7bf49-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bf49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bf49-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bf49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf49-135">CommonParameters</span></span>
<span data-ttu-id="7bf49-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf49-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bf49-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf49-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bf49-138">INPUTS</span></span>

### <span data-ttu-id="7bf49-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bf49-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7bf49-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7bf49-140">System.String</span></span>

### <span data-ttu-id="7bf49-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7bf49-141">System.Int32</span></span>

### <span data-ttu-id="7bf49-142">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7bf49-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7bf49-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bf49-143">OUTPUTS</span></span>

### <span data-ttu-id="7bf49-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7bf49-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7bf49-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bf49-145">NOTES</span></span>

## <span data-ttu-id="7bf49-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bf49-146">RELATED LINKS</span></span>
