---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946694"
---
# <span data-ttu-id="73a05-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="73a05-101">New-OfferObject</span></span>

## <span data-ttu-id="73a05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73a05-102">SYNOPSIS</span></span>
<span data-ttu-id="73a05-103">Representa uma oferta de serviços em que uma assinatura pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="73a05-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="73a05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73a05-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="73a05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73a05-105">DESCRIPTION</span></span>
<span data-ttu-id="73a05-106">Representa uma oferta de serviços em que uma assinatura pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="73a05-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="73a05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73a05-107">EXAMPLES</span></span>

### <span data-ttu-id="73a05-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73a05-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="73a05-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="73a05-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="73a05-110">OS</span><span class="sxs-lookup"><span data-stu-id="73a05-110">PARAMETERS</span></span>

### <span data-ttu-id="73a05-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="73a05-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="73a05-112">Referências a planos de complemento que um locatário pode adquirir opcionalmente como parte da oferta.</span><span class="sxs-lookup"><span data-stu-id="73a05-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="73a05-113">-BasePlanIds</span></span>
<span data-ttu-id="73a05-114">Identificadores dos planos base que se tornam disponíveis para o locatário imediatamente quando um locatário assina a oferta.</span><span class="sxs-lookup"><span data-stu-id="73a05-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="73a05-115">-Description</span></span>
<span data-ttu-id="73a05-116">Descrição da oferta.</span><span class="sxs-lookup"><span data-stu-id="73a05-116">Description of offer.</span></span>

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

### <span data-ttu-id="73a05-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="73a05-117">-DisplayName</span></span>
<span data-ttu-id="73a05-118">Exibir o nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="73a05-118">Display name of offer.</span></span>

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

### <span data-ttu-id="73a05-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="73a05-119">-ExternalReferenceId</span></span>
<span data-ttu-id="73a05-120">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="73a05-120">External reference identifier.</span></span>

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

### <span data-ttu-id="73a05-121">-ID</span><span class="sxs-lookup"><span data-stu-id="73a05-121">-Id</span></span>
<span data-ttu-id="73a05-122">URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="73a05-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-123">-Local</span><span class="sxs-lookup"><span data-stu-id="73a05-123">-Location</span></span>
<span data-ttu-id="73a05-124">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="73a05-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="73a05-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="73a05-126">Máximo de assinaturas por conta.</span><span class="sxs-lookup"><span data-stu-id="73a05-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="73a05-127">-Name</span></span>
<span data-ttu-id="73a05-128">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="73a05-128">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="73a05-129">-State</span></span>
<span data-ttu-id="73a05-130">Oferecer o estado de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="73a05-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="73a05-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="73a05-131">-SubscriptionCount</span></span>
<span data-ttu-id="73a05-132">Contagem de assinaturas atual.</span><span class="sxs-lookup"><span data-stu-id="73a05-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-133">-Marcas</span><span class="sxs-lookup"><span data-stu-id="73a05-133">-Tags</span></span>
<span data-ttu-id="73a05-134">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="73a05-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a05-135">-Digite</span><span class="sxs-lookup"><span data-stu-id="73a05-135">-Type</span></span>
<span data-ttu-id="73a05-136">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="73a05-136">Type of resource.</span></span>

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

### <span data-ttu-id="73a05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a05-137">CommonParameters</span></span>
<span data-ttu-id="73a05-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a05-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a05-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a05-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73a05-140">INPUTS</span></span>

## <span data-ttu-id="73a05-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73a05-141">OUTPUTS</span></span>

## <span data-ttu-id="73a05-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73a05-142">NOTES</span></span>

## <span data-ttu-id="73a05-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73a05-143">RELATED LINKS</span></span>

