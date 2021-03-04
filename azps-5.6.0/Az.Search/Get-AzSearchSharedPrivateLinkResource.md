---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ac27d706afcce4b8b431e0253b0a4e5146883640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889159"
---
# <span data-ttu-id="d2fe7-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d2fe7-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d2fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2fe7-103">Obtém recursos de link privado compartilhados do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d2fe7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2fe7-104">SYNTAX</span></span>

### <span data-ttu-id="d2fe7-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2fe7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2fe7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2fe7-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2fe7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2fe7-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2fe7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="d2fe7-109">O cmdlet **Get-AzSearchSharedPrivateLinkResource** obtém recursos de link privado compartilhados do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d2fe7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="d2fe7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2fe7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="d2fe7-112">Este exemplo lista todos os recursos de link privado compartilhados do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="d2fe7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2fe7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="d2fe7-114">Este exemplo lista um recurso de link privado compartilhado específico pelo nome do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d2fe7-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-115">PARAMETERS</span></span>

### <span data-ttu-id="d2fe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2fe7-116">-DefaultProfile</span></span>
<span data-ttu-id="d2fe7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2fe7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d2fe7-118">-Name</span></span>
<span data-ttu-id="d2fe7-119">Recurso de link privado compartilhado da Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="d2fe7-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fe7-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2fe7-120">-ParentObject</span></span>
<span data-ttu-id="d2fe7-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fe7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2fe7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2fe7-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fe7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2fe7-124">-ResourceId</span></span>
<span data-ttu-id="d2fe7-125">ID de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="d2fe7-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fe7-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2fe7-126">-ServiceName</span></span>
<span data-ttu-id="d2fe7-127">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-127">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fe7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2fe7-128">-Confirm</span></span>
<span data-ttu-id="d2fe7-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2fe7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2fe7-130">-WhatIf</span></span>
<span data-ttu-id="d2fe7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2fe7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2fe7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2fe7-133">CommonParameters</span></span>
<span data-ttu-id="d2fe7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2fe7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2fe7-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2fe7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2fe7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-136">INPUTS</span></span>

### <span data-ttu-id="d2fe7-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d2fe7-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d2fe7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d2fe7-138">System.String</span></span>

## <span data-ttu-id="d2fe7-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-139">OUTPUTS</span></span>

### <span data-ttu-id="d2fe7-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d2fe7-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d2fe7-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2fe7-141">NOTES</span></span>

## <span data-ttu-id="d2fe7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2fe7-142">RELATED LINKS</span></span>

[<span data-ttu-id="d2fe7-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d2fe7-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d2fe7-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d2fe7-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d2fe7-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d2fe7-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
