---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887195"
---
# <span data-ttu-id="9283d-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="9283d-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="9283d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9283d-102">SYNOPSIS</span></span>
<span data-ttu-id="9283d-103">Obtém o espaço de trabalho vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="9283d-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="9283d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9283d-104">SYNTAX</span></span>

### <span data-ttu-id="9283d-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9283d-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9283d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9283d-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9283d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9283d-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9283d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9283d-108">DESCRIPTION</span></span>
<span data-ttu-id="9283d-109">Obtém o espaço de trabalho vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="9283d-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="9283d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9283d-110">EXAMPLES</span></span>

### <span data-ttu-id="9283d-111">Exemplo 1: Listar todos os pares de vnet em um databricks</span><span class="sxs-lookup"><span data-stu-id="9283d-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="9283d-112">Este comando lista todos os pares de vnet em um databricks.</span><span class="sxs-lookup"><span data-stu-id="9283d-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="9283d-113">Exemplo 2: Obter um par de vnet</span><span class="sxs-lookup"><span data-stu-id="9283d-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="9283d-114">Este comando obtém um par de vnet.</span><span class="sxs-lookup"><span data-stu-id="9283d-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="9283d-115">Exemplo 3: Obter um par de vnet por objeto</span><span class="sxs-lookup"><span data-stu-id="9283d-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="9283d-116">Este comando obtém um ponto de vnet por objeto.</span><span class="sxs-lookup"><span data-stu-id="9283d-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="9283d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9283d-117">PARAMETERS</span></span>

### <span data-ttu-id="9283d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9283d-118">-DefaultProfile</span></span>
<span data-ttu-id="9283d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9283d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9283d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9283d-120">-InputObject</span></span>
<span data-ttu-id="9283d-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9283d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9283d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9283d-122">-Name</span></span>
<span data-ttu-id="9283d-123">O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9283d-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="9283d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9283d-124">-PassThru</span></span>
<span data-ttu-id="9283d-125">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9283d-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9283d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9283d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9283d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9283d-127">The name of the resource group.</span></span>
<span data-ttu-id="9283d-128">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9283d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9283d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9283d-129">-SubscriptionId</span></span>
<span data-ttu-id="9283d-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9283d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9283d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9283d-131">-WorkspaceName</span></span>
<span data-ttu-id="9283d-132">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9283d-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="9283d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9283d-133">CommonParameters</span></span>
<span data-ttu-id="9283d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9283d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9283d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9283d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9283d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9283d-136">INPUTS</span></span>

### <span data-ttu-id="9283d-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="9283d-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="9283d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9283d-138">OUTPUTS</span></span>

### <span data-ttu-id="9283d-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="9283d-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="9283d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="9283d-140">NOTES</span></span>

<span data-ttu-id="9283d-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9283d-141">ALIASES</span></span>

<span data-ttu-id="9283d-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9283d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9283d-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9283d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9283d-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9283d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9283d-145">INPUTOBJECT <IDatabricksIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="9283d-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9283d-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9283d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9283d-147">`[PeeringName <String>]`: O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9283d-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="9283d-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9283d-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9283d-149">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9283d-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="9283d-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="9283d-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9283d-151">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9283d-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="9283d-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9283d-152">RELATED LINKS</span></span>

