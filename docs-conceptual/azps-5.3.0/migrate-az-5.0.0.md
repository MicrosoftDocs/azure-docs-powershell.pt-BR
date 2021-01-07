---
title: Guia de migração para o Az 5.0.0
description: Este guia de migração contém uma lista de alterações da falha feitas no Azure PowerShell no lançamento do Az versão 5.0.0.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893441"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="1d0ef-103">Guia de Migração para o Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="1d0ef-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="1d0ef-104">Este documento descreverá as alterações do Az entre as versões 4.0.0 e 5.0.0.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="1d0ef-105">Guia de Migração para o Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="1d0ef-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="1d0ef-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d0ef-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="1d0ef-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1d0ef-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="1d0ef-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1d0ef-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="1d0ef-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d0ef-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="1d0ef-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d0ef-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="1d0ef-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="1d0ef-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="1d0ef-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="1d0ef-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="1d0ef-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="1d0ef-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="1d0ef-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="1d0ef-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="1d0ef-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="1d0ef-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1d0ef-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="1d0ef-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1d0ef-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="1d0ef-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1d0ef-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="1d0ef-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="1d0ef-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="1d0ef-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1d0ef-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="1d0ef-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="1d0ef-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="1d0ef-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="1d0ef-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="1d0ef-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="1d0ef-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="1d0ef-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="1d0ef-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="1d0ef-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="1d0ef-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="1d0ef-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="1d0ef-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="1d0ef-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="1d0ef-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="1d0ef-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="1d0ef-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="1d0ef-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="1d0ef-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="1d0ef-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="1d0ef-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="1d0ef-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="1d0ef-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="1d0ef-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="1d0ef-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="1d0ef-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="1d0ef-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="1d0ef-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="1d0ef-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="1d0ef-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="1d0ef-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="1d0ef-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="1d0ef-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="1d0ef-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="1d0ef-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="1d0ef-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d0ef-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="1d0ef-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1d0ef-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="1d0ef-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="1d0ef-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="1d0ef-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1d0ef-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="1d0ef-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1d0ef-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="1d0ef-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d0ef-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="1d0ef-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="1d0ef-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="1d0ef-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="1d0ef-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="1d0ef-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="1d0ef-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="1d0ef-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="1d0ef-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1d0ef-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="1d0ef-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1d0ef-169">New-AzAksCluster</span></span>

- <span data-ttu-id="1d0ef-170">Não é mais compatível com o parâmetro `NodeOsType`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original. Ele sempre será `Linux`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="1d0ef-171">Não é mais compatível com o alias `ClientIdAndSecret` para o parâmetro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="1d0ef-172">O valor padrão de `NodeVmSetType` foi alterado de `AvailabilitySet` para `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="1d0ef-173">O valor padrão de `NetworkPlugin` foi alterado de `none` para `azure`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-174">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-175">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="1d0ef-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1d0ef-176">Set-AzAksCluster</span></span>

<span data-ttu-id="1d0ef-177">Não é mais compatível com o alias `ClientIdAndSecret` para o parâmetro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-178">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-179">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="1d0ef-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d0ef-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="1d0ef-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d0ef-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="1d0ef-182">Não é mais compatível com o parâmetro `StorageAccountName` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-183">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="1d0ef-184">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-184">After</span></span>

<span data-ttu-id="1d0ef-185">`Classic` foi preterido e `StorageAccountName` foi removido, pois ele só funcionava com um Registro de Contêiner Clássico.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="1d0ef-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="1d0ef-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="1d0ef-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="1d0ef-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="1d0ef-188">Remoção do parâmetro de opção `IncludeSlot` de todos os parâmetros, exceto de um conjunto de parâmetros de `Get-AzFunctionApp`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="1d0ef-189">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados quando `-IncludeSlot` for especificado.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="1d0ef-190">Essa funcionalidade foi interrompida na versão anterior do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="1d0ef-191">No entanto, isso foi corrigido.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="1d0ef-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="1d0ef-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="1d0ef-193">Correção de `-DisableApplicationInsights` em `New-AzFunctionApp` para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="1d0ef-194">Remoção do suporte para criar aplicativos de funções do PowerShell 6.2, pois o PowerShell 6.2 é EOL.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="1d0ef-195">As diretrizes atuais para os clientes é criar aplicativos de funções do PowerShell 7.0 como alternativa.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="1d0ef-196">Alteração da versão de runtime padrão da 6.2 para a 7.0 no Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro `RuntimeVersion` não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="1d0ef-197">Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro `RuntimeVersion` não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="1d0ef-198">No entanto, os usuários ainda poderão criar aplicativos de funções do Node 10 especificando `-Runtime Node` e `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="1d0ef-199">Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro `RuntimeVersion` não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="1d0ef-200">No entanto, os usuários ainda poderão criar aplicativos de funções do Python 3.7 especificando `-Runtime Python` e `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-201">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="1d0ef-202">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="1d0ef-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="1d0ef-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-204">New-AzKeyVault</span></span>

<span data-ttu-id="1d0ef-205">Não é mais compatível com o parâmetro `DisableSoftDelete` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-206">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="1d0ef-207">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-207">After</span></span>

<span data-ttu-id="1d0ef-208">A capacidade de atualizar a configuração de exclusão reversível será preterida no Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="1d0ef-209">Leia mais: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="1d0ef-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="1d0ef-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d0ef-210">Update-AzKeyVault</span></span>

<span data-ttu-id="1d0ef-211">Não é mais compatível com os parâmetros `EnableSoftDelete` e `SoftDeleteRetentionInDays`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-212">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="1d0ef-213">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-213">After</span></span>

<span data-ttu-id="1d0ef-214">A capacidade de atualizar a configuração de exclusão reversível será preterida no Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="1d0ef-215">Leia mais: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="1d0ef-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="1d0ef-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1d0ef-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="1d0ef-217">A propriedade `SecretValueText` do tipo `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` foi removida.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="1d0ef-218">A propriedade `SecretValueText` foi substituída por `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-219">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="1d0ef-220">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="1d0ef-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1d0ef-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="1d0ef-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1d0ef-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="1d0ef-223">Não é mais compatível com o parâmetro `ResourceId` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-224">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-225">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="1d0ef-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="1d0ef-227">Não é mais compatível com os parâmetros `RegistrationDefinitionName` e `RegistrationDefinitionResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-228">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-229">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="1d0ef-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="1d0ef-231">Não é mais compatível com os parâmetros `Id` e `ResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-232">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-233">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="1d0ef-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1d0ef-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="1d0ef-235">Não é mais compatível com os parâmetros `Id` e `ResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-236">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-237">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="1d0ef-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="1d0ef-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="1d0ef-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="1d0ef-240">Não é mais compatível com o parâmetro `ApiVersion` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-241">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-242">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="1d0ef-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="1d0ef-244">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="1d0ef-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-245">Get-AzDeployment</span></span>

<span data-ttu-id="1d0ef-246">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="1d0ef-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="1d0ef-248">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="1d0ef-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="1d0ef-250">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="1d0ef-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="1d0ef-252">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="1d0ef-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="1d0ef-254">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="1d0ef-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="1d0ef-256">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="1d0ef-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-257">New-AzDeployment</span></span>

<span data-ttu-id="1d0ef-258">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="1d0ef-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="1d0ef-260">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="1d0ef-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="1d0ef-262">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="1d0ef-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-263">Remove-AzDeployment</span></span>

<span data-ttu-id="1d0ef-264">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="1d0ef-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="1d0ef-266">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="1d0ef-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="1d0ef-268">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="1d0ef-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="1d0ef-270">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="1d0ef-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="1d0ef-272">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="1d0ef-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="1d0ef-274">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="1d0ef-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-275">Stop-AzDeployment</span></span>

<span data-ttu-id="1d0ef-276">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="1d0ef-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="1d0ef-278">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="1d0ef-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="1d0ef-280">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="1d0ef-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-281">Test-AzDeployment</span></span>

<span data-ttu-id="1d0ef-282">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="1d0ef-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="1d0ef-284">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="1d0ef-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="1d0ef-286">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="1d0ef-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1d0ef-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="1d0ef-288">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="1d0ef-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="1d0ef-290">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="1d0ef-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="1d0ef-292">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="1d0ef-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="1d0ef-294">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="1d0ef-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1d0ef-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="1d0ef-296">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="1d0ef-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="1d0ef-298">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="1d0ef-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1d0ef-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="1d0ef-300">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="1d0ef-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="1d0ef-302">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="1d0ef-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="1d0ef-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="1d0ef-304">O mesmo ocorre com `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="1d0ef-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1d0ef-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="1d0ef-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1d0ef-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="1d0ef-307">Não é mais compatível com o parâmetro `IsAzureADOnlyAuthentication` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-308">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="1d0ef-309">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="1d0ef-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="1d0ef-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="1d0ef-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1d0ef-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="1d0ef-312">Não é mais compatível com os parâmetros: `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` e `RestorePoint`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-313">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="1d0ef-314">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="1d0ef-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1d0ef-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="1d0ef-316">Não é mais compatível com os parâmetros `Suspend` e `Resume`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="1d0ef-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1d0ef-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="1d0ef-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="1d0ef-319">Não é mais compatível com o parâmetro `PrivateLinkResourceType` e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-320">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="1d0ef-321">Depois</span><span class="sxs-lookup"><span data-stu-id="1d0ef-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="1d0ef-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="1d0ef-323">O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="1d0ef-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="1d0ef-325">O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="1d0ef-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="1d0ef-327">O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="1d0ef-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1d0ef-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="1d0ef-329">O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="1d0ef-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="1d0ef-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="1d0ef-331">Não é mais compatível com os parâmetros `FilterType` e `FilterItem`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="1d0ef-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="1d0ef-332">Antes</span><span class="sxs-lookup"><span data-stu-id="1d0ef-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="1d0ef-333">After (após)</span><span class="sxs-lookup"><span data-stu-id="1d0ef-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
