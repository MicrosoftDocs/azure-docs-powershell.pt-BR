---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 8cbf938917f26b1229b5c18d25448da4df3bb5b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888490"
---
# <span data-ttu-id="dfb66-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfb66-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="dfb66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb66-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb66-103">Obtém detalhes da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="dfb66-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dfb66-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dfb66-104">SYNTAX</span></span>

### <span data-ttu-id="dfb66-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dfb66-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfb66-106">Obter</span><span class="sxs-lookup"><span data-stu-id="dfb66-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfb66-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfb66-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb66-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfb66-108">DESCRIPTION</span></span>
<span data-ttu-id="dfb66-109">Obtém detalhes da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="dfb66-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dfb66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfb66-110">EXAMPLES</span></span>

### <span data-ttu-id="dfb66-111">Exemplo 1: Obter todas as configurações do cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="dfb66-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="dfb66-112">Este comando obtém todas as configurações do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dfb66-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="dfb66-113">Exemplo 2: Obter uma configuração do cluster kubernetes pelo nome</span><span class="sxs-lookup"><span data-stu-id="dfb66-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="dfb66-114">Este comando obtém uma configuração do cluster kubernetes pelo nome.</span><span class="sxs-lookup"><span data-stu-id="dfb66-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="dfb66-115">Exemplo 3: Obter uma configuração de cluster kubernetes por objeto</span><span class="sxs-lookup"><span data-stu-id="dfb66-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="dfb66-116">Este comando obtém uma configuração de cluster kubernetes por objeto.</span><span class="sxs-lookup"><span data-stu-id="dfb66-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="dfb66-117">Exemplo 4: obter uma configuração do cluster kubernetes por pipeline</span><span class="sxs-lookup"><span data-stu-id="dfb66-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="dfb66-118">Este comando obtém uma configuração de cluster kubernetes por pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfb66-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="dfb66-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dfb66-119">PARAMETERS</span></span>

### <span data-ttu-id="dfb66-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfb66-120">-ClusterName</span></span>
<span data-ttu-id="dfb66-121">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dfb66-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="dfb66-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="dfb66-122">-ClusterRp</span></span>
<span data-ttu-id="dfb66-123">O RP do cluster Kubernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Kubernetes (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dfb66-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dfb66-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="dfb66-124">-ClusterType</span></span>
<span data-ttu-id="dfb66-125">O nome do recurso de cluster Kubernetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dfb66-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dfb66-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb66-126">-DefaultProfile</span></span>
<span data-ttu-id="dfb66-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb66-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb66-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfb66-128">-InputObject</span></span>
<span data-ttu-id="dfb66-129">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dfb66-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dfb66-130">-Name</span><span class="sxs-lookup"><span data-stu-id="dfb66-130">-Name</span></span>
<span data-ttu-id="dfb66-131">Nome da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="dfb66-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="dfb66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb66-132">-ResourceGroupName</span></span>
<span data-ttu-id="dfb66-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfb66-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfb66-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfb66-134">-SubscriptionId</span></span>
<span data-ttu-id="dfb66-135">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb66-135">The Azure subscription ID.</span></span>
<span data-ttu-id="dfb66-136">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="dfb66-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="dfb66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb66-137">CommonParameters</span></span>
<span data-ttu-id="dfb66-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb66-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfb66-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb66-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfb66-140">INPUTS</span></span>

### <span data-ttu-id="dfb66-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="dfb66-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="dfb66-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dfb66-142">OUTPUTS</span></span>

### <span data-ttu-id="dfb66-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfb66-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="dfb66-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="dfb66-144">NOTES</span></span>

<span data-ttu-id="dfb66-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dfb66-145">ALIASES</span></span>

<span data-ttu-id="dfb66-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="dfb66-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfb66-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dfb66-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfb66-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfb66-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfb66-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="dfb66-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfb66-150">`[ClusterName <String>]`: O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dfb66-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="dfb66-151">`[ClusterResourceName <String>]`: O nome do recurso de cluster Kubernetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dfb66-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dfb66-152">`[ClusterRp <String>]`: O RP do cluster Kubernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Kubernetes (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dfb66-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dfb66-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="dfb66-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfb66-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfb66-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dfb66-155">`[SourceControlConfigurationName <String>]`: Nome da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="dfb66-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="dfb66-156">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb66-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="dfb66-157">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="dfb66-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="dfb66-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfb66-158">RELATED LINKS</span></span>

