---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111384"
---
# <span data-ttu-id="6b523-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6b523-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="6b523-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b523-102">SYNOPSIS</span></span>
<span data-ttu-id="6b523-103">Atualize o recurso de link privado compartilhado para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b523-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b523-104">SYNTAX</span></span>

### <span data-ttu-id="6b523-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b523-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b523-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b523-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b523-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b523-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b523-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b523-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b523-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b523-109">DESCRIPTION</span></span>
<span data-ttu-id="6b523-110">Este **Set-AzSearchSharedPrivateLinkResource** atualiza o recurso de link privado compartilhado para o serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b523-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b523-111">EXAMPLES</span></span>

### <span data-ttu-id="6b523-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b523-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="6b523-113">Este exemplo atualiza a mensagem de solicitação do recurso de link privado compartilhado pendente para o serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6b523-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b523-114">PARAMETERS</span></span>

### <span data-ttu-id="6b523-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b523-115">-AsJob</span></span>
<span data-ttu-id="6b523-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6b523-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b523-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b523-117">-DefaultProfile</span></span>
<span data-ttu-id="6b523-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b523-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b523-119">-InputObject</span></span>
<span data-ttu-id="6b523-120">Objeto de entrada de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="6b523-120">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b523-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b523-121">-Name</span></span>
<span data-ttu-id="6b523-122">Recurso de link privado compartilhado da Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="6b523-122">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b523-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b523-123">-ParentObject</span></span>
<span data-ttu-id="6b523-124">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b523-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="6b523-125">-RequestMessage</span></span>
<span data-ttu-id="6b523-126">Mensagem de solicitação de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="6b523-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b523-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b523-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b523-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="6b523-128">Resource Group name.</span></span>

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

### <span data-ttu-id="6b523-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b523-129">-ResourceId</span></span>
<span data-ttu-id="6b523-130">ID de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="6b523-130">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b523-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b523-131">-ServiceName</span></span>
<span data-ttu-id="6b523-132">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b523-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="6b523-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6b523-133">-Confirm</span></span>
<span data-ttu-id="6b523-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b523-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b523-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b523-135">-WhatIf</span></span>
<span data-ttu-id="6b523-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6b523-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b523-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b523-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b523-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b523-138">CommonParameters</span></span>
<span data-ttu-id="6b523-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b523-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b523-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b523-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b523-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b523-141">INPUTS</span></span>

### <span data-ttu-id="6b523-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6b523-142">None</span></span>

## <span data-ttu-id="6b523-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b523-143">OUTPUTS</span></span>

### <span data-ttu-id="6b523-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6b523-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="6b523-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6b523-145">NOTES</span></span>

## <span data-ttu-id="6b523-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b523-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b523-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b523-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="6b523-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b523-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="6b523-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="6b523-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)