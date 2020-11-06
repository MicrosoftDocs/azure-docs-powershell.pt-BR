---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601797"
---
# <span data-ttu-id="064ee-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="064ee-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="064ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="064ee-102">SYNOPSIS</span></span>
<span data-ttu-id="064ee-103">Obtenha a lista de assinaturas de usuários como operadora.</span><span class="sxs-lookup"><span data-stu-id="064ee-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="064ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="064ee-104">SYNTAX</span></span>

### <span data-ttu-id="064ee-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="064ee-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="064ee-106">Obter</span><span class="sxs-lookup"><span data-stu-id="064ee-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="064ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="064ee-107">DESCRIPTION</span></span>
<span data-ttu-id="064ee-108">Obtenha a lista de assinaturas de usuários como operadora.</span><span class="sxs-lookup"><span data-stu-id="064ee-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="064ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="064ee-109">EXAMPLES</span></span>

### <span data-ttu-id="064ee-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="064ee-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="064ee-111">Obtenha a lista de assinaturas de usuários como operadora.</span><span class="sxs-lookup"><span data-stu-id="064ee-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="064ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="064ee-112">PARAMETERS</span></span>

### <span data-ttu-id="064ee-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="064ee-113">-Filter</span></span>
<span data-ttu-id="064ee-114">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="064ee-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064ee-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="064ee-115">-SubscriptionId</span></span>
<span data-ttu-id="064ee-116">Parâmetro ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="064ee-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064ee-117">CommonParameters</span></span>
<span data-ttu-id="064ee-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064ee-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="064ee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064ee-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="064ee-120">INPUTS</span></span>

## <span data-ttu-id="064ee-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="064ee-121">OUTPUTS</span></span>

### <span data-ttu-id="064ee-122">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="064ee-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="064ee-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="064ee-123">NOTES</span></span>

## <span data-ttu-id="064ee-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="064ee-124">RELATED LINKS</span></span>

