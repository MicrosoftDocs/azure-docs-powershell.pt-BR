---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889039"
---
# <span data-ttu-id="f45ef-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="f45ef-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="f45ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f45ef-103">Obtém os SKUs disponíveis para uma conta.</span><span class="sxs-lookup"><span data-stu-id="f45ef-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="f45ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f45ef-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45ef-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f45ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f45ef-106">O cmdlet **Get-AzCognitiveServicesAccountSku** obtém as SKUs disponíveis para uma conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="f45ef-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="f45ef-107">O SKU é o plano de camadas de uma conta.</span><span class="sxs-lookup"><span data-stu-id="f45ef-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="f45ef-108">Ele define o preço, o limite de chamada e a taxa da conta.</span><span class="sxs-lookup"><span data-stu-id="f45ef-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="f45ef-109">O SKU F0 é uma camada livre.</span><span class="sxs-lookup"><span data-stu-id="f45ef-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="f45ef-110">As camadas pagas incluem S0, S1, S2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f45ef-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="f45ef-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f45ef-111">EXAMPLES</span></span>

### <span data-ttu-id="f45ef-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f45ef-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="f45ef-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f45ef-113">PARAMETERS</span></span>

### <span data-ttu-id="f45ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45ef-114">-DefaultProfile</span></span>
<span data-ttu-id="f45ef-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f45ef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f45ef-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f45ef-116">-Location</span></span>
<span data-ttu-id="f45ef-117">Local da conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="f45ef-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45ef-118">-Type</span><span class="sxs-lookup"><span data-stu-id="f45ef-118">-Type</span></span>
<span data-ttu-id="f45ef-119">Tipo de conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="f45ef-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45ef-120">CommonParameters</span></span>
<span data-ttu-id="f45ef-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f45ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45ef-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f45ef-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45ef-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f45ef-123">INPUTS</span></span>

### <span data-ttu-id="f45ef-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f45ef-124">System.String</span></span>

## <span data-ttu-id="f45ef-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f45ef-125">OUTPUTS</span></span>

### <span data-ttu-id="f45ef-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="f45ef-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="f45ef-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="f45ef-127">NOTES</span></span>

## <span data-ttu-id="f45ef-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f45ef-128">RELATED LINKS</span></span>
