---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 8799450cc73784b45804ea1fa26785716a895bed
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399576"
---
# <span data-ttu-id="4032d-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4032d-101">Remove-AzADUser</span></span>

## <span data-ttu-id="4032d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4032d-102">SYNOPSIS</span></span>
<span data-ttu-id="4032d-103">Exclui um usuário do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4032d-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="4032d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4032d-104">SYNTAX</span></span>

### <span data-ttu-id="4032d-105">UPNOrObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4032d-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4032d-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4032d-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4032d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4032d-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4032d-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4032d-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4032d-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4032d-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4032d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4032d-110">DESCRIPTION</span></span>
<span data-ttu-id="4032d-111">Exclui um usuário do Active Directory (conta de trabalho/escola também conhecida popularmente como id da organização).</span><span class="sxs-lookup"><span data-stu-id="4032d-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4032d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4032d-112">EXAMPLES</span></span>

### <span data-ttu-id="4032d-113">Exemplo 1 - Remover um usuário por nome de entidade de usuário</span><span class="sxs-lookup"><span data-stu-id="4032d-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="4032d-114">Remove o usuário com o nome de usuário principal " foo@domain.com " do locatário.</span><span class="sxs-lookup"><span data-stu-id="4032d-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="4032d-115">Exemplo 2 - Remover um usuário por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="4032d-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="4032d-116">Remove o usuário com a ID do objeto '7a9582cf-88c4-4319-842b-7a5d60967a69' do locatário.</span><span class="sxs-lookup"><span data-stu-id="4032d-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="4032d-117">Exemplo 3 - Remover um usuário por piping</span><span class="sxs-lookup"><span data-stu-id="4032d-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="4032d-118">Obtém o usuário com a ID do objeto '7a9582cf-88c4-4319-842b-7a5d60967a69' e os canos no cmdlet Remove-AzADUser para remover o usuário do locatário.</span><span class="sxs-lookup"><span data-stu-id="4032d-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="4032d-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4032d-119">PARAMETERS</span></span>

### <span data-ttu-id="4032d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4032d-120">-DefaultProfile</span></span>
<span data-ttu-id="4032d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4032d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4032d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4032d-122">-DisplayName</span></span>
<span data-ttu-id="4032d-123">O nome de exibição do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4032d-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="4032d-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4032d-124">-Force</span></span>
<span data-ttu-id="4032d-125">Se especificado, não solicita confirmação para excluir o usuário.</span><span class="sxs-lookup"><span data-stu-id="4032d-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="4032d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4032d-126">-InputObject</span></span>
<span data-ttu-id="4032d-127">O objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4032d-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4032d-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4032d-128">-ObjectId</span></span>
<span data-ttu-id="4032d-129">A ID do objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4032d-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4032d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4032d-130">-PassThru</span></span>
<span data-ttu-id="4032d-131">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4032d-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4032d-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4032d-132">-UPNOrObjectId</span></span>
<span data-ttu-id="4032d-133">O nome principal do usuário ou a ID do objeto do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4032d-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="4032d-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4032d-134">-UserPrincipalName</span></span>
<span data-ttu-id="4032d-135">O nome principal do usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4032d-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="4032d-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4032d-136">-Confirm</span></span>
<span data-ttu-id="4032d-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4032d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4032d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4032d-138">-WhatIf</span></span>
<span data-ttu-id="4032d-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4032d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4032d-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4032d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4032d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4032d-141">CommonParameters</span></span>
<span data-ttu-id="4032d-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4032d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4032d-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4032d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4032d-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="4032d-144">INPUTS</span></span>

### <span data-ttu-id="4032d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4032d-145">System.String</span></span>

### <span data-ttu-id="4032d-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="4032d-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="4032d-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="4032d-147">OUTPUTS</span></span>

### <span data-ttu-id="4032d-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4032d-148">System.Boolean</span></span>

## <span data-ttu-id="4032d-149">Notas</span><span class="sxs-lookup"><span data-stu-id="4032d-149">NOTES</span></span>

## <span data-ttu-id="4032d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4032d-150">RELATED LINKS</span></span>

[<span data-ttu-id="4032d-151">Novo-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4032d-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="4032d-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4032d-152">Get-AzADUser</span></span>](./Get-AzADUser.md)


