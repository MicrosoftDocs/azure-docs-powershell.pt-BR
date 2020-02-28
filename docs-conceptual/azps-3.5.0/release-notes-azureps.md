---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477226"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0b3c7-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b3c7-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0b3c7-104">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="0b3c7-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-105">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-105">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-106">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="0b3c7-107">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0b3c7-108">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-109">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-110">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-111">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-112">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-114">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0b3c7-115">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="0b3c7-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-116">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-117">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="0b3c7-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-118">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-119">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="0b3c7-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-120">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-121">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0b3c7-122">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="0b3c7-123">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0b3c7-124">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0b3c7-125">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0b3c7-126">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-127">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-128">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="0b3c7-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-129">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-130">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0b3c7-131">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0b3c7-132">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-133">Az.Network</span></span>
* <span data-ttu-id="0b3c7-134">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0b3c7-135">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0b3c7-136">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0b3c7-137">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0b3c7-138">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-138">No new cmdlets are added.</span></span> <span data-ttu-id="0b3c7-139">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-141">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-142">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-143">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0b3c7-144">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0b3c7-145">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0b3c7-146">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="0b3c7-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0b3c7-147">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0b3c7-148">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="0b3c7-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0b3c7-149">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0b3c7-150">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-151">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-152">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0b3c7-153">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0b3c7-154">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0b3c7-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0b3c7-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b3c7-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0b3c7-156">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0b3c7-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0b3c7-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0b3c7-157">Az.StorageSync</span></span>
* <span data-ttu-id="0b3c7-158">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0b3c7-159">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="0b3c7-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-160">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-160">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-161">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0b3c7-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0b3c7-162">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-163">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-164">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="0b3c7-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0b3c7-165">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="0b3c7-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-166">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-167">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0b3c7-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0b3c7-168">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0b3c7-169">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="0b3c7-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0b3c7-170">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-171">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-172">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0b3c7-173">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0b3c7-174">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0b3c7-176">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-177">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-178">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0b3c7-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0b3c7-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="0b3c7-180">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0b3c7-181">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="0b3c7-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-182">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-183">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-184">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-185">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-186">Az.Network</span></span>
* <span data-ttu-id="0b3c7-187">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0b3c7-188">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0b3c7-189">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-190">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="0b3c7-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0b3c7-191">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0b3c7-192">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0b3c7-193">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0b3c7-194">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0b3c7-195">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-195">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0b3c7-197">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0b3c7-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0b3c7-199">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0b3c7-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="0b3c7-201">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="0b3c7-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0b3c7-202">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0b3c7-203">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="0b3c7-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0b3c7-204">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="0b3c7-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-206">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0b3c7-207">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-208">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-209">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="0b3c7-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0b3c7-210">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="0b3c7-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-211">Az.Sql</span></span>
<span data-ttu-id="0b3c7-212">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-213">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-214">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0b3c7-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="0b3c7-216">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0b3c7-217">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-218">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-219">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="0b3c7-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0b3c7-220">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="0b3c7-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0b3c7-221">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="0b3c7-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-222">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-223">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0b3c7-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-224">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-225">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-226">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-227">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0b3c7-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="0b3c7-229">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0b3c7-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0b3c7-231">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0b3c7-232">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0b3c7-233">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0b3c7-234">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0b3c7-235">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0b3c7-236">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0b3c7-237">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0b3c7-238">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0b3c7-239">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0b3c7-240">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0b3c7-241">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0b3c7-242">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0b3c7-243">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0b3c7-244">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0b3c7-245">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0b3c7-246">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0b3c7-247">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0b3c7-248">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-249">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-250">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0b3c7-251">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0b3c7-252">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0b3c7-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0b3c7-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="0b3c7-254">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="0b3c7-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-255">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-256">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="0b3c7-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-257">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-258">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0b3c7-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0b3c7-259">Az.MachineLearning</span></span>
* <span data-ttu-id="0b3c7-260">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="0b3c7-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0b3c7-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0b3c7-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0b3c7-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0b3c7-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0b3c7-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0b3c7-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0b3c7-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0b3c7-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0b3c7-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0b3c7-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0b3c7-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0b3c7-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-268">Az.Network</span></span>
* <span data-ttu-id="0b3c7-269">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="0b3c7-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-271">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0b3c7-272">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0b3c7-273">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0b3c7-274">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-275">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-276">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-277">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-278">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0b3c7-279">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="0b3c7-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0b3c7-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b3c7-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0b3c7-281">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="0b3c7-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-282">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-283">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="0b3c7-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0b3c7-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0b3c7-285">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="0b3c7-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="0b3c7-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0b3c7-287">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0b3c7-288">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-288">General</span></span>
* <span data-ttu-id="0b3c7-289">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-290">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-291">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="0b3c7-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0b3c7-292">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="0b3c7-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0b3c7-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-293">Az.Batch</span></span>
* <span data-ttu-id="0b3c7-294">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-295">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-296">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-297">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-298">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="0b3c7-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0b3c7-299">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="0b3c7-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0b3c7-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0b3c7-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="0b3c7-301">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="0b3c7-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-302">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-303">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="0b3c7-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0b3c7-304">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="0b3c7-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0b3c7-305">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-306">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-307">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0b3c7-308">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="0b3c7-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0b3c7-309">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-310">Az.Network</span></span>
* <span data-ttu-id="0b3c7-311">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-312">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-313">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0b3c7-314">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-315">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-316">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-317">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-318">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="0b3c7-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0b3c7-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0b3c7-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0b3c7-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0b3c7-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0b3c7-321">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0b3c7-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0b3c7-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0b3c7-323">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0b3c7-324">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="0b3c7-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0b3c7-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0b3c7-327">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0b3c7-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0b3c7-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0b3c7-329">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0b3c7-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0b3c7-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0b3c7-331">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-332">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-332">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-333">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0b3c7-334">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-335">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-336">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-336">VM Reapply feature</span></span>
    - <span data-ttu-id="0b3c7-337">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0b3c7-338">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0b3c7-339">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0b3c7-340">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0b3c7-341">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0b3c7-342">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0b3c7-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0b3c7-343">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="0b3c7-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0b3c7-344">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0b3c7-345">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="0b3c7-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0b3c7-346">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0b3c7-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0b3c7-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0b3c7-348">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0b3c7-349">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-349">Get the Order</span></span>
* <span data-ttu-id="0b3c7-350">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0b3c7-351">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-351">Create new Order</span></span>
* <span data-ttu-id="0b3c7-352">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0b3c7-353">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-353">Remove the Order</span></span>
* <span data-ttu-id="0b3c7-354">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0b3c7-355">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="0b3c7-355">Now creates Local Share</span></span>
* <span data-ttu-id="0b3c7-356">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0b3c7-357">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="0b3c7-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0b3c7-358">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0b3c7-359">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0b3c7-360">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0b3c7-361">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="0b3c7-362">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0b3c7-363">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-363">Create new Triggers</span></span>
* <span data-ttu-id="0b3c7-364">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0b3c7-365">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-366">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-367">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0b3c7-368">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-370">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-371">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-372">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-373">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-374">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0b3c7-375">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0b3c7-376">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="0b3c7-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0b3c7-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-378">Az.Network</span></span>
* <span data-ttu-id="0b3c7-379">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0b3c7-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0b3c7-380">Az.PrivateDns</span></span>
* <span data-ttu-id="0b3c7-381">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-383">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0b3c7-384">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0b3c7-385">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0b3c7-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-386">Az.RedisCache</span></span>
* <span data-ttu-id="0b3c7-387">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0b3c7-388">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0b3c7-389">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-390">Az.Resources</span></span>
- <span data-ttu-id="0b3c7-391">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0b3c7-392">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="0b3c7-393">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0b3c7-394">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0b3c7-395">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-396">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-397">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0b3c7-398">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="0b3c7-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0b3c7-399">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0b3c7-400">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-400">General</span></span>
* <span data-ttu-id="0b3c7-401">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-402">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-403">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0b3c7-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-404">Az.Advisor</span></span>
* <span data-ttu-id="0b3c7-405">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0b3c7-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-406">Az.Batch</span></span>
* <span data-ttu-id="0b3c7-407">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0b3c7-408">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0b3c7-409">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0b3c7-410">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0b3c7-411">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0b3c7-412">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0b3c7-413">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0b3c7-414">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0b3c7-415">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0b3c7-416">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0b3c7-417">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0b3c7-418">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0b3c7-419">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0b3c7-420">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0b3c7-421">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0b3c7-422">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0b3c7-423">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0b3c7-424">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0b3c7-425">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0b3c7-426">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="0b3c7-427">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0b3c7-428">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0b3c7-429">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0b3c7-430">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="0b3c7-431">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0b3c7-432">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="0b3c7-433">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0b3c7-434">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0b3c7-435">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0b3c7-436">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0b3c7-437">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0b3c7-438">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0b3c7-439">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0b3c7-440">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0b3c7-441">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0b3c7-442">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-443">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-444">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0b3c7-445">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-446">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-447">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="0b3c7-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0b3c7-448">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0b3c7-449">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="0b3c7-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0b3c7-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0b3c7-451">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0b3c7-452">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0b3c7-453">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="0b3c7-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0b3c7-454">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0b3c7-455">Alterações da falha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-455">Breaking changes</span></span>
    - <span data-ttu-id="0b3c7-456">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0b3c7-457">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-458">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-459">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-461">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="0b3c7-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0b3c7-462">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0b3c7-463">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="0b3c7-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0b3c7-464">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="0b3c7-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0b3c7-465">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0b3c7-466">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="0b3c7-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-467">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-468">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-469">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-470">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0b3c7-471">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0b3c7-472">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0b3c7-473">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0b3c7-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0b3c7-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0b3c7-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0b3c7-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0b3c7-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0b3c7-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0b3c7-479">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-480">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0b3c7-481">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0b3c7-482">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0b3c7-483">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0b3c7-484">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0b3c7-485">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0b3c7-486">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0b3c7-487">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0b3c7-488">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0b3c7-489">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0b3c7-490">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="0b3c7-491">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-492">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-493">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-493">Breaking changes:</span></span>
    - <span data-ttu-id="0b3c7-494">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0b3c7-495">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0b3c7-496">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0b3c7-497">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0b3c7-498">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0b3c7-499">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0b3c7-500">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0b3c7-501">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0b3c7-502">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0b3c7-503">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0b3c7-504">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0b3c7-505">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-507">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-508">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0b3c7-509">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0b3c7-510">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-511">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-512">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-513">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-514">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-515">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="0b3c7-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-516">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-517">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-518">Az.Network</span></span>
* <span data-ttu-id="0b3c7-519">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de Serviço Genérico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0b3c7-520">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0b3c7-526">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de Serviço Genérico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0b3c7-527">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-527">New cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0b3c7-529">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0b3c7-530">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0b3c7-531">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0b3c7-532">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0b3c7-533">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0b3c7-534">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0b3c7-535">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0b3c7-536">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-536">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0b3c7-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0b3c7-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0b3c7-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0b3c7-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0b3c7-542">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0b3c7-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0b3c7-543">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0b3c7-544">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0b3c7-545">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0b3c7-546">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0b3c7-547">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0b3c7-548">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0b3c7-549">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-549">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0b3c7-551">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0b3c7-552">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0b3c7-553">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0b3c7-554">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0b3c7-555">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0b3c7-556">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0b3c7-557">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="0b3c7-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0b3c7-558">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-558">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0b3c7-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0b3c7-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0b3c7-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0b3c7-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0b3c7-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0b3c7-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0b3c7-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0b3c7-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0b3c7-565">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0b3c7-566">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0b3c7-567">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0b3c7-568">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0b3c7-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0b3c7-569">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0b3c7-570">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0b3c7-571">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0b3c7-572">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0b3c7-573">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0b3c7-574">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0b3c7-575">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0b3c7-576">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-576">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="0b3c7-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0b3c7-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0b3c7-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-582">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-583">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-584">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0b3c7-585">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0b3c7-586">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0b3c7-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0b3c7-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0b3c7-589">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0b3c7-590">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0b3c7-591">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="0b3c7-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="0b3c7-592">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-593">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-594">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0b3c7-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0b3c7-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0b3c7-597">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="0b3c7-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0b3c7-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0b3c7-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0b3c7-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0b3c7-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="0b3c7-600">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0b3c7-601">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-601">General</span></span>
* <span data-ttu-id="0b3c7-602">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-603">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-604">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-605">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-606">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0b3c7-607">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="0b3c7-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-608">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-609">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="0b3c7-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-610">Az.Batch</span></span>
* <span data-ttu-id="0b3c7-611">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-612">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-613">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0b3c7-614">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0b3c7-615">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="0b3c7-616">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-617">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-618">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0b3c7-619">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0b3c7-620">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-622">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="0b3c7-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0b3c7-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0b3c7-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="0b3c7-624">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0b3c7-625">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0b3c7-626">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="0b3c7-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0b3c7-627">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-628">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-629">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0b3c7-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0b3c7-630">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b3c7-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-631">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-632">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0b3c7-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0b3c7-633">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0b3c7-634">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="0b3c7-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0b3c7-635">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-636">Az.Network</span></span>
* <span data-ttu-id="0b3c7-637">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0b3c7-638">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0b3c7-639">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-639">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0b3c7-641">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0b3c7-642">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="0b3c7-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0b3c7-643">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="0b3c7-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0b3c7-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0b3c7-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0b3c7-647">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="0b3c7-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0b3c7-648">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0b3c7-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0b3c7-649">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0b3c7-650">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0b3c7-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-651">Az.RedisCache</span></span>
* <span data-ttu-id="0b3c7-652">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-653">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-654">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-655">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-656">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0b3c7-657">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0b3c7-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0b3c7-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0b3c7-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0b3c7-659">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0b3c7-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0b3c7-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0b3c7-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0b3c7-661">Az.StorageSync</span></span>
* <span data-ttu-id="0b3c7-662">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-663">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-664">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="0b3c7-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0b3c7-665">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-666">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-667">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0b3c7-668">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0b3c7-669">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-670">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-671">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0b3c7-672">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="0b3c7-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0b3c7-673">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-674">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-675">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0b3c7-676">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0b3c7-677">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0b3c7-678">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0b3c7-679">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0b3c7-680">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0b3c7-681">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0b3c7-682">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0b3c7-683">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-684">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-685">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0b3c7-686">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="0b3c7-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-687">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-688">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-689">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-690">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0b3c7-691">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0b3c7-692">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-692">New cmdlets are:</span></span>
    - <span data-ttu-id="0b3c7-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0b3c7-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0b3c7-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0b3c7-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-697">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-698">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0b3c7-699">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0b3c7-700">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0b3c7-701">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0b3c7-702">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0b3c7-703">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0b3c7-704">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0b3c7-705">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0b3c7-706">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0b3c7-707">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0b3c7-708">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0b3c7-709">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0b3c7-710">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0b3c7-711">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="0b3c7-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0b3c7-712">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="0b3c7-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0b3c7-713">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0b3c7-714">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0b3c7-715">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0b3c7-716">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0b3c7-717">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-717">Overall improved help files</span></span>
* <span data-ttu-id="0b3c7-718">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-719">Az.Network</span></span>
* <span data-ttu-id="0b3c7-720">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="0b3c7-721">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="0b3c7-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0b3c7-722">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0b3c7-723">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0b3c7-724">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="0b3c7-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0b3c7-725">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="0b3c7-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0b3c7-726">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0b3c7-727">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0b3c7-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0b3c7-728">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0b3c7-729">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0b3c7-730">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0b3c7-731">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0b3c7-732">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-732">New cmdlets</span></span>
        - <span data-ttu-id="0b3c7-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0b3c7-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0b3c7-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0b3c7-735">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-736">New-VpnSite</span></span>
        - <span data-ttu-id="0b3c7-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-737">Update-VpnSite</span></span>
        - <span data-ttu-id="0b3c7-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-738">New-VpnConnection</span></span>
        - <span data-ttu-id="0b3c7-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-739">Update-VpnConnection</span></span>
* <span data-ttu-id="0b3c7-740">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-742">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0b3c7-743">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="0b3c7-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-744">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-745">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-747">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0b3c7-748">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0b3c7-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0b3c7-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0b3c7-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0b3c7-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0b3c7-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0b3c7-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0b3c7-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0b3c7-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0b3c7-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0b3c7-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0b3c7-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0b3c7-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0b3c7-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0b3c7-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0b3c7-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0b3c7-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0b3c7-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0b3c7-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0b3c7-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0b3c7-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0b3c7-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0b3c7-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0b3c7-762">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0b3c7-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-763">Az.SignalR</span></span>
* <span data-ttu-id="0b3c7-764">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-765">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-766">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0b3c7-767">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0b3c7-768">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0b3c7-769">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0b3c7-770">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-771">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-772">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0b3c7-773">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="0b3c7-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0b3c7-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0b3c7-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0b3c7-776">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0b3c7-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0b3c7-778">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0b3c7-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0b3c7-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0b3c7-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0b3c7-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-783">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-784">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="0b3c7-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0b3c7-785">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="0b3c7-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0b3c7-786">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0b3c7-787">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0b3c7-788">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-788">General</span></span>
* <span data-ttu-id="0b3c7-789">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-790">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-791">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0b3c7-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0b3c7-792">Az.Aks</span></span>
* <span data-ttu-id="0b3c7-793">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0b3c7-794">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0b3c7-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-795">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-796">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="0b3c7-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0b3c7-797">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="0b3c7-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0b3c7-798">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0b3c7-799">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0b3c7-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0b3c7-800">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0b3c7-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-801">Az.Batch</span></span>
* <span data-ttu-id="0b3c7-802">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="0b3c7-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-803">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-804">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="0b3c7-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-805">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-806">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0b3c7-807">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0b3c7-808">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0b3c7-809">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0b3c7-810">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0b3c7-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0b3c7-811">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0b3c7-812">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="0b3c7-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0b3c7-813">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-814">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-815">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0b3c7-816">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="0b3c7-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0b3c7-817">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0b3c7-818">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="0b3c7-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-820">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-821">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-822">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0b3c7-823">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="0b3c7-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0b3c7-824">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0b3c7-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0b3c7-825">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="0b3c7-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0b3c7-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0b3c7-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0b3c7-827">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-828">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-829">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-830">Az.Network</span></span>
* <span data-ttu-id="0b3c7-831">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0b3c7-832">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0b3c7-833">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0b3c7-834">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="0b3c7-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0b3c7-835">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="0b3c7-836">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0b3c7-837">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0b3c7-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-839">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0b3c7-840">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-840">Added example</span></span>
    - <span data-ttu-id="0b3c7-841">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0b3c7-842">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0b3c7-843">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-845">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-846">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-847">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0b3c7-848">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="0b3c7-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0b3c7-849">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0b3c7-850">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-851">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-852">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0b3c7-853">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="0b3c7-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0b3c7-854">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="0b3c7-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-856">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0b3c7-857">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0b3c7-858">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0b3c7-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0b3c7-859">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0b3c7-860">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0b3c7-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0b3c7-861">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0b3c7-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-862">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-863">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-864">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-865">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b3c7-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0b3c7-866">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="0b3c7-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0b3c7-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0b3c7-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0b3c7-869">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="0b3c7-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0b3c7-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-871">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-872">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0b3c7-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0b3c7-873">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-874">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-875">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0b3c7-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0b3c7-877">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-878">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-879">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-881">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-882">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-883">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0b3c7-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0b3c7-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0b3c7-885">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0b3c7-886">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0b3c7-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-887">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-888">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0b3c7-889">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="0b3c7-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-890">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-891">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0b3c7-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0b3c7-892">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="0b3c7-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-893">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-894">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0b3c7-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-895">Az.LogicApp</span></span>
* <span data-ttu-id="0b3c7-896">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="0b3c7-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0b3c7-897">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0b3c7-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-898">Az.ManagedServices</span></span>
* <span data-ttu-id="0b3c7-899">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-900">Az.Network</span></span>
* <span data-ttu-id="0b3c7-901">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0b3c7-902">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-902">New cmdlets</span></span>
        - <span data-ttu-id="0b3c7-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0b3c7-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0b3c7-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0b3c7-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0b3c7-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0b3c7-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0b3c7-911">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="0b3c7-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0b3c7-912">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0b3c7-913">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0b3c7-914">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0b3c7-915">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0b3c7-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0b3c7-916">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="0b3c7-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0b3c7-917">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-917">Updated cmdlets</span></span>
        - <span data-ttu-id="0b3c7-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0b3c7-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0b3c7-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0b3c7-921">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0b3c7-922">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0b3c7-923">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0b3c7-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0b3c7-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0b3c7-927">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0b3c7-928">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0b3c7-929">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-931">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="0b3c7-932">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="0b3c7-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-934">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0b3c7-935">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0b3c7-936">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0b3c7-937">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0b3c7-938">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0b3c7-939">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0b3c7-940">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0b3c7-941">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0b3c7-942">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0b3c7-943">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-944">Az.Resources</span></span>
- <span data-ttu-id="0b3c7-945">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0b3c7-946">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0b3c7-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-947">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-948">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0b3c7-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0b3c7-949">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="0b3c7-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-950">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-951">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0b3c7-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0b3c7-952">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="0b3c7-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0b3c7-953">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-954">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-955">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="0b3c7-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0b3c7-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0b3c7-956">Az.StorageSync</span></span>
* <span data-ttu-id="0b3c7-957">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0b3c7-958">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="0b3c7-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-959">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-960">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0b3c7-961">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0b3c7-962">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0b3c7-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0b3c7-963">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-964">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-965">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="0b3c7-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0b3c7-966">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0b3c7-967">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b3c7-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0b3c7-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-968">Az.Advisor</span></span>
* <span data-ttu-id="0b3c7-969">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0b3c7-970">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-971">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-972">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="0b3c7-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0b3c7-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0b3c7-974">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="0b3c7-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0b3c7-975">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0b3c7-976">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="0b3c7-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0b3c7-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0b3c7-978">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="0b3c7-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-979">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-980">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-981">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-982">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-983">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-984">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0b3c7-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b3c7-985">Az.EventGrid</span></span>
* <span data-ttu-id="0b3c7-986">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-987">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-988">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-989">Az.Network</span></span>
* <span data-ttu-id="0b3c7-990">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="0b3c7-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0b3c7-991">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0b3c7-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="0b3c7-993">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="0b3c7-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0b3c7-994">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0b3c7-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-996">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-998">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-999">Az.Resources</span></span>
    - <span data-ttu-id="0b3c7-1000">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0b3c7-1001">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0b3c7-1002">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0b3c7-1003">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-1005">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1006">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1007">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0b3c7-1008">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0b3c7-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0b3c7-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0b3c7-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0b3c7-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0b3c7-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0b3c7-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0b3c7-1015">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1016">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1017">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0b3c7-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0b3c7-1019">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0b3c7-1020">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0b3c7-1021">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0b3c7-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0b3c7-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0b3c7-1024">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0b3c7-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0b3c7-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0b3c7-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1027">Az.StorageSync</span></span>
* <span data-ttu-id="0b3c7-1028">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0b3c7-1029">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1030">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1031">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0b3c7-1032">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0b3c7-1033">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0b3c7-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0b3c7-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1036">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1037">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0b3c7-1038">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0b3c7-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1039">Az.Dns</span></span>
* <span data-ttu-id="0b3c7-1040">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0b3c7-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1041">Az.EventGrid</span></span>
* <span data-ttu-id="0b3c7-1042">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0b3c7-1043">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1043">New cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0b3c7-1045">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0b3c7-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0b3c7-1047">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0b3c7-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0b3c7-1049">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0b3c7-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0b3c7-1051">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0b3c7-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0b3c7-1053">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0b3c7-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0b3c7-1055">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0b3c7-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0b3c7-1057">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0b3c7-1058">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0b3c7-1059">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0b3c7-1060">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0b3c7-1062">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0b3c7-1063">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0b3c7-1064">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0b3c7-1065">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0b3c7-1066">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0b3c7-1067">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0b3c7-1068">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0b3c7-1069">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0b3c7-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0b3c7-1071">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0b3c7-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0b3c7-1073">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0b3c7-1074">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0b3c7-1077">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0b3c7-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0b3c7-1079">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1080">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1081">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0b3c7-1082">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1082">New cmdlets</span></span>
        - <span data-ttu-id="0b3c7-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0b3c7-1084">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0b3c7-1085">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1085">New cmdlets</span></span> 
        - <span data-ttu-id="0b3c7-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0b3c7-1087">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0b3c7-1088">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1088">New cmdlets</span></span> 
        - <span data-ttu-id="0b3c7-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0b3c7-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0b3c7-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0b3c7-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0b3c7-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0b3c7-1094">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0b3c7-1095">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1095">New cmdlets</span></span>
        - <span data-ttu-id="0b3c7-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0b3c7-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0b3c7-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0b3c7-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0b3c7-1100">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0b3c7-1101">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0b3c7-1102">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0b3c7-1103">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0b3c7-1104">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0b3c7-1105">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0b3c7-1106">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0b3c7-1107">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0b3c7-1108">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0b3c7-1109">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0b3c7-1110">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0b3c7-1111">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0b3c7-1112">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0b3c7-1113">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0b3c7-1114">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-1115">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0b3c7-1116">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0b3c7-1117">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0b3c7-1118">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0b3c7-1119">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0b3c7-1120">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0b3c7-1121">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0b3c7-1122">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-1124">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1125">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1126">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0b3c7-1127">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0b3c7-1128">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0b3c7-1129">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-1131">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1132">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1133">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0b3c7-1134">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0b3c7-1135">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0b3c7-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0b3c7-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0b3c7-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0b3c7-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0b3c7-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1141">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1142">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0b3c7-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="0b3c7-1144">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0b3c7-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1146">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1147">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0b3c7-1148">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0b3c7-1149">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0b3c7-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1150">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-1151">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1152">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1153">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0b3c7-1154">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1155">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-1156">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0b3c7-1157">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1158">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1159">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0b3c7-1160">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0b3c7-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="0b3c7-1162">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1164">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-1166">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-1168">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0b3c7-1169">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1170">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1171">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0b3c7-1172">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0b3c7-1173">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0b3c7-1174">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1175">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1176">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0b3c7-1177">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-1179">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0b3c7-1180">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0b3c7-1181">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0b3c7-1182">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0b3c7-1183">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0b3c7-1184">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0b3c7-1185">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0b3c7-1186">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0b3c7-1187">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0b3c7-1188">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0b3c7-1189">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0b3c7-1190">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0b3c7-1191">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0b3c7-1192">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0b3c7-1193">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0b3c7-1194">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0b3c7-1195">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0b3c7-1196">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0b3c7-1197">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0b3c7-1198">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0b3c7-1199">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0b3c7-1200">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0b3c7-1201">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0b3c7-1202">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0b3c7-1203">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0b3c7-1204">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0b3c7-1205">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0b3c7-1206">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0b3c7-1207">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0b3c7-1208">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0b3c7-1209">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0b3c7-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0b3c7-1211">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0b3c7-1212">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0b3c7-1213">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0b3c7-1214">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0b3c7-1215">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0b3c7-1216">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0b3c7-1217">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0b3c7-1218">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0b3c7-1219">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0b3c7-1220">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0b3c7-1221">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0b3c7-1222">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0b3c7-1223">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0b3c7-1224">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0b3c7-1225">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0b3c7-1226">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0b3c7-1227">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0b3c7-1228">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0b3c7-1229">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0b3c7-1230">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0b3c7-1231">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0b3c7-1232">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0b3c7-1233">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0b3c7-1234">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0b3c7-1235">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0b3c7-1236">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0b3c7-1237">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0b3c7-1238">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0b3c7-1239">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0b3c7-1240">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0b3c7-1241">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0b3c7-1242">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0b3c7-1243">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0b3c7-1244">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0b3c7-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0b3c7-1246">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0b3c7-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0b3c7-1248">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0b3c7-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0b3c7-1250">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0b3c7-1251">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0b3c7-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0b3c7-1253">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0b3c7-1254">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0b3c7-1255">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1256">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1257">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0b3c7-1258">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0b3c7-1259">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0b3c7-1260">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0b3c7-1261">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0b3c7-1262">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0b3c7-1263">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1264">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1265">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0b3c7-1266">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1268">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1269">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-1270">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1271">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1272">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0b3c7-1273">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="0b3c7-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0b3c7-1275">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1276">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1277">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1278">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1279">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0b3c7-1280">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1281">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1282">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-1284">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0b3c7-1285">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1286">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1287">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0b3c7-1288">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0b3c7-1289">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0b3c7-1290">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0b3c7-1291">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0b3c7-1292">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0b3c7-1293">Alterações da falha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1293">Breaking changes</span></span>
    - <span data-ttu-id="0b3c7-1294">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0b3c7-1295">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0b3c7-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="0b3c7-1297">Primeira versão em disponibilidade geral dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0b3c7-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1298">Az.Dns</span></span>
* <span data-ttu-id="0b3c7-1299">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0b3c7-1300">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0b3c7-1301">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="0b3c7-1303">Primeira versão em disponibilidade geral dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0b3c7-1304">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1305">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-1306">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0b3c7-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0b3c7-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0b3c7-1309">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0b3c7-1310">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0b3c7-1311">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0b3c7-1312">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1313">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-1314">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0b3c7-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0b3c7-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0b3c7-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0b3c7-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0b3c7-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0b3c7-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0b3c7-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0b3c7-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0b3c7-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0b3c7-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0b3c7-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0b3c7-1326">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0b3c7-1327">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1328">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1329">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0b3c7-1330">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1330">New cmdlets</span></span>
        - <span data-ttu-id="0b3c7-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="0b3c7-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0b3c7-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0b3c7-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0b3c7-1335">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="0b3c7-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0b3c7-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0b3c7-1338">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0b3c7-1339">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0b3c7-1340">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0b3c7-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="0b3c7-1342">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0b3c7-1343">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0b3c7-1344">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1346">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0b3c7-1347">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0b3c7-1348">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0b3c7-1349">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0b3c7-1350">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0b3c7-1351">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0b3c7-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1352">Az.Relay</span></span>
* <span data-ttu-id="0b3c7-1353">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-1355">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1356">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1357">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0b3c7-1358">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0b3c7-1359">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0b3c7-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="0b3c7-1361">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0b3c7-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0b3c7-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0b3c7-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1365">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1366">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0b3c7-1367">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0b3c7-1368">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-1369">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-1370">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="0b3c7-1371">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0b3c7-1372">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0b3c7-1373">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0b3c7-1374">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0b3c7-1375">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1376">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1377">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1378">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0b3c7-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1379">Az.Batch</span></span>
* <span data-ttu-id="0b3c7-1380">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1381">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-1382">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-1384">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1385">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1386">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0b3c7-1387">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1388">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1389">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-1390">Adicionar SsisProperties se NodeCount não for nulo para o Integration Runtime gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1392">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0b3c7-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1393">Az.EventGrid</span></span>
* <span data-ttu-id="0b3c7-1394">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1395">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-1396">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0b3c7-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1397">Az.HDInsight</span></span>
* <span data-ttu-id="0b3c7-1398">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1399">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-1400">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1401">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-1402">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1403">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0b3c7-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="0b3c7-1405">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0b3c7-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1406">Az.Media</span></span>
* <span data-ttu-id="0b3c7-1407">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1408">Az.Monitor</span></span>
  * <span data-ttu-id="0b3c7-1409">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0b3c7-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0b3c7-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0b3c7-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0b3c7-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0b3c7-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0b3c7-1415">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1416">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1417">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1418">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0b3c7-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="0b3c7-1420">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-1422">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0b3c7-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0b3c7-1424">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1426">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1427">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0b3c7-1428">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0b3c7-1429">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0b3c7-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1430">Az.RedisCache</span></span>
* <span data-ttu-id="0b3c7-1431">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1432">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1433">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1434">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1435">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0b3c7-1436">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1437">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0b3c7-1438">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0b3c7-1439">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0b3c7-1440">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0b3c7-1441">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1442">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1443">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0b3c7-1444">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0b3c7-1445">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0b3c7-1446">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0b3c7-1447">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-1448">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-1449">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="0b3c7-1450">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0b3c7-1451">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0b3c7-1452">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0b3c7-1453">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0b3c7-1454">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1455">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1456">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1457">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0b3c7-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="0b3c7-1459">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0b3c7-1460">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração da falha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1461">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1462">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0b3c7-1463">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0b3c7-1464">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1465">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1466">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0b3c7-1467">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0b3c7-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="0b3c7-1469">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1470">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-1471">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0b3c7-1472">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1473">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1474">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0b3c7-1475">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0b3c7-1476">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0b3c7-1477">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0b3c7-1478">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0b3c7-1479">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1480">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1481">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1482">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1483">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0b3c7-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="0b3c7-1485">Propriedades do Serviço Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0b3c7-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0b3c7-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0b3c7-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0b3c7-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0b3c7-1490">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0b3c7-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0b3c7-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0b3c7-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0b3c7-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0b3c7-1495">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0b3c7-1496">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="0b3c7-1497">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="0b3c7-1498">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0b3c7-1499">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0b3c7-1500">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0b3c7-1501">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0b3c7-1502">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1503">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1504">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1505">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0b3c7-1506">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="0b3c7-1507">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1507">Pre-Post script</span></span>
    * <span data-ttu-id="0b3c7-1508">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1509">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1510">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0b3c7-1511">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1512">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-1513">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1514">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1515">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0b3c7-1516">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1518">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0b3c7-1519">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1520">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1521">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0b3c7-1522">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1523">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1524">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1525">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1526">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0b3c7-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0b3c7-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0b3c7-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0b3c7-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0b3c7-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0b3c7-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1533">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1534">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0b3c7-1535">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1536">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1537">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0b3c7-1538">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1539">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1540">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0b3c7-1541">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0b3c7-1542">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1543">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-1544">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1545">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1546">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1547">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-1548">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0b3c7-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1549">Az.LogicApp</span></span>
* <span data-ttu-id="0b3c7-1550">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1551">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1552">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1554">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0b3c7-1555">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1555">SDK Update</span></span>
* <span data-ttu-id="0b3c7-1556">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0b3c7-1557">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1558">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1559">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0b3c7-1560">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0b3c7-1561">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0b3c7-1562">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0b3c7-1563">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0b3c7-1564">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1565">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1566">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0b3c7-1567">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1568">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1569">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0b3c7-1570">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0b3c7-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="0b3c7-1572">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1573">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1574">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0b3c7-1575">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0b3c7-1576">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-1578">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1579">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1580">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0b3c7-1581">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0b3c7-1582">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0b3c7-1583">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1585">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0b3c7-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1586">Az.EventHub</span></span>
* <span data-ttu-id="0b3c7-1587">Adição da nova propriedade booliana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1588">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-1589">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0b3c7-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1590">Az.LogicApp</span></span>
* <span data-ttu-id="0b3c7-1591">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0b3c7-1592">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0b3c7-1593">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0b3c7-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0b3c7-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0b3c7-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0b3c7-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0b3c7-1598">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0b3c7-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0b3c7-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0b3c7-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0b3c7-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0b3c7-1603">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0b3c7-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1604">Az.Monitor</span></span>
* <span data-ttu-id="0b3c7-1605">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1606">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1607">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="0b3c7-1609">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0b3c7-1610">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0b3c7-1611">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1612">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1613">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0b3c7-1614">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0b3c7-1615">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0b3c7-1616">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1617">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1618">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0b3c7-1619">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1620">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1621">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0b3c7-1622">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1623">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1624">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0b3c7-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="0b3c7-1626">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1627">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1628">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0b3c7-1629">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0b3c7-1630">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="0b3c7-1632">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1633">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1634">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0b3c7-1635">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0b3c7-1636">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0b3c7-1637">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1638">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1639">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0b3c7-1640">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0b3c7-1641">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0b3c7-1642">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1643">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1644">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0b3c7-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="0b3c7-1646">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="0b3c7-1648">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0b3c7-1649">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1650">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1651">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0b3c7-1652">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0b3c7-1653">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0b3c7-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1654">Az.Aks</span></span>
* <span data-ttu-id="0b3c7-1655">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0b3c7-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1656">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1657">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0b3c7-1658">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0b3c7-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1659">Az.Cdn</span></span>
* <span data-ttu-id="0b3c7-1660">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1661">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1662">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0b3c7-1663">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0b3c7-1664">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0b3c7-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0b3c7-1666">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0b3c7-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1667">Az.DataFactory</span></span>
* <span data-ttu-id="0b3c7-1668">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1670">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0b3c7-1671">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0b3c7-1672">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1673">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-1674">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1675">Az.KeyVault</span></span>
* <span data-ttu-id="0b3c7-1676">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1677">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1678">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1679">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1680">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0b3c7-1681">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0b3c7-1682">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0b3c7-1683">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0b3c7-1684">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0b3c7-1685">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0b3c7-1686">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-1688">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0b3c7-1689">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1689">Fix some error messages.</span></span>
* <span data-ttu-id="0b3c7-1690">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0b3c7-1691">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0b3c7-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1692">Az.SignalR</span></span>
* <span data-ttu-id="0b3c7-1693">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1694">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1695">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0b3c7-1696">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0b3c7-1697">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0b3c7-1698">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1699">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1700">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0b3c7-1701">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0b3c7-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0b3c7-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0b3c7-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="0b3c7-1705">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1706">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1707">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0b3c7-1708">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0b3c7-1709">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0b3c7-1710">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1711">Az.Accounts</span></span>
* <span data-ttu-id="0b3c7-1712">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1713">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1714">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0b3c7-1715">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0b3c7-1716">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1718">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0b3c7-1719">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0b3c7-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1720">Az.EventGrid</span></span>
* <span data-ttu-id="0b3c7-1721">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0b3c7-1722">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0b3c7-1723">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0b3c7-1724">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0b3c7-1725">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0b3c7-1726">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0b3c7-1727">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0b3c7-1728">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0b3c7-1729">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0b3c7-1730">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="0b3c7-1731">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0b3c7-1732">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0b3c7-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1733">Az.IotHub</span></span>
* <span data-ttu-id="0b3c7-1734">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0b3c7-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1735">Az.LogicApp</span></span>
* <span data-ttu-id="0b3c7-1736">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1737">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1738">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0b3c7-1739">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0b3c7-1740">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0b3c7-1741">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0b3c7-1742">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0b3c7-1743">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0b3c7-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1744">Az.SignalR</span></span>
* <span data-ttu-id="0b3c7-1745">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1746">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1747">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0b3c7-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1748">Az.Storage</span></span>
* <span data-ttu-id="0b3c7-1749">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0b3c7-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="0b3c7-1751">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0b3c7-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1753">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-1754">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0b3c7-1755">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0b3c7-1756">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0b3c7-1757">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1757">General</span></span>

- <span data-ttu-id="0b3c7-1758">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="0b3c7-1759">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1759">Online help for each module</span></span>
- <span data-ttu-id="0b3c7-1760">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0b3c7-1761">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0b3c7-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1762">Az.Accounts</span></span>
- <span data-ttu-id="0b3c7-1763">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="0b3c7-1764">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="0b3c7-1766">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1766">Fixes for #7002</span></span>
- <span data-ttu-id="0b3c7-1767">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0b3c7-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1768">Az.Batch</span></span>
- <span data-ttu-id="0b3c7-1769">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0b3c7-1770">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0b3c7-1771">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0b3c7-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1772">Az.Billing</span></span>
- <span data-ttu-id="0b3c7-1773">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0b3c7-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="0b3c7-1775">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0b3c7-1776">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0b3c7-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="0b3c7-1778">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0b3c7-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0b3c7-1780">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="0b3c7-1782">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0b3c7-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1783">Az.Monitor</span></span>
- <span data-ttu-id="0b3c7-1784">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0b3c7-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1785">Az.KeyVault</span></span>
- <span data-ttu-id="0b3c7-1786">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0b3c7-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="0b3c7-1788">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0b3c7-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1789">Az.Media</span></span>
- <span data-ttu-id="0b3c7-1790">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1791">Az.Network</span></span>
<span data-ttu-id="0b3c7-1792">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0b3c7-1793">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="0b3c7-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0b3c7-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0b3c7-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0b3c7-1802">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0b3c7-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0b3c7-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0b3c7-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0b3c7-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0b3c7-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0b3c7-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0b3c7-1809">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0b3c7-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0b3c7-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0b3c7-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0b3c7-1813">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0b3c7-1814">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0b3c7-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="0b3c7-1816">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0b3c7-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1817">Az.Profile</span></span>
- <span data-ttu-id="0b3c7-1818">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="0b3c7-1820">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0b3c7-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1821">Az.Resources</span></span>
- <span data-ttu-id="0b3c7-1822">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="0b3c7-1824">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0b3c7-1825">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0b3c7-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="0b3c7-1827">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0b3c7-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1828">Az.Sql</span></span>
- <span data-ttu-id="0b3c7-1829">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0b3c7-1830">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0b3c7-1831">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0b3c7-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1832">Az.Storage</span></span>
- <span data-ttu-id="0b3c7-1833">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1834">Az.Websites</span></span>
- <span data-ttu-id="0b3c7-1835">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0b3c7-1836">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0b3c7-1837">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1837">General</span></span>

* <span data-ttu-id="0b3c7-1838">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0b3c7-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1839">Az.Compute</span></span>

* <span data-ttu-id="0b3c7-1840">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="0b3c7-1842">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0b3c7-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="0b3c7-1844">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="0b3c7-1845">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0b3c7-1846">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0b3c7-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="0b3c7-1848">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0b3c7-1849">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0b3c7-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1850">Az.Resources</span></span>

* <span data-ttu-id="0b3c7-1851">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0b3c7-1852">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0b3c7-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1853">Az.Sql</span></span>

* <span data-ttu-id="0b3c7-1854">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0b3c7-1855">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0b3c7-1856">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0b3c7-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1857">Az.Storage</span></span>

* <span data-ttu-id="0b3c7-1858">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0b3c7-1859">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0b3c7-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0b3c7-1861">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="0b3c7-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0b3c7-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0b3c7-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1864">Az.Websites</span></span>

* <span data-ttu-id="0b3c7-1865">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0b3c7-1866">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0b3c7-1867">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0b3c7-1868">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0b3c7-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="0b3c7-1870">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0b3c7-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1871">Az.Automation</span></span>
* <span data-ttu-id="0b3c7-1872">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0b3c7-1873">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0b3c7-1874">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0b3c7-1875">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0b3c7-1876">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0b3c7-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1877">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1878">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0b3c7-1879">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0b3c7-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="0b3c7-1881">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0b3c7-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0b3c7-1883">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1884">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1885">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0b3c7-1886">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0b3c7-1887">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0b3c7-1888">Corrigir problemas com o uso de memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0b3c7-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0b3c7-1890">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0b3c7-1891">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0b3c7-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0b3c7-1893">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0b3c7-1894">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0b3c7-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1895">Az.Relay</span></span>
* <span data-ttu-id="0b3c7-1896">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0b3c7-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1897">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1898">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0b3c7-1899">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0b3c7-1900">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-1902">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0b3c7-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1903">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-1904">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0b3c7-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0b3c7-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0b3c7-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0b3c7-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0b3c7-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0b3c7-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0b3c7-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0b3c7-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0b3c7-1913">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0b3c7-1914">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0b3c7-1915">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0b3c7-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0b3c7-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0b3c7-1918">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0b3c7-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0b3c7-1920">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0b3c7-1921">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0b3c7-1922">Geral</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1922">General</span></span>
* <span data-ttu-id="0b3c7-1923">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0b3c7-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1924">Az.Profile</span></span>
* <span data-ttu-id="0b3c7-1925">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0b3c7-1926">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0b3c7-1927">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0b3c7-1928">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0b3c7-1929">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0b3c7-1930">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0b3c7-1931">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-1933">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1934">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1935">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0b3c7-1936">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0b3c7-1937">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1939">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0b3c7-1940">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0b3c7-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1941">Az.Insights</span></span>
* <span data-ttu-id="0b3c7-1942">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0b3c7-1943">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0b3c7-1944">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0b3c7-1945">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1946">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1947">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0b3c7-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0b3c7-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0b3c7-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0b3c7-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0b3c7-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0b3c7-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0b3c7-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="0b3c7-1955">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1956">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1957">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0b3c7-1958">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0b3c7-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="0b3c7-1960">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0b3c7-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="0b3c7-1962">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0b3c7-1963">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0b3c7-1964">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0b3c7-1965">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0b3c7-1966">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0b3c7-1967">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0b3c7-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1968">Az.Profile</span></span>
* <span data-ttu-id="0b3c7-1969">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0b3c7-1970">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1971">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1972">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0b3c7-1973">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0b3c7-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="0b3c7-1975">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0b3c7-1976">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0b3c7-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0b3c7-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0b3c7-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1980">Az.Network</span></span>
* <span data-ttu-id="0b3c7-1981">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0b3c7-1982">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1983">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-1984">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0b3c7-1985">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0b3c7-1986">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0b3c7-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1987">Azure.Storage</span></span>
* <span data-ttu-id="0b3c7-1988">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0b3c7-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0b3c7-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0b3c7-1991">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0b3c7-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0b3c7-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="0b3c7-1994">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0b3c7-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1995">Az.Compute</span></span>
* <span data-ttu-id="0b3c7-1996">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0b3c7-1997">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0b3c7-1998">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0b3c7-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b3c7-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0b3c7-2000">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0b3c7-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2001">Az.Network</span></span>
* <span data-ttu-id="0b3c7-2002">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0b3c7-2003">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2003">new cmdlets added</span></span>
    - <span data-ttu-id="0b3c7-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0b3c7-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0b3c7-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0b3c7-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0b3c7-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0b3c7-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0b3c7-2010">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0b3c7-2011">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0b3c7-2012">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0b3c7-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2013">Az.RedisCache</span></span>
* <span data-ttu-id="0b3c7-2014">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0b3c7-2015">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0b3c7-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2016">Az.Resources</span></span>
* <span data-ttu-id="0b3c7-2017">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0b3c7-2018">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0b3c7-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2019">Az.Sql</span></span>
* <span data-ttu-id="0b3c7-2020">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0b3c7-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2021">Az.Websites</span></span>
* <span data-ttu-id="0b3c7-2022">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0b3c7-2023">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0b3c7-2024">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0b3c7-2025">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="0b3c7-2025">Initial Release</span></span>
