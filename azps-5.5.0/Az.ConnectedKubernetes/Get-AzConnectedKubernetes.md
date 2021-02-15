---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115453"
---
# <span data-ttu-id="640ff-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="640ff-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="640ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="640ff-102">SYNOPSIS</span></span>
<span data-ttu-id="640ff-103">Retorna as propriedades do cluster conectado especificado, incluindo nome, identidade, propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="640ff-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="640ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="640ff-104">SYNTAX</span></span>

### <span data-ttu-id="640ff-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="640ff-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="640ff-106">Obter</span><span class="sxs-lookup"><span data-stu-id="640ff-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="640ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="640ff-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="640ff-108">Lista</span><span class="sxs-lookup"><span data-stu-id="640ff-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="640ff-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="640ff-109">DESCRIPTION</span></span>
<span data-ttu-id="640ff-110">Retorna as propriedades do cluster conectado especificado, incluindo nome, identidade, propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="640ff-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="640ff-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="640ff-111">EXAMPLES</span></span>

### <span data-ttu-id="640ff-112">Exemplo 1: Obter todas as redes conectadas em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="640ff-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="640ff-113">Esse comando obtém todas as redes conectadas em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="640ff-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="640ff-114">Exemplo 2: Obter todas as rede conectadas sob o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="640ff-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="640ff-115">Esse comando obtém todas as redes conectadas sob o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="640ff-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="640ff-116">Exemplo 3: Obter uma rede conectada</span><span class="sxs-lookup"><span data-stu-id="640ff-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="640ff-117">Esse comando obtém uma rede conectada.</span><span class="sxs-lookup"><span data-stu-id="640ff-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="640ff-118">Exemplo 4: Obter uma rede por objeto conectada</span><span class="sxs-lookup"><span data-stu-id="640ff-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="640ff-119">Esse comando obtém uma rede conectada por objeto.</span><span class="sxs-lookup"><span data-stu-id="640ff-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="640ff-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="640ff-120">PARAMETERS</span></span>

### <span data-ttu-id="640ff-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="640ff-121">-ClusterName</span></span>
<span data-ttu-id="640ff-122">O nome do cluster Desernetes no qual obter é chamado.</span><span class="sxs-lookup"><span data-stu-id="640ff-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="640ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640ff-123">-DefaultProfile</span></span>
<span data-ttu-id="640ff-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="640ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="640ff-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="640ff-125">-InputObject</span></span>
<span data-ttu-id="640ff-126">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="640ff-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="640ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="640ff-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="640ff-128">The name of the resource group.</span></span>
<span data-ttu-id="640ff-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="640ff-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="640ff-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="640ff-130">-SubscriptionId</span></span>
<span data-ttu-id="640ff-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="640ff-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="640ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640ff-132">CommonParameters</span></span>
<span data-ttu-id="640ff-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640ff-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="640ff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640ff-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="640ff-135">INPUTS</span></span>

### <span data-ttu-id="640ff-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="640ff-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="640ff-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="640ff-137">OUTPUTS</span></span>

### <span data-ttu-id="640ff-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="640ff-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="640ff-139">Notas</span><span class="sxs-lookup"><span data-stu-id="640ff-139">NOTES</span></span>

<span data-ttu-id="640ff-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="640ff-140">ALIASES</span></span>

<span data-ttu-id="640ff-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="640ff-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="640ff-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="640ff-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="640ff-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="640ff-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="640ff-144">INPUTOBJECT: <IConnectedKubernetesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="640ff-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="640ff-145">`[ClusterName <String>]`: o nome do cluster Desarnetes no qual se chama obter.</span><span class="sxs-lookup"><span data-stu-id="640ff-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="640ff-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="640ff-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="640ff-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="640ff-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="640ff-148">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="640ff-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="640ff-149">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="640ff-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="640ff-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="640ff-150">RELATED LINKS</span></span>

