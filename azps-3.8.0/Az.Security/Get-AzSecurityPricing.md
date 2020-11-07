---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 176ef6d90fed93a65da10a1f1174f2b81f1fe094
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941596"
---
# <span data-ttu-id="ceb46-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ceb46-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="ceb46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceb46-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb46-103">Obtém os dados da camada de preços do Azure Security Center para um escopo.</span><span class="sxs-lookup"><span data-stu-id="ceb46-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="ceb46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceb46-104">SYNTAX</span></span>

### <span data-ttu-id="ceb46-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="ceb46-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceb46-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ceb46-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceb46-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="ceb46-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb46-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceb46-108">DESCRIPTION</span></span>
<span data-ttu-id="ceb46-109">O tipo de preço da central de segurança do Azure é decidido por escopo, com esse cmdlet você pode obter os tipos de preços configurados.</span><span class="sxs-lookup"><span data-stu-id="ceb46-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="ceb46-110">O tipo de preço da assinatura inclui todos os grupos de recursos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="ceb46-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="ceb46-111">O tipo de preço do grupo de recursos substituirá o tipo de preço da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ceb46-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="ceb46-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceb46-112">EXAMPLES</span></span>

### <span data-ttu-id="ceb46-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ceb46-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="ceb46-114">Obtém todas as faixas de preços configuradas para a assinatura e os grupos de recursos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="ceb46-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="ceb46-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ceb46-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="ceb46-116">Obtém a camada de preços configurada para o grupo de recursos "myService1".</span><span class="sxs-lookup"><span data-stu-id="ceb46-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="ceb46-117">OS</span><span class="sxs-lookup"><span data-stu-id="ceb46-117">PARAMETERS</span></span>

### <span data-ttu-id="ceb46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb46-118">-DefaultProfile</span></span>
<span data-ttu-id="ceb46-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb46-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceb46-120">-Name</span></span>
<span data-ttu-id="ceb46-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ceb46-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb46-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceb46-122">-ResourceId</span></span>
<span data-ttu-id="ceb46-123">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ceb46-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb46-124">CommonParameters</span></span>
<span data-ttu-id="ceb46-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb46-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb46-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb46-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceb46-127">INPUTS</span></span>

### <span data-ttu-id="ceb46-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ceb46-128">System.String</span></span>

## <span data-ttu-id="ceb46-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceb46-129">OUTPUTS</span></span>

### <span data-ttu-id="ceb46-130">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ceb46-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="ceb46-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceb46-131">NOTES</span></span>

## <span data-ttu-id="ceb46-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceb46-132">RELATED LINKS</span></span>
