---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602195"
---
# <span data-ttu-id="eead6-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="eead6-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="eead6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eead6-102">SYNOPSIS</span></span>
<span data-ttu-id="eead6-103">Atualiza um usuário existente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eead6-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eead6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eead6-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eead6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eead6-105">DESCRIPTION</span></span>
<span data-ttu-id="eead6-106">Atualiza um usuário existente do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="eead6-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="eead6-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="eead6-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="eead6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eead6-108">EXAMPLES</span></span>

### <span data-ttu-id="eead6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eead6-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="eead6-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="eead6-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="eead6-111">OS</span><span class="sxs-lookup"><span data-stu-id="eead6-111">PARAMETERS</span></span>

### <span data-ttu-id="eead6-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eead6-112">-DisplayName</span></span>
<span data-ttu-id="eead6-113">Novo nome para exibir no catálogo de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="eead6-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="eead6-114">Exemplo-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="eead6-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="eead6-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="eead6-115">-EnableAccount</span></span>
<span data-ttu-id="eead6-116">Verdadeiro para habilitar a conta; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="eead6-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eead6-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="eead6-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="eead6-118">Ele deve ser especificado somente quando você estiver atualizando a senha.</span><span class="sxs-lookup"><span data-stu-id="eead6-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="eead6-119">Caso contrário, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="eead6-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="eead6-120">Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="eead6-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="eead6-121">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="eead6-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="eead6-122">-Senha</span><span class="sxs-lookup"><span data-stu-id="eead6-122">-Password</span></span>
<span data-ttu-id="eead6-123">Nova senha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="eead6-123">New password for the user.</span></span>
<span data-ttu-id="eead6-124">Ele deve atender aos requisitos de complexidade da senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="eead6-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="eead6-125">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="eead6-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="eead6-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="eead6-126">-UPNOrObjectId</span></span>
<span data-ttu-id="eead6-127">O nome UPN do usuário (por exemplo, ' someuser@contoso.com ') ou o ObjectID do usuário para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="eead6-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="eead6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eead6-128">-Confirm</span></span>
<span data-ttu-id="eead6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eead6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eead6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eead6-130">-WhatIf</span></span>
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

### <span data-ttu-id="eead6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eead6-131">-DefaultProfile</span></span>
<span data-ttu-id="eead6-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eead6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eead6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eead6-133">CommonParameters</span></span>
<span data-ttu-id="eead6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eead6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eead6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eead6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eead6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eead6-136">INPUTS</span></span>

## <span data-ttu-id="eead6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eead6-137">OUTPUTS</span></span>

### <span data-ttu-id="eead6-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="eead6-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="eead6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eead6-139">NOTES</span></span>

## <span data-ttu-id="eead6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eead6-140">RELATED LINKS</span></span>

[<span data-ttu-id="eead6-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="eead6-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="eead6-142">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="eead6-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="eead6-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="eead6-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

