---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: daa058d1f3cc13e073d8533403341dad3db7c319
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113054"
---
# <span data-ttu-id="27a70-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="27a70-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="27a70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27a70-102">SYNOPSIS</span></span>
<span data-ttu-id="27a70-103">Obtém detalhes da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="27a70-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="27a70-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27a70-104">SYNTAX</span></span>

### <span data-ttu-id="27a70-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="27a70-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27a70-106">Obter</span><span class="sxs-lookup"><span data-stu-id="27a70-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27a70-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27a70-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="27a70-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="27a70-108">DESCRIPTION</span></span>
<span data-ttu-id="27a70-109">Obtém detalhes da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="27a70-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="27a70-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27a70-110">EXAMPLES</span></span>

### <span data-ttu-id="27a70-111">Exemplo 1: Obter todas as configurações de cluster de rede</span><span class="sxs-lookup"><span data-stu-id="27a70-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="27a70-112">Esse comando obtém todas as configurações de cluster de rede.</span><span class="sxs-lookup"><span data-stu-id="27a70-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="27a70-113">Exemplo 2: Obter uma configuração de cluster de rede por nome</span><span class="sxs-lookup"><span data-stu-id="27a70-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="27a70-114">Esse comando obtém uma configuração de cluster de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="27a70-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="27a70-115">Exemplo 3: Obter uma configuração de cluster de rede por objeto</span><span class="sxs-lookup"><span data-stu-id="27a70-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="27a70-116">Esse comando obtém uma configuração de cluster de rede por objeto.</span><span class="sxs-lookup"><span data-stu-id="27a70-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="27a70-117">Exemplo 4: Obter uma configuração de cluster de rede por pipeline</span><span class="sxs-lookup"><span data-stu-id="27a70-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="27a70-118">Esse comando obtém uma configuração de cluster de rede por pipeline.</span><span class="sxs-lookup"><span data-stu-id="27a70-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="27a70-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27a70-119">PARAMETERS</span></span>

### <span data-ttu-id="27a70-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="27a70-120">-ClusterName</span></span>
<span data-ttu-id="27a70-121">O nome do cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="27a70-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="27a70-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="27a70-122">-ClusterRp</span></span>
<span data-ttu-id="27a70-123">O cluster DEXernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Rouernetes (para clusteres OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="27a70-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="27a70-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="27a70-124">-ClusterType</span></span>
<span data-ttu-id="27a70-125">O nome do recurso cluster Desternetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="27a70-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="27a70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a70-126">-DefaultProfile</span></span>
<span data-ttu-id="27a70-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27a70-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a70-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27a70-128">-InputObject</span></span>
<span data-ttu-id="27a70-129">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="27a70-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27a70-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="27a70-130">-Name</span></span>
<span data-ttu-id="27a70-131">Nome da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="27a70-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="27a70-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a70-132">-ResourceGroupName</span></span>
<span data-ttu-id="27a70-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27a70-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="27a70-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27a70-134">-SubscriptionId</span></span>
<span data-ttu-id="27a70-135">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="27a70-135">The Azure subscription ID.</span></span>
<span data-ttu-id="27a70-136">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="27a70-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="27a70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a70-137">CommonParameters</span></span>
<span data-ttu-id="27a70-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a70-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27a70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a70-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="27a70-140">INPUTS</span></span>

### <span data-ttu-id="27a70-141">Microsoft.Azure.PowerShell.Cmdlets.VoernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="27a70-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="27a70-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="27a70-142">OUTPUTS</span></span>

### <span data-ttu-id="27a70-143">Microsoft.Azure.PowerShell.Cmdlets.RouernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27a70-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="27a70-144">Notas</span><span class="sxs-lookup"><span data-stu-id="27a70-144">NOTES</span></span>

<span data-ttu-id="27a70-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="27a70-145">ALIASES</span></span>

<span data-ttu-id="27a70-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="27a70-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27a70-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="27a70-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27a70-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27a70-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27a70-149">INPUTOBJECT: <IKubernetesConfigurationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="27a70-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27a70-150">`[ClusterName <String>]`: o nome do cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="27a70-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="27a70-151">`[ClusterResourceName <String>]`: O nome do recurso cluster Desternetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="27a70-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="27a70-152">`[ClusterRp <String>]`: O cluster DEXernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Rouernetes (para clusteres OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="27a70-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="27a70-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="27a70-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27a70-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27a70-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="27a70-155">`[SourceControlConfigurationName <String>]`: Nome da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="27a70-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="27a70-156">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="27a70-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="27a70-157">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="27a70-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="27a70-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27a70-158">RELATED LINKS</span></span>

