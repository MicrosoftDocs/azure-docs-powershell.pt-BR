---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945718"
---
# <span data-ttu-id="d1daa-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d1daa-101">Add-AzureVhd</span></span>

## <span data-ttu-id="d1daa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1daa-102">SYNOPSIS</span></span>
<span data-ttu-id="d1daa-103">Carrega um arquivo VHD de um computador local para um blob em uma conta de armazenamento na nuvem no Azure.</span><span class="sxs-lookup"><span data-stu-id="d1daa-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="d1daa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1daa-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1daa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1daa-105">DESCRIPTION</span></span>
<span data-ttu-id="d1daa-106">O cmdlet **Add-AzureVhd** carrega imagens do VHD (disco rígido virtual) local para uma conta de armazenamento blob como imagens. vhd fixadas.</span><span class="sxs-lookup"><span data-stu-id="d1daa-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="d1daa-107">Ele tem parâmetros para configurar o processo de carregamento, como especificar o número de threads de upload que serão usados ou substituir um blob que já existe no URI de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="d1daa-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="d1daa-108">Para imagens VHD locais, o cenário de patch também tem suporte para que as imagens de disco de comparação possam ser carregadas sem precisar carregar as imagens base já carregadas.</span><span class="sxs-lookup"><span data-stu-id="d1daa-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="d1daa-109">Também há suporte para URI de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="d1daa-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="d1daa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1daa-110">EXAMPLES</span></span>

### <span data-ttu-id="d1daa-111">Exemplo 1: adicionar um arquivo VHD</span><span class="sxs-lookup"><span data-stu-id="d1daa-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="d1daa-112">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d1daa-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d1daa-113">Exemplo 2: adicionar um arquivo VHD e substituir o destino</span><span class="sxs-lookup"><span data-stu-id="d1daa-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="d1daa-114">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d1daa-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d1daa-115">Exemplo 3: adicionar um arquivo VHD e especificar o número de threads</span><span class="sxs-lookup"><span data-stu-id="d1daa-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="d1daa-116">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento e especifica o número de threads a serem usados para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d1daa-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="d1daa-117">Exemplo 4: adicionar um arquivo VHD e especificar o URI da SAS</span><span class="sxs-lookup"><span data-stu-id="d1daa-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="d1daa-118">Esse comando adiciona um arquivo. vhd a uma conta de armazenamento e especifica o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="d1daa-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="d1daa-119">OS</span><span class="sxs-lookup"><span data-stu-id="d1daa-119">PARAMETERS</span></span>

### <span data-ttu-id="d1daa-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="d1daa-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="d1daa-121">Especifica um URI para um blob de imagem base no armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1daa-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="d1daa-122">Também há suporte para SAS na entrada de URI.</span><span class="sxs-lookup"><span data-stu-id="d1daa-122">SAS in URI input is supported as well.</span></span>

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

### <span data-ttu-id="d1daa-123">-Destino</span><span class="sxs-lookup"><span data-stu-id="d1daa-123">-Destination</span></span>
<span data-ttu-id="d1daa-124">Especifica um URI para um blob no armazenamento de blob do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1daa-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="d1daa-125">Há suporte para SAS na entrada de URI.</span><span class="sxs-lookup"><span data-stu-id="d1daa-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="d1daa-126">No entanto, em cenários de patch, o destino não pode ser um URI de SAS.</span><span class="sxs-lookup"><span data-stu-id="d1daa-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

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

### <span data-ttu-id="d1daa-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d1daa-127">-InformationAction</span></span>
<span data-ttu-id="d1daa-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d1daa-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d1daa-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d1daa-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1daa-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d1daa-130">Continue</span></span>
- <span data-ttu-id="d1daa-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d1daa-131">Ignore</span></span>
- <span data-ttu-id="d1daa-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="d1daa-132">Inquire</span></span>
- <span data-ttu-id="d1daa-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d1daa-133">SilentlyContinue</span></span>
- <span data-ttu-id="d1daa-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d1daa-134">Stop</span></span>
- <span data-ttu-id="d1daa-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d1daa-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1daa-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d1daa-136">-InformationVariable</span></span>
<span data-ttu-id="d1daa-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d1daa-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1daa-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d1daa-138">-LocalFilePath</span></span>
<span data-ttu-id="d1daa-139">Especifica o caminho do arquivo do arquivo. vhd local.</span><span class="sxs-lookup"><span data-stu-id="d1daa-139">Species the file path of the local .vhd file.</span></span>

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

### <span data-ttu-id="d1daa-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="d1daa-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="d1daa-141">Especifica o número de threads a serem usados para carregamento.</span><span class="sxs-lookup"><span data-stu-id="d1daa-141">Specifies the number of threads to use for upload.</span></span>

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

### <span data-ttu-id="d1daa-142">-Substituir</span><span class="sxs-lookup"><span data-stu-id="d1daa-142">-OverWrite</span></span>
<span data-ttu-id="d1daa-143">Especifica que esse cmdlet exclui o blob existente no URI de destino especificado, se existir.</span><span class="sxs-lookup"><span data-stu-id="d1daa-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="d1daa-144">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d1daa-144">-Profile</span></span>
<span data-ttu-id="d1daa-145">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d1daa-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1daa-146">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d1daa-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1daa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1daa-147">CommonParameters</span></span>
<span data-ttu-id="d1daa-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1daa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1daa-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1daa-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1daa-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1daa-150">INPUTS</span></span>

## <span data-ttu-id="d1daa-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1daa-151">OUTPUTS</span></span>

## <span data-ttu-id="d1daa-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1daa-152">NOTES</span></span>

## <span data-ttu-id="d1daa-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1daa-153">RELATED LINKS</span></span>

[<span data-ttu-id="d1daa-154">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d1daa-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


