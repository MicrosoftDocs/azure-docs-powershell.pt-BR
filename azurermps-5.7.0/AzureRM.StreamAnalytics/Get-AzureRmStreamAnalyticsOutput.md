---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: ff9ab6f4efe5794b3f1eca9b8ceab91b5cd11316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431539"
---
# <span data-ttu-id="89674-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="89674-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="89674-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89674-102">SYNOPSIS</span></span>
<span data-ttu-id="89674-103">Obtém as saídas definidas em um trabalho ou saída de análise de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="89674-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89674-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89674-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89674-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89674-105">DESCRIPTION</span></span>
<span data-ttu-id="89674-106">O cmdlet **Get-AzureRmStreamAnalyticsOutput** lista todas as saídas definidas em um trabalho de análise de fluxo especificado ou obtém informações sobre uma saída específica.</span><span class="sxs-lookup"><span data-stu-id="89674-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="89674-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89674-107">EXAMPLES</span></span>

### <span data-ttu-id="89674-108">EXEMPLO 1: obter informações sobre saídas de trabalho</span><span class="sxs-lookup"><span data-stu-id="89674-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="89674-109">Esse comando retorna informações sobre as saídas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="89674-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="89674-110">EXEMPLO 2: obter informações sobre uma saída de trabalho específica</span><span class="sxs-lookup"><span data-stu-id="89674-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="89674-111">Esse comando retorna informações sobre a saída chamada output definida no Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="89674-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="89674-112">OS</span><span class="sxs-lookup"><span data-stu-id="89674-112">PARAMETERS</span></span>

### <span data-ttu-id="89674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89674-113">-DefaultProfile</span></span>
<span data-ttu-id="89674-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89674-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89674-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="89674-115">-JobName</span></span>
<span data-ttu-id="89674-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="89674-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="89674-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="89674-117">-Name</span></span>
<span data-ttu-id="89674-118">Especifica o nome da saída do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="89674-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="89674-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89674-119">-ResourceGroupName</span></span>
<span data-ttu-id="89674-120">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="89674-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="89674-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89674-121">CommonParameters</span></span>
<span data-ttu-id="89674-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89674-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89674-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89674-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89674-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89674-124">INPUTS</span></span>

### <span data-ttu-id="89674-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="89674-125">None</span></span>
<span data-ttu-id="89674-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="89674-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89674-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89674-127">OUTPUTS</span></span>

### <span data-ttu-id="89674-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="89674-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="89674-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89674-129">NOTES</span></span>

## <span data-ttu-id="89674-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89674-130">RELATED LINKS</span></span>

[<span data-ttu-id="89674-131">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="89674-131">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="89674-132">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="89674-132">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="89674-133">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="89674-133">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


