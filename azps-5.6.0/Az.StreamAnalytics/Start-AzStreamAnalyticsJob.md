---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: cd7d6aaa9a295f888d8e765d12b4088525eff1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890691"
---
# <span data-ttu-id="2e5e5-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e5e5-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="2e5e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5e5-103">Inicia um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="2e5e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e5e5-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e5e5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e5e5-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5e5-106">O cmdlet **Start-AzStreamAnalyticsJob** implanta de forma assíncrona e inicia um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="2e5e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-107">EXAMPLES</span></span>

### <span data-ttu-id="2e5e5-108">Exemplo 1: Iniciar um trabalho do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2e5e5-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="2e5e5-109">Este comando inicia o trabalho StreamingJob e especifica que o fluxo de eventos de saída deve começar no timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="2e5e5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-110">PARAMETERS</span></span>

### <span data-ttu-id="2e5e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5e5-111">-DefaultProfile</span></span>
<span data-ttu-id="2e5e5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e5e5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2e5e5-113">-Name</span></span>
<span data-ttu-id="2e5e5-114">Especifica o nome do trabalho do Azure Stream Analytics para iniciar.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="2e5e5-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="2e5e5-115">-OutputStartMode</span></span>
<span data-ttu-id="2e5e5-116">Especifica o modo de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="2e5e5-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="2e5e5-117">Valid values are:</span></span> 
- <span data-ttu-id="2e5e5-118">JobStartTime - Esse valor indica que o ponto inicial do fluxo de eventos de saída deve começar quando o trabalho for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="2e5e5-119">CustomTime - Esse valor indica que o ponto inicial do fluxo de eventos de saída deve começar em um horário personalizado especificado no parâmetro *OutputStartTime.*</span><span class="sxs-lookup"><span data-stu-id="2e5e5-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="2e5e5-120">LastOutputEventTime - Esse valor indica que o ponto inicial do fluxo de eventos de saída deve começar a partir do último tempo de saída do evento.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="2e5e5-121">Se a propriedade estiver ausente, o padrão será JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="2e5e5-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="2e5e5-122">-OutputStartTime</span></span>
<span data-ttu-id="2e5e5-123">Especifica o horário de início da saída.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-123">Specifies the output start time.</span></span>
<span data-ttu-id="2e5e5-124">Esse valor é um carimbo de hora formatado ISO-8601 que indica o ponto inicial do fluxo de eventos de saída ou $Null para indicar que o fluxo de eventos de saída será iniciado sempre que o trabalho de streaming for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="2e5e5-125">Essa propriedade deve ter um valor *se OutputStartMode* estiver definido como CustomTime.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e5e5-127">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="2e5e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5e5-128">CommonParameters</span></span>
<span data-ttu-id="2e5e5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5e5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5e5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5e5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-131">INPUTS</span></span>

### <span data-ttu-id="2e5e5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2e5e5-132">System.String</span></span>

### <span data-ttu-id="2e5e5-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e5e5-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2e5e5-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-134">OUTPUTS</span></span>

### <span data-ttu-id="2e5e5-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e5e5-135">System.Boolean</span></span>

## <span data-ttu-id="2e5e5-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e5e5-136">NOTES</span></span>

## <span data-ttu-id="2e5e5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e5e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e5e5-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e5e5-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e5e5-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e5e5-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e5e5-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e5e5-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e5e5-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e5e5-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


