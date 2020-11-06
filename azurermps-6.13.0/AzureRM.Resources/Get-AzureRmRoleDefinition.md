---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 9db953cf4c02497fd3056a57ed7b71a78687411d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611024"
---
# <span data-ttu-id="ea140-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ea140-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="ea140-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea140-102">SYNOPSIS</span></span>
<span data-ttu-id="ea140-103">Lista todas as funções RBAC do Azure que estão disponíveis para atribuição.</span><span class="sxs-lookup"><span data-stu-id="ea140-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea140-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea140-104">SYNTAX</span></span>

### <span data-ttu-id="ea140-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea140-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea140-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea140-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea140-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea140-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea140-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea140-108">DESCRIPTION</span></span>
<span data-ttu-id="ea140-109">Use o comando Get-AzureRmRoleDefinition com um nome de função específico para exibir os detalhes.</span><span class="sxs-lookup"><span data-stu-id="ea140-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="ea140-110">Para inspecionar as operações individuais às quais uma função concede acesso, examine as propriedades Actions e não-Actions da função.</span><span class="sxs-lookup"><span data-stu-id="ea140-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="ea140-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea140-111">EXAMPLES</span></span>

### <span data-ttu-id="ea140-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea140-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="ea140-113">Obter a definição da função do leitor</span><span class="sxs-lookup"><span data-stu-id="ea140-113">Get the Reader role definition</span></span>

### <span data-ttu-id="ea140-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea140-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="ea140-115">Lista todas as definições de função RBAC</span><span class="sxs-lookup"><span data-stu-id="ea140-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="ea140-116">OS</span><span class="sxs-lookup"><span data-stu-id="ea140-116">PARAMETERS</span></span>

### <span data-ttu-id="ea140-117">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="ea140-117">-Custom</span></span>
<span data-ttu-id="ea140-118">Se especificado, exibe somente as funções criadas personalizadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="ea140-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="ea140-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea140-119">-DefaultProfile</span></span>
<span data-ttu-id="ea140-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ea140-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea140-121">-ID</span><span class="sxs-lookup"><span data-stu-id="ea140-121">-Id</span></span>
<span data-ttu-id="ea140-122">ID da definição da função.</span><span class="sxs-lookup"><span data-stu-id="ea140-122">Role definition Id.</span></span>

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

### <span data-ttu-id="ea140-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea140-123">-Name</span></span>
<span data-ttu-id="ea140-124">Nome da definição de função.</span><span class="sxs-lookup"><span data-stu-id="ea140-124">Role definition name.</span></span>
<span data-ttu-id="ea140-125">Por exemplo, leitor, colaborador, colaborador da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea140-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="ea140-126">-Escopo</span><span class="sxs-lookup"><span data-stu-id="ea140-126">-Scope</span></span>
<span data-ttu-id="ea140-127">Escopo da definição de função.</span><span class="sxs-lookup"><span data-stu-id="ea140-127">Role definition scope.</span></span>

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

### <span data-ttu-id="ea140-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea140-128">CommonParameters</span></span>
<span data-ttu-id="ea140-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea140-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea140-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea140-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea140-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea140-131">INPUTS</span></span>

### <span data-ttu-id="ea140-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ea140-132">System.String</span></span>
<span data-ttu-id="ea140-133">Parâmetros: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea140-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="ea140-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ea140-134">System.Guid</span></span>

### <span data-ttu-id="ea140-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea140-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea140-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea140-136">OUTPUTS</span></span>

### <span data-ttu-id="ea140-137">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ea140-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="ea140-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea140-138">NOTES</span></span>
<span data-ttu-id="ea140-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="ea140-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ea140-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea140-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea140-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ea140-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="ea140-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ea140-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="ea140-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ea140-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="ea140-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ea140-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

