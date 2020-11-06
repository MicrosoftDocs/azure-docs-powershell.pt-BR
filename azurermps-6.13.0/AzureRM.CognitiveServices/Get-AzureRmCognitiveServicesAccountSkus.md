---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432327"
---
# <span data-ttu-id="b889a-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b889a-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="b889a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b889a-102">SYNOPSIS</span></span>
<span data-ttu-id="b889a-103">Obtém as SKUs disponíveis para uma conta.</span><span class="sxs-lookup"><span data-stu-id="b889a-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b889a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b889a-104">SYNTAX</span></span>

### <span data-ttu-id="b889a-105">GetSkusWithAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="b889a-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b889a-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="b889a-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b889a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b889a-107">DESCRIPTION</span></span>
<span data-ttu-id="b889a-108">O cmdlet **Get-AzureRmCognitiveServicesAccountSkus** Obtém os SKUs disponíveis para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="b889a-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="b889a-109">A SKU é o plano de camada de uma conta.</span><span class="sxs-lookup"><span data-stu-id="b889a-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="b889a-110">Ele define o preço, o limite de chamadas e a taxa da conta.</span><span class="sxs-lookup"><span data-stu-id="b889a-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="b889a-111">O SKU de F0 é uma camada gratuita.</span><span class="sxs-lookup"><span data-stu-id="b889a-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="b889a-112">Os níveis pagos incluem S0, S1, S2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b889a-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="b889a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b889a-113">EXAMPLES</span></span>

### <span data-ttu-id="b889a-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b889a-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="b889a-115">OS</span><span class="sxs-lookup"><span data-stu-id="b889a-115">PARAMETERS</span></span>

### <span data-ttu-id="b889a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b889a-116">-DefaultProfile</span></span>
<span data-ttu-id="b889a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b889a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b889a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b889a-118">-Location</span></span>
<span data-ttu-id="b889a-119">Localização da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="b889a-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b889a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b889a-120">-Name</span></span>
<span data-ttu-id="b889a-121">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="b889a-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b889a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b889a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b889a-123">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="b889a-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b889a-124">-Digite</span><span class="sxs-lookup"><span data-stu-id="b889a-124">-Type</span></span>
<span data-ttu-id="b889a-125">Tipo de conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="b889a-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b889a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b889a-126">CommonParameters</span></span>
<span data-ttu-id="b889a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b889a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b889a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b889a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b889a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b889a-129">INPUTS</span></span>

### <span data-ttu-id="b889a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b889a-130">System.String</span></span>

## <span data-ttu-id="b889a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b889a-131">OUTPUTS</span></span>

### <span data-ttu-id="b889a-132">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="b889a-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="b889a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b889a-133">NOTES</span></span>

## <span data-ttu-id="b889a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b889a-134">RELATED LINKS</span></span>
