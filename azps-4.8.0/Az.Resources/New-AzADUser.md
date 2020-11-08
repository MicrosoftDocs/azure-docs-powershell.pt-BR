---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: c7863e62330dc26d9733d21eb8e4d11753e06d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110969"
---
# <span data-ttu-id="871df-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="871df-101">New-AzADUser</span></span>

## <span data-ttu-id="871df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="871df-102">SYNOPSIS</span></span>
<span data-ttu-id="871df-103">Cria um novo usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="871df-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="871df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="871df-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="871df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="871df-105">DESCRIPTION</span></span>
<span data-ttu-id="871df-106">Cria um novo usuário do Active Directory (conta corporativa/de estudante também conhecida conhecida como org-ID).</span><span class="sxs-lookup"><span data-stu-id="871df-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="871df-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="871df-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="871df-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="871df-108">EXAMPLES</span></span>

### <span data-ttu-id="871df-109">Exemplo 1: criar um novo usuário do AD</span><span class="sxs-lookup"><span data-stu-id="871df-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="871df-110">Cria um novo usuário do AD com o nome "MyDisplayName" e o nome UPN myemail@domain.com do usuário "" em um locatário.</span><span class="sxs-lookup"><span data-stu-id="871df-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="871df-111">OS</span><span class="sxs-lookup"><span data-stu-id="871df-111">PARAMETERS</span></span>

### <span data-ttu-id="871df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871df-112">-DefaultProfile</span></span>
<span data-ttu-id="871df-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="871df-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="871df-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="871df-114">-DisplayName</span></span>
<span data-ttu-id="871df-115">O nome a ser exibido no catálogo de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="871df-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="871df-116">exemplo ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="871df-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="871df-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="871df-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="871df-118">Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="871df-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="871df-119">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="871df-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="871df-120">-Imutávelid</span><span class="sxs-lookup"><span data-stu-id="871df-120">-ImmutableId</span></span>
<span data-ttu-id="871df-121">Ele precisa ser especificado apenas se você estiver usando um domínio federado para a propriedade de nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="871df-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="871df-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="871df-122">-MailNickname</span></span>
<span data-ttu-id="871df-123">O alias do email do usuário.</span><span class="sxs-lookup"><span data-stu-id="871df-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="871df-124">-Senha</span><span class="sxs-lookup"><span data-stu-id="871df-124">-Password</span></span>
<span data-ttu-id="871df-125">Senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="871df-125">Password for the user.</span></span>
<span data-ttu-id="871df-126">Ele deve atender aos requisitos de complexidade da senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="871df-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="871df-127">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="871df-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="871df-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="871df-128">-UserPrincipalName</span></span>
<span data-ttu-id="871df-129">O nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="871df-129">The user principal name.</span></span>
<span data-ttu-id="871df-130">Exemplo-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="871df-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="871df-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="871df-131">-Confirm</span></span>
<span data-ttu-id="871df-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="871df-133">-WhatIf</span></span>
<span data-ttu-id="871df-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="871df-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871df-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="871df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871df-136">CommonParameters</span></span>
<span data-ttu-id="871df-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871df-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="871df-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871df-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="871df-139">INPUTS</span></span>

### <span data-ttu-id="871df-140">System. String</span><span class="sxs-lookup"><span data-stu-id="871df-140">System.String</span></span>

### <span data-ttu-id="871df-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="871df-141">System.Security.SecureString</span></span>

### <span data-ttu-id="871df-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="871df-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="871df-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="871df-143">OUTPUTS</span></span>

### <span data-ttu-id="871df-144">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="871df-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="871df-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="871df-145">NOTES</span></span>

## <span data-ttu-id="871df-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="871df-146">RELATED LINKS</span></span>

[<span data-ttu-id="871df-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="871df-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="871df-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="871df-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="871df-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="871df-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
