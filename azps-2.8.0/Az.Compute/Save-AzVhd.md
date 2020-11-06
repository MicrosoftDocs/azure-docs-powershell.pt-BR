---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f1af93009c905e8d66bd081ef8aa288c9acc0c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597259"
---
# <span data-ttu-id="74b6f-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="74b6f-101">Save-AzVhd</span></span>

## <span data-ttu-id="74b6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="74b6f-103">Salva localmente as imagens. vhd baixadas.</span><span class="sxs-lookup"><span data-stu-id="74b6f-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="74b6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74b6f-104">SYNTAX</span></span>

### <span data-ttu-id="74b6f-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="74b6f-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74b6f-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="74b6f-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b6f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74b6f-107">DESCRIPTION</span></span>
<span data-ttu-id="74b6f-108">O cmdlet **Save-AzVhd** salva imagens. VHD de um blob onde elas são armazenadas em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="74b6f-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="74b6f-109">Você pode especificar o número de threads de download que o processo usa e se deseja substituir um arquivo que já existe.</span><span class="sxs-lookup"><span data-stu-id="74b6f-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="74b6f-110">Esse cmdlet baixa o conteúdo como se encontra.</span><span class="sxs-lookup"><span data-stu-id="74b6f-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="74b6f-111">Ele não aplica qualquer conversão de formato de disco rígido virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="74b6f-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="74b6f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74b6f-112">EXAMPLES</span></span>

### <span data-ttu-id="74b6f-113">Exemplo 1: baixar uma imagem</span><span class="sxs-lookup"><span data-stu-id="74b6f-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="74b6f-114">Esse comando baixa um arquivo. vhd e o armazena no caminho local C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="74b6f-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="74b6f-115">Exemplo 2: baixar uma imagem e substituir o arquivo local</span><span class="sxs-lookup"><span data-stu-id="74b6f-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="74b6f-116">Esse comando baixa um arquivo. vhd e o armazena no caminho local.</span><span class="sxs-lookup"><span data-stu-id="74b6f-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="74b6f-117">O comando inclui o parâmetro *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="74b6f-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="74b6f-118">Portanto, se o C:\vhd\Win7Image.vhd já existir, esse comando o substituirá.</span><span class="sxs-lookup"><span data-stu-id="74b6f-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="74b6f-119">Exemplo 3: baixar uma imagem usando um número especificado de threads</span><span class="sxs-lookup"><span data-stu-id="74b6f-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="74b6f-120">Esse comando baixa um arquivo. vhd e o armazena no caminho local.</span><span class="sxs-lookup"><span data-stu-id="74b6f-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="74b6f-121">O comando especifica um valor de 32 para o parâmetro *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="74b6f-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="74b6f-122">Portanto, o cmdlet usa segmentos 32 para essa ação.</span><span class="sxs-lookup"><span data-stu-id="74b6f-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="74b6f-123">Exemplo 4: baixar uma imagem e especificar a chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="74b6f-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="74b6f-124">Esse comando baixa um arquivo. vhd e especifica a chave de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74b6f-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="74b6f-125">OS</span><span class="sxs-lookup"><span data-stu-id="74b6f-125">PARAMETERS</span></span>

### <span data-ttu-id="74b6f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74b6f-126">-AsJob</span></span>
<span data-ttu-id="74b6f-127">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="74b6f-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b6f-128">-DefaultProfile</span></span>
<span data-ttu-id="74b6f-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74b6f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b6f-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="74b6f-130">-LocalFilePath</span></span>
<span data-ttu-id="74b6f-131">Especifica o caminho do arquivo local da imagem salva.</span><span class="sxs-lookup"><span data-stu-id="74b6f-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="74b6f-132">-NumberOfThreads</span></span>
<span data-ttu-id="74b6f-133">Especifica o número de threads de download que este cmdlet usa durante o download.</span><span class="sxs-lookup"><span data-stu-id="74b6f-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-134">-Substituir</span><span class="sxs-lookup"><span data-stu-id="74b6f-134">-OverWrite</span></span>
<span data-ttu-id="74b6f-135">Indica que esse cmdlet substitui o arquivo especificado pelo arquivo *LocalFilePath* se ele existir.</span><span class="sxs-lookup"><span data-stu-id="74b6f-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b6f-136">-ResourceGroupName</span></span>
<span data-ttu-id="74b6f-137">Especifica o nome do grupo de recursos da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74b6f-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="74b6f-138">-SourceUri</span></span>
<span data-ttu-id="74b6f-139">Especifica o URI (Uniform Resource Identifier) do blob em `Azure` .</span><span class="sxs-lookup"><span data-stu-id="74b6f-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="74b6f-140">-StorageKey</span></span>
<span data-ttu-id="74b6f-141">Especifica a chave de armazenamento da conta de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="74b6f-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="74b6f-142">Se você não especificar uma chave, esse cmdlet tenta determinar a chave de armazenamento da *conta em repositório do Azure* .</span><span class="sxs-lookup"><span data-stu-id="74b6f-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b6f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b6f-143">CommonParameters</span></span>
<span data-ttu-id="74b6f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b6f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b6f-145">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74b6f-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b6f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74b6f-146">INPUTS</span></span>

### <span data-ttu-id="74b6f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="74b6f-147">System.String</span></span>

### <span data-ttu-id="74b6f-148">System. URI</span><span class="sxs-lookup"><span data-stu-id="74b6f-148">System.Uri</span></span>

## <span data-ttu-id="74b6f-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74b6f-149">OUTPUTS</span></span>

### <span data-ttu-id="74b6f-150">Microsoft. Azure. Commands. COMPUTE. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="74b6f-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="74b6f-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74b6f-151">NOTES</span></span>

## <span data-ttu-id="74b6f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74b6f-152">RELATED LINKS</span></span>

[<span data-ttu-id="74b6f-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="74b6f-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


