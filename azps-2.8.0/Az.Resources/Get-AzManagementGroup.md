---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 0232fd194452db1ab50be70df27ac63a85e713f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772589"
---
# <span data-ttu-id="4edbb-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4edbb-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="4edbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4edbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4edbb-103">Obtém grupo (s) de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4edbb-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="4edbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4edbb-104">SYNTAX</span></span>

### <span data-ttu-id="4edbb-105">ListOperation (padrão)</span><span class="sxs-lookup"><span data-stu-id="4edbb-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4edbb-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="4edbb-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4edbb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4edbb-107">DESCRIPTION</span></span>
<span data-ttu-id="4edbb-108">O cmdlet Get-AzManagementGroup Obtém tudo ou um grupo de gerenciamento específico.</span><span class="sxs-lookup"><span data-stu-id="4edbb-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="4edbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4edbb-109">EXAMPLES</span></span>

### <span data-ttu-id="4edbb-110">Exemplo 1: obter todos os grupos de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4edbb-110">Example 1: Get all Management Groups</span></span>
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

### <span data-ttu-id="4edbb-111">Exemplo 2: obter um grupo de gerenciamento específico</span><span class="sxs-lookup"><span data-stu-id="4edbb-111">Example 2: Get specific Management Group</span></span>
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

### <span data-ttu-id="4edbb-112">Exemplo 3: obter um grupo de gerenciamento específico e o primeiro nível de hierarquia</span><span class="sxs-lookup"><span data-stu-id="4edbb-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
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

<span data-ttu-id="4edbb-113">Com o `Expand` sinalizador, um pode navegar pela `Children` matriz e obter detalhes de cada filho.</span><span class="sxs-lookup"><span data-stu-id="4edbb-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="4edbb-114">Por exemplo, `Children[0]` forneceremos detalhes do grupo com nome para exibição `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="4edbb-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="4edbb-115">Exemplo 4: obter um grupo de gerenciamento específico e todos os níveis de hierarquia</span><span class="sxs-lookup"><span data-stu-id="4edbb-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
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

## <span data-ttu-id="4edbb-116">OS</span><span class="sxs-lookup"><span data-stu-id="4edbb-116">PARAMETERS</span></span>

### <span data-ttu-id="4edbb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4edbb-117">-DefaultProfile</span></span>
<span data-ttu-id="4edbb-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4edbb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4edbb-119">-Expandir</span><span class="sxs-lookup"><span data-stu-id="4edbb-119">-Expand</span></span>
<span data-ttu-id="4edbb-120">Expanda a saída para listar os filhos do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4edbb-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="4edbb-121">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="4edbb-121">-GroupName</span></span>
<span data-ttu-id="4edbb-122">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4edbb-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4edbb-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="4edbb-123">-Recurse</span></span>
<span data-ttu-id="4edbb-124">Listar os filhos do grupo de gerenciamento recursivamente</span><span class="sxs-lookup"><span data-stu-id="4edbb-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="4edbb-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4edbb-125">-Confirm</span></span>
<span data-ttu-id="4edbb-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4edbb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4edbb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4edbb-127">-WhatIf</span></span>
<span data-ttu-id="4edbb-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4edbb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4edbb-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4edbb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4edbb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4edbb-130">CommonParameters</span></span>
<span data-ttu-id="4edbb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4edbb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4edbb-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4edbb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4edbb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4edbb-133">INPUTS</span></span>

### <span data-ttu-id="4edbb-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4edbb-134">None</span></span>

## <span data-ttu-id="4edbb-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4edbb-135">OUTPUTS</span></span>

### <span data-ttu-id="4edbb-136">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="4edbb-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="4edbb-137">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4edbb-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="4edbb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4edbb-138">NOTES</span></span>

## <span data-ttu-id="4edbb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4edbb-139">RELATED LINKS</span></span>
