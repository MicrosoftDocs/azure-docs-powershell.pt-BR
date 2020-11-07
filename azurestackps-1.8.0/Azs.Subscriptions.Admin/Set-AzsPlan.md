---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774740"
---
# <span data-ttu-id="09264-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="09264-101">Set-AzsPlan</span></span>

## <span data-ttu-id="09264-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09264-102">SYNOPSIS</span></span>
<span data-ttu-id="09264-103">Atualiza o plano especificado</span><span class="sxs-lookup"><span data-stu-id="09264-103">Updates the specified plan</span></span>

## <span data-ttu-id="09264-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09264-104">SYNTAX</span></span>

### <span data-ttu-id="09264-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="09264-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09264-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="09264-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09264-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="09264-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09264-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09264-108">DESCRIPTION</span></span>
<span data-ttu-id="09264-109">Atualiza o plano especificado</span><span class="sxs-lookup"><span data-stu-id="09264-109">Updates the specified plan</span></span>

## <span data-ttu-id="09264-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09264-110">EXAMPLES</span></span>

### <span data-ttu-id="09264-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="09264-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="09264-112">Atualiza o plano especificado</span><span class="sxs-lookup"><span data-stu-id="09264-112">Updates the specified plan</span></span>

## <span data-ttu-id="09264-113">OS</span><span class="sxs-lookup"><span data-stu-id="09264-113">PARAMETERS</span></span>

### <span data-ttu-id="09264-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="09264-114">-Description</span></span>
<span data-ttu-id="09264-115">Descrição do plano.</span><span class="sxs-lookup"><span data-stu-id="09264-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09264-116">-DisplayName</span></span>
<span data-ttu-id="09264-117">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="09264-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="09264-118">-ExternalReferenceId</span></span>
<span data-ttu-id="09264-119">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="09264-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09264-120">-InputObject</span></span>
<span data-ttu-id="09264-121">O objeto de entrada do tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="09264-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09264-122">-Local</span><span class="sxs-lookup"><span data-stu-id="09264-122">-Location</span></span>
<span data-ttu-id="09264-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="09264-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="09264-124">-Name</span></span>
<span data-ttu-id="09264-125">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="09264-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="09264-126">-QuotaIds</span></span>
<span data-ttu-id="09264-127">Identificadores de cota sob o plano.</span><span class="sxs-lookup"><span data-stu-id="09264-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09264-128">-ResourceGroupName</span></span>
<span data-ttu-id="09264-129">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="09264-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09264-130">-ResourceId</span></span>
<span data-ttu-id="09264-131">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="09264-131">The resource id.</span></span>

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

### <span data-ttu-id="09264-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="09264-132">-SkuIds</span></span>
<span data-ttu-id="09264-133">Identificadores de SKU.</span><span class="sxs-lookup"><span data-stu-id="09264-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="09264-134">-SubscriptionCount</span></span>
<span data-ttu-id="09264-135">Contagem de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="09264-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09264-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09264-136">-Confirm</span></span>
<span data-ttu-id="09264-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09264-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09264-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09264-138">-WhatIf</span></span>
<span data-ttu-id="09264-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09264-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09264-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09264-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09264-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09264-141">CommonParameters</span></span>
<span data-ttu-id="09264-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09264-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09264-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09264-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09264-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09264-144">INPUTS</span></span>

## <span data-ttu-id="09264-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09264-145">OUTPUTS</span></span>

### <span data-ttu-id="09264-146">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="09264-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="09264-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09264-147">NOTES</span></span>

## <span data-ttu-id="09264-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09264-148">RELATED LINKS</span></span>

