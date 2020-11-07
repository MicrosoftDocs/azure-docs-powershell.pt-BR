---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: c733c071bb0c7c2bc1c0c2d1fe1c2142d89e8590
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777906"
---
# <span data-ttu-id="698c0-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="698c0-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="698c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="698c0-102">SYNOPSIS</span></span>
<span data-ttu-id="698c0-103">Inicia um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="698c0-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="698c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="698c0-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="698c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="698c0-105">DESCRIPTION</span></span>
<span data-ttu-id="698c0-106">O cmdlet **Start-AzStreamAnalyticsJob** implanta e inicia de forma assíncrona um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="698c0-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="698c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="698c0-107">EXAMPLES</span></span>

### <span data-ttu-id="698c0-108">EXEMPLO 1: iniciar um trabalho do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="698c0-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="698c0-109">Esse comando inicia o trabalho StreamingJob e especifica que o fluxo do evento de saída deve iniciar no timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="698c0-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="698c0-110">OS</span><span class="sxs-lookup"><span data-stu-id="698c0-110">PARAMETERS</span></span>

### <span data-ttu-id="698c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698c0-111">-DefaultProfile</span></span>
<span data-ttu-id="698c0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="698c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="698c0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="698c0-113">-Name</span></span>
<span data-ttu-id="698c0-114">Especifica o nome do trabalho do Azure Stream Analytics para iniciar.</span><span class="sxs-lookup"><span data-stu-id="698c0-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="698c0-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="698c0-115">-OutputStartMode</span></span>
<span data-ttu-id="698c0-116">Especifica o modo de início para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="698c0-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="698c0-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="698c0-117">Valid values are:</span></span> 
- <span data-ttu-id="698c0-118">JobStartTime-esse valor indica que o ponto de partida do fluxo de evento de saída deve começar quando o trabalho for iniciado.</span><span class="sxs-lookup"><span data-stu-id="698c0-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="698c0-119">CustomTime-esse valor indica que o ponto inicial do fluxo do evento de saída deve começar em um horário personalizado especificado no parâmetro *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="698c0-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="698c0-120">LastOutputEventTime-esse valor indica que o ponto de partida do fluxo de evento de saída deve começar no último tempo de saída do evento.</span><span class="sxs-lookup"><span data-stu-id="698c0-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="698c0-121">Se a propriedade estiver ausente, o padrão será JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="698c0-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="698c0-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="698c0-122">-OutputStartTime</span></span>
<span data-ttu-id="698c0-123">Especifica a hora de início da saída.</span><span class="sxs-lookup"><span data-stu-id="698c0-123">Specifies the output start time.</span></span>
<span data-ttu-id="698c0-124">Esse valor é um carimbo de data/hora formatado ISO-8601 que indica o ponto inicial do fluxo de eventos de saída ou $Null para indicar que o fluxo do evento de saída será iniciado sempre que o trabalho de streaming for iniciado.</span><span class="sxs-lookup"><span data-stu-id="698c0-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="698c0-125">Essa propriedade deve ter um valor se *OutputStartMode* estiver definida como CustomTime.</span><span class="sxs-lookup"><span data-stu-id="698c0-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="698c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="698c0-127">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="698c0-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="698c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698c0-128">CommonParameters</span></span>
<span data-ttu-id="698c0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698c0-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698c0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698c0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="698c0-131">INPUTS</span></span>

### <span data-ttu-id="698c0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="698c0-132">System.String</span></span>

### <span data-ttu-id="698c0-133">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="698c0-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="698c0-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="698c0-134">OUTPUTS</span></span>

### <span data-ttu-id="698c0-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="698c0-135">System.Boolean</span></span>

## <span data-ttu-id="698c0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="698c0-136">NOTES</span></span>

## <span data-ttu-id="698c0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="698c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="698c0-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="698c0-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="698c0-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="698c0-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="698c0-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="698c0-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="698c0-141">Parar-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="698c0-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


