---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116527"
---
# <span data-ttu-id="7b518-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="7b518-101">New-AzImageConfig</span></span>

## <span data-ttu-id="7b518-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b518-102">SYNOPSIS</span></span>
<span data-ttu-id="7b518-103">Cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="7b518-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="7b518-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b518-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b518-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b518-105">DESCRIPTION</span></span>
<span data-ttu-id="7b518-106">O **cmdlet New-AzImageConfig** cria um objeto de imagem configurável.</span><span class="sxs-lookup"><span data-stu-id="7b518-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="7b518-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b518-107">EXAMPLES</span></span>

### <span data-ttu-id="7b518-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b518-108">Example 1</span></span>
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

<span data-ttu-id="7b518-109">O primeiro comando cria um objeto de imagem e o armazena na variável $imageConfig imagem.</span><span class="sxs-lookup"><span data-stu-id="7b518-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="7b518-110">Os três comandos a seguir atribuem caminhos de disco do sistema operacional e dois discos de dados às variáveis $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="7b518-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="7b518-111">Esta abordagem é apenas para a capacidade de leitura dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b518-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7b518-112">Os três comandos a seguir adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="7b518-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7b518-113">O URI de cada disco é armazenado $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="7b518-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="7b518-114">O comando final cria uma imagem chamada 'ImageName01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="7b518-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7b518-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b518-115">PARAMETERS</span></span>

### <span data-ttu-id="7b518-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="7b518-116">-DataDisk</span></span>
<span data-ttu-id="7b518-117">Especifica o objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="7b518-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="7b518-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b518-118">-DefaultProfile</span></span>
<span data-ttu-id="7b518-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7b518-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b518-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="7b518-120">-HyperVGeneration</span></span>
<span data-ttu-id="7b518-121">Especifica o Tipo de HiperVGeneração para a máquina virtual criada a partir da imagem.</span><span class="sxs-lookup"><span data-stu-id="7b518-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="7b518-122">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="7b518-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="7b518-123">-Local</span><span class="sxs-lookup"><span data-stu-id="7b518-123">-Location</span></span>
<span data-ttu-id="7b518-124">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="7b518-124">Specifies a location.</span></span>

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

### <span data-ttu-id="7b518-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="7b518-125">-OsDisk</span></span>
<span data-ttu-id="7b518-126">Especifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7b518-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="7b518-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7b518-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="7b518-128">Especifica a ID do computador virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="7b518-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="7b518-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b518-129">-Tag</span></span>
<span data-ttu-id="7b518-130">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7b518-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b518-131">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7b518-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b518-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="7b518-132">-ZoneResilient</span></span>
<span data-ttu-id="7b518-133">Habilitar zona resiliente</span><span class="sxs-lookup"><span data-stu-id="7b518-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="7b518-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7b518-134">-Confirm</span></span>
<span data-ttu-id="7b518-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b518-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b518-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b518-136">-WhatIf</span></span>
<span data-ttu-id="7b518-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7b518-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b518-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b518-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b518-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b518-139">CommonParameters</span></span>
<span data-ttu-id="7b518-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b518-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b518-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b518-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b518-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="7b518-142">INPUTS</span></span>

### <span data-ttu-id="7b518-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7b518-143">System.String</span></span>

### <span data-ttu-id="7b518-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b518-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7b518-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="7b518-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="7b518-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="7b518-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="7b518-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="7b518-147">OUTPUTS</span></span>

### <span data-ttu-id="7b518-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="7b518-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7b518-149">Notas</span><span class="sxs-lookup"><span data-stu-id="7b518-149">NOTES</span></span>

## <span data-ttu-id="7b518-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b518-150">RELATED LINKS</span></span>
