---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: 779561ee3ff0a0b687104bd828890c314612f100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281590"
---
# <span data-ttu-id="1cf17-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1cf17-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1cf17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cf17-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf17-103">Atualize um aplicativo do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="1cf17-103">Update a service fabric application.</span></span> <span data-ttu-id="1cf17-104">Isso permite atualizar os parâmetros do aplicativo e/ou atualizar a versão do tipo de aplicativo, que acionará uma atualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="1cf17-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cf17-105">SYNTAX</span></span>

### <span data-ttu-id="1cf17-106">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cf17-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cf17-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1cf17-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf17-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1cf17-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cf17-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cf17-109">DESCRIPTION</span></span>
<span data-ttu-id="1cf17-110">Esse cmdlet pode ser usado para atualizar os parâmetros do aplicativo e atualizar a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="1cf17-111">Atualizar o parâmetro somente alterará o modelo no braço, apenas quando uma nova versão do tipo for usada, o comando acionará uma atualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="1cf17-112">A versão de tipo especificada já deve ser criada no cluster usando **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="1cf17-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="1cf17-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cf17-113">EXAMPLES</span></span>

### <span data-ttu-id="1cf17-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1cf17-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1cf17-115">Este exemplo iniciará uma atualização do aplicativo para atualizar a versão do tipo para "v2", que foi criada com **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="1cf17-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="1cf17-116">Os parâmetros do aplicativo usados devem ser definidos no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="1cf17-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1cf17-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="1cf17-118">Este exemplo atualizará o número mínimo e máximo de restrições de nós para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="1cf17-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1cf17-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="1cf17-120">Este exemplo iniciará uma atualização do aplicativo para atualizar a versão do tipo para "v2" e também definirá alguns parâmetros da política de atualização que entrarão em vigor na atualização atual.</span><span class="sxs-lookup"><span data-stu-id="1cf17-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="1cf17-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="1cf17-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1cf17-122">Este exemplo atualiza os parâmetros do aplicativo, mas essas alterações só serão efetivadas até a próxima atualização da versão para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="1cf17-123">OS</span><span class="sxs-lookup"><span data-stu-id="1cf17-123">PARAMETERS</span></span>

### <span data-ttu-id="1cf17-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="1cf17-124">-ApplicationParameter</span></span>
<span data-ttu-id="1cf17-125">Especifique os parâmetros do aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="1cf17-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="1cf17-126">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1cf17-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="1cf17-128">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1cf17-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1cf17-129">-ClusterName</span></span>
<span data-ttu-id="1cf17-130">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1cf17-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="1cf17-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="1cf17-132">Indica se um evento de integridade de aviso deve ser tratado como um evento de erro durante a avaliação de integridade.</span><span class="sxs-lookup"><span data-stu-id="1cf17-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf17-133">-DefaultProfile</span></span>
<span data-ttu-id="1cf17-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf17-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cf17-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="1cf17-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="1cf17-136">Especifica a porcentagem máxima de partições unhelthy por serviço permitidas pela política de integridade para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="1cf17-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="1cf17-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="1cf17-138">Especifica a porcentagem máxima de réplicas do unhelthy por serviço permitida pela política de integridade para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="1cf17-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="1cf17-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="1cf17-140">Especifica a porcentagem máxima de serviços de unhelthy permitidos pela política de integridade para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="1cf17-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-141">-Falha na</span><span class="sxs-lookup"><span data-stu-id="1cf17-141">-FailureAction</span></span>
<span data-ttu-id="1cf17-142">Especifica a ação a ser tomada se a atualização monitorada falhar.</span><span class="sxs-lookup"><span data-stu-id="1cf17-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="1cf17-143">Os valores aceitáveis para esse parâmetro são rollback ou manual.</span><span class="sxs-lookup"><span data-stu-id="1cf17-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="1cf17-144">-ForceRestart</span></span>
<span data-ttu-id="1cf17-145">Indica que o host de serviço é reiniciado mesmo se a atualização for uma alteração somente de configuração.</span><span class="sxs-lookup"><span data-stu-id="1cf17-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="1cf17-147">Especifica a duração, em segundos, após a qual o Service Fabric tentará novamente a verificação de integridade se a verificação de integridade anterior falhar.</span><span class="sxs-lookup"><span data-stu-id="1cf17-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="1cf17-149">Especifica a duração, em segundos, que a malha de serviço aguarda para verificar se o aplicativo é estável antes de passar para o próximo domínio de atualização ou para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="1cf17-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="1cf17-150">Essa duração de espera impede alterações não detectadas de integridade logo após a verificação de integridade.</span><span class="sxs-lookup"><span data-stu-id="1cf17-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="1cf17-152">Especifica a duração, em segundos, que a malha de serviço aguarda antes de realizar a verificação de integridade inicial após concluir a atualização no domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="1cf17-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cf17-153">-InputObject</span></span>
<span data-ttu-id="1cf17-154">O recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1cf17-155">-MaximumNodeCount</span></span>
<span data-ttu-id="1cf17-156">Especifica o número máximo de nós nos quais colocar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="1cf17-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1cf17-157">-MinimumNodeCount</span></span>
<span data-ttu-id="1cf17-158">Especifica o número mínimo de nós em que o Service Fabric reservará capacidade para este aplicativo</span><span class="sxs-lookup"><span data-stu-id="1cf17-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cf17-159">-Name</span></span>
<span data-ttu-id="1cf17-160">Especificar o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1cf17-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf17-161">-ResourceGroupName</span></span>
<span data-ttu-id="1cf17-162">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cf17-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cf17-163">-ResourceId</span></span>
<span data-ttu-id="1cf17-164">Resourcebinding do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cf17-164">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="1cf17-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="1cf17-166">Especifica o mapa da política de integridade a ser usada para tipos de serviço diferentes como uma tabela de hash no seguinte formato: @ {"imtypename": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="1cf17-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="1cf17-167">Por exemplo: @ {"ServiceTypeName01" = "5, 10, 5"; "ServiceTypeName02" = "5, 5, 5"}</span><span class="sxs-lookup"><span data-stu-id="1cf17-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="1cf17-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="1cf17-169">Especifica o percentual máximo das instâncias de aplicativo implantadas nos nós do cluster que têm um estado de integridade de erro antes do estado de integridade do aplicativo para o cluster ser um erro.</span><span class="sxs-lookup"><span data-stu-id="1cf17-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="1cf17-171">Especifica o tempo máximo, em segundos, que o Service Fabric leva para atualizar um único domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="1cf17-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="1cf17-172">Após esse período, a atualização falha.</span><span class="sxs-lookup"><span data-stu-id="1cf17-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="1cf17-174">Especifica o tempo máximo que a malha de serviço aguarda para um serviço ser reconfigurado em um estado seguro, se ainda não estiver em um estado seguro, antes que a malha de serviço prossiga com a atualização.</span><span class="sxs-lookup"><span data-stu-id="1cf17-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="1cf17-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="1cf17-176">Especifica o tempo máximo, em segundos, que o Service Fabric leva para toda a atualização.</span><span class="sxs-lookup"><span data-stu-id="1cf17-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="1cf17-177">Após esse período, a atualização falha.</span><span class="sxs-lookup"><span data-stu-id="1cf17-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf17-178">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1cf17-178">-Confirm</span></span>
<span data-ttu-id="1cf17-179">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cf17-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf17-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf17-180">-WhatIf</span></span>
<span data-ttu-id="1cf17-181">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cf17-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf17-182">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cf17-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf17-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf17-183">CommonParameters</span></span>
<span data-ttu-id="1cf17-184">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cf17-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf17-185">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cf17-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf17-186">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cf17-186">INPUTS</span></span>

### <span data-ttu-id="1cf17-187">System. String</span><span class="sxs-lookup"><span data-stu-id="1cf17-187">System.String</span></span>

### <span data-ttu-id="1cf17-188">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1cf17-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1cf17-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cf17-189">OUTPUTS</span></span>

### <span data-ttu-id="1cf17-190">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1cf17-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1cf17-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cf17-191">NOTES</span></span>

## <span data-ttu-id="1cf17-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cf17-192">RELATED LINKS</span></span>
