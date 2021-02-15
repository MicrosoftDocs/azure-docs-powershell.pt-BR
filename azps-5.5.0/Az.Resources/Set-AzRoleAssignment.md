---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112625"
---
# <span data-ttu-id="28a48-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="28a48-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="28a48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28a48-102">SYNOPSIS</span></span>
<span data-ttu-id="28a48-103">Atualizar uma Atribuição de Função existente.</span><span class="sxs-lookup"><span data-stu-id="28a48-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="28a48-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28a48-104">SYNTAX</span></span>

### <span data-ttu-id="28a48-105">RoleAssignmentParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28a48-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a48-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a48-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a48-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28a48-107">DESCRIPTION</span></span>
<span data-ttu-id="28a48-108">Use o comando New-AzRoleAssignment para modificar uma atribuição existente.</span><span class="sxs-lookup"><span data-stu-id="28a48-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="28a48-109">Descrições podem ser qualquer cadeia de caracteres válida, use-as para diferentá-la umas das outras.</span><span class="sxs-lookup"><span data-stu-id="28a48-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="28a48-110">se a Condição estiver definida, a versão da condição também deve ser definida, mas se você estiver atualizando uma Condição que não é necessária.</span><span class="sxs-lookup"><span data-stu-id="28a48-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="28a48-111">A versão de condição pode ser atualizada de 1.0 para 2.0, mas não pode ser rebaixada.</span><span class="sxs-lookup"><span data-stu-id="28a48-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="28a48-112">Seja cuidadoso, pois 2.0 não é retrocompatível com 1.0.</span><span class="sxs-lookup"><span data-stu-id="28a48-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="28a48-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28a48-113">EXAMPLES</span></span>

### <span data-ttu-id="28a48-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28a48-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="28a48-115">Atualizar uma atribuição de função existente modificando um objeto</span><span class="sxs-lookup"><span data-stu-id="28a48-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="28a48-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28a48-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="28a48-117">Atualizar uma atribuição de função existente usando um arquivo</span><span class="sxs-lookup"><span data-stu-id="28a48-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="28a48-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28a48-118">PARAMETERS</span></span>

### <span data-ttu-id="28a48-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a48-119">-DefaultProfile</span></span>
<span data-ttu-id="28a48-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28a48-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a48-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="28a48-121">-InputFile</span></span>
<span data-ttu-id="28a48-122">Nome de arquivo que contém uma única definição de função.</span><span class="sxs-lookup"><span data-stu-id="28a48-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a48-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a48-123">-InputObject</span></span>
<span data-ttu-id="28a48-124">Atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="28a48-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a48-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28a48-125">-PassThru</span></span>
<span data-ttu-id="28a48-126">Se especificado, exibirá a atribuição de função atualizada</span><span class="sxs-lookup"><span data-stu-id="28a48-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="28a48-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="28a48-127">-Confirm</span></span>
<span data-ttu-id="28a48-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28a48-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a48-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a48-129">-WhatIf</span></span>
<span data-ttu-id="28a48-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="28a48-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28a48-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28a48-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a48-132">CommonParameters</span></span>
<span data-ttu-id="28a48-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a48-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a48-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a48-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="28a48-135">INPUTS</span></span>

### <span data-ttu-id="28a48-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="28a48-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="28a48-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="28a48-137">OUTPUTS</span></span>

### <span data-ttu-id="28a48-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="28a48-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="28a48-139">Notas</span><span class="sxs-lookup"><span data-stu-id="28a48-139">NOTES</span></span>

## <span data-ttu-id="28a48-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28a48-140">RELATED LINKS</span></span>
