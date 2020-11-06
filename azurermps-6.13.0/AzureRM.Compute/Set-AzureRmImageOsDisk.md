---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 74dbe48c40dfa08df9fd224f43774095d10a539c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440818"
---
# <span data-ttu-id="cf623-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="cf623-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="cf623-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf623-102">SYNOPSIS</span></span>
<span data-ttu-id="cf623-103">Define as propriedades de disco do sistema operacional em um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="cf623-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf623-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf623-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf623-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf623-105">DESCRIPTION</span></span>
<span data-ttu-id="cf623-106">O cmdlet **set-AzureRmImageOsDisk** define as propriedades de disco do sistema operacional em um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="cf623-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="cf623-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf623-107">EXAMPLES</span></span>

### <span data-ttu-id="cf623-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf623-108">Example 1</span></span>
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

<span data-ttu-id="cf623-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="cf623-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="cf623-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="cf623-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="cf623-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf623-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="cf623-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="cf623-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="cf623-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="cf623-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="cf623-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cf623-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cf623-115">OS</span><span class="sxs-lookup"><span data-stu-id="cf623-115">PARAMETERS</span></span>

### <span data-ttu-id="cf623-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="cf623-116">-BlobUri</span></span>
<span data-ttu-id="cf623-117">Especifica o URI do blob.</span><span class="sxs-lookup"><span data-stu-id="cf623-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="cf623-118">-Cache</span><span class="sxs-lookup"><span data-stu-id="cf623-118">-Caching</span></span>
<span data-ttu-id="cf623-119">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="cf623-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="cf623-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf623-120">-DefaultProfile</span></span>
<span data-ttu-id="cf623-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf623-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf623-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cf623-122">-DiskSizeGB</span></span>
<span data-ttu-id="cf623-123">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="cf623-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="cf623-124">-Imagem</span><span class="sxs-lookup"><span data-stu-id="cf623-124">-Image</span></span>
<span data-ttu-id="cf623-125">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="cf623-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="cf623-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="cf623-126">-ManagedDiskId</span></span>
<span data-ttu-id="cf623-127">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf623-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="cf623-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="cf623-128">-OsState</span></span>
<span data-ttu-id="cf623-129">Especifica o estado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf623-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="cf623-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="cf623-130">-OsType</span></span>
<span data-ttu-id="cf623-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cf623-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="cf623-132">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="cf623-132">-SnapshotId</span></span>
<span data-ttu-id="cf623-133">Especifica a ID de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cf623-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="cf623-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cf623-134">-StorageAccountType</span></span>
<span data-ttu-id="cf623-135">O tipo de conta de armazenamento do disco de imagem do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="cf623-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="cf623-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf623-136">-Confirm</span></span>
<span data-ttu-id="cf623-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf623-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf623-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf623-138">-WhatIf</span></span>
<span data-ttu-id="cf623-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf623-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf623-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf623-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf623-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf623-141">CommonParameters</span></span>
<span data-ttu-id="cf623-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf623-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf623-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf623-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf623-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf623-144">INPUTS</span></span>

### <span data-ttu-id="cf623-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="cf623-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="cf623-146">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf623-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cf623-147">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf623-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cf623-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cf623-148">System.String</span></span>

### <span data-ttu-id="cf623-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf623-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cf623-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cf623-150">System.Int32</span></span>

## <span data-ttu-id="cf623-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf623-151">OUTPUTS</span></span>

### <span data-ttu-id="cf623-152">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="cf623-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="cf623-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf623-153">NOTES</span></span>

## <span data-ttu-id="cf623-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf623-154">RELATED LINKS</span></span>
