---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: ec44b1ace55a36ebaa56c8b0242db485581c5e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887194"
---
# <span data-ttu-id="c372c-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c372c-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c372c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c372c-102">SYNOPSIS</span></span>
<span data-ttu-id="c372c-103">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c372c-103">Gets the workspace.</span></span>

## <span data-ttu-id="c372c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c372c-104">SYNTAX</span></span>

### <span data-ttu-id="c372c-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c372c-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c372c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c372c-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c372c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c372c-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c372c-108">Listar</span><span class="sxs-lookup"><span data-stu-id="c372c-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c372c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c372c-109">DESCRIPTION</span></span>
<span data-ttu-id="c372c-110">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c372c-110">Gets the workspace.</span></span>

## <span data-ttu-id="c372c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c372c-111">EXAMPLES</span></span>

### <span data-ttu-id="c372c-112">Exemplo 1: Obter um espaço de trabalho Databricks com nome</span><span class="sxs-lookup"><span data-stu-id="c372c-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="c372c-113">Esse comando obtém um espaço de trabalho Databricks em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c372c-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="c372c-114">Exemplo 2: Listar todos os espaços de trabalho Databricks em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c372c-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="c372c-115">Este comando lista todos os espaços de trabalho Databricks em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c372c-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="c372c-116">Exemplo 3: Listar todos os espaços de trabalho Databricks em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c372c-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="c372c-117">Este comando lista todos os espaços de trabalho Databricks em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c372c-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="c372c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c372c-118">PARAMETERS</span></span>

### <span data-ttu-id="c372c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c372c-119">-DefaultProfile</span></span>
<span data-ttu-id="c372c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c372c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c372c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c372c-121">-InputObject</span></span>
<span data-ttu-id="c372c-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c372c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c372c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c372c-123">-Name</span></span>
<span data-ttu-id="c372c-124">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c372c-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c372c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c372c-125">-ResourceGroupName</span></span>
<span data-ttu-id="c372c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c372c-126">The name of the resource group.</span></span>
<span data-ttu-id="c372c-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c372c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c372c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c372c-128">-SubscriptionId</span></span>
<span data-ttu-id="c372c-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c372c-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c372c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c372c-130">CommonParameters</span></span>
<span data-ttu-id="c372c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c372c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c372c-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c372c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c372c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c372c-133">INPUTS</span></span>

### <span data-ttu-id="c372c-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="c372c-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c372c-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c372c-135">OUTPUTS</span></span>

### <span data-ttu-id="c372c-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c372c-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c372c-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="c372c-137">NOTES</span></span>

<span data-ttu-id="c372c-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c372c-138">ALIASES</span></span>

<span data-ttu-id="c372c-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="c372c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c372c-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c372c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c372c-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c372c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c372c-142">INPUTOBJECT <IDatabricksIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="c372c-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c372c-143">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c372c-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c372c-144">`[PeeringName <String>]`: O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c372c-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c372c-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c372c-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c372c-146">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c372c-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="c372c-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c372c-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c372c-148">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c372c-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c372c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c372c-149">RELATED LINKS</span></span>

