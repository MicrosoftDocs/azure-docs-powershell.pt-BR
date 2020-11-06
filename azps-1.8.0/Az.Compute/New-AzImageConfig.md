---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: f7f2a9ee7119b54722862b3796e9a5372b9b1d09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601312"
---
# <span data-ttu-id="0d7f8-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0d7f8-101">New-AzImageConfig</span></span>

## <span data-ttu-id="0d7f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7f8-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="0d7f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d7f8-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="0d7f8-106">O cmdlet **New-AzImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="0d7f8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-107">EXAMPLES</span></span>

### <span data-ttu-id="0d7f8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d7f8-108">Example 1</span></span>
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

<span data-ttu-id="0d7f8-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="0d7f8-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="0d7f8-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="0d7f8-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0d7f8-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="0d7f8-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0d7f8-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0d7f8-115">OS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-115">PARAMETERS</span></span>

### <span data-ttu-id="0d7f8-116">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="0d7f8-116">-DataDisk</span></span>
<span data-ttu-id="0d7f8-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="0d7f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7f8-118">-DefaultProfile</span></span>
<span data-ttu-id="0d7f8-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d7f8-120">-Local</span><span class="sxs-lookup"><span data-stu-id="0d7f8-120">-Location</span></span>
<span data-ttu-id="0d7f8-121">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-121">Specifies a location.</span></span>

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

### <span data-ttu-id="0d7f8-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="0d7f8-122">-OsDisk</span></span>
<span data-ttu-id="0d7f8-123">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="0d7f8-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0d7f8-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="0d7f8-125">Especifica a ID da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="0d7f8-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="0d7f8-126">-Tag</span></span>
<span data-ttu-id="0d7f8-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d7f8-128">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0d7f8-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0d7f8-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="0d7f8-129">-ZoneResilient</span></span>
<span data-ttu-id="0d7f8-130">Habilitar a zona resistente</span><span class="sxs-lookup"><span data-stu-id="0d7f8-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="0d7f8-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d7f8-131">-Confirm</span></span>
<span data-ttu-id="0d7f8-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7f8-133">-WhatIf</span></span>
<span data-ttu-id="0d7f8-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d7f8-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7f8-136">CommonParameters</span></span>
<span data-ttu-id="0d7f8-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7f8-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d7f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7f8-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d7f8-139">INPUTS</span></span>

### <span data-ttu-id="0d7f8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7f8-140">System.String</span></span>

### <span data-ttu-id="0d7f8-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0d7f8-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0d7f8-142">Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="0d7f8-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="0d7f8-143">Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="0d7f8-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="0d7f8-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d7f8-144">OUTPUTS</span></span>

### <span data-ttu-id="0d7f8-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="0d7f8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0d7f8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d7f8-146">NOTES</span></span>

## <span data-ttu-id="0d7f8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d7f8-147">RELATED LINKS</span></span>
