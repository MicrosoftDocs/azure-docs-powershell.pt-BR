---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 5f723ea475ed909ee5445f3788386a2163af697d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602548"
---
# <span data-ttu-id="60cc7-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="60cc7-101">New-AzureRmImage</span></span>

## <span data-ttu-id="60cc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="60cc7-103">Cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="60cc7-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60cc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60cc7-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60cc7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="60cc7-106">O cmdlet **New-AzureRmImage** cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="60cc7-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="60cc7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="60cc7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60cc7-108">Example 1</span></span>
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

<span data-ttu-id="60cc7-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="60cc7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="60cc7-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="60cc7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="60cc7-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="60cc7-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="60cc7-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="60cc7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="60cc7-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="60cc7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="60cc7-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="60cc7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="60cc7-115">OS</span><span class="sxs-lookup"><span data-stu-id="60cc7-115">PARAMETERS</span></span>

### <span data-ttu-id="60cc7-116">-Imagem</span><span class="sxs-lookup"><span data-stu-id="60cc7-116">-Image</span></span>
<span data-ttu-id="60cc7-117">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="60cc7-117">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60cc7-118">-ImageName</span><span class="sxs-lookup"><span data-stu-id="60cc7-118">-ImageName</span></span>
<span data-ttu-id="60cc7-119">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="60cc7-119">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60cc7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cc7-120">-ResourceGroupName</span></span>
<span data-ttu-id="60cc7-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60cc7-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60cc7-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60cc7-122">-Confirm</span></span>
<span data-ttu-id="60cc7-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60cc7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60cc7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60cc7-124">-WhatIf</span></span>
<span data-ttu-id="60cc7-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60cc7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60cc7-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60cc7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60cc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cc7-127">CommonParameters</span></span>
<span data-ttu-id="60cc7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cc7-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cc7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cc7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60cc7-130">INPUTS</span></span>

### <span data-ttu-id="60cc7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="60cc7-131">System.String</span></span>
<span data-ttu-id="60cc7-132">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="60cc7-132">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="60cc7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60cc7-133">OUTPUTS</span></span>

### <span data-ttu-id="60cc7-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="60cc7-134">System.Object</span></span>

## <span data-ttu-id="60cc7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60cc7-135">NOTES</span></span>

## <span data-ttu-id="60cc7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60cc7-136">RELATED LINKS</span></span>

