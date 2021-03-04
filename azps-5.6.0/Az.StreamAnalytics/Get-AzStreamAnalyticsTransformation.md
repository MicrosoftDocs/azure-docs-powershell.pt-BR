---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 0c009ed05b475e466ab0b2c0dd7c6f18e70c2f9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888116"
---
# <span data-ttu-id="51e35-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="51e35-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="51e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e35-102">SYNOPSIS</span></span>
<span data-ttu-id="51e35-103">Obtém informações sobre uma transformação de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e35-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="51e35-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51e35-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51e35-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51e35-105">DESCRIPTION</span></span>
<span data-ttu-id="51e35-106">O cmdlet **Get-AzStreamAnalyticsTransformation obtém** informações sobre uma transformação definida em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="51e35-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="51e35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51e35-107">EXAMPLES</span></span>

### <span data-ttu-id="51e35-108">EXEMPLO 1: Obter informações sobre uma transformação do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="51e35-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="51e35-109">Este comando retorna informações sobre a transformação chamada StreamingJob no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="51e35-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="51e35-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51e35-110">PARAMETERS</span></span>

### <span data-ttu-id="51e35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e35-111">-DefaultProfile</span></span>
<span data-ttu-id="51e35-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="51e35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51e35-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="51e35-113">-JobName</span></span>
<span data-ttu-id="51e35-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="51e35-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="51e35-115">-Name</span><span class="sxs-lookup"><span data-stu-id="51e35-115">-Name</span></span>
<span data-ttu-id="51e35-116">Especifica o nome da transformação do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="51e35-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e35-117">-ResourceGroupName</span></span>
<span data-ttu-id="51e35-118">Especifica o nome do grupo de recursos ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="51e35-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="51e35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e35-119">CommonParameters</span></span>
<span data-ttu-id="51e35-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e35-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e35-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e35-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51e35-122">INPUTS</span></span>

### <span data-ttu-id="51e35-123">System.String</span><span class="sxs-lookup"><span data-stu-id="51e35-123">System.String</span></span>

## <span data-ttu-id="51e35-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51e35-124">OUTPUTS</span></span>

### <span data-ttu-id="51e35-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="51e35-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="51e35-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="51e35-126">NOTES</span></span>

## <span data-ttu-id="51e35-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51e35-127">RELATED LINKS</span></span>

[<span data-ttu-id="51e35-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="51e35-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


