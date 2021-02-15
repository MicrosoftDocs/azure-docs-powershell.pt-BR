---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112637"
---
# <span data-ttu-id="75b83-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="75b83-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="75b83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75b83-102">SYNOPSIS</span></span>
<span data-ttu-id="75b83-103">Cria um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="75b83-103">Creates a Management Group</span></span>

## <span data-ttu-id="75b83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b83-104">SYNTAX</span></span>

### <span data-ttu-id="75b83-105">GroupOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75b83-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b83-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="75b83-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b83-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="75b83-107">DESCRIPTION</span></span>
<span data-ttu-id="75b83-108">O **cmdlet New-AzManagementGroup** cria um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="75b83-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="75b83-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75b83-109">EXAMPLES</span></span>

### <span data-ttu-id="75b83-110">Exemplo 1: Criar um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="75b83-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="75b83-111">Criação de um novo grupo com `DisplayName` e `ParentId` definido como `null` .</span><span class="sxs-lookup"><span data-stu-id="75b83-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="75b83-112">O mesmo será o pai do grupo e o `DisplayName` `GroupName` locatário.</span><span class="sxs-lookup"><span data-stu-id="75b83-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="75b83-113">Exemplo 2: Criar um Grupo de Gerenciamento com um nome para exibição</span><span class="sxs-lookup"><span data-stu-id="75b83-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="75b83-114">Nesse caso, o pai do grupo será o locatário e o valor será `DisplayName` definido como determinado.</span><span class="sxs-lookup"><span data-stu-id="75b83-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="75b83-115">Exemplo 3: Criar um Grupo de Gerenciamento com um pai e um nome para exibição</span><span class="sxs-lookup"><span data-stu-id="75b83-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="75b83-116">Exemplo 4: Criar um Grupo de Gerenciamento com um pai (usando um objeto pai)</span><span class="sxs-lookup"><span data-stu-id="75b83-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="75b83-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75b83-117">PARAMETERS</span></span>

### <span data-ttu-id="75b83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b83-118">-DefaultProfile</span></span>
<span data-ttu-id="75b83-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75b83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b83-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75b83-120">-DisplayName</span></span>
<span data-ttu-id="75b83-121">Nome de Exibição do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="75b83-121">Display Name of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b83-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="75b83-122">-GroupName</span></span>
<span data-ttu-id="75b83-123">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="75b83-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b83-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="75b83-124">-ParentId</span></span>
<span data-ttu-id="75b83-125">ID do responsável do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="75b83-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b83-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75b83-126">-ParentObject</span></span>
<span data-ttu-id="75b83-127">Objeto pai</span><span class="sxs-lookup"><span data-stu-id="75b83-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b83-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="75b83-128">-Confirm</span></span>
<span data-ttu-id="75b83-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b83-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b83-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b83-130">-WhatIf</span></span>
<span data-ttu-id="75b83-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="75b83-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b83-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75b83-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b83-133">CommonParameters</span></span>
<span data-ttu-id="75b83-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b83-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75b83-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b83-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="75b83-136">INPUTS</span></span>

### <span data-ttu-id="75b83-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75b83-137">None</span></span>

## <span data-ttu-id="75b83-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="75b83-138">OUTPUTS</span></span>

### <span data-ttu-id="75b83-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="75b83-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="75b83-140">Notas</span><span class="sxs-lookup"><span data-stu-id="75b83-140">NOTES</span></span>

## <span data-ttu-id="75b83-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75b83-141">RELATED LINKS</span></span>

[<span data-ttu-id="75b83-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="75b83-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="75b83-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="75b83-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="75b83-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="75b83-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)