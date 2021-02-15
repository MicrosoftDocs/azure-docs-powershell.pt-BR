---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118759"
---
# <span data-ttu-id="709bb-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="709bb-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="709bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="709bb-102">SYNOPSIS</span></span>
<span data-ttu-id="709bb-103">Lista todas as funções do Azure RBAC disponíveis para atribuição.</span><span class="sxs-lookup"><span data-stu-id="709bb-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="709bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="709bb-104">SYNTAX</span></span>

### <span data-ttu-id="709bb-105">RoleDefinitionNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="709bb-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="709bb-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="709bb-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="709bb-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="709bb-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="709bb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="709bb-108">DESCRIPTION</span></span>
<span data-ttu-id="709bb-109">Use o comando Get-AzRoleDefinition com um nome de função específico para exibir seus detalhes.</span><span class="sxs-lookup"><span data-stu-id="709bb-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="709bb-110">Para inspecionar as operações individuais às que uma função concede acesso, examine as propriedades Ações e NotActions da função.</span><span class="sxs-lookup"><span data-stu-id="709bb-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="709bb-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="709bb-111">EXAMPLES</span></span>

### <span data-ttu-id="709bb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="709bb-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="709bb-113">Obter a definição da função Leitor</span><span class="sxs-lookup"><span data-stu-id="709bb-113">Get the Reader role definition</span></span>

### <span data-ttu-id="709bb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="709bb-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="709bb-115">Lista todas as definições de função RBAC</span><span class="sxs-lookup"><span data-stu-id="709bb-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="709bb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="709bb-116">PARAMETERS</span></span>

### <span data-ttu-id="709bb-117">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="709bb-117">-Custom</span></span>
<span data-ttu-id="709bb-118">Se especificado, exibirá apenas as funções criadas personalizadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="709bb-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="709bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709bb-119">-DefaultProfile</span></span>
<span data-ttu-id="709bb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="709bb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="709bb-121">-ID</span><span class="sxs-lookup"><span data-stu-id="709bb-121">-Id</span></span>
<span data-ttu-id="709bb-122">ID de definição de função.</span><span class="sxs-lookup"><span data-stu-id="709bb-122">Role definition Id.</span></span>

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

### <span data-ttu-id="709bb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="709bb-123">-Name</span></span>
<span data-ttu-id="709bb-124">Nome da definição de função.</span><span class="sxs-lookup"><span data-stu-id="709bb-124">Role definition name.</span></span>
<span data-ttu-id="709bb-125">Por exemplo, Reader, Contributor, Virtual Machine Contributor.</span><span class="sxs-lookup"><span data-stu-id="709bb-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="709bb-126">-Escopo</span><span class="sxs-lookup"><span data-stu-id="709bb-126">-Scope</span></span>
<span data-ttu-id="709bb-127">Escopo de definição de função.</span><span class="sxs-lookup"><span data-stu-id="709bb-127">Role definition scope.</span></span>

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

### <span data-ttu-id="709bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709bb-128">CommonParameters</span></span>
<span data-ttu-id="709bb-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709bb-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="709bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709bb-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="709bb-131">INPUTS</span></span>

### <span data-ttu-id="709bb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="709bb-132">System.String</span></span>

### <span data-ttu-id="709bb-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="709bb-133">System.Guid</span></span>

### <span data-ttu-id="709bb-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="709bb-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="709bb-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="709bb-135">OUTPUTS</span></span>

### <span data-ttu-id="709bb-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="709bb-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="709bb-137">Notas</span><span class="sxs-lookup"><span data-stu-id="709bb-137">NOTES</span></span>
<span data-ttu-id="709bb-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="709bb-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="709bb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="709bb-139">RELATED LINKS</span></span>

[<span data-ttu-id="709bb-140">Novo-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="709bb-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="709bb-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="709bb-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="709bb-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="709bb-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="709bb-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="709bb-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

