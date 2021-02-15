---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118794"
---
# <span data-ttu-id="4fc54-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="4fc54-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="4fc54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fc54-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc54-103">Obtém o espaço de trabalho da vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="4fc54-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="4fc54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fc54-104">SYNTAX</span></span>

### <span data-ttu-id="4fc54-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4fc54-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4fc54-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4fc54-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4fc54-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4fc54-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4fc54-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fc54-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc54-109">Obtém o espaço de trabalho da vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="4fc54-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="4fc54-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4fc54-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc54-111">Exemplo 1: Listar todos os pares de vnet em um databções</span><span class="sxs-lookup"><span data-stu-id="4fc54-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="4fc54-112">Esse comando lista todos os pares de vnet sob um datab peering.</span><span class="sxs-lookup"><span data-stu-id="4fc54-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="4fc54-113">Exemplo 2: Obter um par de vnet</span><span class="sxs-lookup"><span data-stu-id="4fc54-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="4fc54-114">Esse comando obtém um par de vnet.</span><span class="sxs-lookup"><span data-stu-id="4fc54-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="4fc54-115">Exemplo 3: Obter um ponto de vnet por objeto</span><span class="sxs-lookup"><span data-stu-id="4fc54-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="4fc54-116">Esse comando obtém um ponto de vnet por objeto.</span><span class="sxs-lookup"><span data-stu-id="4fc54-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="4fc54-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fc54-117">PARAMETERS</span></span>

### <span data-ttu-id="4fc54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc54-118">-DefaultProfile</span></span>
<span data-ttu-id="4fc54-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fc54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc54-120">-InputObject</span></span>
<span data-ttu-id="4fc54-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4fc54-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4fc54-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fc54-122">-Name</span></span>
<span data-ttu-id="4fc54-123">O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4fc54-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="4fc54-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fc54-124">-PassThru</span></span>
<span data-ttu-id="4fc54-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4fc54-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4fc54-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc54-126">-ResourceGroupName</span></span>
<span data-ttu-id="4fc54-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fc54-127">The name of the resource group.</span></span>
<span data-ttu-id="4fc54-128">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fc54-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4fc54-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fc54-129">-SubscriptionId</span></span>
<span data-ttu-id="4fc54-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4fc54-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4fc54-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4fc54-131">-WorkspaceName</span></span>
<span data-ttu-id="4fc54-132">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4fc54-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="4fc54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc54-133">CommonParameters</span></span>
<span data-ttu-id="4fc54-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc54-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc54-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc54-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4fc54-136">INPUTS</span></span>

### <span data-ttu-id="4fc54-137">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="4fc54-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="4fc54-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="4fc54-138">OUTPUTS</span></span>

### <span data-ttu-id="4fc54-139">Microsoft.Azure.PowerShell.Cmdlets.Datab sérvios.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fc54-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="4fc54-140">Notas</span><span class="sxs-lookup"><span data-stu-id="4fc54-140">NOTES</span></span>

<span data-ttu-id="4fc54-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="4fc54-141">ALIASES</span></span>

<span data-ttu-id="4fc54-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4fc54-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4fc54-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4fc54-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4fc54-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4fc54-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4fc54-145">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4fc54-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4fc54-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4fc54-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4fc54-147">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4fc54-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="4fc54-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fc54-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4fc54-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fc54-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="4fc54-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4fc54-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4fc54-151">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4fc54-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="4fc54-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fc54-152">RELATED LINKS</span></span>

