---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775143"
---
# <span data-ttu-id="cd336-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="cd336-101">New-AzsPlan</span></span>

## <span data-ttu-id="cd336-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd336-102">SYNOPSIS</span></span>
<span data-ttu-id="cd336-103">Cria um novo plano</span><span class="sxs-lookup"><span data-stu-id="cd336-103">Creates a new plan</span></span>

## <span data-ttu-id="cd336-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd336-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd336-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd336-105">DESCRIPTION</span></span>
<span data-ttu-id="cd336-106">Cria um novo plano</span><span class="sxs-lookup"><span data-stu-id="cd336-106">Creates a new plan</span></span>

## <span data-ttu-id="cd336-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd336-107">EXAMPLES</span></span>

### <span data-ttu-id="cd336-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd336-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="cd336-109">Cria um novo plano</span><span class="sxs-lookup"><span data-stu-id="cd336-109">Creates a new plan</span></span>

## <span data-ttu-id="cd336-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd336-110">PARAMETERS</span></span>

### <span data-ttu-id="cd336-111">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cd336-111">-Description</span></span>
<span data-ttu-id="cd336-112">Descrição do plano.</span><span class="sxs-lookup"><span data-stu-id="cd336-112">Description of the plan.</span></span>

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

### <span data-ttu-id="cd336-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd336-113">-DisplayName</span></span>
<span data-ttu-id="cd336-114">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="cd336-114">Display name.</span></span>

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

### <span data-ttu-id="cd336-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="cd336-115">-ExternalReferenceId</span></span>
<span data-ttu-id="cd336-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="cd336-116">External reference identifier.</span></span>

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

### <span data-ttu-id="cd336-117">-Local</span><span class="sxs-lookup"><span data-stu-id="cd336-117">-Location</span></span>
<span data-ttu-id="cd336-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd336-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd336-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd336-119">-Name</span></span>
<span data-ttu-id="cd336-120">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="cd336-120">Name of the plan.</span></span>

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

### <span data-ttu-id="cd336-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="cd336-121">-QuotaIds</span></span>
<span data-ttu-id="cd336-122">Identificadores de cota sob o plano.</span><span class="sxs-lookup"><span data-stu-id="cd336-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd336-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd336-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd336-124">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="cd336-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="cd336-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="cd336-125">-SkuIds</span></span>
<span data-ttu-id="cd336-126">Identificadores de SKU.</span><span class="sxs-lookup"><span data-stu-id="cd336-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd336-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="cd336-127">-SubscriptionCount</span></span>
<span data-ttu-id="cd336-128">Contagem de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="cd336-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd336-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd336-129">-Confirm</span></span>
<span data-ttu-id="cd336-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd336-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd336-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd336-131">-WhatIf</span></span>
<span data-ttu-id="cd336-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd336-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd336-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd336-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd336-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd336-134">CommonParameters</span></span>
<span data-ttu-id="cd336-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd336-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd336-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd336-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd336-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd336-137">INPUTS</span></span>

## <span data-ttu-id="cd336-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd336-138">OUTPUTS</span></span>

### <span data-ttu-id="cd336-139">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="cd336-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="cd336-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd336-140">NOTES</span></span>

## <span data-ttu-id="cd336-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd336-141">RELATED LINKS</span></span>

