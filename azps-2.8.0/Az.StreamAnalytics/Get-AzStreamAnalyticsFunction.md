---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 5e34e0b1ba9e9ab24c0cb47de636ceecec9751f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774354"
---
# <span data-ttu-id="556c5-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="556c5-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="556c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="556c5-102">SYNOPSIS</span></span>
<span data-ttu-id="556c5-103">Obtém funções em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="556c5-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="556c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="556c5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="556c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="556c5-105">DESCRIPTION</span></span>
<span data-ttu-id="556c5-106">O cmdlet **Get-AzStreamAnalyticsFunction** Obtém uma lista das funções definidas em um trabalho do Azure Stream Analytics ou informações sobre uma função específica.</span><span class="sxs-lookup"><span data-stu-id="556c5-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="556c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="556c5-107">EXAMPLES</span></span>

### <span data-ttu-id="556c5-108">Exemplo 1: obter todas as funções do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="556c5-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="556c5-109">Esse comando obtém as funções definidas no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="556c5-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="556c5-110">Exemplo 2: obter uma função de análise de fluxo específica</span><span class="sxs-lookup"><span data-stu-id="556c5-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="556c5-111">Esse comando obtém informações sobre a função chamada ScoreTweet definida no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="556c5-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="556c5-112">OS</span><span class="sxs-lookup"><span data-stu-id="556c5-112">PARAMETERS</span></span>

### <span data-ttu-id="556c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556c5-113">-DefaultProfile</span></span>
<span data-ttu-id="556c5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="556c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="556c5-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="556c5-115">-JobName</span></span>
<span data-ttu-id="556c5-116">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="556c5-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="556c5-117">Este cmdlet obtém funções para o trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="556c5-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="556c5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="556c5-118">-Name</span></span>
<span data-ttu-id="556c5-119">Especifica o nome da função do Stream Analytics que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="556c5-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="556c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="556c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="556c5-121">Especifica o nome do grupo de recursos ao qual a função do Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="556c5-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="556c5-122">Este cmdlet obtém funções para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="556c5-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="556c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556c5-123">CommonParameters</span></span>
<span data-ttu-id="556c5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="556c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556c5-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="556c5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556c5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="556c5-126">INPUTS</span></span>

### <span data-ttu-id="556c5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="556c5-127">System.String</span></span>

## <span data-ttu-id="556c5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="556c5-128">OUTPUTS</span></span>

### <span data-ttu-id="556c5-129">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="556c5-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="556c5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="556c5-130">NOTES</span></span>

## <span data-ttu-id="556c5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="556c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="556c5-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="556c5-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="556c5-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="556c5-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="556c5-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="556c5-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


