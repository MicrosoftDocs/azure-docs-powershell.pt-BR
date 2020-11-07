---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 091f54b69cd713d93def4c727181f9c8e7d5b0d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776358"
---
# <span data-ttu-id="4eba5-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4eba5-101">Remove-AzADUser</span></span>

## <span data-ttu-id="4eba5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4eba5-102">SYNOPSIS</span></span>
<span data-ttu-id="4eba5-103">Exclui um usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4eba5-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="4eba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4eba5-104">SYNTAX</span></span>

### <span data-ttu-id="4eba5-105">UPNOrObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4eba5-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eba5-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eba5-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eba5-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eba5-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eba5-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eba5-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eba5-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eba5-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eba5-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4eba5-110">DESCRIPTION</span></span>
<span data-ttu-id="4eba5-111">Exclui um usuário do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).</span><span class="sxs-lookup"><span data-stu-id="4eba5-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4eba5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eba5-112">EXAMPLES</span></span>

### <span data-ttu-id="4eba5-113">Exemplo 1-remover um usuário pelo nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="4eba5-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="4eba5-114">Remove o usuário com o nome de usuário principal " foo@domain.com " do locatário.</span><span class="sxs-lookup"><span data-stu-id="4eba5-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="4eba5-115">Exemplo 2-remover um usuário por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="4eba5-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="4eba5-116">Remove o usuário com a ID de objeto ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' do locatário.</span><span class="sxs-lookup"><span data-stu-id="4eba5-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="4eba5-117">Exemplo 3-remover um usuário por meio do encanamento</span><span class="sxs-lookup"><span data-stu-id="4eba5-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="4eba5-118">Obtém o usuário com a ID de objeto ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' e canaliza-se para o cmdlet Remove-AzADUser para remover o usuário do locatário.</span><span class="sxs-lookup"><span data-stu-id="4eba5-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="4eba5-119">OS</span><span class="sxs-lookup"><span data-stu-id="4eba5-119">PARAMETERS</span></span>

### <span data-ttu-id="4eba5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eba5-120">-DefaultProfile</span></span>
<span data-ttu-id="4eba5-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4eba5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eba5-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4eba5-122">-DisplayName</span></span>
<span data-ttu-id="4eba5-123">O nome de exibição do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4eba5-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eba5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4eba5-124">-Force</span></span>
<span data-ttu-id="4eba5-125">Se especificado, não solicita confirmação para excluir o usuário.</span><span class="sxs-lookup"><span data-stu-id="4eba5-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="4eba5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eba5-126">-InputObject</span></span>
<span data-ttu-id="4eba5-127">O objeto de usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4eba5-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="4eba5-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4eba5-128">-ObjectId</span></span>
<span data-ttu-id="4eba5-129">A ID de objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4eba5-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="4eba5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eba5-130">-PassThru</span></span>
<span data-ttu-id="4eba5-131">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4eba5-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4eba5-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4eba5-132">-UPNOrObjectId</span></span>
<span data-ttu-id="4eba5-133">O nome principal do usuário ou o objectId do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4eba5-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="4eba5-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4eba5-134">-UserPrincipalName</span></span>
<span data-ttu-id="4eba5-135">O nome UPN do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4eba5-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="4eba5-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4eba5-136">-Confirm</span></span>
<span data-ttu-id="4eba5-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eba5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eba5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eba5-138">-WhatIf</span></span>
<span data-ttu-id="4eba5-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4eba5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eba5-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4eba5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eba5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eba5-141">CommonParameters</span></span>
<span data-ttu-id="4eba5-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eba5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eba5-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eba5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eba5-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4eba5-144">INPUTS</span></span>

### <span data-ttu-id="4eba5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4eba5-145">System.String</span></span>

### <span data-ttu-id="4eba5-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4eba5-146">System.Guid</span></span>

### <span data-ttu-id="4eba5-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="4eba5-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="4eba5-148">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4eba5-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4eba5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4eba5-149">OUTPUTS</span></span>

### <span data-ttu-id="4eba5-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4eba5-150">System.Boolean</span></span>

## <span data-ttu-id="4eba5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4eba5-151">NOTES</span></span>

## <span data-ttu-id="4eba5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eba5-152">RELATED LINKS</span></span>

[<span data-ttu-id="4eba5-153">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4eba5-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="4eba5-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4eba5-154">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="4eba5-155">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4eba5-155">Set-AzADUser</span></span>](./Set-AzADUser.md)

