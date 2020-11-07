---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774769"
---
# <span data-ttu-id="32f88-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="32f88-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="32f88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32f88-102">SYNOPSIS</span></span>
<span data-ttu-id="32f88-103">Obter a lista de assinaturas de usuários como administrador.</span><span class="sxs-lookup"><span data-stu-id="32f88-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="32f88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32f88-104">SYNTAX</span></span>

### <span data-ttu-id="32f88-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="32f88-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="32f88-106">Obter</span><span class="sxs-lookup"><span data-stu-id="32f88-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="32f88-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32f88-107">DESCRIPTION</span></span>
<span data-ttu-id="32f88-108">Obter a lista de assinaturas de usuários como administrador.</span><span class="sxs-lookup"><span data-stu-id="32f88-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="32f88-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32f88-109">EXAMPLES</span></span>

### <span data-ttu-id="32f88-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="32f88-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="32f88-111">Obter a lista de assinaturas de usuários como administrador.</span><span class="sxs-lookup"><span data-stu-id="32f88-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="32f88-112">OS</span><span class="sxs-lookup"><span data-stu-id="32f88-112">PARAMETERS</span></span>

### <span data-ttu-id="32f88-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="32f88-113">-Filter</span></span>
<span data-ttu-id="32f88-114">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="32f88-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="32f88-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32f88-115">-SubscriptionId</span></span>
<span data-ttu-id="32f88-116">Parâmetro ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="32f88-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="32f88-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f88-117">CommonParameters</span></span>
<span data-ttu-id="32f88-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f88-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f88-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f88-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f88-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32f88-120">INPUTS</span></span>

## <span data-ttu-id="32f88-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32f88-121">OUTPUTS</span></span>

### <span data-ttu-id="32f88-122">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="32f88-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="32f88-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32f88-123">NOTES</span></span>

## <span data-ttu-id="32f88-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32f88-124">RELATED LINKS</span></span>

