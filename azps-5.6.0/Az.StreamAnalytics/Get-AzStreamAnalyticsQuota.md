---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: 8583227cee19a9429a7dfe4cd6bd8678e72d33ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888117"
---
# <span data-ttu-id="07d1e-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="07d1e-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="07d1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="07d1e-103">Obtém informações sobre a cota de Unidade de Streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="07d1e-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="07d1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07d1e-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="07d1e-106">O cmdlet **Get-AzStreamAnalyticsQuota** obtém informações sobre a cota de Unidade de Streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="07d1e-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="07d1e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="07d1e-108">EXEMPLO 1: Obter informações sobre a cota de Unidade de Streaming para uma região</span><span class="sxs-lookup"><span data-stu-id="07d1e-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="07d1e-109">Este comando retorna informações sobre a cota e o uso da Unidade de Streaming na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="07d1e-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="07d1e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07d1e-110">PARAMETERS</span></span>

### <span data-ttu-id="07d1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d1e-111">-DefaultProfile</span></span>
<span data-ttu-id="07d1e-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="07d1e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d1e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="07d1e-113">-Location</span></span>
<span data-ttu-id="07d1e-114">Especifica o nome de uma região do Azure ou local do data center para o qual obter informações de cota da Unidade de Streaming.</span><span class="sxs-lookup"><span data-stu-id="07d1e-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="07d1e-115">Consulte http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services uma lista de regiões com suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="07d1e-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="07d1e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d1e-116">CommonParameters</span></span>
<span data-ttu-id="07d1e-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d1e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d1e-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d1e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d1e-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07d1e-119">INPUTS</span></span>

### <span data-ttu-id="07d1e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="07d1e-120">System.String</span></span>

## <span data-ttu-id="07d1e-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07d1e-121">OUTPUTS</span></span>

### <span data-ttu-id="07d1e-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="07d1e-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="07d1e-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="07d1e-123">NOTES</span></span>

## <span data-ttu-id="07d1e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07d1e-124">RELATED LINKS</span></span>

[<span data-ttu-id="07d1e-125">Azure Stream Analytics Cmdlets</span><span class="sxs-lookup"><span data-stu-id="07d1e-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


