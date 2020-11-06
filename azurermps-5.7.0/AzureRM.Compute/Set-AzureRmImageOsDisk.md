---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426792"
---
# <span data-ttu-id="9fedd-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="9fedd-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="9fedd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fedd-102">SYNOPSIS</span></span>
<span data-ttu-id="9fedd-103">Define as propriedades de disco do sistema operacional em um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="9fedd-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fedd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fedd-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fedd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fedd-105">DESCRIPTION</span></span>
<span data-ttu-id="9fedd-106">O cmdlet **set-AzureRmImageOsDisk** define as propriedades de disco do sistema operacional em um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="9fedd-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="9fedd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fedd-107">EXAMPLES</span></span>

### <span data-ttu-id="9fedd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fedd-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="9fedd-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="9fedd-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="9fedd-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="9fedd-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="9fedd-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9fedd-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="9fedd-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="9fedd-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="9fedd-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="9fedd-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="9fedd-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9fedd-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9fedd-115">OS</span><span class="sxs-lookup"><span data-stu-id="9fedd-115">PARAMETERS</span></span>

### <span data-ttu-id="9fedd-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="9fedd-116">-BlobUri</span></span>
<span data-ttu-id="9fedd-117">Especifica o URI do blob.</span><span class="sxs-lookup"><span data-stu-id="9fedd-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="9fedd-118">-Caching</span></span>
<span data-ttu-id="9fedd-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="9fedd-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9fedd-120">-DiskSizeGB</span></span>
<span data-ttu-id="9fedd-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="9fedd-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="9fedd-122">-Imagem</span><span class="sxs-lookup"><span data-stu-id="9fedd-122">-Image</span></span>
<span data-ttu-id="9fedd-123">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="9fedd-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-124">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9fedd-124">-ManagedDiskId</span></span>
<span data-ttu-id="9fedd-125">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9fedd-125">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="9fedd-126">-OsState</span></span>
<span data-ttu-id="9fedd-127">Especifica o estado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9fedd-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="9fedd-128">-OsType</span></span>
<span data-ttu-id="9fedd-129">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9fedd-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-130">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="9fedd-130">-SnapshotId</span></span>
<span data-ttu-id="9fedd-131">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9fedd-131">Specifies the ID of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9fedd-132">-StorageAccountType</span></span>
<span data-ttu-id="9fedd-133">O tipo de conta de armazenamento do disco de imagem do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9fedd-133">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fedd-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fedd-134">-Confirm</span></span>
<span data-ttu-id="9fedd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fedd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fedd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fedd-136">-WhatIf</span></span>
<span data-ttu-id="9fedd-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fedd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fedd-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fedd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fedd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fedd-139">CommonParameters</span></span>
<span data-ttu-id="9fedd-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fedd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fedd-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fedd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fedd-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fedd-142">INPUTS</span></span>

### <span data-ttu-id="9fedd-143">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="9fedd-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="9fedd-144">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Anulável `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9fedd-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9fedd-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fedd-145">OUTPUTS</span></span>

### <span data-ttu-id="9fedd-146">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="9fedd-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="9fedd-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fedd-147">NOTES</span></span>

## <span data-ttu-id="9fedd-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fedd-148">RELATED LINKS</span></span>

