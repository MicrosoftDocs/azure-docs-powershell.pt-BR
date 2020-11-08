---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111251"
---
# <span data-ttu-id="6356f-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="6356f-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="6356f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6356f-102">SYNOPSIS</span></span>
<span data-ttu-id="6356f-103">Obtém a definição padrão de uma função no Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6356f-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="6356f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6356f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6356f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6356f-105">DESCRIPTION</span></span>
<span data-ttu-id="6356f-106">O cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition** Obtém a definição padrão de uma função no Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6356f-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="6356f-107">Você pode usar a definição padrão e o cmdlet New-AzStreamAnalyticsFunction para criar uma função.</span><span class="sxs-lookup"><span data-stu-id="6356f-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="6356f-108">Você pode modificar a definição padrão antes de criar uma função.</span><span class="sxs-lookup"><span data-stu-id="6356f-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="6356f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6356f-109">EXAMPLES</span></span>

### <span data-ttu-id="6356f-110">Exemplo 1: obter a definição padrão de uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="6356f-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="6356f-111">Esse comando obtém a definição padrão da função chamada ScoreTweet usando os parâmetros especificados no RetrieveDefaultDefinitionRequest.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="6356f-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="6356f-112">OS</span><span class="sxs-lookup"><span data-stu-id="6356f-112">PARAMETERS</span></span>

### <span data-ttu-id="6356f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6356f-113">-DefaultProfile</span></span>
<span data-ttu-id="6356f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6356f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6356f-115">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="6356f-115">-File</span></span>
<span data-ttu-id="6356f-116">Especifica o caminho de um arquivo. JSON que contém a representação JSON (JavaScript Object Notation) do corpo da solicitação da solicitação de definição da função padrão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6356f-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6356f-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="6356f-117">-JobName</span></span>
<span data-ttu-id="6356f-118">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="6356f-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="6356f-119">Esse cmdlet obtém a definição padrão para uma função no trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6356f-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="6356f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6356f-120">-Name</span></span>
<span data-ttu-id="6356f-121">Especifica o nome da função Stream Analytics para a qual esse cmdlet obtém a definição padrão.</span><span class="sxs-lookup"><span data-stu-id="6356f-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6356f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6356f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6356f-123">Especifica o nome do grupo de recursos ao qual a função do Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="6356f-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="6356f-124">Esse cmdlet obtém uma definição de função para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6356f-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6356f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6356f-125">CommonParameters</span></span>
<span data-ttu-id="6356f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6356f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6356f-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6356f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6356f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6356f-128">INPUTS</span></span>

### <span data-ttu-id="6356f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6356f-129">System.String</span></span>

## <span data-ttu-id="6356f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6356f-130">OUTPUTS</span></span>

### <span data-ttu-id="6356f-131">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="6356f-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="6356f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6356f-132">NOTES</span></span>

## <span data-ttu-id="6356f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6356f-133">RELATED LINKS</span></span>

[<span data-ttu-id="6356f-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6356f-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


