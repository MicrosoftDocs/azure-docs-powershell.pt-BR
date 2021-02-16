---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 16b1e6f56cd5d324815dcf9453bc7f94e0de2480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113048"
---
# <span data-ttu-id="fba98-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="fba98-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="fba98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fba98-102">SYNOPSIS</span></span>
<span data-ttu-id="fba98-103">Isso excluirá o arquivo YAML usado para configurar a configuração do controle de origem, interrompendo assim a sincronização futura do repo de origem.</span><span class="sxs-lookup"><span data-stu-id="fba98-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="fba98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fba98-104">SYNTAX</span></span>

### <span data-ttu-id="fba98-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fba98-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fba98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fba98-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fba98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fba98-107">DESCRIPTION</span></span>
<span data-ttu-id="fba98-108">Isso excluirá o arquivo YAML usado para configurar a configuração do controle de origem, interrompendo assim a sincronização futura do repo de origem.</span><span class="sxs-lookup"><span data-stu-id="fba98-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="fba98-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fba98-109">EXAMPLES</span></span>

### <span data-ttu-id="fba98-110">Exemplo 1: Remover uma configuração de cluster de dioranetes por nome</span><span class="sxs-lookup"><span data-stu-id="fba98-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="fba98-111">Esse comando remove uma configuração de cluster de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="fba98-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="fba98-112">Exemplo 2: Remover uma configuração de cluster de rede por objeto</span><span class="sxs-lookup"><span data-stu-id="fba98-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="fba98-113">Esse comando remove uma configuração de cluster de rede por objeto.</span><span class="sxs-lookup"><span data-stu-id="fba98-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="fba98-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fba98-114">PARAMETERS</span></span>

### <span data-ttu-id="fba98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fba98-115">-AsJob</span></span>
<span data-ttu-id="fba98-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fba98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fba98-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fba98-117">-ClusterName</span></span>
<span data-ttu-id="fba98-118">O nome do cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="fba98-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="fba98-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="fba98-119">-ClusterType</span></span>
<span data-ttu-id="fba98-120">O nome do recurso cluster Desternetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="fba98-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="fba98-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba98-121">-DefaultProfile</span></span>
<span data-ttu-id="fba98-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fba98-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba98-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fba98-123">-InputObject</span></span>
<span data-ttu-id="fba98-124">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fba98-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fba98-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fba98-125">-Name</span></span>
<span data-ttu-id="fba98-126">Nome da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="fba98-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="fba98-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fba98-127">-NoWait</span></span>
<span data-ttu-id="fba98-128">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="fba98-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fba98-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fba98-129">-PassThru</span></span>
<span data-ttu-id="fba98-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fba98-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fba98-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba98-131">-ResourceGroupName</span></span>
<span data-ttu-id="fba98-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fba98-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="fba98-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fba98-133">-SubscriptionId</span></span>
<span data-ttu-id="fba98-134">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="fba98-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="fba98-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fba98-135">-Confirm</span></span>
<span data-ttu-id="fba98-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba98-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba98-137">-WhatIf</span></span>
<span data-ttu-id="fba98-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fba98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fba98-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fba98-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba98-140">CommonParameters</span></span>
<span data-ttu-id="fba98-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba98-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fba98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba98-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="fba98-143">INPUTS</span></span>

### <span data-ttu-id="fba98-144">Microsoft.Azure.PowerShell.Cmdlets.VoernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="fba98-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="fba98-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="fba98-145">OUTPUTS</span></span>

### <span data-ttu-id="fba98-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fba98-146">System.Boolean</span></span>

## <span data-ttu-id="fba98-147">Notas</span><span class="sxs-lookup"><span data-stu-id="fba98-147">NOTES</span></span>

<span data-ttu-id="fba98-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="fba98-148">ALIASES</span></span>

<span data-ttu-id="fba98-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="fba98-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fba98-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fba98-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fba98-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fba98-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fba98-152">INPUTOBJECT: <IKubernetesConfigurationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="fba98-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fba98-153">`[ClusterName <String>]`: o nome do cluster de lança-redes.</span><span class="sxs-lookup"><span data-stu-id="fba98-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="fba98-154">`[ClusterResourceName <String>]`: O nome do recurso cluster Desternetes - managedClusters (para clusters AKS) ou connectedClusters (para clusters OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="fba98-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="fba98-155">`[ClusterRp <String>]`: O cluster DEXernetes - Microsoft.ContainerService (para clusters AKS) ou Microsoft.Rouernetes (para clusteres OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="fba98-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="fba98-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="fba98-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fba98-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fba98-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fba98-158">`[SourceControlConfigurationName <String>]`: Nome da Configuração do Controle de Origem.</span><span class="sxs-lookup"><span data-stu-id="fba98-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="fba98-159">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="fba98-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="fba98-160">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="fba98-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="fba98-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fba98-161">RELATED LINKS</span></span>

