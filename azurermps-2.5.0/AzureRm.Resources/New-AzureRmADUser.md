---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 5a1f0b5bac62c4b10912fbbffc07cda7c1f2fb7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786051"
---
# <span data-ttu-id="3fac0-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="3fac0-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="3fac0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fac0-102">SYNOPSIS</span></span>
<span data-ttu-id="3fac0-103">Cria um novo usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3fac0-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fac0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fac0-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fac0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fac0-105">DESCRIPTION</span></span>
<span data-ttu-id="3fac0-106">Cria um novo usuário do Active Directory (conta corporativa/de estudante também conhecida conhecida como org-ID).</span><span class="sxs-lookup"><span data-stu-id="3fac0-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="3fac0-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="3fac0-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="3fac0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fac0-108">EXAMPLES</span></span>

### <span data-ttu-id="3fac0-109">Exemplo 1-criar um novo usuário do AD</span><span class="sxs-lookup"><span data-stu-id="3fac0-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="3fac0-110">Cria um novo usuário do AD com o nome "MyDisplayName" e o nome UPN myemail@domain.com do usuário "" em um locatário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="3fac0-111">OS</span><span class="sxs-lookup"><span data-stu-id="3fac0-111">PARAMETERS</span></span>

### <span data-ttu-id="3fac0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fac0-112">-DefaultProfile</span></span>
<span data-ttu-id="3fac0-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3fac0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fac0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3fac0-114">-DisplayName</span></span>
<span data-ttu-id="3fac0-115">O nome a ser exibido no catálogo de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="3fac0-116">exemplo ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="3fac0-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="3fac0-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="3fac0-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="3fac0-118">Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="3fac0-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="3fac0-119">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3fac0-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="3fac0-120">-Imutávelid</span><span class="sxs-lookup"><span data-stu-id="3fac0-120">-ImmutableId</span></span>
<span data-ttu-id="3fac0-121">Ele precisa ser especificado apenas se você estiver usando um domínio federado para a propriedade de nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="3fac0-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="3fac0-122">-MailNickname</span></span>
<span data-ttu-id="3fac0-123">O alias do email do usuário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="3fac0-124">-Senha</span><span class="sxs-lookup"><span data-stu-id="3fac0-124">-Password</span></span>
<span data-ttu-id="3fac0-125">Senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-125">Password for the user.</span></span>
<span data-ttu-id="3fac0-126">Ele deve atender aos requisitos de complexidade da senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="3fac0-127">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="3fac0-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="3fac0-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3fac0-128">-UserPrincipalName</span></span>
<span data-ttu-id="3fac0-129">O nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="3fac0-129">The user principal name.</span></span>
<span data-ttu-id="3fac0-130">Exemplo-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="3fac0-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="3fac0-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fac0-131">-Confirm</span></span>
<span data-ttu-id="3fac0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fac0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fac0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fac0-133">-WhatIf</span></span>
<span data-ttu-id="3fac0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fac0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fac0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fac0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fac0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fac0-136">CommonParameters</span></span>
<span data-ttu-id="3fac0-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fac0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fac0-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fac0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fac0-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fac0-139">INPUTS</span></span>

### <span data-ttu-id="3fac0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3fac0-140">System.String</span></span>

### <span data-ttu-id="3fac0-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3fac0-141">System.Security.SecureString</span></span>

### <span data-ttu-id="3fac0-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3fac0-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3fac0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fac0-143">OUTPUTS</span></span>

### <span data-ttu-id="3fac0-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="3fac0-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="3fac0-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fac0-145">NOTES</span></span>

## <span data-ttu-id="3fac0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fac0-146">RELATED LINKS</span></span>

[<span data-ttu-id="3fac0-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="3fac0-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



[<span data-ttu-id="3fac0-148">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="3fac0-148">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
