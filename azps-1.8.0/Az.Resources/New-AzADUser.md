---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: cd8834dd329ab82e98316cb0d94b554eb3bb6c13
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399644"
---
# <span data-ttu-id="6476b-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6476b-101">New-AzADUser</span></span>

## <span data-ttu-id="6476b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6476b-102">SYNOPSIS</span></span>
<span data-ttu-id="6476b-103">Cria um novo usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6476b-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="6476b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6476b-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6476b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6476b-105">DESCRIPTION</span></span>
<span data-ttu-id="6476b-106">Cria um novo usuário do Active Directory (conta de trabalho/escola também conhecida popularmente como org-id).</span><span class="sxs-lookup"><span data-stu-id="6476b-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="6476b-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="6476b-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="6476b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6476b-108">EXAMPLES</span></span>

### <span data-ttu-id="6476b-109">Exemplo 1 - Criar um novo usuário do AD</span><span class="sxs-lookup"><span data-stu-id="6476b-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="6476b-110">Cria um novo usuário do AD com o nome "MeuDisplayName" e o nome principal do usuário myemail@domain.com " em um locatário.</span><span class="sxs-lookup"><span data-stu-id="6476b-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="6476b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6476b-111">PARAMETERS</span></span>

### <span data-ttu-id="6476b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6476b-112">-DefaultProfile</span></span>
<span data-ttu-id="6476b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6476b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6476b-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6476b-114">-DisplayName</span></span>
<span data-ttu-id="6476b-115">O nome a ser exibido no livro de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="6476b-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="6476b-116">exemplo 'Alex Wu'.</span><span class="sxs-lookup"><span data-stu-id="6476b-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="6476b-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="6476b-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="6476b-118">Ele deve ser especificado se o usuário deve alterar a senha no próximo logon bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="6476b-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="6476b-119">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6476b-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="6476b-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="6476b-120">-ImmutableId</span></span>
<span data-ttu-id="6476b-121">Ele só deve ser especificado se você estiver usando um domínio federado para a propriedade de nome de usuário principal (upn) do usuário.</span><span class="sxs-lookup"><span data-stu-id="6476b-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="6476b-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="6476b-122">-MailNickname</span></span>
<span data-ttu-id="6476b-123">O alias de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="6476b-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="6476b-124">-Senha</span><span class="sxs-lookup"><span data-stu-id="6476b-124">-Password</span></span>
<span data-ttu-id="6476b-125">Senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="6476b-125">Password for the user.</span></span>
<span data-ttu-id="6476b-126">Ele deve atender aos requisitos de complexidade de senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="6476b-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="6476b-127">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="6476b-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="6476b-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6476b-128">-UserPrincipalName</span></span>
<span data-ttu-id="6476b-129">O nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="6476b-129">The user principal name.</span></span>
<span data-ttu-id="6476b-130">Exemplo'' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="6476b-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="6476b-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6476b-131">-Confirm</span></span>
<span data-ttu-id="6476b-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6476b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6476b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6476b-133">-WhatIf</span></span>
<span data-ttu-id="6476b-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6476b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6476b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6476b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6476b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6476b-136">CommonParameters</span></span>
<span data-ttu-id="6476b-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6476b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6476b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6476b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6476b-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="6476b-139">INPUTS</span></span>

### <span data-ttu-id="6476b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6476b-140">System.String</span></span>

### <span data-ttu-id="6476b-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="6476b-141">System.Security.SecureString</span></span>

### <span data-ttu-id="6476b-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6476b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6476b-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6476b-143">OUTPUTS</span></span>

### <span data-ttu-id="6476b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="6476b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6476b-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6476b-145">NOTES</span></span>

## <span data-ttu-id="6476b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6476b-146">RELATED LINKS</span></span>

[<span data-ttu-id="6476b-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6476b-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="6476b-148">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6476b-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
