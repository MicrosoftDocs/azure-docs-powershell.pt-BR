---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786537"
---
# <span data-ttu-id="84a6a-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="84a6a-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="84a6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="84a6a-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="84a6a-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84a6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84a6a-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="84a6a-106">O cmdlet **Update-AzureRmImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="84a6a-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="84a6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="84a6a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84a6a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="84a6a-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="84a6a-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="84a6a-110">OS</span><span class="sxs-lookup"><span data-stu-id="84a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="84a6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84a6a-111">-AsJob</span></span>
<span data-ttu-id="84a6a-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="84a6a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84a6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a6a-113">-DefaultProfile</span></span>
<span data-ttu-id="84a6a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84a6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84a6a-115">-Imagem</span><span class="sxs-lookup"><span data-stu-id="84a6a-115">-Image</span></span>
<span data-ttu-id="84a6a-116">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="84a6a-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="84a6a-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="84a6a-117">-ImageName</span></span>
<span data-ttu-id="84a6a-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="84a6a-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="84a6a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a6a-119">-ResourceGroupName</span></span>
<span data-ttu-id="84a6a-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84a6a-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="84a6a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84a6a-121">-Confirm</span></span>
<span data-ttu-id="84a6a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a6a-123">-WhatIf</span></span>
<span data-ttu-id="84a6a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84a6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a6a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84a6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a6a-126">CommonParameters</span></span>
<span data-ttu-id="84a6a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a6a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a6a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84a6a-129">INPUTS</span></span>

### <span data-ttu-id="84a6a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="84a6a-130">System.String</span></span>
<span data-ttu-id="84a6a-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="84a6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="84a6a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84a6a-132">OUTPUTS</span></span>

### <span data-ttu-id="84a6a-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="84a6a-133">System.Object</span></span>

## <span data-ttu-id="84a6a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84a6a-134">NOTES</span></span>

## <span data-ttu-id="84a6a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84a6a-135">RELATED LINKS</span></span>

