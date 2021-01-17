---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428762"
---
# <span data-ttu-id="ec1db-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="ec1db-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="ec1db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec1db-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1db-103">Obtenha uma única consulta de gráfico por meio de seu Resource resourcer.</span><span class="sxs-lookup"><span data-stu-id="ec1db-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="ec1db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec1db-104">SYNTAX</span></span>

### <span data-ttu-id="ec1db-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec1db-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec1db-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ec1db-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec1db-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec1db-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec1db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec1db-108">DESCRIPTION</span></span>
<span data-ttu-id="ec1db-109">Obtenha uma única consulta de gráfico por meio de seu Resource resourcer.</span><span class="sxs-lookup"><span data-stu-id="ec1db-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="ec1db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec1db-110">EXAMPLES</span></span>

### <span data-ttu-id="ec1db-111">Exemplo 1: obter toda a consulta de gráfico de recursos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ec1db-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="ec1db-112">Esse comando obtém toda a consulta de gráfico de recursos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec1db-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="ec1db-113">Exemplo 2: obter uma consulta de gráfico de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="ec1db-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="ec1db-114">Esse comando obtém uma consulta de gráfico de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="ec1db-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="ec1db-115">Exemplo 2: obter uma consulta de gráfico de recursos por objecy</span><span class="sxs-lookup"><span data-stu-id="ec1db-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="ec1db-116">Esse comando obtém uma consulta de gráfico de recursos por objeto.</span><span class="sxs-lookup"><span data-stu-id="ec1db-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="ec1db-117">OS</span><span class="sxs-lookup"><span data-stu-id="ec1db-117">PARAMETERS</span></span>

### <span data-ttu-id="ec1db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1db-118">-DefaultProfile</span></span>
<span data-ttu-id="ec1db-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1db-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec1db-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec1db-120">-InputObject</span></span>
<span data-ttu-id="ec1db-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ec1db-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec1db-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec1db-122">-Name</span></span>
<span data-ttu-id="ec1db-123">O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ec1db-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="ec1db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1db-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec1db-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec1db-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec1db-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec1db-126">-SubscriptionId</span></span>
<span data-ttu-id="ec1db-127">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1db-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="ec1db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1db-128">CommonParameters</span></span>
<span data-ttu-id="ec1db-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec1db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1db-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec1db-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1db-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec1db-131">INPUTS</span></span>

### <span data-ttu-id="ec1db-132">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="ec1db-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="ec1db-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec1db-133">OUTPUTS</span></span>

### <span data-ttu-id="ec1db-134">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="ec1db-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="ec1db-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec1db-135">NOTES</span></span>

<span data-ttu-id="ec1db-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ec1db-136">ALIASES</span></span>

<span data-ttu-id="ec1db-137">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ec1db-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec1db-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ec1db-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec1db-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec1db-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec1db-140">INPUTobject <IResourceGraphIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ec1db-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec1db-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ec1db-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec1db-142">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec1db-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ec1db-143">`[ResourceName <String>]`: O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ec1db-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="ec1db-144">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1db-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="ec1db-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec1db-145">RELATED LINKS</span></span>

