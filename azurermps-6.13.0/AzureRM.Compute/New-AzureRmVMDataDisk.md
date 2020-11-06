---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
ms.openlocfilehash: 6eb86e0c2ddb8c5e3a46cf10f98bcea52ba03dd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432040"
---
# <span data-ttu-id="ddbbf-101">New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ddbbf-101">New-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="ddbbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbbf-103">Cria um objeto de disco de dados local para uma máquina virtual ou uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddbbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddbbf-104">SYNTAX</span></span>

### <span data-ttu-id="ddbbf-105">NormalDiskParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ddbbf-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddbbf-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ddbbf-106">ManagedDiskParameterSetName</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddbbf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddbbf-107">DESCRIPTION</span></span>
<span data-ttu-id="ddbbf-108">O cmdlet **New-AzureRmVMDataDisk** cria um objeto de disco de dados local para uma máquina virtual ou uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-108">The **New-AzureRmVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="ddbbf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddbbf-109">EXAMPLES</span></span>

### <span data-ttu-id="ddbbf-110">Exemplo 1: adicionar um disco de dados gerenciado a uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="ddbbf-111">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="ddbbf-112">O próximo comando cria um objeto de disco de dados com o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="ddbbf-113">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="ddbbf-114">O comando final atualiza a VM Vmss adicionando um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="ddbbf-115">OS</span><span class="sxs-lookup"><span data-stu-id="ddbbf-115">PARAMETERS</span></span>

### <span data-ttu-id="ddbbf-116">-Cache</span><span class="sxs-lookup"><span data-stu-id="ddbbf-116">-Caching</span></span>
<span data-ttu-id="ddbbf-117">O cache do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-118">-Createoption</span><span class="sxs-lookup"><span data-stu-id="ddbbf-118">-CreateOption</span></span>
<span data-ttu-id="ddbbf-119">A opção de criação do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbbf-120">-DefaultProfile</span></span>
<span data-ttu-id="ddbbf-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbbf-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ddbbf-122">-DiskSizeInGB</span></span>
<span data-ttu-id="ddbbf-123">O tamanho do disco dos dados da máquina virtual em GB.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="ddbbf-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="ddbbf-124">-Lun</span></span>
<span data-ttu-id="ddbbf-125">O LUN do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-125">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ddbbf-126">-ManagedDiskId</span></span>
<span data-ttu-id="ddbbf-127">A ID do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-127">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddbbf-128">-Name</span></span>
<span data-ttu-id="ddbbf-129">O nome do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="ddbbf-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="ddbbf-130">-SourceImageUri</span></span>
<span data-ttu-id="ddbbf-131">O URI da imagem de origem do disco do so da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-131">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ddbbf-132">-StorageAccountType</span></span>
<span data-ttu-id="ddbbf-133">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="ddbbf-134">-VhdUri</span></span>
<span data-ttu-id="ddbbf-135">O URI do VHD do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-135">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ddbbf-136">-WriteAccelerator</span></span>
<span data-ttu-id="ddbbf-137">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddbbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbbf-138">CommonParameters</span></span>
<span data-ttu-id="ddbbf-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbbf-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbbf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbbf-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddbbf-141">INPUTS</span></span>

### <span data-ttu-id="ddbbf-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ddbbf-142">System.Int32</span></span>

### <span data-ttu-id="ddbbf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbbf-143">System.String</span></span>

### <span data-ttu-id="ddbbf-144">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="ddbbf-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="ddbbf-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ddbbf-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ddbbf-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddbbf-146">OUTPUTS</span></span>

### <span data-ttu-id="ddbbf-147">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="ddbbf-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="ddbbf-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddbbf-148">NOTES</span></span>

## <span data-ttu-id="ddbbf-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddbbf-149">RELATED LINKS</span></span>
