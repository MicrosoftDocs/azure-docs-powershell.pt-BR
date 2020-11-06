---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603321"
---
# <span data-ttu-id="e72d9-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e72d9-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="e72d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e72d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e72d9-103">Exclui uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e72d9-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e72d9-104">A função a ser excluída é especificada usando-se a propriedade ID da função.</span><span class="sxs-lookup"><span data-stu-id="e72d9-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="e72d9-105">A exclusão falhará se houver atribuições de função existentes à função personalizada.</span><span class="sxs-lookup"><span data-stu-id="e72d9-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e72d9-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e72d9-106">SYNTAX</span></span>

### <span data-ttu-id="e72d9-107">RoleDefinitionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e72d9-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72d9-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72d9-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72d9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e72d9-109">DESCRIPTION</span></span>
<span data-ttu-id="e72d9-110">O cmdlet Remove-AzureRmRoleDefinition exclui uma função personalizada no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="e72d9-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e72d9-111">Forneça o parâmetro ID de uma função personalizada existente para excluir essa função personalizada.</span><span class="sxs-lookup"><span data-stu-id="e72d9-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="e72d9-112">Por padrão, Remove-AzureRmRoleDefinition solicita que você confirme a confirmação.</span><span class="sxs-lookup"><span data-stu-id="e72d9-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="e72d9-113">Para suprimir o prompt, use o parâmetro Force.</span><span class="sxs-lookup"><span data-stu-id="e72d9-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="e72d9-114">Se houver atribuições de função feitas à função personalizada a serem excluídas, a exclusão falhará.</span><span class="sxs-lookup"><span data-stu-id="e72d9-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="e72d9-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e72d9-115">EXAMPLES</span></span>

### <span data-ttu-id="e72d9-116">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e72d9-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="e72d9-117">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e72d9-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="e72d9-118">OS</span><span class="sxs-lookup"><span data-stu-id="e72d9-118">PARAMETERS</span></span>

### <span data-ttu-id="e72d9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e72d9-119">-Force</span></span>
<span data-ttu-id="e72d9-120">Se definido, não solicita uma confirmação antes de excluir a função personalizada</span><span class="sxs-lookup"><span data-stu-id="e72d9-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="e72d9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e72d9-121">-Id</span></span>
<span data-ttu-id="e72d9-122">ID da definição de função a ser excluída</span><span class="sxs-lookup"><span data-stu-id="e72d9-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="e72d9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e72d9-123">-Name</span></span>
<span data-ttu-id="e72d9-124">Nome da definição de função a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="e72d9-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="e72d9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e72d9-125">-PassThru</span></span>
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

### <span data-ttu-id="e72d9-126">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e72d9-126">-Scope</span></span>
<span data-ttu-id="e72d9-127">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="e72d9-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72d9-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e72d9-128">-Confirm</span></span>
<span data-ttu-id="e72d9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72d9-130">-WhatIf</span></span>
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

### <span data-ttu-id="e72d9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72d9-131">-DefaultProfile</span></span>
<span data-ttu-id="e72d9-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e72d9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72d9-133">CommonParameters</span></span>
<span data-ttu-id="e72d9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72d9-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72d9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e72d9-136">INPUTS</span></span>

## <span data-ttu-id="e72d9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e72d9-137">OUTPUTS</span></span>

### <span data-ttu-id="e72d9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e72d9-138">System.Boolean</span></span>

## <span data-ttu-id="e72d9-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e72d9-139">NOTES</span></span>
<span data-ttu-id="e72d9-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="e72d9-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e72d9-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e72d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="e72d9-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e72d9-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="e72d9-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e72d9-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="e72d9-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e72d9-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

