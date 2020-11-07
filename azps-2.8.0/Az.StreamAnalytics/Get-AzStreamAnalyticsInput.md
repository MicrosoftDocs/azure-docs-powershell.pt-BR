---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: cd6e7e4bf9ba9a99b9b3a9a5f58acb9578236037
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774030"
---
# <span data-ttu-id="58c1f-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58c1f-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="58c1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="58c1f-103">Obtém as entradas do trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="58c1f-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="58c1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c1f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="58c1f-106">O cmdlet **Get-AzStreamAnalyticsInput** lista todas as entradas definidas em um trabalho do Stream Analytics ou obtém informações sobre uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="58c1f-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="58c1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="58c1f-108">EXEMPLO 1: obter informações sobre as entradas definidas em um trabalho</span><span class="sxs-lookup"><span data-stu-id="58c1f-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="58c1f-109">Esse comando retorna informações sobre todas as entradas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="58c1f-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="58c1f-110">EXEMPLO 2: obter informações sobre uma entrada específica definida em um trabalho</span><span class="sxs-lookup"><span data-stu-id="58c1f-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="58c1f-111">Esse comando retorna informações sobre a entrada chamada EntryStream definida no StreamingJob do trabalho.</span><span class="sxs-lookup"><span data-stu-id="58c1f-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="58c1f-112">OS</span><span class="sxs-lookup"><span data-stu-id="58c1f-112">PARAMETERS</span></span>

### <span data-ttu-id="58c1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c1f-113">-DefaultProfile</span></span>
<span data-ttu-id="58c1f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58c1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58c1f-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="58c1f-115">-JobName</span></span>
<span data-ttu-id="58c1f-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="58c1f-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="58c1f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c1f-117">-Name</span></span>
<span data-ttu-id="58c1f-118">Especifica o nome da entrada do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="58c1f-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="58c1f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c1f-119">-ResourceGroupName</span></span>
<span data-ttu-id="58c1f-120">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="58c1f-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="58c1f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c1f-121">CommonParameters</span></span>
<span data-ttu-id="58c1f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c1f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c1f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c1f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c1f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58c1f-124">INPUTS</span></span>

### <span data-ttu-id="58c1f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58c1f-125">System.String</span></span>

## <span data-ttu-id="58c1f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58c1f-126">OUTPUTS</span></span>

### <span data-ttu-id="58c1f-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="58c1f-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="58c1f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58c1f-128">NOTES</span></span>

## <span data-ttu-id="58c1f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58c1f-129">RELATED LINKS</span></span>

[<span data-ttu-id="58c1f-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58c1f-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="58c1f-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58c1f-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="58c1f-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58c1f-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)

