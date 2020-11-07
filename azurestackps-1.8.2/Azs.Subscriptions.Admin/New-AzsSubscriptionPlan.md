---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946911"
---
# <span data-ttu-id="12e49-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="12e49-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="12e49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12e49-102">SYNOPSIS</span></span>
<span data-ttu-id="12e49-103">Cria um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="12e49-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="12e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e49-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12e49-105">DESCRIPTION</span></span>
<span data-ttu-id="12e49-106">Cria um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="12e49-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="12e49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12e49-107">EXAMPLES</span></span>

### <span data-ttu-id="12e49-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12e49-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="12e49-109">Crie um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="12e49-109">Create an subscription plan.</span></span>

## <span data-ttu-id="12e49-110">OS</span><span class="sxs-lookup"><span data-stu-id="12e49-110">PARAMETERS</span></span>

### <span data-ttu-id="12e49-111">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="12e49-111">-AcquisitionId</span></span>
<span data-ttu-id="12e49-112">Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="12e49-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e49-113">-PlanID</span><span class="sxs-lookup"><span data-stu-id="12e49-113">-PlanId</span></span>
<span data-ttu-id="12e49-114">Identificador do plano no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="12e49-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="12e49-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e49-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="12e49-116">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="12e49-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e49-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12e49-117">-Confirm</span></span>
<span data-ttu-id="12e49-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e49-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e49-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e49-119">-WhatIf</span></span>
<span data-ttu-id="12e49-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12e49-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e49-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12e49-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e49-122">CommonParameters</span></span>
<span data-ttu-id="12e49-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e49-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e49-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e49-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12e49-125">INPUTS</span></span>

## <span data-ttu-id="12e49-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12e49-126">OUTPUTS</span></span>

### <span data-ttu-id="12e49-127">Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="12e49-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="12e49-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12e49-128">NOTES</span></span>

## <span data-ttu-id="12e49-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12e49-129">RELATED LINKS</span></span>

