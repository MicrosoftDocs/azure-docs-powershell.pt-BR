---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f7ed4b70b3b0575b41f081e088e55944b46656aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773311"
---
# <span data-ttu-id="796e2-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="796e2-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="796e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="796e2-102">SYNOPSIS</span></span>
<span data-ttu-id="796e2-103">Exclui uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="796e2-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="796e2-104">A função a ser excluída é especificada usando-se a propriedade ID da função.</span><span class="sxs-lookup"><span data-stu-id="796e2-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="796e2-105">A exclusão falhará se houver atribuições de função existentes à função personalizada.</span><span class="sxs-lookup"><span data-stu-id="796e2-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="796e2-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="796e2-106">SYNTAX</span></span>

### <span data-ttu-id="796e2-107">RoleDefinitionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="796e2-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796e2-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="796e2-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796e2-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="796e2-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796e2-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="796e2-110">DESCRIPTION</span></span>
<span data-ttu-id="796e2-111">O cmdlet Remove-AzRoleDefinition exclui uma função personalizada no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="796e2-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="796e2-112">Forneça o parâmetro ID de uma função personalizada existente para excluir essa função personalizada.</span><span class="sxs-lookup"><span data-stu-id="796e2-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="796e2-113">Por padrão, Remove-AzRoleDefinition solicita que você confirme a confirmação.</span><span class="sxs-lookup"><span data-stu-id="796e2-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="796e2-114">Para suprimir o prompt, use o parâmetro Force.</span><span class="sxs-lookup"><span data-stu-id="796e2-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="796e2-115">Se houver atribuições de função feitas à função personalizada a serem excluídas, a exclusão falhará.</span><span class="sxs-lookup"><span data-stu-id="796e2-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="796e2-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="796e2-116">EXAMPLES</span></span>

### <span data-ttu-id="796e2-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="796e2-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="796e2-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="796e2-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="796e2-119">OS</span><span class="sxs-lookup"><span data-stu-id="796e2-119">PARAMETERS</span></span>

### <span data-ttu-id="796e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796e2-120">-DefaultProfile</span></span>
<span data-ttu-id="796e2-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="796e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="796e2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="796e2-122">-Force</span></span>
<span data-ttu-id="796e2-123">Se definido, não solicita uma confirmação antes de excluir a função personalizada</span><span class="sxs-lookup"><span data-stu-id="796e2-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="796e2-124">-ID</span><span class="sxs-lookup"><span data-stu-id="796e2-124">-Id</span></span>
<span data-ttu-id="796e2-125">ID da definição de função a ser excluída</span><span class="sxs-lookup"><span data-stu-id="796e2-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="796e2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="796e2-126">-InputObject</span></span>
<span data-ttu-id="796e2-127">O objeto que representa a definição de função a ser removida.</span><span class="sxs-lookup"><span data-stu-id="796e2-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="796e2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="796e2-128">-Name</span></span>
<span data-ttu-id="796e2-129">Nome da definição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="796e2-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="796e2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="796e2-130">-PassThru</span></span>
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

### <span data-ttu-id="796e2-131">-Escopo</span><span class="sxs-lookup"><span data-stu-id="796e2-131">-Scope</span></span>
<span data-ttu-id="796e2-132">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="796e2-132">Role definition scope.</span></span>

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

### <span data-ttu-id="796e2-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="796e2-133">-Confirm</span></span>
<span data-ttu-id="796e2-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="796e2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796e2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796e2-135">-WhatIf</span></span>
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

### <span data-ttu-id="796e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796e2-136">CommonParameters</span></span>
<span data-ttu-id="796e2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796e2-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796e2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796e2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="796e2-139">INPUTS</span></span>

### <span data-ttu-id="796e2-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="796e2-140">System.Guid</span></span>

### <span data-ttu-id="796e2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="796e2-141">System.String</span></span>

### <span data-ttu-id="796e2-142">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="796e2-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="796e2-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="796e2-143">OUTPUTS</span></span>

### <span data-ttu-id="796e2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="796e2-144">System.Boolean</span></span>

## <span data-ttu-id="796e2-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="796e2-145">NOTES</span></span>
<span data-ttu-id="796e2-146">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="796e2-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="796e2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="796e2-147">RELATED LINKS</span></span>

[<span data-ttu-id="796e2-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="796e2-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="796e2-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="796e2-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="796e2-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="796e2-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)
