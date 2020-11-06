---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: bf4a8734304ce92dac1bc329d6ae0ffa0f30c09c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598462"
---
# <span data-ttu-id="af914-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="af914-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="af914-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af914-102">SYNOPSIS</span></span>
<span data-ttu-id="af914-103">Obtém as saídas definidas em um trabalho ou saída de análise de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="af914-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="af914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af914-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af914-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af914-105">DESCRIPTION</span></span>
<span data-ttu-id="af914-106">O cmdlet **Get-AzStreamAnalyticsOutput** lista todas as saídas definidas em um trabalho de análise de fluxo especificado ou obtém informações sobre uma saída específica.</span><span class="sxs-lookup"><span data-stu-id="af914-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="af914-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af914-107">EXAMPLES</span></span>

### <span data-ttu-id="af914-108">EXEMPLO 1: obter informações sobre saídas de trabalho</span><span class="sxs-lookup"><span data-stu-id="af914-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="af914-109">Esse comando retorna informações sobre as saídas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="af914-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="af914-110">EXEMPLO 2: obter informações sobre uma saída de trabalho específica</span><span class="sxs-lookup"><span data-stu-id="af914-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="af914-111">Esse comando retorna informações sobre a saída chamada output definida no Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="af914-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="af914-112">OS</span><span class="sxs-lookup"><span data-stu-id="af914-112">PARAMETERS</span></span>

### <span data-ttu-id="af914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af914-113">-DefaultProfile</span></span>
<span data-ttu-id="af914-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af914-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af914-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="af914-115">-JobName</span></span>
<span data-ttu-id="af914-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="af914-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="af914-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="af914-117">-Name</span></span>
<span data-ttu-id="af914-118">Especifica o nome da saída do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="af914-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="af914-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af914-119">-ResourceGroupName</span></span>
<span data-ttu-id="af914-120">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="af914-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="af914-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af914-121">CommonParameters</span></span>
<span data-ttu-id="af914-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af914-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af914-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af914-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af914-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af914-124">INPUTS</span></span>

### <span data-ttu-id="af914-125">System. String</span><span class="sxs-lookup"><span data-stu-id="af914-125">System.String</span></span>

## <span data-ttu-id="af914-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af914-126">OUTPUTS</span></span>

### <span data-ttu-id="af914-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="af914-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="af914-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af914-128">NOTES</span></span>

## <span data-ttu-id="af914-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af914-129">RELATED LINKS</span></span>

[<span data-ttu-id="af914-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="af914-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="af914-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="af914-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="af914-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="af914-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


