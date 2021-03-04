---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 726d9d9294c4cf6e5789399ec821d4657e6f787e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888120"
---
# <span data-ttu-id="13131-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="13131-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="13131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13131-102">SYNOPSIS</span></span>
<span data-ttu-id="13131-103">Obtém entradas de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="13131-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="13131-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="13131-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13131-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13131-105">DESCRIPTION</span></span>
<span data-ttu-id="13131-106">O cmdlet **Get-AzStreamAnalyticsInput** lista todas as entradas definidas em um trabalho do Stream Analytics ou obtém informações sobre uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="13131-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="13131-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13131-107">EXAMPLES</span></span>

### <span data-ttu-id="13131-108">Exemplo 1: obter informações sobre as entradas definidas em um trabalho</span><span class="sxs-lookup"><span data-stu-id="13131-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="13131-109">Este comando retorna informações sobre todas as entradas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="13131-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="13131-110">Exemplo 2: obter informações sobre uma entrada específica definida em um trabalho</span><span class="sxs-lookup"><span data-stu-id="13131-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="13131-111">Este comando retorna informações sobre a entrada chamada EntryStream definida no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="13131-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="13131-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="13131-112">PARAMETERS</span></span>

### <span data-ttu-id="13131-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13131-113">-DefaultProfile</span></span>
<span data-ttu-id="13131-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="13131-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13131-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="13131-115">-JobName</span></span>
<span data-ttu-id="13131-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="13131-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="13131-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13131-117">-Name</span></span>
<span data-ttu-id="13131-118">Especifica o nome da entrada do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="13131-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="13131-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13131-119">-ResourceGroupName</span></span>
<span data-ttu-id="13131-120">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="13131-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="13131-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13131-121">CommonParameters</span></span>
<span data-ttu-id="13131-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13131-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13131-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13131-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13131-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13131-124">INPUTS</span></span>

### <span data-ttu-id="13131-125">System.String</span><span class="sxs-lookup"><span data-stu-id="13131-125">System.String</span></span>

## <span data-ttu-id="13131-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="13131-126">OUTPUTS</span></span>

### <span data-ttu-id="13131-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="13131-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="13131-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="13131-128">NOTES</span></span>

## <span data-ttu-id="13131-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13131-129">RELATED LINKS</span></span>

[<span data-ttu-id="13131-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="13131-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="13131-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="13131-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="13131-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="13131-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


