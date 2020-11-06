---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 5e04013ee8f9452ee28cf7975066f512e2eae1c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426994"
---
# <span data-ttu-id="a22cd-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a22cd-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="a22cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a22cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a22cd-103">Adiciona um disco de dados ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="a22cd-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a22cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a22cd-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a22cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a22cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a22cd-106">O cmdlet **Add-AzureRmVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="a22cd-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a22cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a22cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a22cd-108">Exemplo 1: adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="a22cd-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="a22cd-109">Esse comando adiciona um disco de dados vazio ao objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="a22cd-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="a22cd-110">OS</span><span class="sxs-lookup"><span data-stu-id="a22cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a22cd-111">-Cache</span><span class="sxs-lookup"><span data-stu-id="a22cd-111">-Caching</span></span>
<span data-ttu-id="a22cd-112">Especifica o tipo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="a22cd-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="a22cd-113">-Createoption</span><span class="sxs-lookup"><span data-stu-id="a22cd-113">-CreateOption</span></span>
<span data-ttu-id="a22cd-114">Especifica a opção criar do disco.</span><span class="sxs-lookup"><span data-stu-id="a22cd-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22cd-115">-DefaultProfile</span></span>
<span data-ttu-id="a22cd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a22cd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a22cd-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a22cd-117">-DiskSizeGB</span></span>
<span data-ttu-id="a22cd-118">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="a22cd-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="a22cd-119">-Lun</span></span>
<span data-ttu-id="a22cd-120">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="a22cd-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="a22cd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a22cd-121">-Name</span></span>
<span data-ttu-id="a22cd-122">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="a22cd-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="a22cd-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a22cd-123">-StorageAccountType</span></span>
<span data-ttu-id="a22cd-124">Especifica o tipo de conta de armazenamento do disco.</span><span class="sxs-lookup"><span data-stu-id="a22cd-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a22cd-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a22cd-126">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="a22cd-126">Specify the VMSS object.</span></span>
<span data-ttu-id="a22cd-127">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="a22cd-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a22cd-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a22cd-128">-Confirm</span></span>
<span data-ttu-id="a22cd-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a22cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a22cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a22cd-130">-WhatIf</span></span>
<span data-ttu-id="a22cd-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a22cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a22cd-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a22cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a22cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22cd-133">CommonParameters</span></span>
<span data-ttu-id="a22cd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22cd-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22cd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22cd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a22cd-136">INPUTS</span></span>

### <span data-ttu-id="a22cd-137">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a22cd-137">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="a22cd-138">Sistema System. String System. Int32. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a22cd-138">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a22cd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a22cd-139">OUTPUTS</span></span>

### <span data-ttu-id="a22cd-140">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a22cd-140">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="a22cd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a22cd-141">NOTES</span></span>

## <span data-ttu-id="a22cd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a22cd-142">RELATED LINKS</span></span>

