---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 4f9dc4bebfa0c7e84c1d52e81796e5c4938e465f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891531"
---
# <span data-ttu-id="62e91-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="62e91-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="62e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e91-102">SYNOPSIS</span></span>
<span data-ttu-id="62e91-103">Desconecta uma conta do Azure conectada e remove todas as credenciais e contextos associados a essa conta.</span><span class="sxs-lookup"><span data-stu-id="62e91-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="62e91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="62e91-104">SYNTAX</span></span>

### <span data-ttu-id="62e91-105">ContextName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62e91-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e91-106">UserId</span><span class="sxs-lookup"><span data-stu-id="62e91-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e91-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="62e91-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e91-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="62e91-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e91-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="62e91-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e91-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="62e91-110">DESCRIPTION</span></span>
<span data-ttu-id="62e91-111">O Disconnect-AzAccount cmdlet desconecta uma conta conectada do Azure e remove todas as credenciais e contextos (informações de assinatura e locatário) associados a essa conta.</span><span class="sxs-lookup"><span data-stu-id="62e91-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="62e91-112">Depois de executar esse cmdlet, você precisará fazer logon novamente usando Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="62e91-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="62e91-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62e91-113">EXAMPLES</span></span>

### <span data-ttu-id="62e91-114">Exemplo 1: Logout da conta atual</span><span class="sxs-lookup"><span data-stu-id="62e91-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="62e91-115">Faz logs da conta do Azure associada ao contexto atual.</span><span class="sxs-lookup"><span data-stu-id="62e91-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="62e91-116">Exemplo 2: Logout da conta associada a um contexto específico</span><span class="sxs-lookup"><span data-stu-id="62e91-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="62e91-117">Registra a conta associada ao contexto determinado (chamado 'Trabalho').</span><span class="sxs-lookup"><span data-stu-id="62e91-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="62e91-118">Como isso usa o escopo 'CurrentUser', todas as credenciais e contextos serão excluídos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="62e91-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="62e91-119">Exemplo 3: Fazer logoff de um usuário específico</span><span class="sxs-lookup"><span data-stu-id="62e91-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="62e91-120">Logs out the ' ' user - todas as credenciais e todos os user1@contoso.org contextos associados a esse usuário serão removidos.</span><span class="sxs-lookup"><span data-stu-id="62e91-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="62e91-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="62e91-121">PARAMETERS</span></span>

### <span data-ttu-id="62e91-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="62e91-122">-ApplicationId</span></span>
<span data-ttu-id="62e91-123">ID servicePrincipal (id global exclusiva)</span><span class="sxs-lookup"><span data-stu-id="62e91-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="62e91-124">-AzureContext</span></span>
<span data-ttu-id="62e91-125">Contexto</span><span class="sxs-lookup"><span data-stu-id="62e91-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="62e91-126">-ContextName</span></span>
<span data-ttu-id="62e91-127">Nome do contexto do qual fazer logoff</span><span class="sxs-lookup"><span data-stu-id="62e91-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e91-128">-DefaultProfile</span></span>
<span data-ttu-id="62e91-129">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="62e91-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62e91-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62e91-130">-InputObject</span></span>
<span data-ttu-id="62e91-131">O objeto account a ser removido</span><span class="sxs-lookup"><span data-stu-id="62e91-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="62e91-132">-Scope</span></span>
<span data-ttu-id="62e91-133">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="62e91-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="62e91-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="62e91-134">-TenantId</span></span>
<span data-ttu-id="62e91-135">ID do locatário (id global exclusiva)</span><span class="sxs-lookup"><span data-stu-id="62e91-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-136">-Username</span><span class="sxs-lookup"><span data-stu-id="62e91-136">-Username</span></span>
<span data-ttu-id="62e91-137">Nome de usuário do formulário ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="62e91-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e91-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62e91-138">-Confirm</span></span>
<span data-ttu-id="62e91-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e91-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e91-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e91-140">-WhatIf</span></span>
<span data-ttu-id="62e91-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62e91-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e91-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62e91-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="62e91-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e91-143">CommonParameters</span></span>
<span data-ttu-id="62e91-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e91-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e91-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e91-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e91-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62e91-146">INPUTS</span></span>

### <span data-ttu-id="62e91-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="62e91-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="62e91-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="62e91-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="62e91-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="62e91-149">OUTPUTS</span></span>

### <span data-ttu-id="62e91-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="62e91-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="62e91-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="62e91-151">NOTES</span></span>

## <span data-ttu-id="62e91-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62e91-152">RELATED LINKS</span></span>
