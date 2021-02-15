---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111421"
---
# <span data-ttu-id="6257f-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6257f-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="6257f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6257f-102">SYNOPSIS</span></span>
<span data-ttu-id="6257f-103">Obtém Grupos de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6257f-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="6257f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6257f-104">SYNTAX</span></span>

### <span data-ttu-id="6257f-105">ListOperation (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6257f-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6257f-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="6257f-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6257f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6257f-107">DESCRIPTION</span></span>
<span data-ttu-id="6257f-108">O Get-AzManagementGroup cmdlet Obtém todo ou um Grupo de Gerenciamento específico.</span><span class="sxs-lookup"><span data-stu-id="6257f-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="6257f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6257f-109">EXAMPLES</span></span>

### <span data-ttu-id="6257f-110">Exemplo 1: Obter todos os Grupos de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6257f-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="6257f-111">Exemplo 2: Obter grupo de gerenciamento específico</span><span class="sxs-lookup"><span data-stu-id="6257f-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="6257f-112">Exemplo 3: Obter Um Grupo de Gerenciamento específico e o primeiro nível de hierarquia</span><span class="sxs-lookup"><span data-stu-id="6257f-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="6257f-113">Com o `Expand` sinalizador, é possível navegar pela `Children` matriz e obter detalhes para cada filho.</span><span class="sxs-lookup"><span data-stu-id="6257f-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="6257f-114">Por exemplo, `Children[0]` dará detalhes para o grupo com nome para exibição. `TestGroup1DisplayName`</span><span class="sxs-lookup"><span data-stu-id="6257f-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="6257f-115">Exemplo 4: Obter um Grupo de Gerenciamento específico e todos os níveis de hierarquia</span><span class="sxs-lookup"><span data-stu-id="6257f-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="6257f-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6257f-116">PARAMETERS</span></span>

### <span data-ttu-id="6257f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6257f-117">-DefaultProfile</span></span>
<span data-ttu-id="6257f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6257f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6257f-119">-Expandir</span><span class="sxs-lookup"><span data-stu-id="6257f-119">-Expand</span></span>
<span data-ttu-id="6257f-120">Expandir a saída para listar os filhos do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6257f-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6257f-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="6257f-121">-GroupName</span></span>
<span data-ttu-id="6257f-122">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6257f-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6257f-123">-Recorrência</span><span class="sxs-lookup"><span data-stu-id="6257f-123">-Recurse</span></span>
<span data-ttu-id="6257f-124">Listar recursivamente os filhos do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6257f-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6257f-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6257f-125">-Confirm</span></span>
<span data-ttu-id="6257f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6257f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6257f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6257f-127">-WhatIf</span></span>
<span data-ttu-id="6257f-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6257f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6257f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6257f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6257f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6257f-130">CommonParameters</span></span>
<span data-ttu-id="6257f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6257f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6257f-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6257f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6257f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="6257f-133">INPUTS</span></span>

### <span data-ttu-id="6257f-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6257f-134">None</span></span>

## <span data-ttu-id="6257f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="6257f-135">OUTPUTS</span></span>

### <span data-ttu-id="6257f-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="6257f-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="6257f-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6257f-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6257f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="6257f-138">NOTES</span></span>

## <span data-ttu-id="6257f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6257f-139">RELATED LINKS</span></span>
