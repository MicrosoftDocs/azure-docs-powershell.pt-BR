---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774248"
---
# <span data-ttu-id="ad006-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="ad006-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="ad006-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad006-102">SYNOPSIS</span></span>
<span data-ttu-id="ad006-103">Obtenha a lista de cotas do provedor de recursos de assinatura em um local.</span><span class="sxs-lookup"><span data-stu-id="ad006-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="ad006-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad006-104">SYNTAX</span></span>

### <span data-ttu-id="ad006-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ad006-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad006-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ad006-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad006-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="ad006-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad006-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad006-108">DESCRIPTION</span></span>
<span data-ttu-id="ad006-109">Obter a lista de cotas em um local.</span><span class="sxs-lookup"><span data-stu-id="ad006-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="ad006-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad006-110">EXAMPLES</span></span>

### <span data-ttu-id="ad006-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad006-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="ad006-112">Obtenha a lista de cotas do provedor de recursos de assinatura em um local.</span><span class="sxs-lookup"><span data-stu-id="ad006-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="ad006-113">OS</span><span class="sxs-lookup"><span data-stu-id="ad006-113">PARAMETERS</span></span>

### <span data-ttu-id="ad006-114">-Local</span><span class="sxs-lookup"><span data-stu-id="ad006-114">-Location</span></span>
<span data-ttu-id="ad006-115">O local do AzureStack.</span><span class="sxs-lookup"><span data-stu-id="ad006-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad006-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad006-116">-Name</span></span>
<span data-ttu-id="ad006-117">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="ad006-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad006-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad006-118">-ResourceId</span></span>
<span data-ttu-id="ad006-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ad006-119">The resource id.</span></span>

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

### <span data-ttu-id="ad006-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad006-120">CommonParameters</span></span>
<span data-ttu-id="ad006-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad006-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad006-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad006-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad006-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad006-123">INPUTS</span></span>

## <span data-ttu-id="ad006-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad006-124">OUTPUTS</span></span>

### <span data-ttu-id="ad006-125">Microsoft. AzureStack. Management. subscriptions. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="ad006-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="ad006-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad006-126">NOTES</span></span>

## <span data-ttu-id="ad006-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad006-127">RELATED LINKS</span></span>

