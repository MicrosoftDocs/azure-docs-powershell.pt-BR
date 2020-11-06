---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmManagementGroup.md
ms.openlocfilehash: 2542740db9cb8f5b0809bf071e2b960ba8979de8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429359"
---
# <span data-ttu-id="977fc-101">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="977fc-101">Update-AzureRmManagementGroup</span></span>

## <span data-ttu-id="977fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="977fc-102">SYNOPSIS</span></span>
<span data-ttu-id="977fc-103">Atualiza um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-103">Updates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="977fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="977fc-104">SYNTAX</span></span>

### <span data-ttu-id="977fc-105">GroupOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="977fc-105">GroupOperations (Default)</span></span>
```
Update-AzureRmManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="977fc-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="977fc-106">ParentAndManagementGroupObject</span></span>
```
Update-AzureRmManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="977fc-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="977fc-107">ManagementGroupObject</span></span>
```
Update-AzureRmManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="977fc-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="977fc-108">ParentGroupObject</span></span>
```
Update-AzureRmManagementGroup -GroupName <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="977fc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="977fc-109">DESCRIPTION</span></span>
<span data-ttu-id="977fc-110">O cmdlet **Update-AzureRMManagementGroup** atualiza **parentID** ou **DisplayName** para um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="977fc-110">The **Update-AzureRMManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="977fc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="977fc-111">EXAMPLES</span></span>

### <span data-ttu-id="977fc-112">Exemplo 1: atualizar o nome de exibição de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzureRMManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

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

### <span data-ttu-id="977fc-113">Exemplo 2: atualizar o pai de um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzureRMManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="977fc-114">Exemplo 3: atualizar um grupo de gerenciamento por objeto de PSManagementGroup de tubulação</span><span class="sxs-lookup"><span data-stu-id="977fc-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName "TestGroup" | Update-AzureRMManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="977fc-115">Exemplo 4: atualizar o pai de um grupo de gerenciamento usando ParentObject</span><span class="sxs-lookup"><span data-stu-id="977fc-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="977fc-116">OS</span><span class="sxs-lookup"><span data-stu-id="977fc-116">PARAMETERS</span></span>

### <span data-ttu-id="977fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977fc-117">-DefaultProfile</span></span>
<span data-ttu-id="977fc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="977fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="977fc-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="977fc-119">-DisplayName</span></span>
<span data-ttu-id="977fc-120">Nome para exibição do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="977fc-121">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="977fc-121">-GroupName</span></span>
<span data-ttu-id="977fc-122">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977fc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="977fc-123">-InputObject</span></span>
<span data-ttu-id="977fc-124">Objeto de entrada da chamada Get</span><span class="sxs-lookup"><span data-stu-id="977fc-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="977fc-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="977fc-125">-ParentId</span></span>
<span data-ttu-id="977fc-126">ID pai do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="977fc-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="977fc-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="977fc-127">-ParentObject</span></span>
<span data-ttu-id="977fc-128">Objeto de entrada da chamada Get</span><span class="sxs-lookup"><span data-stu-id="977fc-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="977fc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="977fc-129">-Confirm</span></span>
<span data-ttu-id="977fc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="977fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="977fc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="977fc-131">-WhatIf</span></span>
<span data-ttu-id="977fc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="977fc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="977fc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="977fc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="977fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977fc-134">CommonParameters</span></span>
<span data-ttu-id="977fc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977fc-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977fc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977fc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="977fc-137">INPUTS</span></span>

### <span data-ttu-id="977fc-138">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="977fc-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="977fc-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="977fc-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="977fc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="977fc-140">OUTPUTS</span></span>

### <span data-ttu-id="977fc-141">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="977fc-141">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="977fc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="977fc-142">NOTES</span></span>

## <span data-ttu-id="977fc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="977fc-143">RELATED LINKS</span></span>
