---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124976"
---
# <span data-ttu-id="91c81-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="91c81-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="91c81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91c81-102">SYNOPSIS</span></span>
<span data-ttu-id="91c81-103">Isso excluirá o arquivo YAML usado para configurar a configuração do controle do código-fonte, por isso interrompendo a sincronização futura do repositório de origem.</span><span class="sxs-lookup"><span data-stu-id="91c81-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="91c81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91c81-104">SYNTAX</span></span>

### <span data-ttu-id="91c81-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="91c81-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91c81-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91c81-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91c81-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91c81-107">DESCRIPTION</span></span>
<span data-ttu-id="91c81-108">Isso excluirá o arquivo YAML usado para configurar a configuração do controle do código-fonte, por isso interrompendo a sincronização futura do repositório de origem.</span><span class="sxs-lookup"><span data-stu-id="91c81-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="91c81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91c81-109">EXAMPLES</span></span>

### <span data-ttu-id="91c81-110">Exemplo 1: remover um configuation do cluster kubernetes por nome</span><span class="sxs-lookup"><span data-stu-id="91c81-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="91c81-111">Esse comando Remove um configuation do cluster kubernetes por nome.</span><span class="sxs-lookup"><span data-stu-id="91c81-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="91c81-112">Exemplo 2: remover um configuation do cluster do kubernetes por objeto</span><span class="sxs-lookup"><span data-stu-id="91c81-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="91c81-113">Esse comando Remove um configuation do cluster kubernetes por objeto.</span><span class="sxs-lookup"><span data-stu-id="91c81-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="91c81-114">OS</span><span class="sxs-lookup"><span data-stu-id="91c81-114">PARAMETERS</span></span>

### <span data-ttu-id="91c81-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c81-115">-AsJob</span></span>
<span data-ttu-id="91c81-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="91c81-116">Run the command as a job</span></span>

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

### <span data-ttu-id="91c81-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91c81-117">-ClusterName</span></span>
<span data-ttu-id="91c81-118">O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="91c81-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="91c81-119">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="91c81-119">-ClusterType</span></span>
<span data-ttu-id="91c81-120">O nome do recurso de cluster kubernetes-managedClusters (para clusters AKS) ou connectedClusters (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="91c81-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="91c81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c81-121">-DefaultProfile</span></span>
<span data-ttu-id="91c81-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91c81-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c81-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c81-123">-InputObject</span></span>
<span data-ttu-id="91c81-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="91c81-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91c81-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="91c81-125">-Name</span></span>
<span data-ttu-id="91c81-126">Nome da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="91c81-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="91c81-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="91c81-127">-NoWait</span></span>
<span data-ttu-id="91c81-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="91c81-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="91c81-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91c81-129">-PassThru</span></span>
<span data-ttu-id="91c81-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="91c81-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="91c81-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c81-131">-ResourceGroupName</span></span>
<span data-ttu-id="91c81-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="91c81-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="91c81-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91c81-133">-SubscriptionId</span></span>
<span data-ttu-id="91c81-134">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="91c81-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="91c81-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91c81-135">-Confirm</span></span>
<span data-ttu-id="91c81-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c81-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c81-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c81-137">-WhatIf</span></span>
<span data-ttu-id="91c81-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91c81-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c81-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91c81-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c81-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c81-140">CommonParameters</span></span>
<span data-ttu-id="91c81-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c81-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c81-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c81-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c81-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91c81-143">INPUTS</span></span>

### <span data-ttu-id="91c81-144">Microsoft. Azure. PowerShell. cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="91c81-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="91c81-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91c81-145">OUTPUTS</span></span>

### <span data-ttu-id="91c81-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91c81-146">System.Boolean</span></span>

## <span data-ttu-id="91c81-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91c81-147">NOTES</span></span>

<span data-ttu-id="91c81-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="91c81-148">ALIASES</span></span>

<span data-ttu-id="91c81-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="91c81-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91c81-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="91c81-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91c81-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91c81-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91c81-152">INPUTobject <IKubernetesConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="91c81-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91c81-153">`[ClusterName <String>]`: O nome do cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="91c81-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="91c81-154">`[ClusterResourceName <String>]`: O nome do recurso de cluster kubernetes-managedClusters (para clusters AKS) ou connectedClusters (para clusters de K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="91c81-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="91c81-155">`[ClusterRp <String>]`: O kubernetes do cluster do RP-Microsoft. ContainerService (para clusters AKS) ou Microsoft. kubernetes (para clusters do K8S onlocal).</span><span class="sxs-lookup"><span data-stu-id="91c81-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="91c81-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="91c81-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91c81-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="91c81-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="91c81-158">`[SourceControlConfigurationName <String>]`: Nome da configuração de controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="91c81-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="91c81-159">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="91c81-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="91c81-160">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="91c81-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="91c81-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91c81-161">RELATED LINKS</span></span>

