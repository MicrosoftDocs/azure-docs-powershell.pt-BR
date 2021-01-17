---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427265"
---
# <span data-ttu-id="0b796-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b796-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="0b796-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b796-102">SYNOPSIS</span></span>
<span data-ttu-id="0b796-103">Cria um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b796-103">Creates a Management Group</span></span>

## <span data-ttu-id="0b796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b796-104">SYNTAX</span></span>

### <span data-ttu-id="0b796-105">GroupOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b796-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b796-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="0b796-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b796-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b796-107">DESCRIPTION</span></span>
<span data-ttu-id="0b796-108">O cmdlet **New-AzManagementGroup** cria um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0b796-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="0b796-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b796-109">EXAMPLES</span></span>

### <span data-ttu-id="0b796-110">Exemplo 1: criar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b796-110">Example 1: Create a Management Group</span></span>
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

<span data-ttu-id="0b796-111">Criação de um novo grupo com `DisplayName` e `ParentId` definido como `null` .</span><span class="sxs-lookup"><span data-stu-id="0b796-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="0b796-112">O `DisplayName` será o mesmo que o `GroupName` pai do grupo será o locatário.</span><span class="sxs-lookup"><span data-stu-id="0b796-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="0b796-113">Exemplo 2: criar um grupo de gerenciamento com um nome para exibição</span><span class="sxs-lookup"><span data-stu-id="0b796-113">Example 2: Create a Management Group with a display name</span></span>
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

<span data-ttu-id="0b796-114">Nesse caso, o pai do grupo será o locatário e o `DisplayName` será definido como o valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="0b796-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="0b796-115">Exemplo 3: criar um grupo de gerenciamento com um nome pai e um nome para exibição</span><span class="sxs-lookup"><span data-stu-id="0b796-115">Example 3: Create a Management Group with a parent and a display name</span></span>
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

### <span data-ttu-id="0b796-116">Exemplo 4: criar um grupo de gerenciamento com um pai (usando um objeto pai)</span><span class="sxs-lookup"><span data-stu-id="0b796-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
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

## <span data-ttu-id="0b796-117">OS</span><span class="sxs-lookup"><span data-stu-id="0b796-117">PARAMETERS</span></span>

### <span data-ttu-id="0b796-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b796-118">-DefaultProfile</span></span>
<span data-ttu-id="0b796-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b796-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b796-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b796-120">-DisplayName</span></span>
<span data-ttu-id="0b796-121">Nome para exibição do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b796-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="0b796-122">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="0b796-122">-GroupName</span></span>
<span data-ttu-id="0b796-123">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b796-123">Management Group Id</span></span>

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

### <span data-ttu-id="0b796-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="0b796-124">-ParentId</span></span>
<span data-ttu-id="0b796-125">ID pai do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b796-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="0b796-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b796-126">-ParentObject</span></span>
<span data-ttu-id="0b796-127">Objeto pai</span><span class="sxs-lookup"><span data-stu-id="0b796-127">Parent Object</span></span>

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

### <span data-ttu-id="0b796-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b796-128">-Confirm</span></span>
<span data-ttu-id="0b796-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b796-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b796-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b796-130">-WhatIf</span></span>
<span data-ttu-id="0b796-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b796-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b796-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b796-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b796-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b796-133">CommonParameters</span></span>
<span data-ttu-id="0b796-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b796-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b796-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b796-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b796-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b796-136">INPUTS</span></span>

### <span data-ttu-id="0b796-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b796-137">None</span></span>

## <span data-ttu-id="0b796-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b796-138">OUTPUTS</span></span>

### <span data-ttu-id="0b796-139">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b796-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="0b796-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b796-140">NOTES</span></span>

## <span data-ttu-id="0b796-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b796-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b796-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b796-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="0b796-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b796-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="0b796-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b796-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)