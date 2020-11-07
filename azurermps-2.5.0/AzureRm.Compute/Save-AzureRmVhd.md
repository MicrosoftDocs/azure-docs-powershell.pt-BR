---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786557"
---
# <span data-ttu-id="73d0d-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="73d0d-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="73d0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="73d0d-103">Salva localmente as imagens. vhd baixadas.</span><span class="sxs-lookup"><span data-stu-id="73d0d-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73d0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73d0d-104">SYNTAX</span></span>

### <span data-ttu-id="73d0d-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="73d0d-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73d0d-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="73d0d-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73d0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73d0d-107">DESCRIPTION</span></span>
<span data-ttu-id="73d0d-108">O cmdlet **Save-AzureRmVhd** salva imagens. VHD de um blob onde elas são armazenadas em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="73d0d-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="73d0d-109">Você pode especificar o número de threads de download que o processo usa e se deseja substituir um arquivo que já existe.</span><span class="sxs-lookup"><span data-stu-id="73d0d-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="73d0d-110">Esse cmdlet baixa o conteúdo como se encontra.</span><span class="sxs-lookup"><span data-stu-id="73d0d-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="73d0d-111">Ele não aplica qualquer conversão de formato de disco rígido virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="73d0d-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="73d0d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73d0d-112">EXAMPLES</span></span>

### <span data-ttu-id="73d0d-113">Exemplo 1: baixar uma imagem</span><span class="sxs-lookup"><span data-stu-id="73d0d-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="73d0d-114">Esse comando baixa um arquivo. vhd e o armazena no caminho local C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="73d0d-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="73d0d-115">Exemplo 2: baixar uma imagem e substituir o arquivo local</span><span class="sxs-lookup"><span data-stu-id="73d0d-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="73d0d-116">Esse comando baixa um arquivo. vhd e o armazena no caminho local.</span><span class="sxs-lookup"><span data-stu-id="73d0d-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="73d0d-117">O comando inclui o parâmetro *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="73d0d-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="73d0d-118">Portanto, se o C:\vhd\Win7Image.vhd já existir, esse comando o substituirá.</span><span class="sxs-lookup"><span data-stu-id="73d0d-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="73d0d-119">Exemplo 3: baixar uma imagem usando um número especificado de threads</span><span class="sxs-lookup"><span data-stu-id="73d0d-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="73d0d-120">Esse comando baixa um arquivo. vhd e o armazena no caminho local.</span><span class="sxs-lookup"><span data-stu-id="73d0d-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="73d0d-121">O comando especifica um valor de 32 para o parâmetro *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="73d0d-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="73d0d-122">Portanto, o cmdlet usa segmentos 32 para essa ação.</span><span class="sxs-lookup"><span data-stu-id="73d0d-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="73d0d-123">Exemplo 4: baixar uma imagem e especificar a chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="73d0d-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="73d0d-124">Esse comando baixa um arquivo. vhd e especifica a chave de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="73d0d-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="73d0d-125">OS</span><span class="sxs-lookup"><span data-stu-id="73d0d-125">PARAMETERS</span></span>

### <span data-ttu-id="73d0d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73d0d-126">-AsJob</span></span>
<span data-ttu-id="73d0d-127">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="73d0d-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d0d-128">-DefaultProfile</span></span>
<span data-ttu-id="73d0d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73d0d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="73d0d-130">-LocalFilePath</span></span>
<span data-ttu-id="73d0d-131">Especifica o caminho do arquivo local da imagem salva.</span><span class="sxs-lookup"><span data-stu-id="73d0d-131">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="73d0d-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="73d0d-132">-NumberOfThreads</span></span>
<span data-ttu-id="73d0d-133">Especifica o número de threads de download que este cmdlet usa durante o download.</span><span class="sxs-lookup"><span data-stu-id="73d0d-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="73d0d-134">-Substituir</span><span class="sxs-lookup"><span data-stu-id="73d0d-134">-OverWrite</span></span>
<span data-ttu-id="73d0d-135">Indica que esse cmdlet substitui o arquivo especificado pelo arquivo *LocalFilePath* se ele existir.</span><span class="sxs-lookup"><span data-stu-id="73d0d-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d0d-136">-ResourceGroupName</span></span>
<span data-ttu-id="73d0d-137">Especifica o nome do grupo de recursos da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="73d0d-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="73d0d-138">-SourceUri</span></span>
<span data-ttu-id="73d0d-139">Especifica o URI (Uniform Resource Identifier) do blob em `Azure` .</span><span class="sxs-lookup"><span data-stu-id="73d0d-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="73d0d-140">-StorageKey</span></span>
<span data-ttu-id="73d0d-141">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="73d0d-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="73d0d-142">Se você não especificar uma chave, esse cmdlet tenta determinar a chave de armazenamento da *conta em repositório do Azure* .</span><span class="sxs-lookup"><span data-stu-id="73d0d-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d0d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d0d-143">CommonParameters</span></span>
<span data-ttu-id="73d0d-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d0d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d0d-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d0d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d0d-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73d0d-146">INPUTS</span></span>

### <span data-ttu-id="73d0d-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73d0d-147">None</span></span>
<span data-ttu-id="73d0d-148">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="73d0d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73d0d-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73d0d-149">OUTPUTS</span></span>

### <span data-ttu-id="73d0d-150">Microsoft. Azure. Commands. COMPUTE. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="73d0d-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="73d0d-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73d0d-151">NOTES</span></span>

## <span data-ttu-id="73d0d-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73d0d-152">RELATED LINKS</span></span>

[<span data-ttu-id="73d0d-153">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="73d0d-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


