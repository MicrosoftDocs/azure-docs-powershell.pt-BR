---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
ms.openlocfilehash: 0a03126be62c528d0879eaff093d6a3969802ce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785367"
---
# <span data-ttu-id="becfa-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="becfa-101">New-AzureRmImage</span></span>

## <span data-ttu-id="becfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="becfa-102">SYNOPSIS</span></span>
<span data-ttu-id="becfa-103">Cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="becfa-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="becfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="becfa-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="becfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="becfa-105">DESCRIPTION</span></span>
<span data-ttu-id="becfa-106">O cmdlet **New-AzureRmImage** cria uma imagem.</span><span class="sxs-lookup"><span data-stu-id="becfa-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="becfa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="becfa-107">EXAMPLES</span></span>

### <span data-ttu-id="becfa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="becfa-108">Example 1</span></span>
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

<span data-ttu-id="becfa-109">O primeiro comando cria um objeto Image e, em seguida, armazena-o na variável $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="becfa-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="becfa-110">Os próximos três comandos atribuem caminhos de disco do sistema operacional e dois discos de dados para o $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2 variáveis.</span><span class="sxs-lookup"><span data-stu-id="becfa-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="becfa-111">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="becfa-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="becfa-112">Os próximos três comandos adicionam um disco do sistema operacional e dois discos de dados à imagem armazenada em $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="becfa-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="becfa-113">O URI de cada disco é armazenado em $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="becfa-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="becfa-114">O comando final cria uma imagem chamada "ImageName01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="becfa-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="becfa-115">OS</span><span class="sxs-lookup"><span data-stu-id="becfa-115">PARAMETERS</span></span>

### <span data-ttu-id="becfa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="becfa-116">-AsJob</span></span>
<span data-ttu-id="becfa-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="becfa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="becfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becfa-118">-DefaultProfile</span></span>
<span data-ttu-id="becfa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="becfa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="becfa-120">-Imagem</span><span class="sxs-lookup"><span data-stu-id="becfa-120">-Image</span></span>
<span data-ttu-id="becfa-121">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="becfa-121">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="becfa-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="becfa-122">-ImageName</span></span>
<span data-ttu-id="becfa-123">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="becfa-123">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becfa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="becfa-124">-ResourceGroupName</span></span>
<span data-ttu-id="becfa-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="becfa-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becfa-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="becfa-126">-Confirm</span></span>
<span data-ttu-id="becfa-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="becfa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becfa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becfa-128">-WhatIf</span></span>
<span data-ttu-id="becfa-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="becfa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="becfa-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="becfa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="becfa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becfa-131">CommonParameters</span></span>
<span data-ttu-id="becfa-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="becfa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becfa-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="becfa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becfa-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="becfa-134">INPUTS</span></span>

### <span data-ttu-id="becfa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="becfa-135">System.String</span></span>
<span data-ttu-id="becfa-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="becfa-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="becfa-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="becfa-137">OUTPUTS</span></span>

### <span data-ttu-id="becfa-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="becfa-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="becfa-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="becfa-139">System.Object</span></span>

## <span data-ttu-id="becfa-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="becfa-140">NOTES</span></span>

## <span data-ttu-id="becfa-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="becfa-141">RELATED LINKS</span></span>

