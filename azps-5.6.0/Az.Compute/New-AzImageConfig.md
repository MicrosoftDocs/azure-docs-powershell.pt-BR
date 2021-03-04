---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de59e8a9dc2fdcc4fa29409eaffc7f82e7d57b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888576"
---
# <span data-ttu-id="803a6-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="803a6-101">New-AzImageConfig</span></span>

## <span data-ttu-id="803a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="803a6-102">SYNOPSIS</span></span>
<span data-ttu-id="803a6-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="803a6-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="803a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="803a6-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="803a6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="803a6-105">DESCRIPTION</span></span>
<span data-ttu-id="803a6-106">O cmdlet **New-AzImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="803a6-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="803a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="803a6-107">EXAMPLES</span></span>

### <span data-ttu-id="803a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="803a6-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="803a6-109">O primeiro comando cria um objeto image e o armazena na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="803a6-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="803a6-110">Os três comandos a seguir atribuem caminhos do disco do sistema operacional e dois discos de dados às variáveis $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="803a6-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="803a6-111">Essa abordagem é apenas para a capacidade de leitura dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="803a6-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="803a6-112">Os três comandos a seguir adicionam um disco operacional e dois discos de dados à imagem armazenada $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="803a6-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="803a6-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="803a6-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="803a6-114">O comando final cria uma imagem chamada 'ImageName01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="803a6-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="803a6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="803a6-115">PARAMETERS</span></span>

### <span data-ttu-id="803a6-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="803a6-116">-DataDisk</span></span>
<span data-ttu-id="803a6-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="803a6-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803a6-118">-DefaultProfile</span></span>
<span data-ttu-id="803a6-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="803a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="803a6-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="803a6-120">-HyperVGeneration</span></span>
<span data-ttu-id="803a6-121">Especifica o Tipo de HyperVGeneration para a máquina virtual criada a partir da imagem.</span><span class="sxs-lookup"><span data-stu-id="803a6-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="803a6-122">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="803a6-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="803a6-123">-Location</span><span class="sxs-lookup"><span data-stu-id="803a6-123">-Location</span></span>
<span data-ttu-id="803a6-124">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="803a6-124">Specifies a location.</span></span>

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

### <span data-ttu-id="803a6-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="803a6-125">-OsDisk</span></span>
<span data-ttu-id="803a6-126">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="803a6-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a6-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="803a6-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="803a6-128">Especifica a ID da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="803a6-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="803a6-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="803a6-129">-Tag</span></span>
<span data-ttu-id="803a6-130">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="803a6-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="803a6-131">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="803a6-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a6-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="803a6-132">-ZoneResilient</span></span>
<span data-ttu-id="803a6-133">Habilitar zona resiliente</span><span class="sxs-lookup"><span data-stu-id="803a6-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="803a6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="803a6-134">-Confirm</span></span>
<span data-ttu-id="803a6-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="803a6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="803a6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="803a6-136">-WhatIf</span></span>
<span data-ttu-id="803a6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="803a6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="803a6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="803a6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="803a6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803a6-139">CommonParameters</span></span>
<span data-ttu-id="803a6-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803a6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803a6-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="803a6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803a6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="803a6-142">INPUTS</span></span>

### <span data-ttu-id="803a6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="803a6-143">System.String</span></span>

### <span data-ttu-id="803a6-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="803a6-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="803a6-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="803a6-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="803a6-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="803a6-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="803a6-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="803a6-147">OUTPUTS</span></span>

### <span data-ttu-id="803a6-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="803a6-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="803a6-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="803a6-149">NOTES</span></span>

## <span data-ttu-id="803a6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="803a6-150">RELATED LINKS</span></span>
