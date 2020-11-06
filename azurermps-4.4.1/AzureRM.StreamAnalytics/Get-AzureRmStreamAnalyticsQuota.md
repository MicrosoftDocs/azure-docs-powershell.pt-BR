---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427735"
---
# <span data-ttu-id="2dad7-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="2dad7-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="2dad7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dad7-102">SYNOPSIS</span></span>
<span data-ttu-id="2dad7-103">Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="2dad7-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dad7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dad7-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dad7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dad7-105">DESCRIPTION</span></span>
<span data-ttu-id="2dad7-106">O cmdlet **Get-AzureRmStreamAnalyticsQuota** Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="2dad7-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="2dad7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dad7-107">EXAMPLES</span></span>

### <span data-ttu-id="2dad7-108">EXEMPLO 1: obter informações sobre a cota de unidade de streaming para uma região</span><span class="sxs-lookup"><span data-stu-id="2dad7-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="2dad7-109">Esse comando retorna informações sobre a cota da unidade de streaming e o uso na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2dad7-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="2dad7-110">OS</span><span class="sxs-lookup"><span data-stu-id="2dad7-110">PARAMETERS</span></span>

### <span data-ttu-id="2dad7-111">-Local</span><span class="sxs-lookup"><span data-stu-id="2dad7-111">-Location</span></span>
<span data-ttu-id="2dad7-112">Especifica o nome de uma região do Azure ou o local do Data Center para o qual obter informações sobre a cota da unidade de streaming.</span><span class="sxs-lookup"><span data-stu-id="2dad7-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="2dad7-113">Consulte https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services para obter uma lista de regiões do Azure com suporte.</span><span class="sxs-lookup"><span data-stu-id="2dad7-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="2dad7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dad7-114">-DefaultProfile</span></span>
<span data-ttu-id="2dad7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dad7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dad7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dad7-116">CommonParameters</span></span>
<span data-ttu-id="2dad7-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dad7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dad7-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dad7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dad7-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dad7-119">INPUTS</span></span>

## <span data-ttu-id="2dad7-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dad7-120">OUTPUTS</span></span>

### <span data-ttu-id="2dad7-121">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="2dad7-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="2dad7-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dad7-122">NOTES</span></span>

## <span data-ttu-id="2dad7-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dad7-123">RELATED LINKS</span></span>

[<span data-ttu-id="2dad7-124">Cmdlets do Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2dad7-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


