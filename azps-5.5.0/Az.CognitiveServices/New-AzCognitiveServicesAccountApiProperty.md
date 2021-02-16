---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117894"
---
# <span data-ttu-id="2d338-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="2d338-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="2d338-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d338-102">SYNOPSIS</span></span>
<span data-ttu-id="2d338-103">Gerar uma nova instância de ApiProperties de Contas dos Serviços Cognitivas</span><span class="sxs-lookup"><span data-stu-id="2d338-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="2d338-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d338-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d338-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d338-105">DESCRIPTION</span></span>
<span data-ttu-id="2d338-106">Gere uma nova instância de ApiProperties de Contas dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="2d338-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="2d338-107">ApiProperties podem ser usadas ao criar uma nova conta ou atualizar uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="2d338-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="2d338-108">ApiProperties é necessária para determinados tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="2d338-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="2d338-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d338-109">EXAMPLES</span></span>

### <span data-ttu-id="2d338-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d338-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="2d338-111">O exemplo acima criará uma conta do QnAMaker, com a propriedade da API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="2d338-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="2d338-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d338-112">PARAMETERS</span></span>

### <span data-ttu-id="2d338-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d338-113">-DefaultProfile</span></span>
<span data-ttu-id="2d338-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d338-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d338-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2d338-115">-Confirm</span></span>
<span data-ttu-id="2d338-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d338-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d338-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d338-117">-WhatIf</span></span>
<span data-ttu-id="2d338-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2d338-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d338-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d338-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d338-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d338-120">CommonParameters</span></span>
<span data-ttu-id="2d338-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d338-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d338-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d338-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d338-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d338-123">INPUTS</span></span>

### <span data-ttu-id="2d338-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2d338-124">None</span></span>

## <span data-ttu-id="2d338-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d338-125">OUTPUTS</span></span>

### <span data-ttu-id="2d338-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="2d338-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="2d338-127">Notas</span><span class="sxs-lookup"><span data-stu-id="2d338-127">NOTES</span></span>

## <span data-ttu-id="2d338-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d338-128">RELATED LINKS</span></span>
