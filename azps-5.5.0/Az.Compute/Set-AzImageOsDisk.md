---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117826"
---
# <span data-ttu-id="eadbf-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="eadbf-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="eadbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eadbf-102">SYNOPSIS</span></span>
<span data-ttu-id="eadbf-103">Define as propriedades de disco do sistema operacional em um objeto de imagem.</span><span class="sxs-lookup"><span data-stu-id="eadbf-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="eadbf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eadbf-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eadbf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eadbf-105">DESCRIPTION</span></span>
<span data-ttu-id="eadbf-106">O **cmdlet Set-AzImageOsDisk** define as propriedades de disco do sistema operacional em um objeto de imagem.</span><span class="sxs-lookup"><span data-stu-id="eadbf-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="eadbf-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eadbf-107">EXAMPLES</span></span>

### <span data-ttu-id="eadbf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eadbf-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="eadbf-109">O primeiro comando cria um objeto de imagem e o armazena na variável $imageConfig imagem.</span><span class="sxs-lookup"><span data-stu-id="eadbf-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="eadbf-110">Os três comandos a seguir atribuem caminhos de disco do sistema operacional e dois discos de dados às variáveis $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="eadbf-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="eadbf-111">Esta abordagem é apenas para a capacidade de leitura dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="eadbf-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="eadbf-112">Os três comandos a seguir adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="eadbf-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="eadbf-113">O URI de cada disco é armazenado $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="eadbf-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="eadbf-114">O comando final cria uma imagem chamada 'ImageName01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="eadbf-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eadbf-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eadbf-115">PARAMETERS</span></span>

### <span data-ttu-id="eadbf-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="eadbf-116">-BlobUri</span></span>
<span data-ttu-id="eadbf-117">Especifica o Uri do blob.</span><span class="sxs-lookup"><span data-stu-id="eadbf-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eadbf-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="eadbf-118">-Caching</span></span>
<span data-ttu-id="eadbf-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="eadbf-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eadbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadbf-120">-DefaultProfile</span></span>
<span data-ttu-id="eadbf-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eadbf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eadbf-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="eadbf-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="eadbf-123">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="eadbf-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="eadbf-124">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="eadbf-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="eadbf-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="eadbf-125">-DiskSizeGB</span></span>
<span data-ttu-id="eadbf-126">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="eadbf-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="eadbf-127">-Imagem</span><span class="sxs-lookup"><span data-stu-id="eadbf-127">-Image</span></span>
<span data-ttu-id="eadbf-128">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="eadbf-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eadbf-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="eadbf-129">-ManagedDiskId</span></span>
<span data-ttu-id="eadbf-130">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="eadbf-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="eadbf-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="eadbf-131">-OsState</span></span>
<span data-ttu-id="eadbf-132">Especifica o estado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="eadbf-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eadbf-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="eadbf-133">-OsType</span></span>
<span data-ttu-id="eadbf-134">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="eadbf-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eadbf-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="eadbf-135">-SnapshotId</span></span>
<span data-ttu-id="eadbf-136">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="eadbf-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="eadbf-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="eadbf-137">-StorageAccountType</span></span>
<span data-ttu-id="eadbf-138">O tipo de Conta de Armazenamento do Disco de Imagem do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="eadbf-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="eadbf-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eadbf-139">-Confirm</span></span>
<span data-ttu-id="eadbf-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eadbf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadbf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadbf-141">-WhatIf</span></span>
<span data-ttu-id="eadbf-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eadbf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eadbf-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eadbf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadbf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadbf-144">CommonParameters</span></span>
<span data-ttu-id="eadbf-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eadbf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadbf-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eadbf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadbf-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="eadbf-147">INPUTS</span></span>

### <span data-ttu-id="eadbf-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="eadbf-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="eadbf-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eadbf-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eadbf-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eadbf-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eadbf-151">System.String</span><span class="sxs-lookup"><span data-stu-id="eadbf-151">System.String</span></span>

### <span data-ttu-id="eadbf-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eadbf-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eadbf-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="eadbf-153">System.Int32</span></span>

## <span data-ttu-id="eadbf-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="eadbf-154">OUTPUTS</span></span>

### <span data-ttu-id="eadbf-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="eadbf-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="eadbf-156">Notas</span><span class="sxs-lookup"><span data-stu-id="eadbf-156">NOTES</span></span>

## <span data-ttu-id="eadbf-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eadbf-157">RELATED LINKS</span></span>
