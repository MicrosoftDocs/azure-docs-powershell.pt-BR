---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 275f43d184e6b34aeeba83a9563a812649a6044c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887355"
---
# <span data-ttu-id="51b85-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="51b85-101">New-AzADUser</span></span>

## <span data-ttu-id="51b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b85-102">SYNOPSIS</span></span>
<span data-ttu-id="51b85-103">Cria um novo usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="51b85-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="51b85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51b85-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51b85-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51b85-105">DESCRIPTION</span></span>
<span data-ttu-id="51b85-106">Cria um novo usuário do Active Directory (conta de trabalho/escola também popularmente conhecida como org-id).</span><span class="sxs-lookup"><span data-stu-id="51b85-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="51b85-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="51b85-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="51b85-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51b85-108">EXAMPLES</span></span>

### <span data-ttu-id="51b85-109">Exemplo 1: Criar um novo usuário do AD</span><span class="sxs-lookup"><span data-stu-id="51b85-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="51b85-110">Cria um novo usuário do AD com o nome "MyDisplayName" e o nome principal do usuário myemail@domain.com " em um locatário.</span><span class="sxs-lookup"><span data-stu-id="51b85-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="51b85-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51b85-111">PARAMETERS</span></span>

### <span data-ttu-id="51b85-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b85-112">-DefaultProfile</span></span>
<span data-ttu-id="51b85-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="51b85-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51b85-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="51b85-114">-DisplayName</span></span>
<span data-ttu-id="51b85-115">O nome a ser exibido no livro de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="51b85-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="51b85-116">exemplo 'Alex Wu'.</span><span class="sxs-lookup"><span data-stu-id="51b85-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="51b85-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="51b85-118">Ele deve ser especificado se o usuário deve alterar a senha no próximo logon bem-sucedido (true).</span><span class="sxs-lookup"><span data-stu-id="51b85-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="51b85-119">O comportamento padrão é (false) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="51b85-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="51b85-120">-ImmutableId</span></span>
<span data-ttu-id="51b85-121">Ele precisa ser especificado somente se você estiver usando um domínio federado para a propriedade user principal name (upn).</span><span class="sxs-lookup"><span data-stu-id="51b85-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="51b85-122">-MailNickname</span></span>
<span data-ttu-id="51b85-123">O alias de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="51b85-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-124">-Password</span><span class="sxs-lookup"><span data-stu-id="51b85-124">-Password</span></span>
<span data-ttu-id="51b85-125">Senha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="51b85-125">Password for the user.</span></span>
<span data-ttu-id="51b85-126">Ele deve atender aos requisitos de complexidade de senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="51b85-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="51b85-127">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="51b85-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="51b85-128">-UserPrincipalName</span></span>
<span data-ttu-id="51b85-129">O nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="51b85-129">The user principal name.</span></span>
<span data-ttu-id="51b85-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="51b85-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b85-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51b85-131">-Confirm</span></span>
<span data-ttu-id="51b85-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51b85-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b85-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b85-133">-WhatIf</span></span>
<span data-ttu-id="51b85-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51b85-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b85-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51b85-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b85-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b85-136">CommonParameters</span></span>
<span data-ttu-id="51b85-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b85-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b85-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51b85-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b85-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51b85-139">INPUTS</span></span>

### <span data-ttu-id="51b85-140">System.String</span><span class="sxs-lookup"><span data-stu-id="51b85-140">System.String</span></span>

### <span data-ttu-id="51b85-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="51b85-141">System.Security.SecureString</span></span>

### <span data-ttu-id="51b85-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="51b85-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="51b85-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51b85-143">OUTPUTS</span></span>

### <span data-ttu-id="51b85-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="51b85-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="51b85-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="51b85-145">NOTES</span></span>

## <span data-ttu-id="51b85-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51b85-146">RELATED LINKS</span></span>

[<span data-ttu-id="51b85-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="51b85-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="51b85-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="51b85-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="51b85-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="51b85-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
