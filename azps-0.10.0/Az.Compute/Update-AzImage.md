---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775945"
---
# <span data-ttu-id="7e848-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7e848-101">Update-AzImage</span></span>

## <span data-ttu-id="7e848-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e848-102">SYNOPSIS</span></span>
<span data-ttu-id="7e848-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7e848-103">Updates an image.</span></span>

## <span data-ttu-id="7e848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e848-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e848-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e848-105">DESCRIPTION</span></span>
<span data-ttu-id="7e848-106">O cmdlet **Update-AzImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7e848-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="7e848-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e848-107">EXAMPLES</span></span>

### <span data-ttu-id="7e848-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e848-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="7e848-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="7e848-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7e848-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e848-110">PARAMETERS</span></span>

### <span data-ttu-id="7e848-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e848-111">-AsJob</span></span>
<span data-ttu-id="7e848-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7e848-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e848-113">-DefaultProfile</span></span>
<span data-ttu-id="7e848-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e848-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e848-115">-Imagem</span><span class="sxs-lookup"><span data-stu-id="7e848-115">-Image</span></span>
<span data-ttu-id="7e848-116">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="7e848-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7e848-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7e848-117">-ImageName</span></span>
<span data-ttu-id="7e848-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7e848-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7e848-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e848-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e848-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e848-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7e848-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e848-121">-Confirm</span></span>
<span data-ttu-id="7e848-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e848-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e848-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e848-123">-WhatIf</span></span>
<span data-ttu-id="7e848-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e848-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e848-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e848-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e848-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e848-126">CommonParameters</span></span>
<span data-ttu-id="7e848-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e848-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e848-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e848-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e848-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e848-129">INPUTS</span></span>

### <span data-ttu-id="7e848-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e848-130">System.String</span></span>
<span data-ttu-id="7e848-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="7e848-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7e848-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e848-132">OUTPUTS</span></span>

### <span data-ttu-id="7e848-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="7e848-133">System.Object</span></span>

## <span data-ttu-id="7e848-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e848-134">NOTES</span></span>

## <span data-ttu-id="7e848-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e848-135">RELATED LINKS</span></span>

