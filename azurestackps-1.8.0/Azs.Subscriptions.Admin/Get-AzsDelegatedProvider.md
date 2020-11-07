---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774789"
---
# <span data-ttu-id="a51bf-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="a51bf-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="a51bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a51bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a51bf-103">Obter a lista de delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a51bf-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a51bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a51bf-104">SYNTAX</span></span>

### <span data-ttu-id="a51bf-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="a51bf-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="a51bf-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a51bf-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="a51bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a51bf-107">DESCRIPTION</span></span>
<span data-ttu-id="a51bf-108">Obter a lista de delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="a51bf-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="a51bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a51bf-109">EXAMPLES</span></span>

### <span data-ttu-id="a51bf-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a51bf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="a51bf-111">Obter uma lista de provedores delegados.</span><span class="sxs-lookup"><span data-stu-id="a51bf-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="a51bf-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a51bf-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="a51bf-113">Obter um provedor delegado específico.</span><span class="sxs-lookup"><span data-stu-id="a51bf-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="a51bf-114">OS</span><span class="sxs-lookup"><span data-stu-id="a51bf-114">PARAMETERS</span></span>

### <span data-ttu-id="a51bf-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="a51bf-115">-DelegatedProviderId</span></span>
<span data-ttu-id="a51bf-116">{{Fill DelegatedProviderId descrição}}</span><span class="sxs-lookup"><span data-stu-id="a51bf-116">{{Fill DelegatedProviderId Description}}</span></span>

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

### <span data-ttu-id="a51bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51bf-117">CommonParameters</span></span>
<span data-ttu-id="a51bf-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51bf-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a51bf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51bf-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a51bf-120">INPUTS</span></span>

## <span data-ttu-id="a51bf-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a51bf-121">OUTPUTS</span></span>

### <span data-ttu-id="a51bf-122">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="a51bf-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="a51bf-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a51bf-123">NOTES</span></span>

## <span data-ttu-id="a51bf-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a51bf-124">RELATED LINKS</span></span>
