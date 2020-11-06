---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426619"
---
# <span data-ttu-id="2af7b-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="2af7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2af7b-102">SYNOPSIS</span></span>
<span data-ttu-id="2af7b-103">Atualiza um usuário existente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2af7b-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2af7b-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2af7b-105">DESCRIPTION</span></span>
<span data-ttu-id="2af7b-106">Atualiza um usuário existente do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="2af7b-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="2af7b-107">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="2af7b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2af7b-108">EXAMPLES</span></span>

### <span data-ttu-id="2af7b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2af7b-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2af7b-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="2af7b-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="2af7b-111">OS</span><span class="sxs-lookup"><span data-stu-id="2af7b-111">PARAMETERS</span></span>

### <span data-ttu-id="2af7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af7b-112">-DefaultProfile</span></span>
<span data-ttu-id="2af7b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2af7b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2af7b-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2af7b-114">-DisplayName</span></span>
<span data-ttu-id="2af7b-115">Novo nome para exibir no catálogo de endereços do usuário.</span><span class="sxs-lookup"><span data-stu-id="2af7b-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="2af7b-116">Exemplo-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="2af7b-116">Example-'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="2af7b-117">-EnableAccount</span></span>
<span data-ttu-id="2af7b-118">Verdadeiro para habilitar a conta; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="2af7b-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="2af7b-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="2af7b-120">Ele deve ser especificado somente quando você estiver atualizando a senha.</span><span class="sxs-lookup"><span data-stu-id="2af7b-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="2af7b-121">Caso contrário, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="2af7b-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="2af7b-122">Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).</span><span class="sxs-lookup"><span data-stu-id="2af7b-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="2af7b-123">O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2af7b-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-124">-Senha</span><span class="sxs-lookup"><span data-stu-id="2af7b-124">-Password</span></span>
<span data-ttu-id="2af7b-125">Nova senha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2af7b-125">New password for the user.</span></span>
<span data-ttu-id="2af7b-126">Ele deve atender aos requisitos de complexidade da senha do locatário.</span><span class="sxs-lookup"><span data-stu-id="2af7b-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="2af7b-127">É recomendável definir uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="2af7b-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="2af7b-128">-UPNOrObjectId</span></span>
<span data-ttu-id="2af7b-129">O nome UPN do usuário (por exemplo, ' someuser@contoso.com ') ou o ObjectID do usuário para o qual as propriedades precisam ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="2af7b-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2af7b-130">-Confirm</span></span>
<span data-ttu-id="2af7b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af7b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af7b-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af7b-133">CommonParameters</span></span>
<span data-ttu-id="2af7b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2af7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af7b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af7b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af7b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2af7b-136">INPUTS</span></span>

### <span data-ttu-id="2af7b-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2af7b-137">None</span></span>
<span data-ttu-id="2af7b-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2af7b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2af7b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2af7b-139">OUTPUTS</span></span>

### <span data-ttu-id="2af7b-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="2af7b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2af7b-141">NOTES</span></span>

## <span data-ttu-id="2af7b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2af7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="2af7b-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="2af7b-144">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="2af7b-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2af7b-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

