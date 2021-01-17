---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432914"
---
# <span data-ttu-id="66fd8-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="66fd8-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="66fd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="66fd8-103">Obtém informações sobre uma transformação de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="66fd8-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="66fd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66fd8-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66fd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="66fd8-106">O cmdlet **Get-AzStreamAnalyticsTransformation** Obtém informações sobre uma transformação definida em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="66fd8-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="66fd8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66fd8-107">EXAMPLES</span></span>

### <span data-ttu-id="66fd8-108">EXEMPLO 1: obter informações sobre uma transformação do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="66fd8-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="66fd8-109">Esse comando retorna informações sobre a transformação chamada StreamingJob no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="66fd8-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="66fd8-110">OS</span><span class="sxs-lookup"><span data-stu-id="66fd8-110">PARAMETERS</span></span>

### <span data-ttu-id="66fd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fd8-111">-DefaultProfile</span></span>
<span data-ttu-id="66fd8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66fd8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66fd8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="66fd8-113">-JobName</span></span>
<span data-ttu-id="66fd8-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="66fd8-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="66fd8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="66fd8-115">-Name</span></span>
<span data-ttu-id="66fd8-116">Especifica o nome da transformação do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="66fd8-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="66fd8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fd8-117">-ResourceGroupName</span></span>
<span data-ttu-id="66fd8-118">Especifica o nome do grupo de recursos ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="66fd8-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="66fd8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fd8-119">CommonParameters</span></span>
<span data-ttu-id="66fd8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fd8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fd8-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fd8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fd8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66fd8-122">INPUTS</span></span>

### <span data-ttu-id="66fd8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="66fd8-123">System.String</span></span>

## <span data-ttu-id="66fd8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66fd8-124">OUTPUTS</span></span>

### <span data-ttu-id="66fd8-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="66fd8-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="66fd8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66fd8-126">NOTES</span></span>

## <span data-ttu-id="66fd8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66fd8-127">RELATED LINKS</span></span>

[<span data-ttu-id="66fd8-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="66fd8-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


