---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 77a4879d403b52a828460bcfec5666b7071dcea9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886344"
---
# <span data-ttu-id="ddfd4-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="ddfd4-101">New-AzImage</span></span>

## <span data-ttu-id="ddfd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfd4-103">Cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-103">Creates an image.</span></span>

## <span data-ttu-id="ddfd4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddfd4-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddfd4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddfd4-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfd4-106">O cmdlet **New-AzImage** cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="ddfd4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfd4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddfd4-108">Example 1</span></span>
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

<span data-ttu-id="ddfd4-109">O primeiro comando cria um objeto image e o armazena na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="ddfd4-110">Os três comandos a seguir atribuem caminhos do disco do sistema operacional e dois discos de dados às variáveis $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="ddfd4-111">Essa abordagem é apenas para a capacidade de leitura dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="ddfd4-112">Os três comandos a seguir adicionam um disco operacional e dois discos de dados à imagem armazenada $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="ddfd4-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="ddfd4-114">O comando final cria uma imagem chamada 'ImageName01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ddfd4-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-115">PARAMETERS</span></span>

### <span data-ttu-id="ddfd4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddfd4-116">-AsJob</span></span>
<span data-ttu-id="ddfd4-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ddfd4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddfd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfd4-118">-DefaultProfile</span></span>
<span data-ttu-id="ddfd4-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddfd4-120">-Image</span><span class="sxs-lookup"><span data-stu-id="ddfd4-120">-Image</span></span>
<span data-ttu-id="ddfd4-121">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfd4-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ddfd4-122">-ImageName</span></span>
<span data-ttu-id="ddfd4-123">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddfd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddfd4-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfd4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddfd4-126">-Confirm</span></span>
<span data-ttu-id="ddfd4-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddfd4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddfd4-128">-WhatIf</span></span>
<span data-ttu-id="ddfd4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddfd4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddfd4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfd4-131">CommonParameters</span></span>
<span data-ttu-id="ddfd4-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfd4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfd4-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddfd4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfd4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-134">INPUTS</span></span>

### <span data-ttu-id="ddfd4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ddfd4-135">System.String</span></span>

### <span data-ttu-id="ddfd4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="ddfd4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ddfd4-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-137">OUTPUTS</span></span>

### <span data-ttu-id="ddfd4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="ddfd4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ddfd4-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddfd4-139">NOTES</span></span>

## <span data-ttu-id="ddfd4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddfd4-140">RELATED LINKS</span></span>
