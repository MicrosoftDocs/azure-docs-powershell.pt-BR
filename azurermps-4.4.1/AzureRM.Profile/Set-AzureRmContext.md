---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603343"
---
# <span data-ttu-id="f09d0-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f09d0-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="f09d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f09d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f09d0-103">Define o locatário, a assinatura e o ambiente para cmdlets a serem usados na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="f09d0-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f09d0-104">SYNTAX</span></span>

### <span data-ttu-id="f09d0-105">Contexto (padrão)</span><span class="sxs-lookup"><span data-stu-id="f09d0-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09d0-106">Tenantobject</span><span class="sxs-lookup"><span data-stu-id="f09d0-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09d0-107">Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="f09d0-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09d0-108">Expira</span><span class="sxs-lookup"><span data-stu-id="f09d0-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09d0-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="f09d0-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09d0-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f09d0-110">DESCRIPTION</span></span>
<span data-ttu-id="f09d0-111">O cmdlet Set-AzureRmContext define informações de autenticação para cmdlets que você executa na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="f09d0-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="f09d0-112">O contexto inclui informações de locatário, assinatura e ambiente.</span><span class="sxs-lookup"><span data-stu-id="f09d0-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="f09d0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f09d0-113">EXAMPLES</span></span>

### <span data-ttu-id="f09d0-114">Exemplo 1: definir o contexto da assinatura</span><span class="sxs-lookup"><span data-stu-id="f09d0-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="f09d0-115">Este comando define o contexto para usar a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="f09d0-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="f09d0-116">OS</span><span class="sxs-lookup"><span data-stu-id="f09d0-116">PARAMETERS</span></span>

### <span data-ttu-id="f09d0-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f09d0-117">-Context</span></span>
<span data-ttu-id="f09d0-118">Especifica o contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="f09d0-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09d0-119">-DefaultProfile</span></span>
<span data-ttu-id="f09d0-120">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f09d0-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09d0-121">-Extended</span><span class="sxs-lookup"><span data-stu-id="f09d0-121">-ExtendedProperty</span></span>
<span data-ttu-id="f09d0-122">Propriedades de contexto adicionais</span><span class="sxs-lookup"><span data-stu-id="f09d0-122">Additional context properties</span></span>

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

### <span data-ttu-id="f09d0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f09d0-123">-Force</span></span>
<span data-ttu-id="f09d0-124">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="f09d0-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="f09d0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f09d0-125">-Name</span></span>
<span data-ttu-id="f09d0-126">Nome do contexto</span><span class="sxs-lookup"><span data-stu-id="f09d0-126">Name of the context</span></span>

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

### <span data-ttu-id="f09d0-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f09d0-127">-Scope</span></span>
<span data-ttu-id="f09d0-128">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="f09d0-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f09d0-129">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f09d0-129">-Subscription</span></span>
<span data-ttu-id="f09d0-130">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="f09d0-130">Subscription Name or Id</span></span>

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

### <span data-ttu-id="f09d0-131">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="f09d0-131">-SubscriptionObject</span></span>
<span data-ttu-id="f09d0-132">Um objeto de assinatura</span><span class="sxs-lookup"><span data-stu-id="f09d0-132">A subscription object</span></span>

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

### <span data-ttu-id="f09d0-133">-Locatário</span><span class="sxs-lookup"><span data-stu-id="f09d0-133">-Tenant</span></span>
<span data-ttu-id="f09d0-134">Nome ou ID do locatário</span><span class="sxs-lookup"><span data-stu-id="f09d0-134">Tenant name or ID</span></span>

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

### <span data-ttu-id="f09d0-135">-Tenantobject</span><span class="sxs-lookup"><span data-stu-id="f09d0-135">-TenantObject</span></span>
<span data-ttu-id="f09d0-136">Um objeto locatário</span><span class="sxs-lookup"><span data-stu-id="f09d0-136">A Tenant Object</span></span>

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

### <span data-ttu-id="f09d0-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f09d0-137">-Confirm</span></span>
<span data-ttu-id="f09d0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09d0-139">-WhatIf</span></span>
<span data-ttu-id="f09d0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f09d0-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f09d0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f09d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09d0-142">CommonParameters</span></span>
<span data-ttu-id="f09d0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09d0-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09d0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09d0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f09d0-145">INPUTS</span></span>

### <span data-ttu-id="f09d0-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f09d0-146">PSAzureContext</span></span>
<span data-ttu-id="f09d0-147">O parâmetro ' Context ' aceita o valor do tipo ' PSAzureContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f09d0-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="f09d0-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f09d0-148">OUTPUTS</span></span>

### <span data-ttu-id="f09d0-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f09d0-149">PSAzureContext</span></span>

## <span data-ttu-id="f09d0-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f09d0-150">NOTES</span></span>

## <span data-ttu-id="f09d0-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f09d0-151">RELATED LINKS</span></span>

[<span data-ttu-id="f09d0-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f09d0-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

