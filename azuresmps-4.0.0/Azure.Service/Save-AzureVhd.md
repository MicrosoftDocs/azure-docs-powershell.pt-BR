---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945461"
---
# <span data-ttu-id="996ac-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="996ac-101">Save-AzureVhd</span></span>

## <span data-ttu-id="996ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="996ac-102">SYNOPSIS</span></span>
<span data-ttu-id="996ac-103">Habilita o download de imagens. vhd.</span><span class="sxs-lookup"><span data-stu-id="996ac-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="996ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="996ac-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="996ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="996ac-105">DESCRIPTION</span></span>
<span data-ttu-id="996ac-106">O cmdlet **Save-AzureVhd** permite o download de imagens. VHD de um blob onde elas são armazenadas em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="996ac-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="996ac-107">Ele tem parâmetros para configurar o processo de download especificando o número de threads de download que são usados ou substituindo o arquivo que já existe no caminho de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="996ac-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="996ac-108">**Save-AzureVhd** não realiza nenhuma conversão de formato VHD, e o blob é baixado como se encontra.</span><span class="sxs-lookup"><span data-stu-id="996ac-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="996ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="996ac-109">EXAMPLES</span></span>

### <span data-ttu-id="996ac-110">Exemplo 1: baixar um arquivo VHD</span><span class="sxs-lookup"><span data-stu-id="996ac-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="996ac-111">Esse comando baixa um arquivo. vhd.</span><span class="sxs-lookup"><span data-stu-id="996ac-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="996ac-112">Exemplo 2: baixar um arquivo VHD e substituir o arquivo local</span><span class="sxs-lookup"><span data-stu-id="996ac-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="996ac-113">Esse comando baixa um arquivo. vhd e substitui qualquer arquivo no caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="996ac-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="996ac-114">Exemplo 3: baixar um arquivo VHD e especificar o número de threads</span><span class="sxs-lookup"><span data-stu-id="996ac-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="996ac-115">Esse comando baixa um arquivo. vhd e especifica o número de threads.</span><span class="sxs-lookup"><span data-stu-id="996ac-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="996ac-116">Exemplo 4: baixar um arquivo VHD e especificar a chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="996ac-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="996ac-117">Esse comando baixa um arquivo. vhd e especifica a chave de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="996ac-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="996ac-118">OS</span><span class="sxs-lookup"><span data-stu-id="996ac-118">PARAMETERS</span></span>

### <span data-ttu-id="996ac-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="996ac-119">-InformationAction</span></span>
<span data-ttu-id="996ac-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="996ac-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="996ac-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="996ac-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="996ac-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="996ac-122">Continue</span></span>
- <span data-ttu-id="996ac-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="996ac-123">Ignore</span></span>
- <span data-ttu-id="996ac-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="996ac-124">Inquire</span></span>
- <span data-ttu-id="996ac-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="996ac-125">SilentlyContinue</span></span>
- <span data-ttu-id="996ac-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="996ac-126">Stop</span></span>
- <span data-ttu-id="996ac-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="996ac-127">Suspend</span></span>

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

### <span data-ttu-id="996ac-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="996ac-128">-InformationVariable</span></span>
<span data-ttu-id="996ac-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="996ac-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="996ac-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="996ac-130">-LocalFilePath</span></span>
<span data-ttu-id="996ac-131">Especifica o caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="996ac-131">Specifies the local file path.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="996ac-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="996ac-132">-NumberOfThreads</span></span>
<span data-ttu-id="996ac-133">Especifica o número de threads de download que este cmdlet usa durante o download.</span><span class="sxs-lookup"><span data-stu-id="996ac-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="996ac-134">-Substituir</span><span class="sxs-lookup"><span data-stu-id="996ac-134">-OverWrite</span></span>
<span data-ttu-id="996ac-135">Especifica que esse cmdlet exclui o arquivo especificado pelo arquivo *LocalFilePath* se ele existir.</span><span class="sxs-lookup"><span data-stu-id="996ac-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="996ac-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="996ac-136">-Profile</span></span>
<span data-ttu-id="996ac-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="996ac-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="996ac-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="996ac-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="996ac-139">-Fonte</span><span class="sxs-lookup"><span data-stu-id="996ac-139">-Source</span></span>
<span data-ttu-id="996ac-140">Especifica o URI (Uniform Resource Identifier) para o blob em `Azure` .</span><span class="sxs-lookup"><span data-stu-id="996ac-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="996ac-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="996ac-141">-StorageKey</span></span>
<span data-ttu-id="996ac-142">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="996ac-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="996ac-143">Se não for fornecido, **salve-AzureVhd** tenta determinar a chave de armazenamento da conta em *SourceUri* do Azure.</span><span class="sxs-lookup"><span data-stu-id="996ac-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="996ac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996ac-144">CommonParameters</span></span>
<span data-ttu-id="996ac-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996ac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996ac-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996ac-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996ac-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="996ac-147">INPUTS</span></span>

## <span data-ttu-id="996ac-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="996ac-148">OUTPUTS</span></span>

## <span data-ttu-id="996ac-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="996ac-149">NOTES</span></span>

## <span data-ttu-id="996ac-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="996ac-150">RELATED LINKS</span></span>

[<span data-ttu-id="996ac-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="996ac-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


