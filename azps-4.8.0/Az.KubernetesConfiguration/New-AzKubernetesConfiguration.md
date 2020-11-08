---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111858"
---
# <span data-ttu-id="e96ea-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="e96ea-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="e96ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e96ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e96ea-103">Crie uma nova configuração de controle de origem kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e96ea-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="e96ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e96ea-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e96ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e96ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e96ea-106">Crie uma nova configuração de controle de origem kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e96ea-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="e96ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e96ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e96ea-108">Exemplo 1: criar um configuation para o cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="e96ea-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="e96ea-109">Esse comando cria um configuation para kubernetes cluster.</span><span class="sxs-lookup"><span data-stu-id="e96ea-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="e96ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="e96ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e96ea-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e96ea-111">-ClusterName</span></span>
<span data-ttu-id="e96ea-112">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e96ea-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="e96ea-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="e96ea-113">-ClusterScoped</span></span>
<span data-ttu-id="e96ea-114">Se passou, defina o escopo da configuração para cluster (o padrão é nameSpace).</span><span class="sxs-lookup"><span data-stu-id="e96ea-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="e96ea-115">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="e96ea-115">-ClusterType</span></span>
<span data-ttu-id="e96ea-116">O nome do recurso de cluster kubernetes-managedClusters (para clusters AKS) ou connectedClusters (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="e96ea-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="e96ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96ea-117">-DefaultProfile</span></span>
<span data-ttu-id="e96ea-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e96ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e96ea-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="e96ea-119">-EnableHelmOperator</span></span>
<span data-ttu-id="e96ea-120">Opção para habilitar o Helm Operator para esta configuração de git.</span><span class="sxs-lookup"><span data-stu-id="e96ea-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="e96ea-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="e96ea-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="e96ea-122">Substituir valores para o gráfico de Helm do operador.</span><span class="sxs-lookup"><span data-stu-id="e96ea-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="e96ea-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="e96ea-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="e96ea-124">Versão do gráfico Helm do operador.</span><span class="sxs-lookup"><span data-stu-id="e96ea-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="e96ea-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e96ea-125">-Name</span></span>
<span data-ttu-id="e96ea-126">Nome da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e96ea-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="e96ea-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="e96ea-127">-OperatorInstanceName</span></span>
<span data-ttu-id="e96ea-128">Nome da instância do operador-identificando a configuração específica.</span><span class="sxs-lookup"><span data-stu-id="e96ea-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="e96ea-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="e96ea-129">-OperatorNamespace</span></span>
<span data-ttu-id="e96ea-130">O namespace para o qual esse operador está instalado.</span><span class="sxs-lookup"><span data-stu-id="e96ea-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="e96ea-131">Máximo de 253 caracteres alfanuméricos minúsculos, somente hífen e período.</span><span class="sxs-lookup"><span data-stu-id="e96ea-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="e96ea-132">-Operatorparameters</span><span class="sxs-lookup"><span data-stu-id="e96ea-132">-OperatorParameters</span></span>
<span data-ttu-id="e96ea-133">Qualquer parâmetro para a instância Operator em formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e96ea-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="e96ea-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="e96ea-134">-RepositoryUrl</span></span>
<span data-ttu-id="e96ea-135">URL do repositório do SourceControl.</span><span class="sxs-lookup"><span data-stu-id="e96ea-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="e96ea-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96ea-136">-ResourceGroupName</span></span>
<span data-ttu-id="e96ea-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e96ea-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="e96ea-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e96ea-138">-SubscriptionId</span></span>
<span data-ttu-id="e96ea-139">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e96ea-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e96ea-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e96ea-140">-Confirm</span></span>
<span data-ttu-id="e96ea-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e96ea-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e96ea-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96ea-142">-WhatIf</span></span>
<span data-ttu-id="e96ea-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e96ea-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96ea-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e96ea-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e96ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96ea-145">CommonParameters</span></span>
<span data-ttu-id="e96ea-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96ea-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e96ea-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96ea-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e96ea-148">INPUTS</span></span>

## <span data-ttu-id="e96ea-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e96ea-149">OUTPUTS</span></span>

### <span data-ttu-id="e96ea-150">Microsoft. Azure. PowerShell. cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e96ea-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="e96ea-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e96ea-151">NOTES</span></span>

<span data-ttu-id="e96ea-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e96ea-152">ALIASES</span></span>

## <span data-ttu-id="e96ea-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e96ea-153">RELATED LINKS</span></span>

