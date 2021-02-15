---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112434"
---
# <span data-ttu-id="66d79-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="66d79-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="66d79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66d79-102">SYNOPSIS</span></span>
<span data-ttu-id="66d79-103">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="66d79-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="66d79-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66d79-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d79-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="66d79-105">DESCRIPTION</span></span>
<span data-ttu-id="66d79-106">O cmdlet **New-AzSubscriptionAlias** cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="66d79-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="66d79-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66d79-107">EXAMPLES</span></span>

### <span data-ttu-id="66d79-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66d79-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="66d79-109">Cria novo alias e assinatura</span><span class="sxs-lookup"><span data-stu-id="66d79-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="66d79-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66d79-110">PARAMETERS</span></span>

### <span data-ttu-id="66d79-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="66d79-111">-AliasName</span></span>
<span data-ttu-id="66d79-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="66d79-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="66d79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66d79-113">-AsJob</span></span>
<span data-ttu-id="66d79-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="66d79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66d79-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="66d79-115">-BillingScope</span></span>
<span data-ttu-id="66d79-116">Escopo da cobrança</span><span class="sxs-lookup"><span data-stu-id="66d79-116">Billing Scope</span></span>

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

### <span data-ttu-id="66d79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d79-117">-DefaultProfile</span></span>
<span data-ttu-id="66d79-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66d79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d79-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="66d79-119">-ResellerId</span></span>
<span data-ttu-id="66d79-120">ID do revendedor</span><span class="sxs-lookup"><span data-stu-id="66d79-120">Reseller Id</span></span>

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

### <span data-ttu-id="66d79-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66d79-121">-SubscriptionId</span></span>
<span data-ttu-id="66d79-122">ID de assinatura existente</span><span class="sxs-lookup"><span data-stu-id="66d79-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="66d79-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="66d79-123">-SubscriptionName</span></span>
<span data-ttu-id="66d79-124">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="66d79-124">Name of the subscription</span></span>

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

### <span data-ttu-id="66d79-125">-Carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="66d79-125">-Workload</span></span>
<span data-ttu-id="66d79-126">Tipo de carga de trabalho</span><span class="sxs-lookup"><span data-stu-id="66d79-126">Type of Workload</span></span>

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

### <span data-ttu-id="66d79-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66d79-127">-Confirm</span></span>
<span data-ttu-id="66d79-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66d79-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d79-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d79-129">-WhatIf</span></span>
<span data-ttu-id="66d79-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66d79-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d79-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66d79-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d79-132">CommonParameters</span></span>
<span data-ttu-id="66d79-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d79-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66d79-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d79-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="66d79-135">INPUTS</span></span>

### <span data-ttu-id="66d79-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="66d79-136">None</span></span>

## <span data-ttu-id="66d79-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="66d79-137">OUTPUTS</span></span>

### <span data-ttu-id="66d79-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="66d79-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="66d79-139">Notas</span><span class="sxs-lookup"><span data-stu-id="66d79-139">NOTES</span></span>

## <span data-ttu-id="66d79-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66d79-140">RELATED LINKS</span></span>
