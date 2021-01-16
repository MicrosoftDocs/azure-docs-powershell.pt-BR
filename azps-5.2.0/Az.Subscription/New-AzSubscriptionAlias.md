---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263760"
---
# <span data-ttu-id="94703-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="94703-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="94703-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94703-102">SYNOPSIS</span></span>
<span data-ttu-id="94703-103">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="94703-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="94703-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94703-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94703-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94703-105">DESCRIPTION</span></span>
<span data-ttu-id="94703-106">O cmdlet **New-AzSubscriptionAlias** cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="94703-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="94703-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94703-107">EXAMPLES</span></span>

### <span data-ttu-id="94703-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94703-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="94703-109">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="94703-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="94703-110">OS</span><span class="sxs-lookup"><span data-stu-id="94703-110">PARAMETERS</span></span>

### <span data-ttu-id="94703-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="94703-111">-AliasName</span></span>
<span data-ttu-id="94703-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="94703-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="94703-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94703-113">-AsJob</span></span>
<span data-ttu-id="94703-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="94703-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94703-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="94703-115">-BillingScope</span></span>
<span data-ttu-id="94703-116">Escopo de cobrança</span><span class="sxs-lookup"><span data-stu-id="94703-116">Billing Scope</span></span>

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

### <span data-ttu-id="94703-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94703-117">-DefaultProfile</span></span>
<span data-ttu-id="94703-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94703-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94703-119">-Revendedora</span><span class="sxs-lookup"><span data-stu-id="94703-119">-ResellerId</span></span>
<span data-ttu-id="94703-120">ID do revendedor</span><span class="sxs-lookup"><span data-stu-id="94703-120">Reseller Id</span></span>

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

### <span data-ttu-id="94703-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94703-121">-SubscriptionId</span></span>
<span data-ttu-id="94703-122">ID de assinatura existente</span><span class="sxs-lookup"><span data-stu-id="94703-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="94703-123">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="94703-123">-SubscriptionName</span></span>
<span data-ttu-id="94703-124">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="94703-124">Name of the subscription</span></span>

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

### <span data-ttu-id="94703-125">-Carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="94703-125">-Workload</span></span>
<span data-ttu-id="94703-126">Tipo de carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="94703-126">Type of Workload</span></span>

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

### <span data-ttu-id="94703-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94703-127">-Confirm</span></span>
<span data-ttu-id="94703-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94703-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94703-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94703-129">-WhatIf</span></span>
<span data-ttu-id="94703-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94703-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94703-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94703-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94703-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94703-132">CommonParameters</span></span>
<span data-ttu-id="94703-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94703-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94703-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94703-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94703-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94703-135">INPUTS</span></span>

### <span data-ttu-id="94703-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="94703-136">None</span></span>

## <span data-ttu-id="94703-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94703-137">OUTPUTS</span></span>

### <span data-ttu-id="94703-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="94703-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="94703-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94703-139">NOTES</span></span>

## <span data-ttu-id="94703-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94703-140">RELATED LINKS</span></span>
