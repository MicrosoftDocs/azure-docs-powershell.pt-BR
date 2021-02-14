---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117106"
---
# <span data-ttu-id="4f1a2-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4f1a2-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="4f1a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1a2-103">Crie um novo serviço de malha de serviço sob o aplicativo e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="4f1a2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1a2-104">SYNTAX</span></span>

### <span data-ttu-id="4f1a2-105">Stateless-Singleton (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4f1a2-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f1a2-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="4f1a2-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f1a2-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="4f1a2-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1a2-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="4f1a2-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1a2-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="4f1a2-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1a2-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="4f1a2-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1a2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f1a2-111">DESCRIPTION</span></span>
<span data-ttu-id="4f1a2-112">Esse cmdlet permite a criação de serviços sem estado ou estado no aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="4f1a2-113">O serviço deve sair no manifesto do aplicativo e o tipo deve ser o mesmo que o do manifesto.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="4f1a2-114">O nome do aplicativo deve ser um prefixo do nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="4f1a2-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f1a2-115">EXAMPLES</span></span>

### <span data-ttu-id="4f1a2-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f1a2-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="4f1a2-117">Este exemplo criará um novo serviço sem estado "testApp~testService1" com contagem de instâncias -1 (em todos os nós).</span><span class="sxs-lookup"><span data-stu-id="4f1a2-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="4f1a2-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4f1a2-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="4f1a2-119">Este exemplo criará um novo serviço stateful "testApp~testService2" com um destino de 5 nós.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="4f1a2-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1a2-120">PARAMETERS</span></span>

### <span data-ttu-id="4f1a2-121">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4f1a2-121">-ApplicationName</span></span>
<span data-ttu-id="4f1a2-122">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="4f1a2-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4f1a2-123">-ClusterName</span></span>
<span data-ttu-id="4f1a2-124">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4f1a2-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="4f1a2-125">-DefaultMoveCost</span></span>
<span data-ttu-id="4f1a2-126">Especifique o custo padrão de uma movimentação.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="4f1a2-127">Os custos mais altos fazem com que seja menos provável que o Gerenciador de Recursos de Cluster mova a replica ao tentar equilibrar o cluster</span><span class="sxs-lookup"><span data-stu-id="4f1a2-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="4f1a2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1a2-128">-DefaultProfile</span></span>
<span data-ttu-id="4f1a2-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1a2-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="4f1a2-130">-InstanceCount</span></span>
<span data-ttu-id="4f1a2-131">Especificar a contagem de instâncias para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="4f1a2-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="4f1a2-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="4f1a2-133">Especificar o tamanho mínimo de conjunto de replicas para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="4f1a2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f1a2-134">-Name</span></span>
<span data-ttu-id="4f1a2-135">Especifique o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="4f1a2-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="4f1a2-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="4f1a2-137">Indica que o serviço usa o esquema de partição nomeado.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="4f1a2-138">Os serviços que usam esse modelo geralmente têm dados que podem ser bucketed dentro de um conjunto limitado.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="4f1a2-139">Alguns exemplos comuns de campos de dados usados como chaves de partição nomeadas seriam regiões, códigos postais, grupos de clientes ou outros limites comerciais.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="4f1a2-140">-PartitionSchemeSing ltda</span><span class="sxs-lookup"><span data-stu-id="4f1a2-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="4f1a2-141">Indica que o serviço usa o esquema de partição de singleton.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="4f1a2-142">As partições singleton geralmente são usadas quando o serviço não exige qualquer roteamento adicional.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="4f1a2-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="4f1a2-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="4f1a2-144">Indica que o serviço usa o esquema de partição UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="4f1a2-145">Isso significa que cada partição possui um intervalo de teclas int64.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="4f1a2-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="4f1a2-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="4f1a2-147">Especificar a duração de espera de perda de quo quorum para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="4f1a2-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="4f1a2-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="4f1a2-149">Especificar a duração de espera de reinicialização de replica para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="4f1a2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f1a2-150">-ResourceGroupName</span></span>
<span data-ttu-id="4f1a2-151">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4f1a2-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="4f1a2-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="4f1a2-153">Especificar a duração da replica de stand by para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="4f1a2-154">-Estado</span><span class="sxs-lookup"><span data-stu-id="4f1a2-154">-Stateful</span></span>
<span data-ttu-id="4f1a2-155">Usar para serviço de estado</span><span class="sxs-lookup"><span data-stu-id="4f1a2-155">Use for stateful service</span></span>

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

### <span data-ttu-id="4f1a2-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="4f1a2-156">-Stateless</span></span>
<span data-ttu-id="4f1a2-157">Usar para serviços sem estado</span><span class="sxs-lookup"><span data-stu-id="4f1a2-157">Use for stateless service</span></span>

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

### <span data-ttu-id="4f1a2-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="4f1a2-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="4f1a2-159">Especificar o tamanho do conjunto de replicas de destino para o serviço</span><span class="sxs-lookup"><span data-stu-id="4f1a2-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="4f1a2-160">-Tipo</span><span class="sxs-lookup"><span data-stu-id="4f1a2-160">-Type</span></span>
<span data-ttu-id="4f1a2-161">Especifique o nome do tipo de serviço do aplicativo, deve existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="4f1a2-162">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4f1a2-162">-Confirm</span></span>
<span data-ttu-id="4f1a2-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1a2-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1a2-164">-WhatIf</span></span>
<span data-ttu-id="4f1a2-165">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f1a2-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1a2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1a2-167">CommonParameters</span></span>
<span data-ttu-id="4f1a2-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1a2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1a2-169">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f1a2-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1a2-170">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f1a2-170">INPUTS</span></span>

### <span data-ttu-id="4f1a2-171">System.String</span><span class="sxs-lookup"><span data-stu-id="4f1a2-171">System.String</span></span>

## <span data-ttu-id="4f1a2-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f1a2-172">OUTPUTS</span></span>

### <span data-ttu-id="4f1a2-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="4f1a2-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="4f1a2-174">Notas</span><span class="sxs-lookup"><span data-stu-id="4f1a2-174">NOTES</span></span>

## <span data-ttu-id="4f1a2-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f1a2-175">RELATED LINKS</span></span>
