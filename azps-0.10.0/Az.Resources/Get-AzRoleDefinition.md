---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776421"
---
# <span data-ttu-id="0d56b-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56b-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="0d56b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d56b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d56b-103">Lista todas as funções RBAC do Azure que estão disponíveis para atribuição.</span><span class="sxs-lookup"><span data-stu-id="0d56b-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="0d56b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d56b-104">SYNTAX</span></span>

### <span data-ttu-id="0d56b-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56b-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d56b-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56b-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d56b-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56b-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d56b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d56b-108">DESCRIPTION</span></span>
<span data-ttu-id="0d56b-109">Use o comando Get-AzRoleDefinition com um nome de função específico para exibir os detalhes.</span><span class="sxs-lookup"><span data-stu-id="0d56b-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="0d56b-110">Para inspecionar as operações individuais às quais uma função concede acesso, examine as propriedades Actions e não-Actions da função.</span><span class="sxs-lookup"><span data-stu-id="0d56b-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="0d56b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d56b-111">EXAMPLES</span></span>

### <span data-ttu-id="0d56b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d56b-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="0d56b-113">Obter a definição da função do leitor</span><span class="sxs-lookup"><span data-stu-id="0d56b-113">Get the Reader role definition</span></span>

### <span data-ttu-id="0d56b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0d56b-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="0d56b-115">Lista todas as definições de função RBAC</span><span class="sxs-lookup"><span data-stu-id="0d56b-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="0d56b-116">OS</span><span class="sxs-lookup"><span data-stu-id="0d56b-116">PARAMETERS</span></span>

### <span data-ttu-id="0d56b-117">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="0d56b-117">-Custom</span></span>
<span data-ttu-id="0d56b-118">Se especificado, exibe somente as funções criadas personalizadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="0d56b-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="0d56b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d56b-119">-DefaultProfile</span></span>
<span data-ttu-id="0d56b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0d56b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d56b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0d56b-121">-Id</span></span>
<span data-ttu-id="0d56b-122">ID da definição da função.</span><span class="sxs-lookup"><span data-stu-id="0d56b-122">Role definition Id.</span></span>

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

### <span data-ttu-id="0d56b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d56b-123">-Name</span></span>
<span data-ttu-id="0d56b-124">Nome da definição de função.</span><span class="sxs-lookup"><span data-stu-id="0d56b-124">Role definition name.</span></span>
<span data-ttu-id="0d56b-125">Por exemplo, leitor, colaborador, colaborador da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0d56b-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="0d56b-126">-Escopo</span><span class="sxs-lookup"><span data-stu-id="0d56b-126">-Scope</span></span>
<span data-ttu-id="0d56b-127">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="0d56b-127">Role definition scope.</span></span>

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

### <span data-ttu-id="0d56b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d56b-128">CommonParameters</span></span>
<span data-ttu-id="0d56b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d56b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d56b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d56b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d56b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d56b-131">INPUTS</span></span>

### <span data-ttu-id="0d56b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0d56b-132">System.String</span></span>
<span data-ttu-id="0d56b-133">Parâmetros: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d56b-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="0d56b-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0d56b-134">System.Guid</span></span>

### <span data-ttu-id="0d56b-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0d56b-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d56b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d56b-136">OUTPUTS</span></span>

### <span data-ttu-id="0d56b-137">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56b-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="0d56b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d56b-138">NOTES</span></span>
<span data-ttu-id="0d56b-139">Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="0d56b-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0d56b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d56b-140">RELATED LINKS</span></span>

[<span data-ttu-id="0d56b-141">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0d56b-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="0d56b-142">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0d56b-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="0d56b-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56b-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="0d56b-144">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56b-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

