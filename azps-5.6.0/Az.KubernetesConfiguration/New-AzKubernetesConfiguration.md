---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888489"
---
# <span data-ttu-id="56913-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="56913-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="56913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56913-102">SYNOPSIS</span></span>
<span data-ttu-id="56913-103">Crie uma nova Configuração de Controle de Origem do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="56913-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="56913-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56913-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56913-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56913-105">DESCRIPTION</span></span>
<span data-ttu-id="56913-106">Crie uma nova Configuração de Controle de Origem do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="56913-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="56913-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56913-107">EXAMPLES</span></span>

### <span data-ttu-id="56913-108">Exemplo 1: Criar uma configuração para cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="56913-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="56913-109">Este comando cria uma configuração para cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="56913-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="56913-110">Exemplo 1: Criar uma configuração para cluster kubernetes com especificar o operatornamespace do paramter</span><span class="sxs-lookup"><span data-stu-id="56913-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="56913-111">Este comando cria uma configuração no novo namespace do operador para cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="56913-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="56913-112">Observação: Não é possível criar uma configuração em um namespace de operador existente.</span><span class="sxs-lookup"><span data-stu-id="56913-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="56913-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56913-113">PARAMETERS</span></span>

### <span data-ttu-id="56913-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="56913-114">-ClusterName</span></span>
<span data-ttu-id="56913-115">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="56913-115">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="56913-116">-ClusterScoped</span></span>
<span data-ttu-id="56913-117">Se aprovado definir o escopo da Configuração como Cluster (o padrão é nameSpace).</span><span class="sxs-lookup"><span data-stu-id="56913-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="56913-118">-ClusterType</span></span>
<span data-ttu-id="56913-119">O nome do recurso de cluster Kubernetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="56913-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56913-120">-DefaultProfile</span></span>
<span data-ttu-id="56913-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56913-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56913-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="56913-122">-EnableHelmOperator</span></span>
<span data-ttu-id="56913-123">Opção para habilitar o Operador de Helm para essa configuração do git.</span><span class="sxs-lookup"><span data-stu-id="56913-123">Option to enable Helm Operator for this git configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="56913-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="56913-125">Os valores substituem o gráfico do operador Helm.</span><span class="sxs-lookup"><span data-stu-id="56913-125">Values override for the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="56913-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="56913-127">Versão do gráfico do operador Helm.</span><span class="sxs-lookup"><span data-stu-id="56913-127">Version of the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-128">-Name</span><span class="sxs-lookup"><span data-stu-id="56913-128">-Name</span></span>
<span data-ttu-id="56913-129">Nome da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="56913-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="56913-130">-OperatorInstanceName</span></span>
<span data-ttu-id="56913-131">Nome da instância do operador - identificando a configuração específica.</span><span class="sxs-lookup"><span data-stu-id="56913-131">Instance name of the operator - identifying the specific configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="56913-132">-OperatorNamespace</span></span>
<span data-ttu-id="56913-133">O namespace para o qual esse operador está instalado.</span><span class="sxs-lookup"><span data-stu-id="56913-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="56913-134">Máximo de 253 caracteres alfanuméricos de caso inferior, hífen e somente ponto.</span><span class="sxs-lookup"><span data-stu-id="56913-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="56913-135">-OperatorParameters</span></span>
<span data-ttu-id="56913-136">Quaisquer Parâmetros para a instância do Operador no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="56913-136">Any Parameters for the Operator instance in string format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="56913-137">-RepositoryUrl</span></span>
<span data-ttu-id="56913-138">Url do Repositório SourceControl.</span><span class="sxs-lookup"><span data-stu-id="56913-138">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56913-139">-ResourceGroupName</span></span>
<span data-ttu-id="56913-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56913-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56913-141">-SubscriptionId</span></span>
<span data-ttu-id="56913-142">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="56913-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56913-143">-Confirm</span></span>
<span data-ttu-id="56913-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56913-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56913-145">-WhatIf</span></span>
<span data-ttu-id="56913-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56913-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56913-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56913-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56913-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56913-148">CommonParameters</span></span>
<span data-ttu-id="56913-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56913-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56913-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56913-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56913-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56913-151">INPUTS</span></span>

## <span data-ttu-id="56913-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56913-152">OUTPUTS</span></span>

### <span data-ttu-id="56913-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="56913-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="56913-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="56913-154">NOTES</span></span>

<span data-ttu-id="56913-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56913-155">ALIASES</span></span>

## <span data-ttu-id="56913-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56913-156">RELATED LINKS</span></span>

