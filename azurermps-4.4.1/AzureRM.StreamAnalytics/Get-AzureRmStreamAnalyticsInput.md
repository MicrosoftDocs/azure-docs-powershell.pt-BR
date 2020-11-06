---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: e9f4017156a72b1284de8b62d1ae2ebf7d8321ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429939"
---
# <span data-ttu-id="58322-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58322-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="58322-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58322-102">SYNOPSIS</span></span>
<span data-ttu-id="58322-103">Obtém as entradas do trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="58322-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58322-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58322-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58322-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58322-105">DESCRIPTION</span></span>
<span data-ttu-id="58322-106">O cmdlet **Get-AzureRmStreamAnalyticsInput** lista todas as entradas definidas em um trabalho do Stream Analytics ou obtém informações sobre uma entrada específica.</span><span class="sxs-lookup"><span data-stu-id="58322-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="58322-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58322-107">EXAMPLES</span></span>

### <span data-ttu-id="58322-108">EXEMPLO 1: obter informações sobre as entradas definidas em um trabalho</span><span class="sxs-lookup"><span data-stu-id="58322-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="58322-109">Esse comando retorna informações sobre todas as entradas definidas no trabalho StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="58322-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="58322-110">EXEMPLO 2: obter informações sobre uma entrada específica definida em um trabalho</span><span class="sxs-lookup"><span data-stu-id="58322-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="58322-111">Esse comando retorna informações sobre a entrada chamada EntryStream definida no StreamingJob do trabalho.</span><span class="sxs-lookup"><span data-stu-id="58322-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="58322-112">OS</span><span class="sxs-lookup"><span data-stu-id="58322-112">PARAMETERS</span></span>

### <span data-ttu-id="58322-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="58322-113">-JobName</span></span>
<span data-ttu-id="58322-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="58322-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="58322-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="58322-115">-Name</span></span>
<span data-ttu-id="58322-116">Especifica o nome da entrada do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="58322-116">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="58322-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58322-117">-ResourceGroupName</span></span>
<span data-ttu-id="58322-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="58322-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="58322-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58322-119">-DefaultProfile</span></span>
<span data-ttu-id="58322-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58322-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58322-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58322-121">CommonParameters</span></span>
<span data-ttu-id="58322-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58322-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58322-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58322-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58322-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58322-124">INPUTS</span></span>

## <span data-ttu-id="58322-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58322-125">OUTPUTS</span></span>

### <span data-ttu-id="58322-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="58322-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="58322-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58322-127">NOTES</span></span>

## <span data-ttu-id="58322-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58322-128">RELATED LINKS</span></span>

[<span data-ttu-id="58322-129">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58322-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="58322-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58322-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="58322-131">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="58322-131">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)

