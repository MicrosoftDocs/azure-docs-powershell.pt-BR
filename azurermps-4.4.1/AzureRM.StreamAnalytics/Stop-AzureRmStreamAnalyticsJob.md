---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 990cd9d10dd90ee68c179fa65ea4d0575bdda1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427731"
---
# <span data-ttu-id="2aee4-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="2aee4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2aee4-102">SYNOPSIS</span></span>
<span data-ttu-id="2aee4-103">Interrompe um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2aee4-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aee4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2aee4-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aee4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2aee4-105">DESCRIPTION</span></span>
<span data-ttu-id="2aee4-106">O cmdlet **Stop-AzureRmStreamAnalyticsJob** interrompe de forma assíncrona um trabalho do Stream Analytics seja executado no Azure e desatribuirá os recursos que estavam sendo usados.</span><span class="sxs-lookup"><span data-stu-id="2aee4-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="2aee4-107">A definição do trabalho e os metadados permanecem disponíveis na sua assinatura por meio do portal do Azure e das APIs de gerenciamento, de forma que o trabalho possa ser editado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="2aee4-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="2aee4-108">Você não será cobrado por um trabalho no estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="2aee4-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="2aee4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aee4-109">EXAMPLES</span></span>

### <span data-ttu-id="2aee4-110">EXEMPLO 1: parar um trabalho em execução</span><span class="sxs-lookup"><span data-stu-id="2aee4-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="2aee4-111">Esse comando interrompe o trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2aee4-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="2aee4-112">OS</span><span class="sxs-lookup"><span data-stu-id="2aee4-112">PARAMETERS</span></span>

### <span data-ttu-id="2aee4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2aee4-113">-Name</span></span>
<span data-ttu-id="2aee4-114">Especifica o nome do trabalho do Azure Stream Analytics para parar.</span><span class="sxs-lookup"><span data-stu-id="2aee4-114">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="2aee4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aee4-115">-ResourceGroupName</span></span>
<span data-ttu-id="2aee4-116">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="2aee4-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="2aee4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aee4-117">-DefaultProfile</span></span>
<span data-ttu-id="2aee4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aee4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aee4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aee4-119">CommonParameters</span></span>
<span data-ttu-id="2aee4-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aee4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aee4-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aee4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aee4-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2aee4-122">INPUTS</span></span>

## <span data-ttu-id="2aee4-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2aee4-123">OUTPUTS</span></span>

### <span data-ttu-id="2aee4-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="2aee4-124">System.Object</span></span>

## <span data-ttu-id="2aee4-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2aee4-125">NOTES</span></span>

## <span data-ttu-id="2aee4-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aee4-126">RELATED LINKS</span></span>

[<span data-ttu-id="2aee4-127">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-127">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2aee4-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2aee4-129">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-129">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2aee4-130">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-130">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2aee4-131">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2aee4-131">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


