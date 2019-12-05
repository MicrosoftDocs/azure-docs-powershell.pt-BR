---
title: Guia de migração para o Az 3.0.0
description: Este guia de migração contém uma lista das alterações da falha feitas no Azure PowerShell no lançamento da versão 3.0 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: e88752e0c997efc4f49161e358072803cb63450a
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656903"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="4ad25-103">Guia de migração para o Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4ad25-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="4ad25-104">Este documento descreve as alterações entre as versões 2.0.0 e 3.0.0 do Az</span><span class="sxs-lookup"><span data-stu-id="4ad25-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="4ad25-105">Guia de migração para o Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4ad25-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="4ad25-106">Batch</span><span class="sxs-lookup"><span data-stu-id="4ad25-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="4ad25-107">Incompatibilidade com versões anteriores do `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="4ad25-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="4ad25-108">Computação</span><span class="sxs-lookup"><span data-stu-id="4ad25-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="4ad25-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ad25-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="4ad25-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="4ad25-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="4ad25-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ad25-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="4ad25-112">Recursos</span><span class="sxs-lookup"><span data-stu-id="4ad25-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="4ad25-113">Incompatibilidade com versões anteriores do `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="4ad25-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="4ad25-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ad25-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="4ad25-115">Sql</span><span class="sxs-lookup"><span data-stu-id="4ad25-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="4ad25-116">Lote</span><span class="sxs-lookup"><span data-stu-id="4ad25-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="4ad25-117">`Get-AzBatchNodeAgentSku` foi removido e substituído por `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="4ad25-118">`Get-AzBatchSupportedImage` retorna os mesmos dados que `Get-AzBatchNodeAgentSku`, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="4ad25-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="4ad25-119">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="4ad25-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="4ad25-120">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="4ad25-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-121">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="4ad25-122">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="4ad25-123">Incompatibilidade com a versão anterior do módulo Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ad25-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="4ad25-124">A versão 2.0.1 do módulo "Az.Batch" é incompatível com as versões anteriores (versão 1.7.0 ou anterior) do módulo "Az.Resources".</span><span class="sxs-lookup"><span data-stu-id="4ad25-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="4ad25-125">Assim, não será possível importar a versão 1.7.0 do módulo "Az.Resources" quando a versão 2.0.1 do módulo "Az.Batch" for importada.</span><span class="sxs-lookup"><span data-stu-id="4ad25-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="4ad25-126">Para corrigir esse problema, basta atualizar o módulo "Az.Resources" para a versão 1.7.1 ou posterior, ou simplesmente instalar a versão mais recente do módulo "Az".</span><span class="sxs-lookup"><span data-stu-id="4ad25-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="4ad25-127">Computação</span><span class="sxs-lookup"><span data-stu-id="4ad25-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="4ad25-128">O parâmetro `UploadSizeInBytes` será usado em vez do `DiskSizeGB` para `New-AzDiskConfig` quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="4ad25-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-129">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="4ad25-130">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="4ad25-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ad25-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="4ad25-132">Atualização do cmdlet `Get-AzHDInsightJobOutput` para dar suporte ao acesso granular baseado em função à chave de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ad25-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="4ad25-133">Os usuários com as funções Operador do Cluster HDInsight, Colaborador ou Proprietário não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="4ad25-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="4ad25-134">Os usuários com apenas a função Leitor precisarão especificar o parâmetro `DefaultStorageAccountKey` explicitamente.</span><span class="sxs-lookup"><span data-stu-id="4ad25-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-135">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="4ad25-136">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="4ad25-137">O cmdlet `Add-AzHDInsightConfigValue` removeu o alias para `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-138">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-138">Before</span></span>
<span data-ttu-id="4ad25-139">Uso do alias preterido</span><span class="sxs-lookup"><span data-stu-id="4ad25-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="4ad25-140">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="4ad25-141">Adição de um novo cmdlet `Disable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="4ad25-142">Use este cmdlet para desabilitar o monitoramento em um cluster HDInsight (substitui `Disable-AzHDInsightOperationsManagementSuite` e `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="4ad25-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-143">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="4ad25-144">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="4ad25-145">Adição de um novo cmdlet `Enable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="4ad25-146">Use este cmdlet para habilitar o monitoramento em um cluster HDInsight (substitui `Enable-AzHDInsightOperationsManagementSuite` e `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="4ad25-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-147">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="4ad25-148">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="4ad25-149">Adição de um novo cmdlet `Get-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="4ad25-150">Use este cmdlet para obter o status da instalação de monitoramento em um cluster do Azure HDInsight (substitui `Get-AzHDInsightOperationsManagementSuite` e `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="4ad25-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-151">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="4ad25-152">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="4ad25-153">O cmdlet `Get-HDInsightProperty` removeu o alias para `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-154">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-154">Before</span></span>
<span data-ttu-id="4ad25-155">Uso do alias preterido</span><span class="sxs-lookup"><span data-stu-id="4ad25-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="4ad25-156">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="4ad25-157">Remoção dos cmdlets `Grant-AzHDInsightRdpServicesAccess` e `Revoke-AzHDInsightRdpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="4ad25-158">Eles não são mais necessários porque não há suporte para os clusters que usam o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4ad25-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="4ad25-159">Em vez disso, crie um cluster que usa o tipo de sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="4ad25-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="4ad25-160">O tipo de saída de `Remove-AzHDInsightCluster` foi alterado de `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` para `bool`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-161">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="4ad25-162">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="4ad25-163">O cmdlet foi preterido.</span><span class="sxs-lookup"><span data-stu-id="4ad25-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="4ad25-164">Não há nenhuma substituição para ele.</span><span class="sxs-lookup"><span data-stu-id="4ad25-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="4ad25-165">O tipo de saída de `Set-AzHDInsightGatewayCredential` foi alterado de `HttpConnectivitySettings` para `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="4ad25-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="4ad25-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="4ad25-167">Este alias foi removido. Use `New-AzIotHubImportDevice` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4ad25-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-168">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="4ad25-169">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="4ad25-170">Este alias foi removido. Use `New-AzIotHubExportDevice` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4ad25-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-171">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="4ad25-172">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="4ad25-173">O parâmetro `EventHubEndPointName` será preterido sem ser substituído, pois IotHub vem com apenas um ponto de extremidade interno ("events") que pode manipular mensagens do sistema e do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ad25-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-174">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="4ad25-175">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="4ad25-176">O parâmetro `EventHubEndPointName` será preterido sem ser substituído, pois IotHub vem com apenas um ponto de extremidade interno ("events") que pode manipular mensagens do sistema e do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ad25-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-177">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="4ad25-178">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="4ad25-179">O parâmetro `EventHubEndPointName` será preterido sem ser substituído, pois IotHub vem com apenas um ponto de extremidade interno ("events") que pode manipular mensagens do sistema e do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ad25-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-180">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="4ad25-181">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="4ad25-182">O parâmetro `OperationsMonitoringProperties` será preterido sem ser substituído, pois IotHub não está mais usando um ponto de extremidade interno ("operationsMonitoringEvents").</span><span class="sxs-lookup"><span data-stu-id="4ad25-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="4ad25-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ad25-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="4ad25-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` e `ASRRecoveryPlanGroup.EndGroupActions` são removidos da saída.</span><span class="sxs-lookup"><span data-stu-id="4ad25-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="4ad25-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` e `ASRRecoveryPlanGroup.EndGroupActions` são removidos da saída.</span><span class="sxs-lookup"><span data-stu-id="4ad25-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="4ad25-186">O parâmetro IncludeDiskId é alterado para oferecer suporte para a gravação direta em um disco gerenciado no Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4ad25-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-187">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="4ad25-188">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="4ad25-189">Recursos</span><span class="sxs-lookup"><span data-stu-id="4ad25-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="4ad25-190">Incompatibilidade com a versão anterior do módulo Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ad25-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="4ad25-191">A versão 1.7.1 do módulo "Az.Resources" é incompatível com as versões anteriores (versão 1.1.2 ou anterior) do módulo "Az.Batch".</span><span class="sxs-lookup"><span data-stu-id="4ad25-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="4ad25-192">Assim, não será possível importar a versão 1.1.2 do módulo "Az.Batch" quando a versão 1.7.1 do módulo "Az.Resources" for importada.</span><span class="sxs-lookup"><span data-stu-id="4ad25-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="4ad25-193">Para corrigir esse problema, basta atualizar o módulo "Az.Batch" para a versão 2.0.1 ou posterior, ou simplesmente instalar a versão mais recente do módulo "Az".</span><span class="sxs-lookup"><span data-stu-id="4ad25-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="4ad25-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ad25-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="4ad25-195">`Add-ServiceFabricApplicationCertificate` foi removido, pois esse cenário é abordado por `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-196">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="4ad25-197">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="4ad25-198">Sql</span><span class="sxs-lookup"><span data-stu-id="4ad25-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="4ad25-199">Observe que a conexão segura foi preterida e, portanto, o comando é removido.</span><span class="sxs-lookup"><span data-stu-id="4ad25-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="4ad25-200">Use a folha do banco de dados SQL no portal do Azure para exibir as cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="4ad25-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="4ad25-201">O alias `Get-AzSqlDatabaseIndexRecommendations` é removido.</span><span class="sxs-lookup"><span data-stu-id="4ad25-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="4ad25-202">Use `Get-AzSqlDatabaseIndexRecommendation` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4ad25-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="4ad25-203">O alias `Get-AzSqlDatabaseRestorePoints` é removido.</span><span class="sxs-lookup"><span data-stu-id="4ad25-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="4ad25-204">Use `Get-AzSqlDatabaseRestorePoint` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4ad25-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="4ad25-205">O cmdlet `Get-AzSqlDatabaseAudit` está substituindo este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad25-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="4ad25-206">O tipo de saída está sendo alterado do tipo existente: 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' para o novo tipo: 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removendo as propriedades `AuditState` e `StorageAccountName`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="4ad25-207">e `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="4ad25-208">Os scripts podem recuperar informações da conta de armazenamento da nova propriedade `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-209">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="4ad25-210">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="4ad25-211">O cmdlet `Set-AzSqlDatabaseAudit` está substituindo este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad25-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="4ad25-212">O tipo de saída está sendo alterado do tipo existente: 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' para o novo tipo :'bool'</span><span class="sxs-lookup"><span data-stu-id="4ad25-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-213">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-214">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="4ad25-215">O cmdlet `Get-AzSqlServerAudit` está substituindo este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad25-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="4ad25-216">O tipo de saída está sendo alterado do tipo existente: 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' para o novo tipo: 'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span><span class="sxs-lookup"><span data-stu-id="4ad25-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="4ad25-217">As propriedades `AuditState`, `StorageAccountName` e `StorageAccountSubscriptionId` são removidas.</span><span class="sxs-lookup"><span data-stu-id="4ad25-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="4ad25-218">Os scripts que usam as propriedades `StorageAccountName` e `StorageAccountSubscriptionId` podem recuperar essas informações da nova propriedade `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="4ad25-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-219">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="4ad25-220">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="4ad25-221">O cmdlet `Set-AzSqlServerAudit` está substituindo este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad25-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="4ad25-222">O tipo de saída está sendo alterado do tipo existente: 'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' para o novo tipo :'bool'</span><span class="sxs-lookup"><span data-stu-id="4ad25-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-223">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="4ad25-224">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-225">O cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` é substituído por `Get-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-226">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-227">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-228">O cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` é substituído por `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-229">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-230">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-231">O cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` é substituído por `Update-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-232">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="4ad25-233">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-234">O cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` é substituído por `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-235">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-236">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-237">O cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` é substituído por `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-238">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="4ad25-239">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="4ad25-240">O cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` é substituído por `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-241">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-242">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-243">O cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` é substituído por `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-244">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="4ad25-245">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-246">O cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` é substituído por `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-247">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-248">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-249">O cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` é substituído por `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-250">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-251">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-252">O cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` é substituído por `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-253">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="4ad25-254">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-255">O cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` é substituído por `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-256">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-257">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-258">O cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` é substituído por `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-259">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-260">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-261">O cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` é substituído por `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-262">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="4ad25-263">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-264">O cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` é substituído por `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-265">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-266">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-267">O cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` é substituído por `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-268">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-269">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-270">O cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` é substituído por `Update-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-271">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="4ad25-272">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-273">O cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` é substituído por `Get-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-274">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-275">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="4ad25-276">O cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` é substituído por `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-277">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-278">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="4ad25-279">O cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` é excluído e nenhum cmdlet o substitui</span><span class="sxs-lookup"><span data-stu-id="4ad25-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="4ad25-280">O cmdlet `Get-AzSqlServerThreatDetectionPolicy` é substituído por `Get-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-281">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="4ad25-282">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="4ad25-283">O cmdlet `Remove-AzSqlServerThreatDetectionPolicy` é substituído por `Clear-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-284">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-285">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="4ad25-286">O cmdlet `Set-AzSqlServerThreatDetectionPolicy` é substituído por `Update-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-287">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="4ad25-288">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="4ad25-289">O cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` é substituído por `Get-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-290">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="4ad25-291">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="4ad25-292">O cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` é substituído por `Update-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-293">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="4ad25-294">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="4ad25-295">O cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` é substituído por `Clear-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="4ad25-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="4ad25-296">Antes</span><span class="sxs-lookup"><span data-stu-id="4ad25-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="4ad25-297">após</span><span class="sxs-lookup"><span data-stu-id="4ad25-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
