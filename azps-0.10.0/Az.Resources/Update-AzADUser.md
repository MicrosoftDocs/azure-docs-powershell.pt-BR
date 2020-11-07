---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 2fe2162221672522596065ef615a8098bfc12a60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776294"
---
# <span data-ttu-id="15933-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="15933-101">Update-AzADUser</span></span>

## <span data-ttu-id="15933-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15933-102">SYNOPSIS</span></span>
<span data-ttu-id="15933-103">Atualiza um usuário existente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15933-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="15933-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15933-104">SYNTAX</span></span>

### <span data-ttu-id="15933-105">UPNOrObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="15933-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15933-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="15933-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15933-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15933-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15933-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15933-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15933-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15933-109">DESCRIPTION</span></span>
<span data-ttu-id="15933-110">Atualiza um usuário existente do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="15933-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="15933-111">Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="15933-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="15933-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15933-112">EXAMPLES</span></span>

### <span data-ttu-id="15933-113">Exemplo 1-atualize o nome de exibição de um usuário usando a ID do objeto</span><span class="sxs-lookup"><span data-stu-id="15933-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="15933-114">Atualiza o nome de exibição do usuário com a ID de objeto ' 155a5c10-93A9-4941-a0df-96d83ab5ab24 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="15933-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="15933-115">Exemplo 2-Atualize o nome de exibição de um usuário usando o nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="15933-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="15933-116">Atualiza o nome de exibição do usuário com o nome de usuário principal ' foo@domain.com ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="15933-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="15933-117">Exemplo 3-atualize o nome de exibição de um usuário usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="15933-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="15933-118">Obtém o usuário com a ID de objeto ' 155a5c10-93A9-4941-a0df-96d83ab5ab24 ' e canaliza-se para o cmdlet Update-AzADUser para atualizar o nome de exibição do usuário para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="15933-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="15933-119">OS</span><span class="sxs-lookup"><span data-stu-id="15933-119">PARAMETERS</span></span>

### <span data-ttu-id="15933-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15933-120">-DefaultProfile</span></span>
<span data-ttu-id="15933-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15933-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15933-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15933-122">-DisplayName</span></span>
<span data-ttu-id="15933-123">Novo nome de exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="15933-123">New display name for the user.</span></span>

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

### <span data-ttu-id="15933-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="15933-124">-EnableAccount</span></span>
<span data-ttu-id="15933-125">verdadeiro para habilitar a conta; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="15933-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="15933-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="15933-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="15933-127">Ele deve ser especificado se o usuário deve alterar a senha no próximo logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="15933-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="15933-128">Válido somente se senha for atualizado, caso contrário, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="15933-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="15933-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15933-129">-InputObject</span></span>
<span data-ttu-id="15933-130">O objeto que representa o usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="15933-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="15933-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15933-131">-ObjectId</span></span>
<span data-ttu-id="15933-132">A ID de objeto do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="15933-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="15933-133">-Senha</span><span class="sxs-lookup"><span data-stu-id="15933-133">-Password</span></span>
<span data-ttu-id="15933-134">Nova senha para o usuário.</span><span class="sxs-lookup"><span data-stu-id="15933-134">New password for the user.</span></span>

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

### <span data-ttu-id="15933-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="15933-135">-UPNOrObjectId</span></span>
<span data-ttu-id="15933-136">O nome UPN ou a ID do objeto do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="15933-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="15933-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="15933-137">-UserPrincipalName</span></span>
<span data-ttu-id="15933-138">O nome UPN do usuário a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="15933-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="15933-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15933-139">-Confirm</span></span>
<span data-ttu-id="15933-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15933-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15933-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15933-141">-WhatIf</span></span>
<span data-ttu-id="15933-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15933-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15933-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15933-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15933-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15933-144">CommonParameters</span></span>
<span data-ttu-id="15933-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15933-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15933-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15933-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15933-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15933-147">INPUTS</span></span>

### <span data-ttu-id="15933-148">System. String</span><span class="sxs-lookup"><span data-stu-id="15933-148">System.String</span></span>

### <span data-ttu-id="15933-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="15933-149">System.Guid</span></span>

### <span data-ttu-id="15933-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="15933-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="15933-151">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15933-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="15933-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="15933-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="15933-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="15933-153">System.Security.SecureString</span></span>

## <span data-ttu-id="15933-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15933-154">OUTPUTS</span></span>

### <span data-ttu-id="15933-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="15933-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="15933-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15933-156">NOTES</span></span>

## <span data-ttu-id="15933-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15933-157">RELATED LINKS</span></span>
