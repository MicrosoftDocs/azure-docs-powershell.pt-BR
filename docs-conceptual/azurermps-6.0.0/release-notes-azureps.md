---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911996"
---
# <a name="release-notes"></a><span data-ttu-id="93927-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="93927-103">Release notes</span></span>

<span data-ttu-id="93927-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93927-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="93927-105">6.0.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="93927-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="93927-106">Geral</span><span class="sxs-lookup"><span data-stu-id="93927-106">General</span></span>
* <span data-ttu-id="93927-107">Definir dependência mínima de módulos do PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="93927-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="93927-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="93927-108">Azure.Storage</span></span>
* <span data-ttu-id="93927-109">Suporte como nome do contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="93927-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="93927-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93927-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="93927-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="93927-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="93927-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="93927-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="93927-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="93927-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="93927-114">Corrija o problema que a saída de algumas falhas de cmdlets de Armazenamento não contém informações de falhas de detalhes</span><span class="sxs-lookup"><span data-stu-id="93927-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="93927-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="93927-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="93927-116">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-117">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="93927-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="93927-118">AzureRM.Automation</span></span>
* <span data-ttu-id="93927-119">Remover o alias “Marcas” preterido dos cmdlets</span><span class="sxs-lookup"><span data-stu-id="93927-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="93927-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="93927-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="93927-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="93927-121">AzureRM.Batch</span></span>
* <span data-ttu-id="93927-122">Documentação de New-AzureBatchPool atualizada para remover o exemplo preterido</span><span class="sxs-lookup"><span data-stu-id="93927-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="93927-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="93927-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="93927-124">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-125">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="93927-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="93927-126">AzureRM.Compute</span></span>
* <span data-ttu-id="93927-127">Saída detalhada de 'New-AzureRmVm' e 'New-AzureRmVmss' dos parâmetros de suporte</span><span class="sxs-lookup"><span data-stu-id="93927-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="93927-128">'New-AzureRmVm' e 'New-AzureRmVmss' (conjunto de parâmetros simples) suportam a atribuição de identidades definidas pelo usuário e/ou definidas pelo sistema para as VMs.</span><span class="sxs-lookup"><span data-stu-id="93927-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="93927-129">Recurso de reimplantação de VMSS e PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="93927-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="93927-130">Adicionar um novo parâmetro de opção -Reimplantação e -PerformMaintenance a 'Set-AzureRmVmss' e 'Set-AzureRmVmssVM'</span><span class="sxs-lookup"><span data-stu-id="93927-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="93927-131">Adicionar o parâmetro de opção DisableVMAgent ao cmdlet 'Set-AzureRmVMOperatingSystem'</span><span class="sxs-lookup"><span data-stu-id="93927-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="93927-132">“New-AzureRmVm” e “New-AzureRmVmss” (conjunto de parâmetro simples) oferece suporte a uma imagem “Win10”.</span><span class="sxs-lookup"><span data-stu-id="93927-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="93927-133">O cmdlet 'Repair-AzureRmVmssServiceFabricUpdateDomain' é adicionado.</span><span class="sxs-lookup"><span data-stu-id="93927-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="93927-134">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-135">Consulte o guia de migração para obter mais detalhes</span><span class="sxs-lookup"><span data-stu-id="93927-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="93927-136">'Set-AzureRmVmDiskEncryptionExtension' torna os parâmetros do AAD opcionais</span><span class="sxs-lookup"><span data-stu-id="93927-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="93927-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="93927-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="93927-138">Remover o alias “Marcas” preterido dos cmdlets</span><span class="sxs-lookup"><span data-stu-id="93927-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="93927-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="93927-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="93927-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="93927-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="93927-141">Versão atualizada do SDK do .Net ADF para versão prévia 0.7.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="93927-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="93927-142">Parâmetros de execução adicional e a propriedade de gerenciadores de conexão na atividade de ExecuteSSISPackage</span><span class="sxs-lookup"><span data-stu-id="93927-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="93927-143">PostgreSql atualizado, serviço vinculado do MySql para usar a cadeia de conexão completa em vez de servidor, banco de dados, esquema, nome de usuário e senha</span><span class="sxs-lookup"><span data-stu-id="93927-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="93927-144">Removido o esquema do serviço vinculado do DB2</span><span class="sxs-lookup"><span data-stu-id="93927-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="93927-145">Propriedade de esquema removido do serviço vinculado de Teradata</span><span class="sxs-lookup"><span data-stu-id="93927-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="93927-146">Adição do LinkedService, Dataset e CopySource para Responsys</span><span class="sxs-lookup"><span data-stu-id="93927-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="93927-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="93927-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="93927-148">Remover o alias “Marcas” preterido dos cmdlets</span><span class="sxs-lookup"><span data-stu-id="93927-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="93927-149">'Novo AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="93927-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="93927-150">'Set-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="93927-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="93927-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93927-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="93927-152">Adicionar o novo recurso de alteração de Acl recursiva para Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="93927-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="93927-153">Adicionar um novo cmdlet para recuperar o resumo do conteúdo em um diretório</span><span class="sxs-lookup"><span data-stu-id="93927-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="93927-154">Adicionar um novo cmdlet para recuperar o uso do disco e despejo de Acl</span><span class="sxs-lookup"><span data-stu-id="93927-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="93927-155">Corrigir tipo de retorno do bool Set-AzureRmDataLakeStoreItemAcl para IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="93927-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="93927-156">Corrigir tipo de retorno do bool Set-AzureRmDataLakeStoreItemAclEntry para IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="93927-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="93927-157">Alterações de falha no Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem e Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93927-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="93927-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="93927-158">AzureRM.Dns</span></span>
* <span data-ttu-id="93927-159">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-160">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="93927-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="93927-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="93927-162">Ajuda atualizada para os cmdlets com exemplos ausentes</span><span class="sxs-lookup"><span data-stu-id="93927-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="93927-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="93927-163">AzureRM.Insights</span></span>
* <span data-ttu-id="93927-164">Apresentou várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="93927-165">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="93927-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="93927-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="93927-167">Habilitar marcas e Sku básico para o IotHub</span><span class="sxs-lookup"><span data-stu-id="93927-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="93927-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="93927-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="93927-169">Alterações de falha para dar suporte a cenários de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="93927-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="93927-170">Adicionados novos cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval e Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="93927-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="93927-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="93927-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="93927-172">Remover o alias “Marcas” preterido dos cmdlets</span><span class="sxs-lookup"><span data-stu-id="93927-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="93927-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="93927-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="93927-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="93927-174">AzureRM.Media</span></span>
* <span data-ttu-id="93927-175">Remover o alias “Marcas” preterido dos cmdlets</span><span class="sxs-lookup"><span data-stu-id="93927-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="93927-176">'Set-AzureRmMediaService'</span><span class="sxs-lookup"><span data-stu-id="93927-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="93927-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="93927-177">AzureRM.Network</span></span>
* <span data-ttu-id="93927-178">Adicionar suporte ao recurso do plano de proteção contra DDoS</span><span class="sxs-lookup"><span data-stu-id="93927-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="93927-179">Apresentou várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="93927-180">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="93927-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="93927-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="93927-182">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-183">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="93927-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="93927-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="93927-185">Apresenta várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="93927-186">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="93927-187">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="93927-187">AzureRM.Profile</span></span>
* <span data-ttu-id="93927-188">Habilitar salvamento automático de contexto por padrão</span><span class="sxs-lookup"><span data-stu-id="93927-188">Enable context autosave by default</span></span>
* <span data-ttu-id="93927-189">Adicionar propriedades USGovernmentOperationalInsightsEndpoint e USGovernmentOperationalInsightsEndpointResourceId ao ambiente do Azure para o Governos dos Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="93927-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="93927-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="93927-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="93927-191">Cabeçalho de Autenticação nos cenários do SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="93927-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="93927-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="93927-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="93927-193">Apresentou várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="93927-194">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="93927-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="93927-195">AzureRM.Resources</span></span>
* <span data-ttu-id="93927-196">Remover parâmetro obsoleto -AtScopeAndBelow da chamada Get-AzureRmRoledefinition</span><span class="sxs-lookup"><span data-stu-id="93927-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="93927-197">Incluir atribuições para USers/Groups/ServicePrincipals excluído no resultado Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="93927-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="93927-198">Adicionar completadores Guia para Escopo e ResourceType</span><span class="sxs-lookup"><span data-stu-id="93927-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="93927-199">Adicionar cmdlet de conveniência para criar ServicePrincipals</span><span class="sxs-lookup"><span data-stu-id="93927-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="93927-200">Mesclar a funcionalidade Get- e Find- em Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93927-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="93927-201">Adicionar Cmdlets do AD:</span><span class="sxs-lookup"><span data-stu-id="93927-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="93927-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="93927-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="93927-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="93927-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="93927-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="93927-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="93927-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="93927-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="93927-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="93927-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="93927-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="93927-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="93927-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="93927-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="93927-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="93927-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="93927-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="93927-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="93927-211">Atualizar sku de versão de imagem padrão do Linux</span><span class="sxs-lookup"><span data-stu-id="93927-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="93927-212">Atualização de sku padrão NewAzureServiceFabricCluster.cs do UbuntuServer1604</span><span class="sxs-lookup"><span data-stu-id="93927-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="93927-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="93927-213">AzureRM.Storage</span></span>
* <span data-ttu-id="93927-214">Apresentou várias alterações de falha</span><span class="sxs-lookup"><span data-stu-id="93927-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="93927-215">Consulte o guia de migração para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="93927-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="93927-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="93927-216">AzureRM.Websites</span></span>
* <span data-ttu-id="93927-217">Atualizar para a versão mais recente do SDK de sites</span><span class="sxs-lookup"><span data-stu-id="93927-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="93927-218">Propriedades adicionadas de -AssignIdentity e -Httpsonly para Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="93927-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="93927-219">Adicionados dois novos cmdlets: Get-AzureRmWebAppSnapshots e Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="93927-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
