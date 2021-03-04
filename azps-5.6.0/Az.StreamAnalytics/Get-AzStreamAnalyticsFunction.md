---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 681782db0e1621e8d1126ca1f3425ce87e8e30d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888126"
---
# <span data-ttu-id="12a1a-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="12a1a-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="12a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="12a1a-103">Obtém funções em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="12a1a-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="12a1a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12a1a-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a1a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="12a1a-106">O cmdlet **Get-AzStreamAnalyticsFunction** obtém uma lista das funções definidas em um trabalho do Azure Stream Analytics ou informações sobre uma função específica.</span><span class="sxs-lookup"><span data-stu-id="12a1a-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="12a1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="12a1a-108">Exemplo 1: Obter todas as funções do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="12a1a-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="12a1a-109">Este comando obtém as funções definidas no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="12a1a-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="12a1a-110">Exemplo 2: Obter uma função de Análise de Fluxo específica</span><span class="sxs-lookup"><span data-stu-id="12a1a-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="12a1a-111">Este comando obtém informações sobre a função denominada ScoreTweet definida no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="12a1a-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="12a1a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12a1a-112">PARAMETERS</span></span>

### <span data-ttu-id="12a1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a1a-113">-DefaultProfile</span></span>
<span data-ttu-id="12a1a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="12a1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a1a-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="12a1a-115">-JobName</span></span>
<span data-ttu-id="12a1a-116">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="12a1a-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="12a1a-117">Este cmdlet obtém funções para o trabalho que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="12a1a-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a1a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="12a1a-118">-Name</span></span>
<span data-ttu-id="12a1a-119">Especifica o nome da função Stream Analytics que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="12a1a-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a1a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a1a-120">-ResourceGroupName</span></span>
<span data-ttu-id="12a1a-121">Especifica o nome do grupo de recursos ao qual as funções do Stream Analytics pertencem.</span><span class="sxs-lookup"><span data-stu-id="12a1a-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="12a1a-122">Este cmdlet obtém funções para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12a1a-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a1a-123">CommonParameters</span></span>
<span data-ttu-id="12a1a-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a1a-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a1a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a1a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12a1a-126">INPUTS</span></span>

### <span data-ttu-id="12a1a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="12a1a-127">System.String</span></span>

## <span data-ttu-id="12a1a-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12a1a-128">OUTPUTS</span></span>

### <span data-ttu-id="12a1a-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="12a1a-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="12a1a-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="12a1a-130">NOTES</span></span>

## <span data-ttu-id="12a1a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12a1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="12a1a-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="12a1a-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="12a1a-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="12a1a-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="12a1a-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="12a1a-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


