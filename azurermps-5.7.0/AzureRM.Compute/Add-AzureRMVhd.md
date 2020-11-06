---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 7faa179ae8c8c43d750e4f042f7bc925b772f4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429890"
---
# <span data-ttu-id="fe88c-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="fe88c-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="fe88c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe88c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe88c-103">Carrega um disco rígido virtual de uma máquina virtual local para um blob em uma conta de armazenamento na nuvem no Azure.</span><span class="sxs-lookup"><span data-stu-id="fe88c-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe88c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe88c-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [<CommonParameters>]
```

## <span data-ttu-id="fe88c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe88c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe88c-106">O cmdlet **Add-AzureRmVhd** carrega discos rígidos virtuais locais, em formato de arquivo. VHD, para uma conta de armazenamento blob como discos rígidos virtuais fixos.</span><span class="sxs-lookup"><span data-stu-id="fe88c-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="fe88c-107">Você pode configurar o número de threads de upload que serão usados ou substituir um blob existente no URI de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="fe88c-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="fe88c-108">Também é compatível com a capacidade de carregar uma versão corrigida de um arquivo. vhd local.</span><span class="sxs-lookup"><span data-stu-id="fe88c-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="fe88c-109">Quando um disco rígido virtual básico já foi carregado, você pode carregar discos diferenciais que usam a imagem base como pai.</span><span class="sxs-lookup"><span data-stu-id="fe88c-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="fe88c-110">Também há suporte para URI de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="fe88c-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="fe88c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe88c-111">EXAMPLES</span></span>

### <span data-ttu-id="fe88c-112">Exemplo 1: adicionar um arquivo VHD</span><span class="sxs-lookup"><span data-stu-id="fe88c-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="fe88c-113">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe88c-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="fe88c-114">Exemplo 2: adicionar um arquivo VHD e substituir o destino</span><span class="sxs-lookup"><span data-stu-id="fe88c-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="fe88c-115">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe88c-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="fe88c-116">O comando substitui um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="fe88c-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="fe88c-117">Exemplo 3: adicionar um arquivo VHD e especificar o número de threads</span><span class="sxs-lookup"><span data-stu-id="fe88c-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="fe88c-118">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe88c-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="fe88c-119">O comando especifica o número de threads a serem usados para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fe88c-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="fe88c-120">Exemplo 4: adicionar um arquivo VHD e especificar o URI da SAS</span><span class="sxs-lookup"><span data-stu-id="fe88c-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="fe88c-121">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento e especifica o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="fe88c-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="fe88c-122">OS</span><span class="sxs-lookup"><span data-stu-id="fe88c-122">PARAMETERS</span></span>

### <span data-ttu-id="fe88c-123">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="fe88c-123">-BaseImageUriToPatch</span></span>
<span data-ttu-id="fe88c-124">Especifica o URI para um blob de imagem base no armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe88c-124">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="fe88c-125">Uma SAS pode ser especificada como o valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fe88c-125">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe88c-126">-Destino</span><span class="sxs-lookup"><span data-stu-id="fe88c-126">-Destination</span></span>
<span data-ttu-id="fe88c-127">Especifica o URI de um blob no armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="fe88c-127">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="fe88c-128">O parâmetro dá suporte a URI SAS, embora o destino dos cenários de correção não possa ser um URI de SAS.</span><span class="sxs-lookup"><span data-stu-id="fe88c-128">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe88c-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="fe88c-129">-LocalFilePath</span></span>
<span data-ttu-id="fe88c-130">Especifica o caminho do arquivo. vhd local.</span><span class="sxs-lookup"><span data-stu-id="fe88c-130">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe88c-131">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="fe88c-131">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="fe88c-132">Especifica o número de threads de carregamento a serem usados ao carregar o arquivo. vhd.</span><span class="sxs-lookup"><span data-stu-id="fe88c-132">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe88c-133">-Substituir</span><span class="sxs-lookup"><span data-stu-id="fe88c-133">-OverWrite</span></span>
<span data-ttu-id="fe88c-134">Indica que esse cmdlet substitui um blob existente no URI de destino especificado, caso haja um.</span><span class="sxs-lookup"><span data-stu-id="fe88c-134">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe88c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe88c-135">-ResourceGroupName</span></span>
<span data-ttu-id="fe88c-136">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe88c-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fe88c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe88c-137">CommonParameters</span></span>
<span data-ttu-id="fe88c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe88c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe88c-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe88c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe88c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe88c-140">INPUTS</span></span>

### <span data-ttu-id="fe88c-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fe88c-141">None</span></span>
<span data-ttu-id="fe88c-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fe88c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe88c-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe88c-143">OUTPUTS</span></span>

## <span data-ttu-id="fe88c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe88c-144">NOTES</span></span>

## <span data-ttu-id="fe88c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe88c-145">RELATED LINKS</span></span>

[<span data-ttu-id="fe88c-146">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="fe88c-146">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)

