---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740534"
---
## <a name="380---april-2020"></a><span data-ttu-id="893b4-103">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-104">Az.Accounts</span></span>
* <span data-ttu-id="893b4-105">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="893b4-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-106">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-107">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="893b4-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="893b4-108">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="893b4-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-109">Az.Cdn</span></span>
* <span data-ttu-id="893b4-110">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="893b4-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-112">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="893b4-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="893b4-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-113">Az.Compute</span></span>
* <span data-ttu-id="893b4-114">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="893b4-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="893b4-115">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="893b4-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-116">Az.IotHub</span></span>
* <span data-ttu-id="893b4-117">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="893b4-118">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="893b4-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="893b4-119">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="893b4-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="893b4-120">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="893b4-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="893b4-121">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="893b4-122">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="893b4-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="893b4-123">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="893b4-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="893b4-124">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="893b4-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="893b4-125">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-125">New cmdlets are:</span></span>
    - <span data-ttu-id="893b4-126">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="893b4-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="893b4-127">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="893b4-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="893b4-128">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="893b4-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="893b4-129">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="893b4-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="893b4-130">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="893b4-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-131">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-132">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="893b4-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="893b4-133">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="893b4-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="893b4-134">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="893b4-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="893b4-135">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="893b4-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="893b4-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="893b4-136">Az.Maintenance</span></span>
* <span data-ttu-id="893b4-137">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="893b4-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-138">Az.Monitor</span></span>
* <span data-ttu-id="893b4-139">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="893b4-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="893b4-140">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="893b4-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="893b4-141">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="893b4-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="893b4-142">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="893b4-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="893b4-143">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="893b4-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="893b4-144">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="893b4-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="893b4-145">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="893b4-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="893b4-146">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="893b4-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-147">Az.Network</span></span>
* <span data-ttu-id="893b4-148">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="893b4-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="893b4-149">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="893b4-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="893b4-150">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="893b4-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="893b4-151">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="893b4-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="893b4-152">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="893b4-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="893b4-153">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="893b4-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="893b4-154">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="893b4-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="893b4-155">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="893b4-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="893b4-156">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="893b4-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="893b4-157">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="893b4-158">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="893b4-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="893b4-159">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="893b4-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="893b4-160">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="893b4-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="893b4-161">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="893b4-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="893b4-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="893b4-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-165">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="893b4-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="893b4-166">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="893b4-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-168">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="893b4-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-169">Az.Sql</span></span>
* <span data-ttu-id="893b4-170">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="893b4-171">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="893b4-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-172">Az.Storage</span></span>
* <span data-ttu-id="893b4-173">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="893b4-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="893b4-174">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="893b4-175">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="893b4-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="893b4-176">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="893b4-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="893b4-177">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="893b4-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="893b4-178">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="893b4-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="893b4-179">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="893b4-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="893b4-180">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="893b4-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="893b4-181">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="893b4-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="893b4-182">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="893b4-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="893b4-183">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="893b4-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="893b4-184">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="893b4-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="893b4-185">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="893b4-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="893b4-186">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="893b4-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="893b4-187">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-188">Az.Accounts</span></span>
* <span data-ttu-id="893b4-189">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="893b4-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-190">Az.Compute</span></span>
* <span data-ttu-id="893b4-191">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="893b4-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="893b4-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="893b4-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="893b4-193">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="893b4-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="893b4-194">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="893b4-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="893b4-195">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="893b4-195">[#11354]</span></span>
* <span data-ttu-id="893b4-196">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="893b4-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="893b4-197">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="893b4-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="893b4-198">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="893b4-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="893b4-199">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="893b4-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="893b4-200">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="893b4-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="893b4-201">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="893b4-202">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="893b4-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="893b4-203">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="893b4-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="893b4-204">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="893b4-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-205">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-206">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="893b4-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="893b4-207">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="893b4-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-209">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="893b4-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="893b4-210">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="893b4-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-211">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-212">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="893b4-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-213">Az.IotHub</span></span>
* <span data-ttu-id="893b4-214">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="893b4-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="893b4-215">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="893b4-216">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="893b4-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="893b4-217">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="893b4-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-218">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-219">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="893b4-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-220">Az.Monitor</span></span>
* <span data-ttu-id="893b4-221">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="893b4-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-222">Az.Network</span></span>
* <span data-ttu-id="893b4-223">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="893b4-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="893b4-224">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="893b4-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="893b4-225">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="893b4-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="893b4-226">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="893b4-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="893b4-227">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="893b4-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="893b4-228">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="893b4-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-230">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="893b4-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-232">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="893b4-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="893b4-233">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="893b4-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="893b4-234">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="893b4-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="893b4-235">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="893b4-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="893b4-236">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="893b4-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="893b4-237">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="893b4-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-238">Az.Resources</span></span>
* <span data-ttu-id="893b4-239">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="893b4-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="893b4-240">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="893b4-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="893b4-241">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="893b4-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="893b4-242">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="893b4-242">Added example.</span></span>
* <span data-ttu-id="893b4-243">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="893b4-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="893b4-244">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="893b4-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-245">Az.Sql</span></span>
* <span data-ttu-id="893b4-246">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="893b4-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="893b4-247">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="893b4-248">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="893b4-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="893b4-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="893b4-249">Az.Support</span></span>
* <span data-ttu-id="893b4-250">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="893b4-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-251">Az.Websites</span></span>
* <span data-ttu-id="893b4-252">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="893b4-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="893b4-253">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="893b4-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="893b4-254">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="893b4-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="893b4-255">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="893b4-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="893b4-256">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="893b4-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="893b4-257">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-258">Az.Accounts</span></span>
* <span data-ttu-id="893b4-259">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="893b4-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="893b4-260">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="893b4-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="893b4-261">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="893b4-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-262">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-263">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="893b4-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="893b4-264">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="893b4-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="893b4-265">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="893b4-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="893b4-266">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="893b4-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-268">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="893b4-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-269">Az.IotHub</span></span>
* <span data-ttu-id="893b4-270">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="893b4-271">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="893b4-272">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-273">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-274">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-275">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="893b4-276">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="893b4-277">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="893b4-278">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="893b4-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="893b4-279">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="893b4-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="893b4-280">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="893b4-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="893b4-281">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="893b4-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="893b4-282">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="893b4-283">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="893b4-284">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="893b4-285">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="893b4-286">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="893b4-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="893b4-287">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="893b4-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="893b4-288">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="893b4-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-289">Az.Monitor</span></span>
* <span data-ttu-id="893b4-290">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="893b4-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-291">Az.Network</span></span>
* <span data-ttu-id="893b4-292">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="893b4-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="893b4-293">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="893b4-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="893b4-294">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="893b4-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="893b4-295">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="893b4-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-296">Az.Resources</span></span>
* <span data-ttu-id="893b4-297">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="893b4-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="893b4-298">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="893b4-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="893b4-299">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="893b4-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="893b4-300">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="893b4-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="893b4-301">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="893b4-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="893b4-302">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="893b4-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="893b4-303">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="893b4-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="893b4-304">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="893b4-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="893b4-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="893b4-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="893b4-308">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="893b4-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="893b4-310">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="893b4-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-311">Az.Sql</span></span>
* <span data-ttu-id="893b4-312">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="893b4-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="893b4-313">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="893b4-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="893b4-314">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="893b4-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="893b4-315">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="893b4-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="893b4-316">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="893b4-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="893b4-317">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="893b4-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="893b4-318">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="893b4-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="893b4-319">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="893b4-320">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-321">Az.Storage</span></span>
* <span data-ttu-id="893b4-322">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="893b4-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="893b4-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="893b4-324">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="893b4-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="893b4-325">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="893b4-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="893b4-326">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="893b4-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-327">Az.Websites</span></span>
* <span data-ttu-id="893b4-328">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="893b4-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="893b4-329">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="893b4-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="893b4-330">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="893b4-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="893b4-331">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="893b4-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="893b4-332">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="893b4-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="893b4-333">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-334">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-334">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-335">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="893b4-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="893b4-336">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="893b4-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="893b4-337">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="893b4-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-338">Az.Accounts</span></span>
* <span data-ttu-id="893b4-339">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="893b4-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-340">Az.Automation</span></span>
* <span data-ttu-id="893b4-341">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="893b4-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-343">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="893b4-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="893b4-344">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="893b4-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-345">Az.Compute</span></span>
* <span data-ttu-id="893b4-346">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="893b4-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-347">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-348">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="893b4-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-349">Az.IotHub</span></span>
* <span data-ttu-id="893b4-350">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="893b4-351">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="893b4-352">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-353">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-354">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="893b4-355">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="893b4-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-356">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-357">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="893b4-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-358">Az.Monitor</span></span>
* <span data-ttu-id="893b4-359">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="893b4-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="893b4-360">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="893b4-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="893b4-361">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="893b4-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-362">Az.Network</span></span>
* <span data-ttu-id="893b4-363">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="893b4-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="893b4-364">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="893b4-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="893b4-365">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="893b4-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="893b4-366">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="893b4-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="893b4-367">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="893b4-367">No new cmdlets are added.</span></span> <span data-ttu-id="893b4-368">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="893b4-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-370">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="893b4-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-371">Az.Resources</span></span>
* <span data-ttu-id="893b4-372">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="893b4-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="893b4-373">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="893b4-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="893b4-374">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="893b4-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="893b4-375">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="893b4-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="893b4-376">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="893b4-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="893b4-377">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="893b4-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="893b4-378">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="893b4-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="893b4-379">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-380">Az.Sql</span></span>
* <span data-ttu-id="893b4-381">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="893b4-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="893b4-382">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="893b4-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="893b4-383">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="893b4-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="893b4-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="893b4-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="893b4-385">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="893b4-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="893b4-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="893b4-386">Az.StorageSync</span></span>
* <span data-ttu-id="893b4-387">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="893b4-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="893b4-388">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-389">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-389">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-390">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="893b4-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="893b4-391">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-392">Az.Accounts</span></span>
* <span data-ttu-id="893b4-393">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="893b4-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="893b4-394">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="893b4-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-395">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-396">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="893b4-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="893b4-397">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="893b4-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="893b4-398">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="893b4-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="893b4-399">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="893b4-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-400">Az.Compute</span></span>
* <span data-ttu-id="893b4-401">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="893b4-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="893b4-402">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="893b4-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="893b4-403">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="893b4-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="893b4-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="893b4-405">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="893b4-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-406">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-407">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="893b4-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="893b4-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="893b4-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="893b4-409">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="893b4-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="893b4-410">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="893b4-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-411">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-412">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="893b4-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-413">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-414">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="893b4-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-415">Az.Network</span></span>
* <span data-ttu-id="893b4-416">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="893b4-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="893b4-417">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="893b4-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="893b4-418">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="893b4-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="893b4-419">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="893b4-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="893b4-420">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="893b4-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="893b4-421">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="893b4-422">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="893b4-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="893b4-423">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="893b4-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="893b4-424">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-424">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="893b4-426">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="893b4-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="893b4-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="893b4-428">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="893b4-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-430">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="893b4-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="893b4-431">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="893b4-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="893b4-432">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="893b4-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="893b4-433">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="893b4-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-435">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="893b4-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="893b4-436">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="893b4-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-437">Az.Resources</span></span>
* <span data-ttu-id="893b4-438">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="893b4-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="893b4-439">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="893b4-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-440">Az.Sql</span></span>
<span data-ttu-id="893b4-441">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="893b4-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-442">Az.Storage</span></span>
* <span data-ttu-id="893b4-443">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="893b4-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="893b4-445">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="893b4-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="893b4-446">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-447">Az.Websites</span></span>
* <span data-ttu-id="893b4-448">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="893b4-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="893b4-449">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="893b4-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="893b4-450">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="893b4-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-451">Az.Accounts</span></span>
* <span data-ttu-id="893b4-452">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="893b4-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-453">Az.Cdn</span></span>
* <span data-ttu-id="893b4-454">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-455">Az.Compute</span></span>
* <span data-ttu-id="893b4-456">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="893b4-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="893b4-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="893b4-458">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="893b4-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="893b4-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="893b4-460">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="893b4-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="893b4-461">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="893b4-462">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="893b4-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="893b4-463">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="893b4-464">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="893b4-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="893b4-465">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="893b4-466">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="893b4-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="893b4-467">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="893b4-468">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="893b4-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="893b4-469">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="893b4-470">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="893b4-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="893b4-471">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="893b4-472">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="893b4-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="893b4-473">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="893b4-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="893b4-474">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="893b4-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="893b4-475">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="893b4-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="893b4-476">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="893b4-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="893b4-477">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="893b4-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-478">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-479">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="893b4-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="893b4-480">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="893b4-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="893b4-481">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="893b4-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="893b4-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="893b4-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="893b4-483">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="893b4-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-484">Az.EventHub</span></span>
* <span data-ttu-id="893b4-485">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="893b4-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-486">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-487">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="893b4-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="893b4-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="893b4-488">Az.MachineLearning</span></span>
* <span data-ttu-id="893b4-489">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="893b4-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="893b4-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="893b4-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="893b4-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="893b4-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="893b4-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="893b4-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="893b4-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="893b4-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="893b4-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="893b4-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="893b4-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="893b4-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="893b4-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="893b4-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-497">Az.Network</span></span>
* <span data-ttu-id="893b4-498">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="893b4-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-500">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="893b4-501">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="893b4-502">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="893b4-503">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-504">Az.Resources</span></span>
* <span data-ttu-id="893b4-505">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="893b4-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-506">Az.Sql</span></span>
* <span data-ttu-id="893b4-507">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="893b4-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="893b4-508">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="893b4-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="893b4-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="893b4-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="893b4-510">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="893b4-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-511">Az.Storage</span></span>
* <span data-ttu-id="893b4-512">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="893b4-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="893b4-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="893b4-514">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="893b4-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="893b4-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="893b4-516">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="893b4-517">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-517">General</span></span>
* <span data-ttu-id="893b4-518">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="893b4-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-519">Az.Accounts</span></span>
* <span data-ttu-id="893b4-520">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="893b4-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="893b4-521">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="893b4-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="893b4-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-522">Az.Batch</span></span>
* <span data-ttu-id="893b4-523">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="893b4-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-524">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-525">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="893b4-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-526">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-527">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="893b4-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="893b4-528">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="893b4-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="893b4-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="893b4-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="893b4-530">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="893b4-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-531">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-532">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="893b4-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="893b4-533">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="893b4-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="893b4-534">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="893b4-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-535">Az.Monitor</span></span>
* <span data-ttu-id="893b4-536">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="893b4-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="893b4-537">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="893b4-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="893b4-538">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="893b4-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-539">Az.Network</span></span>
* <span data-ttu-id="893b4-540">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-541">Az.Resources</span></span>
* <span data-ttu-id="893b4-542">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="893b4-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="893b4-543">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="893b4-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-544">Az.Sql</span></span>
* <span data-ttu-id="893b4-545">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="893b4-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-546">Az.Storage</span></span>
* <span data-ttu-id="893b4-547">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="893b4-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="893b4-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="893b4-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="893b4-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="893b4-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="893b4-550">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="893b4-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="893b4-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="893b4-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="893b4-552">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="893b4-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="893b4-553">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="893b4-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="893b4-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="893b4-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="893b4-556">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="893b4-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="893b4-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="893b4-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="893b4-558">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="893b4-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="893b4-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="893b4-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="893b4-560">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-561">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-561">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-562">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="893b4-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="893b4-563">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="893b4-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-564">Az.Compute</span></span>
* <span data-ttu-id="893b4-565">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="893b4-565">VM Reapply feature</span></span>
    - <span data-ttu-id="893b4-566">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="893b4-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="893b4-567">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="893b4-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="893b4-568">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="893b4-569">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="893b4-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="893b4-570">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="893b4-571">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="893b4-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="893b4-572">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="893b4-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="893b4-573">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="893b4-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="893b4-574">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="893b4-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="893b4-575">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="893b4-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="893b4-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="893b4-577">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="893b4-578">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="893b4-578">Get the Order</span></span>
* <span data-ttu-id="893b4-579">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="893b4-580">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="893b4-580">Create new Order</span></span>
* <span data-ttu-id="893b4-581">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="893b4-582">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="893b4-582">Remove the Order</span></span>
* <span data-ttu-id="893b4-583">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="893b4-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="893b4-584">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="893b4-584">Now creates Local Share</span></span>
* <span data-ttu-id="893b4-585">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="893b4-586">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="893b4-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="893b4-587">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="893b4-588">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="893b4-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="893b4-589">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="893b4-590">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="893b4-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="893b4-591">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="893b4-592">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="893b4-592">Create new Triggers</span></span>
* <span data-ttu-id="893b4-593">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="893b4-594">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="893b4-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-595">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-596">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="893b4-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="893b4-597">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="893b4-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-599">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="893b4-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-600">Az.EventHub</span></span>
* <span data-ttu-id="893b4-601">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="893b4-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-602">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-603">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="893b4-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="893b4-604">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="893b4-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="893b4-605">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="893b4-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="893b4-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="893b4-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-607">Az.Network</span></span>
* <span data-ttu-id="893b4-608">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="893b4-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="893b4-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="893b4-609">Az.PrivateDns</span></span>
* <span data-ttu-id="893b4-610">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="893b4-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-612">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="893b4-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="893b4-613">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="893b4-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="893b4-614">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="893b4-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="893b4-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="893b4-615">Az.RedisCache</span></span>
* <span data-ttu-id="893b4-616">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="893b4-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="893b4-617">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="893b4-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="893b4-618">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="893b4-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-619">Az.Resources</span></span>
- <span data-ttu-id="893b4-620">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="893b4-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="893b4-621">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="893b4-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="893b4-622">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="893b4-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="893b4-623">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="893b4-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="893b4-624">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="893b4-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-625">Az.Sql</span></span>
* <span data-ttu-id="893b4-626">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="893b4-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="893b4-627">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="893b4-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="893b4-628">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="893b4-629">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-629">General</span></span>
* <span data-ttu-id="893b4-630">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="893b4-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-631">Az.Accounts</span></span>
* <span data-ttu-id="893b4-632">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="893b4-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="893b4-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="893b4-633">Az.Advisor</span></span>
* <span data-ttu-id="893b4-634">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="893b4-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="893b4-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-635">Az.Batch</span></span>
* <span data-ttu-id="893b4-636">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="893b4-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="893b4-637">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="893b4-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="893b4-638">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="893b4-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="893b4-639">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="893b4-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="893b4-640">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="893b4-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="893b4-641">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="893b4-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="893b4-642">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="893b4-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="893b4-643">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="893b4-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="893b4-644">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="893b4-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="893b4-645">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="893b4-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="893b4-646">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="893b4-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="893b4-647">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="893b4-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="893b4-648">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="893b4-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="893b4-649">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="893b4-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="893b4-650">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="893b4-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="893b4-651">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="893b4-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="893b4-652">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="893b4-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="893b4-653">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="893b4-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="893b4-654">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="893b4-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="893b4-655">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="893b4-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="893b4-656">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="893b4-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="893b4-657">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="893b4-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="893b4-658">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="893b4-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="893b4-659">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="893b4-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="893b4-660">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="893b4-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="893b4-661">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="893b4-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="893b4-662">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="893b4-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="893b4-663">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="893b4-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="893b4-664">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="893b4-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="893b4-665">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="893b4-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="893b4-666">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="893b4-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="893b4-667">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="893b4-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="893b4-668">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="893b4-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="893b4-669">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="893b4-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="893b4-670">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="893b4-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="893b4-671">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="893b4-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-672">Az.Cdn</span></span>
* <span data-ttu-id="893b4-673">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="893b4-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="893b4-674">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="893b4-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-675">Az.Compute</span></span>
* <span data-ttu-id="893b4-676">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="893b4-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="893b4-677">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="893b4-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="893b4-678">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="893b4-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="893b4-679">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="893b4-680">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="893b4-681">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="893b4-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="893b4-682">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="893b4-683">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="893b4-683">Breaking changes</span></span>
    - <span data-ttu-id="893b4-684">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="893b4-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="893b4-685">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="893b4-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-686">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-687">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="893b4-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-689">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="893b4-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="893b4-690">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="893b4-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="893b4-691">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="893b4-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="893b4-692">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="893b4-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="893b4-693">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="893b4-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="893b4-694">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="893b4-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-695">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-696">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="893b4-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-697">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-698">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="893b4-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="893b4-699">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="893b4-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="893b4-700">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="893b4-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="893b4-701">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="893b4-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="893b4-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="893b4-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="893b4-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="893b4-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="893b4-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="893b4-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="893b4-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="893b4-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="893b4-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="893b4-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="893b4-707">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="893b4-708">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="893b4-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="893b4-709">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="893b4-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="893b4-710">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="893b4-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="893b4-711">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="893b4-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="893b4-712">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="893b4-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="893b4-713">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="893b4-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="893b4-714">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="893b4-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="893b4-715">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="893b4-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="893b4-716">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="893b4-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="893b4-717">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="893b4-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="893b4-718">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="893b4-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="893b4-719">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="893b4-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-720">Az.IotHub</span></span>
* <span data-ttu-id="893b4-721">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="893b4-721">Breaking changes:</span></span>
    - <span data-ttu-id="893b4-722">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="893b4-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="893b4-723">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="893b4-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="893b4-724">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="893b4-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="893b4-725">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="893b4-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="893b4-726">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="893b4-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="893b4-727">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="893b4-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="893b4-728">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="893b4-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="893b4-729">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="893b4-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="893b4-730">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="893b4-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="893b4-731">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="893b4-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="893b4-732">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="893b4-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="893b4-733">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="893b4-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-735">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-736">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="893b4-737">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="893b4-738">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-739">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-740">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-741">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-742">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-743">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="893b4-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-744">Az.Resources</span></span>
* <span data-ttu-id="893b4-745">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="893b4-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-746">Az.Network</span></span>
* <span data-ttu-id="893b4-747">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="893b4-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="893b4-748">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="893b4-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="893b4-754">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="893b4-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="893b4-755">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-755">New cmdlet:</span></span>
        - <span data-ttu-id="893b4-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="893b4-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="893b4-757">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="893b4-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="893b4-758">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="893b4-759">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="893b4-760">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="893b4-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="893b4-761">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="893b4-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="893b4-762">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="893b4-763">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="893b4-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="893b4-764">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-764">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="893b4-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="893b4-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="893b4-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="893b4-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="893b4-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="893b4-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="893b4-770">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="893b4-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="893b4-771">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="893b4-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="893b4-772">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="893b4-773">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="893b4-774">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="893b4-775">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="893b4-776">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="893b4-777">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-777">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="893b4-779">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="893b4-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="893b4-780">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="893b4-781">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="893b4-782">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="893b4-783">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="893b4-784">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="893b4-785">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="893b4-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="893b4-786">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-786">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="893b4-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="893b4-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="893b4-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="893b4-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="893b4-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="893b4-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="893b4-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="893b4-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="893b4-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="893b4-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="893b4-793">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="893b4-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="893b4-794">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="893b4-795">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="893b4-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="893b4-796">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="893b4-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="893b4-797">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="893b4-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="893b4-798">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="893b4-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="893b4-799">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="893b4-800">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="893b4-801">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="893b4-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="893b4-802">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="893b4-803">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="893b4-804">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-804">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="893b4-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="893b4-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="893b4-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-810">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="893b4-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-811">Az.Sql</span></span>
* <span data-ttu-id="893b4-812">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="893b4-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="893b4-813">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="893b4-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="893b4-814">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="893b4-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="893b4-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="893b4-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="893b4-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="893b4-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="893b4-817">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="893b4-818">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="893b4-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="893b4-819">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="893b4-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="893b4-820">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="893b4-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-821">Az.Storage</span></span>
* <span data-ttu-id="893b4-822">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="893b4-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="893b4-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="893b4-825">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="893b4-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="893b4-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="893b4-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="893b4-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="893b4-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="893b4-828">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="893b4-829">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-829">General</span></span>
* <span data-ttu-id="893b4-830">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="893b4-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-831">Az.Accounts</span></span>
* <span data-ttu-id="893b4-832">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="893b4-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-833">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-834">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="893b4-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="893b4-835">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="893b4-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-836">Az.Automation</span></span>
* <span data-ttu-id="893b4-837">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="893b4-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="893b4-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-838">Az.Batch</span></span>
* <span data-ttu-id="893b4-839">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="893b4-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-840">Az.Compute</span></span>
* <span data-ttu-id="893b4-841">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="893b4-842">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="893b4-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="893b4-843">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="893b4-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="893b4-844">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="893b4-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-845">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-846">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="893b4-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="893b4-847">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="893b4-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="893b4-848">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="893b4-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-850">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="893b4-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="893b4-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="893b4-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="893b4-852">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="893b4-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="893b4-853">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="893b4-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="893b4-854">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="893b4-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="893b4-855">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="893b4-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-856">Az.IotHub</span></span>
* <span data-ttu-id="893b4-857">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="893b4-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="893b4-858">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="893b4-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-859">Az.Monitor</span></span>
* <span data-ttu-id="893b4-860">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="893b4-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="893b4-861">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="893b4-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="893b4-862">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="893b4-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="893b4-863">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="893b4-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-864">Az.Network</span></span>
* <span data-ttu-id="893b4-865">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="893b4-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="893b4-866">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="893b4-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="893b4-867">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-867">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="893b4-869">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="893b4-870">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="893b4-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="893b4-871">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="893b4-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="893b4-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="893b4-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="893b4-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="893b4-875">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="893b4-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="893b4-876">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="893b4-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="893b4-877">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="893b4-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="893b4-878">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="893b4-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="893b4-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="893b4-879">Az.RedisCache</span></span>
* <span data-ttu-id="893b4-880">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="893b4-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-881">Az.Sql</span></span>
* <span data-ttu-id="893b4-882">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="893b4-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-883">Az.Storage</span></span>
* <span data-ttu-id="893b4-884">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="893b4-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="893b4-885">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="893b4-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="893b4-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="893b4-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="893b4-887">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="893b4-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="893b4-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="893b4-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="893b4-889">Az.StorageSync</span></span>
* <span data-ttu-id="893b4-890">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="893b4-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-891">Az.Websites</span></span>
* <span data-ttu-id="893b4-892">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="893b4-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="893b4-893">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="893b4-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-894">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-895">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="893b4-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="893b4-896">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="893b4-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="893b4-897">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="893b4-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-898">Az.Automation</span></span>
* <span data-ttu-id="893b4-899">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="893b4-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="893b4-900">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="893b4-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="893b4-901">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="893b4-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-902">Az.Compute</span></span>
* <span data-ttu-id="893b4-903">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="893b4-904">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="893b4-905">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="893b4-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="893b4-906">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="893b4-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="893b4-907">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="893b4-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="893b4-908">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="893b4-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="893b4-909">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="893b4-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="893b4-910">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="893b4-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="893b4-911">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="893b4-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-912">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-913">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="893b4-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="893b4-914">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="893b4-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-915">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-916">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="893b4-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-917">Az.IotHub</span></span>
* <span data-ttu-id="893b4-918">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="893b4-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="893b4-919">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="893b4-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="893b4-920">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="893b4-920">New cmdlets are:</span></span>
    - <span data-ttu-id="893b4-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="893b4-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="893b4-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="893b4-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="893b4-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="893b4-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="893b4-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="893b4-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-925">Az.Monitor</span></span>
* <span data-ttu-id="893b4-926">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="893b4-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="893b4-927">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="893b4-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="893b4-928">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="893b4-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="893b4-929">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="893b4-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="893b4-930">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="893b4-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="893b4-931">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="893b4-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="893b4-932">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="893b4-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="893b4-933">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="893b4-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="893b4-934">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="893b4-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="893b4-935">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="893b4-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="893b4-936">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="893b4-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="893b4-937">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="893b4-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="893b4-938">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="893b4-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="893b4-939">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="893b4-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="893b4-940">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="893b4-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="893b4-941">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="893b4-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="893b4-942">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="893b4-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="893b4-943">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="893b4-944">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="893b4-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="893b4-945">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-945">Overall improved help files</span></span>
* <span data-ttu-id="893b4-946">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="893b4-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-947">Az.Network</span></span>
* <span data-ttu-id="893b4-948">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="893b4-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="893b4-949">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="893b4-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="893b4-950">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="893b4-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="893b4-951">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="893b4-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="893b4-952">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="893b4-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="893b4-953">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="893b4-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="893b4-954">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="893b4-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="893b4-955">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="893b4-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="893b4-956">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="893b4-957">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="893b4-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="893b4-958">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="893b4-959">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="893b4-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="893b4-960">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-960">New cmdlets</span></span>
        - <span data-ttu-id="893b4-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="893b4-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="893b4-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="893b4-963">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="893b4-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="893b4-964">New-VpnSite</span></span>
        - <span data-ttu-id="893b4-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="893b4-965">Update-VpnSite</span></span>
        - <span data-ttu-id="893b4-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-966">New-VpnConnection</span></span>
        - <span data-ttu-id="893b4-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-967">Update-VpnConnection</span></span>
* <span data-ttu-id="893b4-968">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="893b4-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-970">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="893b4-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="893b4-971">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="893b4-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-972">Az.Resources</span></span>
* <span data-ttu-id="893b4-973">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="893b4-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-975">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="893b4-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="893b4-976">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="893b4-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="893b4-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="893b4-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="893b4-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="893b4-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="893b4-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="893b4-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="893b4-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="893b4-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="893b4-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="893b4-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="893b4-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="893b4-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="893b4-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="893b4-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="893b4-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="893b4-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="893b4-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="893b4-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="893b4-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="893b4-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="893b4-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="893b4-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="893b4-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="893b4-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="893b4-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="893b4-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="893b4-990">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="893b4-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="893b4-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="893b4-991">Az.SignalR</span></span>
* <span data-ttu-id="893b4-992">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="893b4-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-993">Az.Sql</span></span>
* <span data-ttu-id="893b4-994">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="893b4-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="893b4-995">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="893b4-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="893b4-996">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="893b4-997">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="893b4-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="893b4-998">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="893b4-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-999">Az.Storage</span></span>
* <span data-ttu-id="893b4-1000">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="893b4-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="893b4-1001">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="893b4-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="893b4-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="893b4-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="893b4-1004">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="893b4-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="893b4-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="893b4-1006">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="893b4-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="893b4-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="893b4-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="893b4-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="893b4-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="893b4-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1011">Az.Websites</span></span>
* <span data-ttu-id="893b4-1012">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="893b4-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="893b4-1013">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="893b4-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="893b4-1014">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="893b4-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="893b4-1015">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="893b4-1016">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-1016">General</span></span>
* <span data-ttu-id="893b4-1017">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="893b4-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1018">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1019">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="893b4-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="893b4-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="893b4-1020">Az.Aks</span></span>
* <span data-ttu-id="893b4-1021">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="893b4-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="893b4-1022">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="893b4-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-1024">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="893b4-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="893b4-1025">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="893b4-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="893b4-1026">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="893b4-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="893b4-1027">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="893b4-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="893b4-1028">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="893b4-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="893b4-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-1029">Az.Batch</span></span>
* <span data-ttu-id="893b4-1030">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="893b4-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-1031">Az.Cdn</span></span>
* <span data-ttu-id="893b4-1032">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="893b4-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1033">Az.Compute</span></span>
* <span data-ttu-id="893b4-1034">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="893b4-1035">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="893b4-1036">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="893b4-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="893b4-1037">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="893b4-1038">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="893b4-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="893b4-1039">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="893b4-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="893b4-1040">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="893b4-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="893b4-1041">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="893b4-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1042">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1043">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="893b4-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="893b4-1044">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="893b4-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="893b4-1045">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="893b4-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="893b4-1046">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="893b4-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1048">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="893b4-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1049">Az.EventHub</span></span>
* <span data-ttu-id="893b4-1050">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="893b4-1051">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="893b4-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="893b4-1052">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="893b4-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="893b4-1053">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="893b4-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="893b4-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="893b4-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="893b4-1055">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="893b4-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-1056">Az.Monitor</span></span>
* <span data-ttu-id="893b4-1057">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1058">Az.Network</span></span>
* <span data-ttu-id="893b4-1059">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="893b4-1060">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="893b4-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="893b4-1061">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="893b4-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="893b4-1062">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="893b4-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="893b4-1063">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="893b4-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="893b4-1064">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="893b4-1065">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="893b4-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1067">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="893b4-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="893b4-1068">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="893b4-1068">Added example</span></span>
    - <span data-ttu-id="893b4-1069">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="893b4-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="893b4-1070">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="893b4-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="893b4-1071">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="893b4-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1073">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1074">Az.Resources</span></span>
* <span data-ttu-id="893b4-1075">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="893b4-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="893b4-1076">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="893b4-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="893b4-1077">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="893b4-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="893b4-1078">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-1080">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="893b4-1081">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="893b4-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="893b4-1082">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="893b4-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-1084">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="893b4-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="893b4-1085">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="893b4-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="893b4-1086">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="893b4-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="893b4-1087">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="893b4-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="893b4-1088">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="893b4-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="893b4-1089">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="893b4-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1090">Az.Sql</span></span>
* <span data-ttu-id="893b4-1091">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="893b4-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1092">Az.Storage</span></span>
* <span data-ttu-id="893b4-1093">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="893b4-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="893b4-1094">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="893b4-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="893b4-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="893b4-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="893b4-1097">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="893b4-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="893b4-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1099">Az.Websites</span></span>
* <span data-ttu-id="893b4-1100">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893b4-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="893b4-1101">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1102">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1103">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="893b4-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="893b4-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="893b4-1105">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="893b4-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1106">Az.Automation</span></span>
* <span data-ttu-id="893b4-1107">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="893b4-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-1109">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="893b4-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1110">Az.Compute</span></span>
* <span data-ttu-id="893b4-1111">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="893b4-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="893b4-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="893b4-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="893b4-1113">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="893b4-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="893b4-1114">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="893b4-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1115">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1116">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="893b4-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="893b4-1117">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="893b4-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1118">Az.EventHub</span></span>
* <span data-ttu-id="893b4-1119">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="893b4-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="893b4-1120">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="893b4-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1121">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-1122">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="893b4-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="893b4-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1123">Az.LogicApp</span></span>
* <span data-ttu-id="893b4-1124">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="893b4-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="893b4-1125">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="893b4-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="893b4-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="893b4-1127">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="893b4-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1128">Az.Network</span></span>
* <span data-ttu-id="893b4-1129">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="893b4-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="893b4-1130">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1130">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="893b4-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="893b4-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="893b4-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="893b4-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="893b4-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="893b4-1139">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="893b4-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="893b4-1140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="893b4-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="893b4-1141">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="893b4-1142">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="893b4-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="893b4-1143">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="893b4-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="893b4-1144">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="893b4-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="893b4-1145">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="893b4-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="893b4-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="893b4-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="893b4-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="893b4-1149">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="893b4-1150">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="893b4-1151">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="893b4-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="893b4-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="893b4-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="893b4-1155">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="893b4-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="893b4-1156">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="893b4-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="893b4-1157">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="893b4-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1159">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="893b4-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="893b4-1160">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="893b4-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1162">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="893b4-1163">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="893b4-1164">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="893b4-1165">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="893b4-1166">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="893b4-1167">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="893b4-1168">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="893b4-1169">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="893b4-1170">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="893b4-1171">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="893b4-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1172">Az.Resources</span></span>
- <span data-ttu-id="893b4-1173">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="893b4-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="893b4-1174">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="893b4-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-1176">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="893b4-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="893b4-1177">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="893b4-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1178">Az.Sql</span></span>
* <span data-ttu-id="893b4-1179">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="893b4-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="893b4-1180">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="893b4-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="893b4-1181">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="893b4-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1182">Az.Storage</span></span>
* <span data-ttu-id="893b4-1183">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="893b4-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="893b4-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="893b4-1184">Az.StorageSync</span></span>
* <span data-ttu-id="893b4-1185">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="893b4-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="893b4-1186">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="893b4-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1187">Az.Websites</span></span>
* <span data-ttu-id="893b4-1188">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="893b4-1189">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="893b4-1190">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="893b4-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="893b4-1191">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1192">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1193">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="893b4-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="893b4-1194">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="893b4-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="893b4-1195">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="893b4-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="893b4-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="893b4-1196">Az.Advisor</span></span>
* <span data-ttu-id="893b4-1197">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="893b4-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="893b4-1198">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="893b4-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="893b4-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-1200">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="893b4-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="893b4-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="893b4-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="893b4-1202">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="893b4-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="893b4-1203">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="893b4-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="893b4-1204">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="893b4-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="893b4-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="893b4-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="893b4-1206">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="893b4-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1207">Az.Automation</span></span>
* <span data-ttu-id="893b4-1208">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="893b4-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1209">Az.Compute</span></span>
* <span data-ttu-id="893b4-1210">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1211">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1212">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="893b4-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="893b4-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="893b4-1213">Az.EventGrid</span></span>
* <span data-ttu-id="893b4-1214">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="893b4-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1215">Az.IotHub</span></span>
* <span data-ttu-id="893b4-1216">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="893b4-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1217">Az.Network</span></span>
* <span data-ttu-id="893b4-1218">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="893b4-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="893b4-1219">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="893b4-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-1221">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="893b4-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="893b4-1222">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="893b4-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1224">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="893b4-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1226">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="893b4-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1227">Az.Resources</span></span>
    - <span data-ttu-id="893b4-1228">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="893b4-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="893b4-1229">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="893b4-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="893b4-1230">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="893b4-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="893b4-1231">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="893b4-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-1233">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="893b4-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1234">Az.Sql</span></span>
* <span data-ttu-id="893b4-1235">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="893b4-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="893b4-1236">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="893b4-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="893b4-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="893b4-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="893b4-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="893b4-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="893b4-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="893b4-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="893b4-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="893b4-1243">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="893b4-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1244">Az.Storage</span></span>
* <span data-ttu-id="893b4-1245">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="893b4-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="893b4-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="893b4-1247">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="893b4-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="893b4-1248">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="893b4-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="893b4-1249">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="893b4-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="893b4-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="893b4-1252">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="893b4-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="893b4-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="893b4-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="893b4-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="893b4-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="893b4-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="893b4-1255">Az.StorageSync</span></span>
* <span data-ttu-id="893b4-1256">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="893b4-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="893b4-1257">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1258">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1259">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="893b4-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="893b4-1260">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="893b4-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="893b4-1261">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="893b4-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="893b4-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="893b4-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="893b4-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="893b4-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1264">Az.Compute</span></span>
* <span data-ttu-id="893b4-1265">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="893b4-1266">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="893b4-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="893b4-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="893b4-1267">Az.Dns</span></span>
* <span data-ttu-id="893b4-1268">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="893b4-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="893b4-1269">Az.EventGrid</span></span>
* <span data-ttu-id="893b4-1270">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="893b4-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="893b4-1271">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="893b4-1271">New cmdlets:</span></span>
    - <span data-ttu-id="893b4-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="893b4-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="893b4-1273">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="893b4-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="893b4-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="893b4-1275">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="893b4-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="893b4-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="893b4-1277">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="893b4-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="893b4-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="893b4-1279">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="893b4-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="893b4-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="893b4-1281">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="893b4-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="893b4-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="893b4-1283">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="893b4-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="893b4-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="893b4-1285">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="893b4-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="893b4-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="893b4-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="893b4-1287">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="893b4-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="893b4-1288">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="893b4-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="893b4-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="893b4-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="893b4-1290">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="893b4-1291">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="893b4-1292">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="893b4-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="893b4-1293">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="893b4-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="893b4-1294">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="893b4-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="893b4-1295">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="893b4-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="893b4-1296">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="893b4-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="893b4-1297">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="893b4-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="893b4-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="893b4-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="893b4-1299">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="893b4-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="893b4-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="893b4-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="893b4-1301">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="893b4-1302">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="893b4-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="893b4-1305">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="893b4-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="893b4-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="893b4-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="893b4-1307">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="893b4-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1308">Az.Network</span></span>
* <span data-ttu-id="893b4-1309">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="893b4-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="893b4-1310">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1310">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="893b4-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="893b4-1312">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="893b4-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="893b4-1313">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1313">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="893b4-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="893b4-1315">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="893b4-1316">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1316">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="893b4-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="893b4-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="893b4-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="893b4-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="893b4-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="893b4-1322">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="893b4-1323">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1323">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="893b4-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="893b4-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="893b4-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="893b4-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="893b4-1328">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="893b4-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="893b4-1329">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="893b4-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="893b4-1330">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="893b4-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="893b4-1331">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="893b4-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="893b4-1332">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="893b4-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="893b4-1333">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="893b4-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="893b4-1334">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="893b4-1335">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="893b4-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="893b4-1336">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="893b4-1337">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="893b4-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="893b4-1338">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="893b4-1339">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="893b4-1340">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="893b4-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="893b4-1341">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="893b4-1342">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="893b4-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="893b4-1343">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="893b4-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="893b4-1344">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="893b4-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="893b4-1345">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="893b4-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="893b4-1346">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="893b4-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="893b4-1347">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="893b4-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="893b4-1348">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="893b4-1349">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="893b4-1350">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1352">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="893b4-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1353">Az.Resources</span></span>
* <span data-ttu-id="893b4-1354">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="893b4-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="893b4-1355">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="893b4-1356">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="893b4-1357">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="893b4-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-1359">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="893b4-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1360">Az.Sql</span></span>
* <span data-ttu-id="893b4-1361">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="893b4-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="893b4-1362">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="893b4-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="893b4-1363">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="893b4-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="893b4-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="893b4-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="893b4-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="893b4-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="893b4-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="893b4-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="893b4-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="893b4-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="893b4-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="893b4-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1369">Az.Storage</span></span>
* <span data-ttu-id="893b4-1370">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="893b4-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="893b4-1372">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="893b4-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="893b4-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1374">Az.Websites</span></span>
* <span data-ttu-id="893b4-1375">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="893b4-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="893b4-1376">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="893b4-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="893b4-1377">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="893b4-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-1378">Az.Cdn</span></span>
* <span data-ttu-id="893b4-1379">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="893b4-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1380">Az.Compute</span></span>
* <span data-ttu-id="893b4-1381">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="893b4-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="893b4-1382">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="893b4-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1383">Az.EventHub</span></span>
* <span data-ttu-id="893b4-1384">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="893b4-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="893b4-1385">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893b4-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1386">Az.Network</span></span>
* <span data-ttu-id="893b4-1387">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="893b4-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="893b4-1388">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="893b4-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-1390">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="893b4-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1392">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="893b4-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-1394">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893b4-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-1396">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="893b4-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="893b4-1397">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1398">Az.Sql</span></span>
* <span data-ttu-id="893b4-1399">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="893b4-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="893b4-1400">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="893b4-1401">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="893b4-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="893b4-1402">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="893b4-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1403">Az.Websites</span></span>
* <span data-ttu-id="893b4-1404">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="893b4-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="893b4-1405">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="893b4-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-1407">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="893b4-1408">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="893b4-1409">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="893b4-1410">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="893b4-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="893b4-1411">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="893b4-1412">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="893b4-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="893b4-1413">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="893b4-1414">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="893b4-1415">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="893b4-1416">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="893b4-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="893b4-1417">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="893b4-1418">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="893b4-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="893b4-1419">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="893b4-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="893b4-1420">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="893b4-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="893b4-1421">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="893b4-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="893b4-1422">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="893b4-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="893b4-1423">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="893b4-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="893b4-1424">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="893b4-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="893b4-1425">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="893b4-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="893b4-1426">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="893b4-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="893b4-1427">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="893b4-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="893b4-1428">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="893b4-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="893b4-1429">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="893b4-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="893b4-1430">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="893b4-1431">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="893b4-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="893b4-1432">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="893b4-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="893b4-1433">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="893b4-1434">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="893b4-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="893b4-1435">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="893b4-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="893b4-1436">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="893b4-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="893b4-1437">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="893b4-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="893b4-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="893b4-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="893b4-1439">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="893b4-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="893b4-1440">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="893b4-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="893b4-1441">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="893b4-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="893b4-1442">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="893b4-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="893b4-1443">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="893b4-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="893b4-1444">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="893b4-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="893b4-1445">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="893b4-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="893b4-1446">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="893b4-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="893b4-1447">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="893b4-1448">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="893b4-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="893b4-1449">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="893b4-1450">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="893b4-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="893b4-1451">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="893b4-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="893b4-1452">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="893b4-1453">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="893b4-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="893b4-1454">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="893b4-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="893b4-1455">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="893b4-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="893b4-1456">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="893b4-1457">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="893b4-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="893b4-1458">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="893b4-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="893b4-1459">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="893b4-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="893b4-1460">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="893b4-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="893b4-1461">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="893b4-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="893b4-1462">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="893b4-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="893b4-1463">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="893b4-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="893b4-1464">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="893b4-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="893b4-1465">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="893b4-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="893b4-1466">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="893b4-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="893b4-1467">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="893b4-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="893b4-1468">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="893b4-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="893b4-1469">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="893b4-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="893b4-1470">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="893b4-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="893b4-1471">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="893b4-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="893b4-1472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="893b4-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="893b4-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="893b4-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="893b4-1474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="893b4-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="893b4-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="893b4-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="893b4-1476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="893b4-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="893b4-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="893b4-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="893b4-1478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="893b4-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="893b4-1479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="893b4-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="893b4-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="893b4-1481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="893b4-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="893b4-1482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="893b4-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="893b4-1483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="893b4-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1484">Az.Automation</span></span>
* <span data-ttu-id="893b4-1485">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="893b4-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="893b4-1486">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="893b4-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="893b4-1487">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="893b4-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="893b4-1488">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="893b4-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="893b4-1489">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="893b4-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="893b4-1490">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="893b4-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="893b4-1491">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="893b4-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1492">Az.Compute</span></span>
* <span data-ttu-id="893b4-1493">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="893b4-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="893b4-1494">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="893b4-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1496">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-1497">Az.Monitor</span></span>
* <span data-ttu-id="893b4-1498">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1499">Az.Network</span></span>
* <span data-ttu-id="893b4-1500">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="893b4-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="893b4-1501">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="893b4-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="893b4-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="893b4-1503">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893b4-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1504">Az.Resources</span></span>
* <span data-ttu-id="893b4-1505">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="893b4-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1506">Az.Sql</span></span>
* <span data-ttu-id="893b4-1507">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="893b4-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="893b4-1508">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1509">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1510">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="893b4-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-1512">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="893b4-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="893b4-1513">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="893b4-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1514">Az.Compute</span></span>
* <span data-ttu-id="893b4-1515">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="893b4-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="893b4-1516">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="893b4-1517">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="893b4-1518">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="893b4-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="893b4-1519">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="893b4-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="893b4-1520">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="893b4-1521">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="893b4-1521">Breaking changes</span></span>
    - <span data-ttu-id="893b4-1522">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="893b4-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="893b4-1523">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="893b4-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="893b4-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="893b4-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="893b4-1525">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="893b4-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="893b4-1526">Az.Dns</span></span>
* <span data-ttu-id="893b4-1527">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="893b4-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="893b4-1528">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="893b4-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="893b4-1529">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="893b4-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="893b4-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="893b4-1531">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="893b4-1532">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="893b4-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="893b4-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-1533">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-1534">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="893b4-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="893b4-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="893b4-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="893b4-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="893b4-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="893b4-1537">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="893b4-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="893b4-1538">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="893b4-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="893b4-1539">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="893b4-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="893b4-1540">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="893b4-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-1541">Az.Monitor</span></span>
* <span data-ttu-id="893b4-1542">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="893b4-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="893b4-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="893b4-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="893b4-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="893b4-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="893b4-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="893b4-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="893b4-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="893b4-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="893b4-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="893b4-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="893b4-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="893b4-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="893b4-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="893b4-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="893b4-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="893b4-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="893b4-1554">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="893b4-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="893b4-1555">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="893b4-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1556">Az.Network</span></span>
* <span data-ttu-id="893b4-1557">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="893b4-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="893b4-1558">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="893b4-1558">New cmdlets</span></span>
        - <span data-ttu-id="893b4-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="893b4-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="893b4-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="893b4-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="893b4-1563">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="893b4-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="893b4-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="893b4-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="893b4-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="893b4-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="893b4-1566">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="893b4-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="893b4-1567">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="893b4-1568">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="893b4-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-1570">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="893b4-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="893b4-1571">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="893b4-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="893b4-1572">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="893b4-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1574">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="893b4-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="893b4-1575">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="893b4-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="893b4-1576">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="893b4-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="893b4-1577">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="893b4-1578">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="893b4-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="893b4-1579">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="893b4-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="893b4-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="893b4-1580">Az.Relay</span></span>
* <span data-ttu-id="893b4-1581">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="893b4-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-1583">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="893b4-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1584">Az.Storage</span></span>
* <span data-ttu-id="893b4-1585">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="893b4-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="893b4-1586">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="893b4-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="893b4-1587">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="893b4-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="893b4-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="893b4-1589">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="893b4-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="893b4-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="893b4-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="893b4-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1593">Az.Websites</span></span>
* <span data-ttu-id="893b4-1594">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="893b4-1595">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="893b4-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="893b4-1596">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-1597">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-1598">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="893b4-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="893b4-1599">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="893b4-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="893b4-1600">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="893b4-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="893b4-1601">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="893b4-1602">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="893b4-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="893b4-1603">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="893b4-1604">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="893b4-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1605">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1606">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="893b4-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="893b4-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-1607">Az.Batch</span></span>
* <span data-ttu-id="893b4-1608">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-1609">Az.Cdn</span></span>
* <span data-ttu-id="893b4-1610">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-1612">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1613">Az.Compute</span></span>
* <span data-ttu-id="893b4-1614">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="893b4-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="893b4-1615">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1616">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="893b4-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1617">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1618">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="893b4-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1620">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="893b4-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="893b4-1621">Az.EventGrid</span></span>
* <span data-ttu-id="893b4-1622">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="893b4-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1623">Az.EventHub</span></span>
* <span data-ttu-id="893b4-1624">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="893b4-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="893b4-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="893b4-1625">Az.HDInsight</span></span>
* <span data-ttu-id="893b4-1626">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1627">Az.IotHub</span></span>
* <span data-ttu-id="893b4-1628">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1629">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-1630">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1631">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="893b4-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="893b4-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="893b4-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="893b4-1633">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="893b4-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="893b4-1634">Az.Media</span></span>
* <span data-ttu-id="893b4-1635">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-1636">Az.Monitor</span></span>
  * <span data-ttu-id="893b4-1637">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="893b4-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="893b4-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="893b4-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="893b4-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="893b4-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="893b4-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="893b4-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="893b4-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="893b4-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="893b4-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="893b4-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="893b4-1643">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="893b4-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1644">Az.Network</span></span>
* <span data-ttu-id="893b4-1645">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1646">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="893b4-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="893b4-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="893b4-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="893b4-1648">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1650">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="893b4-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="893b4-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="893b4-1652">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1654">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1655">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="893b4-1656">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="893b4-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="893b4-1657">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="893b4-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="893b4-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="893b4-1658">Az.RedisCache</span></span>
* <span data-ttu-id="893b4-1659">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1660">Az.Resources</span></span>
* <span data-ttu-id="893b4-1661">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="893b4-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1662">Az.Sql</span></span>
* <span data-ttu-id="893b4-1663">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="893b4-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="893b4-1664">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1665">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="893b4-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="893b4-1666">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="893b4-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="893b4-1667">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="893b4-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="893b4-1668">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="893b4-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="893b4-1669">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="893b4-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1670">Az.Websites</span></span>
* <span data-ttu-id="893b4-1671">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="893b4-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="893b4-1672">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="893b4-1673">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="893b4-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="893b4-1674">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="893b4-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="893b4-1675">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-1676">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-1677">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="893b4-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="893b4-1678">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="893b4-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="893b4-1679">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="893b4-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="893b4-1680">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="893b4-1681">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="893b4-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="893b4-1682">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="893b4-1683">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="893b4-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="893b4-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1684">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1685">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="893b4-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="893b4-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="893b4-1687">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="893b4-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="893b4-1688">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="893b4-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1689">Az.Automation</span></span>
* <span data-ttu-id="893b4-1690">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="893b4-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="893b4-1691">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="893b4-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="893b4-1692">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1693">Az.Compute</span></span>
* <span data-ttu-id="893b4-1694">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="893b4-1695">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="893b4-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="893b4-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="893b4-1697">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="893b4-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1698">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1699">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="893b4-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="893b4-1700">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="893b4-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1701">Az.Resources</span></span>
* <span data-ttu-id="893b4-1702">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="893b4-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="893b4-1703">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="893b4-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="893b4-1704">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="893b4-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="893b4-1705">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="893b4-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="893b4-1706">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="893b4-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="893b4-1707">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="893b4-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1708">Az.Sql</span></span>
* <span data-ttu-id="893b4-1709">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="893b4-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1710">Az.Storage</span></span>
* <span data-ttu-id="893b4-1711">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="893b4-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="893b4-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="893b4-1713">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="893b4-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="893b4-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="893b4-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="893b4-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="893b4-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="893b4-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="893b4-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="893b4-1718">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="893b4-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="893b4-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="893b4-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="893b4-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="893b4-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="893b4-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="893b4-1723">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="893b4-1724">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="893b4-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="893b4-1725">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="893b4-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="893b4-1726">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="893b4-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="893b4-1727">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="893b4-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="893b4-1728">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="893b4-1729">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="893b4-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="893b4-1730">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="893b4-1731">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="893b4-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1732">Az.Automation</span></span>
* <span data-ttu-id="893b4-1733">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="893b4-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="893b4-1734">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="893b4-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="893b4-1735">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="893b4-1735">Pre-Post script</span></span>
    * <span data-ttu-id="893b4-1736">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="893b4-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1737">Az.Compute</span></span>
* <span data-ttu-id="893b4-1738">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="893b4-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="893b4-1739">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="893b4-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1740">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-1741">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1742">Az.Network</span></span>
* <span data-ttu-id="893b4-1743">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="893b4-1744">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="893b4-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1746">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="893b4-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="893b4-1747">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="893b4-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1748">Az.Resources</span></span>
* <span data-ttu-id="893b4-1749">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="893b4-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="893b4-1750">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="893b4-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1751">Az.Sql</span></span>
* <span data-ttu-id="893b4-1752">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="893b4-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1753">Az.Storage</span></span>
* <span data-ttu-id="893b4-1754">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="893b4-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="893b4-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="893b4-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="893b4-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="893b4-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="893b4-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="893b4-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="893b4-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="893b4-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1761">Az.Websites</span></span>
* <span data-ttu-id="893b4-1762">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="893b4-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="893b4-1763">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1764">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1765">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="893b4-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="893b4-1766">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1767">Az.Automation</span></span>
* <span data-ttu-id="893b4-1768">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="893b4-1769">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="893b4-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="893b4-1770">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="893b4-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-1771">Az.Cdn</span></span>
* <span data-ttu-id="893b4-1772">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="893b4-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1773">Az.Compute</span></span>
* <span data-ttu-id="893b4-1774">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="893b4-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1775">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1776">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="893b4-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="893b4-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1777">Az.LogicApp</span></span>
* <span data-ttu-id="893b4-1778">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="893b4-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1779">Az.Network</span></span>
* <span data-ttu-id="893b4-1780">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1782">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="893b4-1783">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="893b4-1783">SDK Update</span></span>
* <span data-ttu-id="893b4-1784">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="893b4-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="893b4-1785">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="893b4-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1786">Az.Resources</span></span>
* <span data-ttu-id="893b4-1787">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="893b4-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="893b4-1788">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="893b4-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="893b4-1789">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="893b4-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="893b4-1790">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="893b4-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="893b4-1791">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="893b4-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="893b4-1792">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="893b4-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1793">Az.Sql</span></span>
* <span data-ttu-id="893b4-1794">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="893b4-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="893b4-1795">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="893b4-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1796">Az.Storage</span></span>
* <span data-ttu-id="893b4-1797">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="893b4-1798">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="893b4-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="893b4-1800">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1801">Az.Automation</span></span>
* <span data-ttu-id="893b4-1802">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="893b4-1803">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="893b4-1804">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-1806">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="893b4-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1807">Az.Compute</span></span>
* <span data-ttu-id="893b4-1808">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="893b4-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="893b4-1809">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="893b4-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="893b4-1810">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="893b4-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="893b4-1811">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="893b4-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1813">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="893b4-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="893b4-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1814">Az.EventHub</span></span>
* <span data-ttu-id="893b4-1815">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1816">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-1817">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="893b4-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="893b4-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1818">Az.LogicApp</span></span>
* <span data-ttu-id="893b4-1819">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="893b4-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="893b4-1820">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="893b4-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="893b4-1821">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="893b4-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="893b4-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="893b4-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="893b4-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="893b4-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="893b4-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="893b4-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="893b4-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="893b4-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="893b4-1826">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="893b4-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="893b4-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="893b4-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="893b4-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="893b4-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="893b4-1831">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="893b4-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="893b4-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-1832">Az.Monitor</span></span>
* <span data-ttu-id="893b4-1833">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="893b4-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1834">Az.Network</span></span>
* <span data-ttu-id="893b4-1835">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="893b4-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="893b4-1837">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="893b4-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="893b4-1838">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="893b4-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="893b4-1839">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="893b4-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1840">Az.Resources</span></span>
* <span data-ttu-id="893b4-1841">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="893b4-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="893b4-1842">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="893b4-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="893b4-1843">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="893b4-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="893b4-1844">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="893b4-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1845">Az.Sql</span></span>
* <span data-ttu-id="893b4-1846">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="893b4-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="893b4-1847">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="893b4-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1848">Az.Websites</span></span>
* <span data-ttu-id="893b4-1849">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="893b4-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="893b4-1850">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1851">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1852">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="893b4-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="893b4-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="893b4-1854">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="893b4-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1855">Az.Compute</span></span>
* <span data-ttu-id="893b4-1856">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="893b4-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="893b4-1857">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="893b4-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="893b4-1858">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="893b4-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="893b4-1860">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="893b4-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1861">Az.Resources</span></span>
* <span data-ttu-id="893b4-1862">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="893b4-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="893b4-1863">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="893b4-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="893b4-1864">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="893b4-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="893b4-1865">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="893b4-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1866">Az.Sql</span></span>
* <span data-ttu-id="893b4-1867">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="893b4-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="893b4-1868">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="893b4-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="893b4-1869">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="893b4-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="893b4-1870">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1871">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1872">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="893b4-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="893b4-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="893b4-1874">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="893b4-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="893b4-1876">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="893b4-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="893b4-1877">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1878">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1879">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="893b4-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="893b4-1880">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="893b4-1881">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="893b4-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="893b4-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="893b4-1882">Az.Aks</span></span>
* <span data-ttu-id="893b4-1883">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="893b4-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-1884">Az.Automation</span></span>
* <span data-ttu-id="893b4-1885">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="893b4-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="893b4-1886">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="893b4-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="893b4-1887">Az.Cdn</span></span>
* <span data-ttu-id="893b4-1888">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1889">Az.Compute</span></span>
* <span data-ttu-id="893b4-1890">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="893b4-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="893b4-1891">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="893b4-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="893b4-1892">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="893b4-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="893b4-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="893b4-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="893b4-1894">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="893b4-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="893b4-1895">Az.DataFactory</span></span>
* <span data-ttu-id="893b4-1896">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="893b4-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1898">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="893b4-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="893b4-1899">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="893b4-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="893b4-1900">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1901">Az.IotHub</span></span>
* <span data-ttu-id="893b4-1902">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="893b4-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="893b4-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-1903">Az.KeyVault</span></span>
* <span data-ttu-id="893b4-1904">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-1905">Az.Network</span></span>
* <span data-ttu-id="893b4-1906">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1907">Az.Resources</span></span>
* <span data-ttu-id="893b4-1908">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="893b4-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="893b4-1909">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="893b4-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="893b4-1910">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="893b4-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="893b4-1911">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="893b4-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="893b4-1912">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="893b4-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="893b4-1913">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="893b4-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="893b4-1914">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="893b4-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-1916">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="893b4-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="893b4-1917">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="893b4-1917">Fix some error messages.</span></span>
* <span data-ttu-id="893b4-1918">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="893b4-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="893b4-1919">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="893b4-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="893b4-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="893b4-1920">Az.SignalR</span></span>
* <span data-ttu-id="893b4-1921">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1922">Az.Sql</span></span>
* <span data-ttu-id="893b4-1923">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="893b4-1924">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="893b4-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="893b4-1925">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="893b4-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="893b4-1926">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="893b4-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1927">Az.Storage</span></span>
* <span data-ttu-id="893b4-1928">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="893b4-1929">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="893b4-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="893b4-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="893b4-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="893b4-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="893b4-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="893b4-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="893b4-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="893b4-1933">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1934">Az.Websites</span></span>
* <span data-ttu-id="893b4-1935">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="893b4-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="893b4-1936">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="893b4-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="893b4-1937">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="893b4-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="893b4-1938">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="893b4-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="893b4-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1939">Az.Accounts</span></span>
* <span data-ttu-id="893b4-1940">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="893b4-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-1941">Az.Compute</span></span>
* <span data-ttu-id="893b4-1942">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="893b4-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="893b4-1943">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="893b4-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="893b4-1944">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-1946">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="893b4-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="893b4-1947">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="893b4-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="893b4-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="893b4-1948">Az.EventGrid</span></span>
* <span data-ttu-id="893b4-1949">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="893b4-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="893b4-1950">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="893b4-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="893b4-1951">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="893b4-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="893b4-1952">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="893b4-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="893b4-1953">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="893b4-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="893b4-1954">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="893b4-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="893b4-1955">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="893b4-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="893b4-1956">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="893b4-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="893b4-1957">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="893b4-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="893b4-1958">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="893b4-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="893b4-1959">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="893b4-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="893b4-1960">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="893b4-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="893b4-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1961">Az.IotHub</span></span>
* <span data-ttu-id="893b4-1962">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="893b4-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="893b4-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="893b4-1963">Az.LogicApp</span></span>
* <span data-ttu-id="893b4-1964">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="893b4-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-1965">Az.Resources</span></span>
* <span data-ttu-id="893b4-1966">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="893b4-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="893b4-1967">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="893b4-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="893b4-1968">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="893b4-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="893b4-1969">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="893b4-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="893b4-1970">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="893b4-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="893b4-1971">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="893b4-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="893b4-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="893b4-1972">Az.SignalR</span></span>
* <span data-ttu-id="893b4-1973">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-1974">Az.Sql</span></span>
* <span data-ttu-id="893b4-1975">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="893b4-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="893b4-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-1976">Az.Storage</span></span>
* <span data-ttu-id="893b4-1977">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="893b4-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="893b4-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="893b4-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="893b4-1979">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="893b4-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="893b4-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="893b4-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-1981">Az.Websites</span></span>
* <span data-ttu-id="893b4-1982">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="893b4-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="893b4-1983">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="893b4-1984">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="893b4-1985">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-1985">General</span></span>

- <span data-ttu-id="893b4-1986">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="893b4-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="893b4-1987">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="893b4-1987">Online help for each module</span></span>
- <span data-ttu-id="893b4-1988">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="893b4-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="893b4-1989">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="893b4-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="893b4-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-1990">Az.Accounts</span></span>
- <span data-ttu-id="893b4-1991">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="893b4-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="893b4-1992">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="893b4-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="893b4-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="893b4-1994">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="893b4-1994">Fixes for #7002</span></span>
- <span data-ttu-id="893b4-1995">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="893b4-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="893b4-1996">Az.Batch</span></span>
- <span data-ttu-id="893b4-1997">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="893b4-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="893b4-1998">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="893b4-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="893b4-1999">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="893b4-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="893b4-2000">Az.Billing</span></span>
- <span data-ttu-id="893b4-2001">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="893b4-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="893b4-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="893b4-2003">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="893b4-2004">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="893b4-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="893b4-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="893b4-2006">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="893b4-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="893b4-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="893b4-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="893b4-2008">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="893b4-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="893b4-2010">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="893b4-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="893b4-2011">Az.Monitor</span></span>
- <span data-ttu-id="893b4-2012">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="893b4-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="893b4-2013">Az.KeyVault</span></span>
- <span data-ttu-id="893b4-2014">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="893b4-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="893b4-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="893b4-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="893b4-2016">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="893b4-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="893b4-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="893b4-2017">Az.Media</span></span>
- <span data-ttu-id="893b4-2018">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="893b4-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="893b4-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-2019">Az.Network</span></span>
<span data-ttu-id="893b4-2020">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="893b4-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="893b4-2021">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="893b4-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="893b4-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="893b4-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="893b4-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="893b4-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="893b4-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="893b4-2030">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="893b4-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="893b4-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="893b4-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="893b4-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="893b4-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="893b4-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="893b4-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="893b4-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="893b4-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="893b4-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="893b4-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="893b4-2037">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="893b4-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="893b4-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="893b4-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="893b4-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="893b4-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="893b4-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="893b4-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="893b4-2041">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="893b4-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="893b4-2042">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="893b4-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="893b4-2044">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="893b4-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="893b4-2045">Az.Profile</span></span>
- <span data-ttu-id="893b4-2046">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="893b4-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="893b4-2048">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="893b4-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2049">Az.Resources</span></span>
- <span data-ttu-id="893b4-2050">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="893b4-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="893b4-2052">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="893b4-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="893b4-2053">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="893b4-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="893b4-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="893b4-2055">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="893b4-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="893b4-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-2056">Az.Sql</span></span>
- <span data-ttu-id="893b4-2057">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="893b4-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="893b4-2058">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="893b4-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="893b4-2059">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="893b4-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-2060">Az.Storage</span></span>
- <span data-ttu-id="893b4-2061">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="893b4-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-2062">Az.Websites</span></span>
- <span data-ttu-id="893b4-2063">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="893b4-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="893b4-2064">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="893b4-2065">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-2065">General</span></span>

* <span data-ttu-id="893b4-2066">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="893b4-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="893b4-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-2067">Az.Compute</span></span>

* <span data-ttu-id="893b4-2068">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="893b4-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="893b4-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="893b4-2070">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="893b4-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="893b4-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="893b4-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="893b4-2072">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="893b4-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="893b4-2073">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="893b4-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="893b4-2074">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="893b4-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="893b4-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="893b4-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="893b4-2076">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="893b4-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="893b4-2077">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="893b4-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="893b4-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2078">Az.Resources</span></span>

* <span data-ttu-id="893b4-2079">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="893b4-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="893b4-2080">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="893b4-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="893b4-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-2081">Az.Sql</span></span>

* <span data-ttu-id="893b4-2082">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="893b4-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="893b4-2083">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="893b4-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="893b4-2084">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="893b4-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="893b4-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-2085">Az.Storage</span></span>

* <span data-ttu-id="893b4-2086">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="893b4-2087">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="893b4-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="893b4-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="893b4-2089">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="893b4-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="893b4-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="893b4-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="893b4-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="893b4-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="893b4-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-2092">Az.Websites</span></span>

* <span data-ttu-id="893b4-2093">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893b4-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="893b4-2094">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="893b4-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="893b4-2095">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="893b4-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="893b4-2096">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="893b4-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="893b4-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="893b4-2098">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="893b4-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="893b4-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="893b4-2099">Az.Automation</span></span>
* <span data-ttu-id="893b4-2100">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="893b4-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="893b4-2101">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="893b4-2102">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="893b4-2103">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="893b4-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="893b4-2104">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="893b4-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="893b4-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-2105">Az.Compute</span></span>
* <span data-ttu-id="893b4-2106">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="893b4-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="893b4-2107">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="893b4-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="893b4-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="893b4-2109">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="893b4-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="893b4-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="893b4-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="893b4-2111">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="893b4-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="893b4-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-2112">Az.Network</span></span>
* <span data-ttu-id="893b4-2113">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="893b4-2114">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="893b4-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="893b4-2115">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="893b4-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="893b4-2116">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="893b4-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="893b4-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="893b4-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="893b4-2118">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="893b4-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="893b4-2119">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="893b4-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="893b4-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="893b4-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="893b4-2121">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="893b4-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="893b4-2122">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="893b4-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="893b4-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="893b4-2123">Az.Relay</span></span>
* <span data-ttu-id="893b4-2124">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="893b4-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="893b4-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2125">Az.Resources</span></span>
* <span data-ttu-id="893b4-2126">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="893b4-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="893b4-2127">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="893b4-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="893b4-2128">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="893b4-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="893b4-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-2130">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="893b4-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="893b4-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-2131">Az.Sql</span></span>
* <span data-ttu-id="893b4-2132">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="893b4-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="893b4-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="893b4-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="893b4-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="893b4-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="893b4-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="893b4-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="893b4-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="893b4-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="893b4-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="893b4-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="893b4-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="893b4-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="893b4-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="893b4-2141">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="893b4-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="893b4-2142">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="893b4-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="893b4-2143">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="893b4-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="893b4-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="893b4-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="893b4-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="893b4-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="893b4-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="893b4-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="893b4-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="893b4-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="893b4-2148">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="893b4-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="893b4-2149">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="893b4-2150">Geral</span><span class="sxs-lookup"><span data-stu-id="893b4-2150">General</span></span>
* <span data-ttu-id="893b4-2151">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="893b4-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="893b4-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="893b4-2152">Az.Profile</span></span>
* <span data-ttu-id="893b4-2153">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="893b4-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="893b4-2154">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="893b4-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="893b4-2155">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="893b4-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="893b4-2156">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="893b4-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="893b4-2157">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="893b4-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="893b4-2158">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="893b4-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="893b4-2159">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="893b4-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-2161">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="893b4-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-2162">Az.Compute</span></span>
* <span data-ttu-id="893b4-2163">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="893b4-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="893b4-2164">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="893b4-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="893b4-2165">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="893b4-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-2167">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="893b4-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="893b4-2168">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="893b4-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="893b4-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="893b4-2169">Az.Insights</span></span>
* <span data-ttu-id="893b4-2170">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="893b4-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="893b4-2171">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="893b4-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="893b4-2172">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="893b4-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="893b4-2173">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="893b4-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-2174">Az.Network</span></span>
* <span data-ttu-id="893b4-2175">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="893b4-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="893b4-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="893b4-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="893b4-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="893b4-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="893b4-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="893b4-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="893b4-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="893b4-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="893b4-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="893b4-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="893b4-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="893b4-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="893b4-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="893b4-2183">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="893b4-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2184">Az.Resources</span></span>
* <span data-ttu-id="893b4-2185">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="893b4-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="893b4-2186">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="893b4-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="893b4-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="893b4-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="893b4-2188">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="893b4-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="893b4-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="893b4-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="893b4-2190">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="893b4-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="893b4-2191">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="893b4-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="893b4-2192">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="893b4-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="893b4-2193">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="893b4-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="893b4-2194">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="893b4-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="893b4-2195">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="893b4-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="893b4-2196">Az.Profile</span></span>
* <span data-ttu-id="893b4-2197">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="893b4-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="893b4-2198">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="893b4-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-2199">Az.Compute</span></span>
* <span data-ttu-id="893b4-2200">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="893b4-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="893b4-2201">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="893b4-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="893b4-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="893b4-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="893b4-2203">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="893b4-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="893b4-2204">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="893b4-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="893b4-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="893b4-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="893b4-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="893b4-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="893b4-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="893b4-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-2208">Az.Network</span></span>
* <span data-ttu-id="893b4-2209">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="893b4-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="893b4-2210">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="893b4-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2211">Az.Resources</span></span>
* <span data-ttu-id="893b4-2212">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="893b4-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="893b4-2213">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="893b4-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="893b4-2214">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="893b4-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="893b4-2215">Azure.Storage</span></span>
* <span data-ttu-id="893b4-2216">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="893b4-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="893b4-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="893b4-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="893b4-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="893b4-2219">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="893b4-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="893b4-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="893b4-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="893b4-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="893b4-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="893b4-2222">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="893b4-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="893b4-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="893b4-2223">Az.Compute</span></span>
* <span data-ttu-id="893b4-2224">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="893b4-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="893b4-2225">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="893b4-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="893b4-2226">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="893b4-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="893b4-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="893b4-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="893b4-2228">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="893b4-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="893b4-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="893b4-2229">Az.Network</span></span>
* <span data-ttu-id="893b4-2230">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="893b4-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="893b4-2231">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="893b4-2231">new cmdlets added</span></span>
    - <span data-ttu-id="893b4-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="893b4-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="893b4-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="893b4-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="893b4-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="893b4-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="893b4-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="893b4-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="893b4-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="893b4-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="893b4-2238">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="893b4-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="893b4-2239">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="893b4-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="893b4-2240">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="893b4-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="893b4-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="893b4-2241">Az.RedisCache</span></span>
* <span data-ttu-id="893b4-2242">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="893b4-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="893b4-2243">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="893b4-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="893b4-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="893b4-2244">Az.Resources</span></span>
* <span data-ttu-id="893b4-2245">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="893b4-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="893b4-2246">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="893b4-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="893b4-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="893b4-2247">Az.Sql</span></span>
* <span data-ttu-id="893b4-2248">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="893b4-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="893b4-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="893b4-2249">Az.Websites</span></span>
* <span data-ttu-id="893b4-2250">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="893b4-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="893b4-2251">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="893b4-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="893b4-2252">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="893b4-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="893b4-2253">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="893b4-2253">Initial Release</span></span>
