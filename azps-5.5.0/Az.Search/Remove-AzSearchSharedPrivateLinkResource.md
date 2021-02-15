---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118115"
---
# <span data-ttu-id="2a9a1-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2a9a1-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="2a9a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9a1-103">Remova o recurso de link privado compartilhado do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2a9a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a9a1-104">SYNTAX</span></span>

### <span data-ttu-id="2a9a1-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2a9a1-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9a1-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a9a1-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a9a1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a9a1-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a9a1-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a9a1-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a9a1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a9a1-109">DESCRIPTION</span></span>
<span data-ttu-id="2a9a1-110">O cmdlet **Remove-AzSearchSharedPrivateLinkResource** remove o recurso de link privado compartilhado do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2a9a1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a9a1-111">EXAMPLES</span></span>

### <span data-ttu-id="2a9a1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a9a1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2a9a1-113">Este exemplo exclui um recurso de vínculo privado compartilhado pelo nome do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2a9a1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a9a1-114">PARAMETERS</span></span>

### <span data-ttu-id="2a9a1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a9a1-115">-AsJob</span></span>
<span data-ttu-id="2a9a1-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2a9a1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a9a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9a1-117">-DefaultProfile</span></span>
<span data-ttu-id="2a9a1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9a1-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2a9a1-119">-Force</span></span>
<span data-ttu-id="2a9a1-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2a9a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a9a1-121">-InputObject</span></span>
<span data-ttu-id="2a9a1-122">Objeto de entrada de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="2a9a1-122">Shared private link resource input object</span></span>

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

### <span data-ttu-id="2a9a1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a9a1-123">-Name</span></span>
<span data-ttu-id="2a9a1-124">Recurso de link privado compartilhado da Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="2a9a1-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="2a9a1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2a9a1-125">-ParentObject</span></span>
<span data-ttu-id="2a9a1-126">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="2a9a1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a9a1-127">-PassThru</span></span>
<span data-ttu-id="2a9a1-128">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2a9a1-129">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2a9a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="2a9a1-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-131">Resource Group name.</span></span>

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

### <span data-ttu-id="2a9a1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a9a1-132">-ResourceId</span></span>
<span data-ttu-id="2a9a1-133">ID de recurso de link privado compartilhado</span><span class="sxs-lookup"><span data-stu-id="2a9a1-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="2a9a1-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2a9a1-134">-ServiceName</span></span>
<span data-ttu-id="2a9a1-135">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="2a9a1-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2a9a1-136">-Confirm</span></span>
<span data-ttu-id="2a9a1-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a9a1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a9a1-138">-WhatIf</span></span>
<span data-ttu-id="2a9a1-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a9a1-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a9a1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9a1-141">CommonParameters</span></span>
<span data-ttu-id="2a9a1-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9a1-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a9a1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9a1-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="2a9a1-144">INPUTS</span></span>

### <span data-ttu-id="2a9a1-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2a9a1-145">None</span></span>

## <span data-ttu-id="2a9a1-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="2a9a1-146">OUTPUTS</span></span>

### <span data-ttu-id="2a9a1-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a9a1-147">System.Boolean</span></span>

## <span data-ttu-id="2a9a1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="2a9a1-148">NOTES</span></span>

## <span data-ttu-id="2a9a1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a9a1-149">RELATED LINKS</span></span>

[<span data-ttu-id="2a9a1-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2a9a1-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="2a9a1-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2a9a1-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="2a9a1-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="2a9a1-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)