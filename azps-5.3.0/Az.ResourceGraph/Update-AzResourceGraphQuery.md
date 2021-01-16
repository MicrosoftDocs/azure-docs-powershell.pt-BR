---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271563"
---
# <span data-ttu-id="c59a2-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="c59a2-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="c59a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c59a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c59a2-103">Atualiza uma consulta de gráfico que já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="c59a2-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="c59a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c59a2-104">SYNTAX</span></span>

### <span data-ttu-id="c59a2-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c59a2-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c59a2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c59a2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c59a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c59a2-107">DESCRIPTION</span></span>
<span data-ttu-id="c59a2-108">Atualiza uma consulta de gráfico que já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="c59a2-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="c59a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c59a2-109">EXAMPLES</span></span>

### <span data-ttu-id="c59a2-110">Exemplo 1: atualizar a consulta de parâmetro e marcar por nome</span><span class="sxs-lookup"><span data-stu-id="c59a2-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="c59a2-111">Esse comando atualiza a consulta de parâmetro e marca por nome.</span><span class="sxs-lookup"><span data-stu-id="c59a2-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="c59a2-112">Exemplo 2: atualizar o arquivo de parâmetro por objeto</span><span class="sxs-lookup"><span data-stu-id="c59a2-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="c59a2-113">Esse comando atualiza a consulta de parâmetro e marca por objeto.</span><span class="sxs-lookup"><span data-stu-id="c59a2-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="c59a2-114">OS</span><span class="sxs-lookup"><span data-stu-id="c59a2-114">PARAMETERS</span></span>

### <span data-ttu-id="c59a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59a2-115">-DefaultProfile</span></span>
<span data-ttu-id="c59a2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c59a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c59a2-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c59a2-117">-Description</span></span>
<span data-ttu-id="c59a2-118">A descrição de uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="c59a2-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="c59a2-119">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="c59a2-119">-File</span></span>
<span data-ttu-id="c59a2-120">O conteúdo do arquivo será passado para o parâmetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="c59a2-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="c59a2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59a2-121">-InputObject</span></span>
<span data-ttu-id="c59a2-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c59a2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c59a2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c59a2-123">-Name</span></span>
<span data-ttu-id="c59a2-124">O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="c59a2-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="c59a2-125">-Consulta</span><span class="sxs-lookup"><span data-stu-id="c59a2-125">-Query</span></span>
<span data-ttu-id="c59a2-126">KQL consulta que será o gráfico.</span><span class="sxs-lookup"><span data-stu-id="c59a2-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="c59a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="c59a2-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c59a2-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c59a2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c59a2-129">-SubscriptionId</span></span>
<span data-ttu-id="c59a2-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c59a2-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="c59a2-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="c59a2-131">-Tag</span></span>
<span data-ttu-id="c59a2-132">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="c59a2-132">Resource tags</span></span>

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

### <span data-ttu-id="c59a2-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c59a2-133">-Confirm</span></span>
<span data-ttu-id="c59a2-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59a2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59a2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59a2-135">-WhatIf</span></span>
<span data-ttu-id="c59a2-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c59a2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59a2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c59a2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59a2-138">CommonParameters</span></span>
<span data-ttu-id="c59a2-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59a2-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c59a2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59a2-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c59a2-141">INPUTS</span></span>

### <span data-ttu-id="c59a2-142">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="c59a2-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="c59a2-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c59a2-143">OUTPUTS</span></span>

### <span data-ttu-id="c59a2-144">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="c59a2-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="c59a2-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c59a2-145">NOTES</span></span>

<span data-ttu-id="c59a2-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c59a2-146">ALIASES</span></span>

<span data-ttu-id="c59a2-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c59a2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c59a2-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c59a2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c59a2-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c59a2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c59a2-150">INPUTobject <IResourceGraphIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c59a2-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c59a2-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c59a2-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c59a2-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c59a2-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c59a2-153">`[ResourceName <String>]`: O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="c59a2-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="c59a2-154">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c59a2-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="c59a2-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c59a2-155">RELATED LINKS</span></span>

