---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427639"
---
# <span data-ttu-id="7bc62-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7bc62-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="7bc62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bc62-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc62-103">Obtém as SKUs disponíveis para uma conta.</span><span class="sxs-lookup"><span data-stu-id="7bc62-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bc62-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bc62-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc62-106">O cmdlet **Get-AzureRmCognitiveServicesAccountSkus** Obtém os SKUs disponíveis para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="7bc62-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="7bc62-107">A SKU é o plano de camada de uma conta.</span><span class="sxs-lookup"><span data-stu-id="7bc62-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="7bc62-108">Ele define o preço, o limite de chamadas e a taxa da conta.</span><span class="sxs-lookup"><span data-stu-id="7bc62-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="7bc62-109">O SKU de F0 é uma camada gratuita.</span><span class="sxs-lookup"><span data-stu-id="7bc62-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="7bc62-110">Os níveis pagos incluem S0, S1, S2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7bc62-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="7bc62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bc62-111">EXAMPLES</span></span>

## <span data-ttu-id="7bc62-112">OS</span><span class="sxs-lookup"><span data-stu-id="7bc62-112">PARAMETERS</span></span>

### <span data-ttu-id="7bc62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc62-113">-DefaultProfile</span></span>
<span data-ttu-id="7bc62-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7bc62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bc62-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bc62-115">-Name</span></span>
<span data-ttu-id="7bc62-116">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="7bc62-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc62-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bc62-118">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="7bc62-118">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="7bc62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc62-119">CommonParameters</span></span>
<span data-ttu-id="7bc62-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc62-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc62-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc62-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bc62-122">INPUTS</span></span>

### <span data-ttu-id="7bc62-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7bc62-123">None</span></span>
<span data-ttu-id="7bc62-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7bc62-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7bc62-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bc62-125">OUTPUTS</span></span>

### <span data-ttu-id="7bc62-126">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="7bc62-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="7bc62-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bc62-127">NOTES</span></span>

## <span data-ttu-id="7bc62-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bc62-128">RELATED LINKS</span></span>

