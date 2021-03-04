---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893218"
---
# <span data-ttu-id="74280-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="74280-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="74280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74280-102">SYNOPSIS</span></span>
<span data-ttu-id="74280-103">Retorna as propriedades do cluster conectado especificado, incluindo nome, identidade, propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="74280-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="74280-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74280-104">SYNTAX</span></span>

### <span data-ttu-id="74280-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="74280-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74280-106">Obter</span><span class="sxs-lookup"><span data-stu-id="74280-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74280-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74280-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="74280-108">Listar</span><span class="sxs-lookup"><span data-stu-id="74280-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="74280-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74280-109">DESCRIPTION</span></span>
<span data-ttu-id="74280-110">Retorna as propriedades do cluster conectado especificado, incluindo nome, identidade, propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="74280-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="74280-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74280-111">EXAMPLES</span></span>

### <span data-ttu-id="74280-112">Exemplo 1: Obter todos os kubernetes conectados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="74280-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="74280-113">Este comando obtém todos os kubernetes conectados em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="74280-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="74280-114">Exemplo 2: Obter todos os kubernetes conectados no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="74280-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="74280-115">Esse comando obtém todos os kubernetes conectados no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74280-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="74280-116">Exemplo 3: Obter um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="74280-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="74280-117">Este comando obtém um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="74280-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="74280-118">Exemplo 4: Obter um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="74280-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="74280-119">Este comando obtém um kubernetes conectado por objeto.</span><span class="sxs-lookup"><span data-stu-id="74280-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="74280-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74280-120">PARAMETERS</span></span>

### <span data-ttu-id="74280-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="74280-121">-ClusterName</span></span>
<span data-ttu-id="74280-122">O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="74280-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="74280-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74280-123">-DefaultProfile</span></span>
<span data-ttu-id="74280-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74280-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74280-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74280-125">-InputObject</span></span>
<span data-ttu-id="74280-126">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="74280-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74280-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74280-127">-ResourceGroupName</span></span>
<span data-ttu-id="74280-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74280-128">The name of the resource group.</span></span>
<span data-ttu-id="74280-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="74280-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="74280-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74280-130">-SubscriptionId</span></span>
<span data-ttu-id="74280-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="74280-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="74280-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74280-132">CommonParameters</span></span>
<span data-ttu-id="74280-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74280-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74280-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74280-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74280-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74280-135">INPUTS</span></span>

### <span data-ttu-id="74280-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="74280-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="74280-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74280-137">OUTPUTS</span></span>

### <span data-ttu-id="74280-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="74280-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="74280-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="74280-139">NOTES</span></span>

<span data-ttu-id="74280-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="74280-140">ALIASES</span></span>

<span data-ttu-id="74280-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="74280-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74280-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="74280-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74280-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74280-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74280-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="74280-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74280-145">`[ClusterName <String>]`: O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="74280-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="74280-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="74280-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74280-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74280-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="74280-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="74280-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="74280-149">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="74280-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="74280-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74280-150">RELATED LINKS</span></span>

