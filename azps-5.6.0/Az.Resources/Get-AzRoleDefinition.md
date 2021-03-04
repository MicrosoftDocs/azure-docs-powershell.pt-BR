---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890348"
---
# <span data-ttu-id="f98ad-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f98ad-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="f98ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f98ad-103">Lista todas as funções do Azure RBAC disponíveis para atribuição.</span><span class="sxs-lookup"><span data-stu-id="f98ad-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="f98ad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f98ad-104">SYNTAX</span></span>

### <span data-ttu-id="f98ad-105">RoleDefinitionNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f98ad-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f98ad-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ad-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f98ad-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98ad-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f98ad-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f98ad-108">DESCRIPTION</span></span>
<span data-ttu-id="f98ad-109">Use o Get-AzRoleDefinition com um nome de função específico para exibir seus detalhes.</span><span class="sxs-lookup"><span data-stu-id="f98ad-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="f98ad-110">Para inspecionar operações individuais às que uma função concede acesso, examine as propriedades Actions e NotActions da função.</span><span class="sxs-lookup"><span data-stu-id="f98ad-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="f98ad-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f98ad-111">EXAMPLES</span></span>

### <span data-ttu-id="f98ad-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f98ad-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="f98ad-113">Obter a definição de função Leitor</span><span class="sxs-lookup"><span data-stu-id="f98ad-113">Get the Reader role definition</span></span>

### <span data-ttu-id="f98ad-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f98ad-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="f98ad-115">Lista todas as definições de função RBAC</span><span class="sxs-lookup"><span data-stu-id="f98ad-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="f98ad-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f98ad-116">PARAMETERS</span></span>

### <span data-ttu-id="f98ad-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="f98ad-117">-Custom</span></span>
<span data-ttu-id="f98ad-118">Se especificado, exibe apenas as funções criadas personalizadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="f98ad-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98ad-119">-DefaultProfile</span></span>
<span data-ttu-id="f98ad-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f98ad-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f98ad-121">-Id</span><span class="sxs-lookup"><span data-stu-id="f98ad-121">-Id</span></span>
<span data-ttu-id="f98ad-122">ID de definição de função.</span><span class="sxs-lookup"><span data-stu-id="f98ad-122">Role definition Id.</span></span>

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

### <span data-ttu-id="f98ad-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f98ad-123">-Name</span></span>
<span data-ttu-id="f98ad-124">Nome da definição de função.</span><span class="sxs-lookup"><span data-stu-id="f98ad-124">Role definition name.</span></span>
<span data-ttu-id="f98ad-125">Por exemplo, Leitor, Colaborador, Colaborador de Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="f98ad-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98ad-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="f98ad-126">-Scope</span></span>
<span data-ttu-id="f98ad-127">Escopo de definição de função.</span><span class="sxs-lookup"><span data-stu-id="f98ad-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98ad-128">CommonParameters</span></span>
<span data-ttu-id="f98ad-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98ad-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f98ad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98ad-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f98ad-131">INPUTS</span></span>

### <span data-ttu-id="f98ad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f98ad-132">System.String</span></span>

### <span data-ttu-id="f98ad-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f98ad-133">System.Guid</span></span>

### <span data-ttu-id="f98ad-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f98ad-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f98ad-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f98ad-135">OUTPUTS</span></span>

### <span data-ttu-id="f98ad-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f98ad-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f98ad-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="f98ad-137">NOTES</span></span>
<span data-ttu-id="f98ad-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="f98ad-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f98ad-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f98ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="f98ad-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f98ad-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="f98ad-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f98ad-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="f98ad-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f98ad-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f98ad-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f98ad-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

