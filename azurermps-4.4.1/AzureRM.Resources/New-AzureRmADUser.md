---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440959"
---
# <span data-ttu-id="6dd78-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="6dd78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dd78-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd78-103">Cria um novo usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6dd78-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dd78-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dd78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6dd78-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd78-106">Cria um novo usuário do Active Directory (conta corporativa/de estudante também conhecida conhecida como org-ID).</span><span class="sxs-lookup"><span data-stu-id="6dd78-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="6dd78-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="6dd78-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dd78-108">EXAMPLES</span></span>

### <span data-ttu-id="6dd78-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dd78-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6dd78-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="6dd78-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="6dd78-111">OS</span><span class="sxs-lookup"><span data-stu-id="6dd78-111">PARAMETERS</span></span>

### <span data-ttu-id="6dd78-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6dd78-112">-DisplayName</span></span>
<span data-ttu-id="6dd78-113">O nome a ser exibido no catálogo de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="6dd78-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="6dd78-114">exemplo ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="6dd78-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="6dd78-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="6dd78-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="6dd78-116">Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="6dd78-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="6dd78-117">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6dd78-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="6dd78-118">-Imutávelid</span><span class="sxs-lookup"><span data-stu-id="6dd78-118">-ImmutableId</span></span>
<span data-ttu-id="6dd78-119">Ele precisa ser especificado apenas se você estiver usando um domínio federado para a propriedade de nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="6dd78-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="6dd78-120">-Senha</span><span class="sxs-lookup"><span data-stu-id="6dd78-120">-Password</span></span>
<span data-ttu-id="6dd78-121">Senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="6dd78-121">Password for the user.</span></span>
<span data-ttu-id="6dd78-122">Ele deve atender aos requisitos de complexidade da senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="6dd78-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="6dd78-123">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="6dd78-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="6dd78-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6dd78-124">-UserPrincipalName</span></span>
<span data-ttu-id="6dd78-125">O nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="6dd78-125">The user principal name.</span></span>
<span data-ttu-id="6dd78-126">Exemplo-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="6dd78-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="6dd78-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6dd78-127">-Confirm</span></span>
<span data-ttu-id="6dd78-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd78-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd78-129">-WhatIf</span></span>
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

### <span data-ttu-id="6dd78-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd78-130">-DefaultProfile</span></span>
<span data-ttu-id="6dd78-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd78-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dd78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd78-132">CommonParameters</span></span>
<span data-ttu-id="6dd78-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd78-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd78-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6dd78-135">INPUTS</span></span>

## <span data-ttu-id="6dd78-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6dd78-136">OUTPUTS</span></span>

### <span data-ttu-id="6dd78-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6dd78-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6dd78-138">NOTES</span></span>

## <span data-ttu-id="6dd78-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dd78-139">RELATED LINKS</span></span>

[<span data-ttu-id="6dd78-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="6dd78-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="6dd78-142">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6dd78-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
