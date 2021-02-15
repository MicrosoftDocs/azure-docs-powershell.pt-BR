---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112468"
---
# <span data-ttu-id="560e6-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="560e6-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="560e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="560e6-102">SYNOPSIS</span></span>
<span data-ttu-id="560e6-103">Obtém informações sobre a cota de Unidade de Streaming para uma região.</span><span class="sxs-lookup"><span data-stu-id="560e6-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="560e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="560e6-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="560e6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="560e6-105">DESCRIPTION</span></span>
<span data-ttu-id="560e6-106">O cmdlet **Get-AzStreamAnalyticsQuota** obtém informações sobre a cota de Unidade de Streaming de uma região.</span><span class="sxs-lookup"><span data-stu-id="560e6-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="560e6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="560e6-107">EXAMPLES</span></span>

### <span data-ttu-id="560e6-108">EXEMPLO 1: Obter informações sobre a cota de Unidade de Streaming de uma região</span><span class="sxs-lookup"><span data-stu-id="560e6-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="560e6-109">Esse comando retorna informações sobre a cota e o uso da Unidade de Streaming na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="560e6-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="560e6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="560e6-110">PARAMETERS</span></span>

### <span data-ttu-id="560e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560e6-111">-DefaultProfile</span></span>
<span data-ttu-id="560e6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="560e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="560e6-113">-Local</span><span class="sxs-lookup"><span data-stu-id="560e6-113">-Location</span></span>
<span data-ttu-id="560e6-114">Especifica o nome de uma região do Azure ou local do data center para o qual obter informações de cota de Unidade de Streaming.</span><span class="sxs-lookup"><span data-stu-id="560e6-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="560e6-115">Confira http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services uma lista de regiões com suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="560e6-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="560e6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560e6-116">CommonParameters</span></span>
<span data-ttu-id="560e6-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560e6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560e6-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560e6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560e6-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="560e6-119">INPUTS</span></span>

### <span data-ttu-id="560e6-120">System.String</span><span class="sxs-lookup"><span data-stu-id="560e6-120">System.String</span></span>

## <span data-ttu-id="560e6-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="560e6-121">OUTPUTS</span></span>

### <span data-ttu-id="560e6-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="560e6-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="560e6-123">Notas</span><span class="sxs-lookup"><span data-stu-id="560e6-123">NOTES</span></span>

## <span data-ttu-id="560e6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="560e6-124">RELATED LINKS</span></span>

[<span data-ttu-id="560e6-125">Azure Stream Analytics Cmdlets</span><span class="sxs-lookup"><span data-stu-id="560e6-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


