---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 30c90d4b04c6c32144946cbdf98c59991133dbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901554"
---
# <span data-ttu-id="423ed-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="423ed-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="423ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="423ed-102">SYNOPSIS</span></span>
<span data-ttu-id="423ed-103">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="423ed-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="423ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="423ed-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="423ed-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="423ed-105">DESCRIPTION</span></span>
<span data-ttu-id="423ed-106">O cmdlet **New-AzSubscriptionAlias** cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="423ed-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="423ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="423ed-107">EXAMPLES</span></span>

### <span data-ttu-id="423ed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="423ed-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="423ed-109">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="423ed-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="423ed-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="423ed-110">PARAMETERS</span></span>

### <span data-ttu-id="423ed-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="423ed-111">-AliasName</span></span>
<span data-ttu-id="423ed-112">Alias para a assinatura</span><span class="sxs-lookup"><span data-stu-id="423ed-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="423ed-113">-AsJob</span></span>
<span data-ttu-id="423ed-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="423ed-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="423ed-115">-BillingScope</span></span>
<span data-ttu-id="423ed-116">Escopo de cobrança</span><span class="sxs-lookup"><span data-stu-id="423ed-116">Billing Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423ed-117">-DefaultProfile</span></span>
<span data-ttu-id="423ed-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="423ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="423ed-119">-ResellerId</span></span>
<span data-ttu-id="423ed-120">ID do revendedor</span><span class="sxs-lookup"><span data-stu-id="423ed-120">Reseller Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="423ed-121">-SubscriptionId</span></span>
<span data-ttu-id="423ed-122">ID de assinatura existente</span><span class="sxs-lookup"><span data-stu-id="423ed-122">Existing Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="423ed-123">-SubscriptionName</span></span>
<span data-ttu-id="423ed-124">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="423ed-124">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="423ed-125">-Workload</span></span>
<span data-ttu-id="423ed-126">Tipo de carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="423ed-126">Type of Workload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="423ed-127">-Confirm</span></span>
<span data-ttu-id="423ed-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="423ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="423ed-129">-WhatIf</span></span>
<span data-ttu-id="423ed-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="423ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="423ed-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="423ed-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423ed-132">CommonParameters</span></span>
<span data-ttu-id="423ed-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423ed-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="423ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423ed-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="423ed-135">INPUTS</span></span>

### <span data-ttu-id="423ed-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="423ed-136">None</span></span>

## <span data-ttu-id="423ed-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="423ed-137">OUTPUTS</span></span>

### <span data-ttu-id="423ed-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="423ed-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="423ed-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="423ed-139">NOTES</span></span>

## <span data-ttu-id="423ed-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="423ed-140">RELATED LINKS</span></span>
