---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 7b1b3af4a311b923880253573019c62ee399571c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777905"
---
# <span data-ttu-id="60476-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="60476-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60476-102">SYNOPSIS</span></span>
<span data-ttu-id="60476-103">Interrompe um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="60476-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="60476-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60476-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60476-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60476-105">DESCRIPTION</span></span>
<span data-ttu-id="60476-106">O cmdlet **Stop-AzStreamAnalyticsJob** interrompe de forma assíncrona um trabalho do Stream Analytics seja executado no Azure e desatribuirá os recursos que estavam sendo usados.</span><span class="sxs-lookup"><span data-stu-id="60476-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="60476-107">A definição do trabalho e os metadados permanecem disponíveis na sua assinatura por meio do portal do Azure e das APIs de gerenciamento, de forma que o trabalho possa ser editado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="60476-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="60476-108">Você não será cobrado por um trabalho no estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="60476-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="60476-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60476-109">EXAMPLES</span></span>

### <span data-ttu-id="60476-110">EXEMPLO 1: parar um trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="60476-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="60476-111">Esse comando interrompe o trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="60476-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="60476-112">OS</span><span class="sxs-lookup"><span data-stu-id="60476-112">PARAMETERS</span></span>

### <span data-ttu-id="60476-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60476-113">-DefaultProfile</span></span>
<span data-ttu-id="60476-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60476-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60476-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="60476-115">-Name</span></span>
<span data-ttu-id="60476-116">Especifica o nome do trabalho do Azure Stream Analytics para parar.</span><span class="sxs-lookup"><span data-stu-id="60476-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="60476-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60476-117">-ResourceGroupName</span></span>
<span data-ttu-id="60476-118">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="60476-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="60476-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60476-119">CommonParameters</span></span>
<span data-ttu-id="60476-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60476-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60476-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60476-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60476-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60476-122">INPUTS</span></span>

### <span data-ttu-id="60476-123">System. String</span><span class="sxs-lookup"><span data-stu-id="60476-123">System.String</span></span>

## <span data-ttu-id="60476-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60476-124">OUTPUTS</span></span>

### <span data-ttu-id="60476-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60476-125">System.Boolean</span></span>

## <span data-ttu-id="60476-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60476-126">NOTES</span></span>

## <span data-ttu-id="60476-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60476-127">RELATED LINKS</span></span>

[<span data-ttu-id="60476-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="60476-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="60476-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="60476-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="60476-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="60476-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


