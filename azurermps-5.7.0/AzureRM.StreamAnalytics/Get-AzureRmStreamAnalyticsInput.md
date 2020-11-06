---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427396"
---
# <span data-ttu-id="cc3d2-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="cc3d2-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="cc3d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3d2-103">Obtém as entradas do trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc3d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc3d2-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc3d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3d2-106">O cmdlet **Get-AzureRmStreamAnalyticsInput** lista todas as entradas definidas em um trabalho do Stream Analytics ou obtém informações sobre uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="cc3d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc3d2-108">EXEMPLO 1: obter informações sobre as entradas definidas em um trabalho</span><span class="sxs-lookup"><span data-stu-id="cc3d2-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="cc3d2-109">Esse comando retorna informações sobre todas as entradas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="cc3d2-110">EXEMPLO 2: obter informações sobre uma entrada específica definida em um trabalho</span><span class="sxs-lookup"><span data-stu-id="cc3d2-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="cc3d2-111">Esse comando retorna informações sobre a entrada chamada EntryStream definida no StreamingJob do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="cc3d2-112">OS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-112">PARAMETERS</span></span>

### <span data-ttu-id="cc3d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3d2-113">-DefaultProfile</span></span>
<span data-ttu-id="cc3d2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc3d2-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="cc3d2-115">-JobName</span></span>
<span data-ttu-id="cc3d2-116">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="cc3d2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc3d2-117">-Name</span></span>
<span data-ttu-id="cc3d2-118">Especifica o nome da entrada do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc3d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc3d2-120">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="cc3d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3d2-121">CommonParameters</span></span>
<span data-ttu-id="cc3d2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3d2-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3d2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc3d2-124">INPUTS</span></span>

### <span data-ttu-id="cc3d2-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cc3d2-125">None</span></span>
<span data-ttu-id="cc3d2-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc3d2-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc3d2-127">OUTPUTS</span></span>

### <span data-ttu-id="cc3d2-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="cc3d2-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="cc3d2-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc3d2-129">NOTES</span></span>

## <span data-ttu-id="cc3d2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="cc3d2-131">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="cc3d2-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="cc3d2-132">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="cc3d2-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="cc3d2-133">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="cc3d2-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


