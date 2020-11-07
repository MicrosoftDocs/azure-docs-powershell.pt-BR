---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774751"
---
# <span data-ttu-id="0d716-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="0d716-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="0d716-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d716-102">SYNOPSIS</span></span>
<span data-ttu-id="0d716-103">Lista de operações com suporte.</span><span class="sxs-lookup"><span data-stu-id="0d716-103">List of supported operations.</span></span>

## <span data-ttu-id="0d716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d716-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d716-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d716-105">DESCRIPTION</span></span>
<span data-ttu-id="0d716-106">Lista de operações com suporte.</span><span class="sxs-lookup"><span data-stu-id="0d716-106">List of supported operations.</span></span>

## <span data-ttu-id="0d716-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d716-107">EXAMPLES</span></span>

### <span data-ttu-id="0d716-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d716-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0d716-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="0d716-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0d716-110">OS</span><span class="sxs-lookup"><span data-stu-id="0d716-110">PARAMETERS</span></span>

### <span data-ttu-id="0d716-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d716-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="0d716-112">Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="0d716-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="0d716-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0d716-113">-DisplayName</span></span>
<span data-ttu-id="0d716-114">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d716-114">Subscription name.</span></span>

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

### <span data-ttu-id="0d716-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0d716-115">-ExternalReferenceId</span></span>
<span data-ttu-id="0d716-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="0d716-116">External reference identifier.</span></span>

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

### <span data-ttu-id="0d716-117">-ID</span><span class="sxs-lookup"><span data-stu-id="0d716-117">-Id</span></span>
<span data-ttu-id="0d716-118">Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="0d716-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="0d716-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d716-119">-Name</span></span>
<span data-ttu-id="0d716-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0d716-120">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d716-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="0d716-121">-OfferId</span></span>
<span data-ttu-id="0d716-122">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="0d716-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="0d716-123">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="0d716-123">-Owner</span></span>
<span data-ttu-id="0d716-124">Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d716-124">Subscription owner.</span></span>

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

### <span data-ttu-id="0d716-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="0d716-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="0d716-126">Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0d716-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="0d716-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="0d716-127">-State</span></span>
<span data-ttu-id="0d716-128">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d716-128">Subscription state.</span></span>

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

### <span data-ttu-id="0d716-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d716-129">-SubscriptionId</span></span>
<span data-ttu-id="0d716-130">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="0d716-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="0d716-131">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="0d716-131">-TenantId</span></span>
<span data-ttu-id="0d716-132">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="0d716-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="0d716-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d716-133">CommonParameters</span></span>
<span data-ttu-id="0d716-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d716-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d716-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d716-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d716-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d716-136">INPUTS</span></span>

## <span data-ttu-id="0d716-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d716-137">OUTPUTS</span></span>

## <span data-ttu-id="0d716-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d716-138">NOTES</span></span>

## <span data-ttu-id="0d716-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d716-139">RELATED LINKS</span></span>

