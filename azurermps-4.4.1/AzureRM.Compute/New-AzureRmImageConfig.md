---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426978"
---
# <span data-ttu-id="40319-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="40319-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="40319-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40319-102">SYNOPSIS</span></span>
<span data-ttu-id="40319-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="40319-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40319-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40319-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40319-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40319-105">DESCRIPTION</span></span>
<span data-ttu-id="40319-106">O cmdlet **New-AzureRmImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="40319-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="40319-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40319-107">EXAMPLES</span></span>

### <span data-ttu-id="40319-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40319-108">Example 1</span></span>
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

<span data-ttu-id="40319-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="40319-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="40319-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="40319-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="40319-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="40319-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="40319-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="40319-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="40319-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="40319-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="40319-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="40319-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="40319-115">OS</span><span class="sxs-lookup"><span data-stu-id="40319-115">PARAMETERS</span></span>

### <span data-ttu-id="40319-116">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="40319-116">-DataDisk</span></span>
<span data-ttu-id="40319-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="40319-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="40319-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40319-118">-DefaultProfile</span></span>
<span data-ttu-id="40319-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40319-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40319-120">-Local</span><span class="sxs-lookup"><span data-stu-id="40319-120">-Location</span></span>
<span data-ttu-id="40319-121">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="40319-121">Specifies a location.</span></span>

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

### <span data-ttu-id="40319-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="40319-122">-OsDisk</span></span>
<span data-ttu-id="40319-123">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="40319-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="40319-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="40319-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="40319-125">Especifica a ID da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="40319-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="40319-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="40319-126">-Tag</span></span>
<span data-ttu-id="40319-127">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="40319-127">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="40319-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40319-128">-Confirm</span></span>
<span data-ttu-id="40319-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40319-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40319-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40319-130">-WhatIf</span></span>
<span data-ttu-id="40319-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40319-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40319-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40319-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40319-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40319-133">CommonParameters</span></span>
<span data-ttu-id="40319-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40319-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40319-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40319-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40319-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40319-136">INPUTS</span></span>

### <span data-ttu-id="40319-137">System. String</span><span class="sxs-lookup"><span data-stu-id="40319-137">System.String</span></span>
<span data-ttu-id="40319-138">System. Collections. Hashtable Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="40319-138">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="40319-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40319-139">OUTPUTS</span></span>

### <span data-ttu-id="40319-140">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="40319-140">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="40319-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40319-141">NOTES</span></span>

## <span data-ttu-id="40319-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40319-142">RELATED LINKS</span></span>

