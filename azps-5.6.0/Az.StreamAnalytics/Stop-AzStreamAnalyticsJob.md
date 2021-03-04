---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2a13466b792426cdf06b7c52a8067f3adf5b787d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890686"
---
# <span data-ttu-id="65c30-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="65c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65c30-102">SYNOPSIS</span></span>
<span data-ttu-id="65c30-103">Interrompe um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="65c30-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="65c30-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65c30-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65c30-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65c30-105">DESCRIPTION</span></span>
<span data-ttu-id="65c30-106">O cmdlet **Stop-AzStreamAnalyticsJob** de forma assíncrona impede que um trabalho do Stream Analytics seja executado no Azure e desloque recursos que estavam sendo usados.</span><span class="sxs-lookup"><span data-stu-id="65c30-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="65c30-107">A definição de trabalho e os metadados permanecem disponíveis em sua assinatura por meio das APIs do Portal do Azure e do Gerenciamento, de forma que o trabalho possa ser editado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="65c30-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="65c30-108">Você não será cobrado por um trabalho no estado Parado.</span><span class="sxs-lookup"><span data-stu-id="65c30-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="65c30-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65c30-109">EXAMPLES</span></span>

### <span data-ttu-id="65c30-110">Exemplo 1: Parar um trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="65c30-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="65c30-111">Este comando interrompe o trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="65c30-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="65c30-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65c30-112">PARAMETERS</span></span>

### <span data-ttu-id="65c30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c30-113">-DefaultProfile</span></span>
<span data-ttu-id="65c30-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65c30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c30-115">-Name</span><span class="sxs-lookup"><span data-stu-id="65c30-115">-Name</span></span>
<span data-ttu-id="65c30-116">Especifica o nome do trabalho do Azure Stream Analytics para parar.</span><span class="sxs-lookup"><span data-stu-id="65c30-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="65c30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c30-117">-ResourceGroupName</span></span>
<span data-ttu-id="65c30-118">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="65c30-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="65c30-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c30-119">CommonParameters</span></span>
<span data-ttu-id="65c30-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c30-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c30-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c30-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c30-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65c30-122">INPUTS</span></span>

### <span data-ttu-id="65c30-123">System.String</span><span class="sxs-lookup"><span data-stu-id="65c30-123">System.String</span></span>

## <span data-ttu-id="65c30-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65c30-124">OUTPUTS</span></span>

### <span data-ttu-id="65c30-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65c30-125">System.Boolean</span></span>

## <span data-ttu-id="65c30-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="65c30-126">NOTES</span></span>

## <span data-ttu-id="65c30-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65c30-127">RELATED LINKS</span></span>

[<span data-ttu-id="65c30-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="65c30-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="65c30-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="65c30-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="65c30-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65c30-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


