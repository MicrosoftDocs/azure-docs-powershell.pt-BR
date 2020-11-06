---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425772"
---
# <span data-ttu-id="ebf24-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="ebf24-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="ebf24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebf24-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf24-103">Criar uma nova delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="ebf24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebf24-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ebf24-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf24-106">Criar uma nova delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="ebf24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebf24-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf24-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ebf24-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="ebf24-109">Criar uma nova delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="ebf24-110">OS</span><span class="sxs-lookup"><span data-stu-id="ebf24-110">PARAMETERS</span></span>

### <span data-ttu-id="ebf24-111">-Local</span><span class="sxs-lookup"><span data-stu-id="ebf24-111">-Location</span></span>
<span data-ttu-id="ebf24-112">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="ebf24-112">Location of the resource.</span></span>

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

### <span data-ttu-id="ebf24-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ebf24-113">-Name</span></span>
<span data-ttu-id="ebf24-114">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-114">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-115">-Offername</span><span class="sxs-lookup"><span data-stu-id="ebf24-115">-OfferName</span></span>
<span data-ttu-id="ebf24-116">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf24-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebf24-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="ebf24-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebf24-119">-SubscriptionId</span></span>
<span data-ttu-id="ebf24-120">Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="ebf24-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ebf24-121">-Confirm</span></span>
<span data-ttu-id="ebf24-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebf24-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf24-123">-WhatIf</span></span>
<span data-ttu-id="ebf24-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebf24-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf24-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebf24-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf24-126">CommonParameters</span></span>
<span data-ttu-id="ebf24-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf24-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf24-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf24-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ebf24-129">INPUTS</span></span>

## <span data-ttu-id="ebf24-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ebf24-130">OUTPUTS</span></span>

### <span data-ttu-id="ebf24-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="ebf24-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="ebf24-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ebf24-132">NOTES</span></span>

## <span data-ttu-id="ebf24-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebf24-133">RELATED LINKS</span></span>
