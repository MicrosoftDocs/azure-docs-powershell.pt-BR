---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786048"
---
# <span data-ttu-id="6261d-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6261d-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="6261d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6261d-102">SYNOPSIS</span></span>
<span data-ttu-id="6261d-103">Exclui uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="6261d-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="6261d-104">A função a ser excluída é especificada usando-se a propriedade ID da função.</span><span class="sxs-lookup"><span data-stu-id="6261d-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="6261d-105">A exclusão falhará se houver atribuições de função existentes à função personalizada.</span><span class="sxs-lookup"><span data-stu-id="6261d-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6261d-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6261d-106">SYNTAX</span></span>

### <span data-ttu-id="6261d-107">RoleDefinitionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6261d-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6261d-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6261d-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6261d-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6261d-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6261d-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6261d-110">DESCRIPTION</span></span>
<span data-ttu-id="6261d-111">O cmdlet Remove-AzureRmRoleDefinition exclui uma função personalizada no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="6261d-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="6261d-112">Forneça o parâmetro ID de uma função personalizada existente para excluir essa função personalizada.</span><span class="sxs-lookup"><span data-stu-id="6261d-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="6261d-113">Por padrão, Remove-AzureRmRoleDefinition solicita que você confirme a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6261d-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="6261d-114">Para suprimir o prompt, use o parâmetro Force.</span><span class="sxs-lookup"><span data-stu-id="6261d-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="6261d-115">Se houver atribuições de função feitas à função personalizada a serem excluídas, a exclusão falhará.</span><span class="sxs-lookup"><span data-stu-id="6261d-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="6261d-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6261d-116">EXAMPLES</span></span>

### <span data-ttu-id="6261d-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6261d-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="6261d-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6261d-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="6261d-119">OS</span><span class="sxs-lookup"><span data-stu-id="6261d-119">PARAMETERS</span></span>

### <span data-ttu-id="6261d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6261d-120">-DefaultProfile</span></span>
<span data-ttu-id="6261d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6261d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6261d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6261d-122">-Force</span></span>
<span data-ttu-id="6261d-123">Se definido, não solicita uma confirmação antes de excluir a função personalizada</span><span class="sxs-lookup"><span data-stu-id="6261d-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="6261d-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6261d-124">-Id</span></span>
<span data-ttu-id="6261d-125">ID da definição de função a ser excluída</span><span class="sxs-lookup"><span data-stu-id="6261d-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="6261d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6261d-126">-InputObject</span></span>
<span data-ttu-id="6261d-127">O objeto que representa a definição de função a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6261d-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="6261d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6261d-128">-Name</span></span>
<span data-ttu-id="6261d-129">Nome da definição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6261d-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="6261d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6261d-130">-PassThru</span></span>
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

### <span data-ttu-id="6261d-131">-Escopo</span><span class="sxs-lookup"><span data-stu-id="6261d-131">-Scope</span></span>
<span data-ttu-id="6261d-132">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="6261d-132">Role definition scope.</span></span>

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

### <span data-ttu-id="6261d-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6261d-133">-Confirm</span></span>
<span data-ttu-id="6261d-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6261d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6261d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6261d-135">-WhatIf</span></span>
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

### <span data-ttu-id="6261d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6261d-136">CommonParameters</span></span>
<span data-ttu-id="6261d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6261d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6261d-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6261d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6261d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6261d-139">INPUTS</span></span>

### <span data-ttu-id="6261d-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6261d-140">System.Guid</span></span>

### <span data-ttu-id="6261d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6261d-141">System.String</span></span>

### <span data-ttu-id="6261d-142">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6261d-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="6261d-143">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6261d-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6261d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6261d-144">OUTPUTS</span></span>

### <span data-ttu-id="6261d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6261d-145">System.Boolean</span></span>

## <span data-ttu-id="6261d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6261d-146">NOTES</span></span>
<span data-ttu-id="6261d-147">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="6261d-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6261d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6261d-148">RELATED LINKS</span></span>

[<span data-ttu-id="6261d-149">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6261d-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="6261d-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6261d-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="6261d-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6261d-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

