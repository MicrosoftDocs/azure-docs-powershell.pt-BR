---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: dd2a52167a773b241364311ed4e0e00c03ea8459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429646"
---
# <span data-ttu-id="8d072-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8d072-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="8d072-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d072-102">SYNOPSIS</span></span>
<span data-ttu-id="8d072-103">Obtém funções em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="8d072-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d072-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d072-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d072-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d072-105">DESCRIPTION</span></span>
<span data-ttu-id="8d072-106">O cmdlet **Get-AzureRmStreamAnalyticsFunction** Obtém uma lista das funções definidas em um trabalho do Azure Stream Analytics ou informações sobre uma função específica.</span><span class="sxs-lookup"><span data-stu-id="8d072-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="8d072-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d072-107">EXAMPLES</span></span>

### <span data-ttu-id="8d072-108">Exemplo 1: obter todas as funções do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="8d072-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="8d072-109">Esse comando obtém as funções definidas no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="8d072-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="8d072-110">Exemplo 2: obter uma função de análise de fluxo específica</span><span class="sxs-lookup"><span data-stu-id="8d072-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="8d072-111">Esse comando obtém informações sobre a função chamada ScoreTweet definida no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="8d072-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="8d072-112">OS</span><span class="sxs-lookup"><span data-stu-id="8d072-112">PARAMETERS</span></span>

### <span data-ttu-id="8d072-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d072-113">-DefaultProfile</span></span>
<span data-ttu-id="8d072-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d072-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d072-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="8d072-115">-JobName</span></span>
<span data-ttu-id="8d072-116">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="8d072-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="8d072-117">Este cmdlet obtém funções para o trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8d072-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d072-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d072-118">-Name</span></span>
<span data-ttu-id="8d072-119">Especifica o nome da função do Stream Analytics que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8d072-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d072-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d072-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d072-121">Especifica o nome do grupo de recursos ao qual a função do Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="8d072-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="8d072-122">Este cmdlet obtém funções para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8d072-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d072-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d072-123">CommonParameters</span></span>
<span data-ttu-id="8d072-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d072-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d072-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d072-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d072-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d072-126">INPUTS</span></span>

### <span data-ttu-id="8d072-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8d072-127">None</span></span>
<span data-ttu-id="8d072-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8d072-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d072-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d072-129">OUTPUTS</span></span>

### <span data-ttu-id="8d072-130">System. Collections. Generic. list [Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="8d072-130">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="8d072-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d072-131">NOTES</span></span>

## <span data-ttu-id="8d072-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d072-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d072-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8d072-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8d072-134">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8d072-134">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8d072-135">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8d072-135">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


