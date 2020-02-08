---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002666"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6ec2a-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ec2a-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6ec2a-104">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="6ec2a-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6ec2a-105">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6ec2a-105">Highlights since the last major release</span></span>
* <span data-ttu-id="6ec2a-106">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6ec2a-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6ec2a-107">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-108">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-109">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="6ec2a-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6ec2a-110">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="6ec2a-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-111">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-112">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6ec2a-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6ec2a-113">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="6ec2a-114">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="6ec2a-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6ec2a-115">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-116">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-117">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6ec2a-118">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6ec2a-119">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6ec2a-121">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-122">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-123">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6ec2a-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6ec2a-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="6ec2a-125">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6ec2a-126">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="6ec2a-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-127">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-128">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-129">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-130">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-131">Az.Network</span></span>
* <span data-ttu-id="6ec2a-132">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6ec2a-133">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6ec2a-134">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-135">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="6ec2a-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6ec2a-136">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6ec2a-137">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6ec2a-138">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6ec2a-139">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6ec2a-140">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-140">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6ec2a-142">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6ec2a-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6ec2a-144">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6ec2a-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="6ec2a-146">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="6ec2a-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6ec2a-147">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6ec2a-148">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="6ec2a-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6ec2a-149">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="6ec2a-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-151">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6ec2a-152">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-153">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-154">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="6ec2a-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6ec2a-155">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="6ec2a-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-156">Az.Sql</span></span>
<span data-ttu-id="6ec2a-157">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-158">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-159">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6ec2a-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="6ec2a-161">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6ec2a-162">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-163">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-164">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="6ec2a-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6ec2a-165">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="6ec2a-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6ec2a-166">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="6ec2a-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-167">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-168">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6ec2a-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-169">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-170">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-171">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-172">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6ec2a-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="6ec2a-174">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6ec2a-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6ec2a-176">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6ec2a-177">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6ec2a-178">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6ec2a-179">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6ec2a-180">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6ec2a-181">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6ec2a-182">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6ec2a-183">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6ec2a-184">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6ec2a-185">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6ec2a-186">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6ec2a-187">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6ec2a-188">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6ec2a-189">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6ec2a-190">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6ec2a-191">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6ec2a-192">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6ec2a-193">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-194">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-195">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6ec2a-196">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6ec2a-197">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6ec2a-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6ec2a-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="6ec2a-199">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="6ec2a-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-200">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-201">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="6ec2a-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-202">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-203">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6ec2a-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6ec2a-204">Az.MachineLearning</span></span>
* <span data-ttu-id="6ec2a-205">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="6ec2a-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6ec2a-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6ec2a-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6ec2a-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6ec2a-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6ec2a-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6ec2a-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6ec2a-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6ec2a-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6ec2a-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6ec2a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6ec2a-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6ec2a-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-213">Az.Network</span></span>
* <span data-ttu-id="6ec2a-214">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="6ec2a-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-216">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6ec2a-217">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6ec2a-218">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6ec2a-219">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-220">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-221">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-222">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-223">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6ec2a-224">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="6ec2a-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6ec2a-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6ec2a-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6ec2a-226">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="6ec2a-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-227">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-228">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="6ec2a-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6ec2a-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6ec2a-230">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="6ec2a-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="6ec2a-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6ec2a-232">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6ec2a-233">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-233">General</span></span>
* <span data-ttu-id="6ec2a-234">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-235">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-236">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="6ec2a-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6ec2a-237">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="6ec2a-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6ec2a-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-238">Az.Batch</span></span>
* <span data-ttu-id="6ec2a-239">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-240">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-241">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-242">Az.FrontDoor</span></span>
* <span data-ttu-id="6ec2a-243">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="6ec2a-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6ec2a-244">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="6ec2a-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6ec2a-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6ec2a-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="6ec2a-246">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="6ec2a-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-247">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-248">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="6ec2a-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6ec2a-249">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="6ec2a-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6ec2a-250">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-251">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-252">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6ec2a-253">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="6ec2a-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6ec2a-254">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-255">Az.Network</span></span>
* <span data-ttu-id="6ec2a-256">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-257">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-258">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6ec2a-259">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-260">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-261">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-262">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-263">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="6ec2a-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6ec2a-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6ec2a-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6ec2a-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6ec2a-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6ec2a-266">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6ec2a-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6ec2a-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6ec2a-268">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6ec2a-269">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="6ec2a-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6ec2a-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6ec2a-272">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6ec2a-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6ec2a-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6ec2a-274">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6ec2a-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6ec2a-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6ec2a-276">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6ec2a-277">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6ec2a-277">Highlights since the last major release</span></span>
* <span data-ttu-id="6ec2a-278">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6ec2a-279">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-280">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-281">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-281">VM Reapply feature</span></span>
    - <span data-ttu-id="6ec2a-282">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6ec2a-283">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6ec2a-284">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6ec2a-285">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6ec2a-286">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6ec2a-287">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6ec2a-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6ec2a-288">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="6ec2a-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6ec2a-289">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6ec2a-290">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6ec2a-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6ec2a-291">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6ec2a-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6ec2a-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6ec2a-293">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6ec2a-294">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-294">Get the Order</span></span>
* <span data-ttu-id="6ec2a-295">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6ec2a-296">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-296">Create new Order</span></span>
* <span data-ttu-id="6ec2a-297">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6ec2a-298">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-298">Remove the Order</span></span>
* <span data-ttu-id="6ec2a-299">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6ec2a-300">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="6ec2a-300">Now creates Local Share</span></span>
* <span data-ttu-id="6ec2a-301">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6ec2a-302">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="6ec2a-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6ec2a-303">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6ec2a-304">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6ec2a-305">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6ec2a-306">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="6ec2a-307">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6ec2a-308">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-308">Create new Triggers</span></span>
* <span data-ttu-id="6ec2a-309">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6ec2a-310">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-311">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-312">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6ec2a-313">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-315">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-316">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-317">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-318">Az.FrontDoor</span></span>
* <span data-ttu-id="6ec2a-319">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6ec2a-320">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6ec2a-321">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="6ec2a-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6ec2a-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-323">Az.Network</span></span>
* <span data-ttu-id="6ec2a-324">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6ec2a-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6ec2a-325">Az.PrivateDns</span></span>
* <span data-ttu-id="6ec2a-326">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-328">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6ec2a-329">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6ec2a-330">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6ec2a-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-331">Az.RedisCache</span></span>
* <span data-ttu-id="6ec2a-332">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6ec2a-333">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6ec2a-334">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-335">Az.Resources</span></span>
- <span data-ttu-id="6ec2a-336">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6ec2a-337">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="6ec2a-338">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6ec2a-339">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6ec2a-340">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-341">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-342">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6ec2a-343">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="6ec2a-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6ec2a-344">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6ec2a-345">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-345">General</span></span>
* <span data-ttu-id="6ec2a-346">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-347">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-348">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6ec2a-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-349">Az.Advisor</span></span>
* <span data-ttu-id="6ec2a-350">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6ec2a-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-351">Az.Batch</span></span>
* <span data-ttu-id="6ec2a-352">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6ec2a-353">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6ec2a-354">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6ec2a-355">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6ec2a-356">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6ec2a-357">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6ec2a-358">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6ec2a-359">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6ec2a-360">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6ec2a-361">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6ec2a-362">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6ec2a-363">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6ec2a-364">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6ec2a-365">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6ec2a-366">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6ec2a-367">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6ec2a-368">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6ec2a-369">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6ec2a-370">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6ec2a-371">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="6ec2a-372">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6ec2a-373">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6ec2a-374">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6ec2a-375">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="6ec2a-376">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6ec2a-377">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="6ec2a-378">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6ec2a-379">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6ec2a-380">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6ec2a-381">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6ec2a-382">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6ec2a-383">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6ec2a-384">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6ec2a-385">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6ec2a-386">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6ec2a-387">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-388">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-389">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6ec2a-390">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-391">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-392">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="6ec2a-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6ec2a-393">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6ec2a-394">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="6ec2a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6ec2a-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6ec2a-396">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6ec2a-397">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6ec2a-398">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="6ec2a-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6ec2a-399">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6ec2a-400">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="6ec2a-400">Breaking changes</span></span>
    - <span data-ttu-id="6ec2a-401">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6ec2a-402">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-403">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-404">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-406">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="6ec2a-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6ec2a-407">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6ec2a-408">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="6ec2a-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6ec2a-409">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="6ec2a-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6ec2a-410">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6ec2a-411">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="6ec2a-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-412">Az.FrontDoor</span></span>
* <span data-ttu-id="6ec2a-413">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-414">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-415">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6ec2a-416">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6ec2a-417">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6ec2a-418">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6ec2a-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6ec2a-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6ec2a-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ec2a-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6ec2a-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ec2a-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6ec2a-424">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-425">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6ec2a-426">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6ec2a-427">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6ec2a-428">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6ec2a-429">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6ec2a-430">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6ec2a-431">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6ec2a-432">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6ec2a-433">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6ec2a-434">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6ec2a-435">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="6ec2a-436">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-437">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-438">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-438">Breaking changes:</span></span>
    - <span data-ttu-id="6ec2a-439">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6ec2a-440">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6ec2a-441">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6ec2a-442">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6ec2a-443">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6ec2a-444">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6ec2a-445">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6ec2a-446">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6ec2a-447">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6ec2a-448">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6ec2a-449">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6ec2a-450">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-452">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-453">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6ec2a-454">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6ec2a-455">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-456">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-457">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-458">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-459">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-460">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="6ec2a-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-461">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-462">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-463">Az.Network</span></span>
* <span data-ttu-id="6ec2a-464">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6ec2a-465">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6ec2a-471">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6ec2a-472">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-472">New cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6ec2a-474">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6ec2a-475">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6ec2a-476">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6ec2a-477">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6ec2a-478">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6ec2a-479">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6ec2a-480">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6ec2a-481">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-481">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6ec2a-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6ec2a-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6ec2a-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6ec2a-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6ec2a-487">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ec2a-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6ec2a-488">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6ec2a-489">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6ec2a-490">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6ec2a-491">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6ec2a-492">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6ec2a-493">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6ec2a-494">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-494">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6ec2a-496">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6ec2a-497">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6ec2a-498">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6ec2a-499">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6ec2a-500">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6ec2a-501">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6ec2a-502">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="6ec2a-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6ec2a-503">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-503">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6ec2a-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6ec2a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6ec2a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6ec2a-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6ec2a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6ec2a-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6ec2a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6ec2a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6ec2a-510">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6ec2a-511">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6ec2a-512">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6ec2a-513">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6ec2a-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6ec2a-514">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6ec2a-515">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6ec2a-516">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6ec2a-517">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6ec2a-518">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6ec2a-519">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6ec2a-520">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6ec2a-521">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-521">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="6ec2a-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6ec2a-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6ec2a-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-527">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-528">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-529">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6ec2a-530">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6ec2a-531">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6ec2a-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6ec2a-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6ec2a-534">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6ec2a-535">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6ec2a-536">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="6ec2a-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="6ec2a-537">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-538">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-539">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6ec2a-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6ec2a-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6ec2a-542">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="6ec2a-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6ec2a-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6ec2a-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6ec2a-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6ec2a-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="6ec2a-545">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6ec2a-546">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-546">General</span></span>
* <span data-ttu-id="6ec2a-547">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-548">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-549">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-550">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-551">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6ec2a-552">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="6ec2a-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-553">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-554">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="6ec2a-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-555">Az.Batch</span></span>
* <span data-ttu-id="6ec2a-556">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-557">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-558">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6ec2a-559">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6ec2a-560">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="6ec2a-561">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-562">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-563">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6ec2a-564">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6ec2a-565">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-567">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="6ec2a-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6ec2a-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6ec2a-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="6ec2a-569">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6ec2a-570">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6ec2a-571">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="6ec2a-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6ec2a-572">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-573">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-574">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6ec2a-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6ec2a-575">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ec2a-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-576">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-577">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6ec2a-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6ec2a-578">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6ec2a-579">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="6ec2a-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6ec2a-580">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-581">Az.Network</span></span>
* <span data-ttu-id="6ec2a-582">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6ec2a-583">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6ec2a-584">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-584">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6ec2a-586">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6ec2a-587">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="6ec2a-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6ec2a-588">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="6ec2a-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6ec2a-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6ec2a-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6ec2a-592">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="6ec2a-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6ec2a-593">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6ec2a-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6ec2a-594">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6ec2a-595">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6ec2a-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-596">Az.RedisCache</span></span>
* <span data-ttu-id="6ec2a-597">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-598">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-599">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-600">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-601">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6ec2a-602">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="6ec2a-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6ec2a-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6ec2a-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6ec2a-604">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="6ec2a-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6ec2a-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6ec2a-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6ec2a-606">Az.StorageSync</span></span>
* <span data-ttu-id="6ec2a-607">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-608">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-609">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="6ec2a-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6ec2a-610">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-611">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-612">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6ec2a-613">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6ec2a-614">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-615">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-616">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6ec2a-617">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="6ec2a-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6ec2a-618">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-619">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-620">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6ec2a-621">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6ec2a-622">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6ec2a-623">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6ec2a-624">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6ec2a-625">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6ec2a-626">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6ec2a-627">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6ec2a-628">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-629">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-630">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6ec2a-631">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="6ec2a-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-632">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-633">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="6ec2a-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-634">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-635">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6ec2a-636">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6ec2a-637">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-637">New cmdlets are:</span></span>
    - <span data-ttu-id="6ec2a-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6ec2a-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6ec2a-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6ec2a-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6ec2a-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6ec2a-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6ec2a-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6ec2a-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-642">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-643">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6ec2a-644">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6ec2a-645">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6ec2a-646">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6ec2a-647">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6ec2a-648">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6ec2a-649">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6ec2a-650">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6ec2a-651">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6ec2a-652">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6ec2a-653">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6ec2a-654">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6ec2a-655">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6ec2a-656">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="6ec2a-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6ec2a-657">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="6ec2a-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6ec2a-658">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6ec2a-659">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6ec2a-660">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6ec2a-661">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6ec2a-662">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-662">Overall improved help files</span></span>
* <span data-ttu-id="6ec2a-663">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-664">Az.Network</span></span>
* <span data-ttu-id="6ec2a-665">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="6ec2a-666">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="6ec2a-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6ec2a-667">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="6ec2a-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6ec2a-668">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6ec2a-669">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="6ec2a-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6ec2a-670">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="6ec2a-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6ec2a-671">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6ec2a-672">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6ec2a-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6ec2a-673">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6ec2a-674">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6ec2a-675">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6ec2a-676">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6ec2a-677">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-677">New cmdlets</span></span>
        - <span data-ttu-id="6ec2a-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6ec2a-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6ec2a-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6ec2a-680">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-681">New-VpnSite</span></span>
        - <span data-ttu-id="6ec2a-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-682">Update-VpnSite</span></span>
        - <span data-ttu-id="6ec2a-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-683">New-VpnConnection</span></span>
        - <span data-ttu-id="6ec2a-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-684">Update-VpnConnection</span></span>
* <span data-ttu-id="6ec2a-685">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-687">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6ec2a-688">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="6ec2a-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-689">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-690">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-692">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6ec2a-693">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6ec2a-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6ec2a-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6ec2a-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6ec2a-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6ec2a-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6ec2a-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6ec2a-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6ec2a-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6ec2a-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6ec2a-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6ec2a-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6ec2a-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6ec2a-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6ec2a-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6ec2a-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6ec2a-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6ec2a-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6ec2a-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6ec2a-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6ec2a-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6ec2a-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6ec2a-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6ec2a-707">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6ec2a-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-708">Az.SignalR</span></span>
* <span data-ttu-id="6ec2a-709">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-710">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-711">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6ec2a-712">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6ec2a-713">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6ec2a-714">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6ec2a-715">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-716">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-717">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6ec2a-718">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="6ec2a-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6ec2a-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6ec2a-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6ec2a-721">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6ec2a-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6ec2a-723">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6ec2a-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6ec2a-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6ec2a-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6ec2a-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-728">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-729">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="6ec2a-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6ec2a-730">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="6ec2a-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6ec2a-731">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6ec2a-732">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6ec2a-733">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-733">General</span></span>
* <span data-ttu-id="6ec2a-734">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-735">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-736">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6ec2a-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6ec2a-737">Az.Aks</span></span>
* <span data-ttu-id="6ec2a-738">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6ec2a-739">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="6ec2a-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-740">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-741">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="6ec2a-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6ec2a-742">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="6ec2a-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6ec2a-743">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6ec2a-744">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="6ec2a-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6ec2a-745">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6ec2a-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-746">Az.Batch</span></span>
* <span data-ttu-id="6ec2a-747">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="6ec2a-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-748">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-749">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="6ec2a-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-750">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-751">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6ec2a-752">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6ec2a-753">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6ec2a-754">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6ec2a-755">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6ec2a-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6ec2a-756">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6ec2a-757">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="6ec2a-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6ec2a-758">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-759">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-760">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6ec2a-761">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="6ec2a-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6ec2a-762">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6ec2a-763">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="6ec2a-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-765">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-766">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-767">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6ec2a-768">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="6ec2a-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6ec2a-769">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6ec2a-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6ec2a-770">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="6ec2a-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6ec2a-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6ec2a-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6ec2a-772">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-773">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-774">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-775">Az.Network</span></span>
* <span data-ttu-id="6ec2a-776">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6ec2a-777">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6ec2a-778">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6ec2a-779">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="6ec2a-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6ec2a-780">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="6ec2a-781">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6ec2a-782">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6ec2a-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-784">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6ec2a-785">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-785">Added example</span></span>
    - <span data-ttu-id="6ec2a-786">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6ec2a-787">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6ec2a-788">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-790">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-791">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-792">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6ec2a-793">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="6ec2a-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6ec2a-794">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6ec2a-795">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-796">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-797">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6ec2a-798">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="6ec2a-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6ec2a-799">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="6ec2a-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-801">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6ec2a-802">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6ec2a-803">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6ec2a-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6ec2a-804">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6ec2a-805">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6ec2a-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6ec2a-806">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6ec2a-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-807">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-808">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-809">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-810">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ec2a-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6ec2a-811">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="6ec2a-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6ec2a-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6ec2a-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6ec2a-814">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="6ec2a-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6ec2a-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-816">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-817">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6ec2a-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6ec2a-818">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-819">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-820">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6ec2a-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6ec2a-822">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-823">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-824">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-826">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-827">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-828">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6ec2a-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6ec2a-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6ec2a-830">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6ec2a-831">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="6ec2a-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-832">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-833">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6ec2a-834">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="6ec2a-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-835">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-836">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6ec2a-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6ec2a-837">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="6ec2a-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-838">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-839">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6ec2a-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-840">Az.LogicApp</span></span>
* <span data-ttu-id="6ec2a-841">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="6ec2a-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6ec2a-842">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6ec2a-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-843">Az.ManagedServices</span></span>
* <span data-ttu-id="6ec2a-844">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-845">Az.Network</span></span>
* <span data-ttu-id="6ec2a-846">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6ec2a-847">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-847">New cmdlets</span></span>
        - <span data-ttu-id="6ec2a-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6ec2a-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6ec2a-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6ec2a-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6ec2a-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6ec2a-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6ec2a-856">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="6ec2a-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6ec2a-857">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6ec2a-858">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6ec2a-859">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6ec2a-860">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="6ec2a-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6ec2a-861">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="6ec2a-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6ec2a-862">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-862">Updated cmdlets</span></span>
        - <span data-ttu-id="6ec2a-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6ec2a-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6ec2a-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6ec2a-866">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6ec2a-867">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6ec2a-868">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6ec2a-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6ec2a-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6ec2a-872">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6ec2a-873">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6ec2a-874">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-876">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6ec2a-877">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="6ec2a-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-879">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6ec2a-880">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6ec2a-881">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6ec2a-882">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6ec2a-883">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6ec2a-884">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6ec2a-885">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6ec2a-886">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6ec2a-887">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6ec2a-888">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-889">Az.Resources</span></span>
- <span data-ttu-id="6ec2a-890">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6ec2a-891">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6ec2a-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-892">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-893">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6ec2a-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6ec2a-894">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="6ec2a-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-895">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-896">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6ec2a-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6ec2a-897">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="6ec2a-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6ec2a-898">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-899">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-900">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="6ec2a-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6ec2a-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6ec2a-901">Az.StorageSync</span></span>
* <span data-ttu-id="6ec2a-902">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6ec2a-903">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="6ec2a-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-904">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-905">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6ec2a-906">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6ec2a-907">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="6ec2a-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6ec2a-908">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-909">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-910">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="6ec2a-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6ec2a-911">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6ec2a-912">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ec2a-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6ec2a-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-913">Az.Advisor</span></span>
* <span data-ttu-id="6ec2a-914">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6ec2a-915">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-916">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-917">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="6ec2a-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6ec2a-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6ec2a-919">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="6ec2a-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6ec2a-920">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6ec2a-921">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="6ec2a-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6ec2a-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6ec2a-923">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="6ec2a-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-924">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-925">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-926">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-927">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-928">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-929">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6ec2a-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ec2a-930">Az.EventGrid</span></span>
* <span data-ttu-id="6ec2a-931">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-932">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-933">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-934">Az.Network</span></span>
* <span data-ttu-id="6ec2a-935">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="6ec2a-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6ec2a-936">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6ec2a-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="6ec2a-938">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="6ec2a-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6ec2a-939">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="6ec2a-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-941">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-943">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-944">Az.Resources</span></span>
    - <span data-ttu-id="6ec2a-945">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="6ec2a-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6ec2a-946">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="6ec2a-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6ec2a-947">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6ec2a-948">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-949">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-950">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-951">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-952">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="6ec2a-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6ec2a-953">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6ec2a-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6ec2a-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6ec2a-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6ec2a-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6ec2a-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6ec2a-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6ec2a-960">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="6ec2a-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-961">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-962">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6ec2a-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6ec2a-964">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6ec2a-965">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="6ec2a-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6ec2a-966">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6ec2a-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6ec2a-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6ec2a-969">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6ec2a-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6ec2a-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6ec2a-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6ec2a-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6ec2a-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6ec2a-972">Az.StorageSync</span></span>
* <span data-ttu-id="6ec2a-973">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6ec2a-974">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-975">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-976">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="6ec2a-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6ec2a-977">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="6ec2a-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6ec2a-978">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="6ec2a-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6ec2a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6ec2a-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6ec2a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6ec2a-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-981">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-982">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6ec2a-983">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6ec2a-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6ec2a-984">Az.Dns</span></span>
* <span data-ttu-id="6ec2a-985">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6ec2a-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ec2a-986">Az.EventGrid</span></span>
* <span data-ttu-id="6ec2a-987">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6ec2a-988">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-988">New cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6ec2a-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6ec2a-990">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6ec2a-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6ec2a-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6ec2a-992">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6ec2a-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6ec2a-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6ec2a-994">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6ec2a-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6ec2a-996">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6ec2a-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6ec2a-998">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6ec2a-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6ec2a-1000">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6ec2a-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6ec2a-1002">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6ec2a-1003">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6ec2a-1004">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6ec2a-1005">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6ec2a-1007">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6ec2a-1008">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6ec2a-1009">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6ec2a-1010">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6ec2a-1011">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6ec2a-1012">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6ec2a-1013">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6ec2a-1014">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6ec2a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6ec2a-1016">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6ec2a-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6ec2a-1018">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6ec2a-1019">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="6ec2a-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6ec2a-1022">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6ec2a-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6ec2a-1024">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1025">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1026">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6ec2a-1027">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1027">New cmdlets</span></span>
        - <span data-ttu-id="6ec2a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6ec2a-1029">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6ec2a-1030">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1030">New cmdlets</span></span> 
        - <span data-ttu-id="6ec2a-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6ec2a-1032">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6ec2a-1033">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1033">New cmdlets</span></span> 
        - <span data-ttu-id="6ec2a-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6ec2a-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6ec2a-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6ec2a-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6ec2a-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6ec2a-1039">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6ec2a-1040">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1040">New cmdlets</span></span>
        - <span data-ttu-id="6ec2a-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6ec2a-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6ec2a-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6ec2a-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6ec2a-1045">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6ec2a-1046">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6ec2a-1047">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6ec2a-1048">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6ec2a-1049">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6ec2a-1050">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6ec2a-1051">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6ec2a-1052">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6ec2a-1053">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6ec2a-1054">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6ec2a-1055">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6ec2a-1056">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6ec2a-1057">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6ec2a-1058">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6ec2a-1059">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-1060">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6ec2a-1061">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6ec2a-1062">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6ec2a-1063">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6ec2a-1064">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6ec2a-1065">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6ec2a-1066">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6ec2a-1067">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-1069">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1070">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1071">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6ec2a-1072">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6ec2a-1073">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6ec2a-1074">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-1076">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1077">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1078">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6ec2a-1079">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6ec2a-1080">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6ec2a-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6ec2a-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6ec2a-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6ec2a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6ec2a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1086">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1087">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6ec2a-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="6ec2a-1089">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6ec2a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1091">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1092">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6ec2a-1093">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6ec2a-1094">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6ec2a-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1095">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-1096">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1097">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1098">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6ec2a-1099">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1100">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-1101">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6ec2a-1102">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1103">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1104">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6ec2a-1105">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6ec2a-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="6ec2a-1107">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1109">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-1111">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-1113">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6ec2a-1114">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1115">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1116">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6ec2a-1117">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6ec2a-1118">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6ec2a-1119">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1120">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1121">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6ec2a-1122">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-1124">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6ec2a-1125">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6ec2a-1126">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6ec2a-1127">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6ec2a-1128">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6ec2a-1129">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6ec2a-1130">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6ec2a-1131">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6ec2a-1132">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6ec2a-1133">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6ec2a-1134">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6ec2a-1135">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6ec2a-1136">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6ec2a-1137">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6ec2a-1138">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6ec2a-1139">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6ec2a-1140">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6ec2a-1141">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6ec2a-1142">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6ec2a-1143">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6ec2a-1144">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6ec2a-1145">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6ec2a-1146">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6ec2a-1147">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6ec2a-1148">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6ec2a-1149">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6ec2a-1150">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6ec2a-1151">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6ec2a-1152">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6ec2a-1153">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6ec2a-1154">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6ec2a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6ec2a-1156">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6ec2a-1157">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6ec2a-1158">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6ec2a-1159">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6ec2a-1160">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6ec2a-1161">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6ec2a-1162">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6ec2a-1163">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6ec2a-1164">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6ec2a-1165">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6ec2a-1166">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6ec2a-1167">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6ec2a-1168">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6ec2a-1169">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6ec2a-1170">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6ec2a-1171">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6ec2a-1172">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6ec2a-1173">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6ec2a-1174">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6ec2a-1175">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6ec2a-1176">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6ec2a-1177">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6ec2a-1178">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6ec2a-1179">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6ec2a-1180">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6ec2a-1181">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6ec2a-1182">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6ec2a-1183">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6ec2a-1184">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6ec2a-1185">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6ec2a-1186">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6ec2a-1187">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6ec2a-1188">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6ec2a-1189">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6ec2a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6ec2a-1191">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6ec2a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6ec2a-1193">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6ec2a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6ec2a-1195">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6ec2a-1196">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6ec2a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6ec2a-1198">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6ec2a-1199">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6ec2a-1200">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1201">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1202">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6ec2a-1203">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6ec2a-1204">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6ec2a-1205">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6ec2a-1206">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6ec2a-1207">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6ec2a-1208">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1209">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1210">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6ec2a-1211">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1213">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1214">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-1215">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1216">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1217">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6ec2a-1218">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="6ec2a-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6ec2a-1220">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1221">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1222">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1223">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1224">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6ec2a-1225">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1226">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1227">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-1229">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6ec2a-1230">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1231">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1232">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6ec2a-1233">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6ec2a-1234">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6ec2a-1235">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6ec2a-1236">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6ec2a-1237">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6ec2a-1238">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1238">Breaking changes</span></span>
    - <span data-ttu-id="6ec2a-1239">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6ec2a-1240">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6ec2a-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="6ec2a-1242">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6ec2a-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1243">Az.Dns</span></span>
* <span data-ttu-id="6ec2a-1244">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6ec2a-1245">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6ec2a-1246">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="6ec2a-1248">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6ec2a-1249">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1250">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-1251">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6ec2a-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6ec2a-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6ec2a-1254">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6ec2a-1255">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6ec2a-1256">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6ec2a-1257">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1258">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-1259">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6ec2a-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6ec2a-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6ec2a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6ec2a-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6ec2a-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6ec2a-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6ec2a-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6ec2a-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6ec2a-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6ec2a-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6ec2a-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6ec2a-1271">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6ec2a-1272">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1273">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1274">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6ec2a-1275">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1275">New cmdlets</span></span>
        - <span data-ttu-id="6ec2a-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="6ec2a-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6ec2a-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6ec2a-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6ec2a-1280">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="6ec2a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6ec2a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6ec2a-1283">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6ec2a-1284">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6ec2a-1285">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6ec2a-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="6ec2a-1287">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6ec2a-1288">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6ec2a-1289">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1291">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6ec2a-1292">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6ec2a-1293">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6ec2a-1294">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6ec2a-1295">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6ec2a-1296">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6ec2a-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1297">Az.Relay</span></span>
* <span data-ttu-id="6ec2a-1298">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-1300">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1301">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1302">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6ec2a-1303">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6ec2a-1304">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6ec2a-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="6ec2a-1306">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6ec2a-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6ec2a-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6ec2a-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1310">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1311">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6ec2a-1312">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6ec2a-1313">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6ec2a-1314">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="6ec2a-1315">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="6ec2a-1316">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6ec2a-1317">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6ec2a-1318">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6ec2a-1319">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6ec2a-1320">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1321">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1322">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1323">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6ec2a-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1324">Az.Batch</span></span>
* <span data-ttu-id="6ec2a-1325">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1326">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-1327">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-1329">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1330">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1331">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6ec2a-1332">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1333">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1334">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-1335">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1337">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6ec2a-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1338">Az.EventGrid</span></span>
* <span data-ttu-id="6ec2a-1339">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1340">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-1341">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6ec2a-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1342">Az.HDInsight</span></span>
* <span data-ttu-id="6ec2a-1343">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1344">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-1345">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1346">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-1347">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1348">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6ec2a-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="6ec2a-1350">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6ec2a-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1351">Az.Media</span></span>
* <span data-ttu-id="6ec2a-1352">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1353">Az.Monitor</span></span>
  * <span data-ttu-id="6ec2a-1354">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6ec2a-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6ec2a-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6ec2a-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6ec2a-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6ec2a-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6ec2a-1360">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1361">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1362">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1363">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6ec2a-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="6ec2a-1365">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-1367">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6ec2a-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6ec2a-1369">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1371">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1372">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6ec2a-1373">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6ec2a-1374">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6ec2a-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1375">Az.RedisCache</span></span>
* <span data-ttu-id="6ec2a-1376">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1377">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1378">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1379">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1380">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6ec2a-1381">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1382">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6ec2a-1383">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6ec2a-1384">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6ec2a-1385">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6ec2a-1386">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1387">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1388">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6ec2a-1389">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6ec2a-1390">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6ec2a-1391">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6ec2a-1392">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6ec2a-1393">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="6ec2a-1394">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="6ec2a-1395">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6ec2a-1396">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6ec2a-1397">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6ec2a-1398">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6ec2a-1399">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1400">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1401">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1402">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6ec2a-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="6ec2a-1404">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6ec2a-1405">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1406">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1407">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6ec2a-1408">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6ec2a-1409">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1410">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1411">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6ec2a-1412">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6ec2a-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="6ec2a-1414">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1415">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-1416">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6ec2a-1417">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1418">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1419">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6ec2a-1420">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6ec2a-1421">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6ec2a-1422">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6ec2a-1423">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6ec2a-1424">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1425">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1426">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1427">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1428">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6ec2a-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="6ec2a-1430">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6ec2a-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6ec2a-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6ec2a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6ec2a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6ec2a-1435">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6ec2a-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6ec2a-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6ec2a-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6ec2a-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6ec2a-1440">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6ec2a-1441">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="6ec2a-1442">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="6ec2a-1443">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6ec2a-1444">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6ec2a-1445">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6ec2a-1446">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6ec2a-1447">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1448">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1449">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1450">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6ec2a-1451">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="6ec2a-1452">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1452">Pre-Post script</span></span>
    * <span data-ttu-id="6ec2a-1453">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1454">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1455">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6ec2a-1456">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1457">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-1458">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1459">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1460">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6ec2a-1461">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1463">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6ec2a-1464">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1465">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1466">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6ec2a-1467">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1468">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1469">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1470">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1471">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6ec2a-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6ec2a-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6ec2a-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6ec2a-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6ec2a-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6ec2a-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1478">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1479">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6ec2a-1480">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1481">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1482">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6ec2a-1483">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1484">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1485">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6ec2a-1486">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6ec2a-1487">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1488">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-1489">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1490">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1491">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1492">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-1493">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6ec2a-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1494">Az.LogicApp</span></span>
* <span data-ttu-id="6ec2a-1495">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1496">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1497">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1499">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6ec2a-1500">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1500">SDK Update</span></span>
* <span data-ttu-id="6ec2a-1501">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6ec2a-1502">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1503">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1504">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6ec2a-1505">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6ec2a-1506">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6ec2a-1507">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6ec2a-1508">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6ec2a-1509">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1510">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1511">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6ec2a-1512">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1513">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1514">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6ec2a-1515">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6ec2a-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="6ec2a-1517">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1518">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1519">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6ec2a-1520">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6ec2a-1521">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-1523">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1524">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1525">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6ec2a-1526">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6ec2a-1527">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6ec2a-1528">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1530">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6ec2a-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1531">Az.EventHub</span></span>
* <span data-ttu-id="6ec2a-1532">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1533">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-1534">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6ec2a-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1535">Az.LogicApp</span></span>
* <span data-ttu-id="6ec2a-1536">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6ec2a-1537">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6ec2a-1538">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6ec2a-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6ec2a-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6ec2a-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6ec2a-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6ec2a-1543">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6ec2a-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6ec2a-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6ec2a-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6ec2a-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6ec2a-1548">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6ec2a-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1549">Az.Monitor</span></span>
* <span data-ttu-id="6ec2a-1550">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1551">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1552">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="6ec2a-1554">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6ec2a-1555">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6ec2a-1556">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1557">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1558">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6ec2a-1559">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6ec2a-1560">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6ec2a-1561">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1562">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1563">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6ec2a-1564">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1565">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1566">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6ec2a-1567">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1568">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1569">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6ec2a-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="6ec2a-1571">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1572">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1573">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6ec2a-1574">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6ec2a-1575">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="6ec2a-1577">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1578">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1579">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6ec2a-1580">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6ec2a-1581">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6ec2a-1582">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1583">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1584">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6ec2a-1585">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6ec2a-1586">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6ec2a-1587">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1588">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1589">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6ec2a-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="6ec2a-1591">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="6ec2a-1593">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6ec2a-1594">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1595">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1596">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6ec2a-1597">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6ec2a-1598">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6ec2a-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1599">Az.Aks</span></span>
* <span data-ttu-id="6ec2a-1600">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6ec2a-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1601">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1602">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6ec2a-1603">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6ec2a-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1604">Az.Cdn</span></span>
* <span data-ttu-id="6ec2a-1605">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1606">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1607">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6ec2a-1608">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6ec2a-1609">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6ec2a-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6ec2a-1611">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6ec2a-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1612">Az.DataFactory</span></span>
* <span data-ttu-id="6ec2a-1613">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1615">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6ec2a-1616">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6ec2a-1617">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1618">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-1619">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1620">Az.KeyVault</span></span>
* <span data-ttu-id="6ec2a-1621">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1622">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1623">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1624">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1625">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6ec2a-1626">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6ec2a-1627">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6ec2a-1628">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6ec2a-1629">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6ec2a-1630">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6ec2a-1631">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-1633">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6ec2a-1634">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1634">Fix some error messages.</span></span>
* <span data-ttu-id="6ec2a-1635">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6ec2a-1636">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6ec2a-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1637">Az.SignalR</span></span>
* <span data-ttu-id="6ec2a-1638">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1639">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1640">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6ec2a-1641">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6ec2a-1642">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6ec2a-1643">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1644">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1645">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6ec2a-1646">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6ec2a-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6ec2a-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6ec2a-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="6ec2a-1650">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1651">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1652">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6ec2a-1653">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6ec2a-1654">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6ec2a-1655">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1656">Az.Accounts</span></span>
* <span data-ttu-id="6ec2a-1657">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1658">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1659">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6ec2a-1660">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6ec2a-1661">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1663">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6ec2a-1664">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6ec2a-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1665">Az.EventGrid</span></span>
* <span data-ttu-id="6ec2a-1666">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6ec2a-1667">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6ec2a-1668">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6ec2a-1669">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6ec2a-1670">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6ec2a-1671">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6ec2a-1672">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6ec2a-1673">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6ec2a-1674">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6ec2a-1675">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="6ec2a-1676">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6ec2a-1677">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6ec2a-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1678">Az.IotHub</span></span>
* <span data-ttu-id="6ec2a-1679">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6ec2a-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1680">Az.LogicApp</span></span>
* <span data-ttu-id="6ec2a-1681">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1682">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1683">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6ec2a-1684">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6ec2a-1685">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6ec2a-1686">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6ec2a-1687">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6ec2a-1688">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6ec2a-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1689">Az.SignalR</span></span>
* <span data-ttu-id="6ec2a-1690">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1691">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1692">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6ec2a-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1693">Az.Storage</span></span>
* <span data-ttu-id="6ec2a-1694">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6ec2a-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="6ec2a-1696">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6ec2a-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1698">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1699">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6ec2a-1700">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6ec2a-1701">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6ec2a-1702">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1702">General</span></span>

- <span data-ttu-id="6ec2a-1703">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="6ec2a-1704">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1704">Online help for each module</span></span>
- <span data-ttu-id="6ec2a-1705">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6ec2a-1706">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6ec2a-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1707">Az.Accounts</span></span>
- <span data-ttu-id="6ec2a-1708">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="6ec2a-1709">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="6ec2a-1711">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1711">Fixes for #7002</span></span>
- <span data-ttu-id="6ec2a-1712">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6ec2a-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1713">Az.Batch</span></span>
- <span data-ttu-id="6ec2a-1714">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6ec2a-1715">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6ec2a-1716">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6ec2a-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1717">Az.Billing</span></span>
- <span data-ttu-id="6ec2a-1718">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6ec2a-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="6ec2a-1720">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6ec2a-1721">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6ec2a-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="6ec2a-1723">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6ec2a-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6ec2a-1725">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="6ec2a-1727">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6ec2a-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1728">Az.Monitor</span></span>
- <span data-ttu-id="6ec2a-1729">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6ec2a-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1730">Az.KeyVault</span></span>
- <span data-ttu-id="6ec2a-1731">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6ec2a-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="6ec2a-1733">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6ec2a-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1734">Az.Media</span></span>
- <span data-ttu-id="6ec2a-1735">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1736">Az.Network</span></span>
<span data-ttu-id="6ec2a-1737">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6ec2a-1738">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="6ec2a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6ec2a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6ec2a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6ec2a-1747">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6ec2a-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6ec2a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6ec2a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6ec2a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6ec2a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6ec2a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6ec2a-1754">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6ec2a-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6ec2a-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6ec2a-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6ec2a-1758">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6ec2a-1759">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6ec2a-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="6ec2a-1761">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6ec2a-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1762">Az.Profile</span></span>
- <span data-ttu-id="6ec2a-1763">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="6ec2a-1765">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6ec2a-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1766">Az.Resources</span></span>
- <span data-ttu-id="6ec2a-1767">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="6ec2a-1769">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6ec2a-1770">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6ec2a-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="6ec2a-1772">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6ec2a-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1773">Az.Sql</span></span>
- <span data-ttu-id="6ec2a-1774">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6ec2a-1775">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6ec2a-1776">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6ec2a-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1777">Az.Storage</span></span>
- <span data-ttu-id="6ec2a-1778">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1779">Az.Websites</span></span>
- <span data-ttu-id="6ec2a-1780">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6ec2a-1781">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6ec2a-1782">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1782">General</span></span>

* <span data-ttu-id="6ec2a-1783">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6ec2a-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1784">Az.Compute</span></span>

* <span data-ttu-id="6ec2a-1785">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="6ec2a-1787">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6ec2a-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="6ec2a-1789">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="6ec2a-1790">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6ec2a-1791">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6ec2a-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="6ec2a-1793">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6ec2a-1794">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6ec2a-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1795">Az.Resources</span></span>

* <span data-ttu-id="6ec2a-1796">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6ec2a-1797">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6ec2a-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1798">Az.Sql</span></span>

* <span data-ttu-id="6ec2a-1799">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6ec2a-1800">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6ec2a-1801">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6ec2a-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1802">Az.Storage</span></span>

* <span data-ttu-id="6ec2a-1803">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6ec2a-1804">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6ec2a-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6ec2a-1806">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="6ec2a-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6ec2a-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1809">Az.Websites</span></span>

* <span data-ttu-id="6ec2a-1810">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6ec2a-1811">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6ec2a-1812">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6ec2a-1813">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6ec2a-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="6ec2a-1815">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6ec2a-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1816">Az.Automation</span></span>
* <span data-ttu-id="6ec2a-1817">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6ec2a-1818">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6ec2a-1819">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6ec2a-1820">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6ec2a-1821">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6ec2a-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1822">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1823">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6ec2a-1824">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6ec2a-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="6ec2a-1826">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6ec2a-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6ec2a-1828">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1829">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1830">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6ec2a-1831">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6ec2a-1832">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6ec2a-1833">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6ec2a-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6ec2a-1835">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6ec2a-1836">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6ec2a-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6ec2a-1838">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6ec2a-1839">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6ec2a-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1840">Az.Relay</span></span>
* <span data-ttu-id="6ec2a-1841">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6ec2a-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1842">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1843">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6ec2a-1844">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6ec2a-1845">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-1847">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6ec2a-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1848">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1849">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6ec2a-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6ec2a-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6ec2a-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6ec2a-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6ec2a-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6ec2a-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6ec2a-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6ec2a-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6ec2a-1858">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6ec2a-1859">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6ec2a-1860">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6ec2a-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6ec2a-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6ec2a-1863">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6ec2a-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6ec2a-1865">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6ec2a-1866">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6ec2a-1867">Geral</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1867">General</span></span>
* <span data-ttu-id="6ec2a-1868">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6ec2a-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1869">Az.Profile</span></span>
* <span data-ttu-id="6ec2a-1870">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6ec2a-1871">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6ec2a-1872">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6ec2a-1873">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6ec2a-1874">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6ec2a-1875">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6ec2a-1876">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-1878">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1879">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1880">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6ec2a-1881">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6ec2a-1882">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1884">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6ec2a-1885">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6ec2a-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1886">Az.Insights</span></span>
* <span data-ttu-id="6ec2a-1887">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6ec2a-1888">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6ec2a-1889">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6ec2a-1890">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1891">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1892">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6ec2a-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6ec2a-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6ec2a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6ec2a-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6ec2a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6ec2a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6ec2a-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="6ec2a-1900">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1901">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1902">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6ec2a-1903">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6ec2a-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="6ec2a-1905">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6ec2a-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="6ec2a-1907">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6ec2a-1908">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6ec2a-1909">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6ec2a-1910">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6ec2a-1911">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6ec2a-1912">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6ec2a-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1913">Az.Profile</span></span>
* <span data-ttu-id="6ec2a-1914">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6ec2a-1915">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1916">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1917">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6ec2a-1918">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6ec2a-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="6ec2a-1920">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6ec2a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6ec2a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6ec2a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6ec2a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1925">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1926">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6ec2a-1927">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1928">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1929">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6ec2a-1930">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6ec2a-1931">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6ec2a-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1932">Azure.Storage</span></span>
* <span data-ttu-id="6ec2a-1933">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6ec2a-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6ec2a-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6ec2a-1936">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6ec2a-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6ec2a-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="6ec2a-1939">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6ec2a-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1940">Az.Compute</span></span>
* <span data-ttu-id="6ec2a-1941">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6ec2a-1942">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6ec2a-1943">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6ec2a-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6ec2a-1945">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6ec2a-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1946">Az.Network</span></span>
* <span data-ttu-id="6ec2a-1947">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6ec2a-1948">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1948">new cmdlets added</span></span>
    - <span data-ttu-id="6ec2a-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6ec2a-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6ec2a-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6ec2a-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6ec2a-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6ec2a-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6ec2a-1955">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6ec2a-1956">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6ec2a-1957">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6ec2a-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1958">Az.RedisCache</span></span>
* <span data-ttu-id="6ec2a-1959">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6ec2a-1960">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6ec2a-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1961">Az.Resources</span></span>
* <span data-ttu-id="6ec2a-1962">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6ec2a-1963">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6ec2a-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1964">Az.Sql</span></span>
* <span data-ttu-id="6ec2a-1965">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6ec2a-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1966">Az.Websites</span></span>
* <span data-ttu-id="6ec2a-1967">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6ec2a-1968">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6ec2a-1969">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6ec2a-1970">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="6ec2a-1970">Initial Release</span></span>
