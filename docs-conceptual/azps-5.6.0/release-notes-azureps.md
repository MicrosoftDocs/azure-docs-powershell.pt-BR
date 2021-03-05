---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5c1366c40a4bdd8807a6e2a6716fbd959a573860
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872235"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="a18e8-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a18e8-103">Azure PowerShell release notes</span></span>

## <a name="560---march-2021"></a><span data-ttu-id="a18e8-104">5.6.0 – Março de 2021</span><span class="sxs-lookup"><span data-stu-id="a18e8-104">5.6.0 - March 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-105">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-106">Atualize o Azure.Identity para corrigir o problema em que Connect-AzAccount falha quando a credencial do ADFS é usada [#13560]</span><span class="sxs-lookup"><span data-stu-id="a18e8-106">Upgrade Azure.Identity to fix the issue that Connect-AzAccount fails when ADFS credential is used [#13560]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-107">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-107">Az.Automation</span></span>
* <span data-ttu-id="a18e8-108">Correção do problema em que a cadeia de caracteres não pode ser serializada corretamente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-108">Fixed the issue that string cannot be serialized correctly.</span></span> <span data-ttu-id="a18e8-109">[#14215]</span><span class="sxs-lookup"><span data-stu-id="a18e8-109">[#14215]</span></span>
* <span data-ttu-id="a18e8-110">Inclusão de suporte para o tipo de runbook Python3</span><span class="sxs-lookup"><span data-stu-id="a18e8-110">Added Support for Python3 Runbook Type</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-111">Az.Compute</span></span>
* <span data-ttu-id="a18e8-112">Inclusão do parâmetro '-EnableHotpatching' no cmdlet 'Set-AzVMOperatingSystem' para computadores Windows.</span><span class="sxs-lookup"><span data-stu-id="a18e8-112">Added parameter '-EnableHotpatching' to the 'Set-AzVMOperatingSystem' cmdlet for Windows machines.</span></span> 
* <span data-ttu-id="a18e8-113">Inclusão do parâmetro '-PatchMode' aos conjuntos de parâmetros do Linux no cmdlet 'Set-AzVMOperatingSystem'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-113">Added parameter '-PatchMode' to the Linux parameter sets in the cmdlet 'Set-AzVMOperatingSystem'.</span></span> 
* <span data-ttu-id="a18e8-114">[Alteração interruptiva] Alterações interruptivas para os usuários na versão prévia pública do recurso de aplicação de patch de convidado de VM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-114">[Breaking Change] Breaking changes for users in the public preview for the VM Guest Patching feature.</span></span>
    - <span data-ttu-id="a18e8-115">Remoção da propriedade 'RebootStatus' do objeto 'Microsoft.Azure.Management.Compute.Models.LastPatchInstallationSummary'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-115">Removed property 'RebootStatus' from the 'Microsoft.Azure.Management.Compute.Models.LastPatchInstallationSummary' object.</span></span> 
    - <span data-ttu-id="a18e8-116">Remoção da propriedade 'StartedBy' do objeto 'Microsoft.Azure.Management.Compute.Models.LastPatchInstallationSummary'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-116">Removed property 'StartedBy' from the 'Microsoft.Azure.Management.Compute.Models.LastPatchInstallationSummary' object.</span></span>
    - <span data-ttu-id="a18e8-117">Alteração de nome da propriedade 'Kbid' para 'KbId' no objeto 'Microsoft.Azure.Management.Compute.Models.VirtualMachineSoftwarePatchProperties'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-117">Renamed property 'Kbid' to 'KbId' in the 'Microsoft.Azure.Management.Compute.Models.VirtualMachineSoftwarePatchProperties' object.</span></span> 
    - <span data-ttu-id="a18e8-118">Alteração de nome da propriedade 'patches' para 'availablePatches' no objeto 'Microsoft.Azure.Management.Compute.Models.VirtualMachineAssessPatchesResult'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-118">Renamed property 'patches' to 'availablePatches' in the 'Microsoft.Azure.Management.Compute.Models.VirtualMachineAssessPatchesResult' object.</span></span> 
    - <span data-ttu-id="a18e8-119">Alteração de nome do objeto 'Microsoft.Azure.Management.Compute.Models.SoftwareUpdateRebootBehavior' para 'Microsoft.Azure.Management.Compute.Models.VMGuestPatchRebootBehavior'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-119">Renamed object 'Microsoft.Azure.Management.Compute.Models.SoftwareUpdateRebootBehavior' to 'Microsoft.Azure.Management.Compute.Models.VMGuestPatchRebootBehavior'.</span></span>
    - <span data-ttu-id="a18e8-120">Alteração de nome do objeto 'Microsoft.Azure.Management.Compute.Models.InGuestPatchMode' para 'Microsoft.Azure.Management.Compute.Models.WindowsVMGuestPatchMode'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-120">Renamed object 'Microsoft.Azure.Management.Compute.Models.InGuestPatchMode' to 'Microsoft.Azure.Management.Compute.Models.WindowsVMGuestPatchMode'.</span></span>
* <span data-ttu-id="a18e8-121">[Alteração interruptiva] Remoção de todos os cmdlets 'ContainerService'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-121">[Breaking Change] Removed all 'ContainerService' cmdlets.</span></span> <span data-ttu-id="a18e8-122">A API do Serviço de Contêiner foi preterida em janeiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="a18e8-122">The Container Service API was deprecated in January 2020.</span></span> 
    - <span data-ttu-id="a18e8-123">'Add-AzContainerServiceAgentPoolProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-123">'Add-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="a18e8-124">'Get-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-124">'Get-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-125">'New-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-125">'New-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-126">'New-AzContainerServiceConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-126">'New-AzContainerServiceConfig'</span></span>
    - <span data-ttu-id="a18e8-127">'Remove-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-127">'Remove-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-128">'Remove-AzContainerServiceAgentPoolProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-128">'Remove-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="a18e8-129">'Update-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-129">'Update-AzContainerService'</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-130">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-130">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-131">Correção da autenticação de `Connect-AzContainerRegistry`</span><span class="sxs-lookup"><span data-stu-id="a18e8-131">Fixed authentication for `Connect-AzContainerRegistry`</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="a18e8-132">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a18e8-132">Az.CosmosDB</span></span>
* <span data-ttu-id="a18e8-133">Introdução de NetworkAclBypass e NetworkAclBypassResourceIds para os cmdlets de Conta de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-133">Introduced NetworkAclBypass and NetworkAclBypassResourceIds for Database Account cmdlets.</span></span>
* <span data-ttu-id="a18e8-134">Introdução do parâmetro ServerVersion para Update-AzCosmosDBAccount.</span><span class="sxs-lookup"><span data-stu-id="a18e8-134">Introduced ServerVersion parameter to Update-AzCosmosDBAccount.</span></span>
* <span data-ttu-id="a18e8-135">Introdução de BackupInterval e BackupRetention para os cmdlets de Conta de Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="a18e8-135">Introduced BackupInterval and BackupRetention for Database Account cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-136">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-137">Atualização do SDK do .Net do ADF para a versão 4.14.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-137">Updated ADF .Net SDK version to 4.14.0</span></span>

#### <a name="azmigrate"></a><span data-ttu-id="a18e8-138">Az.Migrate</span><span class="sxs-lookup"><span data-stu-id="a18e8-138">Az.Migrate</span></span>
* <span data-ttu-id="a18e8-139">Az.Migrate em disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-139">Az.Migrate GA</span></span>
* <span data-ttu-id="a18e8-140">Incorporação de Initialize-AzMigrateReplicationInfrastructure como cmdlet no módulo Az.Migrate, do script externo que é executado hoje.</span><span class="sxs-lookup"><span data-stu-id="a18e8-140">Incorporated Initialize-AzMigrateReplicationInfrastructure as a cmdlet in the Az.Migrate module, from the external script that is run currently today.</span></span>
* <span data-ttu-id="a18e8-141">Alguns parâmetros de New-AzMigrateServerReplication, New-AzMigrateDiskMapping agora não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-141">Made some parameters of New-AzMigrateServerReplication, New-AzMigrateDiskMapping case insensitive.</span></span>
* <span data-ttu-id="a18e8-142">Inclusão de suporte para dimensionar a alteração do dispositivo para lidar com novas chaves V3.</span><span class="sxs-lookup"><span data-stu-id="a18e8-142">Added support for scale appliance change, to handle new V3 keys.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-143">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-143">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-144">Inclusão de verificação nula para a conta de armazenamento de destino na restauração de FileShare.</span><span class="sxs-lookup"><span data-stu-id="a18e8-144">Added null check for target storage account in FileShare restore.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-145">Az.Resources</span></span>
* <span data-ttu-id="a18e8-146">Inclusão de suporte para a implantação de recursos do Azure na linguagem Bicep</span><span class="sxs-lookup"><span data-stu-id="a18e8-146">Added support for Azure resources deployment in Bicep language</span></span>
* <span data-ttu-id="a18e8-147">Correção de problemas com as implantações TemplateSpec em 'New-AzTenantDeployment' e 'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-147">Fixed issues with TemplateSpec deployments in 'New-AzTenantDeployment' and 'New-AzManagementGroupDeployment'</span></span>
* <span data-ttu-id="a18e8-148">Inclusão de suporte ao parâmetro '-QueryString' nos cmdlets 'Test-Az\*Deployments'</span><span class="sxs-lookup"><span data-stu-id="a18e8-148">Added support for '-QueryString' parameter in 'Test-Az\*Deployments' cmdlets</span></span>
* <span data-ttu-id="a18e8-149">Correção do problema com os parâmetros dinâmicos quando 'New-Az\*Deployments' é usado com '-QueryString'</span><span class="sxs-lookup"><span data-stu-id="a18e8-149">Fixed issue with dynamic parameters when 'New-Az\*Deployments' is used with '-QueryString'</span></span>
* <span data-ttu-id="a18e8-150">Inclusão de suporte ao parâmetro '-TemplateParameterObject' quando o parâmetro '-TemplateSpecId' é usado em cmdlets 'New-Az\*Deployments'</span><span class="sxs-lookup"><span data-stu-id="a18e8-150">Added support for '-TemplateParameterObject' parameter while using '-TemplateSpecId' parameter in 'New-Az\*Deployments' cmdlets</span></span>
* <span data-ttu-id="a18e8-151">Correção da mensagem de erro incorreta recebida ao tentar implantar uma especificação de modelo não existente</span><span class="sxs-lookup"><span data-stu-id="a18e8-151">Fixed the inaccurate error message received on trying to deploy a non-existent template spec</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-152">Az.Storage</span></span>
* <span data-ttu-id="a18e8-153">Atualização para o Microsoft.Azure.Management.Storage 19.0.0 para oferecer suporte à nova versão da API 2021-01-01.</span><span class="sxs-lookup"><span data-stu-id="a18e8-153">Upgraded to Microsoft.Azure.Management.Storage 19.0.0, to support new API version 2021-01-01.</span></span>
* <span data-ttu-id="a18e8-154">Regra de acesso a recursos com suporte no NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-154">Supported resource access rule in NetworkRuleSet</span></span>
    - <span data-ttu-id="a18e8-155">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-155">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="a18e8-156">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-156">'Add-AzStorageAccountNetworkRule'</span></span>
    - <span data-ttu-id="a18e8-157">'Remove-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-157">'Remove-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="a18e8-158">Versão de blob com suporte e tipo de blob de acréscimo na política de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-158">Supported Blob version and Append Blob type in Management Policy</span></span>
    - <span data-ttu-id="a18e8-159">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="a18e8-159">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="a18e8-160">'New-AzStorageAccountManagementPolicyFilter'</span><span class="sxs-lookup"><span data-stu-id="a18e8-160">'New-AzStorageAccountManagementPolicyFilter'</span></span>
    - <span data-ttu-id="a18e8-161">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-161">'Set-AzStorageAccountManagementPolicy'</span></span>
* <span data-ttu-id="a18e8-162">Conta de criação/atualização com suporte com AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-162">Supported create/update account with AllowSharedKeyAccess</span></span>
    - <span data-ttu-id="a18e8-163">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-163">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a18e8-164">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-164">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-165">Criação de escopo de criptografia com suporte com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="a18e8-165">Supported create Encryption Scope with RequireInfrastructureEncryption</span></span>
    - <span data-ttu-id="a18e8-166">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-166">'New-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="a18e8-167">Cópia de blob de blocos com suporte síncrono, com escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="a18e8-167">Supported copy block blob synchronously, with encryption scope</span></span>
    - <span data-ttu-id="a18e8-168">'Copy-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-168">'Copy-AzStorageBlob'</span></span>
* <span data-ttu-id="a18e8-169">Correção do problema em que Get-AzStorageBlobContent usa o caractere separador de diretório incorreto no Linux e no MacOS [#14234]</span><span class="sxs-lookup"><span data-stu-id="a18e8-169">Fixed issue that Get-AzStorageBlobContent use wrong directory separator char on Linux and MacOS [#14234]</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-170">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-170">Az.Websites</span></span>
* <span data-ttu-id="a18e8-171">Introdução de uma opção para fornecer um tempo limite personalizado a 'Publish-AzWebApp'</span><span class="sxs-lookup"><span data-stu-id="a18e8-171">Introduced an option to give custom timeout for 'Publish-AzWebApp'</span></span> 
* <span data-ttu-id="a18e8-172">Inclusão de suporte para o Ambiente do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-172">Added support for App Service Environment</span></span>
    - <span data-ttu-id="a18e8-173">'New-AzAppServiceEnvironment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-173">'New-AzAppServiceEnvironment'</span></span>
    - <span data-ttu-id="a18e8-174">'Remove-AzAppServiceEnvironment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-174">'Remove-AzAppServiceEnvironment'</span></span>
    - <span data-ttu-id="a18e8-175">'Get-AzAppServiceEnvironment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-175">'Get-AzAppServiceEnvironment'</span></span>
    - <span data-ttu-id="a18e8-176">'New-AzAppServiceEnvironmentInboundServices'</span><span class="sxs-lookup"><span data-stu-id="a18e8-176">'New-AzAppServiceEnvironmentInboundServices'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-177">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-177">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-178">@alunmj, Pouca ortografia, alterações de formatação (#14155)</span><span class="sxs-lookup"><span data-stu-id="a18e8-178">@alunmj, Small spelling, formatting changes (#14155)</span></span>
* <span data-ttu-id="a18e8-179">@chakra146, Atualização de Add-AzLoadBalancerInboundNatPoolConfig.md (#14231)</span><span class="sxs-lookup"><span data-stu-id="a18e8-179">@chakra146, Update Add-AzLoadBalancerInboundNatPoolConfig.md (#14231)</span></span>
* <span data-ttu-id="a18e8-180">Martin Ehrnst (@ehrnst), correção de um erro de ortografia no cmdlet (#14112)</span><span class="sxs-lookup"><span data-stu-id="a18e8-180">Martin Ehrnst (@ehrnst), Fixed a typo in the cmdlet (#14112)</span></span>
* <span data-ttu-id="a18e8-181">Jan David Narkiewicz (@jdnark)</span><span class="sxs-lookup"><span data-stu-id="a18e8-181">Jan David Narkiewicz (@jdnark)</span></span>
  * <span data-ttu-id="a18e8-182">Os exemplos usaram o New-AzAks, que é o cmdlet herdado, e o alias para New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="a18e8-182">Examples used New-AzAks which is legacy cmdlet and the alias for New-AzAksCluster.</span></span> <span data-ttu-id="a18e8-183">Alteração dos exemplos para usar New-AzAksCluster, que é o cmdlet que esta página de documentação aborda.</span><span class="sxs-lookup"><span data-stu-id="a18e8-183">Changed examples to use New-AzAksCluster which is the cmdlet this documentation page targets.</span></span> <span data-ttu-id="a18e8-184">(#14088)</span><span class="sxs-lookup"><span data-stu-id="a18e8-184">(#14088)</span></span>
  * <span data-ttu-id="a18e8-185">Tipo Fox: alteração de SshKeyVaule para SshKeyValue (#14087)</span><span class="sxs-lookup"><span data-stu-id="a18e8-185">Type fox: changed SshKeyVaule to SshKeyValue (#14087)</span></span>
* <span data-ttu-id="a18e8-186">Ivan Kulezic (@kukislav), inclusão de exemplos de configuração de manutenção de Mi do SQL (#14216)</span><span class="sxs-lookup"><span data-stu-id="a18e8-186">Ivan Kulezic (@kukislav), Add sql mi maintenance configuration examples (#14216)</span></span>
* <span data-ttu-id="a18e8-187">@webguynj, Atualização de Set-AzNetworkSecurityRuleConfig.md (#14176)</span><span class="sxs-lookup"><span data-stu-id="a18e8-187">@webguynj, Update Set-AzNetworkSecurityRuleConfig.md (#14176)</span></span>
* <span data-ttu-id="a18e8-188">Yannick Dils (@yannickdils), inclusão de um cmdline adicional ao exemplo que aplica as alterações ao balanceador de carga (#14185)</span><span class="sxs-lookup"><span data-stu-id="a18e8-188">Yannick Dils (@yannickdils), Added an additional cmdline to the example which applies the changes to the load balancer (#14185)</span></span>

## <a name="550---february-2021"></a><span data-ttu-id="a18e8-189">5.5.0 – fevereiro de 2021</span><span class="sxs-lookup"><span data-stu-id="a18e8-189">5.5.0 - February 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-190">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-191">Código CloudError rastreado na exceção</span><span class="sxs-lookup"><span data-stu-id="a18e8-191">Tracked CloudError code in exception</span></span>
* <span data-ttu-id="a18e8-192">Evento 'ContextCleared' criado durante a execução de 'Clear-AzContext'</span><span class="sxs-lookup"><span data-stu-id="a18e8-192">Raised 'ContextCleared' event when 'Clear-AzContext' was executed</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-193">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-193">Az.Aks</span></span>
* <span data-ttu-id="a18e8-194">Mensagens de erro refinadas da falha no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a18e8-194">Refined error messages of cmdlet failure.</span></span>
* <span data-ttu-id="a18e8-195">Tratamento de exceções atualizado para usar exceções relacionadas ao Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a18e8-195">Upgraded exception handling to use Azure PowerShell related exceptions.</span></span>
* <span data-ttu-id="a18e8-196">Correção de um problema em que o usuário não podia usar a entidade de serviço fornecida para criar um cluster do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a18e8-196">Fixed the issue that user could not use provided service principal to create Kubernetes cluster.</span></span> <span data-ttu-id="a18e8-197">[#13938]</span><span class="sxs-lookup"><span data-stu-id="a18e8-197">[#13938]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-198">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-198">Az.Automation</span></span>
* <span data-ttu-id="a18e8-199">Correção de um problema de processamento de 'PSCustomObject' e 'Array'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-199">Fixed the issue of processing 'PSCustomObject' and 'Array'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-200">Az.Compute</span></span>
* <span data-ttu-id="a18e8-201">Parâmetro '-EnableAutomaticUpgrade' adicionado ao 'Set-AzVmExtension' e ao 'Add-AzVmssExtension'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-201">Added parameter '-EnableAutomaticUpgrade' to 'Set-AzVmExtension' and 'Add-AzVmssExtension'.</span></span>
* <span data-ttu-id="a18e8-202">Parâmetro FilterExpression removido da documentação do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-202">Removed FilterExpression parameter from 'Get-AzVMImage' cmdlet documentation.</span></span> 
* <span data-ttu-id="a18e8-203">Mensagem de substituição adicionada aos cmdlets de ContainerService:</span><span class="sxs-lookup"><span data-stu-id="a18e8-203">Added deprecation message to the ContainerService cmdlets:</span></span>
    - <span data-ttu-id="a18e8-204">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span><span class="sxs-lookup"><span data-stu-id="a18e8-204">'Add-AzureRmContainerServiceAgentPoolProfileCommand'</span></span>
    - <span data-ttu-id="a18e8-205">'Get-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-205">'Get-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-206">'New-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-206">'New-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-207">'New-AzContainerServiceConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-207">'New-AzContainerServiceConfig'</span></span>
    - <span data-ttu-id="a18e8-208">'Remove-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-208">'Remove-AzContainerService'</span></span>
    - <span data-ttu-id="a18e8-209">'Remove-AzContainerServiceAgentPoolProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-209">'Remove-AzContainerServiceAgentPoolProfile'</span></span>
    - <span data-ttu-id="a18e8-210">'Update-AzContainerService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-210">'Update-AzContainerService'</span></span>
* <span data-ttu-id="a18e8-211">Parâmetro '-BurstingEnabled' adicionado ao 'New-AzDiskConfig' e ao 'New-AzDiskUpdateConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-211">Added parameter '-BurstingEnabled' to 'New-AzDiskConfig' and 'New-AzDiskUpdateConfig'</span></span>
* <span data-ttu-id="a18e8-212">Parâmetros '-GroupByApplicationId' e '-GroupByUserAgent' adicionados aos cmdlets 'Export-AzLogAnalyticThrottledRequest' e 'Export-AzLogAnalyticRequestRateByInterval'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-212">Added '-GroupByApplicationId' and '-GroupByUserAgent' parameters to the 'Export-AzLogAnalyticThrottledRequest' and 'Export-AzLogAnalyticRequestRateByInterval' cmdlets.</span></span>
* <span data-ttu-id="a18e8-213">Conjunto de parâmetros 'VMParameterSet' adicionado ao cmdlet 'Get-AzVMExtension'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-213">Added 'VMParameterSet' parameter set to 'Get-AzVMExtension' cmdlet.</span></span> <span data-ttu-id="a18e8-214">Novo parâmetro '-VM' adicionado a esse conjunto de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a18e8-214">Added new parameter '-VM' to this parameter set.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-215">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-215">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-216">Cmdlets adicionados a operações com suporte de repositório, manifesto e marcação:</span><span class="sxs-lookup"><span data-stu-id="a18e8-216">Added cmdlets to supported repository, manifest, and tag operations:</span></span>
    - <span data-ttu-id="a18e8-217">'Get-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="a18e8-217">'Get-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="a18e8-218">'Update-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="a18e8-218">'Update-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="a18e8-219">'Remove-AzContainerRegistryRepository'</span><span class="sxs-lookup"><span data-stu-id="a18e8-219">'Remove-AzContainerRegistryRepository'</span></span>
    - <span data-ttu-id="a18e8-220">'Get-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="a18e8-220">'Get-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="a18e8-221">'Update-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="a18e8-221">'Update-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="a18e8-222">'Remove-AzContainerRegistryManifest'</span><span class="sxs-lookup"><span data-stu-id="a18e8-222">'Remove-AzContainerRegistryManifest'</span></span>
    - <span data-ttu-id="a18e8-223">'Get-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="a18e8-223">'Get-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="a18e8-224">'Update-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="a18e8-224">'Update-AzContainerRegistryTag'</span></span>
    - <span data-ttu-id="a18e8-225">'Remove-AzContainerRegistryTag'</span><span class="sxs-lookup"><span data-stu-id="a18e8-225">'Remove-AzContainerRegistryTag'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="a18e8-226">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="a18e8-226">Az.Databricks</span></span>
<span data-ttu-id="a18e8-227">Com suporte – Usar EnableNoPublicIP ao criar um workspace do Databricks</span><span class="sxs-lookup"><span data-stu-id="a18e8-227">Supported -EnableNoPublicIP when creating a Databricks workspace</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-228">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-228">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-229">Adição de FrontDoorId às propriedades</span><span class="sxs-lookup"><span data-stu-id="a18e8-229">Added FrontDoorId to properties</span></span>
* <span data-ttu-id="a18e8-230">Exclusões JSON e suporte RequestBodyCheck adicionados às regras gerenciadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-230">Added JSON Exclusions and RequestBodyCheck support to managed rules</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-231">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-231">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-232">Novos parâmetros '-EnableComputeIsolation' e '-ComputeIsolationHostSku' adicionados ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de isolamento de computação</span><span class="sxs-lookup"><span data-stu-id="a18e8-232">Added new parameter '-EnableComputeIsolation' and '-ComputeIsolationHostSku' to the cmdlet 'New-AzHDInsightCluster' to support compute isolation feature</span></span>
* <span data-ttu-id="a18e8-233">Propriedades 'ComputeIsolationProperties' e ' 'ConnectivityEndpoints' adicionadas à classe AzureHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a18e8-233">Added property 'ComputeIsolationProperties' and 'ConnectivityEndpoints' in the class AzureHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-234">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-235">Especificação do tipo de chave e do nome da curva compatível com a importação de chaves por meio de um arquivo BYOK</span><span class="sxs-lookup"><span data-stu-id="a18e8-235">Supported specifying key type and curve name when importing keys via a BYOK file</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-236">Az.Network</span></span>
* <span data-ttu-id="a18e8-237">Novos cmdlets adicionados para substituir 'virtual router', o nome anterior do produto, pelo nome 'route server' no futuro.</span><span class="sxs-lookup"><span data-stu-id="a18e8-237">Added new cmdlets to replace old product name 'virtual router' with new name 'route server' in the future.</span></span>
    - <span data-ttu-id="a18e8-238">'New-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-238">'New-AzRouteServer'</span></span>
    - <span data-ttu-id="a18e8-239">'Get-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-239">'Get-AzRouteServer'</span></span>
    - <span data-ttu-id="a18e8-240">'Remove-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-240">'Remove-AzRouteServer'</span></span>
    - <span data-ttu-id="a18e8-241">'Update-AzRouteServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-241">'Update-AzRouteServer'</span></span>
    - <span data-ttu-id="a18e8-242">'Get-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-242">'Get-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="a18e8-243">'Add-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-243">'Add-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="a18e8-244">'Update-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-244">'Update-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="a18e8-245">'Remove-AzRouteServerPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-245">'Remove-AzRouteServerPeer'</span></span>
    - <span data-ttu-id="a18e8-246">Aviso de substituição de atributo adicionado aos cmdlets anteriores.</span><span class="sxs-lookup"><span data-stu-id="a18e8-246">Added deprecation attribute warning to the old cmdlets.</span></span>
* <span data-ttu-id="a18e8-247">Correção de bug no MacSecConfig do ExpressRouteLink.</span><span class="sxs-lookup"><span data-stu-id="a18e8-247">Bug fix in ExpressRouteLink MacSecConfig.</span></span> <span data-ttu-id="a18e8-248">Nova propriedade 'SciState' adicionada ao 'PSExpressRouteLinkMacSecConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-248">Added new property 'SciState' to 'PSExpressRouteLinkMacSecConfig'</span></span>
* <span data-ttu-id="a18e8-249">Atualização da lista de formatos e de modos de exibição de tabelas de formatos para Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="a18e8-249">Updated format list and format table views for Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-250">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-251">Cancelamento de alterações feitas no PowerShell que aumentaram o limite de linhas de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-251">Retracted changes made in powershell that increased request row limit.</span></span> <span data-ttu-id="a18e8-252">Instrução incorreta removida da paginação de suporte</span><span class="sxs-lookup"><span data-stu-id="a18e8-252">Removed incorrect statement of supporting paging</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-254">limites de validação de política modificados de acordo com o serviço de backup.</span><span class="sxs-lookup"><span data-stu-id="a18e8-254">modified policy validation limits as per backup service.</span></span>
* <span data-ttu-id="a18e8-255">Redundância de Zona adicionada aos Cofres do Serviço de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-255">Added Zone Redundancy for Recovery Service Vaults.</span></span> 
* <span data-ttu-id="a18e8-256">Suporte do Azure Site Recovery para um grupo de posicionamento por proximidade para VMware no Azure e no Hyper-V para provedores do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-256">Azure Site Recovery support for Proximity placement group for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="a18e8-257">Suporte do Azure Site Recovery para uma zona de disponibilidade para VMware no Azure e no Hyper-V para provedores do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-257">Azure Site Recovery support for Availability zone for VMware to Azure and HyperV to Azure providers.</span></span>
* <span data-ttu-id="a18e8-258">Suporte do Azure Site Recovery para UseManagedDisk para Hyper-V no provedor do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-258">Azure Site Recovery support for UseManagedDisk for HyperV to Azure provider</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-259">Az.Resources</span></span>
* <span data-ttu-id="a18e8-260">Remoção do tipo de entidade de segurança em New-AzRoleAssignment e Set-AzRoleAssignment porque o mapeamento atual estava interrompendo determinados cenários</span><span class="sxs-lookup"><span data-stu-id="a18e8-260">Removed principal type on New-AzRoleAssignment and Set-AzRoleAssignment because current mapping was breaking certain scenarios</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-261">Az.Sql</span></span>
* <span data-ttu-id="a18e8-262">Adição de MaintenanceConfigurationId a 'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' e 'Set-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-262">Added MaintenanceConfigurationId to 'New-AzSqlDatabase', 'Set-AzSqlDatabase', 'New-AzSqlElasticPool' and 'Set-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a18e8-263">Correção de regressão em 'Set-AzSqlServerAudit' durante o fornecimento do argumento PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="a18e8-263">Fixed regression in 'Set-AzSqlServerAudit' when PredicateExpression argument is provided</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-264">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-264">Az.Storage</span></span>
* <span data-ttu-id="a18e8-265">Configurações de RoutingPreference compatíveis com a opção criar/atualizar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-265">Supported RoutingPreference settings in create/update Storage account</span></span>
    - <span data-ttu-id="a18e8-266">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-266">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a18e8-267">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-267">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-268">Atualização de Azure.Storage.Blobs para 12.8.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-268">Upgraded Azure.Storage.Blobs to 12.8.0</span></span>
* <span data-ttu-id="a18e8-269">Atualização de Azure.Storage.Files.Shares para 12.6.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-269">Upgraded Azure.Storage.Files.Shares to 12.6.0</span></span>
* <span data-ttu-id="a18e8-270">Atualização de Azure.Storage.Files.DataLake para 12.6.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-270">Upgraded Azure.Storage.Files.DataLake to 12.6.0</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-271">Az.Websites</span></span>
* <span data-ttu-id="a18e8-272">Adição de suporte para a Importação de um certificado do cofre de chaves no WebApp.</span><span class="sxs-lookup"><span data-stu-id="a18e8-272">Added support for Importing a key vault certificate to WebApp.</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-273">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-273">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-274">@atul-ram: atualização do Set-AzEventHub.md (nº 13921)</span><span class="sxs-lookup"><span data-stu-id="a18e8-274">@atul-ram, Update Set-AzEventHub.md (#13921)</span></span>
* <span data-ttu-id="a18e8-275">Christoph Bergmeister [MVP] (@bergmeister): Set-AzDataLakeGen2AclRecursive.md – Correção de erro de digitação (directiry -> directory) (nº 14082)</span><span class="sxs-lookup"><span data-stu-id="a18e8-275">Christoph Bergmeister [MVP] (@bergmeister), Set-AzDataLakeGen2AclRecursive.md - Fix typo (directiry -> directory) (#14082)</span></span>
* <span data-ttu-id="a18e8-276">Alexander Schmidt (@devdeer-alex): correção de link desfeito para acessar diretrizes de contribuição (nº 14009)</span><span class="sxs-lookup"><span data-stu-id="a18e8-276">Alexander Schmidt (@devdeer-alex), Fixed broken link to contribution guidelines (#14009)</span></span>
* <span data-ttu-id="a18e8-277">@JiangYuchun: atualização do Get-AzApplicationGatewayAuthenticationCertificate.md (nº 13972)</span><span class="sxs-lookup"><span data-stu-id="a18e8-277">@JiangYuchun, Update Get-AzApplicationGatewayAuthenticationCertificate.md (#13972)</span></span>
* <span data-ttu-id="a18e8-278">Sebastián Olsen (@Spacebjorn): comando de exemplo corrigido (nº 13901)</span><span class="sxs-lookup"><span data-stu-id="a18e8-278">Sebastian Olsen (@Spacebjorn), Corrected example command (#13901)</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="a18e8-279">5.4.0 – janeiro de 2021</span><span class="sxs-lookup"><span data-stu-id="a18e8-279">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-280">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-281">ID de solicitação do cliente correta mostrada na mensagem de depuração [nº 13745]</span><span class="sxs-lookup"><span data-stu-id="a18e8-281">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="a18e8-282">Tipo de exceção comum do Azure PowerShell adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-282">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="a18e8-283">API 2019-06-01 de armazenamento com suporte</span><span class="sxs-lookup"><span data-stu-id="a18e8-283">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-284">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-284">Az.Automation</span></span>
* <span data-ttu-id="a18e8-285">O problema em que a descrição não era populada para agendamentos de gerenciamento de atualizações foi corrigido</span><span class="sxs-lookup"><span data-stu-id="a18e8-285">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="a18e8-286">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a18e8-286">Az.CosmosDB</span></span>
* <span data-ttu-id="a18e8-287">Disponibilidade geral do módulo 'Az.CosmosDB'</span><span class="sxs-lookup"><span data-stu-id="a18e8-287">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="a18e8-288">Restrição do cmdlet New-AzCosmosDBAccount para fazer chamadas de atualização para Contas de Banco de Dados existentes.</span><span class="sxs-lookup"><span data-stu-id="a18e8-288">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="a18e8-289">Introdução do AnalyticalStorageTTL em SqlContainer.</span><span class="sxs-lookup"><span data-stu-id="a18e8-289">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-290">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-290">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-291">Regressão relativa à geração de token SAS corrigida</span><span class="sxs-lookup"><span data-stu-id="a18e8-291">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-292">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-293">Problema no módulo Gerenciamento de Segredos corrigido</span><span class="sxs-lookup"><span data-stu-id="a18e8-293">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-294">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-295">Problema em que 'Get-AzLogicAppTriggerHistory' e 'Get-AzLogicAppRunAction' só recuperavam a primeira página de resultados corrigido [Nº 9141]</span><span class="sxs-lookup"><span data-stu-id="a18e8-295">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-296">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-296">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-297">Cmdlets adicionados para regras de coleta de dados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-297">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="a18e8-298">'Get-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-298">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="a18e8-299">'New-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-299">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="a18e8-300">'Set-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-300">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="a18e8-301">'Update-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-301">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="a18e8-302">'Remove-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-302">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="a18e8-303">Cmdlets adicionados para associações de regras de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="a18e8-303">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="a18e8-304">'Get-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-304">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="a18e8-305">'New-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-305">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="a18e8-306">'Remove-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-306">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-307">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-307">Az.Network</span></span>
* <span data-ttu-id="a18e8-308">Novos cmdlets adicionados para CRUD de VpnGatewayNATRule.</span><span class="sxs-lookup"><span data-stu-id="a18e8-308">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="a18e8-309">'New-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-309">'New-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="a18e8-310">'Update-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-310">'Update-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="a18e8-311">'Get-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-311">'Get-AzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="a18e8-312">'Remove-AzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-312">'Remove-AzVpnGatewayNatRule'</span></span>  
* <span data-ttu-id="a18e8-313">Cmdlets atualizados para definir NATRule no recurso VpnGateway e associá-lo ao recurso VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="a18e8-313">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="a18e8-314">'New-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-314">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="a18e8-315">'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-315">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="a18e8-316">'New-AzVpnSiteLinkConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-316">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="a18e8-317">Cmdlets atualizados para habilitar a configuração de ConnectionMode em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a18e8-317">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a18e8-318">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-318">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a18e8-319">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-319">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a18e8-320">Cmdlet 'New-AzFirewallPolicyApplicationRule' atualizado:</span><span class="sxs-lookup"><span data-stu-id="a18e8-320">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="a18e8-321">Parâmetro TargetUrl adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-321">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="a18e8-322">Parâmetro TerminateTLS adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-322">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="a18e8-323">Novos cmdlets adicionados para recursos Premium do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-323">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="a18e8-324">'New-AzFirewallPolicyIntrusionDetection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-324">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="a18e8-325">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span><span class="sxs-lookup"><span data-stu-id="a18e8-325">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="a18e8-326">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span><span class="sxs-lookup"><span data-stu-id="a18e8-326">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="a18e8-327">Cmdlet New-AzFirewallPolicy atualizado:</span><span class="sxs-lookup"><span data-stu-id="a18e8-327">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="a18e8-328">Parâmetro -SkuTier adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-328">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="a18e8-329">Parâmetro -Identity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-329">Added parameter -Identity</span></span>
    - <span data-ttu-id="a18e8-330">Parâmetro -UserAssignedIdentityId adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-330">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="a18e8-331">Parâmetro -IntrusionDetection adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-331">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="a18e8-332">Parâmetro -TransportSecurityName adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-332">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="a18e8-333">Parâmetro -TransportSecurityKeyVaultSecretId adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-333">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="a18e8-334">Novo cmdlet para buscar Associações de Segurança IKE para Conexões de Gateway de Rede Virtual adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-334">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a18e8-335">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span><span class="sxs-lookup"><span data-stu-id="a18e8-335">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="a18e8-336">Suporte a várias autenticações para p2sVpnGateway adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-336">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="a18e8-337">New-AzVpnServerConfiguration e Update-AzVpnServerConfiguration adicionados para permitir que vários parâmetros de autenticação sejam definidos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-337">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="a18e8-338">Cmdlet 'New-AzVpnGateway' e 'New-AzP2sVpnGateway' atualizado:</span><span class="sxs-lookup"><span data-stu-id="a18e8-338">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="a18e8-339">Parâmetro EnableRoutingPreferenceInternetFlag adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-339">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-340">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-340">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-341">Recurso Restauração entre Regiões adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-341">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="a18e8-342">Obtenção de configuração de carga de trabalho bloqueada quando o item de destino é um grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="a18e8-342">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-343">Az.Resources</span></span>
* <span data-ttu-id="a18e8-344">Suporte adicionado para o parâmetro -QueryString em cmdlets New-AZ\*Deployments</span><span class="sxs-lookup"><span data-stu-id="a18e8-344">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-345">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-345">Az.Sql</span></span>
* <span data-ttu-id="a18e8-346">Cmdlet 'Start-AzSqlInstanceDatabaseLogReplay' tornado síncrono, sinalizador -AsJob adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-346">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-347">Az.Storage</span></span>
* <span data-ttu-id="a18e8-348">ContinuationToken corrigido para nunca nulo na listagem de blobs com -IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-348">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="a18e8-349">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-349">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-350">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-350">Az.Websites</span></span>
* <span data-ttu-id="a18e8-351">Suporte adicionado para certificados Gerenciados do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-351">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="a18e8-352">'New-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-352">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="a18e8-353">'Remove-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-353">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="a18e8-354">Problema que fazia com que a Senha do Docker fosse removida de appSettings em 'Set-AzWebApp' e 'Set-AzWebAppSlot' corrigido</span><span class="sxs-lookup"><span data-stu-id="a18e8-354">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-355">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-355">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-356">Ivan Akcheurov (@ivanakcheurov), por atualizar Set-AzSecurityWorkspaceSetting.md (Nº 13877)</span><span class="sxs-lookup"><span data-stu-id="a18e8-356">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="a18e8-357">@javiermarasco, atualização de exemplo (Nº 13837)</span><span class="sxs-lookup"><span data-stu-id="a18e8-357">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="a18e8-358">@jhaprakash26, Atualização de Set-AzVirtualNetwork.md (Nº 13857)</span><span class="sxs-lookup"><span data-stu-id="a18e8-358">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="a18e8-359">Michael Holmes (@MichaelHolmesWP), por atualizar New-AzStorageTableStoredAccessPolicy.md (#13871)</span><span class="sxs-lookup"><span data-stu-id="a18e8-359">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="a18e8-360">Michael James (@mikejwhat), por permitir que Get-AzLogicAppTriggerHistory e Get-AzLogicAppRunAction retornem mais de 30 resultados (Nº 13846)</span><span class="sxs-lookup"><span data-stu-id="a18e8-360">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="a18e8-361">@Willem-J-an, correção de bug que fazia a senha do Docker ser removida de appsettings em Set-AzWebApp(Slot) (Nº 13866)</span><span class="sxs-lookup"><span data-stu-id="a18e8-361">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="a18e8-362">5.3.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-362">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-363">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-363">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-364">Foi corrigido o problema em que o proxy http não é respeitado no Windows PowerShell [n. 13647]</span><span class="sxs-lookup"><span data-stu-id="a18e8-364">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="a18e8-365">Foi aprimorado o log de depuração de operações de execução prolongada em módulos gerados</span><span class="sxs-lookup"><span data-stu-id="a18e8-365">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-366">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-366">Az.Automation</span></span>
* <span data-ttu-id="a18e8-367">Foi corrigido o problema em que os parâmetros de 'Start-AzAutomationRunbook' não podem converter a cadeia de caracteres encapsulada de PSObject em cadeia de caracteres JSON [#13240]</span><span class="sxs-lookup"><span data-stu-id="a18e8-367">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="a18e8-368">Foi corrigido o preenchedor de localização para o cmdlet New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="a18e8-368">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-369">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-369">Az.Compute</span></span>
* <span data-ttu-id="a18e8-370">Novo parâmetro 'VM' no novo conjunto de parâmetros 'VMParameterSet' adicionado aos cmdlets 'Get-AzVMDscExtensionStatus' e 'Get-AzVMDscExtension'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-370">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="a18e8-371">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="a18e8-371">Az.Databricks</span></span>
* <span data-ttu-id="a18e8-372">Foi corrigido um problema que fazia com que 'New-AzDatabricksVNetPeering' fosse retornado antes de ser totalmente provisionado (https://github.com/Azure/autorest.powershell/issues/610) )</span><span class="sxs-lookup"><span data-stu-id="a18e8-372">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-373">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-373">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-374">Foi corrigido o problema do comando ' Invoke-AzDataFactoryV2Pipeline' para SupportsShouldProcess</span><span class="sxs-lookup"><span data-stu-id="a18e8-374">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a18e8-375">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a18e8-375">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a18e8-376">Foi adicionada a propriedade StartVMOnConnect ao pool de host.</span><span class="sxs-lookup"><span data-stu-id="a18e8-376">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-377">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-377">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-378">Propriedades adicionadas: FQDN e EffectiveDiskEncryptionKeyUrl na classe AzureHDInsightHostInfo.</span><span class="sxs-lookup"><span data-stu-id="a18e8-378">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-379">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-380">Foi adicionado um novo parâmetro '-AsPlainText' a 'Get-AzKeyVaultSecret' para retornar diretamente o segredo em texto sem formatação [n. 13630]</span><span class="sxs-lookup"><span data-stu-id="a18e8-380">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="a18e8-381">Foi adicionado suporte à restauração seletiva de uma chave de um backup completo de HSM gerenciado [n. 13526]</span><span class="sxs-lookup"><span data-stu-id="a18e8-381">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="a18e8-382">Foram corrigidos alguns problemas secundários [n. 13583] [n. 13584]</span><span class="sxs-lookup"><span data-stu-id="a18e8-382">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="a18e8-383">Foram adicionados objetos de retorno ausentes de 'Get-Secret' no módulo SecretManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-383">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="a18e8-384">Foi corrigido um problema que pode fazer com que o cofre seja criado sem a política de acesso padrão [n. 13687]</span><span class="sxs-lookup"><span data-stu-id="a18e8-384">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="a18e8-385">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="a18e8-385">Az.Kusto</span></span>
* <span data-ttu-id="a18e8-386">Versão da API atualizada para a versão de 18/09/2020.</span><span class="sxs-lookup"><span data-stu-id="a18e8-386">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-387">Az.Network</span></span>
* <span data-ttu-id="a18e8-388">Foi corrigido problema no cmdlet de remoção e emparelhamento e conexão para o cenário ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a18e8-388">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="a18e8-389">'Remove-AzExpressRouteCircuitPeeringConfig' e 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-389">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-390">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-391">Foi adicionado suporte para retorno de resultados paginados para Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a18e8-391">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-392">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-392">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-393">Foi habilitado o recurso de exclusão temporária para SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-393">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="a18e8-394">Foi corrigida a restauração do SQL AG e removida a verificação do nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a18e8-394">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="a18e8-395">Foi alterado o formato de nome de contêiner para o item de backup de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-395">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="a18e8-396">Foi adicionado suporte de recurso CMK para ações do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-396">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-397">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-397">Az.Resources</span></span>
* <span data-ttu-id="a18e8-398">Foi corrigido um problema de exceção de NullRef em 'New-AzureManagedApplication' e 'Set-AzureManagedApplication'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-398">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="a18e8-399">Foi atualizado o SDK do Azure Resource Manager para uso da versão mais recente em GA da API do DeploymentScripts: 01/10/2020.</span><span class="sxs-lookup"><span data-stu-id="a18e8-399">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-400">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-400">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-401">Correção do 'Add-AzServiceFabricNodeType'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-401">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="a18e8-402">Foi adicionado um tipo de nó ao cluster do Service Fabric antes da criação de um conjunto de dimensionamento de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a18e8-402">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-403">Az.Sql</span></span>
* <span data-ttu-id="a18e8-404">Foi corrigida a descrição do parâmetro fixo para o comando 'InstanceFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-404">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="a18e8-405">Foi atualizada a lógica em que schemaName, tableName e columnName estão sendo extraídos da ID dos comandos da Classificação de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-405">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="a18e8-406">Foram corrigidos os campos Status e StatusMessage em 'Get-AzSqlDatabaseImportExportStatus' para estar em conformidade com a documentação</span><span class="sxs-lookup"><span data-stu-id="a18e8-406">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="a18e8-407">Foram adicionados cmdlets de auditoria do DevOps (operações de suporte da Microsoft): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-407">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-408">Az.Storage</span></span>
* <span data-ttu-id="a18e8-409">Foi adicionado suporte à criação/atualização/obtenção/listagem de EncryptionScope de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-409">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="a18e8-410">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-410">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="a18e8-411">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-411">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="a18e8-412">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-412">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="a18e8-413">Foi adicionado suporte para a criação de contêineres e o upload de blobs com a configuração Escopo de Criptografia</span><span class="sxs-lookup"><span data-stu-id="a18e8-413">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="a18e8-414">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-414">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="a18e8-415">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-415">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="a18e8-416">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-416">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-417">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-417">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-418">Andreas Wolter (@AndreasWolter), idioma de marketing removido, melhor filtro de exemplo (n. 13671)</span><span class="sxs-lookup"><span data-stu-id="a18e8-418">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="a18e8-419">Tidjani Belmansour (@BelRarr), Get-AzBillingInvoice.md atualizado (n. 13634)</span><span class="sxs-lookup"><span data-stu-id="a18e8-419">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="a18e8-420">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="a18e8-420">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="a18e8-421">Foi corrigido um erro de ortografia (n. 13677)</span><span class="sxs-lookup"><span data-stu-id="a18e8-421">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="a18e8-422">Atualização do PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="a18e8-422">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="a18e8-423">@kilobyte97, correção de bug para a exclusão da configuração pelo cmdlet remove (n. 13655)</span><span class="sxs-lookup"><span data-stu-id="a18e8-423">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="a18e8-424">@kongou-ae, atualização do Set-AzFirewall.md (n. 13727)</span><span class="sxs-lookup"><span data-stu-id="a18e8-424">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="a18e8-425">@MasterKuat, correção da troca entre título e código na documentação (n. 13666)</span><span class="sxs-lookup"><span data-stu-id="a18e8-425">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="a18e8-426">NickT (@nukeulis), atualização do Set-AzContext.md (n. 13702)</span><span class="sxs-lookup"><span data-stu-id="a18e8-426">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="a18e8-427">@PaulHCode, atualização do Start-AzJitNetworkAccessPolicy.md – correção do exemplo para exibir o cmdlet adequado que está sendo demonstrado (n. 13713)</span><span class="sxs-lookup"><span data-stu-id="a18e8-427">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="a18e8-428">Ryan Borstelmann (@ryanborMSFT), ID da assinatura removida (n. 13715)</span><span class="sxs-lookup"><span data-stu-id="a18e8-428">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="a18e8-429">Shashikant Shakya (@shshakya), atualização do Set-AzSqlDatabase.md (n. 13674)</span><span class="sxs-lookup"><span data-stu-id="a18e8-429">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="a18e8-430">Sebastian Olsen (@Spacebjorn), atualização do Get-AzRecoveryServicesBackupItem.md (n. 13719)</span><span class="sxs-lookup"><span data-stu-id="a18e8-430">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="a18e8-431">5.2.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-431">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-432">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-433">Gerenciado para analisar o tempo de ExpiresOn do token bruto se não for possível obter da biblioteca subjacente</span><span class="sxs-lookup"><span data-stu-id="a18e8-433">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="a18e8-434">Mensagem de aviso aprimorada se a autenticação interativa não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="a18e8-434">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-435">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-436">[Alteração da falha] 'New-AzApiManagementProduct', por padrão, não tem limite de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-436">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-437">Az.Compute</span></span>
* <span data-ttu-id="a18e8-438">Get-AzVm editado para filtrar por '-Name' antes de verificar a limitação devido a muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-438">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="a18e8-439">Novo cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-439">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-440">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-440">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-441">Parâmetro 'Name' com suporte e valor da entrada de pipeline para 'Get-AzContainerRegistryUsage' [nº 13605]</span><span class="sxs-lookup"><span data-stu-id="a18e8-441">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="a18e8-442">Exceções refinadas para 'Connect-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="a18e8-442">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-443">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-444">SDK do .NET do ADF atualizado para a versão 4.13.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-444">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a18e8-445">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a18e8-445">Az.HealthcareApis</span></span>
* <span data-ttu-id="a18e8-446">Suporte adicionado para chaves gerenciadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="a18e8-446">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-447">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-447">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-448">Problema de token SAS corrigido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-448">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-449">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-449">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-450">'Todos' com suporte como uma opção quando são definidas políticas de acesso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a18e8-450">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="a18e8-451">Nova versão com suporte do módulo do SecretManagement [nº 13366]</span><span class="sxs-lookup"><span data-stu-id="a18e8-451">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="a18e8-452">ByteArray, String, PSCredential e Hashtable com suporte para 'SecretValue' em SecretManagementModule [nº 12190]</span><span class="sxs-lookup"><span data-stu-id="a18e8-452">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="a18e8-453">[Alteração da falha] Superfície de API de cmdlets recriada com relação ao HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-453">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-454">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-454">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-455">Parâmetro 'Rule' de 'New-AzAutoscaleProfile' alterado para aceitar lista vazia.</span><span class="sxs-lookup"><span data-stu-id="a18e8-455">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="a18e8-456">[Nº 12903]</span><span class="sxs-lookup"><span data-stu-id="a18e8-456">[#12903]</span></span>
* <span data-ttu-id="a18e8-457">Adição de novos cmdlets para dar suporte à criação de configurações de diagnóstico mais flexíveis:</span><span class="sxs-lookup"><span data-stu-id="a18e8-457">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="a18e8-458">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="a18e8-458">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="a18e8-459">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-459">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="a18e8-460">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-460">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-462">O texto de ajuda e o nome do conjunto de parâmetros foram alterados para o cmdlet 'Restore-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-462">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-463">Az.Resources</span></span>
* <span data-ttu-id="a18e8-464">Suporte ao parâmetro '-Tag' adicionado para 'Set-AzTemplateSpec' e 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="a18e8-464">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="a18e8-465">Suporte à exibição de marcas adicionado para o formatador padrão para Especificações de Modelo</span><span class="sxs-lookup"><span data-stu-id="a18e8-465">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-466">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-467">Exemplo adicionado para 'Set-AzServiceFabricSetting' com o parâmetro SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="a18e8-467">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="a18e8-468">Cmdlets relacionados a aplicativos atualizados para alertar que o suporte é apenas para recursos implantados do ARM</span><span class="sxs-lookup"><span data-stu-id="a18e8-468">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="a18e8-469">Cmdlets de certificado de cluster de 'Add-AzureRmServiceFabricClusterCertificate' e 'Remove-AzureRmServiceFabricClusterCertificate' marcados para substituição</span><span class="sxs-lookup"><span data-stu-id="a18e8-469">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-470">Az.Sql</span></span>
* <span data-ttu-id="a18e8-471">SecondaryType adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a18e8-471">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="a18e8-472">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-472">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="a18e8-473">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-473">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="a18e8-474">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="a18e8-474">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="a18e8-475">HighAvailabilityReplicaCount adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a18e8-475">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="a18e8-476">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-476">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="a18e8-477">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-477">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="a18e8-478">ReadReplicaCount tornado um alias de HighAvailabilityReplicaCount no seguinte:</span><span class="sxs-lookup"><span data-stu-id="a18e8-478">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="a18e8-479">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-479">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="a18e8-480">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-480">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-481">Az.Storage</span></span>
* <span data-ttu-id="a18e8-482">Upload de arquivos do Azure de até 4 TiB com suporte</span><span class="sxs-lookup"><span data-stu-id="a18e8-482">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="a18e8-483">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-483">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="a18e8-484">Azure.Storage.Blobs atualizado para 12.7.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-484">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="a18e8-485">Azure.Storage.Files.Shares atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-485">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="a18e8-486">Azure.Storage.Files.DataLake atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-486">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-487">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-487">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-488">Recurso de política de camadas de sincronização adicionado com política de download e modo de cache local</span><span class="sxs-lookup"><span data-stu-id="a18e8-488">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-489">Az.Websites</span></span>
* <span data-ttu-id="a18e8-490">Impedir regras de restrição de acesso duplicadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-490">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-491">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-491">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-492">Andrew Dawson (@dawsonar802), por atualizar Get-AzKeyVaultCertificate.md – obter certificado e salvá-lo como seção pfx para trabalhar com o PowerShell Core (nº 13557)</span><span class="sxs-lookup"><span data-stu-id="a18e8-492">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="a18e8-493">@iviark, por atualizações de APIs de saúde BYOK do Powershell (nº 13518)</span><span class="sxs-lookup"><span data-stu-id="a18e8-493">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="a18e8-494">John Duckmanton (@johnduckmanton), por corrigir a ortografia de TagPatchOperation (nº 13508)</span><span class="sxs-lookup"><span data-stu-id="a18e8-494">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="a18e8-495">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="a18e8-495">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="a18e8-496">Ajuda organizada do Get-AzLogicAppRunHistory (nº 13513)</span><span class="sxs-lookup"><span data-stu-id="a18e8-496">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="a18e8-497">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="a18e8-497">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="a18e8-498">Atualizar Update-AzAppConfigurationStore.md (nº 13485)</span><span class="sxs-lookup"><span data-stu-id="a18e8-498">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="a18e8-499">Atualizar New-AzCosmosDBAccount.md (nº 13490)</span><span class="sxs-lookup"><span data-stu-id="a18e8-499">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="a18e8-500">@SteppingRazor, New-AzApiManagementProduct: alterar o valor padrão do parâmetro SubscriptionsLimit para nenhum (nº 13457)</span><span class="sxs-lookup"><span data-stu-id="a18e8-500">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="a18e8-501">Steve Burkett (@SteveBurkettNZ), por corrigir erros de digitação para o parâmetro WorkspaceResourceId no exemplo (nº 13589)</span><span class="sxs-lookup"><span data-stu-id="a18e8-501">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="a18e8-502">5.1.0 – Novembro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-502">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-503">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-503">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-504">Correção de um problema em que a TenantId podia não ser respeitada se 'Connect-AzAccount -DeviceCode' [nº 13477] fosse usado</span><span class="sxs-lookup"><span data-stu-id="a18e8-504">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="a18e8-505">Adição do novo cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="a18e8-505">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="a18e8-506">Correção de um problema que ocorria quando o caminho do perfil do usuário estava inacessível</span><span class="sxs-lookup"><span data-stu-id="a18e8-506">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="a18e8-507">Correção de um problema que causava o erro Write-Object durante Connect-AzAccount [nº 13419]</span><span class="sxs-lookup"><span data-stu-id="a18e8-507">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="a18e8-508">Adição do parâmetro 'ContainerRegistryEndpointSuffix' a: 'Add-AzEnvironment', 'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-508">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="a18e8-509">Suporte à interrupção de logon com o clique em <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="a18e8-509">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="a18e8-510">Correção de um problema que fazia com que 'Connect-AzAccount -KeyVaultAccessToken' não funcionasse [nº 13127]</span><span class="sxs-lookup"><span data-stu-id="a18e8-510">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="a18e8-511">Correção da referência nula e da não diferenciação de maiúsculas e minúsculas no método em 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="a18e8-511">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-512">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-512">Az.Aks</span></span>
* <span data-ttu-id="a18e8-513">Correção do problema em que o usuário não podia usar a entidade de serviço para criar um cluster do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a18e8-513">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="a18e8-514">[nº 13012]</span><span class="sxs-lookup"><span data-stu-id="a18e8-514">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="a18e8-515">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-515">Az.AppConfiguration</span></span>
* <span data-ttu-id="a18e8-516">Disponibilidade geral do módulo 'Az.AppConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-516">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-517">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-517">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-518">Aprimoramento da mensagem de erro do comando 'New-AzDataFactoryV2LinkedServiceEncryptedCredential'</span><span class="sxs-lookup"><span data-stu-id="a18e8-518">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-519">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-519">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-520">Atualização do SDK do plano de dados do ADLS para 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="a18e8-520">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="a18e8-521">Alterações: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="a18e8-521">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a18e8-522">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a18e8-522">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a18e8-523">Adição de novos cmdlets do Pacote MSIX e atualização de cmdlets de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-523">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-524">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-524">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-525">Correção de comandos do cluster EventHub sem marcas</span><span class="sxs-lookup"><span data-stu-id="a18e8-525">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="a18e8-526">Atualização do texto da Ajuda de PartnerNamespace dos comandos AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-526">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-527">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-527">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-528">Adição dos parâmetros 'ResourceProviderConnection' e 'PrivateLink' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de link privado e saída de retransmissão</span><span class="sxs-lookup"><span data-stu-id="a18e8-528">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="a18e8-529">Adição do parâmetro 'AmbariDatabase' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de banco de dados personalizado do Ambari</span><span class="sxs-lookup"><span data-stu-id="a18e8-529">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="a18e8-530">Adição do valor de aceitação de 'AmbariDatabase' ao parâmetro 'MetastoreType' do cmdlet 'Add-AzHDInsightMetastore'</span><span class="sxs-lookup"><span data-stu-id="a18e8-530">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-531">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-531">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-532">Permissão de marcas no cmdlet create do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-532">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-533">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-534">Suporte à atualização de marcas do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a18e8-534">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-535">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-536">Correção de Get-AzLogicAppRunHistory, que só recuperava a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="a18e8-536">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-537">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-537">Az.Network</span></span>
* <span data-ttu-id="a18e8-538">Atualização do cmdlet indicado abaixo</span><span class="sxs-lookup"><span data-stu-id="a18e8-538">Updated below cmdlet</span></span> 
    - <span data-ttu-id="a18e8-539">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="a18e8-539">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="a18e8-540">Adição da propriedade PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a18e8-540">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="a18e8-541">Adição da propriedade PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="a18e8-541">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="a18e8-542">Adição de novas propriedades aos cmdlets a seguir para permitir o balanceamento de carga global</span><span class="sxs-lookup"><span data-stu-id="a18e8-542">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="a18e8-543">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="a18e8-543">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="a18e8-544">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="a18e8-544">Added Sku Tier property</span></span>
    - <span data-ttu-id="a18e8-545">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="a18e8-545">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="a18e8-546">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="a18e8-546">Added Sku Tier property</span></span>
    - <span data-ttu-id="a18e8-547">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="a18e8-547">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="a18e8-548">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="a18e8-548">Added Sku Tier property</span></span>
    - <span data-ttu-id="a18e8-549">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="a18e8-549">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="a18e8-550">Adição da propriedade LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a18e8-550">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="a18e8-551">Atualização do planejamento para preterir os avisos dos seguintes cmdlets: –'New-AzVirtualHubRoute'   –'New-AzVirtualHubRouteTable'   –'Add-AzVirtualHubRoute'   –'Add-AzVirtualHubRouteTable'   –'Get-AzVirtualHubRouteTable'   –'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-551">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="a18e8-552">Adição do planejamento para preterir os avisos no argumento 'RouteTable' nos seguintes cmdlets: –'New-AzVirtualHub'   –'Set-AzVirtualHub'   –'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="a18e8-552">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a18e8-553">Os argumentos '-MinScaleUnits' e '-MaxScaleUnits' passaram a ser opcionais em 'Set-AzExpressRouteGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-553">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="a18e8-554">Adição de novos cmdlets para dar suporte à autenticação mútua e aos perfis SSL no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-554">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="a18e8-555">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-555">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="a18e8-556">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-556">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="a18e8-557">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-557">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="a18e8-558">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-558">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="a18e8-559">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-559">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="a18e8-560">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-560">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="a18e8-561">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-561">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="a18e8-562">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-562">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="a18e8-563">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-563">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="a18e8-564">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-564">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="a18e8-565">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-565">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="a18e8-566">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-566">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="a18e8-567">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-567">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="a18e8-568">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-568">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="a18e8-569">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-569">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="a18e8-570">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-570">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="a18e8-571">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-571">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-572">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-572">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-573">A especificação do BackupTime da política está em UTC.</span><span class="sxs-lookup"><span data-stu-id="a18e8-573">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="a18e8-574">Modificação do aviso de alteração da falha no cmdlet Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="a18e8-574">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="a18e8-575">Atualização do texto da Ajuda do script de exemplo para o cmdlet Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a18e8-575">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-576">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-576">Az.Resources</span></span>
* <span data-ttu-id="a18e8-577">Correção de um problema em que What-If mostrava dois escopos de grupo de recursos com usos diferentes de maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="a18e8-577">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="a18e8-578">Atualização de 'Export-AzResourceGroup' para uso do SDK.</span><span class="sxs-lookup"><span data-stu-id="a18e8-578">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="a18e8-579">Adição de informações de cultura aos métodos de análise</span><span class="sxs-lookup"><span data-stu-id="a18e8-579">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-580">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-580">Az.Sql</span></span>
* <span data-ttu-id="a18e8-581">Correção de problemas em que Set-AzSqlDatabaseAudit não dava suporte ao banco de dados de Hiperescala e em que não era possível determinar a edição do banco de dados</span><span class="sxs-lookup"><span data-stu-id="a18e8-581">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="a18e8-582">Adição de MaintenanceConfigurationId a 'New-AzSqlInstance' e 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-582">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="a18e8-583">Correção de um bug em GetAzureSqlDatabaseReplicationLink.cs, em que o parâmetro PartnerServerName era verificado por valor em vez de chave</span><span class="sxs-lookup"><span data-stu-id="a18e8-583">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-584">Az.Websites</span></span>
* <span data-ttu-id="a18e8-585">Adição de suporte para novos recursos de restrição de acesso: ServiceTag, multi-ip e http-headers</span><span class="sxs-lookup"><span data-stu-id="a18e8-585">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-586">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-586">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-587">John Q. Martin (@johnmart82) – Adição de informações de pré-requisitos do firewall (nº 13385)</span><span class="sxs-lookup"><span data-stu-id="a18e8-587">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="a18e8-588">Manikandan Duraisamy (@madurais-msft) – Correção do argumento PublicSubnetName (nº 13417)</span><span class="sxs-lookup"><span data-stu-id="a18e8-588">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="a18e8-589">@mahortas – Atualização dos valores do parâmetro -HostNames (nº 13349)</span><span class="sxs-lookup"><span data-stu-id="a18e8-589">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="a18e8-590">@MariachiForHire – Adição de valores compatíveis com TrafficAnalyticsInterval (nº 13304)</span><span class="sxs-lookup"><span data-stu-id="a18e8-590">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="a18e8-591">Michael James (@mikejwhat) – permissão para que Get-AzLogicAppRunHistory retorne mais de 30 entradas (nº 13393)</span><span class="sxs-lookup"><span data-stu-id="a18e8-591">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="a18e8-592">Shashikant Shakya (@shshakya) – Atualização de Restore-AzSqlInstanceDatabase.md (nº 13404)</span><span class="sxs-lookup"><span data-stu-id="a18e8-592">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="a18e8-593">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-593">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-594">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-595">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-595">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="a18e8-596">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a18e8-596">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-597">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-597">Az.Aks</span></span>
* <span data-ttu-id="a18e8-598">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-598">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="a18e8-599">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-599">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="a18e8-600">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-600">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="a18e8-601">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="a18e8-601">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="a18e8-602">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a18e8-602">Az.Billing</span></span>
* <span data-ttu-id="a18e8-603">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-603">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="a18e8-604">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-604">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="a18e8-605">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-605">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="a18e8-606">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-606">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="a18e8-607">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="a18e8-607">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-608">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-608">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-609">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="a18e8-609">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-610">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-610">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-611">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="a18e8-611">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-612">Az.Compute</span></span>
* <span data-ttu-id="a18e8-613">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="a18e8-613">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="a18e8-614">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-614">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="a18e8-615">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-615">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="a18e8-616">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="a18e8-616">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="a18e8-617">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-617">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-618">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-618">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-619">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-619">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="a18e8-620">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="a18e8-620">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="a18e8-621">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-621">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="a18e8-622">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="a18e8-622">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="a18e8-623">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="a18e8-623">Az.Databricks</span></span>
* <span data-ttu-id="a18e8-624">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-624">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-625">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-626">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-626">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="a18e8-627">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="a18e8-627">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="a18e8-628">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="a18e8-628">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a18e8-629">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a18e8-629">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a18e8-630">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="a18e8-630">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="a18e8-631">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-631">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="a18e8-632">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-632">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="a18e8-633">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-633">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a18e8-634">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-634">Az.Functions</span></span>
* <span data-ttu-id="a18e8-635">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-635">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="a18e8-636">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-636">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="a18e8-637">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="a18e8-637">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="a18e8-638">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-638">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="a18e8-639">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="a18e8-639">[#12728]</span></span>
  - <span data-ttu-id="a18e8-640">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="a18e8-640">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="a18e8-641">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-641">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="a18e8-642">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-642">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="a18e8-643">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-643">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-644">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-644">Az.HDInsight</span></span>
 * <span data-ttu-id="a18e8-645">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="a18e8-645">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="a18e8-646">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-646">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="a18e8-647">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-647">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="a18e8-648">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-648">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="a18e8-649">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-649">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="a18e8-650">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-650">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="a18e8-651">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="a18e8-651">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="a18e8-652">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-652">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="a18e8-653">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="a18e8-653">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="a18e8-654">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="a18e8-654">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="a18e8-655">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-655">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="a18e8-656">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-656">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="a18e8-657">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-657">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="a18e8-658">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-658">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="a18e8-659">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-659">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="a18e8-660">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="a18e8-660">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="a18e8-661">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-661">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="a18e8-662">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="a18e8-662">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="a18e8-663">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-663">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="a18e8-664">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="a18e8-664">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-665">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-666">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="a18e8-666">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="a18e8-667">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="a18e8-667">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="a18e8-668">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="a18e8-668">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="a18e8-669">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="a18e8-669">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="a18e8-670">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="a18e8-670">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a18e8-671">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-671">Az.ManagedServices</span></span>
* <span data-ttu-id="a18e8-672">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="a18e8-672">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-673">Az.Network</span></span>
* <span data-ttu-id="a18e8-674">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="a18e8-674">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="a18e8-675">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-675">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="a18e8-676">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="a18e8-676">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="a18e8-677">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="a18e8-677">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="a18e8-678">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a18e8-678">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="a18e8-679">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="a18e8-679">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="a18e8-680">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="a18e8-680">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="a18e8-681">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="a18e8-681">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="a18e8-682">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="a18e8-682">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="a18e8-683">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="a18e8-683">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="a18e8-684">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="a18e8-684">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="a18e8-685">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="a18e8-685">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="a18e8-686">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="a18e8-686">Added parameter '-Type'</span></span>
    - <span data-ttu-id="a18e8-687">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="a18e8-687">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="a18e8-688">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-688">Added parameter '-Scope'</span></span>
* <span data-ttu-id="a18e8-689">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="a18e8-689">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-690">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-690">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-691">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="a18e8-691">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="a18e8-692">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a18e8-692">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-693">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-693">Az.Resources</span></span>
* <span data-ttu-id="a18e8-694">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="a18e8-694">Fixed parsing bug</span></span>
* <span data-ttu-id="a18e8-695">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="a18e8-695">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="a18e8-696">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="a18e8-696">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="a18e8-697">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="a18e8-697">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="a18e8-698">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-698">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="a18e8-699">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="a18e8-699">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="a18e8-700">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="a18e8-700">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="a18e8-701">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="a18e8-701">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="a18e8-702">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-702">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-703">Az.Sql</span></span>
* <span data-ttu-id="a18e8-704">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="a18e8-704">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="a18e8-705">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="a18e8-705">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="a18e8-706">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="a18e8-706">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="a18e8-707">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-707">Az.Storage</span></span>
* <span data-ttu-id="a18e8-708">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="a18e8-708">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="a18e8-709">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-709">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-710">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-710">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-711">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-711">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="a18e8-712">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-712">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a18e8-713">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="a18e8-713">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="a18e8-714">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-714">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a18e8-715">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-715">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a18e8-716">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="a18e8-716">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="a18e8-717">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-717">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="a18e8-718">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="a18e8-718">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="a18e8-719">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-719">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="a18e8-720">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-720">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="a18e8-721">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="a18e8-721">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="a18e8-722">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="a18e8-722">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="a18e8-723">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="a18e8-723">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="a18e8-724">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="a18e8-724">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="a18e8-725">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="a18e8-725">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="a18e8-726">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-726">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="a18e8-727">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-727">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="a18e8-728">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="a18e8-728">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="a18e8-729">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-729">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="a18e8-730">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-730">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="a18e8-731">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="a18e8-731">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="a18e8-732">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-732">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-733">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-733">Az.Websites</span></span>
* <span data-ttu-id="a18e8-734">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="a18e8-734">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="a18e8-735">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-735">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-736">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-736">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-737">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="a18e8-737">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="a18e8-738">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="a18e8-738">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="a18e8-739">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="a18e8-739">(#13249)</span></span>
* <span data-ttu-id="a18e8-740">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="a18e8-740">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="a18e8-741">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="a18e8-741">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="a18e8-742">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="a18e8-742">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="a18e8-743">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="a18e8-743">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="a18e8-744">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="a18e8-744">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="a18e8-745">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="a18e8-745">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="a18e8-746">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="a18e8-746">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="a18e8-747">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="a18e8-747">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="a18e8-748">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="a18e8-748">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="a18e8-749">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-749">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-750">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-750">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-751">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="a18e8-751">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-752">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-752">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-753">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-753">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="a18e8-754">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-754">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-755">Az.Compute</span></span>
* <span data-ttu-id="a18e8-756">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="a18e8-756">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="a18e8-757">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-757">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="a18e8-758">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="a18e8-758">Az.Databricks</span></span>
* <span data-ttu-id="a18e8-759">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="a18e8-759">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="a18e8-760">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-760">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-761">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-761">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-762">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-762">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-763">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-763">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-764">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-764">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-765">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-765">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-766">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-766">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="a18e8-767">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-767">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="a18e8-768">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-768">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="a18e8-769">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-769">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="a18e8-770">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-770">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="a18e8-771">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="a18e8-771">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-772">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-772">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-773">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-773">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-774">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-774">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-775">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="a18e8-775">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a18e8-776">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-776">Az.ManagedServices</span></span>
* <span data-ttu-id="a18e8-777">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="a18e8-777">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-778">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-778">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-779">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="a18e8-779">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="a18e8-780">[#12889]</span><span class="sxs-lookup"><span data-stu-id="a18e8-780">[#12889]</span></span>
* <span data-ttu-id="a18e8-781">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="a18e8-781">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="a18e8-782">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-782">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-783">Az.Network</span></span>
* <span data-ttu-id="a18e8-784">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="a18e8-784">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="a18e8-785">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-785">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-786">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-786">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-787">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a18e8-787">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a18e8-788">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a18e8-788">Az.RedisCache</span></span>
* <span data-ttu-id="a18e8-789">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="a18e8-789">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-790">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-790">Az.Sql</span></span>
* <span data-ttu-id="a18e8-791">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a18e8-791">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="a18e8-792">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-792">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="a18e8-793">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-793">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="a18e8-794">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="a18e8-794">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="a18e8-795">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-795">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="a18e8-796">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a18e8-796">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-797">Az.Storage</span></span>
* <span data-ttu-id="a18e8-798">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-798">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="a18e8-799">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-799">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="a18e8-800">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-800">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="a18e8-801">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="a18e8-801">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="a18e8-802">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-802">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="a18e8-803">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="a18e8-803">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="a18e8-804">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-804">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="a18e8-805">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="a18e8-805">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="a18e8-806">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-806">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="a18e8-807">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-807">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="a18e8-808">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-808">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-809">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-809">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-810">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-810">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a18e8-811">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="a18e8-811">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="a18e8-812">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="a18e8-812">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="a18e8-813">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-813">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-814">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-814">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-815">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-815">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="a18e8-816">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-816">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-817">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-817">Az.Aks</span></span>
* <span data-ttu-id="a18e8-818">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-818">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="a18e8-819">[#12372]</span><span class="sxs-lookup"><span data-stu-id="a18e8-819">[#12372]</span></span>
* <span data-ttu-id="a18e8-820">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-820">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="a18e8-821">[#11239]</span><span class="sxs-lookup"><span data-stu-id="a18e8-821">[#11239]</span></span>
* <span data-ttu-id="a18e8-822">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-822">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="a18e8-823">[#11239]</span><span class="sxs-lookup"><span data-stu-id="a18e8-823">[#11239]</span></span>
* <span data-ttu-id="a18e8-824">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-824">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="a18e8-825">[#12371]</span><span class="sxs-lookup"><span data-stu-id="a18e8-825">[#12371]</span></span>
* <span data-ttu-id="a18e8-826">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="a18e8-826">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-827">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-828">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="a18e8-828">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-829">Az.Compute</span></span>
* <span data-ttu-id="a18e8-830">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-830">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="a18e8-831">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="a18e8-831">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="a18e8-832">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-832">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="a18e8-833">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-833">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="a18e8-834">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a18e8-834">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="a18e8-835">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="a18e8-835">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="a18e8-836">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-836">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="a18e8-837">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-837">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="a18e8-838">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-838">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="a18e8-839">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="a18e8-839">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-840">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-840">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-841">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-841">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-842">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-842">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-843">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-843">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="a18e8-844">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a18e8-844">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a18e8-845">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-845">Az.Functions</span></span>
* <span data-ttu-id="a18e8-846">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="a18e8-846">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="a18e8-847">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-847">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="a18e8-848">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="a18e8-848">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-849">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-849">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-850">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="a18e8-850">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="a18e8-851">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-851">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="a18e8-852">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="a18e8-852">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="a18e8-853">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-853">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a18e8-854">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-854">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a18e8-855">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-855">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a18e8-856">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-856">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="a18e8-857">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="a18e8-857">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-858">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-858">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-859">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="a18e8-859">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="a18e8-860">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="a18e8-860">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="a18e8-861">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="a18e8-861">Az.Kusto</span></span>
* <span data-ttu-id="a18e8-862">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="a18e8-862">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-863">Az.Network</span></span>
* <span data-ttu-id="a18e8-864">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-864">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="a18e8-865">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="a18e8-865">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="a18e8-866">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="a18e8-866">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="a18e8-867">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="a18e8-867">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="a18e8-868">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="a18e8-868">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="a18e8-869">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-869">Added subscription level parameter set</span></span>
    - <span data-ttu-id="a18e8-870">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="a18e8-870">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="a18e8-871">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-871">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="a18e8-872">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-872">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="a18e8-873">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-873">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="a18e8-874">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-874">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="a18e8-875">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="a18e8-875">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="a18e8-876">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a18e8-876">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="a18e8-877">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="a18e8-877">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="a18e8-878">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-878">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="a18e8-879">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="a18e8-879">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="a18e8-880">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="a18e8-880">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="a18e8-881">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a18e8-881">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="a18e8-882">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="a18e8-882">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="a18e8-883">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="a18e8-883">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="a18e8-884">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-884">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="a18e8-885">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-885">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="a18e8-886">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-886">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="a18e8-887">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="a18e8-887">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-888">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-888">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-889">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-889">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-890">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-890">Az.Resources</span></span>
* <span data-ttu-id="a18e8-891">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a18e8-891">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="a18e8-892">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-892">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="a18e8-893">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="a18e8-893">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="a18e8-894">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="a18e8-894">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-895">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-895">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-896">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-896">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="a18e8-897">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-897">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a18e8-898">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-898">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a18e8-899">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-899">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a18e8-900">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-900">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="a18e8-901">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-901">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="a18e8-902">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-902">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="a18e8-903">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-903">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a18e8-904">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-904">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a18e8-905">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-905">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a18e8-906">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="a18e8-906">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="a18e8-907">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-907">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="a18e8-908">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="a18e8-908">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="a18e8-909">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-909">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="a18e8-910">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="a18e8-910">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="a18e8-911">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-911">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-912">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-912">Az.Sql</span></span>
* <span data-ttu-id="a18e8-913">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-913">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="a18e8-914">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-914">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-915">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-915">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-916">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-916">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="a18e8-917">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-917">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="a18e8-918">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="a18e8-918">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a18e8-919">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="a18e8-919">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a18e8-920">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="a18e8-920">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="a18e8-921">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="a18e8-921">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="a18e8-922">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-922">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-923">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-923">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-924">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-924">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-925">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="a18e8-925">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="a18e8-926">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-926">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="a18e8-927">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="a18e8-927">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="a18e8-928">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-928">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="a18e8-929">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="a18e8-929">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="a18e8-930">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-930">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-931">Az.Storage</span></span>
* <span data-ttu-id="a18e8-932">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="a18e8-932">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="a18e8-933">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="a18e8-933">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="a18e8-934">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-934">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-935">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-935">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="a18e8-936">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="a18e8-936">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="a18e8-937">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="a18e8-937">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="a18e8-938">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="a18e8-938">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="a18e8-939">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-939">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="a18e8-940">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="a18e8-940">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="a18e8-941">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-941">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="a18e8-942">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-942">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="a18e8-943">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-943">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a18e8-944">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-944">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="a18e8-945">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="a18e8-945">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="a18e8-946">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-946">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="a18e8-947">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="a18e8-947">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="a18e8-948">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-948">Thanks to our community contributors</span></span>
* <span data-ttu-id="a18e8-949">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="a18e8-949">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="a18e8-950">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="a18e8-950">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="a18e8-951">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="a18e8-951">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="a18e8-952">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="a18e8-952">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="a18e8-953">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="a18e8-953">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="a18e8-954">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="a18e8-954">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="a18e8-955">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="a18e8-955">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="a18e8-956">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="a18e8-956">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="a18e8-957">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="a18e8-957">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="a18e8-958">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="a18e8-958">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="a18e8-959">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="a18e8-959">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="a18e8-960">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-960">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="a18e8-961">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-961">Az.Compute</span></span>
* <span data-ttu-id="a18e8-962">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="a18e8-962">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="a18e8-963">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-963">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-964">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-965">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="a18e8-965">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="a18e8-966">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="a18e8-966">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-967">Az.Automation</span></span>
* <span data-ttu-id="a18e8-968">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="a18e8-968">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-969">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-969">Az.Compute</span></span>
* <span data-ttu-id="a18e8-970">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="a18e8-970">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="a18e8-971">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="a18e8-971">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="a18e8-972">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-972">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="a18e8-973">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-973">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-974">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-974">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-975">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="a18e8-975">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-976">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-976">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-977">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="a18e8-977">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-978">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-979">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="a18e8-979">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="a18e8-980">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="a18e8-980">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a18e8-981">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a18e8-981">Az.Maintenance</span></span>
* <span data-ttu-id="a18e8-982">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-982">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="a18e8-983">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-983">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a18e8-984">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-984">Az.ManagedServices</span></span>
* <span data-ttu-id="a18e8-985">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="a18e8-985">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-986">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-986">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-987">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="a18e8-987">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="a18e8-988">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="a18e8-988">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-989">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-989">Az.Resources</span></span>
* <span data-ttu-id="a18e8-990">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="a18e8-990">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="a18e8-991">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-991">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="a18e8-992">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-992">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="a18e8-993">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="a18e8-993">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="a18e8-994">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="a18e8-994">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a18e8-995">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="a18e8-995">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="a18e8-996">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="a18e8-996">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="a18e8-997">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-997">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a18e8-998">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-998">Az.SignalR</span></span>
* <span data-ttu-id="a18e8-999">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="a18e8-999">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="a18e8-1000">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1000">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1001">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1002">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="a18e8-1002">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="a18e8-1003">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1003">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="a18e8-1004">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1004">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="a18e8-1005">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1005">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="a18e8-1006">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1006">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="a18e8-1007">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1007">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="a18e8-1008">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1008">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="a18e8-1009">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1009">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="a18e8-1010">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1010">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="a18e8-1011">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1011">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="a18e8-1012">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1012">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a18e8-1013">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1013">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="a18e8-1014">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1014">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="a18e8-1015">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1015">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a18e8-1016">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1016">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="a18e8-1017">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1017">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1018">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1019">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1019">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="a18e8-1020">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1020">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="a18e8-1021">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="a18e8-1021">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="a18e8-1022">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="a18e8-1022">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="a18e8-1023">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="a18e8-1023">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-1024">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-1024">Az.Aks</span></span>
* <span data-ttu-id="a18e8-1025">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="a18e8-1025">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="a18e8-1026">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="a18e8-1026">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1027">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1027">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1028">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1028">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1029">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1029">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1030">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1030">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1031">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1031">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1032">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1032">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1033">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1033">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1034">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1034">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1035">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1035">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1036">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1036">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1037">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1037">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1038">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1038">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1039">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1039">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-1040">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1040">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-1041">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1041">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-1042">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1042">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-1043">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1043">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1044">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1044">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1045">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1045">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="a18e8-1046">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1046">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a18e8-1047">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-1047">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a18e8-1048">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1048">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="a18e8-1049">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1049">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="a18e8-1050">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-1050">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="a18e8-1051">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1051">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1052">Az.Network</span></span>
* <span data-ttu-id="a18e8-1053">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1053">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a18e8-1054">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1054">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="a18e8-1055">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1055">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="a18e8-1056">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1056">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-1057">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1057">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-1058">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="a18e8-1058">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="a18e8-1059">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="a18e8-1059">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="a18e8-1060">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a18e8-1060">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1061">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1061">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1062">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1062">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1063">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1064">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a18e8-1064">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="a18e8-1065">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1065">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1066">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1067">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1067">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a18e8-1068">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a18e8-1068">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1069">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1069">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1070">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="a18e8-1070">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="a18e8-1071">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1071">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="a18e8-1072">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-1072">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="a18e8-1073">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="a18e8-1073">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="a18e8-1074">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-1074">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="a18e8-1075">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="a18e8-1075">Supported get single file share usage</span></span>
    - <span data-ttu-id="a18e8-1076">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-1076">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="a18e8-1077">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1077">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1078">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1078">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1079">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1079">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="a18e8-1080">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1080">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-1081">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-1081">Az.Aks</span></span>
* <span data-ttu-id="a18e8-1082">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1082">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="a18e8-1084">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1084">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-1085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-1085">Az.Automation</span></span>
* <span data-ttu-id="a18e8-1086">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1086">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1087">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1087">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1088">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1088">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1089">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1089">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1090">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1090">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a18e8-1091">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a18e8-1091">Az.EventGrid</span></span>
* <span data-ttu-id="a18e8-1092">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1092">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="a18e8-1093">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1093">Added new features:</span></span>
    - <span data-ttu-id="a18e8-1094">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1094">Input mapping</span></span>
    - <span data-ttu-id="a18e8-1095">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="a18e8-1095">Event Delivery Schema</span></span>
    - <span data-ttu-id="a18e8-1096">Link Privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1096">Private Link</span></span>
    - <span data-ttu-id="a18e8-1097">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="a18e8-1097">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="a18e8-1098">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="a18e8-1098">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="a18e8-1099">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="a18e8-1099">Azure Function As Destination</span></span>
    - <span data-ttu-id="a18e8-1100">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="a18e8-1100">WebHook Batching</span></span>
    - <span data-ttu-id="a18e8-1101">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1101">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="a18e8-1102">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="a18e8-1102">IpFiltering</span></span>
* <span data-ttu-id="a18e8-1103">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1103">Updated cmdlets:</span></span>
    - <span data-ttu-id="a18e8-1104">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="a18e8-1104">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="a18e8-1105">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1105">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="a18e8-1106">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1106">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="a18e8-1107">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1107">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="a18e8-1108">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1108">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="a18e8-1109">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="a18e8-1109">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a18e8-1110">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1110">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="a18e8-1111">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="a18e8-1111">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="a18e8-1112">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1112">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-1113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1113">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-1114">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-1114">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="a18e8-1115">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1115">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1116">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1116">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1117">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1117">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1118">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1118">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1119">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1119">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1120">Az.Network</span></span>
* <span data-ttu-id="a18e8-1121">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1121">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="a18e8-1122">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-1122">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="a18e8-1123">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1123">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a18e8-1124">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1124">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a18e8-1125">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1125">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a18e8-1126">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1126">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="a18e8-1127">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1127">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="a18e8-1128">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-1128">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="a18e8-1129">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1129">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a18e8-1130">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1130">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a18e8-1131">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1131">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a18e8-1132">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1132">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="a18e8-1133">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1133">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="a18e8-1134">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1134">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="a18e8-1135">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1135">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a18e8-1136">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1136">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="a18e8-1137">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1137">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1138">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1138">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1139">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1139">Removed project reference to Authentication</span></span>
* <span data-ttu-id="a18e8-1140">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1140">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="a18e8-1141">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1141">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1142">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1143">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1143">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="a18e8-1144">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1144">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1145">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1146">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1146">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="a18e8-1147">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1147">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="a18e8-1148">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1148">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1149">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1150">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1150">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="a18e8-1151">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-1151">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="a18e8-1152">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1152">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a18e8-1153">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1153">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1154">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1154">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="a18e8-1155">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1155">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="a18e8-1156">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="a18e8-1156">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="a18e8-1157">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1157">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="a18e8-1158">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="a18e8-1158">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="a18e8-1159">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1159">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="a18e8-1160">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1160">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="a18e8-1161">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="a18e8-1161">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="a18e8-1162">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1162">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a18e8-1163">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1163">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="a18e8-1164">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1164">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="a18e8-1165">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1165">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="a18e8-1166">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1166">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-1167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-1167">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-1168">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-1168">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="a18e8-1169">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1169">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="a18e8-1170">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1170">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="a18e8-1171">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1171">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1172">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1173">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1173">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="a18e8-1174">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1174">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1175">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1176">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1176">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="a18e8-1177">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1177">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="a18e8-1178">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1178">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="a18e8-1179">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1179">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-1180">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-1180">Az.Aks</span></span>
* <span data-ttu-id="a18e8-1181">O uso da [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1181">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-1182">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-1182">Az.Batch</span></span>
* <span data-ttu-id="a18e8-1183">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1183">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="a18e8-1184">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1184">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-1185">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1185">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-1186">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1186">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="a18e8-1187">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1187">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1188">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1188">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1189">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1189">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="a18e8-1190">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1190">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="a18e8-1191">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1191">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="a18e8-1192">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1192">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="a18e8-1193">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="a18e8-1193">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1194">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1195">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1195">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-1196">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1196">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-1197">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1197">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a18e8-1198">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-1198">Az.Functions</span></span>
* <span data-ttu-id="a18e8-1199">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="a18e8-1199">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1200">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1200">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1201">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1201">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a18e8-1202">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a18e8-1202">Az.HealthcareApis</span></span>
* <span data-ttu-id="a18e8-1203">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1203">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="a18e8-1204">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1204">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1205">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1206">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1206">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="a18e8-1207">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1207">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1208">Az.Network</span></span>
* <span data-ttu-id="a18e8-1209">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1209">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="a18e8-1210">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-1210">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a18e8-1211">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1211">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="a18e8-1212">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="a18e8-1212">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="a18e8-1213">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="a18e8-1213">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="a18e8-1214">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1214">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="a18e8-1215">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1215">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a18e8-1216">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1216">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a18e8-1217">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1217">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="a18e8-1218">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1218">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="a18e8-1219">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1219">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="a18e8-1220">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-1220">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="a18e8-1221">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1221">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="a18e8-1222">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1222">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="a18e8-1223">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1223">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="a18e8-1224">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1224">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="a18e8-1225">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1225">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="a18e8-1226">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1226">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="a18e8-1227">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1227">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="a18e8-1228">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1228">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="a18e8-1229">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="a18e8-1229">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="a18e8-1230">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="a18e8-1230">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="a18e8-1231">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="a18e8-1231">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="a18e8-1232">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1232">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="a18e8-1233">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1233">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a18e8-1234">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1234">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="a18e8-1235">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1235">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="a18e8-1236">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1236">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="a18e8-1237">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1237">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1238">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1238">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1239">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1239">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1240">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1240">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1241">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1241">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1242">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1242">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="a18e8-1243">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1243">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="a18e8-1244">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1244">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="a18e8-1245">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1245">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a18e8-1246">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1246">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a18e8-1247">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1247">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="a18e8-1248">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1248">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="a18e8-1249">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1249">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="a18e8-1250">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1250">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a18e8-1251">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1251">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="a18e8-1252">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1252">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a18e8-1253">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1253">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a18e8-1254">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1254">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="a18e8-1255">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1255">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="a18e8-1256">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1256">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="a18e8-1257">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1257">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-1258">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1258">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-1259">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1259">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="a18e8-1260">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1260">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="a18e8-1261">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="a18e8-1261">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="a18e8-1262">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1262">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a18e8-1263">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1263">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1264">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1264">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1265">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1265">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="a18e8-1266">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1266">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1267">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1268">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1268">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="a18e8-1269">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1269">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="a18e8-1270">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1270">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="a18e8-1271">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1271">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="a18e8-1272">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="a18e8-1272">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="a18e8-1273">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="a18e8-1273">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1274">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1274">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1275">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="a18e8-1275">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="a18e8-1276">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1276">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="a18e8-1277">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1277">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1278">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1278">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1279">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="a18e8-1279">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="a18e8-1280">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1280">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1281">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1281">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1282">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1282">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1283">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1283">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a18e8-1284">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1284">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="a18e8-1285">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1285">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="a18e8-1286">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-1286">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="a18e8-1287">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="a18e8-1287">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="a18e8-1288">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="a18e8-1288">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="a18e8-1289">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1289">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1290">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1291">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1291">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-1292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1292">Az.AnalysisServices</span></span>
* <span data-ttu-id="a18e8-1293">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1293">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1294">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1294">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1295">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1295">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="a18e8-1296">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a18e8-1296">Az.Billing</span></span>
* <span data-ttu-id="a18e8-1297">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1297">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-1298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1298">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-1299">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1299">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1300">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1300">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1301">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1301">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="a18e8-1302">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-1302">Az.DataShare</span></span>
* <span data-ttu-id="a18e8-1303">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="a18e8-1303">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="a18e8-1304">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="a18e8-1304">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="a18e8-1305">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="a18e8-1305">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-1306">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1306">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-1307">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1307">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="a18e8-1308">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="a18e8-1308">Added optional parameters to</span></span> 
    - <span data-ttu-id="a18e8-1309">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1309">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="a18e8-1310">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1310">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-1311">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1311">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-1312">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1312">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a18e8-1313">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a18e8-1313">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a18e8-1314">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1314">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a18e8-1315">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a18e8-1315">Az.PrivateDns</span></span>
* <span data-ttu-id="a18e8-1316">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1316">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1317">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1317">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1318">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1318">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="a18e8-1319">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a18e8-1319">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1320">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1320">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1321">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a18e8-1321">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="a18e8-1322">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a18e8-1322">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="a18e8-1323">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-1323">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="a18e8-1324">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1324">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="a18e8-1325">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1325">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1326">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1326">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1327">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1327">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a18e8-1328">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1328">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="a18e8-1329">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="a18e8-1329">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1330">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1331">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1331">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="a18e8-1332">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1332">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a18e8-1333">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="a18e8-1333">Highlights since the last release</span></span>
* <span data-ttu-id="a18e8-1334">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a18e8-1334">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="a18e8-1335">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-1335">General availability of Az.Functions</span></span> 
* <span data-ttu-id="a18e8-1336">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-1336">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1337">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1337">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1338">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1338">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="a18e8-1339">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="a18e8-1339">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-1340">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-1340">Az.Aks</span></span>
* <span data-ttu-id="a18e8-1341">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-1341">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="a18e8-1342">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="a18e8-1342">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="a18e8-1343">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1343">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1344">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1344">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1345">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1345">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="a18e8-1346">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1346">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="a18e8-1347">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1347">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a18e8-1348">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1348">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a18e8-1349">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1349">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a18e8-1350">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1350">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="a18e8-1351">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1351">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a18e8-1352">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1352">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a18e8-1353">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1353">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="a18e8-1354">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1354">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="a18e8-1355">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1355">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="a18e8-1356">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1356">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="a18e8-1357">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1357">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="a18e8-1358">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1358">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="a18e8-1359">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1359">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="a18e8-1360">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1360">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a18e8-1361">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1361">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a18e8-1362">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1362">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="a18e8-1363">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1363">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="a18e8-1364">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1364">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-1365">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-1365">Az.Batch</span></span>
* <span data-ttu-id="a18e8-1366">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1366">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="a18e8-1367">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1367">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="a18e8-1368">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1368">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="a18e8-1369">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1369">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="a18e8-1370">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1370">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="a18e8-1371">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1371">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="a18e8-1372">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1372">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="a18e8-1373">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1373">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="a18e8-1374">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1374">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1375">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1375">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1376">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1376">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="a18e8-1377">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1377">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="a18e8-1378">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="a18e8-1378">Breaking changes</span></span>
    - <span data-ttu-id="a18e8-1379">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1379">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="a18e8-1380">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1380">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="a18e8-1381">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1381">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="a18e8-1382">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1382">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="a18e8-1383">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1383">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="a18e8-1384">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1384">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="a18e8-1385">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1385">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1386">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1386">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1387">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1387">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-1388">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1388">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-1389">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="a18e8-1389">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a18e8-1390">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="a18e8-1390">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="a18e8-1391">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1391">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="a18e8-1392">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="a18e8-1392">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="a18e8-1393">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-1393">Az.Functions</span></span>
* <span data-ttu-id="a18e8-1394">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="a18e8-1394">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1395">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1395">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1396">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1396">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a18e8-1397">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a18e8-1397">Az.HealthcareApis</span></span>
* <span data-ttu-id="a18e8-1398">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="a18e8-1398">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1399">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-1400">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1400">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="a18e8-1401">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1401">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="a18e8-1402">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1402">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="a18e8-1403">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1403">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="a18e8-1404">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1404">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="a18e8-1405">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1405">New cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1406">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1406">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a18e8-1407">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1407">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a18e8-1408">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1408">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="a18e8-1409">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1409">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="a18e8-1410">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1410">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="a18e8-1411">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1411">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1412">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1412">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1413">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1413">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="a18e8-1414">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a18e8-1414">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="a18e8-1415">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a18e8-1415">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="a18e8-1416">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1416">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="a18e8-1417">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="a18e8-1417">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="a18e8-1418">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="a18e8-1418">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="a18e8-1419">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1419">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1420">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1421">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1421">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="a18e8-1422">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="a18e8-1422">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="a18e8-1423">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1423">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="a18e8-1424">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="a18e8-1424">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="a18e8-1425">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1425">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="a18e8-1426">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1426">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="a18e8-1427">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1427">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1428">Az.Network</span></span>
* <span data-ttu-id="a18e8-1429">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1429">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="a18e8-1430">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1430">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="a18e8-1431">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1431">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="a18e8-1432">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1432">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="a18e8-1433">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a18e8-1433">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="a18e8-1434">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1434">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-1435">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a18e8-1435">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a18e8-1436">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a18e8-1436">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a18e8-1437">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a18e8-1437">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="a18e8-1438">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a18e8-1438">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="a18e8-1439">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1439">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="a18e8-1440">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-1440">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="a18e8-1441">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1441">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="a18e8-1442">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1442">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="a18e8-1443">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1443">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="a18e8-1444">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1444">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="a18e8-1445">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1445">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="a18e8-1446">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1446">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a18e8-1447">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1447">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a18e8-1448">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1448">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="a18e8-1449">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1449">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="a18e8-1450">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1450">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="a18e8-1451">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1451">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="a18e8-1452">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1452">Updated cmdlet:</span></span>
        - <span data-ttu-id="a18e8-1453">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a18e8-1453">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-1454">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1454">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-1455">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1455">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="a18e8-1456">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="a18e8-1456">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="a18e8-1457">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="a18e8-1457">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="a18e8-1458">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="a18e8-1458">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="a18e8-1459">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="a18e8-1459">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="a18e8-1460">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1460">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="a18e8-1461">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1461">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="a18e8-1462">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1462">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1464">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1464">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="a18e8-1465">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1465">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="a18e8-1466">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1466">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="a18e8-1467">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1467">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="a18e8-1468">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1468">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1469">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1469">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1470">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="a18e8-1470">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="a18e8-1471">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1471">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="a18e8-1472">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1472">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="a18e8-1473">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1473">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="a18e8-1474">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1474">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="a18e8-1475">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1475">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="a18e8-1476">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1476">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="a18e8-1477">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="a18e8-1477">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="a18e8-1478">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1478">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="a18e8-1479">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1479">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="a18e8-1480">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1480">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="a18e8-1481">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="a18e8-1481">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="a18e8-1482">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1482">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="a18e8-1483">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="a18e8-1483">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="a18e8-1484">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="a18e8-1484">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="a18e8-1485">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="a18e8-1485">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="a18e8-1486">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1486">'New-AzDeployment'</span></span>
    - <span data-ttu-id="a18e8-1487">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1487">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="a18e8-1488">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1488">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a18e8-1489">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1489">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-1490">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-1490">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-1491">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1491">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1492">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1492">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1493">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1493">Enhance performance of:</span></span>
    - <span data-ttu-id="a18e8-1494">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1494">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a18e8-1495">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1495">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a18e8-1496">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1496">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a18e8-1497">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1497">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="a18e8-1498">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1498">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a18e8-1499">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1499">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a18e8-1500">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1500">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="a18e8-1501">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1501">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="a18e8-1502">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1502">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="a18e8-1503">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1503">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1504">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1505">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1505">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1506">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="a18e8-1506">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="a18e8-1507">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1507">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1508">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="a18e8-1508">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="a18e8-1509">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1509">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a18e8-1510">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1510">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="a18e8-1511">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1511">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="a18e8-1512">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1512">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="a18e8-1513">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1513">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="a18e8-1514">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1514">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="a18e8-1515">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="a18e8-1515">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="a18e8-1516">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="a18e8-1516">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="a18e8-1517">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1517">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="a18e8-1518">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-1518">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="a18e8-1519">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1519">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="a18e8-1520">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1520">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1521">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1521">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="a18e8-1522">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1522">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="a18e8-1523">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1523">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a18e8-1524">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="a18e8-1524">Supported failover Storage account</span></span>
    - <span data-ttu-id="a18e8-1525">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1525">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="a18e8-1526">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1526">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="a18e8-1527">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-1527">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="a18e8-1528">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="a18e8-1528">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="a18e8-1529">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-1529">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a18e8-1530">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1530">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="a18e8-1531">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1531">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="a18e8-1532">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1532">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a18e8-1533">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1533">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="a18e8-1534">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1534">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="a18e8-1535">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-1535">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a18e8-1536">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1536">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="a18e8-1537">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1537">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="a18e8-1538">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-1538">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="a18e8-1539">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1539">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="a18e8-1540">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1540">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="a18e8-1541">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1541">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="a18e8-1542">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-1542">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="a18e8-1543">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1543">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a18e8-1544">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a18e8-1544">Az.TrafficManager</span></span>
* <span data-ttu-id="a18e8-1545">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1545">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1546">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1547">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1547">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="a18e8-1548">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1548">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="a18e8-1549">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="a18e8-1549">Highlights since the last release</span></span>
* <span data-ttu-id="a18e8-1550">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="a18e8-1550">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1551">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1551">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1552">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1552">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1553">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1553">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1554">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="a18e8-1554">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a18e8-1555">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1555">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-1556">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-1556">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-1557">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="a18e8-1557">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-1558">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1558">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-1559">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="a18e8-1559">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1560">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1561">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1561">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1562">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1562">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-1563">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1563">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-1564">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1564">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1565">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1565">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="a18e8-1566">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1566">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="a18e8-1567">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1567">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="a18e8-1568">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1568">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1569">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1569">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="a18e8-1570">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1570">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="a18e8-1571">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1571">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="a18e8-1572">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1572">New cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1573">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1573">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1574">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1574">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1575">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1575">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="a18e8-1576">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1576">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="a18e8-1577">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1577">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1578">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1578">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1579">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="a18e8-1579">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="a18e8-1580">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1580">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="a18e8-1581">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1581">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="a18e8-1582">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1582">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="a18e8-1583">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="a18e8-1583">Az.Maintenance</span></span>
* <span data-ttu-id="a18e8-1584">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-1584">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1585">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1585">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1586">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1586">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="a18e8-1587">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1587">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a18e8-1588">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1588">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a18e8-1589">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1589">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a18e8-1590">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1590">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="a18e8-1591">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1591">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a18e8-1592">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1592">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="a18e8-1593">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1593">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1594">Az.Network</span></span>
* <span data-ttu-id="a18e8-1595">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1595">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="a18e8-1596">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1596">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a18e8-1597">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1597">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="a18e8-1598">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1598">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="a18e8-1599">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1599">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="a18e8-1600">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1600">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="a18e8-1601">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1601">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="a18e8-1602">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1602">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="a18e8-1603">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1603">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="a18e8-1604">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1604">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a18e8-1605">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="a18e8-1605">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="a18e8-1606">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1606">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="a18e8-1607">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="a18e8-1607">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="a18e8-1608">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1608">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="a18e8-1609">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-1609">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="a18e8-1610">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-1610">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-1611">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1611">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-1612">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="a18e8-1612">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="a18e8-1613">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1613">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-1614">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-1614">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-1615">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1615">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1616">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1616">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1617">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1617">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="a18e8-1618">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1618">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1619">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1619">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1620">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="a18e8-1620">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="a18e8-1621">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1621">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="a18e8-1622">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1622">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="a18e8-1623">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1623">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="a18e8-1624">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="a18e8-1624">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="a18e8-1625">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1625">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a18e8-1626">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1626">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a18e8-1627">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1627">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="a18e8-1628">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1628">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a18e8-1629">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1629">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="a18e8-1630">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1630">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="a18e8-1631">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1631">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="a18e8-1632">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1632">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="a18e8-1633">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1633">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="a18e8-1634">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-1634">General</span></span>
* <span data-ttu-id="a18e8-1635">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1635">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="a18e8-1636">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1636">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="a18e8-1637">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1637">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="a18e8-1638">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1638">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="a18e8-1639">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a18e8-1639">Az.Billing</span></span>
  - <span data-ttu-id="a18e8-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1640">Az.Compute</span></span>
  - <span data-ttu-id="a18e8-1641">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1641">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="a18e8-1642">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1642">Az.EventHub</span></span>
  - <span data-ttu-id="a18e8-1643">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1643">Az.IotHub</span></span>
  - <span data-ttu-id="a18e8-1644">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1644">Az.KeyVault</span></span>
  - <span data-ttu-id="a18e8-1645">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1645">Az.Monitor</span></span>
  - <span data-ttu-id="a18e8-1646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1646">Az.Network</span></span>
  - <span data-ttu-id="a18e8-1647">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1647">Az.Resources</span></span>
  - <span data-ttu-id="a18e8-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1648">Az.Storage</span></span>
  - <span data-ttu-id="a18e8-1649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1649">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1650">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1650">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="a18e8-1651">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="a18e8-1651">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="a18e8-1652">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="a18e8-1652">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="a18e8-1653">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1653">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1654">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1655">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1655">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1656">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1656">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1657">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="a18e8-1657">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="a18e8-1658">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a18e8-1658">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="a18e8-1659">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1659">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1660">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1660">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="a18e8-1661">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1661">[#11354]</span></span>
* <span data-ttu-id="a18e8-1662">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="a18e8-1662">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="a18e8-1663">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1663">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a18e8-1664">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1664">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a18e8-1665">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1665">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="a18e8-1666">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1666">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="a18e8-1667">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-1667">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="a18e8-1668">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1668">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="a18e8-1669">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1669">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="a18e8-1670">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1670">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1671">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1671">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1672">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1672">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="a18e8-1673">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="a18e8-1673">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-1674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-1674">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-1675">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1675">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="a18e8-1676">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1676">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1677">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1677">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1678">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1678">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-1679">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1679">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-1680">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1680">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="a18e8-1681">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1681">New Cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1682">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1682">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="a18e8-1683">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1683">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1684">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1684">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1685">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1685">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1686">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1686">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1687">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1687">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1688">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1688">Az.Network</span></span>
* <span data-ttu-id="a18e8-1689">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="a18e8-1689">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="a18e8-1690">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1690">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a18e8-1691">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1691">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="a18e8-1692">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1692">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="a18e8-1693">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1693">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="a18e8-1694">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-1694">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-1695">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1695">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-1696">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="a18e8-1696">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1697">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1697">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1698">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1698">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="a18e8-1699">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="a18e8-1699">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="a18e8-1700">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1700">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="a18e8-1701">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1701">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="a18e8-1702">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-1702">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="a18e8-1703">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-1703">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1704">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1705">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1705">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="a18e8-1706">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="a18e8-1706">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="a18e8-1707">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1707">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="a18e8-1708">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1708">Added example.</span></span>
* <span data-ttu-id="a18e8-1709">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1709">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="a18e8-1710">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="a18e8-1710">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1711">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1712">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1712">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="a18e8-1713">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1713">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="a18e8-1714">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1714">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="a18e8-1715">Az.Support</span><span class="sxs-lookup"><span data-stu-id="a18e8-1715">Az.Support</span></span>
* <span data-ttu-id="a18e8-1716">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1716">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1717">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1718">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1718">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="a18e8-1719">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1719">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a18e8-1720">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1720">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a18e8-1721">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1721">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="a18e8-1722">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1722">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="a18e8-1723">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1723">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1724">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1724">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1725">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1725">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="a18e8-1726">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1726">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="a18e8-1727">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="a18e8-1727">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1728">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1728">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1729">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1729">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="a18e8-1730">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1730">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="a18e8-1731">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="a18e8-1731">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="a18e8-1732">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1732">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-1734">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1734">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-1735">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1735">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-1736">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1736">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a18e8-1737">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1737">New Cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1738">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1738">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1739">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1739">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1740">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1740">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1741">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1741">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="a18e8-1742">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1742">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="a18e8-1743">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1743">New Cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1744">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1744">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="a18e8-1745">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1745">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="a18e8-1746">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1746">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="a18e8-1747">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1747">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="a18e8-1748">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1748">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a18e8-1749">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1749">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="a18e8-1750">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1750">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="a18e8-1751">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1751">New Cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1752">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1752">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="a18e8-1753">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1753">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="a18e8-1754">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1754">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1755">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1755">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1756">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1756">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1757">Az.Network</span></span>
* <span data-ttu-id="a18e8-1758">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1758">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="a18e8-1759">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1759">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="a18e8-1760">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1760">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="a18e8-1761">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1761">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1762">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1762">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1763">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1763">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="a18e8-1764">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1764">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="a18e8-1765">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1765">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="a18e8-1766">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="a18e8-1766">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="a18e8-1767">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="a18e8-1767">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="a18e8-1768">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="a18e8-1768">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="a18e8-1769">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1769">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="a18e8-1770">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1770">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="a18e8-1771">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1771">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a18e8-1772">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1772">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="a18e8-1773">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1773">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="a18e8-1774">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-1774">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="a18e8-1775">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-1775">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="a18e8-1776">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1776">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1777">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1777">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1778">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1778">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="a18e8-1779">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1779">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="a18e8-1780">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1780">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="a18e8-1781">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="a18e8-1781">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="a18e8-1782">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="a18e8-1782">Remove an LTR backup</span></span>
    - <span data-ttu-id="a18e8-1783">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="a18e8-1783">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="a18e8-1784">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a18e8-1784">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="a18e8-1785">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-1785">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="a18e8-1786">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1786">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1787">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1787">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1788">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-1788">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="a18e8-1789">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1789">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="a18e8-1790">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="a18e8-1790">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="a18e8-1791">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1791">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="a18e8-1792">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1792">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1793">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1794">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1794">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="a18e8-1795">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="a18e8-1795">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="a18e8-1796">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1796">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="a18e8-1797">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="a18e8-1797">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="a18e8-1798">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a18e8-1798">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="a18e8-1799">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1799">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-1800">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-1800">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-1801">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1801">Updated client side telemetry.</span></span>
* <span data-ttu-id="a18e8-1802">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1802">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="a18e8-1803">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1803">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1804">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1804">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1805">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="a18e8-1805">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-1806">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-1806">Az.Automation</span></span>
* <span data-ttu-id="a18e8-1807">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1807">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-1808">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1808">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-1809">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1809">Updated SDK to 7.0</span></span>
* <span data-ttu-id="a18e8-1810">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="a18e8-1810">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1811">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1812">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="a18e8-1812">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-1813">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1813">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-1814">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="a18e8-1814">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-1815">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1815">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-1816">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1816">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="a18e8-1817">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1817">New Cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-1818">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1818">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1819">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1819">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1820">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1820">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="a18e8-1821">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1821">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1822">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1822">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1823">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="a18e8-1823">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-1824">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1824">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-1825">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1825">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="a18e8-1826">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1826">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="a18e8-1827">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="a18e8-1827">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1828">Az.Network</span></span>
* <span data-ttu-id="a18e8-1829">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1829">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="a18e8-1830">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1830">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a18e8-1831">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1831">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="a18e8-1832">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1832">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="a18e8-1833">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1833">No new cmdlets are added.</span></span> <span data-ttu-id="a18e8-1834">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1834">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1836">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1836">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1837">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1838">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1838">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="a18e8-1839">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a18e8-1839">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="a18e8-1840">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a18e8-1840">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="a18e8-1841">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="a18e8-1841">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="a18e8-1842">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a18e8-1842">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="a18e8-1843">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="a18e8-1843">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="a18e8-1844">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1844">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="a18e8-1845">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-1845">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1846">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1846">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1847">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1847">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="a18e8-1848">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="a18e8-1848">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="a18e8-1849">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="a18e8-1849">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a18e8-1850">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a18e8-1850">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a18e8-1851">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-1851">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-1852">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-1852">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-1853">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1853">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="a18e8-1854">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1854">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-1855">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-1855">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-1856">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a18e8-1856">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="a18e8-1857">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1857">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1858">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1858">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1859">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="a18e8-1859">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="a18e8-1860">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="a18e8-1860">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-1861">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-1861">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-1862">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="a18e8-1862">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="a18e8-1863">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="a18e8-1863">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="a18e8-1864">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="a18e8-1864">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="a18e8-1865">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1865">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1866">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1866">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1867">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1867">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="a18e8-1868">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1868">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="a18e8-1869">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1869">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="a18e8-1870">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-1870">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="a18e8-1871">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1871">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1872">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1873">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1873">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a18e8-1874">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a18e8-1874">Az.DeploymentManager</span></span>
* <span data-ttu-id="a18e8-1875">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="a18e8-1875">Adds LIST operations for resources</span></span>
* <span data-ttu-id="a18e8-1876">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="a18e8-1876">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1877">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1877">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1878">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1878">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1879">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1879">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1880">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1880">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1881">Az.Network</span></span>
* <span data-ttu-id="a18e8-1882">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1882">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="a18e8-1883">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1883">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="a18e8-1884">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1884">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a18e8-1885">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="a18e8-1885">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="a18e8-1886">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1886">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="a18e8-1887">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1887">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="a18e8-1888">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1888">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="a18e8-1889">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-1889">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="a18e8-1890">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-1890">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-1891">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-1891">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="a18e8-1892">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-1892">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="a18e8-1893">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1893">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="a18e8-1894">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="a18e8-1894">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-1895">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-1895">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-1896">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="a18e8-1896">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="a18e8-1897">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a18e8-1897">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="a18e8-1898">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="a18e8-1898">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="a18e8-1899">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-1899">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1900">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1900">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1901">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1901">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="a18e8-1902">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1902">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1903">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1904">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="a18e8-1904">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="a18e8-1905">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="a18e8-1905">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1906">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1906">Az.Sql</span></span>
<span data-ttu-id="a18e8-1907">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1907">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1908">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1909">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1909">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="a18e8-1910">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-1910">New-AzStorageAccount</span></span>
* <span data-ttu-id="a18e8-1911">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="a18e8-1911">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="a18e8-1912">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-1912">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-1913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-1913">Az.Websites</span></span>
* <span data-ttu-id="a18e8-1914">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="a18e8-1914">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="a18e8-1915">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="a18e8-1915">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="a18e8-1916">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="a18e8-1916">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1917">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1918">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a18e8-1918">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-1919">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-1919">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-1920">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-1920">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-1921">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-1921">Az.Compute</span></span>
* <span data-ttu-id="a18e8-1922">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1922">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a18e8-1923">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-1923">Az.ContainerInstance</span></span>
* <span data-ttu-id="a18e8-1924">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-1924">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a18e8-1925">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1925">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a18e8-1926">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1926">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a18e8-1927">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1927">Get the Edge Storage Container</span></span>
* <span data-ttu-id="a18e8-1928">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1928">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a18e8-1929">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1929">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="a18e8-1930">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1930">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a18e8-1931">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1931">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="a18e8-1932">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1932">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="a18e8-1933">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1933">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="a18e8-1934">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1934">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a18e8-1935">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1935">Get the Edge Storage Account</span></span>
* <span data-ttu-id="a18e8-1936">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1936">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a18e8-1937">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1937">Create new Edge Storage Account</span></span>
* <span data-ttu-id="a18e8-1938">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1938">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="a18e8-1939">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1939">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="a18e8-1940">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1940">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="a18e8-1941">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-1941">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="a18e8-1942">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="a18e8-1942">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="a18e8-1943">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="a18e8-1943">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1944">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1944">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1945">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a18e8-1945">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="a18e8-1946">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1946">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="a18e8-1947">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1947">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="a18e8-1948">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a18e8-1948">Az.DevTestLabs</span></span>
* <span data-ttu-id="a18e8-1949">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="a18e8-1949">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-1950">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-1950">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-1951">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="a18e8-1951">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-1952">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-1952">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-1953">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1953">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a18e8-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a18e8-1954">Az.MachineLearning</span></span>
* <span data-ttu-id="a18e8-1955">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="a18e8-1955">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="a18e8-1956">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1956">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="a18e8-1957">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-1957">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="a18e8-1958">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1958">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="a18e8-1959">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1959">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="a18e8-1960">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a18e8-1960">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="a18e8-1961">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="a18e8-1961">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="a18e8-1962">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="a18e8-1962">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-1963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-1963">Az.Network</span></span>
* <span data-ttu-id="a18e8-1964">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="a18e8-1964">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-1965">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-1965">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-1966">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1966">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="a18e8-1967">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1967">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a18e8-1968">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1968">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="a18e8-1969">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1969">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-1970">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-1970">Az.Resources</span></span>
* <span data-ttu-id="a18e8-1971">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1971">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-1972">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-1972">Az.Sql</span></span>
* <span data-ttu-id="a18e8-1973">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1973">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="a18e8-1974">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-1974">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="a18e8-1975">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a18e8-1975">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="a18e8-1976">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="a18e8-1976">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-1977">Az.Storage</span></span>
* <span data-ttu-id="a18e8-1978">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="a18e8-1978">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="a18e8-1979">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-1979">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="a18e8-1980">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="a18e8-1980">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="a18e8-1981">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-1981">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="a18e8-1982">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-1982">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="a18e8-1983">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-1983">General</span></span>
* <span data-ttu-id="a18e8-1984">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="a18e8-1984">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-1985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-1985">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-1986">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="a18e8-1986">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="a18e8-1987">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="a18e8-1987">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-1988">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-1988">Az.Batch</span></span>
* <span data-ttu-id="a18e8-1989">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="a18e8-1989">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-1990">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-1990">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-1991">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-1991">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-1992">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-1992">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-1993">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="a18e8-1993">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="a18e8-1994">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="a18e8-1994">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a18e8-1995">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a18e8-1995">Az.HealthcareApis</span></span>
* <span data-ttu-id="a18e8-1996">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="a18e8-1996">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-1997">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-1997">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-1998">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="a18e8-1998">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="a18e8-1999">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="a18e8-1999">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="a18e8-2000">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2000">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-2001">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2001">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-2002">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2002">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="a18e8-2003">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="a18e8-2003">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="a18e8-2004">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2004">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2005">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2005">Az.Network</span></span>
* <span data-ttu-id="a18e8-2006">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2006">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2007">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2007">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2008">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2008">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="a18e8-2009">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2009">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2010">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2010">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2011">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="a18e8-2011">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2012">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2012">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2013">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="a18e8-2013">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="a18e8-2014">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-2014">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="a18e8-2015">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-2015">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="a18e8-2016">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2016">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="a18e8-2017">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="a18e8-2017">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="a18e8-2018">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2018">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="a18e8-2019">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2019">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="a18e8-2020">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2020">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="a18e8-2021">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2021">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="a18e8-2022">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2022">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="a18e8-2023">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a18e8-2023">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="a18e8-2024">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2024">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="a18e8-2025">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a18e8-2025">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="a18e8-2026">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2026">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-2027">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-2027">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-2028">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2028">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="a18e8-2029">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2029">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2030">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2031">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2031">VM Reapply feature</span></span>
    - <span data-ttu-id="a18e8-2032">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2032">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="a18e8-2033">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2033">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="a18e8-2034">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2034">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="a18e8-2035">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2035">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="a18e8-2036">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2036">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a18e8-2037">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a18e8-2037">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="a18e8-2038">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="a18e8-2038">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="a18e8-2039">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2039">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="a18e8-2040">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a18e8-2040">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="a18e8-2041">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2041">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="a18e8-2042">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="a18e8-2042">Az.DataBoxEdge</span></span>
* <span data-ttu-id="a18e8-2043">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2043">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a18e8-2044">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="a18e8-2044">Get the Order</span></span>
* <span data-ttu-id="a18e8-2045">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2045">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a18e8-2046">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="a18e8-2046">Create new Order</span></span>
* <span data-ttu-id="a18e8-2047">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2047">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="a18e8-2048">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="a18e8-2048">Remove the Order</span></span>
* <span data-ttu-id="a18e8-2049">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="a18e8-2049">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="a18e8-2050">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="a18e8-2050">Now creates Local Share</span></span>
* <span data-ttu-id="a18e8-2051">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2051">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="a18e8-2052">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="a18e8-2052">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="a18e8-2053">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2053">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="a18e8-2054">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2054">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="a18e8-2055">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2055">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a18e8-2056">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2056">Gets the information about Triggers</span></span>
* <span data-ttu-id="a18e8-2057">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2057">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a18e8-2058">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2058">Create new Triggers</span></span>
* <span data-ttu-id="a18e8-2059">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2059">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="a18e8-2060">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2060">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2061">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2061">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2062">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2062">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="a18e8-2063">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2063">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-2064">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-2064">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-2065">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a18e8-2065">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-2066">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2066">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-2067">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2067">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-2068">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2068">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-2069">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2069">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="a18e8-2070">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2070">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="a18e8-2071">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="a18e8-2071">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="a18e8-2072">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2072">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2073">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2073">Az.Network</span></span>
* <span data-ttu-id="a18e8-2074">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2074">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="a18e8-2075">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="a18e8-2075">Az.PrivateDns</span></span>
* <span data-ttu-id="a18e8-2076">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2076">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2077">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2077">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2078">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2078">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="a18e8-2079">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2079">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="a18e8-2080">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2080">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a18e8-2081">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a18e8-2081">Az.RedisCache</span></span>
* <span data-ttu-id="a18e8-2082">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2082">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="a18e8-2083">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2083">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="a18e8-2084">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2084">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2085">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2085">Az.Resources</span></span>
- <span data-ttu-id="a18e8-2086">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2086">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="a18e8-2087">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2087">Updated create policy definition help example</span></span>
- <span data-ttu-id="a18e8-2088">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2088">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="a18e8-2089">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2089">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="a18e8-2090">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2090">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2091">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2091">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2092">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2092">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="a18e8-2093">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="a18e8-2093">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="a18e8-2094">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2094">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="a18e8-2095">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-2095">General</span></span>
* <span data-ttu-id="a18e8-2096">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2096">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2097">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2098">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2098">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a18e8-2099">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2099">Az.Advisor</span></span>
* <span data-ttu-id="a18e8-2100">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2100">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-2101">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-2101">Az.Batch</span></span>
* <span data-ttu-id="a18e8-2102">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2102">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="a18e8-2103">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2103">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="a18e8-2104">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2104">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="a18e8-2105">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2105">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="a18e8-2106">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2106">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="a18e8-2107">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2107">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="a18e8-2108">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2108">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="a18e8-2109">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2109">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="a18e8-2110">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2110">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="a18e8-2111">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2111">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a18e8-2112">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2112">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="a18e8-2113">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2113">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="a18e8-2114">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2114">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="a18e8-2115">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2115">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="a18e8-2116">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2116">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="a18e8-2117">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2117">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="a18e8-2118">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2118">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="a18e8-2119">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2119">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="a18e8-2120">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2120">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="a18e8-2121">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2121">This operation is no longer supported.</span></span>
* <span data-ttu-id="a18e8-2122">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2122">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a18e8-2123">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2123">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="a18e8-2124">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2124">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="a18e8-2125">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2125">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="a18e8-2126">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2126">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="a18e8-2127">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2127">New non-verified images are also now returned.</span></span> <span data-ttu-id="a18e8-2128">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2128">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="a18e8-2129">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2129">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="a18e8-2130">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2130">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="a18e8-2131">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2131">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="a18e8-2132">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2132">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="a18e8-2133">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2133">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="a18e8-2134">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2134">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="a18e8-2135">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2135">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="a18e8-2136">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="a18e8-2136">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="a18e8-2137">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="a18e8-2137">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-2138">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-2138">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-2139">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2139">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="a18e8-2140">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2140">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2141">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2141">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2142">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="a18e8-2142">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="a18e8-2143">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-2143">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="a18e8-2144">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a18e8-2144">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="a18e8-2145">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2145">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a18e8-2146">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2146">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="a18e8-2147">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="a18e8-2147">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="a18e8-2148">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2148">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="a18e8-2149">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="a18e8-2149">Breaking changes</span></span>
    - <span data-ttu-id="a18e8-2150">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2150">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="a18e8-2151">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2151">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2152">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2152">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2153">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2153">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-2154">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-2154">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-2155">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="a18e8-2155">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="a18e8-2156">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2156">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="a18e8-2157">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="a18e8-2157">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="a18e8-2158">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="a18e8-2158">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="a18e8-2159">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2159">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="a18e8-2160">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="a18e8-2160">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-2161">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2161">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-2162">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2162">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-2163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-2163">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-2164">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2164">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="a18e8-2165">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2165">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="a18e8-2166">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2166">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="a18e8-2167">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2167">Removed five cmdlets:</span></span>
    - <span data-ttu-id="a18e8-2168">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2168">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a18e8-2169">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2169">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a18e8-2170">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2170">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="a18e8-2171">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-2171">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="a18e8-2172">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-2172">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="a18e8-2173">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2173">Added three cmdlets:</span></span>
    - <span data-ttu-id="a18e8-2174">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2174">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a18e8-2175">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2175">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="a18e8-2176">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2176">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="a18e8-2177">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2177">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="a18e8-2178">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2178">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="a18e8-2179">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2179">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="a18e8-2180">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2180">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="a18e8-2181">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2181">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="a18e8-2182">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2182">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="a18e8-2183">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2183">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="a18e8-2184">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2184">Added some scenario test cases.</span></span>
* <span data-ttu-id="a18e8-2185">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2185">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-2186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2186">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-2187">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2187">Breaking changes:</span></span>
    - <span data-ttu-id="a18e8-2188">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2188">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a18e8-2189">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2189">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a18e8-2190">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2190">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a18e8-2191">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2191">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a18e8-2192">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2192">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="a18e8-2193">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2193">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="a18e8-2194">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2194">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="a18e8-2195">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2195">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="a18e8-2196">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2196">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a18e8-2197">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2197">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="a18e8-2198">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2198">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="a18e8-2199">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2199">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2200">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2200">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2201">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2201">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2202">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2202">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="a18e8-2203">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2203">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="a18e8-2204">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2204">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2205">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2205">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2206">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2206">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2207">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2207">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2208">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2208">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-2209">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="a18e8-2209">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2210">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2211">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="a18e8-2211">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2212">Az.Network</span></span>
* <span data-ttu-id="a18e8-2213">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2213">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="a18e8-2214">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2214">Updated cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2215">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2215">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2216">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2216">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2217">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2217">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2218">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2218">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2219">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2219">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a18e8-2220">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2220">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="a18e8-2221">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2221">New cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2222">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a18e8-2222">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="a18e8-2223">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2223">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="a18e8-2224">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2224">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="a18e8-2225">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2225">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="a18e8-2226">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2226">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="a18e8-2227">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2227">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="a18e8-2228">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2228">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="a18e8-2229">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2229">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="a18e8-2230">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2230">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-2231">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2231">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="a18e8-2232">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-2232">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a18e8-2233">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-2233">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a18e8-2234">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-2234">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="a18e8-2235">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2235">Set-AzVirtualHub</span></span>
* <span data-ttu-id="a18e8-2236">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a18e8-2236">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="a18e8-2237">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2237">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a18e8-2238">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2238">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a18e8-2239">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2239">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="a18e8-2240">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2240">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="a18e8-2241">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2241">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="a18e8-2242">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2242">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="a18e8-2243">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2243">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-2244">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2244">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="a18e8-2245">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2245">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a18e8-2246">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2246">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a18e8-2247">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2247">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a18e8-2248">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2248">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a18e8-2249">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2249">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="a18e8-2250">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2250">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="a18e8-2251">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="a18e8-2251">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="a18e8-2252">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2252">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-2253">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a18e8-2253">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="a18e8-2254">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2254">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="a18e8-2255">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a18e8-2255">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="a18e8-2256">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a18e8-2256">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="a18e8-2257">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-2257">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="a18e8-2258">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-2258">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="a18e8-2259">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2259">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a18e8-2260">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2260">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="a18e8-2261">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-2261">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="a18e8-2262">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="a18e8-2262">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="a18e8-2263">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="a18e8-2263">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="a18e8-2264">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="a18e8-2265">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2265">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="a18e8-2266">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2266">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="a18e8-2267">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2267">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="a18e8-2268">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2268">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="a18e8-2269">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2269">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="a18e8-2270">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2270">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-2271">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2271">New-AzIpGroup</span></span>
        - <span data-ttu-id="a18e8-2272">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2272">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="a18e8-2273">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2273">Get-AzIpGroup</span></span>
        - <span data-ttu-id="a18e8-2274">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2274">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-2275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2275">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-2276">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2276">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2277">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2278">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2278">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="a18e8-2279">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2279">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="a18e8-2280">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2280">Removed deprecated aliases:</span></span>
* <span data-ttu-id="a18e8-2281">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2281">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="a18e8-2282">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2282">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="a18e8-2283">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2283">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a18e8-2284">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2284">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="a18e8-2285">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="a18e8-2285">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="a18e8-2286">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2286">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2287">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2287">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2288">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-2288">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="a18e8-2289">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2289">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a18e8-2290">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2290">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a18e8-2291">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="a18e8-2291">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="a18e8-2292">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a18e8-2292">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="a18e8-2293">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a18e8-2293">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="a18e8-2294">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2294">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a18e8-2295">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-2295">General</span></span>
* <span data-ttu-id="a18e8-2296">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2296">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2297">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2298">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2298">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-2299">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2299">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-2300">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-2300">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a18e8-2301">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a18e8-2301">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-2302">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2302">Az.Automation</span></span>
* <span data-ttu-id="a18e8-2303">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2303">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-2304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-2304">Az.Batch</span></span>
* <span data-ttu-id="a18e8-2305">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2305">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2306">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2306">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2307">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2307">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a18e8-2308">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2308">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a18e8-2309">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2309">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="a18e8-2310">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2310">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2311">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2312">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2312">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a18e8-2313">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2313">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a18e8-2314">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2314">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-2315">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-2315">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-2316">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="a18e8-2316">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a18e8-2317">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a18e8-2317">Az.HealthcareApis</span></span>
* <span data-ttu-id="a18e8-2318">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2318">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a18e8-2319">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="a18e8-2319">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a18e8-2320">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="a18e8-2320">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a18e8-2321">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2321">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-2322">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2322">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-2323">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a18e8-2323">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a18e8-2324">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="a18e8-2324">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2325">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-2326">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a18e8-2326">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a18e8-2327">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2327">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a18e8-2328">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="a18e8-2328">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a18e8-2329">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2329">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2330">Az.Network</span></span>
* <span data-ttu-id="a18e8-2331">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2331">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a18e8-2332">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-2332">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a18e8-2333">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2333">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-2334">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2334">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a18e8-2335">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2335">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a18e8-2336">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="a18e8-2336">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a18e8-2337">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2337">Updated cmdlets:</span></span>
        - <span data-ttu-id="a18e8-2338">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2338">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a18e8-2339">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2339">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a18e8-2340">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2340">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a18e8-2341">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="a18e8-2341">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a18e8-2342">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a18e8-2342">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a18e8-2343">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2343">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a18e8-2344">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2344">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a18e8-2345">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a18e8-2345">Az.RedisCache</span></span>
* <span data-ttu-id="a18e8-2346">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2346">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2347">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2347">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2348">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2348">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2349">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2350">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-2350">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a18e8-2351">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a18e8-2351">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a18e8-2352">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a18e8-2352">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a18e8-2353">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="a18e8-2353">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a18e8-2354">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2354">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-2355">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-2355">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-2356">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2356">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2357">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2357">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2358">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="a18e8-2358">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a18e8-2359">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2359">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-2360">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2360">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-2361">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2361">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a18e8-2362">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2362">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a18e8-2363">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2363">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-2364">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2364">Az.Automation</span></span>
* <span data-ttu-id="a18e8-2365">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2365">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a18e8-2366">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="a18e8-2366">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a18e8-2367">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2367">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2368">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2368">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2369">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2369">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a18e8-2370">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2370">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a18e8-2371">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2371">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a18e8-2372">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2372">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a18e8-2373">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2373">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a18e8-2374">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2374">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a18e8-2375">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2375">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a18e8-2376">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2376">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a18e8-2377">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2377">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2378">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2378">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2379">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a18e8-2379">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a18e8-2380">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="a18e8-2380">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-2381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-2381">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-2382">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="a18e8-2382">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-2383">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2383">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-2384">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2384">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a18e8-2385">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2385">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a18e8-2386">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2386">New cmdlets are:</span></span>
    - <span data-ttu-id="a18e8-2387">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a18e8-2387">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a18e8-2388">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a18e8-2388">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a18e8-2389">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a18e8-2389">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a18e8-2390">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a18e8-2390">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-2391">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2391">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-2392">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-2392">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a18e8-2393">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2393">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a18e8-2394">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2394">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a18e8-2395">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2395">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a18e8-2396">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2396">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a18e8-2397">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2397">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a18e8-2398">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2398">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a18e8-2399">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2399">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a18e8-2400">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2400">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a18e8-2401">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2401">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a18e8-2402">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2402">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a18e8-2403">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2403">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a18e8-2404">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="a18e8-2404">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a18e8-2405">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="a18e8-2405">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a18e8-2406">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="a18e8-2406">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a18e8-2407">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2407">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a18e8-2408">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2408">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a18e8-2409">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-2409">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a18e8-2410">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2410">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a18e8-2411">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-2411">Overall improved help files</span></span>
* <span data-ttu-id="a18e8-2412">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2412">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2413">Az.Network</span></span>
* <span data-ttu-id="a18e8-2414">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2414">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="a18e8-2415">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="a18e8-2415">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a18e8-2416">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="a18e8-2416">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a18e8-2417">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="a18e8-2417">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a18e8-2418">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="a18e8-2418">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a18e8-2419">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="a18e8-2419">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a18e8-2420">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2420">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a18e8-2421">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a18e8-2421">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a18e8-2422">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-2422">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a18e8-2423">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2423">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a18e8-2424">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2424">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a18e8-2425">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-2425">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a18e8-2426">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2426">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2427">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a18e8-2427">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a18e8-2428">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2428">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a18e8-2429">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2429">Updated cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2430">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a18e8-2430">New-VpnSite</span></span>
        - <span data-ttu-id="a18e8-2431">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a18e8-2431">Update-VpnSite</span></span>
        - <span data-ttu-id="a18e8-2432">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2432">New-VpnConnection</span></span>
        - <span data-ttu-id="a18e8-2433">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2433">Update-VpnConnection</span></span>
* <span data-ttu-id="a18e8-2434">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2434">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2435">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2436">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2436">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a18e8-2437">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="a18e8-2437">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2438">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2438">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2439">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2439">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-2440">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2440">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-2441">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2441">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a18e8-2442">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2442">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a18e8-2443">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a18e8-2443">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a18e8-2444">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a18e8-2444">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a18e8-2445">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2445">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a18e8-2446">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2446">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a18e8-2447">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a18e8-2447">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a18e8-2448">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a18e8-2448">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a18e8-2449">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a18e8-2449">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a18e8-2450">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2450">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a18e8-2451">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2451">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a18e8-2452">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a18e8-2452">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a18e8-2453">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a18e8-2453">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a18e8-2454">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a18e8-2454">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a18e8-2455">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a18e8-2455">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a18e8-2456">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2456">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a18e8-2457">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-2457">Az.SignalR</span></span>
* <span data-ttu-id="a18e8-2458">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2458">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2459">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2460">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2460">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a18e8-2461">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="a18e8-2461">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a18e8-2462">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2462">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a18e8-2463">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2463">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a18e8-2464">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a18e8-2464">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2465">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2465">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2466">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2466">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a18e8-2467">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="a18e8-2467">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a18e8-2468">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-2468">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a18e8-2469">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-2469">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a18e8-2470">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2470">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a18e8-2471">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-2471">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a18e8-2472">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-2472">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a18e8-2473">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2473">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a18e8-2474">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2474">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a18e8-2475">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2475">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a18e8-2476">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-2476">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2477">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2477">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2478">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="a18e8-2478">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a18e8-2479">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="a18e8-2479">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a18e8-2480">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2480">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a18e8-2481">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2481">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a18e8-2482">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-2482">General</span></span>
* <span data-ttu-id="a18e8-2483">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2483">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2484">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2484">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2485">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2485">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-2486">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-2486">Az.Aks</span></span>
* <span data-ttu-id="a18e8-2487">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2487">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a18e8-2488">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a18e8-2488">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-2489">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2489">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-2490">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a18e8-2490">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a18e8-2491">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="a18e8-2491">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a18e8-2492">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2492">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a18e8-2493">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a18e8-2493">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a18e8-2494">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2494">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-2495">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-2495">Az.Batch</span></span>
* <span data-ttu-id="a18e8-2496">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="a18e8-2496">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-2497">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-2498">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="a18e8-2498">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2499">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2500">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2500">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a18e8-2501">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2501">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a18e8-2502">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2502">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a18e8-2503">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2503">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a18e8-2504">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a18e8-2504">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a18e8-2505">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2505">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a18e8-2506">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="a18e8-2506">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a18e8-2507">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2507">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2508">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2508">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2509">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2509">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a18e8-2510">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="a18e8-2510">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a18e8-2511">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a18e8-2511">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a18e8-2512">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="a18e8-2512">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-2513">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-2513">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-2514">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2514">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-2515">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2515">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-2516">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-2516">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a18e8-2517">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="a18e8-2517">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a18e8-2518">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a18e8-2518">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a18e8-2519">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="a18e8-2519">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a18e8-2520">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a18e8-2520">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a18e8-2521">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2521">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-2522">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2522">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-2523">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-2523">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2524">Az.Network</span></span>
* <span data-ttu-id="a18e8-2525">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2525">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a18e8-2526">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2526">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a18e8-2527">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2527">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a18e8-2528">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="a18e8-2528">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a18e8-2529">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2529">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="a18e8-2530">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2530">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a18e8-2531">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a18e8-2531">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-2532">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2532">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-2533">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2533">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a18e8-2534">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2534">Added example</span></span>
    - <span data-ttu-id="a18e8-2535">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2535">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a18e8-2536">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a18e8-2536">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a18e8-2537">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="a18e8-2537">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2538">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2538">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2539">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2539">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2540">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2540">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2541">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="a18e8-2541">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a18e8-2542">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="a18e8-2542">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a18e8-2543">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2543">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a18e8-2544">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-2544">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-2545">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-2545">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-2546">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-2546">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a18e8-2547">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="a18e8-2547">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a18e8-2548">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="a18e8-2548">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-2549">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2549">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-2550">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2550">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a18e8-2551">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2551">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a18e8-2552">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a18e8-2552">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a18e8-2553">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2553">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a18e8-2554">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a18e8-2554">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a18e8-2555">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a18e8-2555">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2556">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2557">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2557">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2558">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2559">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="a18e8-2559">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a18e8-2560">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="a18e8-2560">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a18e8-2561">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-2561">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a18e8-2562">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2562">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a18e8-2563">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="a18e8-2563">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a18e8-2564">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2564">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2565">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2566">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a18e8-2566">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a18e8-2567">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2567">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2568">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2569">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a18e8-2569">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a18e8-2570">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2570">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a18e8-2571">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2571">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-2572">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2572">Az.Automation</span></span>
* <span data-ttu-id="a18e8-2573">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2573">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-2574">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2574">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-2575">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2575">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2576">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2576">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2577">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2577">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-2578">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-2578">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-2579">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="a18e8-2579">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a18e8-2580">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a18e8-2580">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2581">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2581">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2582">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2582">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a18e8-2583">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="a18e8-2583">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-2584">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2584">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-2585">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-2585">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a18e8-2586">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="a18e8-2586">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-2587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-2587">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-2588">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2588">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-2589">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-2589">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-2590">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="a18e8-2590">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a18e8-2591">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="a18e8-2591">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a18e8-2592">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2592">Az.ManagedServices</span></span>
* <span data-ttu-id="a18e8-2593">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2593">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2594">Az.Network</span></span>
* <span data-ttu-id="a18e8-2595">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2595">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a18e8-2596">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2596">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2597">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-2597">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a18e8-2598">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2598">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a18e8-2599">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2599">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2600">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2600">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2601">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2601">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2602">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2602">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a18e8-2603">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a18e8-2603">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a18e8-2604">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2604">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a18e8-2605">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="a18e8-2605">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a18e8-2606">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="a18e8-2606">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a18e8-2607">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2607">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a18e8-2608">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2608">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a18e8-2609">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="a18e8-2609">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a18e8-2610">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="a18e8-2610">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a18e8-2611">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2611">Updated cmdlets</span></span>
        - <span data-ttu-id="a18e8-2612">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2612">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a18e8-2613">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2613">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a18e8-2614">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2614">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a18e8-2615">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2615">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a18e8-2616">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-2616">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a18e8-2617">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2617">Updated cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2618">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2618">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a18e8-2619">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2619">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a18e8-2620">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2620">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a18e8-2621">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="a18e8-2621">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a18e8-2622">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2622">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a18e8-2623">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2623">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-2624">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2624">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-2625">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2625">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="a18e8-2626">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="a18e8-2626">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2627">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2628">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2628">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a18e8-2629">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2629">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a18e8-2630">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2630">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a18e8-2631">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2631">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a18e8-2632">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2632">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a18e8-2633">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2633">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a18e8-2634">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2634">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a18e8-2635">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2635">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a18e8-2636">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2636">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a18e8-2637">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2637">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2638">Az.Resources</span></span>
- <span data-ttu-id="a18e8-2639">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2639">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a18e8-2640">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-2640">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-2641">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-2641">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-2642">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-2642">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a18e8-2643">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="a18e8-2643">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2644">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2645">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a18e8-2645">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a18e8-2646">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="a18e8-2646">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a18e8-2647">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2647">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2648">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2649">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="a18e8-2649">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-2650">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-2650">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-2651">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2651">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a18e8-2652">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="a18e8-2652">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2653">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2653">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2654">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-2654">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a18e8-2655">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-2655">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a18e8-2656">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="a18e8-2656">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a18e8-2657">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2657">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2658">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2658">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2659">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="a18e8-2659">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a18e8-2660">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2660">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a18e8-2661">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a18e8-2661">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a18e8-2662">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2662">Az.Advisor</span></span>
* <span data-ttu-id="a18e8-2663">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2663">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a18e8-2664">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2664">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-2665">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2665">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-2666">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a18e8-2666">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a18e8-2667">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2667">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a18e8-2668">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="a18e8-2668">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a18e8-2669">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2669">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a18e8-2670">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a18e8-2670">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a18e8-2671">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2671">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a18e8-2672">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="a18e8-2672">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-2673">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2673">Az.Automation</span></span>
* <span data-ttu-id="a18e8-2674">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2674">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2675">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2676">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2676">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-2677">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-2677">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-2678">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2678">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a18e8-2679">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a18e8-2679">Az.EventGrid</span></span>
* <span data-ttu-id="a18e8-2680">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2680">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-2681">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2681">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-2682">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2682">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2683">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2683">Az.Network</span></span>
* <span data-ttu-id="a18e8-2684">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="a18e8-2684">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a18e8-2685">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2685">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-2686">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2686">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-2687">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a18e8-2687">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a18e8-2688">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a18e8-2688">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-2689">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2689">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-2690">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a18e8-2690">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2691">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2692">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2692">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2693">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2693">Az.Resources</span></span>
    - <span data-ttu-id="a18e8-2694">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="a18e8-2694">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a18e8-2695">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="a18e8-2695">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a18e8-2696">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2696">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a18e8-2697">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2697">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-2698">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-2698">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-2699">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="a18e8-2699">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2700">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2701">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="a18e8-2701">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a18e8-2702">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2702">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a18e8-2703">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2703">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a18e8-2704">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2704">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a18e8-2705">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2705">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a18e8-2706">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2706">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a18e8-2707">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2707">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a18e8-2708">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2708">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a18e8-2709">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="a18e8-2709">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2710">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2711">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2711">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a18e8-2712">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a18e8-2712">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a18e8-2713">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2713">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a18e8-2714">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="a18e8-2714">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a18e8-2715">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2715">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a18e8-2716">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2716">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a18e8-2717">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2717">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a18e8-2718">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2718">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a18e8-2719">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a18e8-2719">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a18e8-2720">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a18e8-2720">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a18e8-2721">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a18e8-2721">Az.StorageSync</span></span>
* <span data-ttu-id="a18e8-2722">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2722">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a18e8-2723">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2723">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2724">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2724">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2725">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="a18e8-2725">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a18e8-2726">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a18e8-2726">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a18e8-2727">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="a18e8-2727">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a18e8-2728">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a18e8-2728">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a18e8-2729">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a18e8-2729">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2730">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2731">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2731">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a18e8-2732">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2732">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a18e8-2733">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a18e8-2733">Az.Dns</span></span>
* <span data-ttu-id="a18e8-2734">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2734">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a18e8-2735">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a18e8-2735">Az.EventGrid</span></span>
* <span data-ttu-id="a18e8-2736">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2736">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a18e8-2737">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2737">New cmdlets:</span></span>
    - <span data-ttu-id="a18e8-2738">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a18e8-2738">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a18e8-2739">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2739">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a18e8-2740">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a18e8-2740">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a18e8-2741">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2741">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a18e8-2742">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a18e8-2742">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a18e8-2743">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2743">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a18e8-2744">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2744">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a18e8-2745">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2745">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a18e8-2746">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2746">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a18e8-2747">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2747">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a18e8-2748">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2748">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a18e8-2749">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2749">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a18e8-2750">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a18e8-2750">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a18e8-2751">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="a18e8-2751">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="a18e8-2752">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2752">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a18e8-2753">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2753">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a18e8-2754">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2754">Updated cmdlets:</span></span>
    - <span data-ttu-id="a18e8-2755">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2755">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a18e8-2756">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2756">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a18e8-2757">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2757">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a18e8-2758">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="a18e8-2758">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a18e8-2759">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2759">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a18e8-2760">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="a18e8-2760">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a18e8-2761">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2761">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a18e8-2762">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2762">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a18e8-2763">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="a18e8-2763">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="a18e8-2764">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2764">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a18e8-2765">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2765">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a18e8-2766">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a18e8-2766">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a18e8-2767">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2767">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a18e8-2768">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2768">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-2769">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2769">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-2770">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2770">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a18e8-2771">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a18e8-2771">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a18e8-2772">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2772">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a18e8-2773">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="a18e8-2773">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2774">Az.Network</span></span>
* <span data-ttu-id="a18e8-2775">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-2775">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a18e8-2776">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2776">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2777">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a18e8-2777">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a18e8-2778">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a18e8-2778">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a18e8-2779">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2779">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2780">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a18e8-2780">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a18e8-2781">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2781">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a18e8-2782">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2782">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2783">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2783">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a18e8-2784">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2784">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a18e8-2785">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a18e8-2785">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a18e8-2786">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2786">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a18e8-2787">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2787">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a18e8-2788">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-2788">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a18e8-2789">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-2789">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-2790">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-2790">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a18e8-2791">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-2791">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a18e8-2792">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a18e8-2792">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a18e8-2793">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2793">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a18e8-2794">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a18e8-2794">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a18e8-2795">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2795">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a18e8-2796">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2796">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a18e8-2797">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2797">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a18e8-2798">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2798">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a18e8-2799">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a18e8-2799">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a18e8-2800">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-2800">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a18e8-2801">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2801">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a18e8-2802">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-2802">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a18e8-2803">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="a18e8-2803">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a18e8-2804">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-2804">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a18e8-2805">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-2805">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a18e8-2806">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="a18e8-2806">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a18e8-2807">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2807">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a18e8-2808">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2808">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2809">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="a18e8-2809">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a18e8-2810">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-2810">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a18e8-2811">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2811">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a18e8-2812">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a18e8-2812">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="a18e8-2813">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2813">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="a18e8-2814">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2814">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a18e8-2815">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2815">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a18e8-2816">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2816">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-2817">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2817">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-2818">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2818">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2819">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2820">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2820">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a18e8-2821">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2821">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a18e8-2822">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2822">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a18e8-2823">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="a18e8-2823">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-2824">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2824">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-2825">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="a18e8-2825">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2826">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2826">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2827">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="a18e8-2827">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a18e8-2828">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="a18e8-2828">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a18e8-2829">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2829">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a18e8-2830">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2830">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a18e8-2831">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2831">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a18e8-2832">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a18e8-2832">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a18e8-2833">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a18e8-2833">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a18e8-2834">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a18e8-2834">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-2835">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-2835">Az.Storage</span></span>
* <span data-ttu-id="a18e8-2836">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-2836">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a18e8-2837">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-2837">New-AzStorageAccount</span></span>
* <span data-ttu-id="a18e8-2838">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="a18e8-2838">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a18e8-2839">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2839">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2840">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2840">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2841">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="a18e8-2841">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a18e8-2842">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a18e8-2842">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a18e8-2843">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2843">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a18e8-2844">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-2844">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-2845">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2845">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2846">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2846">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2847">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2847">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a18e8-2848">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-2848">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-2849">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-2849">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-2850">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2850">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a18e8-2851">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18e8-2851">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2852">Az.Network</span></span>
* <span data-ttu-id="a18e8-2853">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="a18e8-2853">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a18e8-2854">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="a18e8-2854">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-2855">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-2855">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-2856">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a18e8-2856">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-2857">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2857">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-2858">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="a18e8-2858">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-2859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-2859">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-2860">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18e8-2860">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-2861">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2861">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-2862">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2862">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a18e8-2863">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2863">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2864">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2865">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2865">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a18e8-2866">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-2866">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a18e8-2867">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="a18e8-2867">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a18e8-2868">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2868">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-2869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-2869">Az.Websites</span></span>
* <span data-ttu-id="a18e8-2870">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2870">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a18e8-2871">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2871">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a18e8-2872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2872">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-2873">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2873">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a18e8-2874">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2874">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a18e8-2875">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2875">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a18e8-2876">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="a18e8-2876">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a18e8-2877">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2877">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a18e8-2878">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="a18e8-2878">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a18e8-2879">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2879">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a18e8-2880">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2880">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a18e8-2881">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2881">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a18e8-2882">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="a18e8-2882">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a18e8-2883">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2883">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a18e8-2884">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="a18e8-2884">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a18e8-2885">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="a18e8-2885">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a18e8-2886">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2886">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a18e8-2887">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2887">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a18e8-2888">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2888">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a18e8-2889">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2889">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a18e8-2890">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="a18e8-2890">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a18e8-2891">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2891">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="a18e8-2892">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="a18e8-2892">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a18e8-2893">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="a18e8-2893">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a18e8-2894">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2894">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a18e8-2895">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2895">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a18e8-2896">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-2896">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="a18e8-2897">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2897">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a18e8-2898">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2898">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a18e8-2899">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2899">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a18e8-2900">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2900">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a18e8-2901">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2901">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a18e8-2902">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2902">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a18e8-2903">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2903">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="a18e8-2904">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a18e8-2904">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a18e8-2905">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2905">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a18e8-2906">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2906">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a18e8-2907">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2907">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a18e8-2908">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="a18e8-2908">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a18e8-2909">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2909">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a18e8-2910">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2910">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a18e8-2911">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2911">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a18e8-2912">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2912">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a18e8-2913">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2913">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a18e8-2914">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2914">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a18e8-2915">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2915">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a18e8-2916">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2916">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a18e8-2917">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2917">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a18e8-2918">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2918">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a18e8-2919">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2919">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a18e8-2920">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2920">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="a18e8-2921">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2921">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a18e8-2922">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2922">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a18e8-2923">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2923">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a18e8-2924">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2924">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a18e8-2925">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2925">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a18e8-2926">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2926">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a18e8-2927">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2927">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a18e8-2928">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2928">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a18e8-2929">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2929">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a18e8-2930">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2930">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a18e8-2931">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2931">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a18e8-2932">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2932">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a18e8-2933">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a18e8-2933">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a18e8-2934">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2934">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a18e8-2935">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2935">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a18e8-2936">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2936">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a18e8-2937">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="a18e8-2937">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a18e8-2938">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2938">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a18e8-2939">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a18e8-2939">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a18e8-2940">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2940">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a18e8-2941">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a18e8-2941">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a18e8-2942">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2942">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a18e8-2943">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a18e8-2943">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a18e8-2944">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2944">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a18e8-2945">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2945">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a18e8-2946">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-2946">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a18e8-2947">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2947">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="a18e8-2948">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2948">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a18e8-2949">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2949">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-2950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-2950">Az.Automation</span></span>
* <span data-ttu-id="a18e8-2951">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2951">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a18e8-2952">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a18e8-2952">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a18e8-2953">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a18e8-2953">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a18e8-2954">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2954">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a18e8-2955">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a18e8-2955">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a18e8-2956">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2956">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a18e8-2957">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2957">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2958">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2959">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2959">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a18e8-2960">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2960">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-2961">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-2961">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-2962">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2962">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-2963">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2963">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-2964">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-2964">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-2965">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-2965">Az.Network</span></span>
* <span data-ttu-id="a18e8-2966">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="a18e8-2966">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a18e8-2967">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a18e8-2967">Updated cmdlet:</span></span>
        - <span data-ttu-id="a18e8-2968">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-2968">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a18e8-2969">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a18e8-2969">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-2970">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-2970">Az.Resources</span></span>
* <span data-ttu-id="a18e8-2971">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="a18e8-2971">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-2972">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-2972">Az.Sql</span></span>
* <span data-ttu-id="a18e8-2973">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="a18e8-2973">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a18e8-2974">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-2974">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-2975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-2975">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-2976">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="a18e8-2976">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-2977">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-2977">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-2978">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2978">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a18e8-2979">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2979">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-2980">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-2980">Az.Compute</span></span>
* <span data-ttu-id="a18e8-2981">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2981">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a18e8-2982">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-2982">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a18e8-2983">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-2983">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a18e8-2984">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2984">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a18e8-2985">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2985">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a18e8-2986">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-2986">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="a18e8-2987">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="a18e8-2987">Breaking changes</span></span>
    - <span data-ttu-id="a18e8-2988">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2988">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a18e8-2989">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2989">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a18e8-2990">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a18e8-2990">Az.DeploymentManager</span></span>
* <span data-ttu-id="a18e8-2991">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2991">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a18e8-2992">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a18e8-2992">Az.Dns</span></span>
* <span data-ttu-id="a18e8-2993">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="a18e8-2993">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a18e8-2994">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2994">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a18e8-2995">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-2995">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-2996">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-2996">Az.FrontDoor</span></span>
* <span data-ttu-id="a18e8-2997">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-2997">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a18e8-2998">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="a18e8-2998">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-2999">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-2999">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-3000">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3000">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a18e8-3001">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-3001">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a18e8-3002">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-3002">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a18e8-3003">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a18e8-3003">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a18e8-3004">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3004">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a18e8-3005">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3005">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a18e8-3006">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3006">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-3007">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-3007">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-3008">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="a18e8-3008">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="a18e8-3009">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a18e8-3009">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a18e8-3010">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-3010">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a18e8-3011">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a18e8-3011">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a18e8-3012">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3012">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a18e8-3013">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a18e8-3013">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a18e8-3014">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a18e8-3014">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a18e8-3015">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3015">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a18e8-3016">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3016">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a18e8-3017">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3017">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a18e8-3018">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3018">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a18e8-3019">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3019">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a18e8-3020">[Mais](/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="a18e8-3020">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a18e8-3021">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="a18e8-3021">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3022">Az.Network</span></span>
* <span data-ttu-id="a18e8-3023">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="a18e8-3023">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a18e8-3024">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="a18e8-3024">New cmdlets</span></span>
        - <span data-ttu-id="a18e8-3025">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-3025">New-AzNatGateway</span></span>
        - <span data-ttu-id="a18e8-3026">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-3026">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a18e8-3027">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-3027">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a18e8-3028">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-3028">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a18e8-3029">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3029">Updated cmdlets</span></span>
        - <span data-ttu-id="a18e8-3030">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a18e8-3030">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a18e8-3031">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a18e8-3031">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a18e8-3032">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3032">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a18e8-3033">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3033">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a18e8-3034">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3034">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-3035">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3035">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-3036">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3036">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a18e8-3037">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3037">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a18e8-3038">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3038">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3039">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3039">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-3040">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3040">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a18e8-3041">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3041">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a18e8-3042">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3042">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a18e8-3043">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3043">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a18e8-3044">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3044">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a18e8-3045">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3045">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a18e8-3046">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a18e8-3046">Az.Relay</span></span>
* <span data-ttu-id="a18e8-3047">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="a18e8-3047">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-3048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-3048">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-3049">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="a18e8-3049">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3050">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3050">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3051">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="a18e8-3051">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a18e8-3052">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3052">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a18e8-3053">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3053">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a18e8-3054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3054">New-AzStorageAccount</span></span>
* <span data-ttu-id="a18e8-3055">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3055">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a18e8-3056">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3056">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a18e8-3057">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3057">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a18e8-3058">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3058">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3059">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3059">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3060">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-3060">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a18e8-3061">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3061">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a18e8-3062">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3062">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-3063">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-3063">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-3064">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3064">General availability of `Az` module</span></span>
* <span data-ttu-id="a18e8-3065">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a18e8-3065">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a18e8-3066">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a18e8-3066">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a18e8-3067">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3067">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a18e8-3068">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-3068">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a18e8-3069">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3069">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a18e8-3070">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="a18e8-3070">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3071">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3071">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3072">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="a18e8-3072">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a18e8-3073">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-3073">Az.Batch</span></span>
* <span data-ttu-id="a18e8-3074">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3074">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-3075">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-3075">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-3076">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3076">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-3077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3077">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-3078">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3078">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3079">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3080">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="a18e8-3080">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a18e8-3081">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3081">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3082">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="a18e8-3082">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-3083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-3083">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-3084">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3084">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3085">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3085">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3086">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a18e8-3087">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a18e8-3087">Az.EventGrid</span></span>
* <span data-ttu-id="a18e8-3088">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3088">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-3089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3089">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-3090">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="a18e8-3090">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a18e8-3091">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a18e8-3091">Az.HDInsight</span></span>
* <span data-ttu-id="a18e8-3092">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3092">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-3093">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3093">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-3094">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3094">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-3095">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3095">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-3096">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3097">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="a18e8-3097">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a18e8-3098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a18e8-3098">Az.MachineLearning</span></span>
* <span data-ttu-id="a18e8-3099">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3099">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a18e8-3100">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a18e8-3100">Az.Media</span></span>
* <span data-ttu-id="a18e8-3101">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-3102">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-3102">Az.Monitor</span></span>
  * <span data-ttu-id="a18e8-3103">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="a18e8-3103">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a18e8-3104">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a18e8-3104">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a18e8-3105">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a18e8-3105">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a18e8-3106">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3106">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a18e8-3107">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3107">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a18e8-3108">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3108">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a18e8-3109">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a18e8-3109">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3110">Az.Network</span></span>
* <span data-ttu-id="a18e8-3111">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3112">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="a18e8-3112">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a18e8-3113">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a18e8-3113">Az.NotificationHubs</span></span>
* <span data-ttu-id="a18e8-3114">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3114">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-3115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3115">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-3116">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a18e8-3117">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a18e8-3117">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a18e8-3118">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3119">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-3120">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3121">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3121">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a18e8-3122">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a18e8-3122">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a18e8-3123">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="a18e8-3123">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a18e8-3124">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a18e8-3124">Az.RedisCache</span></span>
* <span data-ttu-id="a18e8-3125">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3126">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3127">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="a18e8-3127">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3128">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3129">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="a18e8-3129">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a18e8-3130">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3131">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3131">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a18e8-3132">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3132">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a18e8-3133">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3133">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a18e8-3134">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3134">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a18e8-3135">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="a18e8-3135">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3136">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3136">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3137">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="a18e8-3137">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a18e8-3138">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a18e8-3139">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3139">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a18e8-3140">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3140">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a18e8-3141">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3141">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-3142">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-3142">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-3143">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3143">General availability of `Az` module</span></span>
* <span data-ttu-id="a18e8-3144">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a18e8-3144">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a18e8-3145">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a18e8-3145">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a18e8-3146">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3146">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a18e8-3147">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-3147">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a18e8-3148">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3148">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a18e8-3149">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="a18e8-3149">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3150">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3150">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3151">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a18e8-3151">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-3152">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3152">Az.AnalysisServices</span></span>
* <span data-ttu-id="a18e8-3153">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="a18e8-3153">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a18e8-3154">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="a18e8-3154">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-3155">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3155">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3156">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3156">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a18e8-3157">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3157">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a18e8-3158">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3158">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3159">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3159">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3160">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3160">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a18e8-3161">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3161">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="a18e8-3162">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3162">Az.ContainerInstance</span></span>
* <span data-ttu-id="a18e8-3163">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="a18e8-3163">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-3164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-3164">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-3165">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3165">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a18e8-3166">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3166">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3167">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3168">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="a18e8-3168">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a18e8-3169">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3169">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a18e8-3170">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="a18e8-3170">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a18e8-3171">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a18e8-3171">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a18e8-3172">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="a18e8-3172">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a18e8-3173">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a18e8-3173">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3174">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3174">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3175">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3175">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3176">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3177">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3177">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a18e8-3178">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a18e8-3178">New-AzStorageContext</span></span>
* <span data-ttu-id="a18e8-3179">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-3179">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a18e8-3180">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a18e8-3180">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a18e8-3181">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a18e8-3181">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a18e8-3182">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3182">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a18e8-3183">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3183">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a18e8-3184">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3184">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a18e8-3185">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-3185">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a18e8-3186">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-3186">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a18e8-3187">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-3187">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a18e8-3188">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a18e8-3188">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a18e8-3189">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3189">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a18e8-3190">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="a18e8-3190">Highlights since the last major release</span></span>
* <span data-ttu-id="a18e8-3191">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3191">General availability of `Az` module</span></span>
* <span data-ttu-id="a18e8-3192">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a18e8-3192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a18e8-3193">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a18e8-3193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a18e8-3194">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a18e8-3195">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-3195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a18e8-3196">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a18e8-3197">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="a18e8-3197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-3198">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3198">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3199">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3199">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a18e8-3200">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="a18e8-3200">Dynamic grouping</span></span>
    * <span data-ttu-id="a18e8-3201">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="a18e8-3201">Pre-Post script</span></span>
    * <span data-ttu-id="a18e8-3202">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="a18e8-3202">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3203">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3204">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a18e8-3204">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a18e8-3205">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3205">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-3206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3206">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-3207">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3207">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3208">Az.Network</span></span>
* <span data-ttu-id="a18e8-3209">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3209">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a18e8-3210">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-3210">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3211">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3211">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-3212">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3212">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a18e8-3213">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="a18e8-3213">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3214">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3214">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3215">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a18e8-3215">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a18e8-3216">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="a18e8-3216">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3217">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3218">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3218">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3219">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3220">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-3220">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a18e8-3221">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3221">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a18e8-3222">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3222">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a18e8-3223">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3223">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a18e8-3224">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a18e8-3224">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a18e8-3225">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a18e8-3225">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a18e8-3226">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3226">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3227">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3228">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="a18e8-3228">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="a18e8-3229">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3229">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3230">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3230">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3231">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="a18e8-3231">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a18e8-3232">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3232">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-3233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3233">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3234">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3234">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a18e8-3235">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3235">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a18e8-3236">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="a18e8-3236">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-3237">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-3237">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-3238">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3238">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3239">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3239">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3240">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="a18e8-3240">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-3241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-3241">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-3242">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-3242">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-3243">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-3243">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-3244">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3244">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3245">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3245">Az.Network</span></span>
* <span data-ttu-id="a18e8-3246">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3246">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3247">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-3248">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3248">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a18e8-3249">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="a18e8-3249">SDK Update</span></span>
* <span data-ttu-id="a18e8-3250">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a18e8-3250">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a18e8-3251">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a18e8-3251">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3252">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3252">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3253">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="a18e8-3253">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a18e8-3254">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a18e8-3254">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a18e8-3255">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3255">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a18e8-3256">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a18e8-3256">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a18e8-3257">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3257">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a18e8-3258">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a18e8-3258">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3259">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3260">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3260">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a18e8-3261">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3261">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3262">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3263">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3263">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a18e8-3264">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3264">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-3265">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3265">Az.AnalysisServices</span></span>
* <span data-ttu-id="a18e8-3266">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3266">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-3267">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3267">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3268">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3268">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a18e8-3269">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3269">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a18e8-3270">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3270">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-3271">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3271">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-3272">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3272">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3273">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3273">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3274">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="a18e8-3274">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a18e8-3275">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="a18e8-3275">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a18e8-3276">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3276">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a18e8-3277">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3277">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3278">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3278">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3279">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3279">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a18e8-3280">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3280">Az.EventHub</span></span>
* <span data-ttu-id="a18e8-3281">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3281">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-3282">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3282">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-3283">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a18e8-3283">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-3284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-3284">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-3285">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="a18e8-3285">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a18e8-3286">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="a18e8-3286">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a18e8-3287">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="a18e8-3287">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a18e8-3288">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a18e8-3288">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a18e8-3289">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a18e8-3289">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a18e8-3290">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a18e8-3290">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a18e8-3291">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a18e8-3291">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a18e8-3292">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="a18e8-3292">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a18e8-3293">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3293">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a18e8-3294">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3294">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a18e8-3295">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3295">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a18e8-3296">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3296">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a18e8-3297">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-3297">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a18e8-3298">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-3298">Az.Monitor</span></span>
* <span data-ttu-id="a18e8-3299">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a18e8-3299">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3300">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3300">Az.Network</span></span>
* <span data-ttu-id="a18e8-3301">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a18e8-3301">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-3302">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3302">Az.OperationalInsights</span></span>
* <span data-ttu-id="a18e8-3303">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3303">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a18e8-3304">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3304">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="a18e8-3305">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3305">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3306">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3306">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3307">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a18e8-3307">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a18e8-3308">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a18e8-3308">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a18e8-3309">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a18e8-3309">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a18e8-3310">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a18e8-3310">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3311">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3312">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-3312">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a18e8-3313">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="a18e8-3313">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3314">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3315">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a18e8-3315">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a18e8-3316">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3316">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3317">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3318">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a18e8-3318">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-3319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3319">Az.AnalysisServices</span></span>
<span data-ttu-id="a18e8-3320">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3320">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3321">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3321">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3322">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="a18e8-3322">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a18e8-3323">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a18e8-3323">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a18e8-3324">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3324">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3325">Az.RecoveryServices</span></span>
<span data-ttu-id="a18e8-3326">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3326">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3327">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3328">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3328">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="a18e8-3329">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a18e8-3329">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a18e8-3330">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a18e8-3330">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="a18e8-3331">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a18e8-3331">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3332">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3332">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3333">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3333">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a18e8-3334">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-3334">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a18e8-3335">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a18e8-3335">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a18e8-3336">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3336">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3337">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3337">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3338">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="a18e8-3338">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a18e8-3339">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3339">Az.AnalysisServices</span></span>
* <span data-ttu-id="a18e8-3340">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-3340">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3341">Az.RecoveryServices</span></span>
* <span data-ttu-id="a18e8-3342">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-3342">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a18e8-3343">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3343">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3344">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3345">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a18e8-3345">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a18e8-3346">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3346">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a18e8-3347">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a18e8-3347">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a18e8-3348">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a18e8-3348">Az.Aks</span></span>
* <span data-ttu-id="a18e8-3349">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3349">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a18e8-3350">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3350">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3351">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3351">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a18e8-3352">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3352">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a18e8-3353">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a18e8-3353">Az.Cdn</span></span>
* <span data-ttu-id="a18e8-3354">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3354">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3355">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3355">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3356">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3356">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a18e8-3357">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a18e8-3357">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a18e8-3358">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a18e8-3358">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a18e8-3359">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a18e8-3359">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a18e8-3360">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3360">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a18e8-3361">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a18e8-3361">Az.DataFactory</span></span>
* <span data-ttu-id="a18e8-3362">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a18e8-3362">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3363">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3363">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3364">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="a18e8-3364">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a18e8-3365">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a18e8-3365">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a18e8-3366">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3366">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-3367">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3367">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-3368">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3368">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a18e8-3369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3369">Az.KeyVault</span></span>
* <span data-ttu-id="a18e8-3370">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3370">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3371">Az.Network</span></span>
* <span data-ttu-id="a18e8-3372">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3372">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3373">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3373">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3374">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3374">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a18e8-3375">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3375">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a18e8-3376">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="a18e8-3376">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a18e8-3377">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a18e8-3377">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a18e8-3378">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a18e8-3378">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a18e8-3379">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3379">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a18e8-3380">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a18e8-3380">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-3381">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-3381">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-3382">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a18e8-3382">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a18e8-3383">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3383">Fix some error messages.</span></span>
* <span data-ttu-id="a18e8-3384">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3384">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a18e8-3385">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3385">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a18e8-3386">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-3386">Az.SignalR</span></span>
* <span data-ttu-id="a18e8-3387">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3387">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3388">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3389">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3389">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a18e8-3390">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a18e8-3390">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a18e8-3391">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="a18e8-3391">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a18e8-3392">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="a18e8-3392">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3393">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3394">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3394">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a18e8-3395">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3395">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a18e8-3396">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a18e8-3396">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a18e8-3397">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a18e8-3397">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a18e8-3398">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a18e8-3398">Az.TrafficManager</span></span>
* <span data-ttu-id="a18e8-3399">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3399">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3400">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3401">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="a18e8-3401">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a18e8-3402">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3402">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a18e8-3403">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3403">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a18e8-3404">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="a18e8-3404">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a18e8-3405">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3405">Az.Accounts</span></span>
* <span data-ttu-id="a18e8-3406">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a18e8-3406">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3407">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3408">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3408">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a18e8-3409">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="a18e8-3409">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a18e8-3410">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3410">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3411">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3411">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3412">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3412">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a18e8-3413">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="a18e8-3413">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a18e8-3414">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a18e8-3414">Az.EventGrid</span></span>
* <span data-ttu-id="a18e8-3415">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3415">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a18e8-3416">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a18e8-3416">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a18e8-3417">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3417">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a18e8-3418">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="a18e8-3418">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a18e8-3419">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3419">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a18e8-3420">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="a18e8-3420">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a18e8-3421">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3421">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a18e8-3422">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="a18e8-3422">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a18e8-3423">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3423">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a18e8-3424">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="a18e8-3424">Dead letter endpoint.</span></span>
* <span data-ttu-id="a18e8-3425">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3425">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a18e8-3426">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3426">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a18e8-3427">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3427">Az.IotHub</span></span>
* <span data-ttu-id="a18e8-3428">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="a18e8-3428">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a18e8-3429">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a18e8-3429">Az.LogicApp</span></span>
* <span data-ttu-id="a18e8-3430">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="a18e8-3430">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3431">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3431">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3432">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3432">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a18e8-3433">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a18e8-3433">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a18e8-3434">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a18e8-3434">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a18e8-3435">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a18e8-3435">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a18e8-3436">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3436">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a18e8-3437">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a18e8-3437">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a18e8-3438">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-3438">Az.SignalR</span></span>
* <span data-ttu-id="a18e8-3439">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3439">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3440">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3441">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3441">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a18e8-3442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3442">Az.Storage</span></span>
* <span data-ttu-id="a18e8-3443">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="a18e8-3443">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a18e8-3444">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a18e8-3444">New-AzStorageContext</span></span>
* <span data-ttu-id="a18e8-3445">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3445">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a18e8-3446">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a18e8-3446">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3447">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3448">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="a18e8-3448">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a18e8-3449">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3449">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a18e8-3450">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3450">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a18e8-3451">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-3451">General</span></span>

- <span data-ttu-id="a18e8-3452">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="a18e8-3452">General Availability of Az Module</span></span>
- <span data-ttu-id="a18e8-3453">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3453">Online help for each module</span></span>
- <span data-ttu-id="a18e8-3454">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a18e8-3454">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a18e8-3455">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="a18e8-3455">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a18e8-3456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3456">Az.Accounts</span></span>
- <span data-ttu-id="a18e8-3457">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3457">Changed from Az.Profile</span></span>
- <span data-ttu-id="a18e8-3458">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="a18e8-3458">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a18e8-3459">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-3459">Az.ApiManagement</span></span>
- <span data-ttu-id="a18e8-3460">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="a18e8-3460">Fixes for #7002</span></span>
- <span data-ttu-id="a18e8-3461">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3461">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a18e8-3462">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a18e8-3462">Az.Batch</span></span>
- <span data-ttu-id="a18e8-3463">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3463">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a18e8-3464">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3464">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a18e8-3465">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3465">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a18e8-3466">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a18e8-3466">Az.Billing</span></span>
- <span data-ttu-id="a18e8-3467">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3467">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a18e8-3468">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3468">Az.CognitivServices</span></span>
- <span data-ttu-id="a18e8-3469">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3469">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a18e8-3470">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a18e8-3470">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a18e8-3471">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3471">Az.ContainerInstance</span></span>
- <span data-ttu-id="a18e8-3472">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a18e8-3472">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a18e8-3473">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a18e8-3473">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a18e8-3474">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3475">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3475">Az.DataLakeStore</span></span>
- <span data-ttu-id="a18e8-3476">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a18e8-3477">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a18e8-3477">Az.Monitor</span></span>
- <span data-ttu-id="a18e8-3478">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3478">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a18e8-3479">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a18e8-3479">Az.KeyVault</span></span>
- <span data-ttu-id="a18e8-3480">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="a18e8-3480">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a18e8-3481">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a18e8-3481">Az.MachineLearning</span></span>
- <span data-ttu-id="a18e8-3482">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3482">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a18e8-3483">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a18e8-3483">Az.Media</span></span>
- <span data-ttu-id="a18e8-3484">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a18e8-3484">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a18e8-3485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3485">Az.Network</span></span>
<span data-ttu-id="a18e8-3486">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3486">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a18e8-3487">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="a18e8-3487">New cmdlets added:</span></span>
        - <span data-ttu-id="a18e8-3488">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3488">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3489">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3489">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3490">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3490">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3491">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3491">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3492">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3492">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3493">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3493">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a18e8-3494">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3494">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a18e8-3495">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a18e8-3495">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a18e8-3496">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3496">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a18e8-3497">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a18e8-3497">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a18e8-3498">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3498">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a18e8-3499">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a18e8-3499">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a18e8-3500">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3500">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a18e8-3501">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3501">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a18e8-3502">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3502">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a18e8-3503">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a18e8-3503">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a18e8-3504">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a18e8-3504">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a18e8-3505">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a18e8-3505">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a18e8-3506">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a18e8-3506">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a18e8-3507">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a18e8-3507">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a18e8-3508">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3508">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a18e8-3509">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3509">Az.OperationalInsights</span></span>
- <span data-ttu-id="a18e8-3510">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3510">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a18e8-3511">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3511">Az.Profile</span></span>
- <span data-ttu-id="a18e8-3512">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a18e8-3512">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3513">Az.RecoveryServices</span></span>
- <span data-ttu-id="a18e8-3514">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3514">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a18e8-3515">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3515">Az.Resources</span></span>
- <span data-ttu-id="a18e8-3516">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a18e8-3517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-3517">Az.ServiceFabric</span></span>
- <span data-ttu-id="a18e8-3518">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="a18e8-3518">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a18e8-3519">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3519">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a18e8-3520">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-3520">Az.SIgnalR</span></span>
- <span data-ttu-id="a18e8-3521">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a18e8-3521">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a18e8-3522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3522">Az.Sql</span></span>
- <span data-ttu-id="a18e8-3523">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="a18e8-3523">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a18e8-3524">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="a18e8-3524">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a18e8-3525">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3525">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a18e8-3526">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3526">Az.Storage</span></span>
- <span data-ttu-id="a18e8-3527">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3527">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a18e8-3528">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3528">Az.Websites</span></span>
- <span data-ttu-id="a18e8-3529">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="a18e8-3529">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a18e8-3530">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3530">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a18e8-3531">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-3531">General</span></span>

* <span data-ttu-id="a18e8-3532">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="a18e8-3532">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a18e8-3533">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3533">Az.Compute</span></span>

* <span data-ttu-id="a18e8-3534">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3534">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3535">Az.DataLakeStore</span></span>

* <span data-ttu-id="a18e8-3536">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="a18e8-3536">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a18e8-3537">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a18e8-3537">Az.FrontDoor</span></span>

* <span data-ttu-id="a18e8-3538">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="a18e8-3538">Fixed some broken links</span></span>
    - <span data-ttu-id="a18e8-3539">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3539">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a18e8-3540">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3540">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a18e8-3541">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3541">Az.RecoveryServices</span></span>

* <span data-ttu-id="a18e8-3542">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3542">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a18e8-3543">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3543">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a18e8-3544">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3544">Az.Resources</span></span>

* <span data-ttu-id="a18e8-3545">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a18e8-3545">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a18e8-3546">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3546">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a18e8-3547">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3547">Az.Sql</span></span>

* <span data-ttu-id="a18e8-3548">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="a18e8-3548">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a18e8-3549">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="a18e8-3549">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a18e8-3550">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3550">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a18e8-3551">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3551">Az.Storage</span></span>

* <span data-ttu-id="a18e8-3552">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3552">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a18e8-3553">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="a18e8-3553">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a18e8-3554">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3554">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a18e8-3555">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="a18e8-3555">Support Static Website configuration</span></span>
    - <span data-ttu-id="a18e8-3556">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a18e8-3556">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a18e8-3557">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a18e8-3557">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a18e8-3558">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3558">Az.Websites</span></span>

* <span data-ttu-id="a18e8-3559">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a18e8-3559">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="a18e8-3560">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3560">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a18e8-3561">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3561">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a18e8-3562">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3562">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a18e8-3563">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a18e8-3563">Az.ApiManagement</span></span>
* <span data-ttu-id="a18e8-3564">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3564">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a18e8-3565">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a18e8-3565">Az.Automation</span></span>
* <span data-ttu-id="a18e8-3566">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="a18e8-3566">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a18e8-3567">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3567">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a18e8-3568">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3568">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a18e8-3569">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="a18e8-3569">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a18e8-3570">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="a18e8-3570">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a18e8-3571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3571">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3572">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a18e8-3572">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a18e8-3573">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3573">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a18e8-3574">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3574">Az.ContainerInstance</span></span>
* <span data-ttu-id="a18e8-3575">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3575">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a18e8-3576">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a18e8-3576">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a18e8-3577">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="a18e8-3577">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a18e8-3578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3578">Az.Network</span></span>
* <span data-ttu-id="a18e8-3579">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3579">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a18e8-3580">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="a18e8-3580">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a18e8-3581">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3581">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="a18e8-3582">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a18e8-3582">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a18e8-3583">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a18e8-3583">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a18e8-3584">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3584">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a18e8-3585">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3585">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a18e8-3586">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a18e8-3586">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a18e8-3587">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a18e8-3587">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a18e8-3588">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="a18e8-3588">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a18e8-3589">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a18e8-3589">Az.Relay</span></span>
* <span data-ttu-id="a18e8-3590">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3590">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a18e8-3591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3591">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3592">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a18e8-3592">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a18e8-3593">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="a18e8-3593">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a18e8-3594">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a18e8-3594">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a18e8-3595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-3595">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-3596">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="a18e8-3596">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a18e8-3597">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3597">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3598">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="a18e8-3598">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a18e8-3599">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3599">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a18e8-3600">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3600">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a18e8-3601">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3601">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a18e8-3602">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a18e8-3602">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a18e8-3603">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a18e8-3603">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a18e8-3604">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a18e8-3604">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a18e8-3605">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a18e8-3605">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a18e8-3606">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a18e8-3606">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a18e8-3607">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3607">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a18e8-3608">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3608">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a18e8-3609">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3609">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a18e8-3610">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3610">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a18e8-3611">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3611">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a18e8-3612">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3612">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a18e8-3613">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3613">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a18e8-3614">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a18e8-3614">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a18e8-3615">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3615">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a18e8-3616">Geral</span><span class="sxs-lookup"><span data-stu-id="a18e8-3616">General</span></span>
* <span data-ttu-id="a18e8-3617">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="a18e8-3617">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a18e8-3618">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3618">Az.Profile</span></span>
* <span data-ttu-id="a18e8-3619">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a18e8-3619">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a18e8-3620">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="a18e8-3620">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a18e8-3621">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a18e8-3621">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a18e8-3622">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="a18e8-3622">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a18e8-3623">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="a18e8-3623">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a18e8-3624">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="a18e8-3624">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a18e8-3625">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="a18e8-3625">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-3626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3626">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-3627">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3627">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3628">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3629">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a18e8-3629">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a18e8-3630">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a18e8-3630">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a18e8-3631">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3631">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3632">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3632">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3633">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3633">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a18e8-3634">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3634">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a18e8-3635">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3635">Az.Insights</span></span>
* <span data-ttu-id="a18e8-3636">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="a18e8-3636">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a18e8-3637">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="a18e8-3637">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a18e8-3638">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="a18e8-3638">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a18e8-3639">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="a18e8-3639">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3640">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3640">Az.Network</span></span>
* <span data-ttu-id="a18e8-3641">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="a18e8-3641">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a18e8-3642">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-3642">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a18e8-3643">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-3643">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a18e8-3644">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a18e8-3644">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a18e8-3645">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-3645">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a18e8-3646">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a18e8-3646">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a18e8-3647">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a18e8-3647">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a18e8-3648">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a18e8-3648">Az.PolicyInsights</span></span>
* <span data-ttu-id="a18e8-3649">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="a18e8-3649">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3650">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3650">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3651">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a18e8-3651">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a18e8-3652">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="a18e8-3652">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a18e8-3653">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a18e8-3653">Az.ServiceBus</span></span>
* <span data-ttu-id="a18e8-3654">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3654">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a18e8-3655">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a18e8-3655">Az.ServiceFabric</span></span>
* <span data-ttu-id="a18e8-3656">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3656">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a18e8-3657">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="a18e8-3657">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a18e8-3658">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a18e8-3658">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a18e8-3659">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a18e8-3659">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a18e8-3660">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3660">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a18e8-3661">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3661">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a18e8-3662">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3662">Az.Profile</span></span>
* <span data-ttu-id="a18e8-3663">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="a18e8-3663">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a18e8-3664">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a18e8-3664">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3665">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3666">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="a18e8-3666">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a18e8-3667">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3667">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a18e8-3668">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a18e8-3668">Az.DataLakeStore</span></span>
* <span data-ttu-id="a18e8-3669">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="a18e8-3669">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a18e8-3670">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3670">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a18e8-3671">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3671">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a18e8-3672">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3672">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a18e8-3673">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3673">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3674">Az.Network</span></span>
* <span data-ttu-id="a18e8-3675">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3675">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a18e8-3676">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3676">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3677">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3678">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3678">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a18e8-3679">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3679">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a18e8-3680">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3680">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a18e8-3681">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3681">Azure.Storage</span></span>
* <span data-ttu-id="a18e8-3682">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3682">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a18e8-3683">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3683">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a18e8-3684">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a18e8-3684">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a18e8-3685">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3685">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a18e8-3686">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a18e8-3686">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a18e8-3687">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a18e8-3687">Az.CognitiveServices</span></span>
* <span data-ttu-id="a18e8-3688">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3688">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a18e8-3689">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a18e8-3689">Az.Compute</span></span>
* <span data-ttu-id="a18e8-3690">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="a18e8-3690">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a18e8-3691">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3691">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a18e8-3692">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="a18e8-3692">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a18e8-3693">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a18e8-3693">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a18e8-3694">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3694">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a18e8-3695">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a18e8-3695">Az.Network</span></span>
* <span data-ttu-id="a18e8-3696">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3696">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a18e8-3697">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="a18e8-3697">new cmdlets added</span></span>
    - <span data-ttu-id="a18e8-3698">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3698">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a18e8-3699">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3699">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a18e8-3700">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3700">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a18e8-3701">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a18e8-3701">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a18e8-3702">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3702">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a18e8-3703">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3703">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a18e8-3704">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="a18e8-3704">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a18e8-3705">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a18e8-3705">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a18e8-3706">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a18e8-3706">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a18e8-3707">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a18e8-3707">Az.RedisCache</span></span>
* <span data-ttu-id="a18e8-3708">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="a18e8-3708">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a18e8-3709">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a18e8-3709">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a18e8-3710">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a18e8-3710">Az.Resources</span></span>
* <span data-ttu-id="a18e8-3711">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a18e8-3711">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a18e8-3712">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="a18e8-3712">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a18e8-3713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a18e8-3713">Az.Sql</span></span>
* <span data-ttu-id="a18e8-3714">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="a18e8-3714">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a18e8-3715">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a18e8-3715">Az.Websites</span></span>
* <span data-ttu-id="a18e8-3716">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="a18e8-3716">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a18e8-3717">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="a18e8-3717">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a18e8-3718">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="a18e8-3718">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a18e8-3719">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="a18e8-3719">Initial Release</span></span>
