---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110809"
---
# <span data-ttu-id="8a942-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="8a942-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="8a942-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a942-102">SYNOPSIS</span></span>
<span data-ttu-id="8a942-103">Atualiza uma consulta de gráfico que já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="8a942-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="8a942-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a942-104">SYNTAX</span></span>

### <span data-ttu-id="8a942-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a942-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a942-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8a942-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a942-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a942-107">DESCRIPTION</span></span>
<span data-ttu-id="8a942-108">Atualiza uma consulta de gráfico que já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="8a942-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="8a942-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a942-109">EXAMPLES</span></span>

### <span data-ttu-id="8a942-110">Exemplo 1: Atualizar a consulta de parâmetro e marcar por nome</span><span class="sxs-lookup"><span data-stu-id="8a942-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="8a942-111">Esse comando atualiza a consulta de parâmetro e marca por nome.</span><span class="sxs-lookup"><span data-stu-id="8a942-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="8a942-112">Exemplo 2: Atualizar o arquivo de parâmetro por objeto</span><span class="sxs-lookup"><span data-stu-id="8a942-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="8a942-113">Esse comando atualiza a consulta de parâmetro e marca por objeto.</span><span class="sxs-lookup"><span data-stu-id="8a942-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="8a942-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a942-114">PARAMETERS</span></span>

### <span data-ttu-id="8a942-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a942-115">-DefaultProfile</span></span>
<span data-ttu-id="8a942-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a942-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8a942-117">-Description</span></span>
<span data-ttu-id="8a942-118">A descrição de uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="8a942-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="8a942-119">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="8a942-119">-File</span></span>
<span data-ttu-id="8a942-120">O conteúdo do arquivo será passado para o parâmetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="8a942-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="8a942-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a942-121">-InputObject</span></span>
<span data-ttu-id="8a942-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8a942-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a942-123">-Name</span></span>
<span data-ttu-id="8a942-124">O nome do recurso Consulta de Gráfico.</span><span class="sxs-lookup"><span data-stu-id="8a942-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="8a942-125">-Query</span></span>
<span data-ttu-id="8a942-126">Consulta KQL que será gráfica.</span><span class="sxs-lookup"><span data-stu-id="8a942-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="8a942-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a942-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a942-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a942-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a942-129">-SubscriptionId</span></span>
<span data-ttu-id="8a942-130">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a942-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a942-131">-Tag</span></span>
<span data-ttu-id="8a942-132">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="8a942-132">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a942-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8a942-133">-Confirm</span></span>
<span data-ttu-id="8a942-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a942-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a942-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a942-135">-WhatIf</span></span>
<span data-ttu-id="8a942-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8a942-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a942-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a942-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a942-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a942-138">CommonParameters</span></span>
<span data-ttu-id="8a942-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a942-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a942-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a942-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a942-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a942-141">INPUTS</span></span>

### <span data-ttu-id="8a942-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="8a942-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="8a942-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a942-143">OUTPUTS</span></span>

### <span data-ttu-id="8a942-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="8a942-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="8a942-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8a942-145">NOTES</span></span>

<span data-ttu-id="8a942-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="8a942-146">ALIASES</span></span>

<span data-ttu-id="8a942-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8a942-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a942-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8a942-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a942-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a942-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a942-150">INPUTOBJECT: <IResourceGraphIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8a942-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a942-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8a942-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a942-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a942-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8a942-153">`[ResourceName <String>]`: o nome do recurso Consulta de Gráfico.</span><span class="sxs-lookup"><span data-stu-id="8a942-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="8a942-154">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a942-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="8a942-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a942-155">RELATED LINKS</span></span>

