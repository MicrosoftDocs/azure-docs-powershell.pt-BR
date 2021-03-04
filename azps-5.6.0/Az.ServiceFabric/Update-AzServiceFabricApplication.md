---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: febf0ecb24be1b419353142805c9f91e0c771de5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885838"
---
# <span data-ttu-id="edd7d-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="edd7d-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="edd7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="edd7d-103">Atualize um aplicativo de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="edd7d-103">Update a service fabric application.</span></span> <span data-ttu-id="edd7d-104">Isso permite atualizar os parâmetros do aplicativo e/ou atualizar a versão do tipo de aplicativo que disparará uma atualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="edd7d-105">Só dá suporte ARM aplicativos implantados.</span><span class="sxs-lookup"><span data-stu-id="edd7d-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="edd7d-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="edd7d-106">SYNTAX</span></span>

### <span data-ttu-id="edd7d-107">ByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="edd7d-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="edd7d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="edd7d-108">ByResourceId</span></span>
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

### <span data-ttu-id="edd7d-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edd7d-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd7d-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="edd7d-110">DESCRIPTION</span></span>
<span data-ttu-id="edd7d-111">Esse cmdlet pode ser usado para atualizar parâmetros de aplicativo e atualizar a versão do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="edd7d-112">A atualização do parâmetro só alterará o modelo no lado ARM, somente quando uma nova versão de tipo for usada, o comando disparará uma atualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="edd7d-113">A versão do tipo especificada já deve ser criada no cluster usando **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="edd7d-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="edd7d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edd7d-114">EXAMPLES</span></span>

### <span data-ttu-id="edd7d-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="edd7d-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="edd7d-116">Este exemplo iniciará uma atualização de aplicativo para atualizar a versão de tipo para "v2" que foi criada com **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="edd7d-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="edd7d-117">Os parâmetros de aplicativo usados devem ser definidos no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="edd7d-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="edd7d-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="edd7d-119">Este exemplo atualizará o número mínimo e máximo de restrições de nós para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="edd7d-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="edd7d-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="edd7d-121">Este exemplo iniciará uma atualização de aplicativo para atualizar a versão de tipo como "v2" e também define alguns parâmetros de política de atualização que terão efeito a partir da atualização atual.</span><span class="sxs-lookup"><span data-stu-id="edd7d-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="edd7d-122">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="edd7d-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="edd7d-123">Este exemplo atualiza os parâmetros do aplicativo, mas essas alterações só terão efeito até a próxima atualização de versão para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="edd7d-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="edd7d-124">PARAMETERS</span></span>

### <span data-ttu-id="edd7d-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="edd7d-125">-ApplicationParameter</span></span>
<span data-ttu-id="edd7d-126">Especifique os parâmetros do aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="edd7d-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="edd7d-127">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="edd7d-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="edd7d-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="edd7d-129">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="edd7d-129">Specify the application type version</span></span>

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

### <span data-ttu-id="edd7d-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="edd7d-130">-ClusterName</span></span>
<span data-ttu-id="edd7d-131">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="edd7d-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="edd7d-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="edd7d-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="edd7d-133">Indica se um evento de saúde de aviso deve ser tratado como um evento de erro durante a avaliação de saúde.</span><span class="sxs-lookup"><span data-stu-id="edd7d-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="edd7d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd7d-134">-DefaultProfile</span></span>
<span data-ttu-id="edd7d-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="edd7d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd7d-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="edd7d-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="edd7d-137">Especifica a porcentagem máxima de partições inocentadas por serviço permitidas pela política de saúde para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="edd7d-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="edd7d-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="edd7d-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="edd7d-139">Especifica a porcentagem máxima de réplicas inocentadas por serviço permitidas pela política de saúde para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="edd7d-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="edd7d-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="edd7d-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="edd7d-141">Especifica a porcentagem máxima de serviços não-essenciais permitidos pela política de saúde para o tipo de serviço padrão a ser usado para a atualização monitorada.</span><span class="sxs-lookup"><span data-stu-id="edd7d-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="edd7d-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="edd7d-142">-FailureAction</span></span>
<span data-ttu-id="edd7d-143">Especifica a ação a ser tomada se a atualização monitorada falhar.</span><span class="sxs-lookup"><span data-stu-id="edd7d-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="edd7d-144">Os valores aceitáveis para este parâmetro são Rollback ou Manual.</span><span class="sxs-lookup"><span data-stu-id="edd7d-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="edd7d-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="edd7d-145">-ForceRestart</span></span>
<span data-ttu-id="edd7d-146">Indica que o host de serviço é reiniciado mesmo que a atualização seja uma alteração somente de configuração.</span><span class="sxs-lookup"><span data-stu-id="edd7d-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="edd7d-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="edd7d-148">Especifica a duração, em segundos, após a qual o Service Fabric recupera a verificação de saúde se a verificação de saúde anterior falhar.</span><span class="sxs-lookup"><span data-stu-id="edd7d-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="edd7d-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="edd7d-150">Especifica a duração, em segundos, que o Service Fabric aguarda para verificar se o aplicativo está estável antes de mover para o próximo domínio de atualização ou concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="edd7d-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="edd7d-151">Essa duração de espera impede alterações de saúde não detectadas logo após a verificação de saúde ser executada.</span><span class="sxs-lookup"><span data-stu-id="edd7d-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="edd7d-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="edd7d-153">Especifica a duração, em segundos, que o Service Fabric aguarda antes de executar a verificação de saúde inicial após concluir a atualização no domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="edd7d-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="edd7d-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edd7d-154">-InputObject</span></span>
<span data-ttu-id="edd7d-155">O recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-155">The application resource.</span></span>

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

### <span data-ttu-id="edd7d-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="edd7d-156">-MaximumNodeCount</span></span>
<span data-ttu-id="edd7d-157">Especifica o número máximo de nós nos quais colocar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="edd7d-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="edd7d-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="edd7d-158">-MinimumNodeCount</span></span>
<span data-ttu-id="edd7d-159">Especifica o número mínimo de nós onde o Service Fabric reservará capacidade para este aplicativo</span><span class="sxs-lookup"><span data-stu-id="edd7d-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="edd7d-160">-Name</span><span class="sxs-lookup"><span data-stu-id="edd7d-160">-Name</span></span>
<span data-ttu-id="edd7d-161">Especificar o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="edd7d-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="edd7d-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd7d-162">-ResourceGroupName</span></span>
<span data-ttu-id="edd7d-163">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="edd7d-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="edd7d-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edd7d-164">-ResourceId</span></span>
<span data-ttu-id="edd7d-165">Arm ResourceId do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edd7d-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="edd7d-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="edd7d-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="edd7d-167">Especifica o mapa da política de saúde a ser usada para diferentes tipos de serviço como uma tabela de hash no seguinte formato: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="edd7d-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="edd7d-168">Por exemplo: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="edd7d-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="edd7d-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="edd7d-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="edd7d-170">Especifica a porcentagem máxima das instâncias de aplicativo implantadas nos nós no cluster que têm um estado de erro de saúde antes que o estado de saúde do aplicativo para o cluster seja erro.</span><span class="sxs-lookup"><span data-stu-id="edd7d-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="edd7d-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="edd7d-172">Especifica o tempo máximo, em segundos, que o Service Fabric leva para atualizar um único domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="edd7d-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="edd7d-173">Após esse período, a atualização falha.</span><span class="sxs-lookup"><span data-stu-id="edd7d-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="edd7d-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="edd7d-175">Especifica o tempo máximo que o Service Fabric aguarda para que um serviço seja reconfigurado em um estado seguro, se ainda não estiver em um estado seguro, antes que o Service Fabric prossiga com a atualização.</span><span class="sxs-lookup"><span data-stu-id="edd7d-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="edd7d-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="edd7d-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="edd7d-177">Especifica o tempo máximo, em segundos, que o Service Fabric leva para toda a atualização.</span><span class="sxs-lookup"><span data-stu-id="edd7d-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="edd7d-178">Após esse período, a atualização falha.</span><span class="sxs-lookup"><span data-stu-id="edd7d-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="edd7d-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edd7d-179">-Confirm</span></span>
<span data-ttu-id="edd7d-180">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd7d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd7d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd7d-181">-WhatIf</span></span>
<span data-ttu-id="edd7d-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="edd7d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd7d-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="edd7d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd7d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd7d-184">CommonParameters</span></span>
<span data-ttu-id="edd7d-185">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd7d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd7d-186">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edd7d-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd7d-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edd7d-187">INPUTS</span></span>

### <span data-ttu-id="edd7d-188">System.String</span><span class="sxs-lookup"><span data-stu-id="edd7d-188">System.String</span></span>

### <span data-ttu-id="edd7d-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="edd7d-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="edd7d-190">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="edd7d-190">OUTPUTS</span></span>

### <span data-ttu-id="edd7d-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="edd7d-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="edd7d-192">NOTES</span><span class="sxs-lookup"><span data-stu-id="edd7d-192">NOTES</span></span>

## <span data-ttu-id="edd7d-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edd7d-193">RELATED LINKS</span></span>
