---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430675"
---
# <span data-ttu-id="958f1-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="958f1-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="958f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="958f1-102">SYNOPSIS</span></span>
<span data-ttu-id="958f1-103">Remover todas as credenciais e contextos associados a determinada conta.</span><span class="sxs-lookup"><span data-stu-id="958f1-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="958f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="958f1-104">SYNTAX</span></span>

### <span data-ttu-id="958f1-105">Contextname (padrão)</span><span class="sxs-lookup"><span data-stu-id="958f1-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958f1-106">ID</span><span class="sxs-lookup"><span data-stu-id="958f1-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958f1-107">ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="958f1-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958f1-108">Accountobject</span><span class="sxs-lookup"><span data-stu-id="958f1-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958f1-109">Contextobject</span><span class="sxs-lookup"><span data-stu-id="958f1-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="958f1-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="958f1-110">DESCRIPTION</span></span>
<span data-ttu-id="958f1-111">Remover todas as credenciais e contextos (informações de assinatura e locatário) associadas a determinada conta.</span><span class="sxs-lookup"><span data-stu-id="958f1-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="958f1-112">Depois de executar esse cmdlet, você precisará fazer logon novamente usando Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="958f1-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="958f1-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="958f1-113">EXAMPLES</span></span>

### <span data-ttu-id="958f1-114">Desconectar a conta do curent</span><span class="sxs-lookup"><span data-stu-id="958f1-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="958f1-115">Registra a conta associada ao contexto atual.</span><span class="sxs-lookup"><span data-stu-id="958f1-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="958f1-116">Fazer logoff da conta associada a um contexto específico</span><span class="sxs-lookup"><span data-stu-id="958f1-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="958f1-117">Registra a conta associada ao contexto especificado (chamado ' trabalho ').</span><span class="sxs-lookup"><span data-stu-id="958f1-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="958f1-118">Como isso usa o escopo ' CurrentUser ', todas as credenciais e contextos serão excluídos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="958f1-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="958f1-119">Fazer logoff de um usuário específico</span><span class="sxs-lookup"><span data-stu-id="958f1-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="958f1-120">Registra o " user1@contoso.org usuário – todas as credenciais e todos os contextos associados a este usuário serão removidos.</span><span class="sxs-lookup"><span data-stu-id="958f1-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="958f1-121">OS</span><span class="sxs-lookup"><span data-stu-id="958f1-121">PARAMETERS</span></span>

### <span data-ttu-id="958f1-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="958f1-122">-ApplicationId</span></span>
<span data-ttu-id="958f1-123">ID do UserPrincipal (ID globalmente exclusivo)</span><span class="sxs-lookup"><span data-stu-id="958f1-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="958f1-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="958f1-124">-AzureContext</span></span>
<span data-ttu-id="958f1-125">Atalho</span><span class="sxs-lookup"><span data-stu-id="958f1-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="958f1-126">-Contextname</span><span class="sxs-lookup"><span data-stu-id="958f1-126">-ContextName</span></span>
<span data-ttu-id="958f1-127">Nome do contexto para fazer logoff</span><span class="sxs-lookup"><span data-stu-id="958f1-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="958f1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958f1-128">-DefaultProfile</span></span>
<span data-ttu-id="958f1-129">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="958f1-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="958f1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="958f1-130">-InputObject</span></span>
<span data-ttu-id="958f1-131">O objeto de conta a ser removido</span><span class="sxs-lookup"><span data-stu-id="958f1-131">The account object to remove</span></span>

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

### <span data-ttu-id="958f1-132">-Escopo</span><span class="sxs-lookup"><span data-stu-id="958f1-132">-Scope</span></span>
<span data-ttu-id="958f1-133">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="958f1-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="958f1-134">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="958f1-134">-TenantId</span></span>
<span data-ttu-id="958f1-135">ID do locatário (ID globalmente exclusivo)</span><span class="sxs-lookup"><span data-stu-id="958f1-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="958f1-136">-Username</span><span class="sxs-lookup"><span data-stu-id="958f1-136">-Username</span></span>
<span data-ttu-id="958f1-137">Nome de usuário do formulário ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="958f1-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="958f1-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="958f1-138">-Confirm</span></span>
<span data-ttu-id="958f1-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="958f1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958f1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="958f1-140">-WhatIf</span></span>
<span data-ttu-id="958f1-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="958f1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958f1-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="958f1-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="958f1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958f1-143">CommonParameters</span></span>
<span data-ttu-id="958f1-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958f1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958f1-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958f1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958f1-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="958f1-146">INPUTS</span></span>

### <span data-ttu-id="958f1-147">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="958f1-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="958f1-148">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="958f1-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="958f1-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="958f1-149">OUTPUTS</span></span>

### <span data-ttu-id="958f1-150">Microsoft. Azure. Commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="958f1-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="958f1-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="958f1-151">NOTES</span></span>

## <span data-ttu-id="958f1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="958f1-152">RELATED LINKS</span></span>

