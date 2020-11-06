---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602826"
---
# <span data-ttu-id="df842-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="df842-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="df842-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df842-102">SYNOPSIS</span></span>
<span data-ttu-id="df842-103">Obtém informações sobre uma transformação de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="df842-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df842-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df842-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df842-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df842-105">DESCRIPTION</span></span>
<span data-ttu-id="df842-106">O cmdlet **Get-AzureRmStreamAnalyticsTransformation** Obtém informações sobre uma transformação definida em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="df842-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="df842-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df842-107">EXAMPLES</span></span>

### <span data-ttu-id="df842-108">EXEMPLO 1: obter informações sobre uma transformação do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="df842-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="df842-109">Esse comando retorna informações sobre a transformação chamada StreamingJob no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="df842-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="df842-110">OS</span><span class="sxs-lookup"><span data-stu-id="df842-110">PARAMETERS</span></span>

### <span data-ttu-id="df842-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df842-111">-DefaultProfile</span></span>
<span data-ttu-id="df842-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df842-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df842-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="df842-113">-JobName</span></span>
<span data-ttu-id="df842-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="df842-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="df842-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="df842-115">-Name</span></span>
<span data-ttu-id="df842-116">Especifica o nome da transformação do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="df842-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df842-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df842-117">-ResourceGroupName</span></span>
<span data-ttu-id="df842-118">Especifica o nome do grupo de recursos ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="df842-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="df842-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df842-119">CommonParameters</span></span>
<span data-ttu-id="df842-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df842-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df842-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df842-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df842-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df842-122">INPUTS</span></span>

### <span data-ttu-id="df842-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="df842-123">None</span></span>
<span data-ttu-id="df842-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="df842-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df842-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df842-125">OUTPUTS</span></span>

### <span data-ttu-id="df842-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="df842-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="df842-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df842-127">NOTES</span></span>

## <span data-ttu-id="df842-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df842-128">RELATED LINKS</span></span>

[<span data-ttu-id="df842-129">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="df842-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


