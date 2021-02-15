---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118793"
---
# <span data-ttu-id="fcde5-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="fcde5-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="fcde5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcde5-102">SYNOPSIS</span></span>
<span data-ttu-id="fcde5-103">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcde5-103">Gets the workspace.</span></span>

## <span data-ttu-id="fcde5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcde5-104">SYNTAX</span></span>

### <span data-ttu-id="fcde5-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fcde5-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fcde5-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fcde5-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fcde5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fcde5-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fcde5-108">Lista</span><span class="sxs-lookup"><span data-stu-id="fcde5-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fcde5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcde5-109">DESCRIPTION</span></span>
<span data-ttu-id="fcde5-110">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcde5-110">Gets the workspace.</span></span>

## <span data-ttu-id="fcde5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fcde5-111">EXAMPLES</span></span>

### <span data-ttu-id="fcde5-112">Exemplo 1: Obter um espaço de trabalho Datab fredericks com nome</span><span class="sxs-lookup"><span data-stu-id="fcde5-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="fcde5-113">Esse comando obtém um espaço de trabalho Databções em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcde5-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="fcde5-114">Exemplo 2: Listar todos os espaços de trabalho databéticos em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="fcde5-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="fcde5-115">Esse comando lista todos os espaços de trabalho Datab adobe em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="fcde5-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="fcde5-116">Exemplo 3: Listar todos os espaços de trabalho databéticos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fcde5-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="fcde5-117">Esse comando lista todos os espaços de trabalho Databções em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcde5-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="fcde5-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcde5-118">PARAMETERS</span></span>

### <span data-ttu-id="fcde5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcde5-119">-DefaultProfile</span></span>
<span data-ttu-id="fcde5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcde5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcde5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcde5-121">-InputObject</span></span>
<span data-ttu-id="fcde5-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fcde5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcde5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcde5-123">-Name</span></span>
<span data-ttu-id="fcde5-124">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcde5-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="fcde5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcde5-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcde5-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcde5-126">The name of the resource group.</span></span>
<span data-ttu-id="fcde5-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fcde5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fcde5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcde5-128">-SubscriptionId</span></span>
<span data-ttu-id="fcde5-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fcde5-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fcde5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcde5-130">CommonParameters</span></span>
<span data-ttu-id="fcde5-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcde5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcde5-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcde5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcde5-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="fcde5-133">INPUTS</span></span>

### <span data-ttu-id="fcde5-134">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="fcde5-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="fcde5-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="fcde5-135">OUTPUTS</span></span>

### <span data-ttu-id="fcde5-136">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="fcde5-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="fcde5-137">Notas</span><span class="sxs-lookup"><span data-stu-id="fcde5-137">NOTES</span></span>

<span data-ttu-id="fcde5-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="fcde5-138">ALIASES</span></span>

<span data-ttu-id="fcde5-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="fcde5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcde5-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fcde5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcde5-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fcde5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcde5-142">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="fcde5-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fcde5-143">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fcde5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fcde5-144">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcde5-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="fcde5-145">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcde5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fcde5-146">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fcde5-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="fcde5-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fcde5-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fcde5-148">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fcde5-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="fcde5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcde5-149">RELATED LINKS</span></span>

