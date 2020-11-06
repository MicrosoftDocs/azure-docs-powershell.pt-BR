---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b012704eebfa9d2c2a868679450cd0231667f585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611079"
---
# <span data-ttu-id="2d968-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2d968-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="2d968-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d968-102">SYNOPSIS</span></span>
<span data-ttu-id="2d968-103">Inicia um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2d968-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d968-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d968-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d968-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d968-105">DESCRIPTION</span></span>
<span data-ttu-id="2d968-106">O cmdlet **Start-AzureRmStreamAnalyticsJob** implanta e inicia de forma assíncrona um trabalho do Stream Analytics no Azure.</span><span class="sxs-lookup"><span data-stu-id="2d968-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="2d968-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d968-107">EXAMPLES</span></span>

### <span data-ttu-id="2d968-108">EXEMPLO 1: iniciar um trabalho do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2d968-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="2d968-109">Esse comando inicia o trabalho StreamingJob e especifica que o fluxo do evento de saída deve iniciar no timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="2d968-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="2d968-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d968-110">PARAMETERS</span></span>

### <span data-ttu-id="2d968-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d968-111">-Name</span></span>
<span data-ttu-id="2d968-112">Especifica o nome do trabalho do Azure Stream Analytics para iniciar.</span><span class="sxs-lookup"><span data-stu-id="2d968-112">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="2d968-113">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="2d968-113">-OutputStartMode</span></span>
<span data-ttu-id="2d968-114">Especifica o modo de início para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="2d968-114">Specifies the start mode for the job.</span></span>
<span data-ttu-id="2d968-115">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="2d968-115">Valid values are:</span></span> 

- <span data-ttu-id="2d968-116">JobStartTime-esse valor indica que o ponto de partida do fluxo de evento de saída deve começar quando o trabalho for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2d968-116">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="2d968-117">CustomTime-esse valor indica que o ponto inicial do fluxo do evento de saída deve começar em um horário personalizado especificado no parâmetro *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="2d968-117">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="2d968-118">--LastOutputEventTime-esse valor indica que o ponto de partida do fluxo de evento de saída deve começar no último tempo de saída do evento.</span><span class="sxs-lookup"><span data-stu-id="2d968-118">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="2d968-119">Se a propriedade estiver ausente, o padrão será JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="2d968-119">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="2d968-120">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="2d968-120">-OutputStartTime</span></span>
<span data-ttu-id="2d968-121">Especifica a hora de início da saída.</span><span class="sxs-lookup"><span data-stu-id="2d968-121">Specifies the output start time.</span></span>
<span data-ttu-id="2d968-122">Esse valor é um carimbo de data/hora formatado ISO-8601 que indica o ponto inicial do fluxo de eventos de saída ou $Null para indicar que o fluxo do evento de saída será iniciado sempre que o trabalho de streaming for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2d968-122">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="2d968-123">Essa propriedade deve ter um valor se *OutputStartMode* estiver definida como CustomTime.</span><span class="sxs-lookup"><span data-stu-id="2d968-123">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="2d968-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d968-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d968-125">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="2d968-125">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="2d968-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d968-126">-DefaultProfile</span></span>
<span data-ttu-id="2d968-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d968-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d968-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d968-128">CommonParameters</span></span>
<span data-ttu-id="2d968-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d968-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d968-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d968-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d968-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d968-131">INPUTS</span></span>

## <span data-ttu-id="2d968-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d968-132">OUTPUTS</span></span>

### <span data-ttu-id="2d968-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="2d968-133">System.Object</span></span>

## <span data-ttu-id="2d968-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d968-134">NOTES</span></span>

## <span data-ttu-id="2d968-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d968-135">RELATED LINKS</span></span>

[<span data-ttu-id="2d968-136">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2d968-136">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2d968-137">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2d968-137">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2d968-138">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2d968-138">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2d968-139">Parar-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2d968-139">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


