---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439840"
---
# <span data-ttu-id="ea8a2-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ea8a2-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="ea8a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8a2-103">Define o locatário, a assinatura e o ambiente para cmdlets a serem usados na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea8a2-104">SYNTAX</span></span>

### <span data-ttu-id="ea8a2-105">Contexto (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea8a2-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8a2-106">Tenantobject</span><span class="sxs-lookup"><span data-stu-id="ea8a2-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8a2-107">Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="ea8a2-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8a2-108">Expira</span><span class="sxs-lookup"><span data-stu-id="ea8a2-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8a2-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="ea8a2-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea8a2-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea8a2-110">DESCRIPTION</span></span>
<span data-ttu-id="ea8a2-111">O cmdlet Set-AzureRmContext define informações de autenticação para cmdlets que você executa na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="ea8a2-112">O contexto inclui informações de locatário, assinatura e ambiente.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="ea8a2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea8a2-113">EXAMPLES</span></span>

### <span data-ttu-id="ea8a2-114">Exemplo 1: definir o contexto da assinatura</span><span class="sxs-lookup"><span data-stu-id="ea8a2-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="ea8a2-115">Este comando define o contexto para usar a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="ea8a2-116">OS</span><span class="sxs-lookup"><span data-stu-id="ea8a2-116">PARAMETERS</span></span>

### <span data-ttu-id="ea8a2-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ea8a2-117">-Context</span></span>
<span data-ttu-id="ea8a2-118">Especifica o contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8a2-119">-DefaultProfile</span></span>
<span data-ttu-id="ea8a2-120">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="ea8a2-121">-ExtendedProperty</span></span>
<span data-ttu-id="ea8a2-122">Propriedades de contexto adicionais</span><span class="sxs-lookup"><span data-stu-id="ea8a2-122">Additional context properties</span></span>

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

### <span data-ttu-id="ea8a2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ea8a2-123">-Force</span></span>
<span data-ttu-id="ea8a2-124">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea8a2-125">-Name</span></span>
<span data-ttu-id="ea8a2-126">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="ea8a2-126">Name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="ea8a2-127">-Scope</span></span>
<span data-ttu-id="ea8a2-128">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="ea8a2-129">-Subscription</span></span>
<span data-ttu-id="ea8a2-130">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="ea8a2-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-131">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="ea8a2-131">-SubscriptionObject</span></span>
<span data-ttu-id="ea8a2-132">Um objeto de assinatura</span><span class="sxs-lookup"><span data-stu-id="ea8a2-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-133">-Locatário</span><span class="sxs-lookup"><span data-stu-id="ea8a2-133">-Tenant</span></span>
<span data-ttu-id="ea8a2-134">Nome ou ID do locatário</span><span class="sxs-lookup"><span data-stu-id="ea8a2-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-135">-Tenantobject</span><span class="sxs-lookup"><span data-stu-id="ea8a2-135">-TenantObject</span></span>
<span data-ttu-id="ea8a2-136">Um objeto locatário</span><span class="sxs-lookup"><span data-stu-id="ea8a2-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea8a2-137">-Confirm</span></span>
<span data-ttu-id="ea8a2-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8a2-139">-WhatIf</span></span>
<span data-ttu-id="ea8a2-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea8a2-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8a2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8a2-142">CommonParameters</span></span>
<span data-ttu-id="ea8a2-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8a2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8a2-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8a2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8a2-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea8a2-145">INPUTS</span></span>

### <span data-ttu-id="ea8a2-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ea8a2-146">PSAzureContext</span></span>
<span data-ttu-id="ea8a2-147">O parâmetro ' Context ' aceita o valor do tipo ' PSAzureContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ea8a2-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="ea8a2-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea8a2-148">OUTPUTS</span></span>

### <span data-ttu-id="ea8a2-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ea8a2-149">PSAzureContext</span></span>

## <span data-ttu-id="ea8a2-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea8a2-150">NOTES</span></span>

## <span data-ttu-id="ea8a2-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea8a2-151">RELATED LINKS</span></span>

[<span data-ttu-id="ea8a2-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="ea8a2-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

