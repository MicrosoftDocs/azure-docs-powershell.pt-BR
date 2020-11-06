---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598457"
---
# <span data-ttu-id="3ba32-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3ba32-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="3ba32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ba32-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba32-103">Obtém informações sobre uma transformação de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ba32-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="3ba32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ba32-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ba32-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ba32-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba32-106">O cmdlet **Get-AzStreamAnalyticsTransformation** Obtém informações sobre uma transformação definida em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ba32-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="3ba32-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ba32-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba32-108">EXEMPLO 1: obter informações sobre uma transformação do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="3ba32-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="3ba32-109">Esse comando retorna informações sobre a transformação chamada StreamingJob no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3ba32-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="3ba32-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ba32-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba32-111">-DefaultProfile</span></span>
<span data-ttu-id="3ba32-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba32-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3ba32-113">-JobName</span></span>
<span data-ttu-id="3ba32-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="3ba32-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="3ba32-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ba32-115">-Name</span></span>
<span data-ttu-id="3ba32-116">Especifica o nome da transformação do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="3ba32-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="3ba32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ba32-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ba32-118">Especifica o nome do grupo de recursos ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="3ba32-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="3ba32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba32-119">CommonParameters</span></span>
<span data-ttu-id="3ba32-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba32-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba32-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba32-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ba32-122">INPUTS</span></span>

### <span data-ttu-id="3ba32-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba32-123">System.String</span></span>

## <span data-ttu-id="3ba32-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ba32-124">OUTPUTS</span></span>

### <span data-ttu-id="3ba32-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="3ba32-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="3ba32-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ba32-126">NOTES</span></span>

## <span data-ttu-id="3ba32-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ba32-127">RELATED LINKS</span></span>

[<span data-ttu-id="3ba32-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3ba32-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


