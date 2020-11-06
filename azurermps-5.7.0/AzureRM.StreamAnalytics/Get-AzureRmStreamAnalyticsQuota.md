---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: de676da4e276cf7e2b49558c81e9d7f6876d158b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431540"
---
# <span data-ttu-id="ac44d-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="ac44d-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="ac44d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac44d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac44d-103">Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="ac44d-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac44d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac44d-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac44d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac44d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac44d-106">O cmdlet **Get-AzureRmStreamAnalyticsQuota** Obtém informações sobre a cota de unidade de streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="ac44d-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="ac44d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac44d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac44d-108">EXEMPLO 1: obter informações sobre a cota de unidade de streaming para uma região</span><span class="sxs-lookup"><span data-stu-id="ac44d-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="ac44d-109">Esse comando retorna informações sobre a cota da unidade de streaming e o uso na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ac44d-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="ac44d-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac44d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac44d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac44d-111">-DefaultProfile</span></span>
<span data-ttu-id="ac44d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac44d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac44d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="ac44d-113">-Location</span></span>
<span data-ttu-id="ac44d-114">Especifica o nome de uma região do Azure ou o local do Data Center para o qual obter informações sobre a cota da unidade de streaming.</span><span class="sxs-lookup"><span data-stu-id="ac44d-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="ac44d-115">Consulte https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services para obter uma lista de regiões do Azure com suporte.</span><span class="sxs-lookup"><span data-stu-id="ac44d-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="ac44d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac44d-116">CommonParameters</span></span>
<span data-ttu-id="ac44d-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac44d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac44d-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac44d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac44d-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac44d-119">INPUTS</span></span>

### <span data-ttu-id="ac44d-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac44d-120">None</span></span>
<span data-ttu-id="ac44d-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ac44d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac44d-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac44d-122">OUTPUTS</span></span>

### <span data-ttu-id="ac44d-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="ac44d-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="ac44d-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac44d-124">NOTES</span></span>

## <span data-ttu-id="ac44d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac44d-125">RELATED LINKS</span></span>

[<span data-ttu-id="ac44d-126">Cmdlets do Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="ac44d-126">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


