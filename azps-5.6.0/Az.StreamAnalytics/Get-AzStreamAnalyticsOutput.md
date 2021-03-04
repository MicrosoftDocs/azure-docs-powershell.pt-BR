---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888118"
---
# <span data-ttu-id="c5bbe-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c5bbe-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c5bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bbe-103">Obtém as saídas definidas em um trabalho ou saída do Stream Analytics especificado.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="c5bbe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c5bbe-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5bbe-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c5bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bbe-106">O cmdlet **Get-AzStreamAnalyticsOutput** lista todas as saídas definidas em um trabalho de Análise de Fluxo especificado ou obtém informações sobre uma saída específica.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="c5bbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bbe-108">Exemplo 1: obter informações sobre saídas de trabalho</span><span class="sxs-lookup"><span data-stu-id="c5bbe-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="c5bbe-109">Este comando retorna informações sobre as saídas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="c5bbe-110">Exemplo 2: obter informações sobre uma saída de trabalho específica</span><span class="sxs-lookup"><span data-stu-id="c5bbe-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c5bbe-111">Este comando retorna informações sobre a saída denominada Saída definida no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="c5bbe-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-112">PARAMETERS</span></span>

### <span data-ttu-id="c5bbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bbe-113">-DefaultProfile</span></span>
<span data-ttu-id="c5bbe-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bbe-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="c5bbe-115">-JobName</span></span>
<span data-ttu-id="c5bbe-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c5bbe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c5bbe-117">-Name</span></span>
<span data-ttu-id="c5bbe-118">Especifica o nome da saída do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="c5bbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5bbe-120">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c5bbe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bbe-121">CommonParameters</span></span>
<span data-ttu-id="c5bbe-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bbe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bbe-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bbe-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bbe-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-124">INPUTS</span></span>

### <span data-ttu-id="c5bbe-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c5bbe-125">System.String</span></span>

## <span data-ttu-id="c5bbe-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-126">OUTPUTS</span></span>

### <span data-ttu-id="c5bbe-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="c5bbe-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="c5bbe-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="c5bbe-128">NOTES</span></span>

## <span data-ttu-id="c5bbe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5bbe-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5bbe-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c5bbe-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c5bbe-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c5bbe-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c5bbe-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c5bbe-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


