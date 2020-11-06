---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427162"
---
# <span data-ttu-id="b79c4-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b79c4-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="b79c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b79c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b79c4-103">Obtém os dados da camada de preços do Azure Security Center para um escopo.</span><span class="sxs-lookup"><span data-stu-id="b79c4-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b79c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b79c4-104">SYNTAX</span></span>

### <span data-ttu-id="b79c4-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="b79c4-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b79c4-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b79c4-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b79c4-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b79c4-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b79c4-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b79c4-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b79c4-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="b79c4-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b79c4-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b79c4-110">DESCRIPTION</span></span>
<span data-ttu-id="b79c4-111">O tipo de preço da central de segurança do Azure é decidido por escopo, com esse cmdlet você pode obter os tipos de preços configurados.</span><span class="sxs-lookup"><span data-stu-id="b79c4-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="b79c4-112">O tipo de preço da assinatura inclui todos os grupos de recursos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="b79c4-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="b79c4-113">O tipo de preço do grupo de recursos substituirá o tipo de preço da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b79c4-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="b79c4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b79c4-114">EXAMPLES</span></span>

### <span data-ttu-id="b79c4-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b79c4-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b79c4-116">Obtém todas as faixas de preços configuradas para a assinatura e os grupos de recursos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="b79c4-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="b79c4-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b79c4-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b79c4-118">Obtém a camada de preços configurada para o recurso de gorup de recursos "myService1".</span><span class="sxs-lookup"><span data-stu-id="b79c4-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="b79c4-119">OS</span><span class="sxs-lookup"><span data-stu-id="b79c4-119">PARAMETERS</span></span>

### <span data-ttu-id="b79c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79c4-120">-DefaultProfile</span></span>
<span data-ttu-id="b79c4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b79c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b79c4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b79c4-122">-Name</span></span>
<span data-ttu-id="b79c4-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b79c4-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b79c4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b79c4-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b79c4-126">-ResourceId</span></span>
<span data-ttu-id="b79c4-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b79c4-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79c4-128">CommonParameters</span></span>
<span data-ttu-id="b79c4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79c4-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79c4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b79c4-131">INPUTS</span></span>

### <span data-ttu-id="b79c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b79c4-132">System.String</span></span>

## <span data-ttu-id="b79c4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b79c4-133">OUTPUTS</span></span>

### <span data-ttu-id="b79c4-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b79c4-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="b79c4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b79c4-135">NOTES</span></span>

## <span data-ttu-id="b79c4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b79c4-136">RELATED LINKS</span></span>
