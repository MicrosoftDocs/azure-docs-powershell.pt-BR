---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: e16adfe6db006af0c1f49992d5aff39412d4d4d3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398199"
---
# <span data-ttu-id="5bbe4-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5bbe4-101">Remove-AzADUser</span></span>

## <span data-ttu-id="5bbe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbe4-103">Exclui um usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="5bbe4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bbe4-104">SYNTAX</span></span>

### <span data-ttu-id="5bbe4-105">UPNOrObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5bbe4-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbe4-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bbe4-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbe4-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bbe4-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbe4-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bbe4-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbe4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bbe4-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bbe4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bbe4-110">DESCRIPTION</span></span>
<span data-ttu-id="5bbe4-111">Exclui um usuário do Active Directory (conta de trabalho/escola também conhecida popularmente como id da organização).</span><span class="sxs-lookup"><span data-stu-id="5bbe4-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="5bbe4-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bbe4-112">EXAMPLES</span></span>

### <span data-ttu-id="5bbe4-113">Exemplo 1 - Remover um usuário por nome de entidade de usuário</span><span class="sxs-lookup"><span data-stu-id="5bbe4-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="5bbe4-114">Remove o usuário com o nome de usuário principal " foo@domain.com " do locatário.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="5bbe4-115">Exemplo 2 - Remover um usuário por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="5bbe4-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="5bbe4-116">Remove o usuário com a ID do objeto '7a9582cf-88c4-4319-842b-7a5d60967a69' do locatário.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="5bbe4-117">Exemplo 3 - Remover um usuário por piping</span><span class="sxs-lookup"><span data-stu-id="5bbe4-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="5bbe4-118">Obtém o usuário com a ID do objeto '7a9582cf-88c4-4319-842b-7a5d60967a69' e os canos no cmdlet Remove-AzADUser para remover o usuário do locatário.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="5bbe4-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bbe4-119">PARAMETERS</span></span>

### <span data-ttu-id="5bbe4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbe4-120">-DefaultProfile</span></span>
<span data-ttu-id="5bbe4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5bbe4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bbe4-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5bbe4-122">-DisplayName</span></span>
<span data-ttu-id="5bbe4-123">O nome de exibição do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="5bbe4-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5bbe4-124">-Force</span></span>
<span data-ttu-id="5bbe4-125">Se especificado, não solicita confirmação para excluir o usuário.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="5bbe4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bbe4-126">-InputObject</span></span>
<span data-ttu-id="5bbe4-127">O objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="5bbe4-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5bbe4-128">-ObjectId</span></span>
<span data-ttu-id="5bbe4-129">A ID do objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="5bbe4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bbe4-130">-PassThru</span></span>
<span data-ttu-id="5bbe4-131">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5bbe4-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="5bbe4-132">-UPNOrObjectId</span></span>
<span data-ttu-id="5bbe4-133">O nome principal do usuário ou a ID do objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="5bbe4-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5bbe4-134">-UserPrincipalName</span></span>
<span data-ttu-id="5bbe4-135">O nome principal do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="5bbe4-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5bbe4-136">-Confirm</span></span>
<span data-ttu-id="5bbe4-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bbe4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bbe4-138">-WhatIf</span></span>
<span data-ttu-id="5bbe4-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bbe4-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bbe4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbe4-141">CommonParameters</span></span>
<span data-ttu-id="5bbe4-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bbe4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbe4-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbe4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbe4-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="5bbe4-144">INPUTS</span></span>

### <span data-ttu-id="5bbe4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5bbe4-145">System.String</span></span>

### <span data-ttu-id="5bbe4-146">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5bbe4-146">System.Guid</span></span>

### <span data-ttu-id="5bbe4-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="5bbe4-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="5bbe4-148">Parâmetros: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5bbe4-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5bbe4-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="5bbe4-149">OUTPUTS</span></span>

### <span data-ttu-id="5bbe4-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bbe4-150">System.Boolean</span></span>

## <span data-ttu-id="5bbe4-151">Notas</span><span class="sxs-lookup"><span data-stu-id="5bbe4-151">NOTES</span></span>

## <span data-ttu-id="5bbe4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bbe4-152">RELATED LINKS</span></span>

[<span data-ttu-id="5bbe4-153">Novo-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5bbe4-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="5bbe4-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5bbe4-154">Get-AzADUser</span></span>](./Get-AzADUser.md)


