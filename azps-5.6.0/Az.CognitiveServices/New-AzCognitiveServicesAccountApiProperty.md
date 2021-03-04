---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 50e62158d4b24282753c726845e7dd88d492843c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889035"
---
# <span data-ttu-id="4fcea-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="4fcea-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="4fcea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fcea-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcea-103">Gerar uma nova instância de ApiProperties de Conta de Serviços Cognitivos</span><span class="sxs-lookup"><span data-stu-id="4fcea-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="4fcea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4fcea-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fcea-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4fcea-105">DESCRIPTION</span></span>
<span data-ttu-id="4fcea-106">Gere uma nova instância de ApiProperties de Conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="4fcea-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="4fcea-107">ApiProperties podem ser usadas ao criar uma nova conta ou atualizar uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="4fcea-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="4fcea-108">ApiProperties é exigido por determinados tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="4fcea-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="4fcea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fcea-109">EXAMPLES</span></span>

### <span data-ttu-id="4fcea-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fcea-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="4fcea-111">Exemplo acima criará uma conta QnAMaker, com a propriedade API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="4fcea-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="4fcea-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4fcea-112">PARAMETERS</span></span>

### <span data-ttu-id="4fcea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcea-113">-DefaultProfile</span></span>
<span data-ttu-id="4fcea-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fcea-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fcea-115">-Confirm</span></span>
<span data-ttu-id="4fcea-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fcea-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fcea-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fcea-117">-WhatIf</span></span>
<span data-ttu-id="4fcea-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fcea-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fcea-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fcea-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fcea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcea-120">CommonParameters</span></span>
<span data-ttu-id="4fcea-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fcea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcea-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fcea-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcea-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fcea-123">INPUTS</span></span>

### <span data-ttu-id="4fcea-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4fcea-124">None</span></span>

## <span data-ttu-id="4fcea-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4fcea-125">OUTPUTS</span></span>

### <span data-ttu-id="4fcea-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="4fcea-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="4fcea-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="4fcea-127">NOTES</span></span>

## <span data-ttu-id="4fcea-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fcea-128">RELATED LINKS</span></span>
