---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116753"
---
# <span data-ttu-id="5fb55-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="5fb55-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="5fb55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fb55-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb55-103">Retorna as propriedades do cluster conectado especificado, incluindo o nome, a identidade, as propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="5fb55-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="5fb55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fb55-104">SYNTAX</span></span>

### <span data-ttu-id="5fb55-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fb55-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5fb55-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5fb55-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5fb55-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5fb55-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fb55-108">Programação</span><span class="sxs-lookup"><span data-stu-id="5fb55-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5fb55-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fb55-109">DESCRIPTION</span></span>
<span data-ttu-id="5fb55-110">Retorna as propriedades do cluster conectado especificado, incluindo o nome, a identidade, as propriedades e detalhes adicionais do cluster.</span><span class="sxs-lookup"><span data-stu-id="5fb55-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="5fb55-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fb55-111">EXAMPLES</span></span>

### <span data-ttu-id="5fb55-112">Exemplo 1: obter todos os kubernetes conectados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="5fb55-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="5fb55-113">Este comando obtém todos os kubernetes conectados em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5fb55-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="5fb55-114">Exemplo 2: obter todas as kubernetes conectadas abaixo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5fb55-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="5fb55-115">Esse comando obtém todos os kubernetes conectados no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fb55-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="5fb55-116">Exemplo 3: obter um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="5fb55-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="5fb55-117">Este comando obtém um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="5fb55-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="5fb55-118">Exemplo 4: obter um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="5fb55-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="5fb55-119">Esse comando obtém um kubernetes conectado por objeto.</span><span class="sxs-lookup"><span data-stu-id="5fb55-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="5fb55-120">OS</span><span class="sxs-lookup"><span data-stu-id="5fb55-120">PARAMETERS</span></span>

### <span data-ttu-id="5fb55-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5fb55-121">-ClusterName</span></span>
<span data-ttu-id="5fb55-122">O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="5fb55-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="5fb55-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb55-123">-DefaultProfile</span></span>
<span data-ttu-id="5fb55-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb55-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb55-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fb55-125">-InputObject</span></span>
<span data-ttu-id="5fb55-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5fb55-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5fb55-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb55-127">-ResourceGroupName</span></span>
<span data-ttu-id="5fb55-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fb55-128">The name of the resource group.</span></span>
<span data-ttu-id="5fb55-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5fb55-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5fb55-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fb55-130">-SubscriptionId</span></span>
<span data-ttu-id="5fb55-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5fb55-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5fb55-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb55-132">CommonParameters</span></span>
<span data-ttu-id="5fb55-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb55-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb55-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fb55-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb55-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fb55-135">INPUTS</span></span>

### <span data-ttu-id="5fb55-136">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="5fb55-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="5fb55-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fb55-137">OUTPUTS</span></span>

### <span data-ttu-id="5fb55-138">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="5fb55-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="5fb55-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fb55-139">NOTES</span></span>

<span data-ttu-id="5fb55-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5fb55-140">ALIASES</span></span>

<span data-ttu-id="5fb55-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5fb55-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fb55-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5fb55-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fb55-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fb55-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fb55-144">INPUTobject <IConnectedKubernetesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5fb55-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fb55-145">`[ClusterName <String>]`: O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="5fb55-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="5fb55-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5fb55-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fb55-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fb55-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5fb55-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5fb55-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="5fb55-149">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5fb55-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5fb55-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fb55-150">RELATED LINKS</span></span>

