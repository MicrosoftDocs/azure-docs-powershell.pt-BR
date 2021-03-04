---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888436"
---
# <span data-ttu-id="120c7-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="120c7-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="120c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120c7-102">SYNOPSIS</span></span>
<span data-ttu-id="120c7-103">Cria um recurso de link privado compartilhado para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="120c7-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="120c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="120c7-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="120c7-105">DESCRIPTION</span></span>
<span data-ttu-id="120c7-106">O **New-AzSearchSharedPrivateLinkResource** cria um recurso de link privado compartilhado para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="120c7-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="120c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="120c7-107">EXAMPLES</span></span>

### <span data-ttu-id="120c7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="120c7-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="120c7-109">Este exemplo cria um recurso de link privado compartilhado para o serviço blob de uma conta de armazenamento para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="120c7-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="120c7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="120c7-110">PARAMETERS</span></span>

### <span data-ttu-id="120c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="120c7-111">-AsJob</span></span>
<span data-ttu-id="120c7-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="120c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="120c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120c7-113">-DefaultProfile</span></span>
<span data-ttu-id="120c7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="120c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="120c7-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="120c7-115">-GroupId</span></span>
<span data-ttu-id="120c7-116">ID do grupo de recursos de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="120c7-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="120c7-117">-Name</span></span>
<span data-ttu-id="120c7-118">Recurso de link privado compartilhado da Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="120c7-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="120c7-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="120c7-120">ID de recurso de destino de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="120c7-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="120c7-121">-RequestMessage</span></span>
<span data-ttu-id="120c7-122">Mensagem de solicitação de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="120c7-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="120c7-124">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="120c7-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="120c7-125">-ResourceRegion</span></span>
<span data-ttu-id="120c7-126">(Opcional) Região de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="120c7-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="120c7-127">-ServiceName</span></span>
<span data-ttu-id="120c7-128">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="120c7-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120c7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="120c7-129">-Confirm</span></span>
<span data-ttu-id="120c7-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="120c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120c7-131">-WhatIf</span></span>
<span data-ttu-id="120c7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="120c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120c7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="120c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120c7-134">CommonParameters</span></span>
<span data-ttu-id="120c7-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="120c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120c7-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="120c7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120c7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="120c7-137">INPUTS</span></span>

### <span data-ttu-id="120c7-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="120c7-138">None</span></span>

## <span data-ttu-id="120c7-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="120c7-139">OUTPUTS</span></span>

### <span data-ttu-id="120c7-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="120c7-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="120c7-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="120c7-141">NOTES</span></span>

## <span data-ttu-id="120c7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="120c7-142">RELATED LINKS</span></span>

[<span data-ttu-id="120c7-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="120c7-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="120c7-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="120c7-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="120c7-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="120c7-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
