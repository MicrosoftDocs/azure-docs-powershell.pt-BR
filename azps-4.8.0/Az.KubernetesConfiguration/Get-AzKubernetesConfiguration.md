---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111868"
---
# <span data-ttu-id="5e40f-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e40f-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="5e40f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e40f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e40f-103">Obtém detalhes da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="5e40f-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="5e40f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e40f-104">SYNTAX</span></span>

### <span data-ttu-id="5e40f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e40f-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e40f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5e40f-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e40f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e40f-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e40f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e40f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e40f-109">Obtém detalhes da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="5e40f-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="5e40f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e40f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e40f-111">Exemplo 1: obter todas as configurações do cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="5e40f-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="5e40f-112">Esse comando obtém todas as configurações do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5e40f-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="5e40f-113">Exemplo 2: obter uma configuração do kubernetes cluster por nome</span><span class="sxs-lookup"><span data-stu-id="5e40f-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="5e40f-114">Esse comando obtém uma configuração do cluster kubernetes por nome.</span><span class="sxs-lookup"><span data-stu-id="5e40f-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="5e40f-115">Exemplo 3: obter uma configuração do cluster kubernetes por objeto</span><span class="sxs-lookup"><span data-stu-id="5e40f-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="5e40f-116">Esse comando obtém uma configuração do kubernetes cluster por objeto.</span><span class="sxs-lookup"><span data-stu-id="5e40f-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="5e40f-117">Exemplo 4: obter uma configuração do cluster kubernetes por pipeline</span><span class="sxs-lookup"><span data-stu-id="5e40f-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="5e40f-118">Esse comando obtém uma configuração de cluster de kubernetes por pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e40f-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="5e40f-119">OS</span><span class="sxs-lookup"><span data-stu-id="5e40f-119">PARAMETERS</span></span>

### <span data-ttu-id="5e40f-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5e40f-120">-ClusterName</span></span>
<span data-ttu-id="5e40f-121">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5e40f-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="5e40f-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="5e40f-122">-ClusterRp</span></span>
<span data-ttu-id="5e40f-123">O kubernetes do cluster do RP-Microsoft. ContainerService (para clusters AKS) ou Microsoft. kubernetes (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="5e40f-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="5e40f-124">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="5e40f-124">-ClusterType</span></span>
<span data-ttu-id="5e40f-125">O nome do recurso de cluster kubernetes-managedClusters (para clusters AKS) ou connectedClusters (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="5e40f-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="5e40f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e40f-126">-DefaultProfile</span></span>
<span data-ttu-id="5e40f-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e40f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e40f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e40f-128">-InputObject</span></span>
<span data-ttu-id="5e40f-129">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5e40f-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e40f-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e40f-130">-Name</span></span>
<span data-ttu-id="5e40f-131">Nome da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="5e40f-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e40f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e40f-132">-ResourceGroupName</span></span>
<span data-ttu-id="5e40f-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e40f-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e40f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e40f-134">-SubscriptionId</span></span>
<span data-ttu-id="5e40f-135">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e40f-135">The Azure subscription ID.</span></span>
<span data-ttu-id="5e40f-136">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="5e40f-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="5e40f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e40f-137">CommonParameters</span></span>
<span data-ttu-id="5e40f-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e40f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e40f-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e40f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e40f-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e40f-140">INPUTS</span></span>

### <span data-ttu-id="5e40f-141">Microsoft. Azure. PowerShell. cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="5e40f-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="5e40f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e40f-142">OUTPUTS</span></span>

### <span data-ttu-id="5e40f-143">Microsoft. Azure. PowerShell. cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e40f-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="5e40f-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e40f-144">NOTES</span></span>

<span data-ttu-id="5e40f-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5e40f-145">ALIASES</span></span>

<span data-ttu-id="5e40f-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5e40f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e40f-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5e40f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e40f-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e40f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e40f-149">INPUTobject <IKubernetesConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5e40f-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e40f-150">`[ClusterName <String>]`: O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5e40f-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="5e40f-151">`[ClusterResourceName <String>]`: O nome do recurso de cluster kubernetes-managedClusters (para clusters AKS) ou connectedClusters (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="5e40f-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="5e40f-152">`[ClusterRp <String>]`: O kubernetes do cluster do RP-Microsoft. ContainerService (para clusters AKS) ou Microsoft. kubernetes (para clusters do K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="5e40f-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="5e40f-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5e40f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e40f-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e40f-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5e40f-155">`[SourceControlConfigurationName <String>]`: Nome da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="5e40f-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="5e40f-156">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e40f-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="5e40f-157">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="5e40f-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="5e40f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e40f-158">RELATED LINKS</span></span>

