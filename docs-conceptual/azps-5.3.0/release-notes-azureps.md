---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 613ef1e104cf825c32f50fd012132d1dde91a45c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893460"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="4983e-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4983e-103">Azure PowerShell release notes</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="4983e-104">5.3.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-104">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-105">Az.Accounts</span></span>
* <span data-ttu-id="4983e-106">Foi corrigido o problema em que o proxy http não é respeitado no Windows PowerShell [n. 13647]</span><span class="sxs-lookup"><span data-stu-id="4983e-106">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="4983e-107">Foi aprimorado o log de depuração de operações de execução prolongada em módulos gerados</span><span class="sxs-lookup"><span data-stu-id="4983e-107">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-108">Az.Automation</span></span>
* <span data-ttu-id="4983e-109">Foi corrigido o problema em que os parâmetros de 'Start-AzAutomationRunbook' não podem converter a cadeia de caracteres encapsulada de PSObject em cadeia de caracteres JSON [#13240]</span><span class="sxs-lookup"><span data-stu-id="4983e-109">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="4983e-110">Foi corrigido o preenchedor de localização para o cmdlet New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="4983e-110">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-111">Az.Compute</span></span>
* <span data-ttu-id="4983e-112">Novo parâmetro 'VM' no novo conjunto de parâmetros 'VMParameterSet' adicionado aos cmdlets 'Get-AzVMDscExtensionStatus' e 'Get-AzVMDscExtension'.</span><span class="sxs-lookup"><span data-stu-id="4983e-112">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="4983e-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="4983e-113">Az.Databricks</span></span>
* <span data-ttu-id="4983e-114">Foi corrigido um problema que fazia com que 'New-AzDatabricksVNetPeering' fosse retornado antes de ser totalmente provisionado (https://github.com/Azure/autorest.powershell/issues/610) )</span><span class="sxs-lookup"><span data-stu-id="4983e-114">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-115">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-116">Foi corrigido o problema do comando ' Invoke-AzDataFactoryV2Pipeline' para SupportsShouldProcess</span><span class="sxs-lookup"><span data-stu-id="4983e-116">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4983e-117">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4983e-117">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4983e-118">Foi adicionada a propriedade StartVMOnConnect ao pool de host.</span><span class="sxs-lookup"><span data-stu-id="4983e-118">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-119">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-119">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-120">Propriedades adicionadas: FQDN e EffectiveDiskEncryptionKeyUrl na classe AzureHDInsightHostInfo.</span><span class="sxs-lookup"><span data-stu-id="4983e-120">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-121">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-122">Foi adicionado um novo parâmetro '-AsPlainText' a 'Get-AzKeyVaultSecret' para retornar diretamente o segredo em texto sem formatação [n. 13630]</span><span class="sxs-lookup"><span data-stu-id="4983e-122">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="4983e-123">Foi adicionado suporte à restauração seletiva de uma chave de um backup completo de HSM gerenciado [n. 13526]</span><span class="sxs-lookup"><span data-stu-id="4983e-123">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="4983e-124">Foram corrigidos alguns problemas secundários [n. 13583] [n. 13584]</span><span class="sxs-lookup"><span data-stu-id="4983e-124">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="4983e-125">Foram adicionados objetos de retorno ausentes de 'Get-Secret' no módulo SecretManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-125">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="4983e-126">Foi corrigido um problema que pode fazer com que o cofre seja criado sem a política de acesso padrão [n. 13687]</span><span class="sxs-lookup"><span data-stu-id="4983e-126">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="4983e-127">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="4983e-127">Az.Kusto</span></span>
* <span data-ttu-id="4983e-128">Versão da API atualizada para a versão de 18/09/2020.</span><span class="sxs-lookup"><span data-stu-id="4983e-128">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-129">Az.Network</span></span>
* <span data-ttu-id="4983e-130">Foi corrigido problema no cmdlet de remoção e emparelhamento e conexão para o cenário ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4983e-130">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="4983e-131">'Remove-AzExpressRouteCircuitPeeringConfig' e 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-131">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-132">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-132">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-133">Foi adicionado suporte para retorno de resultados paginados para Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4983e-133">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-135">Foi habilitado o recurso de exclusão temporária para SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-135">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="4983e-136">Foi corrigida a restauração do SQL AG e removida a verificação do nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4983e-136">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="4983e-137">Foi alterado o formato de nome de contêiner para o item de backup de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-137">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="4983e-138">Foi adicionado suporte de recurso CMK para ações do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="4983e-138">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-139">Az.Resources</span></span>
* <span data-ttu-id="4983e-140">Foi corrigido um problema de exceção de NullRef em 'New-AzureManagedApplication' e 'Set-AzureManagedApplication'.</span><span class="sxs-lookup"><span data-stu-id="4983e-140">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="4983e-141">Foi atualizado o SDK do Azure Resource Manager para uso da versão mais recente em GA da API do DeploymentScripts: 01/10/2020.</span><span class="sxs-lookup"><span data-stu-id="4983e-141">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-142">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-142">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-143">Correção do 'Add-AzServiceFabricNodeType'.</span><span class="sxs-lookup"><span data-stu-id="4983e-143">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="4983e-144">Foi adicionado um tipo de nó ao cluster do Service Fabric antes da criação de um conjunto de dimensionamento de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="4983e-144">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-145">Az.Sql</span></span>
* <span data-ttu-id="4983e-146">Foi corrigida a descrição do parâmetro fixo para o comando 'InstanceFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="4983e-146">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="4983e-147">Foi atualizada a lógica em que schemaName, tableName e columnName estão sendo extraídos da ID dos comandos da Classificação de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-147">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="4983e-148">Foram corrigidos os campos Status e StatusMessage em 'Get-AzSqlDatabaseImportExportStatus' para estar em conformidade com a documentação</span><span class="sxs-lookup"><span data-stu-id="4983e-148">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="4983e-149">Foram adicionados cmdlets de auditoria do DevOps (operações de suporte da Microsoft): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-149">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-150">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-150">Az.Storage</span></span>
* <span data-ttu-id="4983e-151">Foi adicionado suporte à criação/atualização/obtenção/listagem de EncryptionScope de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-151">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="4983e-152">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-152">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="4983e-153">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-153">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="4983e-154">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-154">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="4983e-155">Foi adicionado suporte para a criação de contêineres e o upload de blobs com a configuração Escopo de Criptografia</span><span class="sxs-lookup"><span data-stu-id="4983e-155">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="4983e-156">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-156">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="4983e-157">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-157">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="4983e-158">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-158">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="4983e-159">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="4983e-159">Thanks to our community contributors</span></span>
* <span data-ttu-id="4983e-160">Andreas Wolter (@AndreasWolter), idioma de marketing removido, melhor filtro de exemplo (n. 13671)</span><span class="sxs-lookup"><span data-stu-id="4983e-160">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="4983e-161">Tidjani Belmansour (@BelRarr), Get-AzBillingInvoice.md atualizado (n. 13634)</span><span class="sxs-lookup"><span data-stu-id="4983e-161">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="4983e-162">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="4983e-162">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="4983e-163">Foi corrigido um erro de ortografia (n. 13677)</span><span class="sxs-lookup"><span data-stu-id="4983e-163">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="4983e-164">Atualização do PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="4983e-164">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="4983e-165">@kilobyte97, correção de bug para a exclusão da configuração pelo cmdlet remove (n. 13655)</span><span class="sxs-lookup"><span data-stu-id="4983e-165">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="4983e-166">@kongou-ae, atualização do Set-AzFirewall.md (n. 13727)</span><span class="sxs-lookup"><span data-stu-id="4983e-166">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="4983e-167">@MasterKuat, correção da troca entre título e código na documentação (n. 13666)</span><span class="sxs-lookup"><span data-stu-id="4983e-167">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="4983e-168">NickT (@nukeulis), atualização do Set-AzContext.md (n. 13702)</span><span class="sxs-lookup"><span data-stu-id="4983e-168">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="4983e-169">@PaulHCode, atualização do Start-AzJitNetworkAccessPolicy.md – correção do exemplo para exibir o cmdlet adequado que está sendo demonstrado (n. 13713)</span><span class="sxs-lookup"><span data-stu-id="4983e-169">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="4983e-170">Ryan Borstelmann (@ryanborMSFT), ID da assinatura removida (n. 13715)</span><span class="sxs-lookup"><span data-stu-id="4983e-170">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="4983e-171">Shashikant Shakya (@shshakya), atualização do Set-AzSqlDatabase.md (n. 13674)</span><span class="sxs-lookup"><span data-stu-id="4983e-171">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="4983e-172">Sebastian Olsen (@Spacebjorn), atualização do Get-AzRecoveryServicesBackupItem.md (n. 13719)</span><span class="sxs-lookup"><span data-stu-id="4983e-172">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="4983e-173">5.2.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-173">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-174">Az.Accounts</span></span>
* <span data-ttu-id="4983e-175">Gerenciado para analisar o tempo de ExpiresOn do token bruto se não for possível obter da biblioteca subjacente</span><span class="sxs-lookup"><span data-stu-id="4983e-175">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="4983e-176">Mensagem de aviso aprimorada se a autenticação interativa não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="4983e-176">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-177">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-178">[Alteração da falha] 'New-AzApiManagementProduct', por padrão, não tem limite de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-178">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-179">Az.Compute</span></span>
* <span data-ttu-id="4983e-180">Get-AzVm editado para filtrar por '-Name' antes de verificar a limitação devido a muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="4983e-180">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="4983e-181">Novo cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="4983e-181">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4983e-182">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4983e-182">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4983e-183">Parâmetro 'Name' com suporte e valor da entrada de pipeline para 'Get-AzContainerRegistryUsage' [nº 13605]</span><span class="sxs-lookup"><span data-stu-id="4983e-183">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="4983e-184">Exceções refinadas para 'Connect-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="4983e-184">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-185">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-185">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-186">SDK do .NET do ADF atualizado para a versão 4.13.0</span><span class="sxs-lookup"><span data-stu-id="4983e-186">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4983e-187">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4983e-187">Az.HealthcareApis</span></span>
* <span data-ttu-id="4983e-188">Suporte adicionado para chaves gerenciadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="4983e-188">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-189">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-189">Az.IotHub</span></span>
* <span data-ttu-id="4983e-190">Problema de token SAS corrigido.</span><span class="sxs-lookup"><span data-stu-id="4983e-190">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-191">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-191">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-192">'Todos' com suporte como uma opção quando são definidas políticas de acesso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4983e-192">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="4983e-193">Nova versão com suporte do módulo do SecretManagement [nº 13366]</span><span class="sxs-lookup"><span data-stu-id="4983e-193">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="4983e-194">ByteArray, String, PSCredential e Hashtable com suporte para 'SecretValue' em SecretManagementModule [nº 12190]</span><span class="sxs-lookup"><span data-stu-id="4983e-194">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="4983e-195">[Alteração da falha] Superfície de API de cmdlets recriada com relação ao HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4983e-195">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-196">Az.Monitor</span></span>
* <span data-ttu-id="4983e-197">Parâmetro 'Rule' de 'New-AzAutoscaleProfile' alterado para aceitar lista vazia.</span><span class="sxs-lookup"><span data-stu-id="4983e-197">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="4983e-198">[Nº 12903]</span><span class="sxs-lookup"><span data-stu-id="4983e-198">[#12903]</span></span>
* <span data-ttu-id="4983e-199">Adição de novos cmdlets para dar suporte à criação de configurações de diagnóstico mais flexíveis:</span><span class="sxs-lookup"><span data-stu-id="4983e-199">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="4983e-200">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="4983e-200">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="4983e-201">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="4983e-201">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="4983e-202">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="4983e-202">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-203">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-204">O texto de ajuda e o nome do conjunto de parâmetros foram alterados para o cmdlet 'Restore-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="4983e-204">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-205">Az.Resources</span></span>
* <span data-ttu-id="4983e-206">Suporte ao parâmetro '-Tag' adicionado para 'Set-AzTemplateSpec' e 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="4983e-206">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="4983e-207">Suporte à exibição de marcas adicionado para o formatador padrão para Especificações de Modelo</span><span class="sxs-lookup"><span data-stu-id="4983e-207">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-208">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-208">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-209">Exemplo adicionado para 'Set-AzServiceFabricSetting' com o parâmetro SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="4983e-209">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="4983e-210">Cmdlets relacionados a aplicativos atualizados para alertar que o suporte é apenas para recursos implantados do ARM</span><span class="sxs-lookup"><span data-stu-id="4983e-210">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="4983e-211">Cmdlets de certificado de cluster de 'Add-AzureRmServiceFabricClusterCertificate' e 'Remove-AzureRmServiceFabricClusterCertificate' marcados para substituição</span><span class="sxs-lookup"><span data-stu-id="4983e-211">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-212">Az.Sql</span></span>
* <span data-ttu-id="4983e-213">SecondaryType adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="4983e-213">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="4983e-214">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-214">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="4983e-215">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-215">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="4983e-216">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="4983e-216">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="4983e-217">HighAvailabilityReplicaCount adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="4983e-217">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="4983e-218">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-218">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="4983e-219">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-219">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="4983e-220">ReadReplicaCount tornado um alias de HighAvailabilityReplicaCount no seguinte:</span><span class="sxs-lookup"><span data-stu-id="4983e-220">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="4983e-221">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-221">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="4983e-222">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-222">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-223">Az.Storage</span></span>
* <span data-ttu-id="4983e-224">Upload de arquivos do Azure de até 4 TiB com suporte</span><span class="sxs-lookup"><span data-stu-id="4983e-224">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="4983e-225">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-225">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="4983e-226">Azure.Storage.Blobs atualizado para 12.7.0</span><span class="sxs-lookup"><span data-stu-id="4983e-226">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="4983e-227">Azure.Storage.Files.Shares atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="4983e-227">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="4983e-228">Azure.Storage.Files.DataLake atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="4983e-228">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-229">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-229">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-230">Recurso de política de camadas de sincronização adicionado com política de download e modo de cache local</span><span class="sxs-lookup"><span data-stu-id="4983e-230">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-231">Az.Websites</span></span>
* <span data-ttu-id="4983e-232">Impedir regras de restrição de acesso duplicadas</span><span class="sxs-lookup"><span data-stu-id="4983e-232">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="4983e-233">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="4983e-233">Thanks to our community contributors</span></span>
* <span data-ttu-id="4983e-234">Andrew Dawson (@dawsonar802), por atualizar Get-AzKeyVaultCertificate.md – obter certificado e salvá-lo como seção pfx para trabalhar com o PowerShell Core (nº 13557)</span><span class="sxs-lookup"><span data-stu-id="4983e-234">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="4983e-235">@iviark, por atualizações de APIs de saúde BYOK do Powershell (nº 13518)</span><span class="sxs-lookup"><span data-stu-id="4983e-235">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="4983e-236">John Duckmanton (@johnduckmanton), por corrigir a ortografia de TagPatchOperation (nº 13508)</span><span class="sxs-lookup"><span data-stu-id="4983e-236">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="4983e-237">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="4983e-237">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="4983e-238">Ajuda organizada do Get-AzLogicAppRunHistory (nº 13513)</span><span class="sxs-lookup"><span data-stu-id="4983e-238">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="4983e-239">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="4983e-239">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="4983e-240">Atualizar Update-AzAppConfigurationStore.md (nº 13485)</span><span class="sxs-lookup"><span data-stu-id="4983e-240">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="4983e-241">Atualizar New-AzCosmosDBAccount.md (nº 13490)</span><span class="sxs-lookup"><span data-stu-id="4983e-241">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="4983e-242">@SteppingRazor, New-AzApiManagementProduct: alterar o valor padrão do parâmetro SubscriptionsLimit para nenhum (nº 13457)</span><span class="sxs-lookup"><span data-stu-id="4983e-242">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="4983e-243">Steve Burkett (@SteveBurkettNZ), por corrigir erros de digitação para o parâmetro WorkspaceResourceId no exemplo (nº 13589)</span><span class="sxs-lookup"><span data-stu-id="4983e-243">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="4983e-244">5.1.0 – Novembro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-244">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-245">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-245">Az.Accounts</span></span>
* <span data-ttu-id="4983e-246">Correção de um problema em que a TenantId podia não ser respeitada se 'Connect-AzAccount -DeviceCode' [nº 13477] fosse usado</span><span class="sxs-lookup"><span data-stu-id="4983e-246">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="4983e-247">Adição do novo cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="4983e-247">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="4983e-248">Correção de um problema que ocorria quando o caminho do perfil do usuário estava inacessível</span><span class="sxs-lookup"><span data-stu-id="4983e-248">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="4983e-249">Correção de um problema que causava o erro Write-Object durante Connect-AzAccount [nº 13419]</span><span class="sxs-lookup"><span data-stu-id="4983e-249">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="4983e-250">Adição do parâmetro 'ContainerRegistryEndpointSuffix' a: 'Add-AzEnvironment', 'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="4983e-250">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="4983e-251">Suporte à interrupção de logon com o clique em <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="4983e-251">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="4983e-252">Correção de um problema que fazia com que 'Connect-AzAccount -KeyVaultAccessToken' não funcionasse [nº 13127]</span><span class="sxs-lookup"><span data-stu-id="4983e-252">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="4983e-253">Correção da referência nula e da não diferenciação de maiúsculas e minúsculas no método em 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="4983e-253">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-254">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-254">Az.Aks</span></span>
* <span data-ttu-id="4983e-255">Correção do problema em que o usuário não podia usar a entidade de serviço para criar um cluster do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="4983e-255">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="4983e-256">[nº 13012]</span><span class="sxs-lookup"><span data-stu-id="4983e-256">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="4983e-257">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-257">Az.AppConfiguration</span></span>
* <span data-ttu-id="4983e-258">Disponibilidade geral do módulo 'Az.AppConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-258">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-259">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-259">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-260">Aprimoramento da mensagem de erro do comando 'New-AzDataFactoryV2LinkedServiceEncryptedCredential'</span><span class="sxs-lookup"><span data-stu-id="4983e-260">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-261">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-261">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-262">Atualização do SDK do plano de dados do ADLS para 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="4983e-262">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="4983e-263">Alterações: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="4983e-263">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4983e-264">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4983e-264">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4983e-265">Adição de novos cmdlets do Pacote MSIX e atualização de cmdlets de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4983e-265">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-266">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-266">Az.EventHub</span></span>
* <span data-ttu-id="4983e-267">Correção de comandos do cluster EventHub sem marcas</span><span class="sxs-lookup"><span data-stu-id="4983e-267">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="4983e-268">Atualização do texto da Ajuda de PartnerNamespace dos comandos AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-268">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-269">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-269">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-270">Adição dos parâmetros 'ResourceProviderConnection' e 'PrivateLink' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de link privado e saída de retransmissão</span><span class="sxs-lookup"><span data-stu-id="4983e-270">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="4983e-271">Adição do parâmetro 'AmbariDatabase' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de banco de dados personalizado do Ambari</span><span class="sxs-lookup"><span data-stu-id="4983e-271">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="4983e-272">Adição do valor de aceitação de 'AmbariDatabase' ao parâmetro 'MetastoreType' do cmdlet 'Add-AzHDInsightMetastore'</span><span class="sxs-lookup"><span data-stu-id="4983e-272">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-273">Az.IotHub</span></span>
* <span data-ttu-id="4983e-274">Permissão de marcas no cmdlet create do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-274">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-275">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-275">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-276">Suporte à atualização de marcas do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4983e-276">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4983e-277">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4983e-277">Az.LogicApp</span></span>
* <span data-ttu-id="4983e-278">Correção de Get-AzLogicAppRunHistory, que só recuperava a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="4983e-278">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-279">Az.Network</span></span>
* <span data-ttu-id="4983e-280">Atualização do cmdlet indicado abaixo</span><span class="sxs-lookup"><span data-stu-id="4983e-280">Updated below cmdlet</span></span> 
    - <span data-ttu-id="4983e-281">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="4983e-281">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="4983e-282">Adição da propriedade PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4983e-282">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="4983e-283">Adição da propriedade PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="4983e-283">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="4983e-284">Adição de novas propriedades aos cmdlets a seguir para permitir o balanceamento de carga global</span><span class="sxs-lookup"><span data-stu-id="4983e-284">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="4983e-285">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="4983e-285">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="4983e-286">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="4983e-286">Added Sku Tier property</span></span>
    - <span data-ttu-id="4983e-287">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="4983e-287">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="4983e-288">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="4983e-288">Added Sku Tier property</span></span>
    - <span data-ttu-id="4983e-289">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="4983e-289">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="4983e-290">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="4983e-290">Added Sku Tier property</span></span>
    - <span data-ttu-id="4983e-291">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="4983e-291">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="4983e-292">Adição da propriedade LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4983e-292">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="4983e-293">Atualização do planejamento para preterir os avisos dos seguintes cmdlets: –'New-AzVirtualHubRoute'   –'New-AzVirtualHubRouteTable'   –'Add-AzVirtualHubRoute'   –'Add-AzVirtualHubRouteTable'   –'Get-AzVirtualHubRouteTable'   –'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-293">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="4983e-294">Adição do planejamento para preterir os avisos no argumento 'RouteTable' nos seguintes cmdlets: –'New-AzVirtualHub'   –'Set-AzVirtualHub'   –'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4983e-294">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4983e-295">Os argumentos '-MinScaleUnits' e '-MaxScaleUnits' passaram a ser opcionais em 'Set-AzExpressRouteGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-295">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="4983e-296">Adição de novos cmdlets para dar suporte à autenticação mútua e aos perfis SSL no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-296">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="4983e-297">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-297">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="4983e-298">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-298">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="4983e-299">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-299">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="4983e-300">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-300">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="4983e-301">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-301">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="4983e-302">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-302">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="4983e-303">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-303">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="4983e-304">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-304">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="4983e-305">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-305">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="4983e-306">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-306">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="4983e-307">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-307">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="4983e-308">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-308">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="4983e-309">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-309">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="4983e-310">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-310">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="4983e-311">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-311">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="4983e-312">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-312">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="4983e-313">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-313">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-314">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-314">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-315">A especificação do BackupTime da política está em UTC.</span><span class="sxs-lookup"><span data-stu-id="4983e-315">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="4983e-316">Modificação do aviso de alteração da falha no cmdlet Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="4983e-316">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="4983e-317">Atualização do texto da Ajuda do script de exemplo para o cmdlet Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4983e-317">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-318">Az.Resources</span></span>
* <span data-ttu-id="4983e-319">Correção de um problema em que What-If mostrava dois escopos de grupo de recursos com usos diferentes de maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="4983e-319">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="4983e-320">Atualização de 'Export-AzResourceGroup' para uso do SDK.</span><span class="sxs-lookup"><span data-stu-id="4983e-320">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="4983e-321">Adição de informações de cultura aos métodos de análise</span><span class="sxs-lookup"><span data-stu-id="4983e-321">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-322">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-322">Az.Sql</span></span>
* <span data-ttu-id="4983e-323">Correção de problemas em que Set-AzSqlDatabaseAudit não dava suporte ao banco de dados de Hiperescala e em que não era possível determinar a edição do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4983e-323">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="4983e-324">Adição de MaintenanceConfigurationId a 'New-AzSqlInstance' e 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="4983e-324">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="4983e-325">Correção de um bug em GetAzureSqlDatabaseReplicationLink.cs, em que o parâmetro PartnerServerName era verificado por valor em vez de chave</span><span class="sxs-lookup"><span data-stu-id="4983e-325">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-326">Az.Websites</span></span>
* <span data-ttu-id="4983e-327">Adição de suporte para novos recursos de restrição de acesso: ServiceTag, multi-ip e http-headers</span><span class="sxs-lookup"><span data-stu-id="4983e-327">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="4983e-328">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="4983e-328">Thanks to our community contributors</span></span>
* <span data-ttu-id="4983e-329">John Q. Martin (@johnmart82) – Adição de informações de pré-requisitos do firewall (nº 13385)</span><span class="sxs-lookup"><span data-stu-id="4983e-329">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="4983e-330">Manikandan Duraisamy (@madurais-msft) – Correção do argumento PublicSubnetName (nº 13417)</span><span class="sxs-lookup"><span data-stu-id="4983e-330">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="4983e-331">@mahortas – Atualização dos valores do parâmetro -HostNames (nº 13349)</span><span class="sxs-lookup"><span data-stu-id="4983e-331">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="4983e-332">@MariachiForHire – Adição de valores compatíveis com TrafficAnalyticsInterval (nº 13304)</span><span class="sxs-lookup"><span data-stu-id="4983e-332">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="4983e-333">Michael James (@mikejwhat) – permissão para que Get-AzLogicAppRunHistory retorne mais de 30 entradas (nº 13393)</span><span class="sxs-lookup"><span data-stu-id="4983e-333">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="4983e-334">Shashikant Shakya (@shshakya) – Atualização de Restore-AzSqlInstanceDatabase.md (nº 13404)</span><span class="sxs-lookup"><span data-stu-id="4983e-334">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="4983e-335">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-335">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-336">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-336">Az.Accounts</span></span>
* <span data-ttu-id="4983e-337">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-337">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="4983e-338">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4983e-338">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-339">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-339">Az.Aks</span></span>
* <span data-ttu-id="4983e-340">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="4983e-340">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="4983e-341">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="4983e-341">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="4983e-342">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="4983e-342">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="4983e-343">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="4983e-343">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="4983e-344">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4983e-344">Az.Billing</span></span>
* <span data-ttu-id="4983e-345">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-345">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="4983e-346">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-346">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="4983e-347">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="4983e-347">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="4983e-348">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="4983e-348">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="4983e-349">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="4983e-349">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-350">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-350">Az.Cdn</span></span>
* <span data-ttu-id="4983e-351">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="4983e-351">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-352">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-352">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-353">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="4983e-353">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-354">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-354">Az.Compute</span></span>
* <span data-ttu-id="4983e-355">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="4983e-355">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="4983e-356">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="4983e-356">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="4983e-357">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="4983e-357">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="4983e-358">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="4983e-358">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="4983e-359">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="4983e-359">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="4983e-360">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4983e-360">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4983e-361">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="4983e-361">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="4983e-362">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="4983e-362">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="4983e-363">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-363">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="4983e-364">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="4983e-364">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="4983e-365">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="4983e-365">Az.Databricks</span></span>
* <span data-ttu-id="4983e-366">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="4983e-366">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-367">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-367">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-368">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="4983e-368">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="4983e-369">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="4983e-369">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="4983e-370">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="4983e-370">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4983e-371">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4983e-371">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4983e-372">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4983e-372">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="4983e-373">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="4983e-373">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="4983e-374">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="4983e-374">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="4983e-375">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="4983e-375">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4983e-376">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-376">Az.Functions</span></span>
* <span data-ttu-id="4983e-377">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="4983e-377">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="4983e-378">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="4983e-378">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="4983e-379">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="4983e-379">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="4983e-380">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="4983e-380">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="4983e-381">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="4983e-381">[#12728]</span></span>
  - <span data-ttu-id="4983e-382">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="4983e-382">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="4983e-383">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4983e-383">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="4983e-384">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4983e-384">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="4983e-385">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4983e-385">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-386">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-386">Az.HDInsight</span></span>
 * <span data-ttu-id="4983e-387">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="4983e-387">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="4983e-388">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="4983e-388">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="4983e-389">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-389">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="4983e-390">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="4983e-390">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="4983e-391">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="4983e-391">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="4983e-392">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="4983e-392">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="4983e-393">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="4983e-393">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="4983e-394">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-394">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="4983e-395">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="4983e-395">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="4983e-396">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="4983e-396">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="4983e-397">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="4983e-397">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="4983e-398">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-398">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="4983e-399">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="4983e-399">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="4983e-400">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="4983e-400">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="4983e-401">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="4983e-401">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="4983e-402">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="4983e-402">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="4983e-403">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="4983e-403">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="4983e-404">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="4983e-404">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="4983e-405">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="4983e-405">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="4983e-406">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="4983e-406">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-407">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-407">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-408">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="4983e-408">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="4983e-409">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="4983e-409">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="4983e-410">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="4983e-410">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="4983e-411">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="4983e-411">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="4983e-412">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="4983e-412">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4983e-413">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4983e-413">Az.ManagedServices</span></span>
* <span data-ttu-id="4983e-414">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="4983e-414">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-415">Az.Network</span></span>
* <span data-ttu-id="4983e-416">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="4983e-416">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="4983e-417">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-417">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="4983e-418">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="4983e-418">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="4983e-419">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="4983e-419">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="4983e-420">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4983e-420">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="4983e-421">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="4983e-421">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="4983e-422">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="4983e-422">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="4983e-423">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="4983e-423">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="4983e-424">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="4983e-424">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="4983e-425">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="4983e-425">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="4983e-426">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="4983e-426">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="4983e-427">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="4983e-427">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="4983e-428">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="4983e-428">Added parameter '-Type'</span></span>
    - <span data-ttu-id="4983e-429">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="4983e-429">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="4983e-430">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="4983e-430">Added parameter '-Scope'</span></span>
* <span data-ttu-id="4983e-431">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="4983e-431">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-432">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-433">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="4983e-433">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="4983e-434">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="4983e-434">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-435">Az.Resources</span></span>
* <span data-ttu-id="4983e-436">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="4983e-436">Fixed parsing bug</span></span>
* <span data-ttu-id="4983e-437">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="4983e-437">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="4983e-438">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="4983e-438">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="4983e-439">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="4983e-439">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="4983e-440">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-440">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="4983e-441">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="4983e-441">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="4983e-442">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="4983e-442">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="4983e-443">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="4983e-443">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="4983e-444">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="4983e-444">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-445">Az.Sql</span></span>
* <span data-ttu-id="4983e-446">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="4983e-446">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="4983e-447">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="4983e-447">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="4983e-448">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="4983e-448">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="4983e-449">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-449">Az.Storage</span></span>
* <span data-ttu-id="4983e-450">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="4983e-450">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="4983e-451">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-451">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-452">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-452">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-453">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-453">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="4983e-454">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-454">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4983e-455">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="4983e-455">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="4983e-456">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-456">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="4983e-457">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-457">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="4983e-458">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="4983e-458">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="4983e-459">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-459">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="4983e-460">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="4983e-460">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="4983e-461">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-461">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="4983e-462">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-462">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="4983e-463">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="4983e-463">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="4983e-464">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="4983e-464">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="4983e-465">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="4983e-465">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="4983e-466">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="4983e-466">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="4983e-467">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="4983e-467">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="4983e-468">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-468">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="4983e-469">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-469">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="4983e-470">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="4983e-470">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="4983e-471">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-471">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="4983e-472">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-472">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="4983e-473">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="4983e-473">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="4983e-474">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-474">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-475">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-475">Az.Websites</span></span>
* <span data-ttu-id="4983e-476">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="4983e-476">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="4983e-477">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="4983e-477">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="4983e-478">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="4983e-478">Thanks to our community contributors</span></span>
* <span data-ttu-id="4983e-479">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="4983e-479">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="4983e-480">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="4983e-480">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="4983e-481">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="4983e-481">(#13249)</span></span>
* <span data-ttu-id="4983e-482">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="4983e-482">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="4983e-483">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="4983e-483">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="4983e-484">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="4983e-484">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="4983e-485">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="4983e-485">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="4983e-486">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="4983e-486">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="4983e-487">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="4983e-487">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="4983e-488">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="4983e-488">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="4983e-489">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="4983e-489">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="4983e-490">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="4983e-490">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="4983e-491">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-491">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-492">Az.Accounts</span></span>
* <span data-ttu-id="4983e-493">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="4983e-493">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-494">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-494">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-495">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="4983e-495">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="4983e-496">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-496">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-497">Az.Compute</span></span>
* <span data-ttu-id="4983e-498">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="4983e-498">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="4983e-499">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="4983e-499">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="4983e-500">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="4983e-500">Az.Databricks</span></span>
* <span data-ttu-id="4983e-501">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="4983e-501">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="4983e-502">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-502">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-503">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-503">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-504">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="4983e-504">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-505">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-505">Az.EventHub</span></span>
* <span data-ttu-id="4983e-506">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-506">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-507">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-507">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-508">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="4983e-508">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="4983e-509">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="4983e-509">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="4983e-510">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-510">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="4983e-511">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="4983e-511">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="4983e-512">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-512">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="4983e-513">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="4983e-513">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-514">Az.IotHub</span></span>
* <span data-ttu-id="4983e-515">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="4983e-515">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-516">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-516">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-517">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="4983e-517">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4983e-518">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4983e-518">Az.ManagedServices</span></span>
* <span data-ttu-id="4983e-519">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="4983e-519">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-520">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-520">Az.Monitor</span></span>
* <span data-ttu-id="4983e-521">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="4983e-521">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="4983e-522">[#12889]</span><span class="sxs-lookup"><span data-stu-id="4983e-522">[#12889]</span></span>
* <span data-ttu-id="4983e-523">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="4983e-523">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="4983e-524">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="4983e-524">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-525">Az.Network</span></span>
* <span data-ttu-id="4983e-526">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="4983e-526">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="4983e-527">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-527">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-529">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4983e-529">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4983e-530">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4983e-530">Az.RedisCache</span></span>
* <span data-ttu-id="4983e-531">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="4983e-531">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-532">Az.Sql</span></span>
* <span data-ttu-id="4983e-533">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="4983e-533">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="4983e-534">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-534">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="4983e-535">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="4983e-535">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="4983e-536">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="4983e-536">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="4983e-537">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-537">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="4983e-538">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="4983e-538">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-539">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-539">Az.Storage</span></span>
* <span data-ttu-id="4983e-540">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-540">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="4983e-541">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-541">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="4983e-542">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-542">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="4983e-543">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="4983e-543">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="4983e-544">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-544">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="4983e-545">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="4983e-545">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="4983e-546">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-546">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="4983e-547">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="4983e-547">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="4983e-548">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-548">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="4983e-549">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-549">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="4983e-550">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-550">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-551">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-551">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-552">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-552">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4983e-553">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="4983e-553">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="4983e-554">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="4983e-554">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="4983e-555">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-555">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-556">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-556">Az.Accounts</span></span>
* <span data-ttu-id="4983e-557">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="4983e-557">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="4983e-558">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="4983e-558">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-559">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-559">Az.Aks</span></span>
* <span data-ttu-id="4983e-560">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="4983e-560">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="4983e-561">[#12372]</span><span class="sxs-lookup"><span data-stu-id="4983e-561">[#12372]</span></span>
* <span data-ttu-id="4983e-562">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-562">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="4983e-563">[#11239]</span><span class="sxs-lookup"><span data-stu-id="4983e-563">[#11239]</span></span>
* <span data-ttu-id="4983e-564">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="4983e-564">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="4983e-565">[#11239]</span><span class="sxs-lookup"><span data-stu-id="4983e-565">[#11239]</span></span>
* <span data-ttu-id="4983e-566">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-566">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="4983e-567">[#12371]</span><span class="sxs-lookup"><span data-stu-id="4983e-567">[#12371]</span></span>
* <span data-ttu-id="4983e-568">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="4983e-568">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-569">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-569">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-570">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="4983e-570">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-571">Az.Compute</span></span>
* <span data-ttu-id="4983e-572">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-572">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="4983e-573">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="4983e-573">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="4983e-574">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-574">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="4983e-575">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-575">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="4983e-576">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4983e-576">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="4983e-577">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="4983e-577">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="4983e-578">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="4983e-578">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="4983e-579">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-579">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="4983e-580">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-580">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="4983e-581">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="4983e-581">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-582">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-582">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-583">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="4983e-583">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-584">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-584">Az.EventHub</span></span>
* <span data-ttu-id="4983e-585">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="4983e-585">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="4983e-586">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="4983e-586">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4983e-587">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-587">Az.Functions</span></span>
* <span data-ttu-id="4983e-588">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="4983e-588">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="4983e-589">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="4983e-589">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="4983e-590">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="4983e-590">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-591">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-591">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-592">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="4983e-592">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="4983e-593">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-593">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="4983e-594">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="4983e-594">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="4983e-595">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-595">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="4983e-596">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-596">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="4983e-597">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-597">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="4983e-598">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-598">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="4983e-599">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="4983e-599">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-600">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-600">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-601">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="4983e-601">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="4983e-602">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="4983e-602">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="4983e-603">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="4983e-603">Az.Kusto</span></span>
* <span data-ttu-id="4983e-604">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="4983e-604">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-605">Az.Network</span></span>
* <span data-ttu-id="4983e-606">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-606">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="4983e-607">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="4983e-607">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="4983e-608">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="4983e-608">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="4983e-609">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="4983e-609">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="4983e-610">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="4983e-610">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="4983e-611">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-611">Added subscription level parameter set</span></span>
    - <span data-ttu-id="4983e-612">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="4983e-612">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="4983e-613">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="4983e-613">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="4983e-614">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="4983e-614">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="4983e-615">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="4983e-615">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="4983e-616">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-616">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="4983e-617">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="4983e-617">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="4983e-618">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4983e-618">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="4983e-619">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4983e-619">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="4983e-620">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-620">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="4983e-621">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="4983e-621">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="4983e-622">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4983e-622">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="4983e-623">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4983e-623">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="4983e-624">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4983e-624">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="4983e-625">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4983e-625">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="4983e-626">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="4983e-626">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="4983e-627">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="4983e-627">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="4983e-628">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-628">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="4983e-629">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="4983e-629">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-630">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-631">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="4983e-631">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-632">Az.Resources</span></span>
* <span data-ttu-id="4983e-633">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4983e-633">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="4983e-634">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="4983e-634">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="4983e-635">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="4983e-635">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="4983e-636">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="4983e-636">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-638">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="4983e-638">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="4983e-639">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-639">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="4983e-640">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-640">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="4983e-641">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-641">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="4983e-642">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-642">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="4983e-643">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-643">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="4983e-644">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-644">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="4983e-645">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="4983e-645">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="4983e-646">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="4983e-646">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="4983e-647">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="4983e-647">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="4983e-648">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="4983e-648">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="4983e-649">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-649">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="4983e-650">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="4983e-650">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="4983e-651">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-651">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="4983e-652">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="4983e-652">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="4983e-653">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="4983e-653">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-654">Az.Sql</span></span>
* <span data-ttu-id="4983e-655">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="4983e-655">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="4983e-656">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-656">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-657">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-657">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-658">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="4983e-658">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="4983e-659">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-659">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="4983e-660">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="4983e-660">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="4983e-661">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="4983e-661">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="4983e-662">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="4983e-662">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="4983e-663">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="4983e-663">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="4983e-664">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-664">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-665">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-665">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-666">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-666">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-667">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="4983e-667">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="4983e-668">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-668">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="4983e-669">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="4983e-669">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="4983e-670">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-670">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="4983e-671">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="4983e-671">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="4983e-672">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="4983e-672">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-673">Az.Storage</span></span>
* <span data-ttu-id="4983e-674">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="4983e-674">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="4983e-675">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="4983e-675">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="4983e-676">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-676">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-677">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-677">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="4983e-678">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="4983e-678">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="4983e-679">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="4983e-679">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="4983e-680">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="4983e-680">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="4983e-681">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-681">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="4983e-682">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="4983e-682">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="4983e-683">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-683">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="4983e-684">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-684">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="4983e-685">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-685">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="4983e-686">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-686">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="4983e-687">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="4983e-687">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="4983e-688">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-688">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="4983e-689">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="4983e-689">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="4983e-690">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="4983e-690">Thanks to our community contributors</span></span>
* <span data-ttu-id="4983e-691">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="4983e-691">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="4983e-692">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="4983e-692">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="4983e-693">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="4983e-693">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="4983e-694">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="4983e-694">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="4983e-695">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="4983e-695">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="4983e-696">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="4983e-696">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="4983e-697">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="4983e-697">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="4983e-698">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="4983e-698">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="4983e-699">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="4983e-699">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="4983e-700">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="4983e-700">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="4983e-701">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="4983e-701">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="4983e-702">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-702">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="4983e-703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-703">Az.Compute</span></span>
* <span data-ttu-id="4983e-704">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="4983e-704">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="4983e-705">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-705">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-706">Az.Accounts</span></span>
* <span data-ttu-id="4983e-707">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="4983e-707">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="4983e-708">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="4983e-708">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-709">Az.Automation</span></span>
* <span data-ttu-id="4983e-710">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="4983e-710">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-711">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-711">Az.Compute</span></span>
* <span data-ttu-id="4983e-712">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="4983e-712">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="4983e-713">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="4983e-713">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="4983e-714">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-714">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="4983e-715">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="4983e-715">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-716">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-717">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="4983e-717">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-718">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-719">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="4983e-719">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-720">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-720">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-721">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="4983e-721">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="4983e-722">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="4983e-722">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4983e-723">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4983e-723">Az.Maintenance</span></span>
* <span data-ttu-id="4983e-724">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-724">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="4983e-725">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-725">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4983e-726">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4983e-726">Az.ManagedServices</span></span>
* <span data-ttu-id="4983e-727">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="4983e-727">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-728">Az.Monitor</span></span>
* <span data-ttu-id="4983e-729">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="4983e-729">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="4983e-730">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="4983e-730">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-731">Az.Resources</span></span>
* <span data-ttu-id="4983e-732">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="4983e-732">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="4983e-733">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="4983e-733">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="4983e-734">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4983e-734">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="4983e-735">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="4983e-735">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="4983e-736">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="4983e-736">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4983e-737">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="4983e-737">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="4983e-738">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="4983e-738">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="4983e-739">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="4983e-739">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4983e-740">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4983e-740">Az.SignalR</span></span>
* <span data-ttu-id="4983e-741">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="4983e-741">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="4983e-742">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="4983e-742">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-743">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-743">Az.Storage</span></span>
* <span data-ttu-id="4983e-744">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="4983e-744">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="4983e-745">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="4983e-745">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="4983e-746">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-746">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="4983e-747">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="4983e-747">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="4983e-748">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="4983e-748">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="4983e-749">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-749">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="4983e-750">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="4983e-750">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="4983e-751">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-751">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="4983e-752">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-752">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="4983e-753">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-753">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="4983e-754">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-754">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4983e-755">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-755">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4983e-756">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-756">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="4983e-757">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-757">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4983e-758">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-758">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="4983e-759">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-759">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-760">Az.Accounts</span></span>
* <span data-ttu-id="4983e-761">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="4983e-761">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="4983e-762">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="4983e-762">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="4983e-763">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="4983e-763">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="4983e-764">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="4983e-764">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="4983e-765">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="4983e-765">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-766">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-766">Az.Aks</span></span>
* <span data-ttu-id="4983e-767">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="4983e-767">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="4983e-768">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="4983e-768">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-769">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-769">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-770">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-770">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-771">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-771">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-772">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4983e-772">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4983e-773">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="4983e-773">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="4983e-774">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-774">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-775">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4983e-775">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4983e-776">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="4983e-776">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="4983e-777">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-777">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-778">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-778">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-779">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4983e-779">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4983e-780">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-780">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4983e-781">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4983e-781">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-782">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-783">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="4983e-783">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-784">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-784">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-785">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="4983e-785">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-786">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-786">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-787">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="4983e-787">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="4983e-788">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-788">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4983e-789">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-789">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4983e-790">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="4983e-790">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="4983e-791">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-791">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4983e-792">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-792">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4983e-793">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-793">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-794">Az.Network</span></span>
* <span data-ttu-id="4983e-795">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-795">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4983e-796">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="4983e-796">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="4983e-797">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="4983e-797">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="4983e-798">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4983e-798">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-799">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-799">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-800">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="4983e-800">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="4983e-801">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="4983e-801">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="4983e-802">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4983e-802">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-803">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-804">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-804">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-805">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-805">Az.Resources</span></span>
* <span data-ttu-id="4983e-806">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4983e-806">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="4983e-807">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="4983e-807">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-808">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-808">Az.Sql</span></span>
* <span data-ttu-id="4983e-809">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="4983e-809">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4983e-810">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4983e-810">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-811">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-811">Az.Storage</span></span>
* <span data-ttu-id="4983e-812">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="4983e-812">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="4983e-813">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="4983e-813">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="4983e-814">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-814">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="4983e-815">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="4983e-815">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="4983e-816">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-816">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="4983e-817">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="4983e-817">Supported get single file share usage</span></span>
    - <span data-ttu-id="4983e-818">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-818">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="4983e-819">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-819">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-820">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-820">Az.Accounts</span></span>
* <span data-ttu-id="4983e-821">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-821">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="4983e-822">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="4983e-822">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-823">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-823">Az.Aks</span></span>
* <span data-ttu-id="4983e-824">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="4983e-824">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-825">Az.AnalysisServices</span></span>
* <span data-ttu-id="4983e-826">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4983e-826">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-827">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-827">Az.Automation</span></span>
* <span data-ttu-id="4983e-828">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="4983e-828">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-829">Az.Compute</span></span>
* <span data-ttu-id="4983e-830">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="4983e-830">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-831">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-831">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-832">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4983e-832">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4983e-833">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4983e-833">Az.EventGrid</span></span>
* <span data-ttu-id="4983e-834">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="4983e-834">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="4983e-835">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-835">Added new features:</span></span>
    - <span data-ttu-id="4983e-836">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="4983e-836">Input mapping</span></span>
    - <span data-ttu-id="4983e-837">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="4983e-837">Event Delivery Schema</span></span>
    - <span data-ttu-id="4983e-838">Link Privado</span><span class="sxs-lookup"><span data-stu-id="4983e-838">Private Link</span></span>
    - <span data-ttu-id="4983e-839">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="4983e-839">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="4983e-840">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="4983e-840">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="4983e-841">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="4983e-841">Azure Function As Destination</span></span>
    - <span data-ttu-id="4983e-842">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="4983e-842">WebHook Batching</span></span>
    - <span data-ttu-id="4983e-843">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="4983e-843">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="4983e-844">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="4983e-844">IpFiltering</span></span>
* <span data-ttu-id="4983e-845">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4983e-845">Updated cmdlets:</span></span>
    - <span data-ttu-id="4983e-846">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="4983e-846">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="4983e-847">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="4983e-847">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="4983e-848">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="4983e-848">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="4983e-849">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="4983e-849">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="4983e-850">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="4983e-850">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="4983e-851">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4983e-851">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4983e-852">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="4983e-852">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="4983e-853">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4983e-853">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4983e-854">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4983e-854">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-855">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-855">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-856">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="4983e-856">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="4983e-857">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="4983e-857">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-858">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-858">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-859">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="4983e-859">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-860">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-860">Az.Monitor</span></span>
* <span data-ttu-id="4983e-861">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="4983e-861">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-862">Az.Network</span></span>
* <span data-ttu-id="4983e-863">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="4983e-863">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="4983e-864">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-864">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="4983e-865">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4983e-865">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4983e-866">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4983e-866">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4983e-867">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4983e-867">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4983e-868">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4983e-868">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4983e-869">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-869">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="4983e-870">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-870">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="4983e-871">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4983e-871">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4983e-872">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4983e-872">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4983e-873">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4983e-873">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4983e-874">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4983e-874">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4983e-875">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="4983e-875">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="4983e-876">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-876">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="4983e-877">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4983e-877">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4983e-878">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4983e-878">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4983e-879">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4983e-879">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-881">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4983e-881">Removed project reference to Authentication</span></span>
* <span data-ttu-id="4983e-882">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="4983e-882">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="4983e-883">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="4983e-883">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-884">Az.Resources</span></span>
* <span data-ttu-id="4983e-885">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="4983e-885">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="4983e-886">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-886">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-887">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-887">Az.Sql</span></span>
* <span data-ttu-id="4983e-888">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="4983e-888">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="4983e-889">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-889">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="4983e-890">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="4983e-890">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-891">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-891">Az.Storage</span></span>
* <span data-ttu-id="4983e-892">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-892">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="4983e-893">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-893">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="4983e-894">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-894">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4983e-895">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-895">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-896">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-896">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4983e-897">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4983e-897">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4983e-898">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="4983e-898">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="4983e-899">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4983e-899">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="4983e-900">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="4983e-900">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="4983e-901">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4983e-901">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="4983e-902">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4983e-902">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="4983e-903">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="4983e-903">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="4983e-904">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-904">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4983e-905">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="4983e-905">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="4983e-906">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4983e-906">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="4983e-907">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-907">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4983e-908">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="4983e-908">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-909">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-909">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-910">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="4983e-910">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="4983e-911">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-911">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="4983e-912">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="4983e-912">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="4983e-913">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4983e-913">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-914">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-914">Az.Websites</span></span>
* <span data-ttu-id="4983e-915">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-915">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="4983e-916">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-916">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-917">Az.Accounts</span></span>
* <span data-ttu-id="4983e-918">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="4983e-918">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="4983e-919">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="4983e-919">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="4983e-920">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-920">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="4983e-921">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="4983e-921">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-922">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-922">Az.Aks</span></span>
* <span data-ttu-id="4983e-923">O uso da [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="4983e-923">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-924">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-924">Az.Batch</span></span>
* <span data-ttu-id="4983e-925">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="4983e-925">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="4983e-926">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-926">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-927">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-927">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-928">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="4983e-928">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="4983e-929">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4983e-929">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-930">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-930">Az.Compute</span></span>
* <span data-ttu-id="4983e-931">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4983e-931">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="4983e-932">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4983e-932">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="4983e-933">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="4983e-933">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="4983e-934">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4983e-934">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="4983e-935">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="4983e-935">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-936">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-937">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="4983e-937">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-938">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-938">Az.EventHub</span></span>
* <span data-ttu-id="4983e-939">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="4983e-939">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4983e-940">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-940">Az.Functions</span></span>
* <span data-ttu-id="4983e-941">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="4983e-941">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-942">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-942">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-943">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4983e-943">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4983e-944">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4983e-944">Az.HealthcareApis</span></span>
* <span data-ttu-id="4983e-945">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="4983e-945">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="4983e-946">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4983e-946">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-947">Az.Monitor</span></span>
* <span data-ttu-id="4983e-948">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="4983e-948">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="4983e-949">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="4983e-949">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-950">Az.Network</span></span>
* <span data-ttu-id="4983e-951">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-951">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4983e-952">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-952">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4983e-953">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="4983e-953">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="4983e-954">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4983e-954">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="4983e-955">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="4983e-955">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="4983e-956">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-956">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="4983e-957">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4983e-957">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4983e-958">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4983e-958">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4983e-959">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4983e-959">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4983e-960">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4983e-960">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="4983e-961">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-961">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="4983e-962">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-962">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4983e-963">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="4983e-963">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="4983e-964">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-964">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="4983e-965">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4983e-965">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="4983e-966">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4983e-966">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="4983e-967">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-967">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="4983e-968">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-968">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="4983e-969">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="4983e-969">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="4983e-970">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="4983e-970">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="4983e-971">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4983e-971">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="4983e-972">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="4983e-972">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="4983e-973">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4983e-973">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="4983e-974">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="4983e-974">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="4983e-975">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4983e-975">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4983e-976">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4983e-976">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4983e-977">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="4983e-977">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="4983e-978">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-978">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="4983e-979">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-979">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4983e-980">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-980">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4983e-981">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-981">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4983e-982">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-982">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4983e-983">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-983">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4983e-984">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-984">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="4983e-985">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4983e-985">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="4983e-986">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="4983e-986">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="4983e-987">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-987">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4983e-988">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-988">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4983e-989">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-989">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4983e-990">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-990">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="4983e-991">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4983e-991">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="4983e-992">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-992">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4983e-993">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-993">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4983e-994">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-994">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4983e-995">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-995">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4983e-996">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-996">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="4983e-997">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-997">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="4983e-998">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-998">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="4983e-999">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-999">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-1000">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1000">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-1001">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="4983e-1001">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="4983e-1002">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4983e-1002">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="4983e-1003">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="4983e-1003">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="4983e-1004">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4983e-1004">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4983e-1005">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4983e-1005">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1006">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1006">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1007">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1007">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="4983e-1008">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="4983e-1008">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1009">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1009">Az.Resources</span></span>
* <span data-ttu-id="4983e-1010">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="4983e-1010">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="4983e-1011">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="4983e-1011">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="4983e-1012">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4983e-1012">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="4983e-1013">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1013">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="4983e-1014">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="4983e-1014">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="4983e-1015">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="4983e-1015">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1016">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1016">Az.Sql</span></span>
* <span data-ttu-id="4983e-1017">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4983e-1017">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="4983e-1018">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-1018">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="4983e-1019">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="4983e-1019">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1020">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1020">Az.Storage</span></span>
* <span data-ttu-id="4983e-1021">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="4983e-1021">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="4983e-1022">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1022">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-1023">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1023">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-1024">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1024">Az.Websites</span></span>
* <span data-ttu-id="4983e-1025">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4983e-1025">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4983e-1026">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4983e-1026">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="4983e-1027">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4983e-1027">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="4983e-1028">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4983e-1028">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="4983e-1029">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="4983e-1029">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="4983e-1030">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4983e-1030">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="4983e-1031">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1031">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-1032">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1032">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1033">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="4983e-1033">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-1034">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1034">Az.AnalysisServices</span></span>
* <span data-ttu-id="4983e-1035">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1035">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-1036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-1036">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-1037">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1037">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="4983e-1038">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4983e-1038">Az.Billing</span></span>
* <span data-ttu-id="4983e-1039">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1039">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-1040">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1040">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-1041">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4983e-1041">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1042">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1043">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1043">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="4983e-1044">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="4983e-1044">Az.DataShare</span></span>
* <span data-ttu-id="4983e-1045">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="4983e-1045">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4983e-1046">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4983e-1046">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4983e-1047">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="4983e-1047">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-1048">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1048">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-1049">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1049">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="4983e-1050">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="4983e-1050">Added optional parameters to</span></span> 
    - <span data-ttu-id="4983e-1051">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4983e-1051">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4983e-1052">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4983e-1052">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-1053">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1053">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-1054">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="4983e-1054">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4983e-1055">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4983e-1055">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4983e-1056">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1056">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4983e-1057">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4983e-1057">Az.PrivateDns</span></span>
* <span data-ttu-id="4983e-1058">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4983e-1058">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1060">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="4983e-1060">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="4983e-1061">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4983e-1061">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1062">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1062">Az.Resources</span></span>
* <span data-ttu-id="4983e-1063">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="4983e-1063">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="4983e-1064">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4983e-1064">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="4983e-1065">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="4983e-1065">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="4983e-1066">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4983e-1066">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="4983e-1067">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1067">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1068">Az.Sql</span></span>
* <span data-ttu-id="4983e-1069">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4983e-1069">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4983e-1070">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4983e-1070">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4983e-1071">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4983e-1071">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1072">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1072">Az.Storage</span></span>
* <span data-ttu-id="4983e-1073">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1073">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="4983e-1074">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1074">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4983e-1075">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4983e-1075">Highlights since the last release</span></span>
* <span data-ttu-id="4983e-1076">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4983e-1076">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="4983e-1077">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-1077">General availability of Az.Functions</span></span> 
* <span data-ttu-id="4983e-1078">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-1078">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1079">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1080">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="4983e-1080">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="4983e-1081">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="4983e-1081">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-1082">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-1082">Az.Aks</span></span>
* <span data-ttu-id="4983e-1083">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4983e-1083">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="4983e-1084">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4983e-1084">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="4983e-1085">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="4983e-1085">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-1086">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-1086">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-1087">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="4983e-1087">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="4983e-1088">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="4983e-1088">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="4983e-1089">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1089">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4983e-1090">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4983e-1090">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4983e-1091">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1091">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4983e-1092">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4983e-1092">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="4983e-1093">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1093">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4983e-1094">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4983e-1094">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4983e-1095">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1095">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4983e-1096">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4983e-1096">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4983e-1097">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4983e-1097">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="4983e-1098">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="4983e-1098">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="4983e-1099">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4983e-1099">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="4983e-1100">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-1100">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="4983e-1101">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4983e-1101">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="4983e-1102">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4983e-1102">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4983e-1103">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1103">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4983e-1104">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="4983e-1104">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="4983e-1105">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="4983e-1105">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="4983e-1106">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4983e-1106">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-1107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-1107">Az.Batch</span></span>
* <span data-ttu-id="4983e-1108">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="4983e-1108">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="4983e-1109">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1109">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="4983e-1110">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="4983e-1110">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="4983e-1111">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1111">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="4983e-1112">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1112">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="4983e-1113">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="4983e-1113">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="4983e-1114">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1114">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="4983e-1115">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1115">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="4983e-1116">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1116">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1117">Az.Compute</span></span>
* <span data-ttu-id="4983e-1118">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4983e-1118">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="4983e-1119">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1119">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="4983e-1120">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4983e-1120">Breaking changes</span></span>
    - <span data-ttu-id="4983e-1121">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1121">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="4983e-1122">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1122">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="4983e-1123">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1123">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="4983e-1124">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4983e-1124">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="4983e-1125">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="4983e-1125">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="4983e-1126">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="4983e-1126">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="4983e-1127">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="4983e-1127">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1128">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1129">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1129">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-1130">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-1130">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-1131">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4983e-1131">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4983e-1132">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4983e-1132">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4983e-1133">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="4983e-1133">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="4983e-1134">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="4983e-1134">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4983e-1135">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-1135">Az.Functions</span></span>
* <span data-ttu-id="4983e-1136">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="4983e-1136">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-1137">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-1137">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-1138">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="4983e-1138">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4983e-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4983e-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="4983e-1140">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="4983e-1140">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1141">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1141">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1142">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-1142">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="4983e-1143">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="4983e-1143">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="4983e-1144">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="4983e-1144">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="4983e-1145">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="4983e-1145">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="4983e-1146">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="4983e-1146">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="4983e-1147">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1147">New cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1148">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1148">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4983e-1149">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1149">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4983e-1150">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1150">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4983e-1151">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1151">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="4983e-1152">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="4983e-1152">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="4983e-1153">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1153">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1154">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1155">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="4983e-1155">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="4983e-1156">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4983e-1156">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="4983e-1157">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4983e-1157">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="4983e-1158">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="4983e-1158">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="4983e-1159">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="4983e-1159">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="4983e-1160">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="4983e-1160">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="4983e-1161">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-1161">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1162">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1163">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="4983e-1163">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="4983e-1164">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4983e-1164">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="4983e-1165">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="4983e-1165">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="4983e-1166">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="4983e-1166">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="4983e-1167">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="4983e-1167">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="4983e-1168">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="4983e-1168">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="4983e-1169">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="4983e-1169">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1170">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1170">Az.Network</span></span>
* <span data-ttu-id="4983e-1171">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="4983e-1171">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="4983e-1172">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="4983e-1172">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="4983e-1173">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="4983e-1173">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="4983e-1174">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-1174">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="4983e-1175">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4983e-1175">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="4983e-1176">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1176">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-1177">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4983e-1177">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4983e-1178">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4983e-1178">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4983e-1179">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4983e-1179">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4983e-1180">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4983e-1180">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="4983e-1181">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-1181">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="4983e-1182">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4983e-1182">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="4983e-1183">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="4983e-1183">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="4983e-1184">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4983e-1184">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="4983e-1185">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4983e-1185">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="4983e-1186">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4983e-1186">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="4983e-1187">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="4983e-1187">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="4983e-1188">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-1188">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4983e-1189">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-1189">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4983e-1190">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-1190">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4983e-1191">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-1191">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="4983e-1192">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4983e-1192">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="4983e-1193">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4983e-1193">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="4983e-1194">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-1194">Updated cmdlet:</span></span>
        - <span data-ttu-id="4983e-1195">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4983e-1195">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-1196">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1196">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-1197">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="4983e-1197">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="4983e-1198">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="4983e-1198">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="4983e-1199">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4983e-1199">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="4983e-1200">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4983e-1200">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="4983e-1201">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="4983e-1201">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="4983e-1202">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4983e-1202">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="4983e-1203">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4983e-1203">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="4983e-1204">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="4983e-1204">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1205">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1206">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1206">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="4983e-1207">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="4983e-1207">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="4983e-1208">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="4983e-1208">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="4983e-1209">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1209">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="4983e-1210">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="4983e-1210">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1211">Az.Resources</span></span>
* <span data-ttu-id="4983e-1212">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="4983e-1212">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="4983e-1213">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="4983e-1213">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="4983e-1214">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="4983e-1214">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="4983e-1215">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="4983e-1215">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="4983e-1216">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4983e-1216">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="4983e-1217">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4983e-1217">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="4983e-1218">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="4983e-1218">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="4983e-1219">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="4983e-1219">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4983e-1220">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4983e-1220">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="4983e-1221">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4983e-1221">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="4983e-1222">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4983e-1222">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="4983e-1223">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="4983e-1223">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="4983e-1224">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="4983e-1224">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="4983e-1225">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4983e-1225">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="4983e-1226">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4983e-1226">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="4983e-1227">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="4983e-1227">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="4983e-1228">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1228">'New-AzDeployment'</span></span>
    - <span data-ttu-id="4983e-1229">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1229">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="4983e-1230">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1230">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4983e-1231">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1231">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-1232">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-1232">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-1233">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="4983e-1233">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1234">Az.Sql</span></span>
* <span data-ttu-id="4983e-1235">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="4983e-1235">Enhance performance of:</span></span>
    - <span data-ttu-id="4983e-1236">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4983e-1236">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4983e-1237">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4983e-1237">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4983e-1238">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4983e-1238">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4983e-1239">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4983e-1239">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4983e-1240">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4983e-1240">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4983e-1241">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4983e-1241">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4983e-1242">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4983e-1242">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4983e-1243">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4983e-1243">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="4983e-1244">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-1244">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="4983e-1245">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="4983e-1245">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1246">Az.Storage</span></span>
* <span data-ttu-id="4983e-1247">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1247">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-1248">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="4983e-1248">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="4983e-1249">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1249">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-1250">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="4983e-1250">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="4983e-1251">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4983e-1251">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4983e-1252">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="4983e-1252">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="4983e-1253">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-1253">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="4983e-1254">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-1254">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="4983e-1255">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="4983e-1255">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="4983e-1256">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-1256">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="4983e-1257">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="4983e-1257">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="4983e-1258">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="4983e-1258">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="4983e-1259">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4983e-1259">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="4983e-1260">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-1260">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="4983e-1261">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1261">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4983e-1262">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1262">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-1263">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-1263">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="4983e-1264">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-1264">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="4983e-1265">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-1265">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4983e-1266">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="4983e-1266">Supported failover Storage account</span></span>
    - <span data-ttu-id="4983e-1267">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="4983e-1267">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="4983e-1268">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1268">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="4983e-1269">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-1269">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="4983e-1270">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="4983e-1270">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="4983e-1271">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4983e-1271">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4983e-1272">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4983e-1272">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="4983e-1273">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4983e-1273">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="4983e-1274">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1274">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4983e-1275">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1275">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4983e-1276">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="4983e-1276">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="4983e-1277">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4983e-1277">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4983e-1278">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4983e-1278">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="4983e-1279">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4983e-1279">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4983e-1280">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4983e-1280">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4983e-1281">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-1281">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="4983e-1282">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-1282">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="4983e-1283">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-1283">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="4983e-1284">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4983e-1284">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="4983e-1285">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="4983e-1285">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4983e-1286">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4983e-1286">Az.TrafficManager</span></span>
* <span data-ttu-id="4983e-1287">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="4983e-1287">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-1288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1288">Az.Websites</span></span>
* <span data-ttu-id="4983e-1289">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1289">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="4983e-1290">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1290">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4983e-1291">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4983e-1291">Highlights since the last release</span></span>
* <span data-ttu-id="4983e-1292">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4983e-1292">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1293">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1294">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="4983e-1294">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-1295">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-1295">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-1296">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4983e-1296">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4983e-1297">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="4983e-1297">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-1298">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-1298">Az.Cdn</span></span>
* <span data-ttu-id="4983e-1299">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="4983e-1299">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-1300">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1300">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-1301">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="4983e-1301">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1302">Az.Compute</span></span>
* <span data-ttu-id="4983e-1303">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1303">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="4983e-1304">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="4983e-1304">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1305">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1305">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1306">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1306">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1307">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4983e-1307">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="4983e-1308">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4983e-1308">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="4983e-1309">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4983e-1309">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="4983e-1310">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1310">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1311">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4983e-1311">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="4983e-1312">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4983e-1312">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="4983e-1313">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="4983e-1313">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="4983e-1314">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1314">New cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1315">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-1315">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4983e-1316">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-1316">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4983e-1317">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-1317">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4983e-1318">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-1318">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="4983e-1319">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4983e-1319">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1320">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1320">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1321">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="4983e-1321">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="4983e-1322">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="4983e-1322">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="4983e-1323">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="4983e-1323">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="4983e-1324">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4983e-1324">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4983e-1325">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4983e-1325">Az.Maintenance</span></span>
* <span data-ttu-id="4983e-1326">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="4983e-1326">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1327">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1327">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1328">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="4983e-1328">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="4983e-1329">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-1329">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4983e-1330">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-1330">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4983e-1331">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-1331">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4983e-1332">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4983e-1332">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4983e-1333">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4983e-1333">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4983e-1334">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4983e-1334">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4983e-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4983e-1335">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1336">Az.Network</span></span>
* <span data-ttu-id="4983e-1337">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4983e-1337">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="4983e-1338">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-1338">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4983e-1339">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-1339">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4983e-1340">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-1340">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="4983e-1341">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-1341">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="4983e-1342">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="4983e-1342">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="4983e-1343">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-1343">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="4983e-1344">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="4983e-1344">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="4983e-1345">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="4983e-1345">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="4983e-1346">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1346">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4983e-1347">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="4983e-1347">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="4983e-1348">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-1348">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4983e-1349">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="4983e-1349">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="4983e-1350">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4983e-1350">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="4983e-1351">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1351">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="4983e-1352">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1352">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-1353">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1353">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-1354">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="4983e-1354">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="4983e-1355">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="4983e-1355">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-1356">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-1356">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-1357">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="4983e-1357">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1358">Az.Sql</span></span>
* <span data-ttu-id="4983e-1359">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-1359">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="4983e-1360">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="4983e-1360">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1361">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1361">Az.Storage</span></span>
* <span data-ttu-id="4983e-1362">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4983e-1362">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4983e-1363">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-1363">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="4983e-1364">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1364">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="4983e-1365">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1365">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4983e-1366">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="4983e-1366">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="4983e-1367">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-1367">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4983e-1368">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-1368">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4983e-1369">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4983e-1369">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="4983e-1370">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-1370">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4983e-1371">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="4983e-1371">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="4983e-1372">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-1372">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4983e-1373">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1373">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="4983e-1374">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4983e-1374">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="4983e-1375">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1375">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="4983e-1376">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-1376">General</span></span>
* <span data-ttu-id="4983e-1377">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="4983e-1377">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="4983e-1378">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="4983e-1378">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="4983e-1379">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="4983e-1379">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="4983e-1380">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="4983e-1380">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="4983e-1381">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4983e-1381">Az.Billing</span></span>
  - <span data-ttu-id="4983e-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1382">Az.Compute</span></span>
  - <span data-ttu-id="4983e-1383">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4983e-1383">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="4983e-1384">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1384">Az.EventHub</span></span>
  - <span data-ttu-id="4983e-1385">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1385">Az.IotHub</span></span>
  - <span data-ttu-id="4983e-1386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1386">Az.KeyVault</span></span>
  - <span data-ttu-id="4983e-1387">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1387">Az.Monitor</span></span>
  - <span data-ttu-id="4983e-1388">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1388">Az.Network</span></span>
  - <span data-ttu-id="4983e-1389">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1389">Az.Resources</span></span>
  - <span data-ttu-id="4983e-1390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1390">Az.Storage</span></span>
  - <span data-ttu-id="4983e-1391">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1391">Az.Websites</span></span>
* <span data-ttu-id="4983e-1392">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1392">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="4983e-1393">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4983e-1393">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="4983e-1394">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="4983e-1394">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="4983e-1395">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1395">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-1396">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1396">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1397">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="4983e-1397">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1398">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1398">Az.Compute</span></span>
* <span data-ttu-id="4983e-1399">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="4983e-1399">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="4983e-1400">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="4983e-1400">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="4983e-1401">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1401">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="4983e-1402">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1402">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="4983e-1403">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="4983e-1403">[#11354]</span></span>
* <span data-ttu-id="4983e-1404">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="4983e-1404">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="4983e-1405">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-1405">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4983e-1406">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-1406">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4983e-1407">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-1407">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4983e-1408">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-1408">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="4983e-1409">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-1409">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="4983e-1410">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="4983e-1410">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="4983e-1411">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1411">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="4983e-1412">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="4983e-1412">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1413">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1414">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1414">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="4983e-1415">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="4983e-1415">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-1416">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-1416">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-1417">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="4983e-1417">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="4983e-1418">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1418">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-1419">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-1419">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-1420">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="4983e-1420">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1421">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1421">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1422">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4983e-1422">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="4983e-1423">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1423">New Cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1424">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4983e-1424">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="4983e-1425">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4983e-1425">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1426">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1427">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="4983e-1427">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1428">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1429">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="4983e-1429">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1430">Az.Network</span></span>
* <span data-ttu-id="4983e-1431">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="4983e-1431">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="4983e-1432">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-1432">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4983e-1433">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4983e-1433">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4983e-1434">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4983e-1434">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="4983e-1435">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4983e-1435">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4983e-1436">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-1436">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-1437">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1437">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-1438">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="4983e-1438">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1439">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1440">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="4983e-1440">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="4983e-1441">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="4983e-1441">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="4983e-1442">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="4983e-1442">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="4983e-1443">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="4983e-1443">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="4983e-1444">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4983e-1444">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="4983e-1445">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="4983e-1445">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1446">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1446">Az.Resources</span></span>
* <span data-ttu-id="4983e-1447">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="4983e-1447">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="4983e-1448">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="4983e-1448">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="4983e-1449">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1449">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="4983e-1450">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1450">Added example.</span></span>
* <span data-ttu-id="4983e-1451">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="4983e-1451">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="4983e-1452">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="4983e-1452">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1453">Az.Sql</span></span>
* <span data-ttu-id="4983e-1454">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="4983e-1454">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="4983e-1455">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1455">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4983e-1456">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-1456">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="4983e-1457">Az.Support</span><span class="sxs-lookup"><span data-stu-id="4983e-1457">Az.Support</span></span>
* <span data-ttu-id="4983e-1458">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="4983e-1458">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1459">Az.Websites</span></span>
* <span data-ttu-id="4983e-1460">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="4983e-1460">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="4983e-1461">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4983e-1461">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4983e-1462">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4983e-1462">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4983e-1463">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4983e-1463">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4983e-1464">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4983e-1464">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="4983e-1465">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1465">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1466">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1467">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="4983e-1467">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="4983e-1468">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="4983e-1468">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="4983e-1469">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="4983e-1469">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-1470">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-1470">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-1471">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="4983e-1471">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="4983e-1472">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="4983e-1472">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="4983e-1473">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="4983e-1473">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="4983e-1474">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="4983e-1474">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-1475">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-1475">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-1476">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="4983e-1476">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1477">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1478">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1478">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4983e-1479">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1479">New Cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1480">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1480">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1481">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1481">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1482">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1482">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1483">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1483">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="4983e-1484">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1484">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="4983e-1485">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1485">New Cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1486">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4983e-1486">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="4983e-1487">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4983e-1487">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="4983e-1488">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4983e-1488">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="4983e-1489">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4983e-1489">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="4983e-1490">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1490">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4983e-1491">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1491">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4983e-1492">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1492">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="4983e-1493">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1493">New Cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1494">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1494">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="4983e-1495">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4983e-1495">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="4983e-1496">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4983e-1496">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1497">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1498">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="4983e-1498">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1499">Az.Network</span></span>
* <span data-ttu-id="4983e-1500">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-1500">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="4983e-1501">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="4983e-1501">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="4983e-1502">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="4983e-1502">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="4983e-1503">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1503">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1504">Az.Resources</span></span>
* <span data-ttu-id="4983e-1505">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="4983e-1505">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="4983e-1506">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="4983e-1506">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="4983e-1507">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="4983e-1507">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="4983e-1508">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="4983e-1508">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="4983e-1509">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="4983e-1509">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="4983e-1510">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="4983e-1510">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="4983e-1511">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="4983e-1511">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="4983e-1512">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-1512">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="4983e-1513">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-1513">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4983e-1514">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-1514">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4983e-1515">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-1515">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="4983e-1516">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1516">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="4983e-1517">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-1517">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="4983e-1518">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1518">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1519">Az.Sql</span></span>
* <span data-ttu-id="4983e-1520">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1520">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4983e-1521">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4983e-1521">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="4983e-1522">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4983e-1522">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="4983e-1523">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="4983e-1523">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="4983e-1524">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="4983e-1524">Remove an LTR backup</span></span>
    - <span data-ttu-id="4983e-1525">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4983e-1525">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="4983e-1526">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4983e-1526">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="4983e-1527">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-1527">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="4983e-1528">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1528">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1529">Az.Storage</span></span>
* <span data-ttu-id="4983e-1530">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-1530">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="4983e-1531">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-1531">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="4983e-1532">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4983e-1532">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="4983e-1533">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-1533">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="4983e-1534">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4983e-1534">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-1535">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1535">Az.Websites</span></span>
* <span data-ttu-id="4983e-1536">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="4983e-1536">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="4983e-1537">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="4983e-1537">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="4983e-1538">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-1538">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="4983e-1539">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="4983e-1539">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="4983e-1540">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4983e-1540">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="4983e-1541">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1541">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-1542">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-1542">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-1543">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="4983e-1543">Updated client side telemetry.</span></span>
* <span data-ttu-id="4983e-1544">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4983e-1544">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="4983e-1545">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="4983e-1545">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1546">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1547">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="4983e-1547">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-1548">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-1548">Az.Automation</span></span>
* <span data-ttu-id="4983e-1549">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4983e-1549">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-1551">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1551">Updated SDK to 7.0</span></span>
* <span data-ttu-id="4983e-1552">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="4983e-1552">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1553">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1553">Az.Compute</span></span>
* <span data-ttu-id="4983e-1554">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="4983e-1554">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-1555">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-1555">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-1556">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="4983e-1556">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1557">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1557">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1558">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-1558">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4983e-1559">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-1559">New Cmdlets are:</span></span>
    - <span data-ttu-id="4983e-1560">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1560">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1561">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1561">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1562">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1562">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4983e-1563">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4983e-1563">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1564">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1564">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1565">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="4983e-1565">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1566">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1566">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1567">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="4983e-1567">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="4983e-1568">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1568">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="4983e-1569">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="4983e-1569">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1570">Az.Network</span></span>
* <span data-ttu-id="4983e-1571">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1571">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="4983e-1572">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4983e-1572">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4983e-1573">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4983e-1573">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4983e-1574">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4983e-1574">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="4983e-1575">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1575">No new cmdlets are added.</span></span> <span data-ttu-id="4983e-1576">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4983e-1576">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1577">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1577">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1578">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-1578">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1579">Az.Resources</span></span>
* <span data-ttu-id="4983e-1580">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="4983e-1580">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="4983e-1581">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4983e-1581">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="4983e-1582">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4983e-1582">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="4983e-1583">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="4983e-1583">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="4983e-1584">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4983e-1584">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="4983e-1585">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="4983e-1585">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="4983e-1586">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="4983e-1586">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="4983e-1587">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-1587">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1588">Az.Sql</span></span>
* <span data-ttu-id="4983e-1589">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4983e-1589">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="4983e-1590">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="4983e-1590">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="4983e-1591">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4983e-1591">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4983e-1592">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4983e-1592">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4983e-1593">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4983e-1593">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-1594">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-1594">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-1595">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1595">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="4983e-1596">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1596">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-1597">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-1598">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4983e-1598">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="4983e-1599">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1599">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1600">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1601">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="4983e-1601">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="4983e-1602">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="4983e-1602">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-1603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-1603">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-1604">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="4983e-1604">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="4983e-1605">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="4983e-1605">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="4983e-1606">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="4983e-1606">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="4983e-1607">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="4983e-1607">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1608">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1608">Az.Compute</span></span>
* <span data-ttu-id="4983e-1609">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="4983e-1609">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="4983e-1610">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4983e-1610">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="4983e-1611">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4983e-1611">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="4983e-1612">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-1612">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="4983e-1613">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4983e-1613">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1614">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1614">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1615">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1615">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4983e-1616">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4983e-1616">Az.DeploymentManager</span></span>
* <span data-ttu-id="4983e-1617">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="4983e-1617">Adds LIST operations for resources</span></span>
* <span data-ttu-id="4983e-1618">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="4983e-1618">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-1619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-1619">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-1620">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="4983e-1620">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1621">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1621">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1622">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4983e-1622">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1623">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1623">Az.Network</span></span>
* <span data-ttu-id="4983e-1624">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="4983e-1624">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="4983e-1625">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4983e-1625">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="4983e-1626">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4983e-1626">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4983e-1627">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4983e-1627">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="4983e-1628">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="4983e-1628">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="4983e-1629">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="4983e-1629">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="4983e-1630">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="4983e-1630">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="4983e-1631">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-1631">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="4983e-1632">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1632">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-1633">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="4983e-1634">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-1634">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="4983e-1635">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4983e-1635">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="4983e-1636">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="4983e-1636">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-1637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-1637">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-1638">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="4983e-1638">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="4983e-1639">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4983e-1639">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="4983e-1640">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="4983e-1640">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="4983e-1641">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4983e-1641">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1642">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1642">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1643">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1643">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="4983e-1644">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="4983e-1644">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1645">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1645">Az.Resources</span></span>
* <span data-ttu-id="4983e-1646">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="4983e-1646">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="4983e-1647">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="4983e-1647">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1648">Az.Sql</span></span>
<span data-ttu-id="4983e-1649">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4983e-1649">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1650">Az.Storage</span></span>
* <span data-ttu-id="4983e-1651">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-1651">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="4983e-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="4983e-1653">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="4983e-1653">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="4983e-1654">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-1654">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-1655">Az.Websites</span></span>
* <span data-ttu-id="4983e-1656">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="4983e-1656">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="4983e-1657">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="4983e-1657">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="4983e-1658">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4983e-1658">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-1659">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1659">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1660">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4983e-1660">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-1661">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-1661">Az.Cdn</span></span>
* <span data-ttu-id="4983e-1662">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-1662">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1663">Az.Compute</span></span>
* <span data-ttu-id="4983e-1664">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="4983e-1664">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4983e-1665">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-1665">Az.ContainerInstance</span></span>
* <span data-ttu-id="4983e-1666">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-1666">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4983e-1667">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4983e-1667">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4983e-1668">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1668">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4983e-1669">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1669">Get the Edge Storage Container</span></span>
* <span data-ttu-id="4983e-1670">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1670">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4983e-1671">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1671">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="4983e-1672">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1672">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4983e-1673">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1673">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="4983e-1674">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4983e-1674">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4983e-1675">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1675">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="4983e-1676">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1676">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4983e-1677">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1677">Get the Edge Storage Account</span></span>
* <span data-ttu-id="4983e-1678">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1678">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4983e-1679">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1679">Create new Edge Storage Account</span></span>
* <span data-ttu-id="4983e-1680">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4983e-1680">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4983e-1681">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4983e-1681">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="4983e-1682">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="4983e-1682">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="4983e-1683">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="4983e-1683">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="4983e-1684">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="4983e-1684">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="4983e-1685">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="4983e-1685">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1686">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1687">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4983e-1687">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="4983e-1688">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1688">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="4983e-1689">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="4983e-1689">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="4983e-1690">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="4983e-1690">Az.DevTestLabs</span></span>
* <span data-ttu-id="4983e-1691">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="4983e-1691">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-1692">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1692">Az.EventHub</span></span>
* <span data-ttu-id="4983e-1693">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="4983e-1693">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-1694">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-1694">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-1695">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="4983e-1695">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4983e-1696">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4983e-1696">Az.MachineLearning</span></span>
* <span data-ttu-id="4983e-1697">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="4983e-1697">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="4983e-1698">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-1698">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="4983e-1699">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4983e-1699">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="4983e-1700">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-1700">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="4983e-1701">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-1701">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="4983e-1702">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4983e-1702">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="4983e-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="4983e-1703">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="4983e-1704">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="4983e-1704">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1705">Az.Network</span></span>
* <span data-ttu-id="4983e-1706">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="4983e-1706">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1707">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1708">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1708">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="4983e-1709">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1709">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4983e-1710">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1710">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4983e-1711">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1711">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1712">Az.Resources</span></span>
* <span data-ttu-id="4983e-1713">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1713">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1714">Az.Sql</span></span>
* <span data-ttu-id="4983e-1715">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="4983e-1715">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="4983e-1716">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-1716">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4983e-1717">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4983e-1717">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4983e-1718">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="4983e-1718">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1719">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1719">Az.Storage</span></span>
* <span data-ttu-id="4983e-1720">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4983e-1720">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="4983e-1721">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-1721">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="4983e-1722">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4983e-1722">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="4983e-1723">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-1723">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="4983e-1724">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-1724">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="4983e-1725">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-1725">General</span></span>
* <span data-ttu-id="4983e-1726">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="4983e-1726">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1727">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1727">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1728">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4983e-1728">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="4983e-1729">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4983e-1729">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-1730">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-1730">Az.Batch</span></span>
* <span data-ttu-id="4983e-1731">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="4983e-1731">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1732">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1732">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1733">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1733">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-1734">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-1734">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-1735">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="4983e-1735">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="4983e-1736">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4983e-1736">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4983e-1737">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4983e-1737">Az.HealthcareApis</span></span>
* <span data-ttu-id="4983e-1738">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="4983e-1738">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-1739">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-1739">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-1740">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="4983e-1740">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="4983e-1741">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="4983e-1741">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="4983e-1742">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4983e-1742">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-1743">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-1743">Az.Monitor</span></span>
* <span data-ttu-id="4983e-1744">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4983e-1744">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="4983e-1745">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="4983e-1745">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="4983e-1746">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="4983e-1746">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1747">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1747">Az.Network</span></span>
* <span data-ttu-id="4983e-1748">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="4983e-1748">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1749">Az.Resources</span></span>
* <span data-ttu-id="4983e-1750">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="4983e-1750">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="4983e-1751">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4983e-1751">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1752">Az.Sql</span></span>
* <span data-ttu-id="4983e-1753">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="4983e-1753">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-1754">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-1754">Az.Storage</span></span>
* <span data-ttu-id="4983e-1755">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="4983e-1755">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="4983e-1756">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-1756">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="4983e-1757">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-1757">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="4983e-1758">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="4983e-1758">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="4983e-1759">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="4983e-1759">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="4983e-1760">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4983e-1760">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="4983e-1761">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1761">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="4983e-1762">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-1762">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="4983e-1763">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-1763">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="4983e-1764">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="4983e-1764">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="4983e-1765">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4983e-1765">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="4983e-1766">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="4983e-1766">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="4983e-1767">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4983e-1767">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="4983e-1768">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-1768">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-1769">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-1769">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-1770">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4983e-1770">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="4983e-1771">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4983e-1771">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1772">Az.Compute</span></span>
* <span data-ttu-id="4983e-1773">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="4983e-1773">VM Reapply feature</span></span>
    - <span data-ttu-id="4983e-1774">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="4983e-1774">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="4983e-1775">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="4983e-1775">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="4983e-1776">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-1776">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="4983e-1777">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4983e-1777">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="4983e-1778">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-1778">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4983e-1779">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4983e-1779">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="4983e-1780">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="4983e-1780">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="4983e-1781">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4983e-1781">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="4983e-1782">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4983e-1782">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="4983e-1783">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-1783">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4983e-1784">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4983e-1784">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4983e-1785">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1785">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4983e-1786">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="4983e-1786">Get the Order</span></span>
* <span data-ttu-id="4983e-1787">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1787">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4983e-1788">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="4983e-1788">Create new Order</span></span>
* <span data-ttu-id="4983e-1789">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1789">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4983e-1790">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="4983e-1790">Remove the Order</span></span>
* <span data-ttu-id="4983e-1791">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="4983e-1791">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="4983e-1792">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="4983e-1792">Now creates Local Share</span></span>
* <span data-ttu-id="4983e-1793">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1793">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="4983e-1794">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="4983e-1794">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="4983e-1795">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1795">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="4983e-1796">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="4983e-1796">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="4983e-1797">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1797">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4983e-1798">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="4983e-1798">Gets the information about Triggers</span></span>
* <span data-ttu-id="4983e-1799">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1799">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4983e-1800">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="4983e-1800">Create new Triggers</span></span>
* <span data-ttu-id="4983e-1801">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1801">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4983e-1802">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="4983e-1802">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1803">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1803">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1804">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1804">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="4983e-1805">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1805">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-1806">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-1806">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-1807">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="4983e-1807">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-1808">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1808">Az.EventHub</span></span>
* <span data-ttu-id="4983e-1809">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="4983e-1809">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-1810">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-1810">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-1811">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4983e-1811">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="4983e-1812">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="4983e-1812">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="4983e-1813">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="4983e-1813">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="4983e-1814">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="4983e-1814">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1815">Az.Network</span></span>
* <span data-ttu-id="4983e-1816">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1816">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4983e-1817">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4983e-1817">Az.PrivateDns</span></span>
* <span data-ttu-id="4983e-1818">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1818">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1819">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1820">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="4983e-1820">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="4983e-1821">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4983e-1821">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="4983e-1822">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4983e-1822">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4983e-1823">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4983e-1823">Az.RedisCache</span></span>
* <span data-ttu-id="4983e-1824">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1824">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="4983e-1825">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1825">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="4983e-1826">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="4983e-1826">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1827">Az.Resources</span></span>
- <span data-ttu-id="4983e-1828">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4983e-1828">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="4983e-1829">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-1829">Updated create policy definition help example</span></span>
- <span data-ttu-id="4983e-1830">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1830">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="4983e-1831">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-1831">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="4983e-1832">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1832">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-1833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-1833">Az.Sql</span></span>
* <span data-ttu-id="4983e-1834">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-1834">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="4983e-1835">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="4983e-1835">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="4983e-1836">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-1836">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="4983e-1837">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-1837">General</span></span>
* <span data-ttu-id="4983e-1838">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="4983e-1838">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-1839">Az.Accounts</span></span>
* <span data-ttu-id="4983e-1840">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1840">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4983e-1841">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4983e-1841">Az.Advisor</span></span>
* <span data-ttu-id="4983e-1842">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4983e-1842">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-1843">Az.Batch</span></span>
* <span data-ttu-id="4983e-1844">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1844">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="4983e-1845">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1845">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="4983e-1846">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1846">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="4983e-1847">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1847">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="4983e-1848">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="4983e-1848">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="4983e-1849">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1849">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="4983e-1850">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="4983e-1850">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="4983e-1851">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4983e-1851">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="4983e-1852">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4983e-1852">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="4983e-1853">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1853">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4983e-1854">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1854">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="4983e-1855">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1855">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="4983e-1856">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1856">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4983e-1857">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1857">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="4983e-1858">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1858">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="4983e-1859">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1859">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="4983e-1860">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1860">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="4983e-1861">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1861">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="4983e-1862">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="4983e-1862">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="4983e-1863">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4983e-1863">This operation is no longer supported.</span></span>
* <span data-ttu-id="4983e-1864">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1864">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4983e-1865">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1865">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4983e-1866">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1866">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="4983e-1867">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1867">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="4983e-1868">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="4983e-1868">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="4983e-1869">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="4983e-1869">New non-verified images are also now returned.</span></span> <span data-ttu-id="4983e-1870">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="4983e-1870">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="4983e-1871">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="4983e-1871">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="4983e-1872">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="4983e-1872">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="4983e-1873">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1873">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="4983e-1874">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="4983e-1874">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="4983e-1875">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1875">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="4983e-1876">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="4983e-1876">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="4983e-1877">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4983e-1877">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="4983e-1878">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="4983e-1878">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="4983e-1879">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="4983e-1879">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-1880">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-1880">Az.Cdn</span></span>
* <span data-ttu-id="4983e-1881">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="4983e-1881">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="4983e-1882">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="4983e-1882">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-1883">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-1883">Az.Compute</span></span>
* <span data-ttu-id="4983e-1884">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="4983e-1884">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="4983e-1885">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4983e-1885">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="4983e-1886">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4983e-1886">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="4983e-1887">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-1887">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4983e-1888">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-1888">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="4983e-1889">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="4983e-1889">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="4983e-1890">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-1890">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="4983e-1891">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4983e-1891">Breaking changes</span></span>
    - <span data-ttu-id="4983e-1892">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="4983e-1892">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="4983e-1893">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4983e-1893">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-1894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-1894">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-1895">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1895">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-1896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-1896">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-1897">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="4983e-1897">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="4983e-1898">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="4983e-1898">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="4983e-1899">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="4983e-1899">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="4983e-1900">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="4983e-1900">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="4983e-1901">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="4983e-1901">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="4983e-1902">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="4983e-1902">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-1903">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-1903">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-1904">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="4983e-1904">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-1905">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-1905">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-1906">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="4983e-1906">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="4983e-1907">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4983e-1907">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="4983e-1908">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="4983e-1908">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="4983e-1909">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="4983e-1909">Removed five cmdlets:</span></span>
    - <span data-ttu-id="4983e-1910">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4983e-1910">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4983e-1911">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4983e-1911">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4983e-1912">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4983e-1912">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4983e-1913">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-1913">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="4983e-1914">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-1914">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="4983e-1915">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1915">Added three cmdlets:</span></span>
    - <span data-ttu-id="4983e-1916">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4983e-1916">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4983e-1917">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4983e-1917">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4983e-1918">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4983e-1918">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="4983e-1919">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="4983e-1919">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="4983e-1920">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="4983e-1920">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="4983e-1921">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="4983e-1921">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="4983e-1922">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="4983e-1922">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="4983e-1923">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4983e-1923">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="4983e-1924">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="4983e-1924">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="4983e-1925">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="4983e-1925">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="4983e-1926">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="4983e-1926">Added some scenario test cases.</span></span>
* <span data-ttu-id="4983e-1927">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1927">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-1928">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1928">Az.IotHub</span></span>
* <span data-ttu-id="4983e-1929">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="4983e-1929">Breaking changes:</span></span>
    - <span data-ttu-id="4983e-1930">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4983e-1930">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4983e-1931">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4983e-1931">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4983e-1932">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4983e-1932">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4983e-1933">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4983e-1933">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4983e-1934">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4983e-1934">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="4983e-1935">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4983e-1935">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="4983e-1936">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1936">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="4983e-1937">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4983e-1937">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="4983e-1938">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4983e-1938">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4983e-1939">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4983e-1939">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4983e-1940">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4983e-1940">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4983e-1941">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4983e-1941">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-1942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-1942">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-1943">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1943">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1944">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1944">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="4983e-1945">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1945">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="4983e-1946">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1946">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1947">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1947">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1948">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1948">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1949">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1949">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1950">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-1950">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-1951">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="4983e-1951">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-1952">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-1952">Az.Resources</span></span>
* <span data-ttu-id="4983e-1953">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="4983e-1953">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-1954">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-1954">Az.Network</span></span>
* <span data-ttu-id="4983e-1955">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4983e-1955">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="4983e-1956">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-1956">Updated cmdlet:</span></span>
        - <span data-ttu-id="4983e-1957">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1957">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-1958">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1958">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-1959">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1959">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-1960">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1960">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-1961">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1961">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4983e-1962">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4983e-1962">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="4983e-1963">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-1963">New cmdlet:</span></span>
        - <span data-ttu-id="4983e-1964">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4983e-1964">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="4983e-1965">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="4983e-1965">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="4983e-1966">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-1966">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="4983e-1967">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1967">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="4983e-1968">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="4983e-1968">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="4983e-1969">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="4983e-1969">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="4983e-1970">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-1970">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="4983e-1971">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1971">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="4983e-1972">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1972">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-1973">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4983e-1973">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="4983e-1974">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-1974">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4983e-1975">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-1975">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4983e-1976">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-1976">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4983e-1977">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4983e-1977">Set-AzVirtualHub</span></span>
* <span data-ttu-id="4983e-1978">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4983e-1978">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="4983e-1979">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4983e-1979">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4983e-1980">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1980">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4983e-1981">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1981">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4983e-1982">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1982">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="4983e-1983">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1983">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="4983e-1984">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1984">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="4983e-1985">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1985">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-1986">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-1986">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="4983e-1987">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4983e-1987">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4983e-1988">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1988">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4983e-1989">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1989">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4983e-1990">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1990">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4983e-1991">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1991">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4983e-1992">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-1992">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="4983e-1993">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="4983e-1993">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="4983e-1994">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-1994">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-1995">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="4983e-1995">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="4983e-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4983e-1996">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="4983e-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4983e-1997">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="4983e-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4983e-1998">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="4983e-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="4983e-1999">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="4983e-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-2000">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="4983e-2001">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4983e-2001">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4983e-2002">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-2002">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="4983e-2003">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2003">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="4983e-2004">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="4983e-2004">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="4983e-2005">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="4983e-2005">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="4983e-2006">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4983e-2006">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4983e-2007">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-2007">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="4983e-2008">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-2008">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="4983e-2009">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="4983e-2009">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="4983e-2010">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2010">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="4983e-2011">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2011">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="4983e-2012">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-2012">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-2013">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2013">New-AzIpGroup</span></span>
        - <span data-ttu-id="4983e-2014">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2014">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="4983e-2015">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2015">Get-AzIpGroup</span></span>
        - <span data-ttu-id="4983e-2016">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2016">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-2017">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2017">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-2018">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="4983e-2018">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2019">Az.Sql</span></span>
* <span data-ttu-id="4983e-2020">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4983e-2020">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="4983e-2021">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="4983e-2021">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="4983e-2022">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="4983e-2022">Removed deprecated aliases:</span></span>
* <span data-ttu-id="4983e-2023">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4983e-2023">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="4983e-2024">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4983e-2024">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="4983e-2025">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2025">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4983e-2026">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="4983e-2026">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="4983e-2027">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="4983e-2027">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="4983e-2028">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-2028">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2029">Az.Storage</span></span>
* <span data-ttu-id="4983e-2030">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-2030">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="4983e-2031">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2031">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4983e-2032">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2032">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4983e-2033">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="4983e-2033">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="4983e-2034">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4983e-2034">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="4983e-2035">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4983e-2035">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="4983e-2036">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2036">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="4983e-2037">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-2037">General</span></span>
* <span data-ttu-id="4983e-2038">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4983e-2038">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-2039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2039">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2040">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="4983e-2040">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-2041">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2041">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-2042">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4983e-2042">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="4983e-2043">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="4983e-2043">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2044">Az.Automation</span></span>
* <span data-ttu-id="4983e-2045">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="4983e-2045">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-2046">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-2046">Az.Batch</span></span>
* <span data-ttu-id="4983e-2047">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="4983e-2047">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2048">Az.Compute</span></span>
* <span data-ttu-id="4983e-2049">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-2049">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4983e-2050">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2050">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="4983e-2051">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="4983e-2051">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="4983e-2052">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="4983e-2052">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2053">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2054">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="4983e-2054">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="4983e-2055">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="4983e-2055">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="4983e-2056">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="4983e-2056">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-2057">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-2057">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-2058">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="4983e-2058">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4983e-2059">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4983e-2059">Az.HealthcareApis</span></span>
* <span data-ttu-id="4983e-2060">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4983e-2060">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="4983e-2061">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="4983e-2061">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="4983e-2062">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="4983e-2062">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="4983e-2063">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="4983e-2063">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-2064">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2064">Az.IotHub</span></span>
* <span data-ttu-id="4983e-2065">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4983e-2065">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4983e-2066">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="4983e-2066">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2067">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2067">Az.Monitor</span></span>
* <span data-ttu-id="4983e-2068">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="4983e-2068">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="4983e-2069">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="4983e-2069">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="4983e-2070">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="4983e-2070">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="4983e-2071">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4983e-2071">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2072">Az.Network</span></span>
* <span data-ttu-id="4983e-2073">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="4983e-2073">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="4983e-2074">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-2074">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="4983e-2075">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-2075">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-2076">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2076">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="4983e-2077">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2077">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4983e-2078">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4983e-2078">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="4983e-2079">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4983e-2079">Updated cmdlets:</span></span>
        - <span data-ttu-id="4983e-2080">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2080">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4983e-2081">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2081">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4983e-2082">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2082">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4983e-2083">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="4983e-2083">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="4983e-2084">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="4983e-2084">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="4983e-2085">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4983e-2085">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="4983e-2086">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4983e-2086">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4983e-2087">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4983e-2087">Az.RedisCache</span></span>
* <span data-ttu-id="4983e-2088">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="4983e-2088">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2089">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2089">Az.Sql</span></span>
* <span data-ttu-id="4983e-2090">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4983e-2090">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2091">Az.Storage</span></span>
* <span data-ttu-id="4983e-2092">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="4983e-2092">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="4983e-2093">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4983e-2093">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4983e-2094">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4983e-2094">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="4983e-2095">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4983e-2095">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4983e-2096">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2096">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-2097">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-2097">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-2098">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="4983e-2098">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2099">Az.Websites</span></span>
* <span data-ttu-id="4983e-2100">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="4983e-2100">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="4983e-2101">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4983e-2102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2102">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-2103">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-2103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4983e-2104">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="4983e-2104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4983e-2105">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2106">Az.Automation</span></span>
* <span data-ttu-id="4983e-2107">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="4983e-2107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4983e-2108">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="4983e-2108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4983e-2109">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="4983e-2109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2110">Az.Compute</span></span>
* <span data-ttu-id="4983e-2111">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4983e-2112">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4983e-2113">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="4983e-2113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4983e-2114">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4983e-2114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4983e-2115">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4983e-2115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4983e-2116">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-2116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4983e-2117">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="4983e-2117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4983e-2118">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="4983e-2118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4983e-2119">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4983e-2119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2120">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2121">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4983e-2121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4983e-2122">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="4983e-2122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-2123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-2123">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-2124">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="4983e-2124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-2125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2125">Az.IotHub</span></span>
* <span data-ttu-id="4983e-2126">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="4983e-2126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4983e-2127">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="4983e-2127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4983e-2128">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4983e-2128">New cmdlets are:</span></span>
    - <span data-ttu-id="4983e-2129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4983e-2129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4983e-2130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4983e-2130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4983e-2131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4983e-2131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4983e-2132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4983e-2132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2133">Az.Monitor</span></span>
* <span data-ttu-id="4983e-2134">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="4983e-2134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4983e-2135">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="4983e-2135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4983e-2136">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="4983e-2136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4983e-2137">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="4983e-2137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4983e-2138">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="4983e-2138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4983e-2139">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="4983e-2139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4983e-2140">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4983e-2140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4983e-2141">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="4983e-2141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4983e-2142">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4983e-2142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4983e-2143">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4983e-2143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4983e-2144">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4983e-2144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4983e-2145">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4983e-2145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4983e-2146">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4983e-2146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4983e-2147">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4983e-2147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4983e-2148">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4983e-2148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4983e-2149">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4983e-2149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4983e-2150">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="4983e-2150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4983e-2151">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-2151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4983e-2152">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="4983e-2152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4983e-2153">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-2153">Overall improved help files</span></span>
* <span data-ttu-id="4983e-2154">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="4983e-2154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2155">Az.Network</span></span>
* <span data-ttu-id="4983e-2156">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="4983e-2156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="4983e-2157">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="4983e-2157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4983e-2158">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="4983e-2158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4983e-2159">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="4983e-2159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4983e-2160">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="4983e-2160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4983e-2161">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="4983e-2161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4983e-2162">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="4983e-2162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4983e-2163">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4983e-2163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4983e-2164">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-2164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4983e-2165">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="4983e-2165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4983e-2166">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4983e-2167">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-2167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4983e-2168">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2168">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4983e-2169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4983e-2170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4983e-2171">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-2171">Updated cmdlet:</span></span>
        - <span data-ttu-id="4983e-2172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4983e-2172">New-VpnSite</span></span>
        - <span data-ttu-id="4983e-2173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4983e-2173">Update-VpnSite</span></span>
        - <span data-ttu-id="4983e-2174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2174">New-VpnConnection</span></span>
        - <span data-ttu-id="4983e-2175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2175">Update-VpnConnection</span></span>
* <span data-ttu-id="4983e-2176">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4983e-2176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2178">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="4983e-2178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4983e-2179">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="4983e-2179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2180">Az.Resources</span></span>
* <span data-ttu-id="4983e-2181">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="4983e-2181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-2182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2182">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-2183">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4983e-2183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4983e-2184">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="4983e-2184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4983e-2185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4983e-2185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4983e-2186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4983e-2186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4983e-2187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4983e-2187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4983e-2188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4983e-2188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4983e-2189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4983e-2189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4983e-2190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4983e-2190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4983e-2191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4983e-2191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4983e-2192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4983e-2192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4983e-2193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4983e-2193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4983e-2194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4983e-2194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4983e-2195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4983e-2195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4983e-2196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4983e-2196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4983e-2197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4983e-2197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4983e-2198">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4983e-2198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4983e-2199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4983e-2199">Az.SignalR</span></span>
* <span data-ttu-id="4983e-2200">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="4983e-2200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2201">Az.Sql</span></span>
* <span data-ttu-id="4983e-2202">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="4983e-2202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4983e-2203">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="4983e-2203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4983e-2204">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4983e-2205">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4983e-2205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4983e-2206">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4983e-2206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2207">Az.Storage</span></span>
* <span data-ttu-id="4983e-2208">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-2208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4983e-2209">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="4983e-2209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4983e-2210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4983e-2211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4983e-2212">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="4983e-2212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4983e-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4983e-2214">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4983e-2214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4983e-2215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-2215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4983e-2216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-2216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4983e-2217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-2217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4983e-2218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4983e-2218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2219">Az.Websites</span></span>
* <span data-ttu-id="4983e-2220">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="4983e-2220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4983e-2221">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="4983e-2221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4983e-2222">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="4983e-2222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4983e-2223">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4983e-2224">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-2224">General</span></span>
* <span data-ttu-id="4983e-2225">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="4983e-2225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-2226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2226">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2227">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="4983e-2227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-2228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-2228">Az.Aks</span></span>
* <span data-ttu-id="4983e-2229">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="4983e-2229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4983e-2230">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4983e-2230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2231">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-2232">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4983e-2232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4983e-2233">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="4983e-2233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4983e-2234">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="4983e-2234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4983e-2235">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4983e-2235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4983e-2236">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4983e-2236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-2237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-2237">Az.Batch</span></span>
* <span data-ttu-id="4983e-2238">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="4983e-2238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-2239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-2239">Az.Cdn</span></span>
* <span data-ttu-id="4983e-2240">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="4983e-2240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2241">Az.Compute</span></span>
* <span data-ttu-id="4983e-2242">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4983e-2243">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-2243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4983e-2244">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="4983e-2244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4983e-2245">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4983e-2246">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4983e-2246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4983e-2247">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4983e-2247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4983e-2248">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4983e-2248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4983e-2249">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="4983e-2249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2250">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2251">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="4983e-2251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4983e-2252">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="4983e-2252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4983e-2253">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4983e-2253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4983e-2254">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="4983e-2254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-2255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-2255">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-2256">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="4983e-2256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2257">Az.EventHub</span></span>
* <span data-ttu-id="4983e-2258">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-2258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4983e-2259">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="4983e-2259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4983e-2260">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4983e-2260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4983e-2261">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4983e-2261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4983e-2262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4983e-2262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4983e-2263">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="4983e-2263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2264">Az.Monitor</span></span>
* <span data-ttu-id="4983e-2265">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-2265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2266">Az.Network</span></span>
* <span data-ttu-id="4983e-2267">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4983e-2268">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4983e-2268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4983e-2269">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="4983e-2269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4983e-2270">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="4983e-2270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4983e-2271">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="4983e-2271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="4983e-2272">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4983e-2272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4983e-2273">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4983e-2273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-2274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2274">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-2275">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="4983e-2275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4983e-2276">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="4983e-2276">Added example</span></span>
    - <span data-ttu-id="4983e-2277">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="4983e-2277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4983e-2278">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4983e-2278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4983e-2279">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4983e-2279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2280">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2281">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2282">Az.Resources</span></span>
* <span data-ttu-id="4983e-2283">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="4983e-2283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4983e-2284">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="4983e-2284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4983e-2285">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="4983e-2285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4983e-2286">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-2286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-2287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-2287">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-2288">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-2288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4983e-2289">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4983e-2289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4983e-2290">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="4983e-2290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-2291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2291">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-2292">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="4983e-2292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4983e-2293">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4983e-2293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4983e-2294">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4983e-2294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4983e-2295">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="4983e-2295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4983e-2296">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4983e-2296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4983e-2297">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4983e-2297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2298">Az.Sql</span></span>
* <span data-ttu-id="4983e-2299">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4983e-2299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2300">Az.Storage</span></span>
* <span data-ttu-id="4983e-2301">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4983e-2301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4983e-2302">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="4983e-2302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4983e-2303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4983e-2304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-2304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4983e-2305">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="4983e-2305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4983e-2306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-2306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2307">Az.Websites</span></span>
* <span data-ttu-id="4983e-2308">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4983e-2308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4983e-2309">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-2310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2310">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2311">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4983e-2311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4983e-2312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4983e-2313">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="4983e-2313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2314">Az.Automation</span></span>
* <span data-ttu-id="4983e-2315">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="4983e-2315">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-2316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2316">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-2317">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4983e-2317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2318">Az.Compute</span></span>
* <span data-ttu-id="4983e-2319">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="4983e-2319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4983e-2320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4983e-2320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4983e-2321">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="4983e-2321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4983e-2322">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4983e-2322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2323">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2324">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-2324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4983e-2325">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="4983e-2325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-2326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2326">Az.EventHub</span></span>
* <span data-ttu-id="4983e-2327">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-2327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4983e-2328">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4983e-2328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-2329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-2329">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-2330">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4983e-2330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4983e-2331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4983e-2331">Az.LogicApp</span></span>
* <span data-ttu-id="4983e-2332">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="4983e-2332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4983e-2333">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="4983e-2333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4983e-2334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2334">Az.ManagedServices</span></span>
* <span data-ttu-id="4983e-2335">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="4983e-2335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2336">Az.Network</span></span>
* <span data-ttu-id="4983e-2337">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="4983e-2337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4983e-2338">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2338">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-2339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4983e-2340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4983e-2341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-2342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-2343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-2344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4983e-2345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4983e-2345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4983e-2346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4983e-2347">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="4983e-2347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4983e-2348">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="4983e-2348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4983e-2349">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4983e-2349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4983e-2350">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4983e-2350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4983e-2351">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4983e-2351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4983e-2352">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4983e-2352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4983e-2353">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4983e-2353">Updated cmdlets</span></span>
        - <span data-ttu-id="4983e-2354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4983e-2355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4983e-2356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4983e-2357">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4983e-2358">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-2358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4983e-2359">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-2359">Updated cmdlet:</span></span>
        - <span data-ttu-id="4983e-2360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4983e-2361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4983e-2362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4983e-2363">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="4983e-2363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4983e-2364">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="4983e-2364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4983e-2365">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="4983e-2365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-2366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2366">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-2367">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="4983e-2367">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="4983e-2368">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="4983e-2368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2370">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4983e-2371">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4983e-2372">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4983e-2373">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4983e-2374">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4983e-2375">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4983e-2376">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4983e-2377">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4983e-2378">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4983e-2379">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="4983e-2379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2380">Az.Resources</span></span>
- <span data-ttu-id="4983e-2381">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-2381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4983e-2382">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4983e-2382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-2383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-2383">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-2384">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-2384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4983e-2385">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4983e-2385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2386">Az.Sql</span></span>
* <span data-ttu-id="4983e-2387">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4983e-2387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4983e-2388">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="4983e-2388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4983e-2389">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="4983e-2389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2390">Az.Storage</span></span>
* <span data-ttu-id="4983e-2391">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4983e-2391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-2392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-2392">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-2393">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="4983e-2393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4983e-2394">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4983e-2394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2395">Az.Websites</span></span>
* <span data-ttu-id="4983e-2396">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4983e-2396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4983e-2397">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4983e-2397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4983e-2398">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4983e-2398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4983e-2399">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-2400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2400">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2401">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="4983e-2401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4983e-2402">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="4983e-2402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4983e-2403">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4983e-2403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4983e-2404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4983e-2404">Az.Advisor</span></span>
* <span data-ttu-id="4983e-2405">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4983e-2405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4983e-2406">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4983e-2406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4983e-2407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2407">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-2408">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4983e-2408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4983e-2409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4983e-2409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4983e-2410">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="4983e-2410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4983e-2411">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="4983e-2411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4983e-2412">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4983e-2412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4983e-2413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4983e-2413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4983e-2414">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="4983e-2414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2415">Az.Automation</span></span>
* <span data-ttu-id="4983e-2416">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4983e-2416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2417">Az.Compute</span></span>
* <span data-ttu-id="4983e-2418">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2419">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2420">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="4983e-2420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4983e-2421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4983e-2421">Az.EventGrid</span></span>
* <span data-ttu-id="4983e-2422">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="4983e-2422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-2423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2423">Az.IotHub</span></span>
* <span data-ttu-id="4983e-2424">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="4983e-2424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2425">Az.Network</span></span>
* <span data-ttu-id="4983e-2426">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="4983e-2426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4983e-2427">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="4983e-2427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-2428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2428">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-2429">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4983e-2429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4983e-2430">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4983e-2430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-2431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2431">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-2432">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4983e-2432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2433">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2434">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="4983e-2434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2435">Az.Resources</span></span>
    - <span data-ttu-id="4983e-2436">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="4983e-2436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4983e-2437">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4983e-2437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4983e-2438">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="4983e-2438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4983e-2439">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="4983e-2439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-2440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-2440">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-2441">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4983e-2441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2442">Az.Sql</span></span>
* <span data-ttu-id="4983e-2443">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="4983e-2443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4983e-2444">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4983e-2444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4983e-2445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4983e-2446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4983e-2447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4983e-2448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4983e-2449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4983e-2450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4983e-2450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4983e-2451">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="4983e-2451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2452">Az.Storage</span></span>
* <span data-ttu-id="4983e-2453">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-2453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4983e-2454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4983e-2454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4983e-2455">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="4983e-2455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4983e-2456">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="4983e-2456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4983e-2457">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4983e-2458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4983e-2459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4983e-2460">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="4983e-2460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4983e-2461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4983e-2461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4983e-2462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4983e-2462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4983e-2463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4983e-2463">Az.StorageSync</span></span>
* <span data-ttu-id="4983e-2464">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4983e-2464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4983e-2465">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-2466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2466">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2467">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="4983e-2467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4983e-2468">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4983e-2468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4983e-2469">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="4983e-2469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4983e-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4983e-2470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4983e-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4983e-2471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2472">Az.Compute</span></span>
* <span data-ttu-id="4983e-2473">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4983e-2474">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4983e-2474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4983e-2475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4983e-2475">Az.Dns</span></span>
* <span data-ttu-id="4983e-2476">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4983e-2477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4983e-2477">Az.EventGrid</span></span>
* <span data-ttu-id="4983e-2478">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4983e-2478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4983e-2479">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4983e-2479">New cmdlets:</span></span>
    - <span data-ttu-id="4983e-2480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4983e-2480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4983e-2481">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4983e-2482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4983e-2482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4983e-2483">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4983e-2484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4983e-2484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4983e-2485">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4983e-2486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4983e-2487">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4983e-2488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4983e-2489">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4983e-2490">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4983e-2490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4983e-2491">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4983e-2492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4983e-2492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4983e-2493">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="4983e-2493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="4983e-2494">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4983e-2494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4983e-2495">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="4983e-2495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4983e-2496">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4983e-2496">Updated cmdlets:</span></span>
    - <span data-ttu-id="4983e-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4983e-2497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4983e-2498">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4983e-2499">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4983e-2500">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="4983e-2500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4983e-2501">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4983e-2501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4983e-2502">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="4983e-2502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4983e-2503">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="4983e-2503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4983e-2504">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="4983e-2504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4983e-2505">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="4983e-2505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="4983e-2506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4983e-2506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4983e-2507">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4983e-2507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4983e-2508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4983e-2508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4983e-2509">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4983e-2510">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-2511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-2511">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-2512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4983e-2512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4983e-2513">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4983e-2513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4983e-2514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4983e-2514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4983e-2515">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4983e-2515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2516">Az.Network</span></span>
* <span data-ttu-id="4983e-2517">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-2517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4983e-2518">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2518">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4983e-2519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4983e-2520">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4983e-2520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4983e-2521">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2521">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4983e-2522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4983e-2523">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4983e-2524">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2524">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2525">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4983e-2526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4983e-2527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4983e-2527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4983e-2528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4983e-2529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4983e-2530">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-2530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4983e-2531">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2531">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-2532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4983e-2533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-2533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4983e-2534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4983e-2534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4983e-2535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4983e-2536">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4983e-2536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4983e-2537">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4983e-2537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4983e-2538">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4983e-2538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4983e-2539">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4983e-2539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4983e-2540">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4983e-2540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4983e-2541">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4983e-2541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4983e-2542">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-2542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4983e-2543">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="4983e-2543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4983e-2544">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-2544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4983e-2545">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="4983e-2545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4983e-2546">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4983e-2547">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4983e-2548">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4983e-2548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4983e-2549">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4983e-2550">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4983e-2550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4983e-2551">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4983e-2551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4983e-2552">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-2552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4983e-2553">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="4983e-2553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4983e-2554">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4983e-2554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="4983e-2555">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4983e-2555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="4983e-2556">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4983e-2557">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4983e-2558">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-2559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2559">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-2560">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4983e-2560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2561">Az.Resources</span></span>
* <span data-ttu-id="4983e-2562">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="4983e-2562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4983e-2563">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4983e-2564">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4983e-2565">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="4983e-2565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-2566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2566">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-2567">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="4983e-2567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2568">Az.Sql</span></span>
* <span data-ttu-id="4983e-2569">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4983e-2569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4983e-2570">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4983e-2570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4983e-2571">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4983e-2571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4983e-2572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4983e-2573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4983e-2574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4983e-2574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4983e-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4983e-2575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4983e-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4983e-2576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2577">Az.Storage</span></span>
* <span data-ttu-id="4983e-2578">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-2578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4983e-2579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2579">New-AzStorageAccount</span></span>
* <span data-ttu-id="4983e-2580">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="4983e-2580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4983e-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2582">Az.Websites</span></span>
* <span data-ttu-id="4983e-2583">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="4983e-2583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4983e-2584">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4983e-2584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4983e-2585">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4983e-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-2586">Az.Cdn</span></span>
* <span data-ttu-id="4983e-2587">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="4983e-2587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2588">Az.Compute</span></span>
* <span data-ttu-id="4983e-2589">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4983e-2589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4983e-2590">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4983e-2590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-2591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2591">Az.EventHub</span></span>
* <span data-ttu-id="4983e-2592">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="4983e-2592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4983e-2593">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4983e-2593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2594">Az.Network</span></span>
* <span data-ttu-id="4983e-2595">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="4983e-2595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4983e-2596">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="4983e-2596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-2597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2597">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-2598">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4983e-2598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2599">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2600">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="4983e-2600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-2601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-2601">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-2602">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4983e-2602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-2603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2603">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-2604">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4983e-2604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4983e-2605">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2606">Az.Sql</span></span>
* <span data-ttu-id="4983e-2607">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4983e-2607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4983e-2608">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4983e-2609">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4983e-2609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4983e-2610">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4983e-2610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2611">Az.Websites</span></span>
* <span data-ttu-id="4983e-2612">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="4983e-2612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4983e-2613">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4983e-2614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2614">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-2615">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4983e-2616">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4983e-2617">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4983e-2618">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="4983e-2618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4983e-2619">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4983e-2620">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4983e-2620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4983e-2621">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4983e-2622">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4983e-2623">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4983e-2624">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="4983e-2624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4983e-2625">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4983e-2626">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="4983e-2626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4983e-2627">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="4983e-2627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4983e-2628">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="4983e-2628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4983e-2629">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="4983e-2629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4983e-2630">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="4983e-2630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4983e-2631">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4983e-2631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4983e-2632">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4983e-2632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4983e-2633">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="4983e-2633">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="4983e-2634">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="4983e-2634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4983e-2635">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="4983e-2635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4983e-2636">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="4983e-2636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4983e-2637">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="4983e-2637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4983e-2638">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-2638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="4983e-2639">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4983e-2639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4983e-2640">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4983e-2640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4983e-2641">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4983e-2642">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4983e-2642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4983e-2643">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4983e-2643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4983e-2644">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="4983e-2644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4983e-2645">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="4983e-2645">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="4983e-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4983e-2646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4983e-2647">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4983e-2647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4983e-2648">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4983e-2648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4983e-2649">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4983e-2649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4983e-2650">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="4983e-2650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4983e-2651">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="4983e-2651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4983e-2652">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="4983e-2652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4983e-2653">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="4983e-2653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4983e-2654">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4983e-2654">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4983e-2655">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4983e-2656">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-2656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4983e-2657">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4983e-2658">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4983e-2658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4983e-2659">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4983e-2659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4983e-2660">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4983e-2661">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-2661">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4983e-2662">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4983e-2662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4983e-2663">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="4983e-2663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4983e-2664">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4983e-2665">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="4983e-2665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4983e-2666">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="4983e-2666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4983e-2667">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="4983e-2667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4983e-2668">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="4983e-2668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4983e-2669">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="4983e-2669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4983e-2670">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="4983e-2670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4983e-2671">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4983e-2671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4983e-2672">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4983e-2672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4983e-2673">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4983e-2673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4983e-2674">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-2674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4983e-2675">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4983e-2675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4983e-2676">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4983e-2676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4983e-2677">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4983e-2677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4983e-2678">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4983e-2678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4983e-2679">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="4983e-2679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4983e-2680">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="4983e-2680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4983e-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4983e-2681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4983e-2682">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="4983e-2682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4983e-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4983e-2683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4983e-2684">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-2684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4983e-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4983e-2685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4983e-2686">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4983e-2686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4983e-2687">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="4983e-2687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4983e-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4983e-2688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4983e-2689">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="4983e-2689">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="4983e-2690">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4983e-2690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4983e-2691">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="4983e-2691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2692">Az.Automation</span></span>
* <span data-ttu-id="4983e-2693">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="4983e-2693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4983e-2694">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4983e-2694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4983e-2695">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4983e-2695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4983e-2696">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="4983e-2696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4983e-2697">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4983e-2697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4983e-2698">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="4983e-2698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4983e-2699">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="4983e-2699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2700">Az.Compute</span></span>
* <span data-ttu-id="4983e-2701">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4983e-2701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4983e-2702">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="4983e-2702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-2703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-2703">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-2704">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2705">Az.Monitor</span></span>
* <span data-ttu-id="4983e-2706">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-2706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2707">Az.Network</span></span>
* <span data-ttu-id="4983e-2708">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="4983e-2708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4983e-2709">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4983e-2709">Updated cmdlet:</span></span>
        - <span data-ttu-id="4983e-2710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-2710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4983e-2711">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4983e-2711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2712">Az.Resources</span></span>
* <span data-ttu-id="4983e-2713">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="4983e-2713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2714">Az.Sql</span></span>
* <span data-ttu-id="4983e-2715">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="4983e-2715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4983e-2716">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-2717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2717">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2718">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="4983e-2718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-2719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2719">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-2720">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="4983e-2720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4983e-2721">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="4983e-2721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2722">Az.Compute</span></span>
* <span data-ttu-id="4983e-2723">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="4983e-2723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4983e-2724">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4983e-2725">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4983e-2726">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4983e-2726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4983e-2727">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4983e-2727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4983e-2728">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-2728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="4983e-2729">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4983e-2729">Breaking changes</span></span>
    - <span data-ttu-id="4983e-2730">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4983e-2730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4983e-2731">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4983e-2731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4983e-2732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4983e-2732">Az.DeploymentManager</span></span>
* <span data-ttu-id="4983e-2733">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4983e-2734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4983e-2734">Az.Dns</span></span>
* <span data-ttu-id="4983e-2735">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="4983e-2735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4983e-2736">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="4983e-2736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4983e-2737">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="4983e-2737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4983e-2738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-2738">Az.FrontDoor</span></span>
* <span data-ttu-id="4983e-2739">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4983e-2740">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="4983e-2740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4983e-2741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-2741">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-2742">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4983e-2742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4983e-2743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-2743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4983e-2744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-2744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4983e-2745">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4983e-2745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4983e-2746">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="4983e-2746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4983e-2747">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="4983e-2747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4983e-2748">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="4983e-2748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2749">Az.Monitor</span></span>
* <span data-ttu-id="4983e-2750">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4983e-2750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="4983e-2751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4983e-2751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4983e-2752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4983e-2753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4983e-2753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4983e-2754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4983e-2754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4983e-2755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4983e-2755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4983e-2756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4983e-2756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4983e-2757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4983e-2758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4983e-2759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4983e-2760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4983e-2761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4983e-2762">[Mais](/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="4983e-2762">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4983e-2763">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4983e-2763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2764">Az.Network</span></span>
* <span data-ttu-id="4983e-2765">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="4983e-2765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4983e-2766">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4983e-2766">New cmdlets</span></span>
        - <span data-ttu-id="4983e-2767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2767">New-AzNatGateway</span></span>
        - <span data-ttu-id="4983e-2768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4983e-2769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4983e-2770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-2770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4983e-2771">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4983e-2771">Updated cmdlets</span></span>
        - <span data-ttu-id="4983e-2772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4983e-2772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4983e-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4983e-2773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4983e-2774">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="4983e-2774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4983e-2775">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4983e-2776">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4983e-2776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-2777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2777">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-2778">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="4983e-2778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4983e-2779">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="4983e-2779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4983e-2780">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="4983e-2780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2781">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2782">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4983e-2782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4983e-2783">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4983e-2783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4983e-2784">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4983e-2784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4983e-2785">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-2785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4983e-2786">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4983e-2786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4983e-2787">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="4983e-2787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4983e-2788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4983e-2788">Az.Relay</span></span>
* <span data-ttu-id="4983e-2789">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="4983e-2789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-2790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-2790">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-2791">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4983e-2791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2792">Az.Storage</span></span>
* <span data-ttu-id="4983e-2793">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="4983e-2793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4983e-2794">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="4983e-2794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4983e-2795">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="4983e-2795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4983e-2796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2796">New-AzStorageAccount</span></span>
* <span data-ttu-id="4983e-2797">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="4983e-2797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4983e-2798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4983e-2799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4983e-2800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2801">Az.Websites</span></span>
* <span data-ttu-id="4983e-2802">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4983e-2802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4983e-2803">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="4983e-2803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4983e-2804">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-2805">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-2805">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-2806">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4983e-2806">General availability of `Az` module</span></span>
* <span data-ttu-id="4983e-2807">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4983e-2807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4983e-2808">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4983e-2808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4983e-2809">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4983e-2810">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4983e-2810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4983e-2811">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4983e-2812">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4983e-2812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-2813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2813">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2814">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="4983e-2814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4983e-2815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-2815">Az.Batch</span></span>
* <span data-ttu-id="4983e-2816">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-2817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-2817">Az.Cdn</span></span>
* <span data-ttu-id="4983e-2818">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-2819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2819">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-2820">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2821">Az.Compute</span></span>
* <span data-ttu-id="4983e-2822">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="4983e-2822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4983e-2823">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2824">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4983e-2824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2825">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2826">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4983e-2826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-2827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-2827">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-2828">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4983e-2829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4983e-2829">Az.EventGrid</span></span>
* <span data-ttu-id="4983e-2830">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="4983e-2830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-2831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2831">Az.EventHub</span></span>
* <span data-ttu-id="4983e-2832">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4983e-2832">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4983e-2833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4983e-2833">Az.HDInsight</span></span>
* <span data-ttu-id="4983e-2834">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-2835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-2835">Az.IotHub</span></span>
* <span data-ttu-id="4983e-2836">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-2837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-2837">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-2838">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2839">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4983e-2839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4983e-2840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4983e-2840">Az.MachineLearning</span></span>
* <span data-ttu-id="4983e-2841">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4983e-2842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4983e-2842">Az.Media</span></span>
* <span data-ttu-id="4983e-2843">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-2844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-2844">Az.Monitor</span></span>
  * <span data-ttu-id="4983e-2845">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4983e-2845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4983e-2846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4983e-2846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4983e-2847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4983e-2847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4983e-2848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4983e-2848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4983e-2849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4983e-2849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4983e-2850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4983e-2850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4983e-2851">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="4983e-2851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2852">Az.Network</span></span>
* <span data-ttu-id="4983e-2853">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2854">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4983e-2854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4983e-2855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4983e-2855">Az.NotificationHubs</span></span>
* <span data-ttu-id="4983e-2856">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-2857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-2857">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-2858">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4983e-2859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4983e-2859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4983e-2860">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2861">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2862">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2863">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4983e-2864">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4983e-2864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4983e-2865">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="4983e-2865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4983e-2866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4983e-2866">Az.RedisCache</span></span>
* <span data-ttu-id="4983e-2867">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2868">Az.Resources</span></span>
* <span data-ttu-id="4983e-2869">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4983e-2869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2870">Az.Sql</span></span>
* <span data-ttu-id="4983e-2871">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="4983e-2871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4983e-2872">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2873">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="4983e-2873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4983e-2874">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="4983e-2874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4983e-2875">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="4983e-2875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4983e-2876">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4983e-2876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4983e-2877">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4983e-2877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2878">Az.Websites</span></span>
* <span data-ttu-id="4983e-2879">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="4983e-2879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4983e-2880">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4983e-2880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4983e-2881">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="4983e-2881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4983e-2882">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4983e-2882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4983e-2883">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-2884">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-2884">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-2885">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4983e-2885">General availability of `Az` module</span></span>
* <span data-ttu-id="4983e-2886">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4983e-2886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4983e-2887">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4983e-2887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4983e-2888">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4983e-2889">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4983e-2889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4983e-2890">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4983e-2891">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4983e-2891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4983e-2892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2892">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2893">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4983e-2893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-2894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2894">Az.AnalysisServices</span></span>
* <span data-ttu-id="4983e-2895">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="4983e-2895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4983e-2896">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="4983e-2896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2897">Az.Automation</span></span>
* <span data-ttu-id="4983e-2898">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="4983e-2898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4983e-2899">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="4983e-2899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4983e-2900">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2901">Az.Compute</span></span>
* <span data-ttu-id="4983e-2902">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-2902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4983e-2903">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="4983e-2903">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4983e-2904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-2904">Az.ContainerInstance</span></span>
* <span data-ttu-id="4983e-2905">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="4983e-2905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2906">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2907">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="4983e-2907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4983e-2908">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4983e-2908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2909">Az.Resources</span></span>
* <span data-ttu-id="4983e-2910">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="4983e-2910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4983e-2911">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-2911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4983e-2912">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="4983e-2912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4983e-2913">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4983e-2913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4983e-2914">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="4983e-2914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4983e-2915">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4983e-2915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2916">Az.Sql</span></span>
* <span data-ttu-id="4983e-2917">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="4983e-2917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2918">Az.Storage</span></span>
* <span data-ttu-id="4983e-2919">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4983e-2920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4983e-2920">New-AzStorageContext</span></span>
* <span data-ttu-id="4983e-2921">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4983e-2921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4983e-2922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4983e-2922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4983e-2923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4983e-2923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4983e-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4983e-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4983e-2926">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="4983e-2926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4983e-2927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4983e-2928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4983e-2929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4983e-2930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4983e-2930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4983e-2931">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4983e-2932">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4983e-2932">Highlights since the last major release</span></span>
* <span data-ttu-id="4983e-2933">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4983e-2933">General availability of `Az` module</span></span>
* <span data-ttu-id="4983e-2934">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4983e-2934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4983e-2935">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4983e-2935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4983e-2936">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4983e-2937">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4983e-2937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4983e-2938">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4983e-2939">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4983e-2939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2940">Az.Automation</span></span>
* <span data-ttu-id="4983e-2941">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="4983e-2941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4983e-2942">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="4983e-2942">Dynamic grouping</span></span>
    * <span data-ttu-id="4983e-2943">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="4983e-2943">Pre-Post script</span></span>
    * <span data-ttu-id="4983e-2944">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="4983e-2944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2945">Az.Compute</span></span>
* <span data-ttu-id="4983e-2946">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4983e-2946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4983e-2947">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4983e-2947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-2948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-2948">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-2949">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-2949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2950">Az.Network</span></span>
* <span data-ttu-id="4983e-2951">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4983e-2952">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="4983e-2952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2953">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2954">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="4983e-2954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4983e-2955">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="4983e-2955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2956">Az.Resources</span></span>
* <span data-ttu-id="4983e-2957">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4983e-2957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4983e-2958">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="4983e-2958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-2959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-2959">Az.Sql</span></span>
* <span data-ttu-id="4983e-2960">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="4983e-2960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-2961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-2961">Az.Storage</span></span>
* <span data-ttu-id="4983e-2962">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-2962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4983e-2963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4983e-2964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4983e-2965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-2965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4983e-2966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4983e-2966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4983e-2967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4983e-2967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4983e-2968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4983e-2968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-2969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-2969">Az.Websites</span></span>
* <span data-ttu-id="4983e-2970">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="4983e-2970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="4983e-2971">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-2971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-2972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-2972">Az.Accounts</span></span>
* <span data-ttu-id="4983e-2973">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="4983e-2973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4983e-2974">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-2974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-2975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-2975">Az.Automation</span></span>
* <span data-ttu-id="4983e-2976">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4983e-2977">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="4983e-2977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4983e-2978">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="4983e-2978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-2979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-2979">Az.Cdn</span></span>
* <span data-ttu-id="4983e-2980">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="4983e-2980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-2981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-2981">Az.Compute</span></span>
* <span data-ttu-id="4983e-2982">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="4983e-2982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-2983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-2983">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-2984">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4983e-2984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4983e-2985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4983e-2985">Az.LogicApp</span></span>
* <span data-ttu-id="4983e-2986">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="4983e-2986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-2987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2987">Az.Network</span></span>
* <span data-ttu-id="4983e-2988">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="4983e-2988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-2989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-2989">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-2990">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-2990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4983e-2991">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="4983e-2991">SDK Update</span></span>
* <span data-ttu-id="4983e-2992">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4983e-2992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4983e-2993">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4983e-2993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-2994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-2994">Az.Resources</span></span>
* <span data-ttu-id="4983e-2995">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4983e-2995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4983e-2996">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4983e-2996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4983e-2997">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4983e-2997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4983e-2998">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4983e-2998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4983e-2999">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4983e-2999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4983e-3000">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4983e-3000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3001">Az.Sql</span></span>
* <span data-ttu-id="4983e-3002">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="4983e-3002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4983e-3003">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4983e-3003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-3004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3004">Az.Storage</span></span>
* <span data-ttu-id="4983e-3005">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-3005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4983e-3006">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-3006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-3007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3007">Az.AnalysisServices</span></span>
* <span data-ttu-id="4983e-3008">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-3008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-3009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-3009">Az.Automation</span></span>
* <span data-ttu-id="4983e-3010">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4983e-3011">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4983e-3012">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-3013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3013">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-3014">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="4983e-3014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3015">Az.Compute</span></span>
* <span data-ttu-id="4983e-3016">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="4983e-3016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4983e-3017">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="4983e-3017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4983e-3018">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4983e-3018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4983e-3019">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="4983e-3019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3020">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-3021">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="4983e-3021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4983e-3022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-3022">Az.EventHub</span></span>
* <span data-ttu-id="4983e-3023">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="4983e-3023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-3024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-3024">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-3025">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4983e-3025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4983e-3026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4983e-3026">Az.LogicApp</span></span>
* <span data-ttu-id="4983e-3027">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="4983e-3027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4983e-3028">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="4983e-3028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4983e-3029">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="4983e-3029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4983e-3030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4983e-3030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4983e-3031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4983e-3031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4983e-3032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4983e-3032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4983e-3033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4983e-3033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4983e-3034">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="4983e-3034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4983e-3035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4983e-3036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4983e-3037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4983e-3038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4983e-3039">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4983e-3039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4983e-3040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-3040">Az.Monitor</span></span>
* <span data-ttu-id="4983e-3041">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="4983e-3041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-3042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3042">Az.Network</span></span>
* <span data-ttu-id="4983e-3043">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4983e-3043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-3044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-3044">Az.OperationalInsights</span></span>
* <span data-ttu-id="4983e-3045">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="4983e-3045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4983e-3046">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="4983e-3046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="4983e-3047">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="4983e-3047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3048">Az.Resources</span></span>
* <span data-ttu-id="4983e-3049">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4983e-3049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4983e-3050">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4983e-3050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4983e-3051">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4983e-3051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4983e-3052">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="4983e-3052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3053">Az.Sql</span></span>
* <span data-ttu-id="4983e-3054">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-3054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4983e-3055">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="4983e-3055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-3056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3056">Az.Websites</span></span>
* <span data-ttu-id="4983e-3057">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4983e-3057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4983e-3058">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-3058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-3059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3059">Az.Accounts</span></span>
* <span data-ttu-id="4983e-3060">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4983e-3060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-3061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3061">Az.AnalysisServices</span></span>
<span data-ttu-id="4983e-3062">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="4983e-3062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3063">Az.Compute</span></span>
* <span data-ttu-id="4983e-3064">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="4983e-3064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4983e-3065">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4983e-3065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4983e-3066">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4983e-3066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-3067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3067">Az.RecoveryServices</span></span>
<span data-ttu-id="4983e-3068">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="4983e-3068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3069">Az.Resources</span></span>
* <span data-ttu-id="4983e-3070">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4983e-3070">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="4983e-3071">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4983e-3071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4983e-3072">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4983e-3072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="4983e-3073">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4983e-3073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3074">Az.Sql</span></span>
* <span data-ttu-id="4983e-3075">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4983e-3075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4983e-3076">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-3076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4983e-3077">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4983e-3077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4983e-3078">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-3078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-3079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3079">Az.Accounts</span></span>
* <span data-ttu-id="4983e-3080">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="4983e-3080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4983e-3081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3081">Az.AnalysisServices</span></span>
* <span data-ttu-id="4983e-3082">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-3082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-3083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3083">Az.RecoveryServices</span></span>
* <span data-ttu-id="4983e-3084">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-3084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4983e-3085">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-3085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-3086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3086">Az.Accounts</span></span>
* <span data-ttu-id="4983e-3087">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4983e-3087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4983e-3088">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4983e-3089">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4983e-3089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4983e-3090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4983e-3090">Az.Aks</span></span>
* <span data-ttu-id="4983e-3091">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4983e-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-3092">Az.Automation</span></span>
* <span data-ttu-id="4983e-3093">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="4983e-3093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4983e-3094">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4983e-3095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4983e-3095">Az.Cdn</span></span>
* <span data-ttu-id="4983e-3096">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3097">Az.Compute</span></span>
* <span data-ttu-id="4983e-3098">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4983e-3098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4983e-3099">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4983e-3099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4983e-3100">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4983e-3100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4983e-3101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4983e-3101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4983e-3102">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4983e-3103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4983e-3103">Az.DataFactory</span></span>
* <span data-ttu-id="4983e-3104">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4983e-3104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3105">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-3106">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4983e-3106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4983e-3107">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4983e-3107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4983e-3108">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-3109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-3109">Az.IotHub</span></span>
* <span data-ttu-id="4983e-3110">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4983e-3110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4983e-3111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-3111">Az.KeyVault</span></span>
* <span data-ttu-id="4983e-3112">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-3113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3113">Az.Network</span></span>
* <span data-ttu-id="4983e-3114">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3115">Az.Resources</span></span>
* <span data-ttu-id="4983e-3116">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="4983e-3116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4983e-3117">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4983e-3117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4983e-3118">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4983e-3118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4983e-3119">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4983e-3119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4983e-3120">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4983e-3120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4983e-3121">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4983e-3121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4983e-3122">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4983e-3122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-3123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-3123">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-3124">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4983e-3124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4983e-3125">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="4983e-3125">Fix some error messages.</span></span>
* <span data-ttu-id="4983e-3126">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="4983e-3126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4983e-3127">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="4983e-3127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4983e-3128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4983e-3128">Az.SignalR</span></span>
* <span data-ttu-id="4983e-3129">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3130">Az.Sql</span></span>
* <span data-ttu-id="4983e-3131">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4983e-3132">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4983e-3132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4983e-3133">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="4983e-3133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4983e-3134">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4983e-3134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-3135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3135">Az.Storage</span></span>
* <span data-ttu-id="4983e-3136">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4983e-3137">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="4983e-3137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4983e-3138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4983e-3138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4983e-3139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4983e-3139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4983e-3140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4983e-3140">Az.TrafficManager</span></span>
* <span data-ttu-id="4983e-3141">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-3142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3142">Az.Websites</span></span>
* <span data-ttu-id="4983e-3143">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4983e-3143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4983e-3144">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="4983e-3144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4983e-3145">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-3145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4983e-3146">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4983e-3146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4983e-3147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3147">Az.Accounts</span></span>
* <span data-ttu-id="4983e-3148">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4983e-3148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3149">Az.Compute</span></span>
* <span data-ttu-id="4983e-3150">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4983e-3150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4983e-3151">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4983e-3151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4983e-3152">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3153">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-3154">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="4983e-3154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4983e-3155">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="4983e-3155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4983e-3156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4983e-3156">Az.EventGrid</span></span>
* <span data-ttu-id="4983e-3157">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4983e-3157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4983e-3158">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4983e-3158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4983e-3159">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4983e-3159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4983e-3160">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4983e-3160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4983e-3161">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4983e-3161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4983e-3162">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4983e-3162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4983e-3163">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4983e-3163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4983e-3164">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4983e-3164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4983e-3165">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4983e-3165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4983e-3166">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4983e-3166">Dead letter endpoint.</span></span>
* <span data-ttu-id="4983e-3167">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4983e-3167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4983e-3168">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="4983e-3168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4983e-3169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-3169">Az.IotHub</span></span>
* <span data-ttu-id="4983e-3170">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="4983e-3170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4983e-3171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4983e-3171">Az.LogicApp</span></span>
* <span data-ttu-id="4983e-3172">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="4983e-3172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3173">Az.Resources</span></span>
* <span data-ttu-id="4983e-3174">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="4983e-3174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4983e-3175">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4983e-3175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4983e-3176">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4983e-3176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4983e-3177">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4983e-3177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4983e-3178">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="4983e-3178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4983e-3179">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4983e-3179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4983e-3180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4983e-3180">Az.SignalR</span></span>
* <span data-ttu-id="4983e-3181">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3182">Az.Sql</span></span>
* <span data-ttu-id="4983e-3183">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="4983e-3183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4983e-3184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3184">Az.Storage</span></span>
* <span data-ttu-id="4983e-3185">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="4983e-3185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4983e-3186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4983e-3186">New-AzStorageContext</span></span>
* <span data-ttu-id="4983e-3187">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="4983e-3187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4983e-3188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4983e-3188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-3189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3189">Az.Websites</span></span>
* <span data-ttu-id="4983e-3190">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4983e-3190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4983e-3191">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4983e-3192">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4983e-3193">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-3193">General</span></span>

- <span data-ttu-id="4983e-3194">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="4983e-3194">General Availability of Az Module</span></span>
- <span data-ttu-id="4983e-3195">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="4983e-3195">Online help for each module</span></span>
- <span data-ttu-id="4983e-3196">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4983e-3196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4983e-3197">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4983e-3197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4983e-3198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3198">Az.Accounts</span></span>
- <span data-ttu-id="4983e-3199">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4983e-3199">Changed from Az.Profile</span></span>
- <span data-ttu-id="4983e-3200">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="4983e-3200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4983e-3201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-3201">Az.ApiManagement</span></span>
- <span data-ttu-id="4983e-3202">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="4983e-3202">Fixes for #7002</span></span>
- <span data-ttu-id="4983e-3203">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4983e-3204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4983e-3204">Az.Batch</span></span>
- <span data-ttu-id="4983e-3205">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4983e-3205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4983e-3206">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="4983e-3206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4983e-3207">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4983e-3208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4983e-3208">Az.Billing</span></span>
- <span data-ttu-id="4983e-3209">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4983e-3210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3210">Az.CognitivServices</span></span>
- <span data-ttu-id="4983e-3211">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-3211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4983e-3212">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4983e-3212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4983e-3213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3213">Az.ContainerInstance</span></span>
- <span data-ttu-id="4983e-3214">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4983e-3214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4983e-3215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4983e-3215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4983e-3216">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3217">Az.DataLakeStore</span></span>
- <span data-ttu-id="4983e-3218">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4983e-3219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4983e-3219">Az.Monitor</span></span>
- <span data-ttu-id="4983e-3220">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4983e-3221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4983e-3221">Az.KeyVault</span></span>
- <span data-ttu-id="4983e-3222">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="4983e-3222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4983e-3223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4983e-3223">Az.MachineLearning</span></span>
- <span data-ttu-id="4983e-3224">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4983e-3224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4983e-3225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4983e-3225">Az.Media</span></span>
- <span data-ttu-id="4983e-3226">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4983e-3226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4983e-3227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3227">Az.Network</span></span>
<span data-ttu-id="4983e-3228">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4983e-3228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4983e-3229">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4983e-3229">New cmdlets added:</span></span>
        - <span data-ttu-id="4983e-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4983e-3235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4983e-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4983e-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4983e-3237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4983e-3238">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4983e-3238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4983e-3239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4983e-3239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4983e-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4983e-3240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4983e-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4983e-3241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4983e-3242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-3242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4983e-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-3243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4983e-3244">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="4983e-3244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4983e-3245">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4983e-3245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4983e-3246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4983e-3246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4983e-3247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4983e-3247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4983e-3248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4983e-3248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4983e-3249">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4983e-3249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4983e-3250">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4983e-3251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-3251">Az.OperationalInsights</span></span>
- <span data-ttu-id="4983e-3252">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4983e-3253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4983e-3253">Az.Profile</span></span>
- <span data-ttu-id="4983e-3254">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4983e-3254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-3255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3255">Az.RecoveryServices</span></span>
- <span data-ttu-id="4983e-3256">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4983e-3257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3257">Az.Resources</span></span>
- <span data-ttu-id="4983e-3258">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4983e-3259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-3259">Az.ServiceFabric</span></span>
- <span data-ttu-id="4983e-3260">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="4983e-3260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4983e-3261">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4983e-3262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4983e-3262">Az.SIgnalR</span></span>
- <span data-ttu-id="4983e-3263">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4983e-3263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4983e-3264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3264">Az.Sql</span></span>
- <span data-ttu-id="4983e-3265">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="4983e-3265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4983e-3266">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="4983e-3266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4983e-3267">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4983e-3268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3268">Az.Storage</span></span>
- <span data-ttu-id="4983e-3269">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4983e-3270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3270">Az.Websites</span></span>
- <span data-ttu-id="4983e-3271">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4983e-3271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4983e-3272">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4983e-3273">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-3273">General</span></span>

* <span data-ttu-id="4983e-3274">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4983e-3274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4983e-3275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3275">Az.Compute</span></span>

* <span data-ttu-id="4983e-3276">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="4983e-3276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3277">Az.DataLakeStore</span></span>

* <span data-ttu-id="4983e-3278">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="4983e-3278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4983e-3279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4983e-3279">Az.FrontDoor</span></span>

* <span data-ttu-id="4983e-3280">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="4983e-3280">Fixed some broken links</span></span>
    - <span data-ttu-id="4983e-3281">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4983e-3281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4983e-3282">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4983e-3282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4983e-3283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3283">Az.RecoveryServices</span></span>

* <span data-ttu-id="4983e-3284">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="4983e-3284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4983e-3285">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="4983e-3285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4983e-3286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3286">Az.Resources</span></span>

* <span data-ttu-id="4983e-3287">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4983e-3287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4983e-3288">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="4983e-3288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4983e-3289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3289">Az.Sql</span></span>

* <span data-ttu-id="4983e-3290">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4983e-3290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4983e-3291">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="4983e-3291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4983e-3292">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="4983e-3292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4983e-3293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3293">Az.Storage</span></span>

* <span data-ttu-id="4983e-3294">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-3294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4983e-3295">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="4983e-3295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4983e-3296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-3296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4983e-3297">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="4983e-3297">Support Static Website configuration</span></span>
    - <span data-ttu-id="4983e-3298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4983e-3298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4983e-3299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4983e-3299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4983e-3300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3300">Az.Websites</span></span>

* <span data-ttu-id="4983e-3301">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4983e-3301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="4983e-3302">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4983e-3302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4983e-3303">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4983e-3303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4983e-3304">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4983e-3305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4983e-3305">Az.ApiManagement</span></span>
* <span data-ttu-id="4983e-3306">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4983e-3306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4983e-3307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4983e-3307">Az.Automation</span></span>
* <span data-ttu-id="4983e-3308">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="4983e-3308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4983e-3309">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-3309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4983e-3310">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-3310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4983e-3311">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="4983e-3311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4983e-3312">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="4983e-3312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4983e-3313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3313">Az.Compute</span></span>
* <span data-ttu-id="4983e-3314">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4983e-3314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4983e-3315">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4983e-3315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4983e-3316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3316">Az.ContainerInstance</span></span>
* <span data-ttu-id="4983e-3317">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4983e-3317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4983e-3318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4983e-3318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4983e-3319">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="4983e-3319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4983e-3320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3320">Az.Network</span></span>
* <span data-ttu-id="4983e-3321">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-3321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4983e-3322">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="4983e-3322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4983e-3323">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="4983e-3323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="4983e-3324">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4983e-3324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4983e-3325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4983e-3325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4983e-3326">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="4983e-3326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4983e-3327">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="4983e-3327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4983e-3328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4983e-3328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4983e-3329">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4983e-3329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4983e-3330">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4983e-3330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4983e-3331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4983e-3331">Az.Relay</span></span>
* <span data-ttu-id="4983e-3332">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4983e-3332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4983e-3333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3333">Az.Resources</span></span>
* <span data-ttu-id="4983e-3334">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4983e-3334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4983e-3335">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="4983e-3335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4983e-3336">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4983e-3336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4983e-3337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-3337">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-3338">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="4983e-3338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4983e-3339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3339">Az.Sql</span></span>
* <span data-ttu-id="4983e-3340">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="4983e-3340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4983e-3341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4983e-3342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4983e-3343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4983e-3344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4983e-3344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4983e-3345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4983e-3345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4983e-3346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4983e-3346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4983e-3347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4983e-3347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4983e-3348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4983e-3348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4983e-3349">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4983e-3349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4983e-3350">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4983e-3350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4983e-3351">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="4983e-3351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4983e-3352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4983e-3352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4983e-3353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4983e-3353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4983e-3354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4983e-3354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4983e-3355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4983e-3355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4983e-3356">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4983e-3356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4983e-3357">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4983e-3358">Geral</span><span class="sxs-lookup"><span data-stu-id="4983e-3358">General</span></span>
* <span data-ttu-id="4983e-3359">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="4983e-3359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4983e-3360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4983e-3360">Az.Profile</span></span>
* <span data-ttu-id="4983e-3361">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4983e-3361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4983e-3362">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="4983e-3362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4983e-3363">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4983e-3363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4983e-3364">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="4983e-3364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4983e-3365">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="4983e-3365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4983e-3366">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4983e-3366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4983e-3367">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="4983e-3367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-3368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3368">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-3369">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4983e-3369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3370">Az.Compute</span></span>
* <span data-ttu-id="4983e-3371">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4983e-3371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4983e-3372">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4983e-3372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4983e-3373">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="4983e-3373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3374">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-3375">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4983e-3375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4983e-3376">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="4983e-3376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4983e-3377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4983e-3377">Az.Insights</span></span>
* <span data-ttu-id="4983e-3378">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="4983e-3378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4983e-3379">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="4983e-3379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4983e-3380">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="4983e-3380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4983e-3381">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="4983e-3381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-3382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3382">Az.Network</span></span>
* <span data-ttu-id="4983e-3383">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="4983e-3383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4983e-3384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-3384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4983e-3385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4983e-3385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4983e-3386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4983e-3386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4983e-3387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4983e-3387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4983e-3388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4983e-3388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4983e-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4983e-3389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4983e-3390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4983e-3390">Az.PolicyInsights</span></span>
* <span data-ttu-id="4983e-3391">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="4983e-3391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3392">Az.Resources</span></span>
* <span data-ttu-id="4983e-3393">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4983e-3393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4983e-3394">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="4983e-3394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4983e-3395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4983e-3395">Az.ServiceBus</span></span>
* <span data-ttu-id="4983e-3396">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="4983e-3396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4983e-3397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4983e-3397">Az.ServiceFabric</span></span>
* <span data-ttu-id="4983e-3398">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="4983e-3398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4983e-3399">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="4983e-3399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4983e-3400">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4983e-3400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4983e-3401">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4983e-3401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4983e-3402">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="4983e-3402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4983e-3403">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4983e-3404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4983e-3404">Az.Profile</span></span>
* <span data-ttu-id="4983e-3405">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="4983e-3405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4983e-3406">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4983e-3406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3407">Az.Compute</span></span>
* <span data-ttu-id="4983e-3408">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="4983e-3408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4983e-3409">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4983e-3409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4983e-3410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4983e-3410">Az.DataLakeStore</span></span>
* <span data-ttu-id="4983e-3411">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4983e-3411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4983e-3412">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4983e-3412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4983e-3413">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4983e-3413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4983e-3414">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4983e-3414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4983e-3415">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4983e-3415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-3416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3416">Az.Network</span></span>
* <span data-ttu-id="4983e-3417">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="4983e-3417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4983e-3418">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4983e-3418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3419">Az.Resources</span></span>
* <span data-ttu-id="4983e-3420">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="4983e-3420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4983e-3421">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="4983e-3421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4983e-3422">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4983e-3423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4983e-3423">Azure.Storage</span></span>
* <span data-ttu-id="4983e-3424">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="4983e-3424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4983e-3425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-3425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4983e-3426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4983e-3426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4983e-3427">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4983e-3427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4983e-3428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4983e-3428">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4983e-3429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4983e-3429">Az.CognitiveServices</span></span>
* <span data-ttu-id="4983e-3430">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="4983e-3430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4983e-3431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4983e-3431">Az.Compute</span></span>
* <span data-ttu-id="4983e-3432">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="4983e-3432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4983e-3433">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4983e-3433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4983e-3434">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="4983e-3434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4983e-3435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4983e-3435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4983e-3436">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4983e-3436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4983e-3437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4983e-3437">Az.Network</span></span>
* <span data-ttu-id="4983e-3438">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="4983e-3438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4983e-3439">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="4983e-3439">new cmdlets added</span></span>
    - <span data-ttu-id="4983e-3440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4983e-3440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4983e-3441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4983e-3441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4983e-3442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4983e-3442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4983e-3443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4983e-3443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4983e-3444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-3444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4983e-3445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-3445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4983e-3446">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="4983e-3446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4983e-3447">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4983e-3447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4983e-3448">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4983e-3448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4983e-3449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4983e-3449">Az.RedisCache</span></span>
* <span data-ttu-id="4983e-3450">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="4983e-3450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4983e-3451">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4983e-3451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4983e-3452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4983e-3452">Az.Resources</span></span>
* <span data-ttu-id="4983e-3453">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4983e-3453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4983e-3454">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="4983e-3454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4983e-3455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4983e-3455">Az.Sql</span></span>
* <span data-ttu-id="4983e-3456">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="4983e-3456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4983e-3457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4983e-3457">Az.Websites</span></span>
* <span data-ttu-id="4983e-3458">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="4983e-3458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4983e-3459">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4983e-3459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4983e-3460">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4983e-3460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4983e-3461">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="4983e-3461">Initial Release</span></span>