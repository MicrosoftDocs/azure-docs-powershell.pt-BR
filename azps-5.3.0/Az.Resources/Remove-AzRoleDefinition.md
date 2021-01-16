---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271255"
---
# <span data-ttu-id="4302e-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4302e-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="4302e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4302e-102">SYNOPSIS</span></span>
<span data-ttu-id="4302e-103">Exclui uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="4302e-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="4302e-104">A função a ser excluída é especificada usando-se a propriedade ID da função.</span><span class="sxs-lookup"><span data-stu-id="4302e-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="4302e-105">A exclusão falhará se houver atribuições de função existentes à função personalizada.</span><span class="sxs-lookup"><span data-stu-id="4302e-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="4302e-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4302e-106">SYNTAX</span></span>

### <span data-ttu-id="4302e-107">RoleDefinitionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4302e-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4302e-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4302e-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4302e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4302e-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4302e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4302e-110">DESCRIPTION</span></span>
<span data-ttu-id="4302e-111">O cmdlet Remove-AzRoleDefinition exclui uma função personalizada no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="4302e-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="4302e-112">Forneça o parâmetro ID de uma função personalizada existente para excluir essa função personalizada.</span><span class="sxs-lookup"><span data-stu-id="4302e-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="4302e-113">Por padrão, Remove-AzRoleDefinition solicita que você confirme a confirmação.</span><span class="sxs-lookup"><span data-stu-id="4302e-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="4302e-114">Para suprimir o prompt, use o parâmetro Force.</span><span class="sxs-lookup"><span data-stu-id="4302e-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="4302e-115">Se houver atribuições de função feitas à função personalizada a serem excluídas, a exclusão falhará.</span><span class="sxs-lookup"><span data-stu-id="4302e-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="4302e-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4302e-116">EXAMPLES</span></span>

### <span data-ttu-id="4302e-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4302e-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="4302e-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4302e-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="4302e-119">OS</span><span class="sxs-lookup"><span data-stu-id="4302e-119">PARAMETERS</span></span>

### <span data-ttu-id="4302e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4302e-120">-DefaultProfile</span></span>
<span data-ttu-id="4302e-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4302e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4302e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4302e-122">-Force</span></span>
<span data-ttu-id="4302e-123">Se definido, não solicita uma confirmação antes de excluir a função personalizada</span><span class="sxs-lookup"><span data-stu-id="4302e-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="4302e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="4302e-124">-Id</span></span>
<span data-ttu-id="4302e-125">ID da definição de função a ser excluída</span><span class="sxs-lookup"><span data-stu-id="4302e-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="4302e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4302e-126">-InputObject</span></span>
<span data-ttu-id="4302e-127">O objeto que representa a definição de função a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4302e-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="4302e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4302e-128">-Name</span></span>
<span data-ttu-id="4302e-129">Nome da definição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="4302e-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="4302e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4302e-130">-PassThru</span></span>
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

### <span data-ttu-id="4302e-131">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4302e-131">-Scope</span></span>
<span data-ttu-id="4302e-132">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="4302e-132">Role definition scope.</span></span>

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

### <span data-ttu-id="4302e-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4302e-133">-Confirm</span></span>
<span data-ttu-id="4302e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4302e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4302e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4302e-135">-WhatIf</span></span>
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

### <span data-ttu-id="4302e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4302e-136">CommonParameters</span></span>
<span data-ttu-id="4302e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4302e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4302e-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4302e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4302e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4302e-139">INPUTS</span></span>

### <span data-ttu-id="4302e-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4302e-140">System.Guid</span></span>

### <span data-ttu-id="4302e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4302e-141">System.String</span></span>

### <span data-ttu-id="4302e-142">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4302e-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="4302e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4302e-143">OUTPUTS</span></span>

### <span data-ttu-id="4302e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4302e-144">System.Boolean</span></span>

## <span data-ttu-id="4302e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4302e-145">NOTES</span></span>
<span data-ttu-id="4302e-146">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="4302e-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4302e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4302e-147">RELATED LINKS</span></span>

[<span data-ttu-id="4302e-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4302e-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="4302e-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4302e-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="4302e-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4302e-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

