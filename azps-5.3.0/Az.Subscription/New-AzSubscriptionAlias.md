---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272466"
---
# <span data-ttu-id="47855-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="47855-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="47855-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47855-102">SYNOPSIS</span></span>
<span data-ttu-id="47855-103">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="47855-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="47855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47855-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47855-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47855-105">DESCRIPTION</span></span>
<span data-ttu-id="47855-106">O cmdlet **New-AzSubscriptionAlias** cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="47855-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="47855-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47855-107">EXAMPLES</span></span>

### <span data-ttu-id="47855-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47855-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="47855-109">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="47855-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="47855-110">OS</span><span class="sxs-lookup"><span data-stu-id="47855-110">PARAMETERS</span></span>

### <span data-ttu-id="47855-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="47855-111">-AliasName</span></span>
<span data-ttu-id="47855-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="47855-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="47855-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47855-113">-AsJob</span></span>
<span data-ttu-id="47855-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47855-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47855-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="47855-115">-BillingScope</span></span>
<span data-ttu-id="47855-116">Escopo de cobrança</span><span class="sxs-lookup"><span data-stu-id="47855-116">Billing Scope</span></span>

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

### <span data-ttu-id="47855-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47855-117">-DefaultProfile</span></span>
<span data-ttu-id="47855-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47855-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47855-119">-Revendedora</span><span class="sxs-lookup"><span data-stu-id="47855-119">-ResellerId</span></span>
<span data-ttu-id="47855-120">ID do revendedor</span><span class="sxs-lookup"><span data-stu-id="47855-120">Reseller Id</span></span>

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

### <span data-ttu-id="47855-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47855-121">-SubscriptionId</span></span>
<span data-ttu-id="47855-122">ID de assinatura existente</span><span class="sxs-lookup"><span data-stu-id="47855-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="47855-123">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="47855-123">-SubscriptionName</span></span>
<span data-ttu-id="47855-124">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="47855-124">Name of the subscription</span></span>

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

### <span data-ttu-id="47855-125">-Carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="47855-125">-Workload</span></span>
<span data-ttu-id="47855-126">Tipo de carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="47855-126">Type of Workload</span></span>

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

### <span data-ttu-id="47855-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47855-127">-Confirm</span></span>
<span data-ttu-id="47855-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47855-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47855-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47855-129">-WhatIf</span></span>
<span data-ttu-id="47855-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47855-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47855-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47855-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47855-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47855-132">CommonParameters</span></span>
<span data-ttu-id="47855-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47855-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47855-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47855-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47855-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47855-135">INPUTS</span></span>

### <span data-ttu-id="47855-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="47855-136">None</span></span>

## <span data-ttu-id="47855-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47855-137">OUTPUTS</span></span>

### <span data-ttu-id="47855-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="47855-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="47855-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47855-139">NOTES</span></span>

## <span data-ttu-id="47855-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47855-140">RELATED LINKS</span></span>
