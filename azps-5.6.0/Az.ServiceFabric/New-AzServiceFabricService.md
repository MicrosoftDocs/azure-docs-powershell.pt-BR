---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: c0572e994650347d24a6b58ca12b6d2938a182bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892351"
---
# <span data-ttu-id="837b3-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="837b3-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="837b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="837b3-102">SYNOPSIS</span></span>
<span data-ttu-id="837b3-103">Crie um novo serviço de malha de serviço no aplicativo e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="837b3-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="837b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="837b3-104">SYNTAX</span></span>

### <span data-ttu-id="837b3-105">Stateless-Singleton (Padrão)</span><span class="sxs-lookup"><span data-stu-id="837b3-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="837b3-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="837b3-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="837b3-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="837b3-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837b3-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="837b3-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837b3-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="837b3-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837b3-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="837b3-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837b3-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="837b3-111">DESCRIPTION</span></span>
<span data-ttu-id="837b3-112">Esse cmdlet permite a criação de serviços sem estado ou estado no aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="837b3-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="837b3-113">O serviço deve sair no manifesto do aplicativo e o tipo deve ser o mesmo do manifesto.</span><span class="sxs-lookup"><span data-stu-id="837b3-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="837b3-114">O nome do aplicativo deve ser um prefixo do nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="837b3-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="837b3-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="837b3-115">EXAMPLES</span></span>

### <span data-ttu-id="837b3-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="837b3-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="837b3-117">Este exemplo criará um novo serviço sem estado "testApp~testService1" com a contagem de instâncias -1 (em todos os nós).</span><span class="sxs-lookup"><span data-stu-id="837b3-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="837b3-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="837b3-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="837b3-119">Este exemplo criará um novo serviço de estado "testApp~testService2" com um destino de 5 nós.</span><span class="sxs-lookup"><span data-stu-id="837b3-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="837b3-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="837b3-120">PARAMETERS</span></span>

### <span data-ttu-id="837b3-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="837b3-121">-ApplicationName</span></span>
<span data-ttu-id="837b3-122">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="837b3-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="837b3-123">-ClusterName</span></span>
<span data-ttu-id="837b3-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="837b3-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="837b3-125">-DefaultMoveCost</span></span>
<span data-ttu-id="837b3-126">Especifique o custo padrão para uma movimentação.</span><span class="sxs-lookup"><span data-stu-id="837b3-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="837b3-127">Custos mais altos fazem com que seja menos provável que o Gerenciador de Recursos de Cluster mova a réplica ao tentar equilibrar o cluster</span><span class="sxs-lookup"><span data-stu-id="837b3-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837b3-128">-DefaultProfile</span></span>
<span data-ttu-id="837b3-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="837b3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="837b3-130">-InstanceCount</span></span>
<span data-ttu-id="837b3-131">Especificar a contagem de instâncias para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="837b3-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="837b3-133">Especificar o tamanho mínimo do conjunto de réplicas para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="837b3-134">-Name</span></span>
<span data-ttu-id="837b3-135">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="837b3-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="837b3-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="837b3-137">Indica que o serviço usa o esquema de partição nomeado.</span><span class="sxs-lookup"><span data-stu-id="837b3-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="837b3-138">Os serviços que usam esse modelo geralmente têm dados que podem ser lançados dentro de um conjunto limitado.</span><span class="sxs-lookup"><span data-stu-id="837b3-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="837b3-139">Alguns exemplos comuns de campos de dados usados como chaves de partição nomeadas seriam regiões, códigos postais, grupos de clientes ou outros limites comerciais.</span><span class="sxs-lookup"><span data-stu-id="837b3-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="837b3-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="837b3-141">Indica que o serviço usa o esquema de partição singleton.</span><span class="sxs-lookup"><span data-stu-id="837b3-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="837b3-142">As partições singleton geralmente são usadas quando o serviço não exige nenhum roteamento adicional.</span><span class="sxs-lookup"><span data-stu-id="837b3-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="837b3-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="837b3-144">Indica que o serviço usa o esquema de partição UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="837b3-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="837b3-145">Isso significa que cada partição possui um intervalo de teclas int64.</span><span class="sxs-lookup"><span data-stu-id="837b3-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="837b3-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="837b3-147">Especifique a duração de espera de perda de quórum para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="837b3-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="837b3-149">Especifique a duração de espera de reinicialização da réplica para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837b3-150">-ResourceGroupName</span></span>
<span data-ttu-id="837b3-151">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="837b3-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="837b3-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="837b3-153">Especifique a duração da réplica de stand by para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="837b3-154">-Stateful</span></span>
<span data-ttu-id="837b3-155">Usar para serviço de estado</span><span class="sxs-lookup"><span data-stu-id="837b3-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="837b3-156">-Stateless</span></span>
<span data-ttu-id="837b3-157">Usar para serviço sem estado</span><span class="sxs-lookup"><span data-stu-id="837b3-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="837b3-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="837b3-159">Especificar o tamanho do conjunto de réplicas de destino para o serviço</span><span class="sxs-lookup"><span data-stu-id="837b3-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-160">-Type</span><span class="sxs-lookup"><span data-stu-id="837b3-160">-Type</span></span>
<span data-ttu-id="837b3-161">Especifique o nome do tipo de serviço do aplicativo, deve existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="837b3-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="837b3-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="837b3-162">-Confirm</span></span>
<span data-ttu-id="837b3-163">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="837b3-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837b3-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837b3-164">-WhatIf</span></span>
<span data-ttu-id="837b3-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="837b3-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837b3-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="837b3-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837b3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837b3-167">CommonParameters</span></span>
<span data-ttu-id="837b3-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837b3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837b3-169">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="837b3-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837b3-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="837b3-170">INPUTS</span></span>

### <span data-ttu-id="837b3-171">System.String</span><span class="sxs-lookup"><span data-stu-id="837b3-171">System.String</span></span>

## <span data-ttu-id="837b3-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="837b3-172">OUTPUTS</span></span>

### <span data-ttu-id="837b3-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="837b3-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="837b3-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="837b3-174">NOTES</span></span>

## <span data-ttu-id="837b3-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="837b3-175">RELATED LINKS</span></span>
