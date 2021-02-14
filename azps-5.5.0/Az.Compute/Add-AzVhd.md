---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116554"
---
# <span data-ttu-id="95b26-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="95b26-101">Add-AzVhd</span></span>

## <span data-ttu-id="95b26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95b26-102">SYNOPSIS</span></span>
<span data-ttu-id="95b26-103">Carrega um disco rígido virtual de uma máquina virtual local para um blob em uma conta de armazenamento em nuvem no Azure.</span><span class="sxs-lookup"><span data-stu-id="95b26-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="95b26-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95b26-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95b26-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="95b26-105">DESCRIPTION</span></span>
<span data-ttu-id="95b26-106">O cmdlet **Add-AzVhd** carrega discos rígidos virtuais locais, no formato de arquivo .uploadd, para uma conta de armazenamento de blob como discos rígidos virtuais fixos.</span><span class="sxs-lookup"><span data-stu-id="95b26-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="95b26-107">Você pode configurar o número de threads de carregamento que serão usados ou substituir um blob existente no URI de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="95b26-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="95b26-108">Também há suporte para a capacidade de carregar uma versão corrigida de um arquivo .primeiro local.</span><span class="sxs-lookup"><span data-stu-id="95b26-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="95b26-109">Quando um disco rígido virtual base já tiver sido carregado, você poderá carregar discos diferentes que usam a imagem base como pai.</span><span class="sxs-lookup"><span data-stu-id="95b26-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="95b26-110">O URI de assinatura de acesso compartilhado (SAS) também tem suporte.</span><span class="sxs-lookup"><span data-stu-id="95b26-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="95b26-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="95b26-111">EXAMPLES</span></span>

### <span data-ttu-id="95b26-112">Exemplo 1: Adicionar um arquivo EMOT</span><span class="sxs-lookup"><span data-stu-id="95b26-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="95b26-113">Esse comando adiciona um arquivo .pdf a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95b26-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="95b26-114">Exemplo 2: Adicionar um arquivo EMOD e substituir o destino</span><span class="sxs-lookup"><span data-stu-id="95b26-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="95b26-115">Esse comando adiciona um arquivo .pdf a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95b26-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="95b26-116">O comando substitui um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="95b26-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="95b26-117">Exemplo 3: Adicionar um arquivo DESVD e especificar o número de threads</span><span class="sxs-lookup"><span data-stu-id="95b26-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="95b26-118">Esse comando adiciona um arquivo .pdf a uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95b26-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="95b26-119">O comando especifica o número de threads a ser usado para carregar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="95b26-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="95b26-120">Exemplo 4: Adicionar um arquivo DESVD e especificar o URI SAS</span><span class="sxs-lookup"><span data-stu-id="95b26-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="95b26-121">Esse comando adiciona um arquivo .primeiro a uma conta de armazenamento e especifica o URI do SAS.</span><span class="sxs-lookup"><span data-stu-id="95b26-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="95b26-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95b26-122">PARAMETERS</span></span>

### <span data-ttu-id="95b26-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95b26-123">-AsJob</span></span>
<span data-ttu-id="95b26-124">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="95b26-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95b26-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="95b26-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="95b26-126">Especifica o URI a um blob de imagem base no Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="95b26-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="95b26-127">Um SAS pode ser especificado como o valor desse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="95b26-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b26-128">-DefaultProfile</span></span>
<span data-ttu-id="95b26-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="95b26-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b26-130">-Destino</span><span class="sxs-lookup"><span data-stu-id="95b26-130">-Destination</span></span>
<span data-ttu-id="95b26-131">Especifica o URI de um blob no Armazenamento de Blob.</span><span class="sxs-lookup"><span data-stu-id="95b26-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="95b26-132">O parâmetro dá suporte ao URI do SAS, embora o destino de cenários de correção não possa ser um URI SAS.</span><span class="sxs-lookup"><span data-stu-id="95b26-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="95b26-133">-LocalFilePath</span></span>
<span data-ttu-id="95b26-134">Especifica o caminho do arquivo .od local.</span><span class="sxs-lookup"><span data-stu-id="95b26-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="95b26-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="95b26-136">Especifica o número de threads de carregamento a serem usados ao carregar o arquivo .primeiro.</span><span class="sxs-lookup"><span data-stu-id="95b26-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-137">-Substituir</span><span class="sxs-lookup"><span data-stu-id="95b26-137">-OverWrite</span></span>
<span data-ttu-id="95b26-138">Indica que esse cmdlet substitui um blob existente no URI de destino especificado, se houver.</span><span class="sxs-lookup"><span data-stu-id="95b26-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95b26-139">-ResourceGroupName</span></span>
<span data-ttu-id="95b26-140">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95b26-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b26-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b26-141">CommonParameters</span></span>
<span data-ttu-id="95b26-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b26-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b26-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95b26-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b26-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="95b26-144">INPUTS</span></span>

### <span data-ttu-id="95b26-145">System.String</span><span class="sxs-lookup"><span data-stu-id="95b26-145">System.String</span></span>

### <span data-ttu-id="95b26-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="95b26-146">System.Uri</span></span>

### <span data-ttu-id="95b26-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="95b26-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="95b26-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="95b26-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="95b26-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95b26-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95b26-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="95b26-150">OUTPUTS</span></span>

### <span data-ttu-id="95b26-151">Microsoft.Azure.Commands.Compute.Models.MeddUploadContext</span><span class="sxs-lookup"><span data-stu-id="95b26-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="95b26-152">Notas</span><span class="sxs-lookup"><span data-stu-id="95b26-152">NOTES</span></span>

## <span data-ttu-id="95b26-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95b26-153">RELATED LINKS</span></span>

[<span data-ttu-id="95b26-154">Salvar-AzVhd</span><span class="sxs-lookup"><span data-stu-id="95b26-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


