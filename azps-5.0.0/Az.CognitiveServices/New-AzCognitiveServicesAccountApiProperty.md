---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281438"
---
# <span data-ttu-id="24868-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="24868-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="24868-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24868-102">SYNOPSIS</span></span>
<span data-ttu-id="24868-103">Gerar uma nova instância de ApiProperties de conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="24868-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="24868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24868-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24868-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24868-105">DESCRIPTION</span></span>
<span data-ttu-id="24868-106">Gere uma nova instância de ApiProperties de conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="24868-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="24868-107">ApiProperties pode ser usado ao criar uma nova conta ou atualizar uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="24868-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="24868-108">O ApiProperties é necessário para determinados tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="24868-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="24868-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24868-109">EXAMPLES</span></span>

### <span data-ttu-id="24868-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24868-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="24868-111">A seguir, o exemplo criará uma conta QnAMaker com a propriedade API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="24868-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="24868-112">OS</span><span class="sxs-lookup"><span data-stu-id="24868-112">PARAMETERS</span></span>

### <span data-ttu-id="24868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24868-113">-DefaultProfile</span></span>
<span data-ttu-id="24868-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24868-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24868-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24868-115">-Confirm</span></span>
<span data-ttu-id="24868-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24868-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24868-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24868-117">-WhatIf</span></span>
<span data-ttu-id="24868-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24868-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24868-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24868-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24868-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24868-120">CommonParameters</span></span>
<span data-ttu-id="24868-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24868-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24868-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24868-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24868-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24868-123">INPUTS</span></span>

### <span data-ttu-id="24868-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="24868-124">None</span></span>

## <span data-ttu-id="24868-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24868-125">OUTPUTS</span></span>

### <span data-ttu-id="24868-126">Microsoft. Azure. Management. Cognitivaservices. Models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="24868-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="24868-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24868-127">NOTES</span></span>

## <span data-ttu-id="24868-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24868-128">RELATED LINKS</span></span>
