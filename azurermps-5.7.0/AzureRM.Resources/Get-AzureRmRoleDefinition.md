---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432903"
---
# <span data-ttu-id="186ba-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="186ba-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="186ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="186ba-102">SYNOPSIS</span></span>
<span data-ttu-id="186ba-103">Lista todas as funções RBAC do Azure que estão disponíveis para atribuição.</span><span class="sxs-lookup"><span data-stu-id="186ba-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="186ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="186ba-104">SYNTAX</span></span>

### <span data-ttu-id="186ba-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="186ba-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="186ba-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="186ba-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="186ba-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="186ba-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="186ba-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="186ba-108">DESCRIPTION</span></span>
<span data-ttu-id="186ba-109">Use o comando Get-AzureRmRoleDefinition com um nome de função específico para exibir os detalhes.</span><span class="sxs-lookup"><span data-stu-id="186ba-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="186ba-110">Para inspecionar as operações individuais às quais uma função concede acesso, examine as propriedades Actions e não-Actions da função.</span><span class="sxs-lookup"><span data-stu-id="186ba-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="186ba-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="186ba-111">EXAMPLES</span></span>

### <span data-ttu-id="186ba-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="186ba-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="186ba-113">Obter a definição da função do leitor</span><span class="sxs-lookup"><span data-stu-id="186ba-113">Get the Reader role definition</span></span>

### <span data-ttu-id="186ba-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="186ba-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="186ba-115">Lista todas as definições de função RBAC</span><span class="sxs-lookup"><span data-stu-id="186ba-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="186ba-116">OS</span><span class="sxs-lookup"><span data-stu-id="186ba-116">PARAMETERS</span></span>

### <span data-ttu-id="186ba-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="186ba-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="186ba-118">Se especificado, exibe todas as definições de função.</span><span class="sxs-lookup"><span data-stu-id="186ba-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-119">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="186ba-119">-Custom</span></span>
<span data-ttu-id="186ba-120">Se especificado, exibe somente as funções criadas personalizadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="186ba-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186ba-121">-DefaultProfile</span></span>
<span data-ttu-id="186ba-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="186ba-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-123">-ID</span><span class="sxs-lookup"><span data-stu-id="186ba-123">-Id</span></span>
<span data-ttu-id="186ba-124">ID da definição da função.</span><span class="sxs-lookup"><span data-stu-id="186ba-124">Role definition Id.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="186ba-125">-Name</span></span>
<span data-ttu-id="186ba-126">Nome da definição de função.</span><span class="sxs-lookup"><span data-stu-id="186ba-126">Role definition name.</span></span>
<span data-ttu-id="186ba-127">Por exemplo, leitor, colaborador, colaborador da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="186ba-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="186ba-128">-Scope</span></span>
<span data-ttu-id="186ba-129">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="186ba-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="186ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186ba-130">CommonParameters</span></span>
<span data-ttu-id="186ba-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186ba-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="186ba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186ba-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="186ba-133">INPUTS</span></span>

### <span data-ttu-id="186ba-134">String</span><span class="sxs-lookup"><span data-stu-id="186ba-134">String</span></span>
<span data-ttu-id="186ba-135">O parâmetro ' Scope ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="186ba-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="186ba-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="186ba-136">OUTPUTS</span></span>

### <span data-ttu-id="186ba-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="186ba-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="186ba-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="186ba-138">NOTES</span></span>
<span data-ttu-id="186ba-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="186ba-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="186ba-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="186ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="186ba-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="186ba-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="186ba-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="186ba-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="186ba-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="186ba-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="186ba-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="186ba-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

