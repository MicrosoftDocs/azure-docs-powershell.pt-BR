---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261109"
---
# <span data-ttu-id="8b5eb-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="8b5eb-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="8b5eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5eb-103">Obtém o emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="8b5eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b5eb-104">SYNTAX</span></span>

### <span data-ttu-id="8b5eb-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b5eb-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b5eb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8b5eb-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8b5eb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8b5eb-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8b5eb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b5eb-108">DESCRIPTION</span></span>
<span data-ttu-id="8b5eb-109">Obtém o emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="8b5eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b5eb-110">EXAMPLES</span></span>

### <span data-ttu-id="8b5eb-111">Exemplo 1: listar todos os pares de vnet em um databricks</span><span class="sxs-lookup"><span data-stu-id="8b5eb-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="8b5eb-112">Esse comando lista todos os pares de vnet em um databricks.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="8b5eb-113">Exemplo 2: obter um emparelhamento via rede virtual</span><span class="sxs-lookup"><span data-stu-id="8b5eb-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="8b5eb-114">Este comando obtém um emparelhamento via rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="8b5eb-115">Exemplo 3: obter um emparelhamento via rede virtual por objeto</span><span class="sxs-lookup"><span data-stu-id="8b5eb-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="8b5eb-116">Esse comando obtém um emparelhamento via rede virtual por objeto.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="8b5eb-117">OS</span><span class="sxs-lookup"><span data-stu-id="8b5eb-117">PARAMETERS</span></span>

### <span data-ttu-id="8b5eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5eb-118">-DefaultProfile</span></span>
<span data-ttu-id="8b5eb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b5eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b5eb-120">-InputObject</span></span>
<span data-ttu-id="8b5eb-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8b5eb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b5eb-122">-Name</span></span>
<span data-ttu-id="8b5eb-123">O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="8b5eb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b5eb-124">-PassThru</span></span>
<span data-ttu-id="8b5eb-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8b5eb-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b5eb-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-127">The name of the resource group.</span></span>
<span data-ttu-id="8b5eb-128">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8b5eb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b5eb-129">-SubscriptionId</span></span>
<span data-ttu-id="8b5eb-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8b5eb-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b5eb-131">-WorkspaceName</span></span>
<span data-ttu-id="8b5eb-132">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="8b5eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5eb-133">CommonParameters</span></span>
<span data-ttu-id="8b5eb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5eb-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b5eb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5eb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b5eb-136">INPUTS</span></span>

### <span data-ttu-id="8b5eb-137">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="8b5eb-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="8b5eb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b5eb-138">OUTPUTS</span></span>

### <span data-ttu-id="8b5eb-139">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8b5eb-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="8b5eb-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b5eb-140">NOTES</span></span>

<span data-ttu-id="8b5eb-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b5eb-141">ALIASES</span></span>

<span data-ttu-id="8b5eb-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8b5eb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b5eb-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b5eb-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b5eb-145">INPUTobject <IDatabricksIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8b5eb-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b5eb-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8b5eb-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b5eb-147">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="8b5eb-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8b5eb-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="8b5eb-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8b5eb-151">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b5eb-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="8b5eb-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b5eb-152">RELATED LINKS</span></span>

