---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
ms.openlocfilehash: a07d9119d5e83c92d96ab22e98125459945f786b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429358"
---
# <span data-ttu-id="e493c-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e493c-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="e493c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e493c-102">SYNOPSIS</span></span>
<span data-ttu-id="e493c-103">Atualiza um usuário existente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e493c-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e493c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e493c-104">SYNTAX</span></span>

### <span data-ttu-id="e493c-105">UPNOrObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e493c-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e493c-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e493c-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e493c-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e493c-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e493c-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e493c-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e493c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e493c-109">DESCRIPTION</span></span>
<span data-ttu-id="e493c-110">Atualiza um usuário existente do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="e493c-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="e493c-111">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="e493c-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="e493c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e493c-112">EXAMPLES</span></span>

### <span data-ttu-id="e493c-113">Exemplo 1-atualize o nome de exibição de um usuário usando a ID do objeto</span><span class="sxs-lookup"><span data-stu-id="e493c-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e493c-114">Atualiza o nome de exibição do usuário com a ID de objeto ' 155a5c10-93A9-4941-a0df-96d83ab5ab24 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="e493c-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e493c-115">Exemplo 2-Atualize o nome de exibição de um usuário usando o nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="e493c-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="e493c-116">Atualiza o nome de exibição do usuário com o nome de usuário principal ' foo@domain.com ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="e493c-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e493c-117">Exemplo 3-atualize o nome de exibição de um usuário usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="e493c-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="e493c-118">Obtém o usuário com a ID de objeto ' 155a5c10-93A9-4941-a0df-96d83ab5ab24 ' e canaliza-se para o cmdlet Update-AzureRmADUser para atualizar o nome de exibição do usuário para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="e493c-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="e493c-119">OS</span><span class="sxs-lookup"><span data-stu-id="e493c-119">PARAMETERS</span></span>

### <span data-ttu-id="e493c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e493c-120">-DefaultProfile</span></span>
<span data-ttu-id="e493c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e493c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e493c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e493c-122">-DisplayName</span></span>
<span data-ttu-id="e493c-123">Novo nome de exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e493c-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="e493c-124">-EnableAccount</span></span>
<span data-ttu-id="e493c-125">verdadeiro para habilitar a conta; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="e493c-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="e493c-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="e493c-127">Ele deve ser especificado se o usuário deve alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e493c-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="e493c-128">Válido somente se senha for atualizado, caso contrário, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e493c-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="e493c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e493c-129">-InputObject</span></span>
<span data-ttu-id="e493c-130">O objeto que representa o usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e493c-130">The object representing the user to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e493c-131">-ObjectId</span></span>
<span data-ttu-id="e493c-132">A ID de objeto do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e493c-132">The object id of the user to be updated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-133">-Senha</span><span class="sxs-lookup"><span data-stu-id="e493c-133">-Password</span></span>
<span data-ttu-id="e493c-134">Nova senha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e493c-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="e493c-135">-UPNOrObjectId</span></span>
<span data-ttu-id="e493c-136">O nome UPN ou a ID do objeto do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e493c-136">The user principal name or object id of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e493c-137">-UserPrincipalName</span></span>
<span data-ttu-id="e493c-138">O nome UPN do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e493c-138">The user principal name of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e493c-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e493c-139">-Confirm</span></span>
<span data-ttu-id="e493c-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e493c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e493c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e493c-141">-WhatIf</span></span>
<span data-ttu-id="e493c-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e493c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e493c-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e493c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e493c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e493c-144">CommonParameters</span></span>
<span data-ttu-id="e493c-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e493c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e493c-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e493c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e493c-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e493c-147">INPUTS</span></span>

### <span data-ttu-id="e493c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e493c-148">System.String</span></span>

### <span data-ttu-id="e493c-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e493c-149">System.Guid</span></span>

### <span data-ttu-id="e493c-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e493c-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="e493c-151">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e493c-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e493c-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e493c-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e493c-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e493c-153">System.Security.SecureString</span></span>

## <span data-ttu-id="e493c-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e493c-154">OUTPUTS</span></span>

### <span data-ttu-id="e493c-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e493c-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="e493c-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e493c-156">NOTES</span></span>

## <span data-ttu-id="e493c-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e493c-157">RELATED LINKS</span></span>
