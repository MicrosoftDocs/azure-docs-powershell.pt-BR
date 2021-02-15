---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112445"
---
# <span data-ttu-id="b515e-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="b515e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b515e-102">SYNOPSIS</span></span>
<span data-ttu-id="b515e-103">Interrompe um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b515e-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="b515e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b515e-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b515e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b515e-105">DESCRIPTION</span></span>
<span data-ttu-id="b515e-106">O cmdlet **Stop-AzStreamAnalytics Job** assíncrona impede que um trabalho do Stream Analytics seja executado no Azure e desloque recursos que estavam sendo usados.</span><span class="sxs-lookup"><span data-stu-id="b515e-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="b515e-107">A definição de trabalho e os metadados permanecem disponíveis em sua assinatura por meio do Portal do Azure e apIs de gerenciamento, para que o trabalho possa ser editado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b515e-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="b515e-108">Você não será cobrado por um trabalho no estado Interrompido.</span><span class="sxs-lookup"><span data-stu-id="b515e-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="b515e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b515e-109">EXAMPLES</span></span>

### <span data-ttu-id="b515e-110">Exemplo 1: Parar um trabalho de execução</span><span class="sxs-lookup"><span data-stu-id="b515e-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b515e-111">Este comando interrompe o trabalho Streaming Job.</span><span class="sxs-lookup"><span data-stu-id="b515e-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="b515e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b515e-112">PARAMETERS</span></span>

### <span data-ttu-id="b515e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b515e-113">-DefaultProfile</span></span>
<span data-ttu-id="b515e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b515e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b515e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b515e-115">-Name</span></span>
<span data-ttu-id="b515e-116">Especifica o nome do trabalho do Azure Stream Analytics para parar.</span><span class="sxs-lookup"><span data-stu-id="b515e-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="b515e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b515e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b515e-118">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="b515e-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="b515e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b515e-119">CommonParameters</span></span>
<span data-ttu-id="b515e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b515e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b515e-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b515e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b515e-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="b515e-122">INPUTS</span></span>

### <span data-ttu-id="b515e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b515e-123">System.String</span></span>

## <span data-ttu-id="b515e-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="b515e-124">OUTPUTS</span></span>

### <span data-ttu-id="b515e-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b515e-125">System.Boolean</span></span>

## <span data-ttu-id="b515e-126">Notas</span><span class="sxs-lookup"><span data-stu-id="b515e-126">NOTES</span></span>

## <span data-ttu-id="b515e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b515e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b515e-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b515e-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b515e-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b515e-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b515e-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b515e-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


