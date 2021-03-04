---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: a5876f705749d1391540bffdf537899e29b9560d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889032"
---
# <span data-ttu-id="e28a8-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="e28a8-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="e28a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e28a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e28a8-103">Adiciona um disco de dados a um objeto image.</span><span class="sxs-lookup"><span data-stu-id="e28a8-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="e28a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e28a8-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e28a8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e28a8-105">DESCRIPTION</span></span>
<span data-ttu-id="e28a8-106">O cmdlet **Add-AzImageDataDisk** adiciona um disco de dados a um objeto image.</span><span class="sxs-lookup"><span data-stu-id="e28a8-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="e28a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e28a8-107">EXAMPLES</span></span>

### <span data-ttu-id="e28a8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e28a8-108">Example 1</span></span>
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

<span data-ttu-id="e28a8-109">O primeiro comando cria um objeto image e o armazena na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e28a8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="e28a8-110">Os três comandos a seguir atribuem caminhos de disco do sistema operacional e dois discos de dados às variáveis $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e28a8-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="e28a8-111">Essa abordagem é apenas para a capacidade de leitura dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="e28a8-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e28a8-112">Os três comandos a seguir adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e28a8-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e28a8-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e28a8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="e28a8-114">O comando final cria uma imagem chamada ImageName01 no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e28a8-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e28a8-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e28a8-115">PARAMETERS</span></span>

### <span data-ttu-id="e28a8-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="e28a8-116">-BlobUri</span></span>
<span data-ttu-id="e28a8-117">Especifica o link, como um URI, do blob.</span><span class="sxs-lookup"><span data-stu-id="e28a8-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28a8-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="e28a8-118">-Caching</span></span>
<span data-ttu-id="e28a8-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="e28a8-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="e28a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28a8-120">-DefaultProfile</span></span>
<span data-ttu-id="e28a8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e28a8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e28a8-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e28a8-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e28a8-123">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="e28a8-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e28a8-124">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e28a8-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e28a8-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e28a8-125">-DiskSizeGB</span></span>
<span data-ttu-id="e28a8-126">Especifica o tamanho do disco em Gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="e28a8-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="e28a8-127">-Image</span><span class="sxs-lookup"><span data-stu-id="e28a8-127">-Image</span></span>
<span data-ttu-id="e28a8-128">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="e28a8-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="e28a8-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="e28a8-129">-Lun</span></span>
<span data-ttu-id="e28a8-130">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="e28a8-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28a8-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e28a8-131">-ManagedDiskId</span></span>
<span data-ttu-id="e28a8-132">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e28a8-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e28a8-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="e28a8-133">-SnapshotId</span></span>
<span data-ttu-id="e28a8-134">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e28a8-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="e28a8-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e28a8-135">-StorageAccountType</span></span>
<span data-ttu-id="e28a8-136">O tipo de Conta de Armazenamento do disco de imagem de dados</span><span class="sxs-lookup"><span data-stu-id="e28a8-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="e28a8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e28a8-137">-Confirm</span></span>
<span data-ttu-id="e28a8-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e28a8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e28a8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28a8-139">-WhatIf</span></span>
<span data-ttu-id="e28a8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e28a8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e28a8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e28a8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e28a8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28a8-142">CommonParameters</span></span>
<span data-ttu-id="e28a8-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e28a8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28a8-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e28a8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28a8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e28a8-145">INPUTS</span></span>

### <span data-ttu-id="e28a8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e28a8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="e28a8-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e28a8-147">System.Int32</span></span>

### <span data-ttu-id="e28a8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e28a8-148">System.String</span></span>

### <span data-ttu-id="e28a8-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e28a8-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e28a8-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e28a8-150">OUTPUTS</span></span>

### <span data-ttu-id="e28a8-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e28a8-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e28a8-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="e28a8-152">NOTES</span></span>

## <span data-ttu-id="e28a8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e28a8-153">RELATED LINKS</span></span>
