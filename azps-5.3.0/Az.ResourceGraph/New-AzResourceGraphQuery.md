---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428016"
---
# <span data-ttu-id="a880b-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="a880b-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="a880b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a880b-102">SYNOPSIS</span></span>
<span data-ttu-id="a880b-103">Criar uma nova consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="a880b-103">Create a new graph query.</span></span>

## <span data-ttu-id="a880b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a880b-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a880b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a880b-105">DESCRIPTION</span></span>
<span data-ttu-id="a880b-106">Criar uma nova consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="a880b-106">Create a new graph query.</span></span>

## <span data-ttu-id="a880b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a880b-107">EXAMPLES</span></span>

### <span data-ttu-id="a880b-108">Exemplo 1: criar uma consulta de gráfico de recursos pelo parâmetro de consulta</span><span class="sxs-lookup"><span data-stu-id="a880b-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="a880b-109">Esse comando cria uma consulta de gráfico de recursos pelo parâmetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="a880b-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="a880b-110">Exemplo 2: criar uma consulta de gráfico de recursos pelo parâmetro de arquivo</span><span class="sxs-lookup"><span data-stu-id="a880b-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="a880b-111">Esse comando cria uma consulta de gráfico de recursos pelo parâmetro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a880b-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="a880b-112">OS</span><span class="sxs-lookup"><span data-stu-id="a880b-112">PARAMETERS</span></span>

### <span data-ttu-id="a880b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a880b-113">-DefaultProfile</span></span>
<span data-ttu-id="a880b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a880b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a880b-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a880b-115">-Description</span></span>
<span data-ttu-id="a880b-116">A descrição de uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="a880b-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="a880b-117">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="a880b-117">-File</span></span>
<span data-ttu-id="a880b-118">O conteúdo do arquivo será passado para o parâmetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="a880b-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="a880b-119">-Local</span><span class="sxs-lookup"><span data-stu-id="a880b-119">-Location</span></span>
<span data-ttu-id="a880b-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="a880b-120">The location of the resource</span></span>

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

### <span data-ttu-id="a880b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a880b-121">-Name</span></span>
<span data-ttu-id="a880b-122">O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="a880b-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="a880b-123">-Consulta</span><span class="sxs-lookup"><span data-stu-id="a880b-123">-Query</span></span>
<span data-ttu-id="a880b-124">KQL consulta que será o gráfico.</span><span class="sxs-lookup"><span data-stu-id="a880b-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="a880b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a880b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a880b-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a880b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="a880b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a880b-127">-SubscriptionId</span></span>
<span data-ttu-id="a880b-128">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a880b-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a880b-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="a880b-129">-Tag</span></span>
<span data-ttu-id="a880b-130">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a880b-130">Resource tags</span></span>

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

### <span data-ttu-id="a880b-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a880b-131">-Confirm</span></span>
<span data-ttu-id="a880b-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a880b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a880b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a880b-133">-WhatIf</span></span>
<span data-ttu-id="a880b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a880b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a880b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a880b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a880b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a880b-136">CommonParameters</span></span>
<span data-ttu-id="a880b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a880b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a880b-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a880b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a880b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a880b-139">INPUTS</span></span>

### <span data-ttu-id="a880b-140">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="a880b-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="a880b-141">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="a880b-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="a880b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a880b-142">OUTPUTS</span></span>

### <span data-ttu-id="a880b-143">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="a880b-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="a880b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a880b-144">NOTES</span></span>

<span data-ttu-id="a880b-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a880b-145">ALIASES</span></span>

## <span data-ttu-id="a880b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a880b-146">RELATED LINKS</span></span>

