---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440503"
---
# <span data-ttu-id="1a5c1-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="1a5c1-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="1a5c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5c1-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a5c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a5c1-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a5c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1a5c1-106">O cmdlet **New-AzureRmImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="1a5c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a5c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1a5c1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a5c1-108">Example 1</span></span>
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

<span data-ttu-id="1a5c1-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="1a5c1-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="1a5c1-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="1a5c1-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="1a5c1-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="1a5c1-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1a5c1-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1a5c1-115">OS</span><span class="sxs-lookup"><span data-stu-id="1a5c1-115">PARAMETERS</span></span>

### <span data-ttu-id="1a5c1-116">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="1a5c1-116">-DataDisk</span></span>
<span data-ttu-id="1a5c1-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5c1-118">-Local</span><span class="sxs-lookup"><span data-stu-id="1a5c1-118">-Location</span></span>
<span data-ttu-id="1a5c1-119">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-119">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5c1-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="1a5c1-120">-OsDisk</span></span>
<span data-ttu-id="1a5c1-121">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5c1-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1a5c1-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="1a5c1-123">Especifica a ID da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-123">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5c1-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="1a5c1-124">-Tag</span></span>
<span data-ttu-id="1a5c1-125">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a5c1-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a5c1-126">-Confirm</span></span>
<span data-ttu-id="1a5c1-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a5c1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a5c1-128">-WhatIf</span></span>
<span data-ttu-id="1a5c1-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a5c1-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a5c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5c1-131">CommonParameters</span></span>
<span data-ttu-id="1a5c1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5c1-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5c1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5c1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a5c1-134">INPUTS</span></span>

### <span data-ttu-id="1a5c1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1a5c1-135">System.String</span></span>
<span data-ttu-id="1a5c1-136">System. Collections. Hashtable Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="1a5c1-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="1a5c1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a5c1-137">OUTPUTS</span></span>

### <span data-ttu-id="1a5c1-138">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="1a5c1-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="1a5c1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a5c1-139">NOTES</span></span>

## <span data-ttu-id="1a5c1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a5c1-140">RELATED LINKS</span></span>

