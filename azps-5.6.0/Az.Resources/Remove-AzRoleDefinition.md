---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: d4ce9ef88f7043a369d8e566de75651944ea1e88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901438"
---
# <span data-ttu-id="b43e4-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b43e4-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="b43e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b43e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b43e4-103">Exclui uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b43e4-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b43e4-104">A função a ser excluída é especificada usando a propriedade Id da função.</span><span class="sxs-lookup"><span data-stu-id="b43e4-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="b43e4-105">A exclusão falhará se houver atribuições de função existentes feitas à função personalizada.</span><span class="sxs-lookup"><span data-stu-id="b43e4-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="b43e4-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b43e4-106">SYNTAX</span></span>

### <span data-ttu-id="b43e4-107">RoleDefinitionIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b43e4-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43e4-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b43e4-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43e4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b43e4-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b43e4-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b43e4-110">DESCRIPTION</span></span>
<span data-ttu-id="b43e4-111">O cmdlet Remove-AzRoleDefinition exclui uma função personalizada no Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="b43e4-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b43e4-112">Forneça o parâmetro Id de uma função personalizada existente para excluir essa função personalizada.</span><span class="sxs-lookup"><span data-stu-id="b43e4-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="b43e4-113">Por padrão, Remove-AzRoleDefinition solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="b43e4-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="b43e4-114">Para suprimir o prompt, use o parâmetro Force.</span><span class="sxs-lookup"><span data-stu-id="b43e4-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="b43e4-115">Se houver atribuições de função existentes feitas à função personalizada a serem excluídas, a exclusão falhará.</span><span class="sxs-lookup"><span data-stu-id="b43e4-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="b43e4-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b43e4-116">EXAMPLES</span></span>

### <span data-ttu-id="b43e4-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b43e4-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="b43e4-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b43e4-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="b43e4-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b43e4-119">PARAMETERS</span></span>

### <span data-ttu-id="b43e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43e4-120">-DefaultProfile</span></span>
<span data-ttu-id="b43e4-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b43e4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43e4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b43e4-122">-Force</span></span>
<span data-ttu-id="b43e4-123">Se definido, não solicita uma confirmação antes de excluir a função personalizada</span><span class="sxs-lookup"><span data-stu-id="b43e4-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="b43e4-124">-Id</span><span class="sxs-lookup"><span data-stu-id="b43e4-124">-Id</span></span>
<span data-ttu-id="b43e4-125">ID da definição de função a ser excluída</span><span class="sxs-lookup"><span data-stu-id="b43e4-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43e4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b43e4-126">-InputObject</span></span>
<span data-ttu-id="b43e4-127">O objeto que representa a definição de função a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b43e4-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b43e4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b43e4-128">-Name</span></span>
<span data-ttu-id="b43e4-129">Nome da definição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="b43e4-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43e4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b43e4-130">-PassThru</span></span>
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

### <span data-ttu-id="b43e4-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="b43e4-131">-Scope</span></span>
<span data-ttu-id="b43e4-132">Escopo de definição de função.</span><span class="sxs-lookup"><span data-stu-id="b43e4-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43e4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b43e4-133">-Confirm</span></span>
<span data-ttu-id="b43e4-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43e4-135">-WhatIf</span></span>
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

### <span data-ttu-id="b43e4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43e4-136">CommonParameters</span></span>
<span data-ttu-id="b43e4-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43e4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43e4-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b43e4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43e4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b43e4-139">INPUTS</span></span>

### <span data-ttu-id="b43e4-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b43e4-140">System.Guid</span></span>

### <span data-ttu-id="b43e4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b43e4-141">System.String</span></span>

### <span data-ttu-id="b43e4-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b43e4-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b43e4-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b43e4-143">OUTPUTS</span></span>

### <span data-ttu-id="b43e4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b43e4-144">System.Boolean</span></span>

## <span data-ttu-id="b43e4-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="b43e4-145">NOTES</span></span>
<span data-ttu-id="b43e4-146">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="b43e4-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b43e4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b43e4-147">RELATED LINKS</span></span>

[<span data-ttu-id="b43e4-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b43e4-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="b43e4-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b43e4-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="b43e4-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b43e4-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

