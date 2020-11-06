---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: 281bc9cd39891ab2794901d0425b299cc72c4644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426262"
---
# <span data-ttu-id="2f983-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="2f983-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="2f983-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f983-102">SYNOPSIS</span></span>
<span data-ttu-id="2f983-103">Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="2f983-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f983-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f983-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f983-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f983-105">DESCRIPTION</span></span>
<span data-ttu-id="2f983-106">O cmdlet **Get-AzureRmStreamAnalyticsQuota** Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="2f983-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="2f983-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f983-107">EXAMPLES</span></span>

### <span data-ttu-id="2f983-108">EXEMPLO 1: obter informações sobre a cota de unidade de streaming para uma região</span><span class="sxs-lookup"><span data-stu-id="2f983-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="2f983-109">Esse comando retorna informações sobre a cota da unidade de streaming e o uso na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2f983-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="2f983-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f983-110">PARAMETERS</span></span>

### <span data-ttu-id="2f983-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f983-111">-DefaultProfile</span></span>
<span data-ttu-id="2f983-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f983-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f983-113">-Local</span><span class="sxs-lookup"><span data-stu-id="2f983-113">-Location</span></span>
<span data-ttu-id="2f983-114">Especifica o nome de uma região do Azure ou o local do Data Center para o qual obter informações sobre a cota da unidade de streaming.</span><span class="sxs-lookup"><span data-stu-id="2f983-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="2f983-115">Consulte https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services para obter uma lista de regiões do Azure com suporte.</span><span class="sxs-lookup"><span data-stu-id="2f983-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="2f983-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f983-116">CommonParameters</span></span>
<span data-ttu-id="2f983-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f983-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f983-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f983-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f983-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f983-119">INPUTS</span></span>

### <span data-ttu-id="2f983-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2f983-120">System.String</span></span>

## <span data-ttu-id="2f983-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f983-121">OUTPUTS</span></span>

### <span data-ttu-id="2f983-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="2f983-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="2f983-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f983-123">NOTES</span></span>

## <span data-ttu-id="2f983-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f983-124">RELATED LINKS</span></span>

[<span data-ttu-id="2f983-125">Cmdlets do Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2f983-125">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


