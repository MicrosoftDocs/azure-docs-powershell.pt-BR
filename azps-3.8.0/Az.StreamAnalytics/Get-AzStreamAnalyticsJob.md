---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941042"
---
# <span data-ttu-id="7a178-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7a178-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="7a178-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a178-102">SYNOPSIS</span></span>
<span data-ttu-id="7a178-103">Obtém informações de trabalhos do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a178-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="7a178-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a178-104">SYNTAX</span></span>

### <span data-ttu-id="7a178-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7a178-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a178-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="7a178-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a178-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a178-107">DESCRIPTION</span></span>
<span data-ttu-id="7a178-108">O cmdlet **Get-AzStreamAnalyticsJob** lista todos os trabalhos do Stream Analytics definidos na assinatura do Azure ou o grupo de recursos especificado ou obtém informações de trabalho sobre um trabalho específico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a178-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="7a178-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a178-109">EXAMPLES</span></span>

### <span data-ttu-id="7a178-110">EXEMPLO 1: obter informações sobre todos os trabalhos em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="7a178-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="7a178-111">Esse comando retorna informações sobre todos os trabalhos do Stream Analytics na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a178-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="7a178-112">EXEMPLO 2: obter informações sobre todos os trabalhos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7a178-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="7a178-113">Esse comando retorna informações sobre todos os trabalhos do Stream Analytics no grupo de recursos StreamAnalytics-padrão-oeste-US.</span><span class="sxs-lookup"><span data-stu-id="7a178-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="7a178-114">EXEMPLO 3: obter informações sobre um trabalho específico em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7a178-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="7a178-115">Esse comando retorna informações sobre o trabalho do Stream Analytics StreamingJob no grupo de recursos StreamAnalytics-padrão-oeste-US.</span><span class="sxs-lookup"><span data-stu-id="7a178-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="7a178-116">OS</span><span class="sxs-lookup"><span data-stu-id="7a178-116">PARAMETERS</span></span>

### <span data-ttu-id="7a178-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a178-117">-DefaultProfile</span></span>
<span data-ttu-id="7a178-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a178-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a178-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a178-119">-Name</span></span>
<span data-ttu-id="7a178-120">Especifica o nome do trabalho do Azure Stream Analytics a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7a178-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a178-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="7a178-121">-NoExpand</span></span>
<span data-ttu-id="7a178-122">Indica que o cmdlet recuperará o trabalho do Azure Stream Analytics, mas não retornará informações sobre suas entradas, saídas e transformações.</span><span class="sxs-lookup"><span data-stu-id="7a178-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a178-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a178-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a178-124">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="7a178-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a178-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a178-125">CommonParameters</span></span>
<span data-ttu-id="7a178-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a178-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a178-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a178-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a178-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a178-128">INPUTS</span></span>

### <span data-ttu-id="7a178-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7a178-129">System.String</span></span>

### <span data-ttu-id="7a178-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a178-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a178-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a178-131">OUTPUTS</span></span>

### <span data-ttu-id="7a178-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="7a178-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="7a178-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a178-133">NOTES</span></span>

## <span data-ttu-id="7a178-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a178-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a178-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7a178-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7a178-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7a178-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7a178-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7a178-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7a178-138">Parar-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7a178-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


