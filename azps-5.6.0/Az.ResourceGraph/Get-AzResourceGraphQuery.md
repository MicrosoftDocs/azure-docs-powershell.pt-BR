---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891671"
---
# <span data-ttu-id="52c9d-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="52c9d-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="52c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="52c9d-103">Obter uma única consulta de gráfico pelo resourceName.</span><span class="sxs-lookup"><span data-stu-id="52c9d-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="52c9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52c9d-104">SYNTAX</span></span>

### <span data-ttu-id="52c9d-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52c9d-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="52c9d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="52c9d-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52c9d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52c9d-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="52c9d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52c9d-108">DESCRIPTION</span></span>
<span data-ttu-id="52c9d-109">Obter uma única consulta de gráfico pelo resourceName.</span><span class="sxs-lookup"><span data-stu-id="52c9d-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="52c9d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52c9d-110">EXAMPLES</span></span>

### <span data-ttu-id="52c9d-111">Exemplo 1: Obter todas as consultas de gráfico de recursos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="52c9d-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="52c9d-112">Esse comando obtém toda a consulta de gráfico de recursos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52c9d-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="52c9d-113">Exemplo 2: Obter uma consulta de gráfico de recursos pelo nome</span><span class="sxs-lookup"><span data-stu-id="52c9d-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="52c9d-114">Este comando obtém uma consulta de gráfico de recursos pelo nome.</span><span class="sxs-lookup"><span data-stu-id="52c9d-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="52c9d-115">Exemplo 2: Obter uma consulta de gráfico de recursos por objeto</span><span class="sxs-lookup"><span data-stu-id="52c9d-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="52c9d-116">Este comando obtém uma consulta de gráfico de recursos por objeto.</span><span class="sxs-lookup"><span data-stu-id="52c9d-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="52c9d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52c9d-117">PARAMETERS</span></span>

### <span data-ttu-id="52c9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c9d-118">-DefaultProfile</span></span>
<span data-ttu-id="52c9d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52c9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c9d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52c9d-120">-InputObject</span></span>
<span data-ttu-id="52c9d-121">Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="52c9d-121">Identity Parameter</span></span>

<span data-ttu-id="52c9d-122">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52c9d-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52c9d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="52c9d-123">-Name</span></span>
<span data-ttu-id="52c9d-124">O nome do recurso Consulta do Graph.</span><span class="sxs-lookup"><span data-stu-id="52c9d-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="52c9d-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52c9d-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c9d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52c9d-127">-SubscriptionId</span></span>
<span data-ttu-id="52c9d-128">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="52c9d-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c9d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c9d-129">CommonParameters</span></span>
<span data-ttu-id="52c9d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c9d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c9d-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52c9d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c9d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52c9d-132">INPUTS</span></span>

### <span data-ttu-id="52c9d-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="52c9d-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="52c9d-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52c9d-134">OUTPUTS</span></span>

### <span data-ttu-id="52c9d-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="52c9d-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="52c9d-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="52c9d-136">NOTES</span></span>

<span data-ttu-id="52c9d-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52c9d-137">ALIASES</span></span>

<span data-ttu-id="52c9d-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="52c9d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52c9d-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="52c9d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52c9d-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52c9d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52c9d-141">INPUTOBJECT <IResourceGraphIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="52c9d-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52c9d-142">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="52c9d-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52c9d-143">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52c9d-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="52c9d-144">`[ResourceName <String>]`: O nome do recurso Consulta do Graph.</span><span class="sxs-lookup"><span data-stu-id="52c9d-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="52c9d-145">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="52c9d-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="52c9d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52c9d-146">RELATED LINKS</span></span>

