---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 3806a1c609a71c53c0bddc5bafd51d845c0c296e
ms.sourcegitcommit: 16904e0a72c55fb81248e0252769defb86c50f36
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/10/2020
ms.locfileid: "75831637"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d4bdb-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4bdb-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d4bdb-104">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="d4bdb-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-105">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-106">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d4bdb-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-107">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-108">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-108">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-109">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-110">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d4bdb-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4bdb-112">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d4bdb-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d4bdb-114">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4bdb-115">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-115">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d4bdb-116">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4bdb-117">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-117">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d4bdb-118">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4bdb-119">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-119">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d4bdb-120">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d4bdb-121">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-121">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d4bdb-122">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4bdb-123">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-123">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d4bdb-124">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4bdb-125">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-125">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d4bdb-126">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d4bdb-127">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-127">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d4bdb-128">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d4bdb-129">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d4bdb-130">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d4bdb-131">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-132">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-133">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d4bdb-134">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d4bdb-135">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d4bdb-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d4bdb-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="d4bdb-137">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="d4bdb-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-138">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-139">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="d4bdb-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4bdb-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4bdb-140">Az.HDInsight</span></span>
* <span data-ttu-id="d4bdb-141">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d4bdb-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4bdb-142">Az.MachineLearning</span></span>
* <span data-ttu-id="d4bdb-143">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="d4bdb-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d4bdb-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d4bdb-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4bdb-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d4bdb-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d4bdb-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4bdb-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d4bdb-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4bdb-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d4bdb-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d4bdb-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="d4bdb-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d4bdb-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-151">Az.Network</span></span>
* <span data-ttu-id="d4bdb-152">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="d4bdb-152">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-154">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d4bdb-155">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d4bdb-156">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d4bdb-157">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-158">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-159">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-160">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-161">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d4bdb-162">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="d4bdb-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d4bdb-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d4bdb-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d4bdb-164">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="d4bdb-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-165">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-166">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="d4bdb-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d4bdb-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d4bdb-168">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="d4bdb-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="d4bdb-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d4bdb-170">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d4bdb-171">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-171">General</span></span>
* <span data-ttu-id="d4bdb-172">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-173">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-174">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="d4bdb-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d4bdb-175">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="d4bdb-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4bdb-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-176">Az.Batch</span></span>
* <span data-ttu-id="d4bdb-177">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-178">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-179">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-180">Az.FrontDoor</span></span>
* <span data-ttu-id="d4bdb-181">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="d4bdb-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d4bdb-182">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="d4bdb-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4bdb-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4bdb-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4bdb-184">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="d4bdb-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-185">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-186">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="d4bdb-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d4bdb-187">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="d4bdb-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d4bdb-188">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-189">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-190">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d4bdb-191">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="d4bdb-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d4bdb-192">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-193">Az.Network</span></span>
* <span data-ttu-id="d4bdb-194">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-195">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-196">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d4bdb-197">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-198">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-199">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-200">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-201">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="d4bdb-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d4bdb-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d4bdb-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d4bdb-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4bdb-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d4bdb-204">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d4bdb-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="d4bdb-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d4bdb-206">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d4bdb-207">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="d4bdb-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d4bdb-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d4bdb-210">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d4bdb-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="d4bdb-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d4bdb-212">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d4bdb-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d4bdb-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d4bdb-214">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4bdb-215">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d4bdb-215">Highlights since the last major release</span></span>
* <span data-ttu-id="d4bdb-216">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d4bdb-217">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-218">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-219">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-219">VM Reapply feature</span></span>
    - <span data-ttu-id="d4bdb-220">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d4bdb-221">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d4bdb-222">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d4bdb-223">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d4bdb-224">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4bdb-225">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4bdb-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d4bdb-226">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="d4bdb-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d4bdb-227">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d4bdb-228">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="d4bdb-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d4bdb-229">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d4bdb-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4bdb-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d4bdb-231">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4bdb-232">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-232">Get the Order</span></span>
* <span data-ttu-id="d4bdb-233">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4bdb-234">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-234">Create new Order</span></span>
* <span data-ttu-id="d4bdb-235">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4bdb-236">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-236">Remove the Order</span></span>
* <span data-ttu-id="d4bdb-237">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d4bdb-238">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="d4bdb-238">Now creates Local Share</span></span>
* <span data-ttu-id="d4bdb-239">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d4bdb-240">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="d4bdb-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d4bdb-241">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d4bdb-242">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d4bdb-243">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4bdb-244">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="d4bdb-245">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4bdb-246">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-246">Create new Triggers</span></span>
* <span data-ttu-id="d4bdb-247">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4bdb-248">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-249">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-250">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d4bdb-251">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-253">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-254">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-255">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-256">Az.FrontDoor</span></span>
* <span data-ttu-id="d4bdb-257">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d4bdb-258">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d4bdb-259">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="d4bdb-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d4bdb-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-261">Az.Network</span></span>
* <span data-ttu-id="d4bdb-262">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d4bdb-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d4bdb-263">Az.PrivateDns</span></span>
* <span data-ttu-id="d4bdb-264">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-266">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d4bdb-267">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d4bdb-268">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4bdb-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-269">Az.RedisCache</span></span>
* <span data-ttu-id="d4bdb-270">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d4bdb-271">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d4bdb-272">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-273">Az.Resources</span></span>
- <span data-ttu-id="d4bdb-274">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d4bdb-275">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="d4bdb-276">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d4bdb-277">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d4bdb-278">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-279">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-280">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d4bdb-281">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="d4bdb-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d4bdb-282">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4bdb-283">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-283">General</span></span>
* <span data-ttu-id="d4bdb-284">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-285">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-286">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4bdb-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-287">Az.Advisor</span></span>
* <span data-ttu-id="d4bdb-288">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4bdb-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-289">Az.Batch</span></span>
* <span data-ttu-id="d4bdb-290">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d4bdb-291">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d4bdb-292">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d4bdb-293">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d4bdb-294">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d4bdb-295">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d4bdb-296">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d4bdb-297">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d4bdb-298">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d4bdb-299">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4bdb-300">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d4bdb-301">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d4bdb-302">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4bdb-303">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d4bdb-304">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d4bdb-305">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d4bdb-306">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d4bdb-307">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d4bdb-308">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d4bdb-309">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="d4bdb-310">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4bdb-311">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4bdb-312">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d4bdb-313">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="d4bdb-314">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d4bdb-315">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="d4bdb-316">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d4bdb-317">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d4bdb-318">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d4bdb-319">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d4bdb-320">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d4bdb-321">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d4bdb-322">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d4bdb-323">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d4bdb-324">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d4bdb-325">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-326">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-327">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d4bdb-328">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-329">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-330">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="d4bdb-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d4bdb-331">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d4bdb-332">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="d4bdb-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4bdb-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d4bdb-334">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4bdb-335">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d4bdb-336">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="d4bdb-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d4bdb-337">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4bdb-338">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="d4bdb-338">Breaking changes</span></span>
    - <span data-ttu-id="d4bdb-339">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d4bdb-340">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-341">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-342">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-344">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="d4bdb-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d4bdb-345">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d4bdb-346">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="d4bdb-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d4bdb-347">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="d4bdb-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d4bdb-348">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d4bdb-349">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="d4bdb-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-350">Az.FrontDoor</span></span>
* <span data-ttu-id="d4bdb-351">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4bdb-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4bdb-352">Az.HDInsight</span></span>
* <span data-ttu-id="d4bdb-353">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d4bdb-354">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d4bdb-355">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d4bdb-356">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d4bdb-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4bdb-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4bdb-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4bdb-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4bdb-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d4bdb-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4bdb-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d4bdb-362">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="d4bdb-363">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4bdb-364">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4bdb-365">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d4bdb-366">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d4bdb-367">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d4bdb-368">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d4bdb-369">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d4bdb-370">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d4bdb-371">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d4bdb-372">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d4bdb-373">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="d4bdb-374">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-375">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-376">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-376">Breaking changes:</span></span>
    - <span data-ttu-id="d4bdb-377">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4bdb-378">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4bdb-379">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4bdb-380">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4bdb-381">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d4bdb-382">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d4bdb-383">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d4bdb-384">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d4bdb-385">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4bdb-386">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4bdb-387">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4bdb-388">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-390">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-391">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d4bdb-392">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d4bdb-393">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-394">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-395">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-396">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-397">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-398">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="d4bdb-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-399">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-400">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-401">Az.Network</span></span>
* <span data-ttu-id="d4bdb-402">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d4bdb-403">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4bdb-409">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d4bdb-410">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-410">New cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d4bdb-412">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d4bdb-413">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d4bdb-414">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d4bdb-415">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d4bdb-416">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d4bdb-417">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d4bdb-418">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d4bdb-419">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-419">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d4bdb-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4bdb-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4bdb-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4bdb-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d4bdb-425">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4bdb-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d4bdb-426">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4bdb-427">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4bdb-428">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4bdb-429">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d4bdb-430">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d4bdb-431">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d4bdb-432">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-432">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d4bdb-434">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4bdb-435">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4bdb-436">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4bdb-437">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4bdb-438">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4bdb-439">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d4bdb-440">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="d4bdb-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d4bdb-441">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-441">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d4bdb-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d4bdb-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d4bdb-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d4bdb-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d4bdb-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d4bdb-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d4bdb-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d4bdb-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d4bdb-448">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4bdb-449">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d4bdb-450">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d4bdb-451">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d4bdb-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d4bdb-452">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d4bdb-453">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4bdb-454">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d4bdb-455">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d4bdb-456">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d4bdb-457">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d4bdb-458">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d4bdb-459">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-459">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="d4bdb-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d4bdb-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d4bdb-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-465">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-466">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-467">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d4bdb-468">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d4bdb-469">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d4bdb-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d4bdb-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d4bdb-472">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4bdb-473">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d4bdb-474">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="d4bdb-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="d4bdb-475">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-476">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-477">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d4bdb-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4bdb-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4bdb-480">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="d4bdb-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d4bdb-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4bdb-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d4bdb-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4bdb-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="d4bdb-483">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4bdb-484">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-484">General</span></span>
* <span data-ttu-id="d4bdb-485">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-486">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-487">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-488">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-489">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d4bdb-490">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="d4bdb-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-491">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-492">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="d4bdb-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-493">Az.Batch</span></span>
* <span data-ttu-id="d4bdb-494">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-495">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-496">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4bdb-497">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d4bdb-498">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="d4bdb-499">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-500">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-501">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d4bdb-502">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d4bdb-503">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-505">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="d4bdb-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4bdb-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4bdb-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4bdb-507">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d4bdb-508">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d4bdb-509">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="d4bdb-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d4bdb-510">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-511">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-512">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d4bdb-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d4bdb-513">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4bdb-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-514">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-515">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="d4bdb-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d4bdb-516">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d4bdb-517">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="d4bdb-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d4bdb-518">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-519">Az.Network</span></span>
* <span data-ttu-id="d4bdb-520">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d4bdb-521">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d4bdb-522">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-522">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d4bdb-524">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4bdb-525">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d4bdb-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d4bdb-526">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="d4bdb-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4bdb-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4bdb-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4bdb-530">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="d4bdb-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d4bdb-531">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="d4bdb-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d4bdb-532">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d4bdb-533">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4bdb-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-534">Az.RedisCache</span></span>
* <span data-ttu-id="d4bdb-535">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-536">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-537">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-538">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-539">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d4bdb-540">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d4bdb-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4bdb-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d4bdb-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d4bdb-542">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d4bdb-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4bdb-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4bdb-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4bdb-544">Az.StorageSync</span></span>
* <span data-ttu-id="d4bdb-545">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-546">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-547">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="d4bdb-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d4bdb-548">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-549">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-550">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d4bdb-551">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d4bdb-552">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-553">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-554">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d4bdb-555">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="d4bdb-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d4bdb-556">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-557">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-558">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d4bdb-559">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4bdb-560">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d4bdb-561">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d4bdb-562">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d4bdb-563">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d4bdb-564">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d4bdb-565">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d4bdb-566">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-567">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-568">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d4bdb-569">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="d4bdb-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4bdb-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4bdb-570">Az.HDInsight</span></span>
* <span data-ttu-id="d4bdb-571">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="d4bdb-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-572">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-573">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d4bdb-574">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d4bdb-575">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-575">New cmdlets are:</span></span>
    - <span data-ttu-id="d4bdb-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4bdb-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4bdb-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4bdb-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4bdb-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4bdb-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4bdb-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4bdb-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-580">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-581">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d4bdb-582">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d4bdb-583">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d4bdb-584">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d4bdb-585">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d4bdb-586">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d4bdb-587">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d4bdb-588">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d4bdb-589">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4bdb-590">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d4bdb-591">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4bdb-592">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d4bdb-593">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d4bdb-594">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="d4bdb-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d4bdb-595">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="d4bdb-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d4bdb-596">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d4bdb-597">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d4bdb-598">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d4bdb-599">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d4bdb-600">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-600">Overall improved help files</span></span>
* <span data-ttu-id="d4bdb-601">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-602">Az.Network</span></span>
* <span data-ttu-id="d4bdb-603">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="d4bdb-604">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="d4bdb-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d4bdb-605">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="d4bdb-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d4bdb-606">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d4bdb-607">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="d4bdb-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d4bdb-608">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="d4bdb-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d4bdb-609">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d4bdb-610">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d4bdb-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d4bdb-611">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d4bdb-612">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d4bdb-613">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d4bdb-614">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d4bdb-615">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-615">New cmdlets</span></span>
        - <span data-ttu-id="d4bdb-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d4bdb-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d4bdb-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d4bdb-618">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-619">New-VpnSite</span></span>
        - <span data-ttu-id="d4bdb-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-620">Update-VpnSite</span></span>
        - <span data-ttu-id="d4bdb-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-621">New-VpnConnection</span></span>
        - <span data-ttu-id="d4bdb-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-622">Update-VpnConnection</span></span>
* <span data-ttu-id="d4bdb-623">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-625">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d4bdb-626">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="d4bdb-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-627">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-628">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-630">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d4bdb-631">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d4bdb-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4bdb-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4bdb-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4bdb-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4bdb-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4bdb-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4bdb-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4bdb-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4bdb-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4bdb-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4bdb-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4bdb-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4bdb-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4bdb-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4bdb-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4bdb-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4bdb-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4bdb-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4bdb-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4bdb-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4bdb-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d4bdb-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d4bdb-645">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4bdb-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-646">Az.SignalR</span></span>
* <span data-ttu-id="d4bdb-647">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-648">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-649">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d4bdb-650">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d4bdb-651">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d4bdb-652">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d4bdb-653">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-654">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-655">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d4bdb-656">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="d4bdb-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d4bdb-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d4bdb-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d4bdb-659">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d4bdb-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d4bdb-661">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d4bdb-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4bdb-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4bdb-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4bdb-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-666">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-667">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="d4bdb-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d4bdb-668">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="d4bdb-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d4bdb-669">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d4bdb-670">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d4bdb-671">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-671">General</span></span>
* <span data-ttu-id="d4bdb-672">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-673">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-674">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4bdb-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4bdb-675">Az.Aks</span></span>
* <span data-ttu-id="d4bdb-676">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d4bdb-677">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="d4bdb-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-678">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-679">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="d4bdb-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d4bdb-680">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="d4bdb-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d4bdb-681">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d4bdb-682">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="d4bdb-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d4bdb-683">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4bdb-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-684">Az.Batch</span></span>
* <span data-ttu-id="d4bdb-685">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="d4bdb-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-686">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-687">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="d4bdb-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-688">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-689">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d4bdb-690">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d4bdb-691">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d4bdb-692">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d4bdb-693">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d4bdb-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d4bdb-694">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d4bdb-695">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="d4bdb-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d4bdb-696">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-697">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-698">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d4bdb-699">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="d4bdb-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d4bdb-700">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d4bdb-701">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="d4bdb-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-703">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-704">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-705">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d4bdb-706">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="d4bdb-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d4bdb-707">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d4bdb-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d4bdb-708">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="d4bdb-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d4bdb-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4bdb-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4bdb-710">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-711">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-712">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-713">Az.Network</span></span>
* <span data-ttu-id="d4bdb-714">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d4bdb-715">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d4bdb-716">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d4bdb-717">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="d4bdb-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d4bdb-718">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="d4bdb-719">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d4bdb-720">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d4bdb-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-722">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d4bdb-723">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-723">Added example</span></span>
    - <span data-ttu-id="d4bdb-724">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d4bdb-725">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d4bdb-726">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-728">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-729">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-730">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d4bdb-731">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="d4bdb-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d4bdb-732">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d4bdb-733">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-734">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-735">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d4bdb-736">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="d4bdb-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d4bdb-737">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="d4bdb-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-739">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d4bdb-740">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d4bdb-741">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d4bdb-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d4bdb-742">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d4bdb-743">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d4bdb-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d4bdb-744">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d4bdb-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-745">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-746">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-747">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-748">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4bdb-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d4bdb-749">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="d4bdb-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d4bdb-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d4bdb-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d4bdb-752">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="d4bdb-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d4bdb-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-754">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-755">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4bdb-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d4bdb-756">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-757">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-758">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d4bdb-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d4bdb-760">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-761">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-762">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-764">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-765">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-766">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4bdb-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4bdb-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4bdb-768">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d4bdb-769">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d4bdb-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-770">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-771">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d4bdb-772">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="d4bdb-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-773">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-774">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d4bdb-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4bdb-775">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d4bdb-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-776">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-777">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4bdb-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-778">Az.LogicApp</span></span>
* <span data-ttu-id="d4bdb-779">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="d4bdb-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d4bdb-780">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d4bdb-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-781">Az.ManagedServices</span></span>
* <span data-ttu-id="d4bdb-782">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-783">Az.Network</span></span>
* <span data-ttu-id="d4bdb-784">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d4bdb-785">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-785">New cmdlets</span></span>
        - <span data-ttu-id="d4bdb-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4bdb-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4bdb-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4bdb-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d4bdb-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d4bdb-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d4bdb-794">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="d4bdb-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d4bdb-795">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d4bdb-796">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d4bdb-797">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d4bdb-798">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d4bdb-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d4bdb-799">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d4bdb-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d4bdb-800">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-800">Updated cmdlets</span></span>
        - <span data-ttu-id="d4bdb-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4bdb-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4bdb-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4bdb-804">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4bdb-805">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d4bdb-806">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4bdb-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4bdb-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d4bdb-810">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d4bdb-811">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d4bdb-812">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-814">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="d4bdb-815">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="d4bdb-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-817">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4bdb-818">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d4bdb-819">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d4bdb-820">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4bdb-821">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d4bdb-822">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4bdb-823">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d4bdb-824">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4bdb-825">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d4bdb-826">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-827">Az.Resources</span></span>
- <span data-ttu-id="d4bdb-828">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d4bdb-829">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d4bdb-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-830">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-831">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d4bdb-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4bdb-832">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d4bdb-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-833">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-834">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d4bdb-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d4bdb-835">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="d4bdb-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d4bdb-836">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-837">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-838">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="d4bdb-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4bdb-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4bdb-839">Az.StorageSync</span></span>
* <span data-ttu-id="d4bdb-840">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d4bdb-841">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d4bdb-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-842">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-843">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d4bdb-844">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d4bdb-845">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d4bdb-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d4bdb-846">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-847">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-848">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="d4bdb-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d4bdb-849">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d4bdb-850">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4bdb-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4bdb-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-851">Az.Advisor</span></span>
* <span data-ttu-id="d4bdb-852">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d4bdb-853">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-854">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-855">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d4bdb-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d4bdb-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d4bdb-857">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="d4bdb-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d4bdb-858">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d4bdb-859">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d4bdb-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d4bdb-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d4bdb-861">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="d4bdb-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-862">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-863">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-864">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-865">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-866">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-867">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4bdb-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4bdb-868">Az.EventGrid</span></span>
* <span data-ttu-id="d4bdb-869">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-870">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-871">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-872">Az.Network</span></span>
* <span data-ttu-id="d4bdb-873">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="d4bdb-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d4bdb-874">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4bdb-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4bdb-876">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d4bdb-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d4bdb-877">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d4bdb-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-879">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-881">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-882">Az.Resources</span></span>
    - <span data-ttu-id="d4bdb-883">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="d4bdb-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d4bdb-884">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="d4bdb-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d4bdb-885">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d4bdb-886">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-887">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-888">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-889">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-890">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="d4bdb-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d4bdb-891">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d4bdb-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4bdb-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4bdb-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4bdb-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4bdb-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4bdb-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d4bdb-898">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="d4bdb-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-899">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-900">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d4bdb-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d4bdb-902">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d4bdb-903">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="d4bdb-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d4bdb-904">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d4bdb-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4bdb-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4bdb-907">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d4bdb-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4bdb-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d4bdb-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4bdb-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4bdb-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4bdb-910">Az.StorageSync</span></span>
* <span data-ttu-id="d4bdb-911">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d4bdb-912">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-913">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-914">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="d4bdb-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d4bdb-915">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d4bdb-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d4bdb-916">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="d4bdb-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d4bdb-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d4bdb-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d4bdb-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d4bdb-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-919">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-920">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d4bdb-921">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4bdb-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4bdb-922">Az.Dns</span></span>
* <span data-ttu-id="d4bdb-923">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4bdb-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4bdb-924">Az.EventGrid</span></span>
* <span data-ttu-id="d4bdb-925">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d4bdb-926">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-926">New cmdlets:</span></span>
    - <span data-ttu-id="d4bdb-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4bdb-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4bdb-928">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4bdb-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4bdb-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4bdb-930">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d4bdb-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4bdb-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4bdb-932">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4bdb-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4bdb-934">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4bdb-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4bdb-936">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d4bdb-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4bdb-938">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d4bdb-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d4bdb-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d4bdb-940">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="d4bdb-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4bdb-942">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d4bdb-943">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="d4bdb-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d4bdb-945">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4bdb-946">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4bdb-947">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d4bdb-948">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d4bdb-949">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="d4bdb-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d4bdb-950">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d4bdb-951">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d4bdb-952">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="d4bdb-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="d4bdb-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d4bdb-954">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d4bdb-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d4bdb-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d4bdb-956">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d4bdb-957">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-958">Az.FrontDoor</span></span>
* <span data-ttu-id="d4bdb-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d4bdb-960">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d4bdb-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d4bdb-962">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="d4bdb-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-963">Az.Network</span></span>
* <span data-ttu-id="d4bdb-964">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d4bdb-965">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-965">New cmdlets</span></span>
        - <span data-ttu-id="d4bdb-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d4bdb-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d4bdb-967">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d4bdb-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d4bdb-968">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-968">New cmdlets</span></span> 
        - <span data-ttu-id="d4bdb-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d4bdb-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d4bdb-970">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d4bdb-971">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-971">New cmdlets</span></span> 
        - <span data-ttu-id="d4bdb-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="d4bdb-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4bdb-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4bdb-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d4bdb-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4bdb-977">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d4bdb-978">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-978">New cmdlets</span></span>
        - <span data-ttu-id="d4bdb-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4bdb-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4bdb-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bdb-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4bdb-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d4bdb-983">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d4bdb-984">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d4bdb-985">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d4bdb-986">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d4bdb-987">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d4bdb-988">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d4bdb-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d4bdb-989">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d4bdb-990">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d4bdb-991">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d4bdb-992">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d4bdb-993">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d4bdb-994">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d4bdb-995">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d4bdb-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d4bdb-996">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d4bdb-997">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-998">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="d4bdb-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d4bdb-999">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d4bdb-1000">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d4bdb-1001">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="d4bdb-1002">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="d4bdb-1003">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4bdb-1004">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4bdb-1005">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-1007">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1008">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1009">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d4bdb-1010">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4bdb-1011">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4bdb-1012">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-1014">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1015">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1016">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d4bdb-1017">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d4bdb-1018">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d4bdb-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4bdb-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4bdb-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4bdb-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d4bdb-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1024">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1025">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d4bdb-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4bdb-1027">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d4bdb-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1029">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1030">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d4bdb-1031">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d4bdb-1032">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d4bdb-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1033">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-1034">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1035">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1036">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d4bdb-1037">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1038">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-1039">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d4bdb-1040">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1041">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1042">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d4bdb-1043">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4bdb-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4bdb-1045">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1047">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-1049">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-1051">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d4bdb-1052">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1053">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1054">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d4bdb-1055">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4bdb-1056">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d4bdb-1057">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1058">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1059">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d4bdb-1060">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-1062">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d4bdb-1063">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d4bdb-1064">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d4bdb-1065">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d4bdb-1066">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d4bdb-1067">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d4bdb-1068">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d4bdb-1069">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d4bdb-1070">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d4bdb-1071">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d4bdb-1072">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d4bdb-1073">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d4bdb-1074">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d4bdb-1075">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d4bdb-1076">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d4bdb-1077">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d4bdb-1078">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d4bdb-1079">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d4bdb-1080">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d4bdb-1081">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d4bdb-1082">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d4bdb-1083">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d4bdb-1084">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d4bdb-1085">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d4bdb-1086">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4bdb-1087">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4bdb-1088">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d4bdb-1089">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d4bdb-1090">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d4bdb-1091">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d4bdb-1092">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d4bdb-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d4bdb-1094">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d4bdb-1095">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4bdb-1096">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d4bdb-1097">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d4bdb-1098">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d4bdb-1099">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d4bdb-1100">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d4bdb-1101">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d4bdb-1102">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4bdb-1103">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d4bdb-1104">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d4bdb-1105">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d4bdb-1106">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4bdb-1107">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4bdb-1108">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d4bdb-1109">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d4bdb-1110">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d4bdb-1111">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d4bdb-1112">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d4bdb-1113">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d4bdb-1114">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d4bdb-1115">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d4bdb-1116">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d4bdb-1117">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d4bdb-1118">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4bdb-1119">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4bdb-1120">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4bdb-1121">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4bdb-1122">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4bdb-1123">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4bdb-1124">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4bdb-1125">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4bdb-1126">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d4bdb-1127">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d4bdb-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d4bdb-1129">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d4bdb-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d4bdb-1131">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d4bdb-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d4bdb-1133">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d4bdb-1134">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d4bdb-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d4bdb-1136">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d4bdb-1137">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d4bdb-1138">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1139">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1140">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d4bdb-1141">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d4bdb-1142">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d4bdb-1143">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d4bdb-1144">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d4bdb-1145">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d4bdb-1146">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1147">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1148">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d4bdb-1149">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1151">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1152">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-1153">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1154">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1155">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d4bdb-1156">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4bdb-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d4bdb-1158">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1159">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1160">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1161">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1162">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d4bdb-1163">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1164">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1165">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-1167">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d4bdb-1168">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1169">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1170">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d4bdb-1171">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d4bdb-1172">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d4bdb-1173">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d4bdb-1174">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d4bdb-1175">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d4bdb-1176">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1176">Breaking changes</span></span>
    - <span data-ttu-id="d4bdb-1177">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d4bdb-1178">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d4bdb-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="d4bdb-1180">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4bdb-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1181">Az.Dns</span></span>
* <span data-ttu-id="d4bdb-1182">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d4bdb-1183">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d4bdb-1184">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="d4bdb-1186">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d4bdb-1187">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d4bdb-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1188">Az.HDInsight</span></span>
* <span data-ttu-id="d4bdb-1189">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d4bdb-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d4bdb-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4bdb-1192">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4bdb-1193">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d4bdb-1194">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d4bdb-1195">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1196">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-1197">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d4bdb-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d4bdb-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d4bdb-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d4bdb-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d4bdb-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d4bdb-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d4bdb-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4bdb-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4bdb-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4bdb-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4bdb-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4bdb-1209">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d4bdb-1210">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1211">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1212">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d4bdb-1213">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1213">New cmdlets</span></span>
        - <span data-ttu-id="d4bdb-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="d4bdb-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d4bdb-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d4bdb-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d4bdb-1218">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="d4bdb-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d4bdb-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d4bdb-1221">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d4bdb-1222">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d4bdb-1223">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4bdb-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4bdb-1225">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d4bdb-1226">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d4bdb-1227">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1229">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d4bdb-1230">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d4bdb-1231">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d4bdb-1232">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d4bdb-1233">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d4bdb-1234">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d4bdb-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1235">Az.Relay</span></span>
* <span data-ttu-id="d4bdb-1236">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-1238">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1239">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1240">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d4bdb-1241">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d4bdb-1242">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d4bdb-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4bdb-1244">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d4bdb-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d4bdb-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d4bdb-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1248">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1249">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d4bdb-1250">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d4bdb-1251">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4bdb-1252">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="d4bdb-1253">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="d4bdb-1254">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4bdb-1255">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4bdb-1256">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4bdb-1257">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4bdb-1258">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1259">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1260">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1261">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4bdb-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1262">Az.Batch</span></span>
* <span data-ttu-id="d4bdb-1263">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1264">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-1265">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-1267">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1268">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1269">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d4bdb-1270">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1271">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1272">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-1273">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1275">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4bdb-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1276">Az.EventGrid</span></span>
* <span data-ttu-id="d4bdb-1277">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1278">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-1279">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d4bdb-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1280">Az.HDInsight</span></span>
* <span data-ttu-id="d4bdb-1281">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1282">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-1283">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1284">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-1285">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1286">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d4bdb-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="d4bdb-1288">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d4bdb-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1289">Az.Media</span></span>
* <span data-ttu-id="d4bdb-1290">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1291">Az.Monitor</span></span>
  * <span data-ttu-id="d4bdb-1292">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d4bdb-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d4bdb-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d4bdb-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4bdb-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4bdb-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d4bdb-1298">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1299">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1300">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1301">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d4bdb-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="d4bdb-1303">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-1305">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d4bdb-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d4bdb-1307">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1309">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1310">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d4bdb-1311">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d4bdb-1312">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4bdb-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1313">Az.RedisCache</span></span>
* <span data-ttu-id="d4bdb-1314">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1315">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1316">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1317">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1318">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d4bdb-1319">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1320">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d4bdb-1321">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d4bdb-1322">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d4bdb-1323">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d4bdb-1324">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1325">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1326">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d4bdb-1327">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4bdb-1328">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d4bdb-1329">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d4bdb-1330">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4bdb-1331">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="d4bdb-1332">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="d4bdb-1333">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4bdb-1334">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4bdb-1335">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4bdb-1336">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4bdb-1337">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1338">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1339">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1340">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4bdb-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4bdb-1342">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d4bdb-1343">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1344">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1345">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d4bdb-1346">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d4bdb-1347">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1348">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1349">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4bdb-1350">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d4bdb-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4bdb-1352">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1353">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-1354">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d4bdb-1355">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1356">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1357">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d4bdb-1358">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d4bdb-1359">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d4bdb-1360">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d4bdb-1361">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d4bdb-1362">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1363">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1364">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1365">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1366">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d4bdb-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="d4bdb-1368">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d4bdb-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4bdb-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4bdb-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d4bdb-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d4bdb-1373">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d4bdb-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4bdb-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4bdb-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d4bdb-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d4bdb-1378">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4bdb-1379">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="d4bdb-1380">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="d4bdb-1381">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4bdb-1382">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4bdb-1383">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4bdb-1384">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4bdb-1385">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1386">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1387">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1388">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d4bdb-1389">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="d4bdb-1390">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1390">Pre-Post script</span></span>
    * <span data-ttu-id="d4bdb-1391">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1392">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1393">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d4bdb-1394">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1395">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-1396">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1397">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1398">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d4bdb-1399">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1401">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d4bdb-1402">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1403">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1404">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d4bdb-1405">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1406">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1407">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1408">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1409">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d4bdb-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4bdb-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4bdb-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4bdb-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d4bdb-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d4bdb-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1416">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1417">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d4bdb-1418">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1419">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1420">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d4bdb-1421">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1422">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1423">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4bdb-1424">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d4bdb-1425">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1426">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-1427">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1428">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1429">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1430">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-1431">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4bdb-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1432">Az.LogicApp</span></span>
* <span data-ttu-id="d4bdb-1433">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1434">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1435">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1437">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d4bdb-1438">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1438">SDK Update</span></span>
* <span data-ttu-id="d4bdb-1439">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d4bdb-1440">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1441">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1442">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d4bdb-1443">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d4bdb-1444">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d4bdb-1445">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d4bdb-1446">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d4bdb-1447">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1448">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1449">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d4bdb-1450">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1451">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1452">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d4bdb-1453">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d4bdb-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4bdb-1455">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1456">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1457">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d4bdb-1458">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d4bdb-1459">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-1461">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1462">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1463">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d4bdb-1464">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d4bdb-1465">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d4bdb-1466">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1468">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4bdb-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1469">Az.EventHub</span></span>
* <span data-ttu-id="d4bdb-1470">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1471">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-1472">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4bdb-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1473">Az.LogicApp</span></span>
* <span data-ttu-id="d4bdb-1474">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d4bdb-1475">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d4bdb-1476">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d4bdb-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4bdb-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4bdb-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4bdb-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d4bdb-1481">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d4bdb-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4bdb-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4bdb-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4bdb-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d4bdb-1486">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4bdb-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1487">Az.Monitor</span></span>
* <span data-ttu-id="d4bdb-1488">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1489">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1490">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4bdb-1492">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d4bdb-1493">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d4bdb-1494">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1495">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1496">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4bdb-1497">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d4bdb-1498">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d4bdb-1499">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1500">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1501">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d4bdb-1502">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1503">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1504">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d4bdb-1505">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1506">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1507">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4bdb-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="d4bdb-1509">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1510">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1511">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d4bdb-1512">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d4bdb-1513">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="d4bdb-1515">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1516">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1517">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d4bdb-1518">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4bdb-1519">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d4bdb-1520">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1521">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1522">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d4bdb-1523">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d4bdb-1524">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d4bdb-1525">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1526">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1527">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4bdb-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4bdb-1529">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4bdb-1531">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d4bdb-1532">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1533">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1534">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4bdb-1535">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4bdb-1536">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4bdb-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1537">Az.Aks</span></span>
* <span data-ttu-id="d4bdb-1538">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4bdb-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1539">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1540">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d4bdb-1541">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4bdb-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1542">Az.Cdn</span></span>
* <span data-ttu-id="d4bdb-1543">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1544">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1545">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d4bdb-1546">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d4bdb-1547">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4bdb-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4bdb-1549">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4bdb-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1550">Az.DataFactory</span></span>
* <span data-ttu-id="d4bdb-1551">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1553">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d4bdb-1554">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d4bdb-1555">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1556">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-1557">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1558">Az.KeyVault</span></span>
* <span data-ttu-id="d4bdb-1559">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1560">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1561">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1562">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1563">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d4bdb-1564">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d4bdb-1565">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d4bdb-1566">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d4bdb-1567">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d4bdb-1568">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d4bdb-1569">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-1571">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d4bdb-1572">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1572">Fix some error messages.</span></span>
* <span data-ttu-id="d4bdb-1573">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d4bdb-1574">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4bdb-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1575">Az.SignalR</span></span>
* <span data-ttu-id="d4bdb-1576">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1577">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1578">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4bdb-1579">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d4bdb-1580">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d4bdb-1581">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1582">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1583">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4bdb-1584">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d4bdb-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d4bdb-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d4bdb-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="d4bdb-1588">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1589">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1590">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4bdb-1591">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d4bdb-1592">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d4bdb-1593">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1594">Az.Accounts</span></span>
* <span data-ttu-id="d4bdb-1595">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1596">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1597">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d4bdb-1598">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d4bdb-1599">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1601">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d4bdb-1602">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4bdb-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1603">Az.EventGrid</span></span>
* <span data-ttu-id="d4bdb-1604">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d4bdb-1605">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d4bdb-1606">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4bdb-1607">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4bdb-1608">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4bdb-1609">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d4bdb-1610">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4bdb-1611">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4bdb-1612">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4bdb-1613">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="d4bdb-1614">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d4bdb-1615">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4bdb-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1616">Az.IotHub</span></span>
* <span data-ttu-id="d4bdb-1617">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4bdb-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1618">Az.LogicApp</span></span>
* <span data-ttu-id="d4bdb-1619">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1620">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1621">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d4bdb-1622">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d4bdb-1623">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4bdb-1624">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d4bdb-1625">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d4bdb-1626">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4bdb-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1627">Az.SignalR</span></span>
* <span data-ttu-id="d4bdb-1628">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1629">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1630">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4bdb-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1631">Az.Storage</span></span>
* <span data-ttu-id="d4bdb-1632">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d4bdb-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="d4bdb-1634">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d4bdb-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1636">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1637">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d4bdb-1638">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d4bdb-1639">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d4bdb-1640">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1640">General</span></span>

- <span data-ttu-id="d4bdb-1641">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="d4bdb-1642">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1642">Online help for each module</span></span>
- <span data-ttu-id="d4bdb-1643">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d4bdb-1644">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d4bdb-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1645">Az.Accounts</span></span>
- <span data-ttu-id="d4bdb-1646">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="d4bdb-1647">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="d4bdb-1649">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1649">Fixes for #7002</span></span>
- <span data-ttu-id="d4bdb-1650">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d4bdb-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1651">Az.Batch</span></span>
- <span data-ttu-id="d4bdb-1652">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d4bdb-1653">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d4bdb-1654">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d4bdb-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1655">Az.Billing</span></span>
- <span data-ttu-id="d4bdb-1656">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d4bdb-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="d4bdb-1658">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d4bdb-1659">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4bdb-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="d4bdb-1661">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d4bdb-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d4bdb-1663">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="d4bdb-1665">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d4bdb-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1666">Az.Monitor</span></span>
- <span data-ttu-id="d4bdb-1667">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d4bdb-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1668">Az.KeyVault</span></span>
- <span data-ttu-id="d4bdb-1669">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d4bdb-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="d4bdb-1671">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d4bdb-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1672">Az.Media</span></span>
- <span data-ttu-id="d4bdb-1673">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1674">Az.Network</span></span>
<span data-ttu-id="d4bdb-1675">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d4bdb-1676">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="d4bdb-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d4bdb-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d4bdb-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d4bdb-1685">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d4bdb-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d4bdb-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4bdb-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4bdb-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d4bdb-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d4bdb-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d4bdb-1692">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d4bdb-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4bdb-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4bdb-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d4bdb-1696">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d4bdb-1697">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d4bdb-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="d4bdb-1699">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d4bdb-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1700">Az.Profile</span></span>
- <span data-ttu-id="d4bdb-1701">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="d4bdb-1703">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d4bdb-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1704">Az.Resources</span></span>
- <span data-ttu-id="d4bdb-1705">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="d4bdb-1707">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d4bdb-1708">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d4bdb-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="d4bdb-1710">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d4bdb-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1711">Az.Sql</span></span>
- <span data-ttu-id="d4bdb-1712">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d4bdb-1713">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d4bdb-1714">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4bdb-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1715">Az.Storage</span></span>
- <span data-ttu-id="d4bdb-1716">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1717">Az.Websites</span></span>
- <span data-ttu-id="d4bdb-1718">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d4bdb-1719">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d4bdb-1720">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1720">General</span></span>

* <span data-ttu-id="d4bdb-1721">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4bdb-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1722">Az.Compute</span></span>

* <span data-ttu-id="d4bdb-1723">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="d4bdb-1725">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d4bdb-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="d4bdb-1727">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="d4bdb-1728">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d4bdb-1729">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4bdb-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="d4bdb-1731">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d4bdb-1732">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4bdb-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1733">Az.Resources</span></span>

* <span data-ttu-id="d4bdb-1734">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d4bdb-1735">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d4bdb-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1736">Az.Sql</span></span>

* <span data-ttu-id="d4bdb-1737">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d4bdb-1738">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d4bdb-1739">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4bdb-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1740">Az.Storage</span></span>

* <span data-ttu-id="d4bdb-1741">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d4bdb-1742">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d4bdb-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4bdb-1744">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="d4bdb-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d4bdb-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1747">Az.Websites</span></span>

* <span data-ttu-id="d4bdb-1748">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d4bdb-1749">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d4bdb-1750">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d4bdb-1751">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4bdb-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="d4bdb-1753">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d4bdb-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1754">Az.Automation</span></span>
* <span data-ttu-id="d4bdb-1755">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4bdb-1756">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d4bdb-1757">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d4bdb-1758">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d4bdb-1759">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4bdb-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1760">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1761">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d4bdb-1762">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4bdb-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4bdb-1764">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d4bdb-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4bdb-1766">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1767">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1768">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d4bdb-1769">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d4bdb-1770">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d4bdb-1771">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d4bdb-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d4bdb-1773">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d4bdb-1774">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d4bdb-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d4bdb-1776">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d4bdb-1777">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d4bdb-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1778">Az.Relay</span></span>
* <span data-ttu-id="d4bdb-1779">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4bdb-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1780">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1781">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d4bdb-1782">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d4bdb-1783">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-1785">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d4bdb-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1786">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1787">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d4bdb-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4bdb-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4bdb-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4bdb-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4bdb-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4bdb-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4bdb-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4bdb-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d4bdb-1796">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d4bdb-1797">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d4bdb-1798">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d4bdb-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4bdb-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4bdb-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d4bdb-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d4bdb-1803">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d4bdb-1804">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d4bdb-1805">Geral</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1805">General</span></span>
* <span data-ttu-id="d4bdb-1806">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d4bdb-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1807">Az.Profile</span></span>
* <span data-ttu-id="d4bdb-1808">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d4bdb-1809">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d4bdb-1810">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d4bdb-1811">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d4bdb-1812">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d4bdb-1813">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d4bdb-1814">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-1816">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1817">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1818">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d4bdb-1819">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d4bdb-1820">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1822">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d4bdb-1823">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d4bdb-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1824">Az.Insights</span></span>
* <span data-ttu-id="d4bdb-1825">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d4bdb-1826">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d4bdb-1827">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d4bdb-1828">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1829">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1830">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d4bdb-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d4bdb-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d4bdb-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d4bdb-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d4bdb-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d4bdb-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4bdb-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4bdb-1838">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1839">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1840">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d4bdb-1841">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4bdb-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="d4bdb-1843">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4bdb-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4bdb-1845">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d4bdb-1846">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d4bdb-1847">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d4bdb-1848">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d4bdb-1849">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d4bdb-1850">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d4bdb-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1851">Az.Profile</span></span>
* <span data-ttu-id="d4bdb-1852">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d4bdb-1853">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1854">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1855">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d4bdb-1856">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4bdb-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4bdb-1858">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d4bdb-1859">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d4bdb-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4bdb-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4bdb-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1863">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1864">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d4bdb-1865">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1866">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1867">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d4bdb-1868">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d4bdb-1869">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d4bdb-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1870">Azure.Storage</span></span>
* <span data-ttu-id="d4bdb-1871">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d4bdb-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d4bdb-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4bdb-1874">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d4bdb-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d4bdb-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4bdb-1877">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4bdb-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1878">Az.Compute</span></span>
* <span data-ttu-id="d4bdb-1879">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d4bdb-1880">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d4bdb-1881">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d4bdb-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d4bdb-1883">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4bdb-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1884">Az.Network</span></span>
* <span data-ttu-id="d4bdb-1885">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d4bdb-1886">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1886">new cmdlets added</span></span>
    - <span data-ttu-id="d4bdb-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4bdb-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4bdb-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4bdb-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4bdb-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d4bdb-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d4bdb-1893">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d4bdb-1894">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d4bdb-1895">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4bdb-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1896">Az.RedisCache</span></span>
* <span data-ttu-id="d4bdb-1897">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d4bdb-1898">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4bdb-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1899">Az.Resources</span></span>
* <span data-ttu-id="d4bdb-1900">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4bdb-1901">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4bdb-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1902">Az.Sql</span></span>
* <span data-ttu-id="d4bdb-1903">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4bdb-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1904">Az.Websites</span></span>
* <span data-ttu-id="d4bdb-1905">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d4bdb-1906">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d4bdb-1907">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d4bdb-1908">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="d4bdb-1908">Initial Release</span></span>
