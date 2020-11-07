---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947493"
---
# <span data-ttu-id="0510c-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="0510c-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="0510c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0510c-102">SYNOPSIS</span></span>
<span data-ttu-id="0510c-103">Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="0510c-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="0510c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0510c-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0510c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0510c-105">DESCRIPTION</span></span>
<span data-ttu-id="0510c-106">O cmdlet **Get-AzStreamAnalyticsQuota** Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="0510c-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="0510c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0510c-107">EXAMPLES</span></span>

### <span data-ttu-id="0510c-108">EXEMPLO 1: obter informações sobre a cota de unidade de streaming para uma região</span><span class="sxs-lookup"><span data-stu-id="0510c-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="0510c-109">Esse comando retorna informações sobre a cota da unidade de streaming e o uso na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="0510c-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="0510c-110">OS</span><span class="sxs-lookup"><span data-stu-id="0510c-110">PARAMETERS</span></span>

### <span data-ttu-id="0510c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0510c-111">-DefaultProfile</span></span>
<span data-ttu-id="0510c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0510c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0510c-113">-Local</span><span class="sxs-lookup"><span data-stu-id="0510c-113">-Location</span></span>
<span data-ttu-id="0510c-114">Especifica o nome de uma região do Azure ou o local do Data Center para o qual obter informações sobre a cota da unidade de streaming.</span><span class="sxs-lookup"><span data-stu-id="0510c-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="0510c-115">Consulte http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services para obter uma lista de regiões do Azure com suporte.</span><span class="sxs-lookup"><span data-stu-id="0510c-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="0510c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0510c-116">CommonParameters</span></span>
<span data-ttu-id="0510c-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0510c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0510c-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0510c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0510c-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0510c-119">INPUTS</span></span>

### <span data-ttu-id="0510c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0510c-120">System.String</span></span>

## <span data-ttu-id="0510c-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0510c-121">OUTPUTS</span></span>

### <span data-ttu-id="0510c-122">Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="0510c-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="0510c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0510c-123">NOTES</span></span>

## <span data-ttu-id="0510c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0510c-124">RELATED LINKS</span></span>

[<span data-ttu-id="0510c-125">Cmdlets do Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="0510c-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


