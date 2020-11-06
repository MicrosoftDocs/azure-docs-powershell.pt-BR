---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602871"
---
# <span data-ttu-id="5c4fa-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c4fa-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="5c4fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4fa-103">Adiciona um disco de dados ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c4fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c4fa-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="5c4fa-106">O cmdlet **Add-AzureRmVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="5c4fa-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="5c4fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="5c4fa-108">Exemplo 1: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="5c4fa-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="5c4fa-109">Esse comando adiciona um disco de dados vazio ao objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="5c4fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="5c4fa-110">PARAMETERS</span></span>

### <span data-ttu-id="5c4fa-111">-Cache</span><span class="sxs-lookup"><span data-stu-id="5c4fa-111">-Caching</span></span>
<span data-ttu-id="5c4fa-112">Especifica o tipo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="5c4fa-113">-CreateOption</span></span>
<span data-ttu-id="5c4fa-114">Especifica a opção criar do disco.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5c4fa-115">-DiskSizeGB</span></span>
<span data-ttu-id="5c4fa-116">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-116">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="5c4fa-117">-Lun</span></span>
<span data-ttu-id="5c4fa-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c4fa-119">-Name</span></span>
<span data-ttu-id="5c4fa-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5c4fa-121">-StorageAccountType</span></span>
<span data-ttu-id="5c4fa-122">Especifica o tipo de conta de armazenamento do disco.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-122">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c4fa-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c4fa-124">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-124">Specify the VMSS object.</span></span>
<span data-ttu-id="5c4fa-125">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4fa-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c4fa-126">-Confirm</span></span>
<span data-ttu-id="5c4fa-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4fa-128">-WhatIf</span></span>
<span data-ttu-id="5c4fa-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4fa-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4fa-131">CommonParameters</span></span>
<span data-ttu-id="5c4fa-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4fa-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4fa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4fa-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c4fa-134">INPUTS</span></span>

### <span data-ttu-id="5c4fa-135">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c4fa-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c4fa-136">Sistema System. String System. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5c4fa-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5c4fa-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c4fa-137">OUTPUTS</span></span>

### <span data-ttu-id="5c4fa-138">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c4fa-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="5c4fa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c4fa-139">NOTES</span></span>

## <span data-ttu-id="5c4fa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c4fa-140">RELATED LINKS</span></span>
