---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432857"
---
# <span data-ttu-id="a579d-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a579d-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="a579d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a579d-102">SYNOPSIS</span></span>
<span data-ttu-id="a579d-103">Cria uma definição de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a579d-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a579d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a579d-104">SYNTAX</span></span>

### <span data-ttu-id="a579d-105">Criar definição de assinatura</span><span class="sxs-lookup"><span data-stu-id="a579d-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="a579d-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a579d-106">DESCRIPTION</span></span>
<span data-ttu-id="a579d-107">O cmdlet **New-AzureRmSubscriptionDefinition** cria uma definição de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a579d-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="a579d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a579d-108">EXAMPLES</span></span>

### <span data-ttu-id="a579d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a579d-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="a579d-110">Cria uma definição de assinatura com um nome de exibição de assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="a579d-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="a579d-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a579d-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="a579d-112">Cria uma definição de assinatura com um nome de exibição de assinatura personalizado.</span><span class="sxs-lookup"><span data-stu-id="a579d-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="a579d-113">OS</span><span class="sxs-lookup"><span data-stu-id="a579d-113">PARAMETERS</span></span>

### <span data-ttu-id="a579d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a579d-114">-Name</span></span>
<span data-ttu-id="a579d-115">O nome da definição de assinatura a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a579d-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579d-116">-Offertype</span><span class="sxs-lookup"><span data-stu-id="a579d-116">-OfferType</span></span>
<span data-ttu-id="a579d-117">O tipo de oferta a ser usado ao criar a assinatura subjacente.</span><span class="sxs-lookup"><span data-stu-id="a579d-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579d-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="a579d-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="a579d-119">O nome de exibição a ser usado ao criar a assinatura subjacente da definição de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a579d-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a579d-120">CommonParameters</span></span>
<span data-ttu-id="a579d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a579d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a579d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a579d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a579d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a579d-123">INPUTS</span></span>

### <span data-ttu-id="a579d-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a579d-124">None</span></span>

## <span data-ttu-id="a579d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a579d-125">OUTPUTS</span></span>

### <span data-ttu-id="a579d-126">Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a579d-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="a579d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a579d-127">NOTES</span></span>

## <span data-ttu-id="a579d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a579d-128">RELATED LINKS</span></span>

