---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947164"
---
# <span data-ttu-id="cd4d0-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="cd4d0-101">New-PlanObject</span></span>

## <span data-ttu-id="cd4d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4d0-103">Um plano representa um pacote de cotas e recursos que são locatários oferecidos.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="cd4d0-104">Um locatário pode adquirir esse plano por meio de uma oferta para atualizar o acesso aos serviços de nuvem subjacentes.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="cd4d0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd4d0-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="cd4d0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd4d0-106">DESCRIPTION</span></span>
<span data-ttu-id="cd4d0-107">Um plano representa um pacote de cotas e recursos que são locatários oferecidos.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="cd4d0-108">Um locatário pode adquirir esse plano por meio de uma oferta para atualizar o acesso aos serviços de nuvem subjacentes.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="cd4d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd4d0-109">EXAMPLES</span></span>

### <span data-ttu-id="cd4d0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd4d0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cd4d0-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="cd4d0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="cd4d0-112">OS</span><span class="sxs-lookup"><span data-stu-id="cd4d0-112">PARAMETERS</span></span>

### <span data-ttu-id="cd4d0-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cd4d0-113">-Description</span></span>
<span data-ttu-id="cd4d0-114">Descrição do plano.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd4d0-115">-DisplayName</span></span>
<span data-ttu-id="cd4d0-116">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="cd4d0-117">-ExternalReferenceId</span></span>
<span data-ttu-id="cd4d0-118">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-118">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="cd4d0-119">-Id</span></span>
<span data-ttu-id="cd4d0-120">URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-121">-Local</span><span class="sxs-lookup"><span data-stu-id="cd4d0-121">-Location</span></span>
<span data-ttu-id="cd4d0-122">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd4d0-123">-Name</span></span>
<span data-ttu-id="cd4d0-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="cd4d0-125">-QuotaIds</span></span>
<span data-ttu-id="cd4d0-126">Identificadores de cota sob o plano.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="cd4d0-127">-SkuIds</span></span>
<span data-ttu-id="cd4d0-128">Identificadores de SKU.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="cd4d0-129">-SubscriptionCount</span></span>
<span data-ttu-id="cd4d0-130">Contagem de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-131">-Marcas</span><span class="sxs-lookup"><span data-stu-id="cd4d0-131">-Tags</span></span>
<span data-ttu-id="cd4d0-132">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-133">-Digite</span><span class="sxs-lookup"><span data-stu-id="cd4d0-133">-Type</span></span>
<span data-ttu-id="cd4d0-134">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-134">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4d0-135">CommonParameters</span></span>
<span data-ttu-id="cd4d0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4d0-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4d0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4d0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd4d0-138">INPUTS</span></span>

## <span data-ttu-id="cd4d0-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd4d0-139">OUTPUTS</span></span>

## <span data-ttu-id="cd4d0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd4d0-140">NOTES</span></span>

## <span data-ttu-id="cd4d0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd4d0-141">RELATED LINKS</span></span>

