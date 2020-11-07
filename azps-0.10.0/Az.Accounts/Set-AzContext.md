---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 5dcb1636dc4ecc4556bea14f8b3cd52bec7c0927
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775227"
---
# <span data-ttu-id="096dd-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="096dd-101">Set-AzContext</span></span>

## <span data-ttu-id="096dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="096dd-102">SYNOPSIS</span></span>
<span data-ttu-id="096dd-103">Define o locatário, a assinatura e o ambiente para cmdlets a serem usados na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="096dd-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="096dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="096dd-104">SYNTAX</span></span>

### <span data-ttu-id="096dd-105">Contexto (padrão)</span><span class="sxs-lookup"><span data-stu-id="096dd-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="096dd-106">Tenantobject</span><span class="sxs-lookup"><span data-stu-id="096dd-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="096dd-107">Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="096dd-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="096dd-108">Expira</span><span class="sxs-lookup"><span data-stu-id="096dd-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="096dd-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="096dd-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="096dd-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="096dd-110">DESCRIPTION</span></span>
<span data-ttu-id="096dd-111">O cmdlet Set-AzContext define informações de autenticação para cmdlets que você executa na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="096dd-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="096dd-112">O contexto inclui informações de locatário, assinatura e ambiente.</span><span class="sxs-lookup"><span data-stu-id="096dd-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="096dd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="096dd-113">EXAMPLES</span></span>

### <span data-ttu-id="096dd-114">Exemplo 1: definir o contexto da assinatura</span><span class="sxs-lookup"><span data-stu-id="096dd-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="096dd-115">Este comando define o contexto para usar a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="096dd-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="096dd-116">OS</span><span class="sxs-lookup"><span data-stu-id="096dd-116">PARAMETERS</span></span>

### <span data-ttu-id="096dd-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="096dd-117">-Context</span></span>
<span data-ttu-id="096dd-118">Especifica o contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="096dd-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="096dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096dd-119">-DefaultProfile</span></span>
<span data-ttu-id="096dd-120">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="096dd-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096dd-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="096dd-121">-ExtendedProperty</span></span>
<span data-ttu-id="096dd-122">Propriedades de contexto adicionais</span><span class="sxs-lookup"><span data-stu-id="096dd-122">Additional context properties</span></span>

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

### <span data-ttu-id="096dd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="096dd-123">-Force</span></span>
<span data-ttu-id="096dd-124">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="096dd-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="096dd-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="096dd-125">-Name</span></span>
<span data-ttu-id="096dd-126">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="096dd-126">Name of the context</span></span>

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

### <span data-ttu-id="096dd-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="096dd-127">-Scope</span></span>
<span data-ttu-id="096dd-128">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="096dd-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="096dd-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="096dd-129">-Subscription</span></span>
<span data-ttu-id="096dd-130">O nome ou a ID da assinatura à qual o contexto deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="096dd-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="096dd-131">Esse parâmetro tem aliases para-Subscriptionname e-SubscriptionId, portanto, para maior clareza, qualquer um deles pode ser usado em vez de-assinatura ao especificar o nome e a ID, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="096dd-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="096dd-132">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="096dd-132">-SubscriptionObject</span></span>
<span data-ttu-id="096dd-133">Um objeto de assinatura</span><span class="sxs-lookup"><span data-stu-id="096dd-133">A subscription object</span></span>

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

### <span data-ttu-id="096dd-134">-Locatário</span><span class="sxs-lookup"><span data-stu-id="096dd-134">-Tenant</span></span>
<span data-ttu-id="096dd-135">Nome ou ID do locatário</span><span class="sxs-lookup"><span data-stu-id="096dd-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="096dd-136">-Tenantobject</span><span class="sxs-lookup"><span data-stu-id="096dd-136">-TenantObject</span></span>
<span data-ttu-id="096dd-137">Um objeto locatário</span><span class="sxs-lookup"><span data-stu-id="096dd-137">A Tenant Object</span></span>

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

### <span data-ttu-id="096dd-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="096dd-138">-Confirm</span></span>
<span data-ttu-id="096dd-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="096dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096dd-140">-WhatIf</span></span>
<span data-ttu-id="096dd-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="096dd-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="096dd-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="096dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096dd-143">CommonParameters</span></span>
<span data-ttu-id="096dd-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096dd-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="096dd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096dd-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="096dd-146">INPUTS</span></span>

### <span data-ttu-id="096dd-147">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="096dd-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="096dd-148">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="096dd-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="096dd-149">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="096dd-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="096dd-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="096dd-150">OUTPUTS</span></span>

### <span data-ttu-id="096dd-151">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="096dd-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="096dd-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="096dd-152">NOTES</span></span>

## <span data-ttu-id="096dd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="096dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="096dd-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="096dd-154">Get-AzContext</span></span>](./Get-AzContext.md)

