---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263882"
---
# <span data-ttu-id="a1039-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1039-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a1039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1039-102">SYNOPSIS</span></span>
<span data-ttu-id="a1039-103">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1039-103">Gets the workspace.</span></span>

## <span data-ttu-id="a1039-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1039-104">SYNTAX</span></span>

### <span data-ttu-id="a1039-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1039-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1039-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a1039-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1039-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1039-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1039-108">Programação</span><span class="sxs-lookup"><span data-stu-id="a1039-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a1039-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1039-109">DESCRIPTION</span></span>
<span data-ttu-id="a1039-110">Obtém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1039-110">Gets the workspace.</span></span>

## <span data-ttu-id="a1039-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1039-111">EXAMPLES</span></span>

### <span data-ttu-id="a1039-112">Exemplo 1: obter um espaço de trabalho databricks com nome</span><span class="sxs-lookup"><span data-stu-id="a1039-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="a1039-113">Esse comando obtém um espaço de trabalho databricks em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1039-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="a1039-114">Exemplo 2: listar todos os espaços de trabalho databricks em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a1039-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="a1039-115">Esse comando lista todos os espaços de trabalho databricks em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a1039-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="a1039-116">Exemplo 3: listar todos os espaços de trabalho datatijolo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1039-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="a1039-117">Esse comando lista todos os espaços de trabalho databricks em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1039-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="a1039-118">OS</span><span class="sxs-lookup"><span data-stu-id="a1039-118">PARAMETERS</span></span>

### <span data-ttu-id="a1039-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1039-119">-DefaultProfile</span></span>
<span data-ttu-id="a1039-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1039-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1039-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1039-121">-InputObject</span></span>
<span data-ttu-id="a1039-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a1039-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1039-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1039-123">-Name</span></span>
<span data-ttu-id="a1039-124">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1039-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="a1039-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1039-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1039-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1039-126">The name of the resource group.</span></span>
<span data-ttu-id="a1039-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a1039-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a1039-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1039-128">-SubscriptionId</span></span>
<span data-ttu-id="a1039-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a1039-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a1039-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1039-130">CommonParameters</span></span>
<span data-ttu-id="a1039-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1039-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1039-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1039-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1039-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1039-133">INPUTS</span></span>

### <span data-ttu-id="a1039-134">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="a1039-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a1039-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1039-135">OUTPUTS</span></span>

### <span data-ttu-id="a1039-136">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1039-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="a1039-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1039-137">NOTES</span></span>

<span data-ttu-id="a1039-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a1039-138">ALIASES</span></span>

<span data-ttu-id="a1039-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a1039-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1039-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a1039-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1039-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1039-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1039-142">INPUTobject <IDatabricksIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a1039-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1039-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a1039-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1039-144">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1039-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a1039-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1039-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1039-146">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a1039-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1039-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a1039-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1039-148">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1039-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a1039-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1039-149">RELATED LINKS</span></span>

