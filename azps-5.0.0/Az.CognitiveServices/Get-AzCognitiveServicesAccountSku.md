---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117633"
---
# <span data-ttu-id="ad6ec-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="ad6ec-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="ad6ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6ec-103">Obtém as SKUs disponíveis para uma conta.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="ad6ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad6ec-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6ec-106">O cmdlet **Get-AzCognitiveServicesAccountSku** Obtém os SKUs disponíveis para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="ad6ec-107">A SKU é o plano de camada de uma conta.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="ad6ec-108">Ele define o preço, o limite de chamadas e a taxa da conta.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="ad6ec-109">O SKU de F0 é uma camada gratuita.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="ad6ec-110">Os níveis pagos incluem S0, S1, S2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="ad6ec-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad6ec-111">EXAMPLES</span></span>

### <span data-ttu-id="ad6ec-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ad6ec-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="ad6ec-113">OS</span><span class="sxs-lookup"><span data-stu-id="ad6ec-113">PARAMETERS</span></span>

### <span data-ttu-id="ad6ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6ec-114">-DefaultProfile</span></span>
<span data-ttu-id="ad6ec-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ad6ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6ec-116">-Local</span><span class="sxs-lookup"><span data-stu-id="ad6ec-116">-Location</span></span>
<span data-ttu-id="ad6ec-117">Localização da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="ad6ec-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="ad6ec-118">-Type</span></span>
<span data-ttu-id="ad6ec-119">Tipo de conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="ad6ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6ec-120">CommonParameters</span></span>
<span data-ttu-id="ad6ec-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6ec-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad6ec-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6ec-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad6ec-123">INPUTS</span></span>

### <span data-ttu-id="ad6ec-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ad6ec-124">System.String</span></span>

## <span data-ttu-id="ad6ec-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad6ec-125">OUTPUTS</span></span>

### <span data-ttu-id="ad6ec-126">Microsoft. Azure. Management. Cognitivaservices. Models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="ad6ec-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="ad6ec-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad6ec-127">NOTES</span></span>

## <span data-ttu-id="ad6ec-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad6ec-128">RELATED LINKS</span></span>
