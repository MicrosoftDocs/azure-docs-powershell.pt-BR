---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: 23d60b0251c50f5bf4d5174e1ea1b5ef6f60b0ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887958"
---
# <span data-ttu-id="70d33-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70d33-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="70d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d33-102">SYNOPSIS</span></span>
<span data-ttu-id="70d33-103">Atualiza um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-103">Updates a Management Group</span></span>

## <span data-ttu-id="70d33-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70d33-104">SYNTAX</span></span>

### <span data-ttu-id="70d33-105">GroupOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70d33-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d33-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="70d33-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d33-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="70d33-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d33-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="70d33-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d33-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70d33-109">DESCRIPTION</span></span>
<span data-ttu-id="70d33-110">O cmdlet **Update-AzManagementGroup** atualiza **ParentId** ou **DisplayName** para um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="70d33-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="70d33-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70d33-111">EXAMPLES</span></span>

### <span data-ttu-id="70d33-112">Exemplo 1: atualizar o nome de exibição de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="70d33-113">Exemplo 2: Atualizar o pai de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="70d33-114">Exemplo 3: Atualizar um Grupo de Gerenciamento canalização do objeto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70d33-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="70d33-115">Exemplo 4: atualizar o pai de um grupo de gerenciamento usando o Objeto ParentObject</span><span class="sxs-lookup"><span data-stu-id="70d33-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="70d33-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70d33-116">PARAMETERS</span></span>

### <span data-ttu-id="70d33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d33-117">-DefaultProfile</span></span>
<span data-ttu-id="70d33-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70d33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d33-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="70d33-119">-DisplayName</span></span>
<span data-ttu-id="70d33-120">Nome de exibição do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="70d33-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="70d33-121">-GroupName</span></span>
<span data-ttu-id="70d33-122">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d33-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70d33-123">-InputObject</span></span>
<span data-ttu-id="70d33-124">Objeto Input da chamada Get</span><span class="sxs-lookup"><span data-stu-id="70d33-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70d33-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="70d33-125">-ParentId</span></span>
<span data-ttu-id="70d33-126">ID pai do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="70d33-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d33-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="70d33-127">-ParentObject</span></span>
<span data-ttu-id="70d33-128">Objeto Input da chamada Get</span><span class="sxs-lookup"><span data-stu-id="70d33-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d33-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70d33-129">-Confirm</span></span>
<span data-ttu-id="70d33-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d33-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d33-131">-WhatIf</span></span>
<span data-ttu-id="70d33-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70d33-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d33-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70d33-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d33-134">CommonParameters</span></span>
<span data-ttu-id="70d33-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d33-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70d33-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d33-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70d33-137">INPUTS</span></span>

### <span data-ttu-id="70d33-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70d33-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="70d33-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70d33-139">OUTPUTS</span></span>

### <span data-ttu-id="70d33-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="70d33-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="70d33-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="70d33-141">NOTES</span></span>

## <span data-ttu-id="70d33-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70d33-142">RELATED LINKS</span></span>
