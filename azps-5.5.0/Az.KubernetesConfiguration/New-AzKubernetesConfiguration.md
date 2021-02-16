---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113052"
---
# <span data-ttu-id="f49e8-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="f49e8-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="f49e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f49e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f49e8-103">Crie uma nova Configuração de Controle de Origem das Redes.</span><span class="sxs-lookup"><span data-stu-id="f49e8-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="f49e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f49e8-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f49e8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f49e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f49e8-106">Crie uma nova Configuração de Controle de Origem das Redes.</span><span class="sxs-lookup"><span data-stu-id="f49e8-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="f49e8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f49e8-107">EXAMPLES</span></span>

### <span data-ttu-id="f49e8-108">Exemplo 1: Criar uma configuração para cluster de soluções de rede</span><span class="sxs-lookup"><span data-stu-id="f49e8-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="f49e8-109">Esse comando cria uma configuração para cluster de rede de rede.</span><span class="sxs-lookup"><span data-stu-id="f49e8-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="f49e8-110">Exemplo 1: Criar uma configuração para cluster de soluções com especificar OperadorNamespace de paramter</span><span class="sxs-lookup"><span data-stu-id="f49e8-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="f49e8-111">Esse comando cria uma configuração no novo espaço de nome de operador para cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="f49e8-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="f49e8-112">Observação: Não é possível criar uma configuração em um namespace de operador existente.</span><span class="sxs-lookup"><span data-stu-id="f49e8-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="f49e8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f49e8-113">PARAMETERS</span></span>

### <span data-ttu-id="f49e8-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f49e8-114">-ClusterName</span></span>
<span data-ttu-id="f49e8-115">O nome do cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="f49e8-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="f49e8-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="f49e8-116">-ClusterScoped</span></span>
<span data-ttu-id="f49e8-117">Se aprovado, de acordo com o escopo da Configuração como Cluster (o padrão é nameSpace).</span><span class="sxs-lookup"><span data-stu-id="f49e8-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="f49e8-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f49e8-118">-ClusterType</span></span>
<span data-ttu-id="f49e8-119">O nome do recurso cluster Desternetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="f49e8-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="f49e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49e8-120">-DefaultProfile</span></span>
<span data-ttu-id="f49e8-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f49e8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49e8-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="f49e8-122">-EnableHelmOperator</span></span>
<span data-ttu-id="f49e8-123">Opção para habilitar o Operador de Operador Debilitar para esta configuração de git.</span><span class="sxs-lookup"><span data-stu-id="f49e8-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="f49e8-124">-OperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="f49e8-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="f49e8-125">Os valores substituem o operador Gráfico de Gráfico de Gráfico de Gráficos.</span><span class="sxs-lookup"><span data-stu-id="f49e8-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="f49e8-126">-OperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="f49e8-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="f49e8-127">Versão do gráfico de gráfico de gráfico de gráfico de gráficos do operador.</span><span class="sxs-lookup"><span data-stu-id="f49e8-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="f49e8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f49e8-128">-Name</span></span>
<span data-ttu-id="f49e8-129">Nome da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="f49e8-129">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="f49e8-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="f49e8-130">-OperatorInstanceName</span></span>
<span data-ttu-id="f49e8-131">Nome da instância do operador - identificando a configuração específica.</span><span class="sxs-lookup"><span data-stu-id="f49e8-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="f49e8-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="f49e8-132">-OperatorNamespace</span></span>
<span data-ttu-id="f49e8-133">O namespace para o qual este operador está instalado.</span><span class="sxs-lookup"><span data-stu-id="f49e8-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="f49e8-134">Máximo de 253 caracteres alfanuméricos de caso inferior, hífen e somente ponto.</span><span class="sxs-lookup"><span data-stu-id="f49e8-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="f49e8-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="f49e8-135">-OperatorParameters</span></span>
<span data-ttu-id="f49e8-136">Todos os Parâmetros da instância operador no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f49e8-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="f49e8-137">-RepositórioUrl</span><span class="sxs-lookup"><span data-stu-id="f49e8-137">-RepositoryUrl</span></span>
<span data-ttu-id="f49e8-138">URL do Repositório SourceControl.</span><span class="sxs-lookup"><span data-stu-id="f49e8-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="f49e8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49e8-139">-ResourceGroupName</span></span>
<span data-ttu-id="f49e8-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f49e8-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="f49e8-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f49e8-141">-SubscriptionId</span></span>
<span data-ttu-id="f49e8-142">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f49e8-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="f49e8-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f49e8-143">-Confirm</span></span>
<span data-ttu-id="f49e8-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49e8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49e8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49e8-145">-WhatIf</span></span>
<span data-ttu-id="f49e8-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f49e8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49e8-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f49e8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49e8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49e8-148">CommonParameters</span></span>
<span data-ttu-id="f49e8-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49e8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49e8-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f49e8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49e8-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="f49e8-151">INPUTS</span></span>

## <span data-ttu-id="f49e8-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="f49e8-152">OUTPUTS</span></span>

### <span data-ttu-id="f49e8-153">Microsoft.Azure.PowerShell.Cmdlets.RouernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f49e8-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="f49e8-154">Notas</span><span class="sxs-lookup"><span data-stu-id="f49e8-154">NOTES</span></span>

<span data-ttu-id="f49e8-155">Aliases</span><span class="sxs-lookup"><span data-stu-id="f49e8-155">ALIASES</span></span>

## <span data-ttu-id="f49e8-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f49e8-156">RELATED LINKS</span></span>

