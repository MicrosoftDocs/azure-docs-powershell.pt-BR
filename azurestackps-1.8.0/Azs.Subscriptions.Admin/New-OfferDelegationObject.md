---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774753"
---
# <span data-ttu-id="df0e7-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="df0e7-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="df0e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="df0e7-103">Oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="df0e7-103">Offer delegation.</span></span>

## <span data-ttu-id="df0e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df0e7-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="df0e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df0e7-105">DESCRIPTION</span></span>
<span data-ttu-id="df0e7-106">Oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="df0e7-106">Offer delegation.</span></span>

## <span data-ttu-id="df0e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df0e7-107">EXAMPLES</span></span>

### <span data-ttu-id="df0e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df0e7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="df0e7-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="df0e7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="df0e7-110">OS</span><span class="sxs-lookup"><span data-stu-id="df0e7-110">PARAMETERS</span></span>

### <span data-ttu-id="df0e7-111">-ID</span><span class="sxs-lookup"><span data-stu-id="df0e7-111">-Id</span></span>
<span data-ttu-id="df0e7-112">URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="df0e7-112">URI of the resource.</span></span>

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

### <span data-ttu-id="df0e7-113">-Local</span><span class="sxs-lookup"><span data-stu-id="df0e7-113">-Location</span></span>
<span data-ttu-id="df0e7-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="df0e7-114">Location of the resource.</span></span>

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

### <span data-ttu-id="df0e7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="df0e7-115">-Name</span></span>
<span data-ttu-id="df0e7-116">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="df0e7-116">Name of the resource.</span></span>

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

### <span data-ttu-id="df0e7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df0e7-117">-SubscriptionId</span></span>
<span data-ttu-id="df0e7-118">Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="df0e7-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="df0e7-119">-Marcas</span><span class="sxs-lookup"><span data-stu-id="df0e7-119">-Tags</span></span>
<span data-ttu-id="df0e7-120">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="df0e7-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df0e7-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="df0e7-121">-Type</span></span>
<span data-ttu-id="df0e7-122">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="df0e7-122">Type of resource.</span></span>

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

### <span data-ttu-id="df0e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0e7-123">CommonParameters</span></span>
<span data-ttu-id="df0e7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0e7-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0e7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0e7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df0e7-126">INPUTS</span></span>

## <span data-ttu-id="df0e7-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df0e7-127">OUTPUTS</span></span>

## <span data-ttu-id="df0e7-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df0e7-128">NOTES</span></span>

## <span data-ttu-id="df0e7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df0e7-129">RELATED LINKS</span></span>

