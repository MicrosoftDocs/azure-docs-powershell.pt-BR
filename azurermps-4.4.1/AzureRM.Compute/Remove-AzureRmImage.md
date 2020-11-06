---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440678"
---
# <span data-ttu-id="e1e90-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="e1e90-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="e1e90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1e90-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e90-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="e1e90-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1e90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1e90-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1e90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1e90-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e90-106">O cmdlet **Remove-AzureRmImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="e1e90-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="e1e90-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1e90-107">EXAMPLES</span></span>

### <span data-ttu-id="e1e90-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1e90-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="e1e90-109">Este comando Remove a imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e1e90-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e1e90-110">OS</span><span class="sxs-lookup"><span data-stu-id="e1e90-110">PARAMETERS</span></span>

### <span data-ttu-id="e1e90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e90-111">-DefaultProfile</span></span>
<span data-ttu-id="e1e90-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e90-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e1e90-113">-Force</span></span>
<span data-ttu-id="e1e90-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e1e90-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1e90-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e1e90-115">-ImageName</span></span>
<span data-ttu-id="e1e90-116">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="e1e90-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e90-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1e90-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1e90-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e90-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1e90-119">-Confirm</span></span>
<span data-ttu-id="e1e90-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1e90-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e90-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e90-121">-WhatIf</span></span>
<span data-ttu-id="e1e90-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1e90-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e90-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1e90-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e90-124">CommonParameters</span></span>
<span data-ttu-id="e1e90-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e90-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e90-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e90-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1e90-127">INPUTS</span></span>

### <span data-ttu-id="e1e90-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e90-128">System.String</span></span>

## <span data-ttu-id="e1e90-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1e90-129">OUTPUTS</span></span>

### <span data-ttu-id="e1e90-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="e1e90-130">System.Object</span></span>

## <span data-ttu-id="e1e90-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1e90-131">NOTES</span></span>

## <span data-ttu-id="e1e90-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1e90-132">RELATED LINKS</span></span>
