---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946810"
---
# <span data-ttu-id="c895b-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="c895b-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="c895b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c895b-102">SYNOPSIS</span></span>
<span data-ttu-id="c895b-103">Exclui um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c895b-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="c895b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c895b-104">SYNTAX</span></span>

### <span data-ttu-id="c895b-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="c895b-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c895b-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c895b-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c895b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c895b-107">DESCRIPTION</span></span>
<span data-ttu-id="c895b-108">Exclui um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c895b-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="c895b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c895b-109">EXAMPLES</span></span>

### <span data-ttu-id="c895b-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c895b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="c895b-111">Excluir um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c895b-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="c895b-112">OS</span><span class="sxs-lookup"><span data-stu-id="c895b-112">PARAMETERS</span></span>

### <span data-ttu-id="c895b-113">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="c895b-113">-AcquisitionId</span></span>
<span data-ttu-id="c895b-114">O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="c895b-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c895b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c895b-115">-Force</span></span>
<span data-ttu-id="c895b-116">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="c895b-116">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c895b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c895b-117">-ResourceId</span></span>
<span data-ttu-id="c895b-118">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c895b-118">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c895b-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c895b-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="c895b-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c895b-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c895b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c895b-121">-Confirm</span></span>
<span data-ttu-id="c895b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c895b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c895b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c895b-123">-WhatIf</span></span>
<span data-ttu-id="c895b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c895b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c895b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c895b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c895b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c895b-126">CommonParameters</span></span>
<span data-ttu-id="c895b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c895b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c895b-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c895b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c895b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c895b-129">INPUTS</span></span>

## <span data-ttu-id="c895b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c895b-130">OUTPUTS</span></span>

## <span data-ttu-id="c895b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c895b-131">NOTES</span></span>

## <span data-ttu-id="c895b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c895b-132">RELATED LINKS</span></span>

