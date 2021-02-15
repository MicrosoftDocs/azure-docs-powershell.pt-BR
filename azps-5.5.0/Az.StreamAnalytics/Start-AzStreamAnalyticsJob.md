---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112446"
---
# <span data-ttu-id="c535b-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c535b-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="c535b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c535b-102">SYNOPSIS</span></span>
<span data-ttu-id="c535b-103">Inicia um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c535b-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="c535b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c535b-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c535b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c535b-105">DESCRIPTION</span></span>
<span data-ttu-id="c535b-106">O cmdlet **Start-AzStreamAnalytics Job** implanta de forma assíncrona e inicia um trabalho de Análise de Fluxo no Azure.</span><span class="sxs-lookup"><span data-stu-id="c535b-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="c535b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c535b-107">EXAMPLES</span></span>

### <span data-ttu-id="c535b-108">Exemplo 1: Iniciar um trabalho do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="c535b-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="c535b-109">Este comando inicia o trabalho Streaming Job Streaming Job e especifica que o fluxo de evento de saída deve começar no timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="c535b-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="c535b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c535b-110">PARAMETERS</span></span>

### <span data-ttu-id="c535b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c535b-111">-DefaultProfile</span></span>
<span data-ttu-id="c535b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c535b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c535b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c535b-113">-Name</span></span>
<span data-ttu-id="c535b-114">Especifica o nome do trabalho do Azure Stream Analytics para começar.</span><span class="sxs-lookup"><span data-stu-id="c535b-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="c535b-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="c535b-115">-OutputStartMode</span></span>
<span data-ttu-id="c535b-116">Especifica o modo de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c535b-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="c535b-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c535b-117">Valid values are:</span></span> 
- <span data-ttu-id="c535b-118">JobStartTime – Esse valor indica que o ponto de partida do fluxo de eventos de saída deve começar quando o trabalho for iniciado.</span><span class="sxs-lookup"><span data-stu-id="c535b-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="c535b-119">CustomTime - Esse valor indica que o ponto inicial do fluxo de eventos de saída deve começar em um horário personalizado especificado no parâmetro *OutputStartTime.*</span><span class="sxs-lookup"><span data-stu-id="c535b-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="c535b-120">LastOutputEventTime - Esse valor indica que o ponto de partida do stream de evento de saída deve começar a partir do último tempo de saída do evento.</span><span class="sxs-lookup"><span data-stu-id="c535b-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="c535b-121">Se a propriedade estiver ausente, o padrão será JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="c535b-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="c535b-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="c535b-122">-OutputStartTime</span></span>
<span data-ttu-id="c535b-123">Especifica a hora de início da saída.</span><span class="sxs-lookup"><span data-stu-id="c535b-123">Specifies the output start time.</span></span>
<span data-ttu-id="c535b-124">Esse valor é um carimbo de hora formatado iso-8601 que indica o ponto de partida do fluxo de eventos de saída ou $Null para indicar que o fluxo de eventos de saída será iniciado sempre que o trabalho de streaming for iniciado.</span><span class="sxs-lookup"><span data-stu-id="c535b-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="c535b-125">Essa propriedade deve ter um valor se *o OutputStartMode* estiver definido como CustomTime.</span><span class="sxs-lookup"><span data-stu-id="c535b-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="c535b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c535b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c535b-127">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="c535b-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="c535b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c535b-128">CommonParameters</span></span>
<span data-ttu-id="c535b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c535b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c535b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c535b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c535b-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="c535b-131">INPUTS</span></span>

### <span data-ttu-id="c535b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c535b-132">System.String</span></span>

### <span data-ttu-id="c535b-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c535b-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c535b-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c535b-134">OUTPUTS</span></span>

### <span data-ttu-id="c535b-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c535b-135">System.Boolean</span></span>

## <span data-ttu-id="c535b-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c535b-136">NOTES</span></span>

## <span data-ttu-id="c535b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c535b-137">RELATED LINKS</span></span>

[<span data-ttu-id="c535b-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c535b-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c535b-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c535b-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c535b-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c535b-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c535b-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c535b-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


