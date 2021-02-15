---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112466"
---
# <span data-ttu-id="fad66-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="fad66-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="fad66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fad66-102">SYNOPSIS</span></span>
<span data-ttu-id="fad66-103">Obtém informações sobre uma transformação de trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="fad66-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="fad66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fad66-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fad66-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fad66-105">DESCRIPTION</span></span>
<span data-ttu-id="fad66-106">O cmdlet **Get-AzStreamAnalyticsTransformation obtém** informações sobre uma transformação definida em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="fad66-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="fad66-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fad66-107">EXAMPLES</span></span>

### <span data-ttu-id="fad66-108">EXEMPLO 1: Obter informações sobre uma transformação do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="fad66-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="fad66-109">Esse comando retorna informações sobre a transformação chamada Streaming Job no trabalho chamado Streaming Job.</span><span class="sxs-lookup"><span data-stu-id="fad66-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="fad66-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fad66-110">PARAMETERS</span></span>

### <span data-ttu-id="fad66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad66-111">-DefaultProfile</span></span>
<span data-ttu-id="fad66-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fad66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad66-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="fad66-113">-JobName</span></span>
<span data-ttu-id="fad66-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="fad66-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="fad66-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fad66-115">-Name</span></span>
<span data-ttu-id="fad66-116">Especifica o nome da transformação do Azure Stream Analytics a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="fad66-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="fad66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad66-117">-ResourceGroupName</span></span>
<span data-ttu-id="fad66-118">Especifica o nome do grupo de recursos ao qual a transformação do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="fad66-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="fad66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad66-119">CommonParameters</span></span>
<span data-ttu-id="fad66-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad66-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad66-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad66-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="fad66-122">INPUTS</span></span>

### <span data-ttu-id="fad66-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fad66-123">System.String</span></span>

## <span data-ttu-id="fad66-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="fad66-124">OUTPUTS</span></span>

### <span data-ttu-id="fad66-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="fad66-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="fad66-126">Notas</span><span class="sxs-lookup"><span data-stu-id="fad66-126">NOTES</span></span>

## <span data-ttu-id="fad66-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fad66-127">RELATED LINKS</span></span>

[<span data-ttu-id="fad66-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="fad66-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


