---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434394"
---
# <span data-ttu-id="aa872-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="aa872-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="aa872-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa872-102">SYNOPSIS</span></span>
<span data-ttu-id="aa872-103">Adiciona um disco de dados a um objeto de imagem.</span><span class="sxs-lookup"><span data-stu-id="aa872-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="aa872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa872-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa872-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa872-105">DESCRIPTION</span></span>
<span data-ttu-id="aa872-106">O cmdlet **Add-AzImageDataDisk** adiciona um disco de dados a um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="aa872-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="aa872-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa872-107">EXAMPLES</span></span>

### <span data-ttu-id="aa872-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa872-108">Example 1</span></span>
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

<span data-ttu-id="aa872-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="aa872-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="aa872-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="aa872-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="aa872-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa872-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="aa872-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="aa872-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="aa872-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="aa872-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="aa872-114">O comando final cria uma imagem chamada ImageName01 na ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa872-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="aa872-115">OS</span><span class="sxs-lookup"><span data-stu-id="aa872-115">PARAMETERS</span></span>

### <span data-ttu-id="aa872-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="aa872-116">-BlobUri</span></span>
<span data-ttu-id="aa872-117">Especifica o link, como um URI, do blob.</span><span class="sxs-lookup"><span data-stu-id="aa872-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="aa872-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="aa872-118">-Caching</span></span>
<span data-ttu-id="aa872-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="aa872-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="aa872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa872-120">-DefaultProfile</span></span>
<span data-ttu-id="aa872-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa872-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa872-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="aa872-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="aa872-123">Especifica a ID do recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="aa872-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="aa872-124">Só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="aa872-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="aa872-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="aa872-125">-DiskSizeGB</span></span>
<span data-ttu-id="aa872-126">Especifica o tamanho do disco em gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="aa872-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="aa872-127">-Imagem</span><span class="sxs-lookup"><span data-stu-id="aa872-127">-Image</span></span>
<span data-ttu-id="aa872-128">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="aa872-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="aa872-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="aa872-129">-Lun</span></span>
<span data-ttu-id="aa872-130">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="aa872-130">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="aa872-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="aa872-131">-ManagedDiskId</span></span>
<span data-ttu-id="aa872-132">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="aa872-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="aa872-133">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="aa872-133">-SnapshotId</span></span>
<span data-ttu-id="aa872-134">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="aa872-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="aa872-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aa872-135">-StorageAccountType</span></span>
<span data-ttu-id="aa872-136">O tipo de conta de armazenamento do disco de imagem de dados</span><span class="sxs-lookup"><span data-stu-id="aa872-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="aa872-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa872-137">-Confirm</span></span>
<span data-ttu-id="aa872-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa872-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa872-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa872-139">-WhatIf</span></span>
<span data-ttu-id="aa872-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa872-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa872-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa872-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa872-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa872-142">CommonParameters</span></span>
<span data-ttu-id="aa872-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa872-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa872-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa872-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa872-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa872-145">INPUTS</span></span>

### <span data-ttu-id="aa872-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="aa872-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="aa872-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="aa872-147">System.Int32</span></span>

### <span data-ttu-id="aa872-148">System. String</span><span class="sxs-lookup"><span data-stu-id="aa872-148">System.String</span></span>

### <span data-ttu-id="aa872-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aa872-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="aa872-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa872-150">OUTPUTS</span></span>

### <span data-ttu-id="aa872-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="aa872-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="aa872-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa872-152">NOTES</span></span>

## <span data-ttu-id="aa872-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa872-153">RELATED LINKS</span></span>
