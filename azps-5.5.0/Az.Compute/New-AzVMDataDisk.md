---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112113"
---
# <span data-ttu-id="9939c-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9939c-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="9939c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9939c-102">SYNOPSIS</span></span>
<span data-ttu-id="9939c-103">Cria um objeto de disco de dados local para uma máquina virtual ou um VMSS.</span><span class="sxs-lookup"><span data-stu-id="9939c-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="9939c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9939c-104">SYNTAX</span></span>

### <span data-ttu-id="9939c-105">NormalDiskParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9939c-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9939c-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9939c-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9939c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9939c-107">DESCRIPTION</span></span>
<span data-ttu-id="9939c-108">O **cmdlet New-AzVMDataDisk** cria um objeto de disco de dados local para uma máquina virtual ou um VMSS.</span><span class="sxs-lookup"><span data-stu-id="9939c-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="9939c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9939c-109">EXAMPLES</span></span>

### <span data-ttu-id="9939c-110">Exemplo 1: Adicionar um disco de dados gerenciado a um VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="9939c-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="9939c-111">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="9939c-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="9939c-112">O próximo comando cria um objeto de disco de dados com o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9939c-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="9939c-113">O próximo comando obtém um VM Vmss existente dado pelo nome do grupo de recursos, pelo nome do vmss e pela ID da instância.</span><span class="sxs-lookup"><span data-stu-id="9939c-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="9939c-114">O comando final atualiza o VMSS adicionando um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9939c-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="9939c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9939c-115">Example 2</span></span>

<span data-ttu-id="9939c-116">Cria um objeto de disco de dados local para uma máquina virtual ou um VMSS.</span><span class="sxs-lookup"><span data-stu-id="9939c-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="9939c-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="9939c-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="9939c-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9939c-118">PARAMETERS</span></span>

### <span data-ttu-id="9939c-119">-Cache</span><span class="sxs-lookup"><span data-stu-id="9939c-119">-Caching</span></span>
<span data-ttu-id="9939c-120">O cache do disco de dados do computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="9939c-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="9939c-121">-CreateOption</span></span>
<span data-ttu-id="9939c-122">A opção criar disco de dados do computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="9939c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9939c-123">-DefaultProfile</span></span>
<span data-ttu-id="9939c-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9939c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9939c-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9939c-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9939c-126">A ID do conjunto de criptografia de disco gerenciado por computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-126">The virtual machine managed disk encryption set's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9939c-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9939c-127">-DiskSizeInGB</span></span>
<span data-ttu-id="9939c-128">O tamanho do disco de dados do computador virtual em GB.</span><span class="sxs-lookup"><span data-stu-id="9939c-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="9939c-129">-Ltda</span><span class="sxs-lookup"><span data-stu-id="9939c-129">-Lun</span></span>
<span data-ttu-id="9939c-130">O disco de dados virtual do computador.</span><span class="sxs-lookup"><span data-stu-id="9939c-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="9939c-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9939c-131">-ManagedDiskId</span></span>
<span data-ttu-id="9939c-132">A ID do disco virtual gerenciado pelo computador.</span><span class="sxs-lookup"><span data-stu-id="9939c-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="9939c-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="9939c-133">-Name</span></span>
<span data-ttu-id="9939c-134">O nome do disco de dados do computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="9939c-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="9939c-135">-SourceImageUri</span></span>
<span data-ttu-id="9939c-136">O Uri da imagem de origem do disco virtual do computador.</span><span class="sxs-lookup"><span data-stu-id="9939c-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="9939c-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9939c-137">-StorageAccountType</span></span>
<span data-ttu-id="9939c-138">O tipo de conta gerenciada pelo computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="9939c-139">-HighdUri</span><span class="sxs-lookup"><span data-stu-id="9939c-139">-VhdUri</span></span>
<span data-ttu-id="9939c-140">O Uri de datad Uri do computador virtual.</span><span class="sxs-lookup"><span data-stu-id="9939c-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="9939c-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9939c-141">-WriteAccelerator</span></span>
<span data-ttu-id="9939c-142">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9939c-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="9939c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9939c-143">CommonParameters</span></span>
<span data-ttu-id="9939c-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9939c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9939c-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9939c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9939c-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="9939c-146">INPUTS</span></span>

### <span data-ttu-id="9939c-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9939c-147">System.Int32</span></span>

### <span data-ttu-id="9939c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9939c-148">System.String</span></span>

### <span data-ttu-id="9939c-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="9939c-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="9939c-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9939c-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9939c-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="9939c-151">OUTPUTS</span></span>

### <span data-ttu-id="9939c-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="9939c-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="9939c-153">Notas</span><span class="sxs-lookup"><span data-stu-id="9939c-153">NOTES</span></span>

## <span data-ttu-id="9939c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9939c-154">RELATED LINKS</span></span>
