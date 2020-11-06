---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426537"
---
# <span data-ttu-id="d1c86-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="d1c86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1c86-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c86-103">Interrompe um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d1c86-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1c86-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1c86-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c86-106">O cmdlet **Stop-AzureRmStreamAnalyticsJob** interrompe de forma assíncrona um trabalho do Stream Analytics seja executado no Azure e desatribuirá os recursos que estavam sendo usados.</span><span class="sxs-lookup"><span data-stu-id="d1c86-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="d1c86-107">A definição do trabalho e os metadados permanecem disponíveis na sua assinatura por meio do portal do Azure e das APIs de gerenciamento, de forma que o trabalho possa ser editado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="d1c86-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="d1c86-108">Você não será cobrado por um trabalho no estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="d1c86-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="d1c86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1c86-109">EXAMPLES</span></span>

### <span data-ttu-id="d1c86-110">EXEMPLO 1: parar um trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="d1c86-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d1c86-111">Esse comando interrompe o trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d1c86-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="d1c86-112">OS</span><span class="sxs-lookup"><span data-stu-id="d1c86-112">PARAMETERS</span></span>

### <span data-ttu-id="d1c86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c86-113">-DefaultProfile</span></span>
<span data-ttu-id="d1c86-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c86-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1c86-115">-Name</span></span>
<span data-ttu-id="d1c86-116">Especifica o nome do trabalho do Azure Stream Analytics para parar.</span><span class="sxs-lookup"><span data-stu-id="d1c86-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="d1c86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c86-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1c86-118">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="d1c86-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="d1c86-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c86-119">CommonParameters</span></span>
<span data-ttu-id="d1c86-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c86-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c86-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c86-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c86-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1c86-122">INPUTS</span></span>

### <span data-ttu-id="d1c86-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d1c86-123">None</span></span>
<span data-ttu-id="d1c86-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d1c86-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1c86-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1c86-125">OUTPUTS</span></span>

### <span data-ttu-id="d1c86-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="d1c86-126">System.Object</span></span>

## <span data-ttu-id="d1c86-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1c86-127">NOTES</span></span>

## <span data-ttu-id="d1c86-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1c86-128">RELATED LINKS</span></span>

[<span data-ttu-id="d1c86-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1c86-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1c86-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1c86-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d1c86-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d1c86-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


