---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: a63a28d301b5b565a01bf1e3c22acba413ee779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886961"
---
# <span data-ttu-id="ea6cc-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea6cc-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="ea6cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6cc-103">Isso excluirá o arquivo YAML usado para configurar a configuração do controle Source, interrompendo assim a sincronização futura do repo de origem.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="ea6cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea6cc-104">SYNTAX</span></span>

### <span data-ttu-id="ea6cc-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ea6cc-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea6cc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea6cc-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea6cc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea6cc-107">DESCRIPTION</span></span>
<span data-ttu-id="ea6cc-108">Isso excluirá o arquivo YAML usado para configurar a configuração do controle Source, interrompendo assim a sincronização futura do repo de origem.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="ea6cc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-109">EXAMPLES</span></span>

### <span data-ttu-id="ea6cc-110">Exemplo 1: Remover uma configuração de cluster kubernetes pelo nome</span><span class="sxs-lookup"><span data-stu-id="ea6cc-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="ea6cc-111">Este comando remove uma configuração de cluster kubernetes pelo nome.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="ea6cc-112">Exemplo 2: Remover uma configuração de cluster kubernetes por objeto</span><span class="sxs-lookup"><span data-stu-id="ea6cc-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="ea6cc-113">Este comando remove uma configuração de cluster kubernetes por objeto.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="ea6cc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-114">PARAMETERS</span></span>

### <span data-ttu-id="ea6cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea6cc-115">-AsJob</span></span>
<span data-ttu-id="ea6cc-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ea6cc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ea6cc-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ea6cc-117">-ClusterName</span></span>
<span data-ttu-id="ea6cc-118">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ea6cc-119">-ClusterType</span></span>
<span data-ttu-id="ea6cc-120">O nome do recurso de cluster Kubernetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="ea6cc-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6cc-121">-DefaultProfile</span></span>
<span data-ttu-id="ea6cc-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea6cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea6cc-123">-InputObject</span></span>
<span data-ttu-id="ea6cc-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ea6cc-125">-Name</span></span>
<span data-ttu-id="ea6cc-126">Nome da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea6cc-127">-NoWait</span></span>
<span data-ttu-id="ea6cc-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ea6cc-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea6cc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea6cc-129">-PassThru</span></span>
<span data-ttu-id="ea6cc-130">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ea6cc-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ea6cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="ea6cc-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea6cc-133">-SubscriptionId</span></span>
<span data-ttu-id="ea6cc-134">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6cc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea6cc-135">-Confirm</span></span>
<span data-ttu-id="ea6cc-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea6cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea6cc-137">-WhatIf</span></span>
<span data-ttu-id="ea6cc-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea6cc-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea6cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6cc-140">CommonParameters</span></span>
<span data-ttu-id="ea6cc-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6cc-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea6cc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6cc-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-143">INPUTS</span></span>

### <span data-ttu-id="ea6cc-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="ea6cc-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="ea6cc-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-145">OUTPUTS</span></span>

### <span data-ttu-id="ea6cc-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea6cc-146">System.Boolean</span></span>

## <span data-ttu-id="ea6cc-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea6cc-147">NOTES</span></span>

<span data-ttu-id="ea6cc-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ea6cc-148">ALIASES</span></span>

<span data-ttu-id="ea6cc-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ea6cc-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea6cc-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea6cc-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea6cc-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ea6cc-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea6cc-153">`[ClusterName <String>]`: O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="ea6cc-154">`[ClusterResourceName <String>]`: O nome do recurso de cluster Kubernetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="ea6cc-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="ea6cc-155">`[ClusterRp <String>]`: O RP do cluster Kubernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Kubernetes (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="ea6cc-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="ea6cc-156">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ea6cc-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea6cc-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ea6cc-158">`[SourceControlConfigurationName <String>]`: Nome da Configuração de Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="ea6cc-159">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea6cc-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ea6cc-160">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="ea6cc-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ea6cc-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea6cc-161">RELATED LINKS</span></span>

