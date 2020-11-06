---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 6c96114e7f3c430ca81679733d7bb3b007cab27f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441187"
---
# <span data-ttu-id="bb25a-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="bb25a-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="bb25a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb25a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb25a-103">Adiciona um disco de dados a um objeto de imagem.</span><span class="sxs-lookup"><span data-stu-id="bb25a-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb25a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb25a-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb25a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb25a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb25a-106">O cmdlet **Add-AzureRmImageDataDisk** adiciona um disco de dados a um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="bb25a-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="bb25a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb25a-107">EXAMPLES</span></span>

### <span data-ttu-id="bb25a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb25a-108">Example 1</span></span>
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

<span data-ttu-id="bb25a-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="bb25a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="bb25a-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="bb25a-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="bb25a-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb25a-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="bb25a-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="bb25a-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="bb25a-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="bb25a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="bb25a-114">O comando final cria uma imagem chamada ImageName01 na ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb25a-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="bb25a-115">OS</span><span class="sxs-lookup"><span data-stu-id="bb25a-115">PARAMETERS</span></span>

### <span data-ttu-id="bb25a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="bb25a-116">-BlobUri</span></span>
<span data-ttu-id="bb25a-117">Especifica o link, como um URI, do blob.</span><span class="sxs-lookup"><span data-stu-id="bb25a-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="bb25a-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="bb25a-118">-Caching</span></span>
<span data-ttu-id="bb25a-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="bb25a-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="bb25a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb25a-120">-DefaultProfile</span></span>
<span data-ttu-id="bb25a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb25a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb25a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="bb25a-122">-DiskSizeGB</span></span>
<span data-ttu-id="bb25a-123">Especifica o tamanho do disco em gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="bb25a-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="bb25a-124">-Imagem</span><span class="sxs-lookup"><span data-stu-id="bb25a-124">-Image</span></span>
<span data-ttu-id="bb25a-125">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="bb25a-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="bb25a-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="bb25a-126">-Lun</span></span>
<span data-ttu-id="bb25a-127">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="bb25a-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="bb25a-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="bb25a-128">-ManagedDiskId</span></span>
<span data-ttu-id="bb25a-129">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="bb25a-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="bb25a-130">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="bb25a-130">-SnapshotId</span></span>
<span data-ttu-id="bb25a-131">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bb25a-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="bb25a-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bb25a-132">-StorageAccountType</span></span>
<span data-ttu-id="bb25a-133">O tipo de conta de armazenamento do disco de imagem de dados</span><span class="sxs-lookup"><span data-stu-id="bb25a-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="bb25a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb25a-134">-Confirm</span></span>
<span data-ttu-id="bb25a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb25a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb25a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb25a-136">-WhatIf</span></span>
<span data-ttu-id="bb25a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb25a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb25a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb25a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb25a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb25a-139">CommonParameters</span></span>
<span data-ttu-id="bb25a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb25a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb25a-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb25a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb25a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb25a-142">INPUTS</span></span>

### <span data-ttu-id="bb25a-143">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="bb25a-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="bb25a-144">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bb25a-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bb25a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb25a-145">OUTPUTS</span></span>

### <span data-ttu-id="bb25a-146">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="bb25a-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="bb25a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb25a-147">NOTES</span></span>

## <span data-ttu-id="bb25a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb25a-148">RELATED LINKS</span></span>

