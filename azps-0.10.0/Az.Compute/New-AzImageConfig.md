---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de6c09c6c86fa4da7eff57439f556d21d18d94a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776968"
---
# <span data-ttu-id="0648f-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0648f-101">New-AzImageConfig</span></span>

## <span data-ttu-id="0648f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0648f-102">SYNOPSIS</span></span>
<span data-ttu-id="0648f-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="0648f-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="0648f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0648f-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0648f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0648f-105">DESCRIPTION</span></span>
<span data-ttu-id="0648f-106">O cmdlet **New-AzImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="0648f-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="0648f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0648f-107">EXAMPLES</span></span>

### <span data-ttu-id="0648f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0648f-108">Example 1</span></span>
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

<span data-ttu-id="0648f-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0648f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="0648f-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="0648f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="0648f-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0648f-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="0648f-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0648f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0648f-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0648f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="0648f-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0648f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0648f-115">OS</span><span class="sxs-lookup"><span data-stu-id="0648f-115">PARAMETERS</span></span>

### <span data-ttu-id="0648f-116">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="0648f-116">-DataDisk</span></span>
<span data-ttu-id="0648f-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="0648f-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0648f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0648f-118">-DefaultProfile</span></span>
<span data-ttu-id="0648f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0648f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0648f-120">-Local</span><span class="sxs-lookup"><span data-stu-id="0648f-120">-Location</span></span>
<span data-ttu-id="0648f-121">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="0648f-121">Specifies a location.</span></span>

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

### <span data-ttu-id="0648f-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="0648f-122">-OsDisk</span></span>
<span data-ttu-id="0648f-123">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0648f-123">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0648f-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0648f-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="0648f-125">Especifica a ID da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="0648f-125">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0648f-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="0648f-126">-Tag</span></span>
<span data-ttu-id="0648f-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0648f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0648f-128">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0648f-128">For example:</span></span>

<span data-ttu-id="0648f-129">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0648f-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0648f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0648f-130">-Confirm</span></span>
<span data-ttu-id="0648f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0648f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0648f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0648f-132">-WhatIf</span></span>
<span data-ttu-id="0648f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0648f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0648f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0648f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0648f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0648f-135">CommonParameters</span></span>
<span data-ttu-id="0648f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0648f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0648f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0648f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0648f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0648f-138">INPUTS</span></span>

### <span data-ttu-id="0648f-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0648f-139">None</span></span>
<span data-ttu-id="0648f-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0648f-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0648f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0648f-141">OUTPUTS</span></span>

### <span data-ttu-id="0648f-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="0648f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0648f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0648f-143">NOTES</span></span>

## <span data-ttu-id="0648f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0648f-144">RELATED LINKS</span></span>

