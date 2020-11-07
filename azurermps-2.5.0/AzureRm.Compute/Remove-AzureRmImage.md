---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimage
schema: 2.0.0
ms.openlocfilehash: 5e52e75ea1af799eb2640e38cfa0e053b6b3cc7d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786145"
---
# <span data-ttu-id="58de0-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="58de0-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="58de0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58de0-102">SYNOPSIS</span></span>
<span data-ttu-id="58de0-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="58de0-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58de0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58de0-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58de0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58de0-105">DESCRIPTION</span></span>
<span data-ttu-id="58de0-106">O cmdlet **Remove-AzureRmImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="58de0-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="58de0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58de0-107">EXAMPLES</span></span>

### <span data-ttu-id="58de0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58de0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="58de0-109">Este comando Remove a imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="58de0-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="58de0-110">OS</span><span class="sxs-lookup"><span data-stu-id="58de0-110">PARAMETERS</span></span>

### <span data-ttu-id="58de0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58de0-111">-AsJob</span></span>
<span data-ttu-id="58de0-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="58de0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="58de0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58de0-113">-DefaultProfile</span></span>
<span data-ttu-id="58de0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58de0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58de0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="58de0-115">-Force</span></span>
<span data-ttu-id="58de0-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="58de0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58de0-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="58de0-117">-ImageName</span></span>
<span data-ttu-id="58de0-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="58de0-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="58de0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58de0-119">-ResourceGroupName</span></span>
<span data-ttu-id="58de0-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58de0-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="58de0-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58de0-121">-Confirm</span></span>
<span data-ttu-id="58de0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58de0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58de0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58de0-123">-WhatIf</span></span>
<span data-ttu-id="58de0-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58de0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58de0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58de0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58de0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58de0-126">CommonParameters</span></span>
<span data-ttu-id="58de0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58de0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58de0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58de0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58de0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58de0-129">INPUTS</span></span>

### <span data-ttu-id="58de0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="58de0-130">System.String</span></span>

## <span data-ttu-id="58de0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58de0-131">OUTPUTS</span></span>

### <span data-ttu-id="58de0-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="58de0-132">System.Object</span></span>

## <span data-ttu-id="58de0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58de0-133">NOTES</span></span>

## <span data-ttu-id="58de0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58de0-134">RELATED LINKS</span></span>

