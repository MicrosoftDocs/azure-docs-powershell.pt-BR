---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 03bceaee69bfa739268fa4cb1be8c9699f26f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892915"
---
# <span data-ttu-id="427c3-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="427c3-101">Set-AzContext</span></span>

## <span data-ttu-id="427c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="427c3-102">SYNOPSIS</span></span>
<span data-ttu-id="427c3-103">Define o locatário, a assinatura e o ambiente para cmdlets a usar na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="427c3-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="427c3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="427c3-104">SYNTAX</span></span>

### <span data-ttu-id="427c3-105">Contexto (Padrão)</span><span class="sxs-lookup"><span data-stu-id="427c3-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="427c3-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="427c3-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="427c3-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="427c3-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="427c3-108">Assinatura</span><span class="sxs-lookup"><span data-stu-id="427c3-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="427c3-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="427c3-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="427c3-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="427c3-110">DESCRIPTION</span></span>
<span data-ttu-id="427c3-111">O Set-AzContext cmdlet define informações de autenticação para cmdlets executados na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="427c3-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="427c3-112">O contexto inclui informações de locatário, assinatura e ambiente.</span><span class="sxs-lookup"><span data-stu-id="427c3-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="427c3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="427c3-113">EXAMPLES</span></span>

### <span data-ttu-id="427c3-114">Exemplo 1: Definir o contexto da assinatura</span><span class="sxs-lookup"><span data-stu-id="427c3-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="427c3-115">Este comando define o contexto para usar a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="427c3-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="427c3-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="427c3-116">PARAMETERS</span></span>

### <span data-ttu-id="427c3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="427c3-117">-Context</span></span>
<span data-ttu-id="427c3-118">Especifica o contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="427c3-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427c3-119">-DefaultProfile</span></span>
<span data-ttu-id="427c3-120">As credenciais, locatários e assinaturas usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="427c3-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="427c3-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="427c3-121">-ExtendedProperty</span></span>
<span data-ttu-id="427c3-122">Propriedades de contexto adicionais</span><span class="sxs-lookup"><span data-stu-id="427c3-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="427c3-123">-Force</span></span>
<span data-ttu-id="427c3-124">Sobrescreva o contexto existente com o mesmo nome, se for o caso.</span><span class="sxs-lookup"><span data-stu-id="427c3-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="427c3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="427c3-125">-Name</span></span>
<span data-ttu-id="427c3-126">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="427c3-126">Name of the context</span></span>

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

### <span data-ttu-id="427c3-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="427c3-127">-Scope</span></span>
<span data-ttu-id="427c3-128">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="427c3-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="427c3-129">-Subscription</span></span>
<span data-ttu-id="427c3-130">O nome ou a id da assinatura à qual o contexto deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="427c3-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="427c3-131">Esse parâmetro tem aliases para -SubscriptionName e -SubscriptionId, portanto, para esclarecer, um deles pode ser usado em vez de -Subscription ao especificar nome e id, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="427c3-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="427c3-132">-SubscriptionObject</span></span>
<span data-ttu-id="427c3-133">Um objeto subscription</span><span class="sxs-lookup"><span data-stu-id="427c3-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="427c3-134">-Tenant</span></span>
<span data-ttu-id="427c3-135">Nome do locatário ou ID</span><span class="sxs-lookup"><span data-stu-id="427c3-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="427c3-136">-TenantObject</span></span>
<span data-ttu-id="427c3-137">Um objeto Tenant</span><span class="sxs-lookup"><span data-stu-id="427c3-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="427c3-138">-Confirm</span></span>
<span data-ttu-id="427c3-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="427c3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="427c3-140">-WhatIf</span></span>
<span data-ttu-id="427c3-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="427c3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="427c3-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="427c3-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="427c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427c3-143">CommonParameters</span></span>
<span data-ttu-id="427c3-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="427c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427c3-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="427c3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427c3-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="427c3-146">INPUTS</span></span>

### <span data-ttu-id="427c3-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="427c3-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="427c3-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="427c3-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="427c3-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="427c3-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="427c3-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="427c3-150">OUTPUTS</span></span>

### <span data-ttu-id="427c3-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="427c3-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="427c3-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="427c3-152">NOTES</span></span>

## <span data-ttu-id="427c3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="427c3-153">RELATED LINKS</span></span>

[<span data-ttu-id="427c3-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="427c3-154">Get-AzContext</span></span>](./Get-AzContext.md)

