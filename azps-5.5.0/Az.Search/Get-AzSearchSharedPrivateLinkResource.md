---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114894"
---
# <span data-ttu-id="36440-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="36440-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="36440-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36440-102">SYNOPSIS</span></span>
<span data-ttu-id="36440-103">Obtém recursos de links privados compartilhados do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="36440-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36440-104">SYNTAX</span></span>

### <span data-ttu-id="36440-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36440-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36440-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36440-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36440-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36440-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36440-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="36440-108">DESCRIPTION</span></span>
<span data-ttu-id="36440-109">O cmdlet **Get-AzSearchSharedPrivateLinkResource** obtém recursos de link privado compartilhados do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="36440-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36440-110">EXAMPLES</span></span>

### <span data-ttu-id="36440-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36440-111">Example 1</span></span>
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

<span data-ttu-id="36440-112">Este exemplo lista todos os recursos de vínculo privado compartilhados do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="36440-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36440-113">Example 2</span></span>
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

<span data-ttu-id="36440-114">Este exemplo lista um recurso de vínculo privado compartilhado específico por nome do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="36440-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36440-115">PARAMETERS</span></span>

### <span data-ttu-id="36440-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36440-116">-DefaultProfile</span></span>
<span data-ttu-id="36440-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36440-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="36440-118">-Name</span></span>
<span data-ttu-id="36440-119">Recurso de link privado compartilhado da Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="36440-119">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="36440-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36440-120">-ParentObject</span></span>
<span data-ttu-id="36440-121">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="36440-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36440-122">-ResourceGroupName</span></span>
<span data-ttu-id="36440-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="36440-123">Resource Group name.</span></span>

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

### <span data-ttu-id="36440-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36440-124">-ResourceId</span></span>
<span data-ttu-id="36440-125">ID de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="36440-125">Shared private link resource id</span></span>

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

### <span data-ttu-id="36440-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="36440-126">-ServiceName</span></span>
<span data-ttu-id="36440-127">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="36440-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="36440-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="36440-128">-Confirm</span></span>
<span data-ttu-id="36440-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36440-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36440-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36440-130">-WhatIf</span></span>
<span data-ttu-id="36440-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="36440-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36440-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36440-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36440-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36440-133">CommonParameters</span></span>
<span data-ttu-id="36440-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36440-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36440-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36440-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36440-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="36440-136">INPUTS</span></span>

### <span data-ttu-id="36440-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="36440-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="36440-138">System.String</span><span class="sxs-lookup"><span data-stu-id="36440-138">System.String</span></span>

## <span data-ttu-id="36440-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="36440-139">OUTPUTS</span></span>

### <span data-ttu-id="36440-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="36440-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="36440-141">Notas</span><span class="sxs-lookup"><span data-stu-id="36440-141">NOTES</span></span>

## <span data-ttu-id="36440-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36440-142">RELATED LINKS</span></span>

[<span data-ttu-id="36440-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="36440-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="36440-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="36440-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="36440-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="36440-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
