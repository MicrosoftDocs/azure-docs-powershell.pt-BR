---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426042"
---
# <span data-ttu-id="12cb3-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="12cb3-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="12cb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="12cb3-103">Obter a lista de delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="12cb3-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="12cb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12cb3-104">SYNTAX</span></span>

### <span data-ttu-id="12cb3-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="12cb3-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="12cb3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="12cb3-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="12cb3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12cb3-107">DESCRIPTION</span></span>
<span data-ttu-id="12cb3-108">Obter a lista de delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="12cb3-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="12cb3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12cb3-109">EXAMPLES</span></span>

### <span data-ttu-id="12cb3-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12cb3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="12cb3-111">Obter uma lista de provedores delegados.</span><span class="sxs-lookup"><span data-stu-id="12cb3-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="12cb3-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="12cb3-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="12cb3-113">Obter um provedor delegado específico.</span><span class="sxs-lookup"><span data-stu-id="12cb3-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="12cb3-114">OS</span><span class="sxs-lookup"><span data-stu-id="12cb3-114">PARAMETERS</span></span>

### <span data-ttu-id="12cb3-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="12cb3-115">-DelegatedProviderId</span></span>
<span data-ttu-id="12cb3-116">Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="12cb3-116">DelegatedProvider identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cb3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cb3-117">CommonParameters</span></span>
<span data-ttu-id="12cb3-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12cb3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cb3-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cb3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cb3-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12cb3-120">INPUTS</span></span>

## <span data-ttu-id="12cb3-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12cb3-121">OUTPUTS</span></span>

### <span data-ttu-id="12cb3-122">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="12cb3-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="12cb3-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12cb3-123">NOTES</span></span>

## <span data-ttu-id="12cb3-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12cb3-124">RELATED LINKS</span></span>

