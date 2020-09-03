---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c0f322fb0905bae96f89f41949bcc43ad81056c7
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239971"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6d5c3-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d5c3-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="6d5c3-104">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="6d5c3-105">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="6d5c3-105">Highlights since the last release</span></span>
* <span data-ttu-id="6d5c3-106">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="6d5c3-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-107">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-108">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-109">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-110">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="6d5c3-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6d5c3-111">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-112">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-113">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="6d5c3-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-115">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="6d5c3-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-116">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-117">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="6d5c3-118">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-119">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-120">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="6d5c3-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="6d5c3-123">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="6d5c3-124">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="6d5c3-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="6d5c3-127">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="6d5c3-128">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-128">New cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6d5c3-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6d5c3-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6d5c3-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="6d5c3-133">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-134">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-135">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="6d5c3-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="6d5c3-136">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="6d5c3-137">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="6d5c3-138">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="6d5c3-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-139">Az.Maintenance</span></span>
* <span data-ttu-id="6d5c3-140">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-141">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-142">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="6d5c3-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6d5c3-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6d5c3-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6d5c3-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6d5c3-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6d5c3-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6d5c3-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-150">Az.Network</span></span>
* <span data-ttu-id="6d5c3-151">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="6d5c3-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6d5c3-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6d5c3-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="6d5c3-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="6d5c3-156">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="6d5c3-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="6d5c3-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="6d5c3-159">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="6d5c3-160">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6d5c3-161">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="6d5c3-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="6d5c3-162">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6d5c3-163">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="6d5c3-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="6d5c3-164">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="6d5c3-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="6d5c3-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-168">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="6d5c3-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="6d5c3-169">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-171">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-172">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-173">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="6d5c3-174">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-175">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-176">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="6d5c3-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6d5c3-177">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="6d5c3-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="6d5c3-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6d5c3-180">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="6d5c3-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="6d5c3-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6d5c3-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6d5c3-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="6d5c3-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6d5c3-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="6d5c3-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6d5c3-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="6d5c3-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="6d5c3-189">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="6d5c3-190">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-190">General</span></span>
* <span data-ttu-id="6d5c3-191">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="6d5c3-192">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="6d5c3-193">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="6d5c3-194">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="6d5c3-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6d5c3-195">Az.Billing</span></span>
  - <span data-ttu-id="6d5c3-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-196">Az.Compute</span></span>
  - <span data-ttu-id="6d5c3-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="6d5c3-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-198">Az.EventHub</span></span>
  - <span data-ttu-id="6d5c3-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-199">Az.IotHub</span></span>
  - <span data-ttu-id="6d5c3-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-200">Az.KeyVault</span></span>
  - <span data-ttu-id="6d5c3-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-201">Az.Monitor</span></span>
  - <span data-ttu-id="6d5c3-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-202">Az.Network</span></span>
  - <span data-ttu-id="6d5c3-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-203">Az.Resources</span></span>
  - <span data-ttu-id="6d5c3-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-204">Az.Storage</span></span>
  - <span data-ttu-id="6d5c3-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-205">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-206">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-207">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="6d5c3-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="6d5c3-208">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="6d5c3-209">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-210">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-211">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-212">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-213">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="6d5c3-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="6d5c3-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="6d5c3-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="6d5c3-215">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="6d5c3-216">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="6d5c3-217">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-217">[#11354]</span></span>
* <span data-ttu-id="6d5c3-218">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="6d5c3-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="6d5c3-219">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6d5c3-220">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6d5c3-221">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6d5c3-222">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="6d5c3-223">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="6d5c3-224">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="6d5c3-225">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="6d5c3-226">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-227">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-228">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="6d5c3-229">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="6d5c3-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-231">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="6d5c3-232">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-233">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-234">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-235">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-236">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="6d5c3-237">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-238">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="6d5c3-239">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-240">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-241">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-242">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-243">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-244">Az.Network</span></span>
* <span data-ttu-id="6d5c3-245">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="6d5c3-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="6d5c3-246">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6d5c3-247">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6d5c3-248">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="6d5c3-249">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="6d5c3-250">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="6d5c3-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-252">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-254">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="6d5c3-255">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="6d5c3-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="6d5c3-256">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="6d5c3-257">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="6d5c3-258">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="6d5c3-259">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-260">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-261">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="6d5c3-262">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="6d5c3-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="6d5c3-263">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="6d5c3-264">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-264">Added example.</span></span>
* <span data-ttu-id="6d5c3-265">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="6d5c3-266">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="6d5c3-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-267">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-268">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="6d5c3-269">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6d5c3-270">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="6d5c3-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="6d5c3-271">Az.Support</span></span>
* <span data-ttu-id="6d5c3-272">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-273">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-274">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="6d5c3-275">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6d5c3-276">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6d5c3-277">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6d5c3-278">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="6d5c3-279">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-280">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-281">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="6d5c3-282">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="6d5c3-283">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-284">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-285">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="6d5c3-286">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="6d5c3-287">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="6d5c3-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="6d5c3-288">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-290">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-291">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-292">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6d5c3-293">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-294">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-295">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-296">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-297">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="6d5c3-298">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="6d5c3-299">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-300">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="6d5c3-301">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="6d5c3-302">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="6d5c3-303">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="6d5c3-304">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6d5c3-305">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6d5c3-306">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="6d5c3-307">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-308">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="6d5c3-309">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="6d5c3-310">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-311">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-312">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-313">Az.Network</span></span>
* <span data-ttu-id="6d5c3-314">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="6d5c3-315">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="6d5c3-316">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="6d5c3-317">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-318">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-319">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="6d5c3-320">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="6d5c3-321">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="6d5c3-322">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="6d5c3-323">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="6d5c3-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="6d5c3-324">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="6d5c3-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="6d5c3-325">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="6d5c3-326">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="6d5c3-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6d5c3-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6d5c3-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="6d5c3-330">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="6d5c3-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="6d5c3-332">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-333">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-334">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="6d5c3-335">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="6d5c3-336">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="6d5c3-337">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="6d5c3-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="6d5c3-338">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="6d5c3-339">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="6d5c3-340">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6d5c3-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="6d5c3-341">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="6d5c3-342">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-343">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-344">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="6d5c3-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="6d5c3-346">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="6d5c3-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="6d5c3-347">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="6d5c3-348">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-349">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-350">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="6d5c3-351">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="6d5c3-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="6d5c3-352">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="6d5c3-353">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="6d5c3-354">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="6d5c3-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="6d5c3-355">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-356">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-356">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-357">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="6d5c3-358">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="6d5c3-359">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-360">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-361">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-362">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-363">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-365">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="6d5c3-366">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="6d5c3-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-367">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-368">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="6d5c3-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-369">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-370">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="6d5c3-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-371">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-372">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6d5c3-373">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-374">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-375">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-376">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6d5c3-377">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-378">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-379">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="6d5c3-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-380">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-381">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="6d5c3-382">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="6d5c3-383">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-384">Az.Network</span></span>
* <span data-ttu-id="6d5c3-385">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="6d5c3-386">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6d5c3-387">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6d5c3-388">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="6d5c3-389">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-389">No new cmdlets are added.</span></span> <span data-ttu-id="6d5c3-390">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-392">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-393">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-394">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="6d5c3-395">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="6d5c3-396">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="6d5c3-397">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="6d5c3-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="6d5c3-398">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="6d5c3-399">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="6d5c3-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="6d5c3-400">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="6d5c3-401">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-402">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-403">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="6d5c3-404">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="6d5c3-405">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="6d5c3-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6d5c3-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6d5c3-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6d5c3-407">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6d5c3-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6d5c3-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6d5c3-408">Az.StorageSync</span></span>
* <span data-ttu-id="6d5c3-409">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6d5c3-410">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-411">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-411">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-412">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6d5c3-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6d5c3-413">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-414">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-415">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="6d5c3-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6d5c3-416">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="6d5c3-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-417">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-418">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6d5c3-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6d5c3-419">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="6d5c3-420">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="6d5c3-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6d5c3-421">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-422">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-423">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6d5c3-424">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6d5c3-425">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6d5c3-427">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-428">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-429">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6d5c3-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6d5c3-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="6d5c3-431">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6d5c3-432">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="6d5c3-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-433">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-434">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-435">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-436">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-437">Az.Network</span></span>
* <span data-ttu-id="6d5c3-438">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6d5c3-439">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6d5c3-440">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-441">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="6d5c3-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6d5c3-442">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6d5c3-443">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6d5c3-444">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6d5c3-445">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6d5c3-446">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-446">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6d5c3-448">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6d5c3-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6d5c3-450">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-452">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="6d5c3-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6d5c3-453">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6d5c3-454">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="6d5c3-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6d5c3-455">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="6d5c3-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-457">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6d5c3-458">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-459">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-460">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="6d5c3-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6d5c3-461">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="6d5c3-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-462">Az.Sql</span></span>
<span data-ttu-id="6d5c3-463">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-464">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-465">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6d5c3-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="6d5c3-467">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6d5c3-468">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-469">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-470">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="6d5c3-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6d5c3-471">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="6d5c3-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6d5c3-472">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="6d5c3-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-473">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-474">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6d5c3-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-475">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-476">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-477">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-478">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6d5c3-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="6d5c3-480">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6d5c3-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6d5c3-482">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6d5c3-483">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6d5c3-484">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6d5c3-485">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6d5c3-486">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6d5c3-487">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6d5c3-488">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6d5c3-489">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6d5c3-490">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6d5c3-491">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6d5c3-492">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6d5c3-493">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6d5c3-494">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6d5c3-495">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6d5c3-496">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6d5c3-497">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6d5c3-498">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6d5c3-499">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-500">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-501">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6d5c3-502">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6d5c3-503">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6d5c3-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6d5c3-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="6d5c3-505">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="6d5c3-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-506">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-507">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="6d5c3-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-508">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-509">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6d5c3-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6d5c3-510">Az.MachineLearning</span></span>
* <span data-ttu-id="6d5c3-511">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="6d5c3-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6d5c3-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6d5c3-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6d5c3-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6d5c3-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6d5c3-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6d5c3-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6d5c3-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6d5c3-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6d5c3-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6d5c3-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6d5c3-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6d5c3-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-519">Az.Network</span></span>
* <span data-ttu-id="6d5c3-520">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="6d5c3-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-522">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6d5c3-523">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6d5c3-524">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6d5c3-525">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-526">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-527">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-528">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-529">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6d5c3-530">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="6d5c3-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6d5c3-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6d5c3-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6d5c3-532">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="6d5c3-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-533">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-534">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="6d5c3-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6d5c3-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6d5c3-536">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="6d5c3-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="6d5c3-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6d5c3-538">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6d5c3-539">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-539">General</span></span>
* <span data-ttu-id="6d5c3-540">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-541">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-542">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="6d5c3-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6d5c3-543">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="6d5c3-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6d5c3-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-544">Az.Batch</span></span>
* <span data-ttu-id="6d5c3-545">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-546">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-547">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-548">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-549">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="6d5c3-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6d5c3-550">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="6d5c3-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6d5c3-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6d5c3-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="6d5c3-552">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="6d5c3-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-553">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-554">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="6d5c3-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6d5c3-555">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="6d5c3-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6d5c3-556">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-557">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-558">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6d5c3-559">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="6d5c3-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6d5c3-560">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-561">Az.Network</span></span>
* <span data-ttu-id="6d5c3-562">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-563">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-564">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6d5c3-565">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-566">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-567">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-568">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-569">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="6d5c3-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6d5c3-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6d5c3-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6d5c3-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6d5c3-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6d5c3-572">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6d5c3-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6d5c3-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6d5c3-574">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6d5c3-575">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="6d5c3-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6d5c3-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6d5c3-578">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6d5c3-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6d5c3-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6d5c3-580">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6d5c3-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6d5c3-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6d5c3-582">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-583">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-583">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-584">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6d5c3-585">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-586">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-587">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-587">VM Reapply feature</span></span>
    - <span data-ttu-id="6d5c3-588">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6d5c3-589">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6d5c3-590">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6d5c3-591">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6d5c3-592">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6d5c3-593">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6d5c3-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6d5c3-594">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="6d5c3-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6d5c3-595">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6d5c3-596">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5c3-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6d5c3-597">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6d5c3-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6d5c3-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6d5c3-599">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6d5c3-600">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-600">Get the Order</span></span>
* <span data-ttu-id="6d5c3-601">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6d5c3-602">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-602">Create new Order</span></span>
* <span data-ttu-id="6d5c3-603">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6d5c3-604">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-604">Remove the Order</span></span>
* <span data-ttu-id="6d5c3-605">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6d5c3-606">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="6d5c3-606">Now creates Local Share</span></span>
* <span data-ttu-id="6d5c3-607">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6d5c3-608">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="6d5c3-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6d5c3-609">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6d5c3-610">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6d5c3-611">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6d5c3-612">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="6d5c3-613">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6d5c3-614">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-614">Create new Triggers</span></span>
* <span data-ttu-id="6d5c3-615">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6d5c3-616">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-617">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-618">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6d5c3-619">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-621">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-622">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-623">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-624">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-625">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6d5c3-626">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6d5c3-627">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="6d5c3-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6d5c3-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-629">Az.Network</span></span>
* <span data-ttu-id="6d5c3-630">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6d5c3-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6d5c3-631">Az.PrivateDns</span></span>
* <span data-ttu-id="6d5c3-632">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-634">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6d5c3-635">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6d5c3-636">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6d5c3-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-637">Az.RedisCache</span></span>
* <span data-ttu-id="6d5c3-638">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6d5c3-639">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6d5c3-640">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-641">Az.Resources</span></span>
- <span data-ttu-id="6d5c3-642">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6d5c3-643">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="6d5c3-644">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6d5c3-645">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6d5c3-646">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-647">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-648">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6d5c3-649">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="6d5c3-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6d5c3-650">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6d5c3-651">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-651">General</span></span>
* <span data-ttu-id="6d5c3-652">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-653">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-654">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6d5c3-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-655">Az.Advisor</span></span>
* <span data-ttu-id="6d5c3-656">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6d5c3-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-657">Az.Batch</span></span>
* <span data-ttu-id="6d5c3-658">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6d5c3-659">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6d5c3-660">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6d5c3-661">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6d5c3-662">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6d5c3-663">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6d5c3-664">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6d5c3-665">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6d5c3-666">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6d5c3-667">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6d5c3-668">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6d5c3-669">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6d5c3-670">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6d5c3-671">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6d5c3-672">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6d5c3-673">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6d5c3-674">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6d5c3-675">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6d5c3-676">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6d5c3-677">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="6d5c3-678">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6d5c3-679">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6d5c3-680">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6d5c3-681">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="6d5c3-682">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6d5c3-683">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="6d5c3-684">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6d5c3-685">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6d5c3-686">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6d5c3-687">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6d5c3-688">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6d5c3-689">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6d5c3-690">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6d5c3-691">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6d5c3-692">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6d5c3-693">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-694">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-695">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6d5c3-696">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-697">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-698">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="6d5c3-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6d5c3-699">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6d5c3-700">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6d5c3-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6d5c3-701">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6d5c3-702">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6d5c3-703">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="6d5c3-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6d5c3-704">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6d5c3-705">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="6d5c3-705">Breaking changes</span></span>
    - <span data-ttu-id="6d5c3-706">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6d5c3-707">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-708">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-709">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-711">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="6d5c3-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6d5c3-712">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6d5c3-713">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="6d5c3-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6d5c3-714">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="6d5c3-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6d5c3-715">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6d5c3-716">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="6d5c3-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-717">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-718">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-719">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-720">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6d5c3-721">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6d5c3-722">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6d5c3-723">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6d5c3-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6d5c3-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6d5c3-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d5c3-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6d5c3-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d5c3-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6d5c3-729">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-730">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6d5c3-731">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6d5c3-732">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6d5c3-733">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6d5c3-734">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6d5c3-735">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6d5c3-736">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6d5c3-737">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6d5c3-738">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6d5c3-739">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6d5c3-740">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="6d5c3-741">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-742">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-743">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-743">Breaking changes:</span></span>
    - <span data-ttu-id="6d5c3-744">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6d5c3-745">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6d5c3-746">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6d5c3-747">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6d5c3-748">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6d5c3-749">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6d5c3-750">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6d5c3-751">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6d5c3-752">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6d5c3-753">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6d5c3-754">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6d5c3-755">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-757">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-758">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6d5c3-759">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6d5c3-760">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-761">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-762">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-763">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-764">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-765">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="6d5c3-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-766">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-767">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-768">Az.Network</span></span>
* <span data-ttu-id="6d5c3-769">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6d5c3-770">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6d5c3-776">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6d5c3-777">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-777">New cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6d5c3-779">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6d5c3-780">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6d5c3-781">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6d5c3-782">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6d5c3-783">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6d5c3-784">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6d5c3-785">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6d5c3-786">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-786">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6d5c3-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6d5c3-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6d5c3-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6d5c3-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6d5c3-792">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="6d5c3-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6d5c3-793">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6d5c3-794">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6d5c3-795">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6d5c3-796">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6d5c3-797">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6d5c3-798">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6d5c3-799">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-799">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6d5c3-801">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6d5c3-802">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6d5c3-803">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6d5c3-804">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6d5c3-805">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6d5c3-806">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6d5c3-807">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="6d5c3-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6d5c3-808">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-808">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6d5c3-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6d5c3-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6d5c3-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6d5c3-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6d5c3-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6d5c3-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6d5c3-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6d5c3-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6d5c3-815">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6d5c3-816">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6d5c3-817">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6d5c3-818">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="6d5c3-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6d5c3-819">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6d5c3-820">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6d5c3-821">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6d5c3-822">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6d5c3-823">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6d5c3-824">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6d5c3-825">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6d5c3-826">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-826">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="6d5c3-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6d5c3-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6d5c3-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-832">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-833">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-834">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6d5c3-835">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6d5c3-836">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6d5c3-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6d5c3-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6d5c3-839">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6d5c3-840">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6d5c3-841">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="6d5c3-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="6d5c3-842">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-843">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-844">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6d5c3-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6d5c3-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6d5c3-847">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="6d5c3-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6d5c3-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6d5c3-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6d5c3-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6d5c3-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="6d5c3-850">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6d5c3-851">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-851">General</span></span>
* <span data-ttu-id="6d5c3-852">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-853">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-854">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-855">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-856">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6d5c3-857">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="6d5c3-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-858">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-859">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6d5c3-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-860">Az.Batch</span></span>
* <span data-ttu-id="6d5c3-861">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-862">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-863">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6d5c3-864">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6d5c3-865">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="6d5c3-866">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-867">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-868">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6d5c3-869">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6d5c3-870">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-872">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="6d5c3-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6d5c3-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6d5c3-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="6d5c3-874">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6d5c3-875">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6d5c3-876">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="6d5c3-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6d5c3-877">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-878">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-879">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6d5c3-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6d5c3-880">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-881">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-882">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6d5c3-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6d5c3-883">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6d5c3-884">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="6d5c3-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6d5c3-885">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-886">Az.Network</span></span>
* <span data-ttu-id="6d5c3-887">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6d5c3-888">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6d5c3-889">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-889">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6d5c3-891">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6d5c3-892">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="6d5c3-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6d5c3-893">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="6d5c3-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6d5c3-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6d5c3-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6d5c3-897">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="6d5c3-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6d5c3-898">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6d5c3-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6d5c3-899">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6d5c3-900">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6d5c3-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-901">Az.RedisCache</span></span>
* <span data-ttu-id="6d5c3-902">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-903">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-904">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-905">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-906">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6d5c3-907">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="6d5c3-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6d5c3-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6d5c3-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6d5c3-909">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="6d5c3-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6d5c3-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6d5c3-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6d5c3-911">Az.StorageSync</span></span>
* <span data-ttu-id="6d5c3-912">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-913">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-914">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="6d5c3-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6d5c3-915">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-916">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-917">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6d5c3-918">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6d5c3-919">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-920">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-921">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6d5c3-922">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="6d5c3-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6d5c3-923">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-924">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-925">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6d5c3-926">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6d5c3-927">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6d5c3-928">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6d5c3-929">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6d5c3-930">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6d5c3-931">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6d5c3-932">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6d5c3-933">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-934">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-935">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6d5c3-936">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="6d5c3-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-937">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-938">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="6d5c3-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-939">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-940">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6d5c3-941">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6d5c3-942">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-942">New cmdlets are:</span></span>
    - <span data-ttu-id="6d5c3-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6d5c3-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6d5c3-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6d5c3-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-947">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-948">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6d5c3-949">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6d5c3-950">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6d5c3-951">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6d5c3-952">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6d5c3-953">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6d5c3-954">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6d5c3-955">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6d5c3-956">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6d5c3-957">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6d5c3-958">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6d5c3-959">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6d5c3-960">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6d5c3-961">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="6d5c3-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6d5c3-962">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="6d5c3-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6d5c3-963">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6d5c3-964">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6d5c3-965">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6d5c3-966">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6d5c3-967">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-967">Overall improved help files</span></span>
* <span data-ttu-id="6d5c3-968">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-969">Az.Network</span></span>
* <span data-ttu-id="6d5c3-970">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="6d5c3-971">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="6d5c3-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6d5c3-972">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6d5c3-973">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6d5c3-974">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="6d5c3-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6d5c3-975">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="6d5c3-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6d5c3-976">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6d5c3-977">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6d5c3-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6d5c3-978">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6d5c3-979">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6d5c3-980">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6d5c3-981">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6d5c3-982">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-982">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6d5c3-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6d5c3-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6d5c3-985">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-986">New-VpnSite</span></span>
        - <span data-ttu-id="6d5c3-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-987">Update-VpnSite</span></span>
        - <span data-ttu-id="6d5c3-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-988">New-VpnConnection</span></span>
        - <span data-ttu-id="6d5c3-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-989">Update-VpnConnection</span></span>
* <span data-ttu-id="6d5c3-990">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-992">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6d5c3-993">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="6d5c3-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-994">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-995">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-997">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6d5c3-998">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6d5c3-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6d5c3-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6d5c3-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6d5c3-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6d5c3-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6d5c3-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6d5c3-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6d5c3-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6d5c3-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6d5c3-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6d5c3-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6d5c3-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6d5c3-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6d5c3-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6d5c3-1012">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6d5c3-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1013">Az.SignalR</span></span>
* <span data-ttu-id="6d5c3-1014">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1015">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1016">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6d5c3-1017">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6d5c3-1018">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6d5c3-1019">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6d5c3-1020">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1021">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1022">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6d5c3-1023">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6d5c3-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6d5c3-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6d5c3-1026">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6d5c3-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6d5c3-1028">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6d5c3-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6d5c3-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6d5c3-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6d5c3-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1033">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1034">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6d5c3-1035">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6d5c3-1036">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6d5c3-1037">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6d5c3-1038">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1038">General</span></span>
* <span data-ttu-id="6d5c3-1039">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1040">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1041">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6d5c3-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1042">Az.Aks</span></span>
* <span data-ttu-id="6d5c3-1043">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6d5c3-1044">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-1046">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6d5c3-1047">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6d5c3-1048">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6d5c3-1049">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6d5c3-1050">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6d5c3-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1051">Az.Batch</span></span>
* <span data-ttu-id="6d5c3-1052">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1053">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-1054">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1055">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1056">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6d5c3-1057">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6d5c3-1058">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6d5c3-1059">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6d5c3-1060">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6d5c3-1061">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6d5c3-1062">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6d5c3-1063">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1064">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1065">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6d5c3-1066">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6d5c3-1067">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6d5c3-1068">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1070">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1071">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-1072">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6d5c3-1073">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6d5c3-1074">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6d5c3-1075">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6d5c3-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6d5c3-1077">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1078">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-1079">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1080">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1081">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6d5c3-1082">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6d5c3-1083">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6d5c3-1084">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6d5c3-1085">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="6d5c3-1086">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6d5c3-1087">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1089">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6d5c3-1090">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1090">Added example</span></span>
    - <span data-ttu-id="6d5c3-1091">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6d5c3-1092">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6d5c3-1093">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1095">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1096">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1097">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6d5c3-1098">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6d5c3-1099">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6d5c3-1100">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-1102">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6d5c3-1103">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6d5c3-1104">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-1106">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6d5c3-1107">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6d5c3-1108">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6d5c3-1109">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6d5c3-1110">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6d5c3-1111">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1112">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1113">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1114">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1115">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6d5c3-1116">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6d5c3-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6d5c3-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6d5c3-1119">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6d5c3-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1121">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1122">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6d5c3-1123">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1124">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1125">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6d5c3-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6d5c3-1127">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1128">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1129">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-1131">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1132">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1133">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6d5c3-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6d5c3-1135">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6d5c3-1136">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1137">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1138">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6d5c3-1139">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1140">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-1141">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6d5c3-1142">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1143">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-1144">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6d5c3-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1145">Az.LogicApp</span></span>
* <span data-ttu-id="6d5c3-1146">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6d5c3-1147">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6d5c3-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="6d5c3-1149">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1150">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1151">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6d5c3-1152">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1152">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6d5c3-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6d5c3-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6d5c3-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6d5c3-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6d5c3-1161">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6d5c3-1162">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6d5c3-1163">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6d5c3-1164">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6d5c3-1165">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6d5c3-1166">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6d5c3-1167">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6d5c3-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6d5c3-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6d5c3-1171">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6d5c3-1172">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6d5c3-1173">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6d5c3-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6d5c3-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6d5c3-1177">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6d5c3-1178">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6d5c3-1179">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1181">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="6d5c3-1182">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1184">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6d5c3-1185">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6d5c3-1186">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6d5c3-1187">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6d5c3-1188">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6d5c3-1189">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6d5c3-1190">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6d5c3-1191">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6d5c3-1192">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6d5c3-1193">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1194">Az.Resources</span></span>
- <span data-ttu-id="6d5c3-1195">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6d5c3-1196">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-1198">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6d5c3-1199">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1200">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1201">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6d5c3-1202">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6d5c3-1203">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1204">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1205">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6d5c3-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1206">Az.StorageSync</span></span>
* <span data-ttu-id="6d5c3-1207">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6d5c3-1208">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1209">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1210">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6d5c3-1211">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6d5c3-1212">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6d5c3-1213">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1214">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1215">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6d5c3-1216">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6d5c3-1217">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6d5c3-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1218">Az.Advisor</span></span>
* <span data-ttu-id="6d5c3-1219">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6d5c3-1220">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-1222">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6d5c3-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6d5c3-1224">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6d5c3-1225">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6d5c3-1226">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6d5c3-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6d5c3-1228">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1229">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1230">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1231">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1232">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1233">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1234">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6d5c3-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1235">Az.EventGrid</span></span>
* <span data-ttu-id="6d5c3-1236">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1237">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-1238">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1239">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1240">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6d5c3-1241">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-1243">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6d5c3-1244">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1246">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1248">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1249">Az.Resources</span></span>
    - <span data-ttu-id="6d5c3-1250">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6d5c3-1251">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6d5c3-1252">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6d5c3-1253">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-1255">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1256">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1257">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6d5c3-1258">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6d5c3-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6d5c3-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6d5c3-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6d5c3-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6d5c3-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6d5c3-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6d5c3-1265">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1266">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1267">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6d5c3-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6d5c3-1269">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6d5c3-1270">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6d5c3-1271">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6d5c3-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6d5c3-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6d5c3-1274">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6d5c3-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6d5c3-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6d5c3-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1277">Az.StorageSync</span></span>
* <span data-ttu-id="6d5c3-1278">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6d5c3-1279">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1280">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1281">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6d5c3-1282">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6d5c3-1283">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6d5c3-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6d5c3-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1286">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1287">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6d5c3-1288">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6d5c3-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1289">Az.Dns</span></span>
* <span data-ttu-id="6d5c3-1290">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6d5c3-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1291">Az.EventGrid</span></span>
* <span data-ttu-id="6d5c3-1292">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6d5c3-1293">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1293">New cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6d5c3-1295">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6d5c3-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6d5c3-1297">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6d5c3-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6d5c3-1299">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6d5c3-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6d5c3-1301">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6d5c3-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6d5c3-1303">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6d5c3-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6d5c3-1305">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6d5c3-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6d5c3-1307">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="6d5c3-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6d5c3-1309">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6d5c3-1310">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6d5c3-1312">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6d5c3-1313">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6d5c3-1314">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6d5c3-1315">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6d5c3-1316">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6d5c3-1317">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6d5c3-1318">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6d5c3-1319">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="6d5c3-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6d5c3-1321">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6d5c3-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6d5c3-1323">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6d5c3-1324">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6d5c3-1327">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6d5c3-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6d5c3-1329">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1330">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1331">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6d5c3-1332">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1332">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6d5c3-1334">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6d5c3-1335">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1335">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6d5c3-1337">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6d5c3-1338">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1338">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6d5c3-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6d5c3-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6d5c3-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6d5c3-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6d5c3-1344">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6d5c3-1345">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1345">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6d5c3-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6d5c3-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6d5c3-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6d5c3-1350">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6d5c3-1351">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6d5c3-1352">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6d5c3-1353">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6d5c3-1354">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6d5c3-1355">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6d5c3-1356">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6d5c3-1357">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6d5c3-1358">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6d5c3-1359">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6d5c3-1360">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6d5c3-1361">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6d5c3-1362">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6d5c3-1363">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6d5c3-1364">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-1365">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6d5c3-1366">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6d5c3-1367">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6d5c3-1368">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="6d5c3-1369">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="6d5c3-1370">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6d5c3-1371">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6d5c3-1372">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1374">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1375">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1376">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6d5c3-1377">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6d5c3-1378">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6d5c3-1379">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-1381">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1382">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1383">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6d5c3-1384">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6d5c3-1385">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6d5c3-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6d5c3-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6d5c3-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6d5c3-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6d5c3-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1391">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1392">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6d5c3-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="6d5c3-1394">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6d5c3-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1396">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1397">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6d5c3-1398">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6d5c3-1399">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6d5c3-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1400">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-1401">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1402">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1403">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6d5c3-1404">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1405">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-1406">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6d5c3-1407">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1408">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1409">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6d5c3-1410">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-1412">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1414">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-1416">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-1418">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6d5c3-1419">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1420">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1421">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6d5c3-1422">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6d5c3-1423">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6d5c3-1424">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1425">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1426">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6d5c3-1427">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-1429">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6d5c3-1430">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6d5c3-1431">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6d5c3-1432">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6d5c3-1433">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6d5c3-1434">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6d5c3-1435">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6d5c3-1436">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6d5c3-1437">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6d5c3-1438">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6d5c3-1439">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6d5c3-1440">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6d5c3-1441">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6d5c3-1442">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6d5c3-1443">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6d5c3-1444">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6d5c3-1445">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6d5c3-1446">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6d5c3-1447">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="6d5c3-1448">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6d5c3-1449">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6d5c3-1450">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6d5c3-1451">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6d5c3-1452">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="6d5c3-1453">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6d5c3-1454">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6d5c3-1455">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6d5c3-1456">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6d5c3-1457">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6d5c3-1458">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6d5c3-1459">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="6d5c3-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6d5c3-1461">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6d5c3-1462">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6d5c3-1463">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6d5c3-1464">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6d5c3-1465">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6d5c3-1466">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6d5c3-1467">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6d5c3-1468">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6d5c3-1469">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6d5c3-1470">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6d5c3-1471">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6d5c3-1472">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6d5c3-1473">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6d5c3-1474">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6d5c3-1475">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6d5c3-1476">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6d5c3-1477">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6d5c3-1478">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6d5c3-1479">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6d5c3-1480">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6d5c3-1481">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6d5c3-1482">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6d5c3-1483">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6d5c3-1484">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6d5c3-1485">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6d5c3-1486">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6d5c3-1487">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6d5c3-1488">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6d5c3-1489">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6d5c3-1490">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6d5c3-1491">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6d5c3-1492">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6d5c3-1493">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6d5c3-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6d5c3-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6d5c3-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6d5c3-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6d5c3-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6d5c3-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6d5c3-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6d5c3-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6d5c3-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6d5c3-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="6d5c3-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6d5c3-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1506">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1507">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6d5c3-1508">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6d5c3-1509">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6d5c3-1510">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6d5c3-1511">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6d5c3-1512">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6d5c3-1513">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1514">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1515">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6d5c3-1516">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1518">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1519">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-1520">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1521">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1522">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6d5c3-1523">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="6d5c3-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6d5c3-1525">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1526">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1527">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1528">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1529">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6d5c3-1530">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1531">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1532">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-1534">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6d5c3-1535">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1536">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1537">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6d5c3-1538">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6d5c3-1539">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6d5c3-1540">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6d5c3-1541">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6d5c3-1542">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="6d5c3-1543">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1543">Breaking changes</span></span>
    - <span data-ttu-id="6d5c3-1544">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6d5c3-1545">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6d5c3-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="6d5c3-1547">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6d5c3-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1548">Az.Dns</span></span>
* <span data-ttu-id="6d5c3-1549">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6d5c3-1550">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6d5c3-1551">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="6d5c3-1553">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6d5c3-1554">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1555">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-1556">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6d5c3-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6d5c3-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6d5c3-1559">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6d5c3-1560">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6d5c3-1561">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6d5c3-1562">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1563">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-1564">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="6d5c3-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6d5c3-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6d5c3-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6d5c3-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6d5c3-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6d5c3-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6d5c3-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6d5c3-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6d5c3-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6d5c3-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6d5c3-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6d5c3-1576">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6d5c3-1577">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1578">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1579">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6d5c3-1580">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1580">New cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="6d5c3-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6d5c3-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6d5c3-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6d5c3-1585">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="6d5c3-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6d5c3-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6d5c3-1588">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6d5c3-1589">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6d5c3-1590">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-1592">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6d5c3-1593">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6d5c3-1594">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1596">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6d5c3-1597">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6d5c3-1598">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6d5c3-1599">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6d5c3-1600">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6d5c3-1601">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6d5c3-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1602">Az.Relay</span></span>
* <span data-ttu-id="6d5c3-1603">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-1605">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1606">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1607">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6d5c3-1608">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6d5c3-1609">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6d5c3-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="6d5c3-1611">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6d5c3-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6d5c3-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6d5c3-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1615">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1616">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6d5c3-1617">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6d5c3-1618">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-1619">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-1620">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="6d5c3-1621">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6d5c3-1622">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6d5c3-1623">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6d5c3-1624">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6d5c3-1625">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1626">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1627">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1628">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6d5c3-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1629">Az.Batch</span></span>
* <span data-ttu-id="6d5c3-1630">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1631">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-1632">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-1634">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1635">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1636">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6d5c3-1637">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1638">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1639">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1640">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1642">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6d5c3-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1643">Az.EventGrid</span></span>
* <span data-ttu-id="6d5c3-1644">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1645">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-1646">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6d5c3-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1647">Az.HDInsight</span></span>
* <span data-ttu-id="6d5c3-1648">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1649">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-1650">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1651">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-1652">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1653">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6d5c3-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="6d5c3-1655">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6d5c3-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1656">Az.Media</span></span>
* <span data-ttu-id="6d5c3-1657">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1658">Az.Monitor</span></span>
  * <span data-ttu-id="6d5c3-1659">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6d5c3-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6d5c3-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6d5c3-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6d5c3-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6d5c3-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6d5c3-1665">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1666">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1667">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1668">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6d5c3-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="6d5c3-1670">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1672">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6d5c3-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6d5c3-1674">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1676">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1677">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6d5c3-1678">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6d5c3-1679">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6d5c3-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1680">Az.RedisCache</span></span>
* <span data-ttu-id="6d5c3-1681">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1682">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1683">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1684">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1685">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6d5c3-1686">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1687">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6d5c3-1688">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6d5c3-1689">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6d5c3-1690">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6d5c3-1691">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1692">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1693">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6d5c3-1694">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6d5c3-1695">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6d5c3-1696">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6d5c3-1697">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-1698">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-1699">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="6d5c3-1700">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6d5c3-1701">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6d5c3-1702">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6d5c3-1703">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6d5c3-1704">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1705">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1706">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1707">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6d5c3-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="6d5c3-1709">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6d5c3-1710">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1711">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1712">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6d5c3-1713">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6d5c3-1714">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1715">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1716">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6d5c3-1717">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6d5c3-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="6d5c3-1719">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1720">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1721">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6d5c3-1722">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1723">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1724">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6d5c3-1725">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6d5c3-1726">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6d5c3-1727">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6d5c3-1728">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6d5c3-1729">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1730">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1731">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1732">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1733">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6d5c3-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="6d5c3-1735">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6d5c3-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6d5c3-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6d5c3-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6d5c3-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6d5c3-1740">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6d5c3-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6d5c3-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6d5c3-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6d5c3-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6d5c3-1745">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6d5c3-1746">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="6d5c3-1747">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="6d5c3-1748">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6d5c3-1749">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6d5c3-1750">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6d5c3-1751">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6d5c3-1752">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1753">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1754">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1755">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6d5c3-1756">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="6d5c3-1757">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1757">Pre-Post script</span></span>
    * <span data-ttu-id="6d5c3-1758">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1759">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1760">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6d5c3-1761">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1762">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-1763">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1764">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1765">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6d5c3-1766">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1768">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6d5c3-1769">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1770">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1771">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6d5c3-1772">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1773">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1774">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1775">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1776">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6d5c3-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6d5c3-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6d5c3-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6d5c3-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6d5c3-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6d5c3-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1783">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1784">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="6d5c3-1785">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1786">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1787">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6d5c3-1788">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1789">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1790">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6d5c3-1791">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6d5c3-1792">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1793">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-1794">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1795">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1796">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1797">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1798">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6d5c3-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1799">Az.LogicApp</span></span>
* <span data-ttu-id="6d5c3-1800">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1801">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1802">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1804">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6d5c3-1805">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1805">SDK Update</span></span>
* <span data-ttu-id="6d5c3-1806">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6d5c3-1807">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1808">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1809">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6d5c3-1810">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6d5c3-1811">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6d5c3-1812">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6d5c3-1813">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6d5c3-1814">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1815">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1816">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6d5c3-1817">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1818">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1819">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6d5c3-1820">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6d5c3-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="6d5c3-1822">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1823">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1824">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6d5c3-1825">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6d5c3-1826">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-1828">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1829">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1830">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6d5c3-1831">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6d5c3-1832">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6d5c3-1833">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1835">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6d5c3-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1836">Az.EventHub</span></span>
* <span data-ttu-id="6d5c3-1837">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1838">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-1839">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6d5c3-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1840">Az.LogicApp</span></span>
* <span data-ttu-id="6d5c3-1841">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6d5c3-1842">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6d5c3-1843">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6d5c3-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6d5c3-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6d5c3-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6d5c3-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6d5c3-1848">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6d5c3-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6d5c3-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6d5c3-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6d5c3-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6d5c3-1853">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6d5c3-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1854">Az.Monitor</span></span>
* <span data-ttu-id="6d5c3-1855">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1856">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1857">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="6d5c3-1859">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6d5c3-1860">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="6d5c3-1861">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1862">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1863">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6d5c3-1864">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6d5c3-1865">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6d5c3-1866">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1867">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1868">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6d5c3-1869">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1870">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1871">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6d5c3-1872">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1873">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1874">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6d5c3-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="6d5c3-1876">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1877">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1878">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6d5c3-1879">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6d5c3-1880">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="6d5c3-1882">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1883">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1884">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="6d5c3-1885">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6d5c3-1886">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="6d5c3-1887">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1888">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1889">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6d5c3-1890">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6d5c3-1891">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6d5c3-1892">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1893">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1894">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6d5c3-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="6d5c3-1896">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="6d5c3-1898">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6d5c3-1899">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1900">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1901">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6d5c3-1902">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6d5c3-1903">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6d5c3-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1904">Az.Aks</span></span>
* <span data-ttu-id="6d5c3-1905">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6d5c3-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1906">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-1907">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6d5c3-1908">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6d5c3-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1909">Az.Cdn</span></span>
* <span data-ttu-id="6d5c3-1910">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1911">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1912">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6d5c3-1913">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6d5c3-1914">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6d5c3-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6d5c3-1916">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6d5c3-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1917">Az.DataFactory</span></span>
* <span data-ttu-id="6d5c3-1918">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1920">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6d5c3-1921">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6d5c3-1922">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1923">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-1924">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1925">Az.KeyVault</span></span>
* <span data-ttu-id="6d5c3-1926">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1927">Az.Network</span></span>
* <span data-ttu-id="6d5c3-1928">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1929">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1930">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6d5c3-1931">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6d5c3-1932">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6d5c3-1933">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6d5c3-1934">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6d5c3-1935">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6d5c3-1936">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-1938">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6d5c3-1939">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1939">Fix some error messages.</span></span>
* <span data-ttu-id="6d5c3-1940">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6d5c3-1941">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6d5c3-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1942">Az.SignalR</span></span>
* <span data-ttu-id="6d5c3-1943">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1944">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1945">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6d5c3-1946">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6d5c3-1947">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6d5c3-1948">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1949">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1950">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6d5c3-1951">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6d5c3-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6d5c3-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6d5c3-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="6d5c3-1955">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1956">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-1957">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6d5c3-1958">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6d5c3-1959">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6d5c3-1960">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6d5c3-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1961">Az.Accounts</span></span>
* <span data-ttu-id="6d5c3-1962">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1963">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-1964">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6d5c3-1965">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6d5c3-1966">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-1968">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6d5c3-1969">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6d5c3-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1970">Az.EventGrid</span></span>
* <span data-ttu-id="6d5c3-1971">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6d5c3-1972">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6d5c3-1973">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6d5c3-1974">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6d5c3-1975">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6d5c3-1976">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6d5c3-1977">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6d5c3-1978">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6d5c3-1979">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6d5c3-1980">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="6d5c3-1981">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6d5c3-1982">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6d5c3-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1983">Az.IotHub</span></span>
* <span data-ttu-id="6d5c3-1984">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6d5c3-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1985">Az.LogicApp</span></span>
* <span data-ttu-id="6d5c3-1986">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1987">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-1988">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6d5c3-1989">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6d5c3-1990">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6d5c3-1991">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6d5c3-1992">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6d5c3-1993">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6d5c3-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1994">Az.SignalR</span></span>
* <span data-ttu-id="6d5c3-1995">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1996">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-1997">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6d5c3-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1998">Az.Storage</span></span>
* <span data-ttu-id="6d5c3-1999">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="6d5c3-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6d5c3-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="6d5c3-2001">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6d5c3-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2003">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-2004">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6d5c3-2005">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6d5c3-2006">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6d5c3-2007">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2007">General</span></span>

- <span data-ttu-id="6d5c3-2008">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="6d5c3-2009">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2009">Online help for each module</span></span>
- <span data-ttu-id="6d5c3-2010">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6d5c3-2011">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6d5c3-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2012">Az.Accounts</span></span>
- <span data-ttu-id="6d5c3-2013">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="6d5c3-2014">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="6d5c3-2016">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2016">Fixes for #7002</span></span>
- <span data-ttu-id="6d5c3-2017">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6d5c3-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2018">Az.Batch</span></span>
- <span data-ttu-id="6d5c3-2019">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6d5c3-2020">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6d5c3-2021">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6d5c3-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2022">Az.Billing</span></span>
- <span data-ttu-id="6d5c3-2023">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6d5c3-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="6d5c3-2025">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6d5c3-2026">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6d5c3-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="6d5c3-2028">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6d5c3-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6d5c3-2030">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="6d5c3-2032">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6d5c3-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2033">Az.Monitor</span></span>
- <span data-ttu-id="6d5c3-2034">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6d5c3-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2035">Az.KeyVault</span></span>
- <span data-ttu-id="6d5c3-2036">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6d5c3-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="6d5c3-2038">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6d5c3-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2039">Az.Media</span></span>
- <span data-ttu-id="6d5c3-2040">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6d5c3-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2041">Az.Network</span></span>
<span data-ttu-id="6d5c3-2042">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6d5c3-2043">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="6d5c3-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6d5c3-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6d5c3-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6d5c3-2052">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6d5c3-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6d5c3-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6d5c3-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6d5c3-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6d5c3-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6d5c3-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6d5c3-2059">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6d5c3-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6d5c3-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6d5c3-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6d5c3-2063">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6d5c3-2064">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6d5c3-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="6d5c3-2066">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6d5c3-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2067">Az.Profile</span></span>
- <span data-ttu-id="6d5c3-2068">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="6d5c3-2070">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6d5c3-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2071">Az.Resources</span></span>
- <span data-ttu-id="6d5c3-2072">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="6d5c3-2074">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6d5c3-2075">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6d5c3-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="6d5c3-2077">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6d5c3-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2078">Az.Sql</span></span>
- <span data-ttu-id="6d5c3-2079">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6d5c3-2080">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6d5c3-2081">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6d5c3-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2082">Az.Storage</span></span>
- <span data-ttu-id="6d5c3-2083">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6d5c3-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2084">Az.Websites</span></span>
- <span data-ttu-id="6d5c3-2085">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6d5c3-2086">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6d5c3-2087">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2087">General</span></span>

* <span data-ttu-id="6d5c3-2088">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6d5c3-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2089">Az.Compute</span></span>

* <span data-ttu-id="6d5c3-2090">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="6d5c3-2092">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6d5c3-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="6d5c3-2094">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="6d5c3-2095">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6d5c3-2096">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6d5c3-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="6d5c3-2098">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6d5c3-2099">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6d5c3-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2100">Az.Resources</span></span>

* <span data-ttu-id="6d5c3-2101">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6d5c3-2102">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6d5c3-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2103">Az.Sql</span></span>

* <span data-ttu-id="6d5c3-2104">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6d5c3-2105">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6d5c3-2106">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6d5c3-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2107">Az.Storage</span></span>

* <span data-ttu-id="6d5c3-2108">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6d5c3-2109">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6d5c3-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6d5c3-2111">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="6d5c3-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6d5c3-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6d5c3-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2114">Az.Websites</span></span>

* <span data-ttu-id="6d5c3-2115">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="6d5c3-2116">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6d5c3-2117">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6d5c3-2118">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6d5c3-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="6d5c3-2120">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6d5c3-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2121">Az.Automation</span></span>
* <span data-ttu-id="6d5c3-2122">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6d5c3-2123">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6d5c3-2124">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6d5c3-2125">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6d5c3-2126">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6d5c3-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2127">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-2128">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6d5c3-2129">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6d5c3-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="6d5c3-2131">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6d5c3-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6d5c3-2133">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6d5c3-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2134">Az.Network</span></span>
* <span data-ttu-id="6d5c3-2135">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6d5c3-2136">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6d5c3-2137">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="6d5c3-2138">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6d5c3-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6d5c3-2140">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6d5c3-2141">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6d5c3-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6d5c3-2143">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6d5c3-2144">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6d5c3-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2145">Az.Relay</span></span>
* <span data-ttu-id="6d5c3-2146">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6d5c3-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2147">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-2148">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6d5c3-2149">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6d5c3-2150">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-2152">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6d5c3-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2153">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-2154">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6d5c3-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6d5c3-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6d5c3-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6d5c3-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6d5c3-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6d5c3-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6d5c3-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6d5c3-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6d5c3-2163">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6d5c3-2164">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6d5c3-2165">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6d5c3-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6d5c3-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6d5c3-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6d5c3-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6d5c3-2170">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6d5c3-2171">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6d5c3-2172">Geral</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2172">General</span></span>
* <span data-ttu-id="6d5c3-2173">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6d5c3-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2174">Az.Profile</span></span>
* <span data-ttu-id="6d5c3-2175">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6d5c3-2176">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6d5c3-2177">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6d5c3-2178">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6d5c3-2179">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6d5c3-2180">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6d5c3-2181">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-2183">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2184">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-2185">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6d5c3-2186">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6d5c3-2187">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-2189">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6d5c3-2190">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6d5c3-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2191">Az.Insights</span></span>
* <span data-ttu-id="6d5c3-2192">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6d5c3-2193">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6d5c3-2194">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6d5c3-2195">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2196">Az.Network</span></span>
* <span data-ttu-id="6d5c3-2197">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6d5c3-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6d5c3-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6d5c3-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6d5c3-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6d5c3-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6d5c3-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6d5c3-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="6d5c3-2205">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2206">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-2207">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6d5c3-2208">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6d5c3-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="6d5c3-2210">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6d5c3-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="6d5c3-2212">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6d5c3-2213">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6d5c3-2214">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6d5c3-2215">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6d5c3-2216">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6d5c3-2217">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6d5c3-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2218">Az.Profile</span></span>
* <span data-ttu-id="6d5c3-2219">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6d5c3-2220">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2221">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-2222">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6d5c3-2223">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6d5c3-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="6d5c3-2225">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6d5c3-2226">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6d5c3-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6d5c3-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6d5c3-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2230">Az.Network</span></span>
* <span data-ttu-id="6d5c3-2231">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6d5c3-2232">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2233">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-2234">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6d5c3-2235">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6d5c3-2236">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6d5c3-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2237">Azure.Storage</span></span>
* <span data-ttu-id="6d5c3-2238">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6d5c3-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6d5c3-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6d5c3-2241">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6d5c3-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6d5c3-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="6d5c3-2244">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6d5c3-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2245">Az.Compute</span></span>
* <span data-ttu-id="6d5c3-2246">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6d5c3-2247">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6d5c3-2248">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6d5c3-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6d5c3-2250">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6d5c3-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2251">Az.Network</span></span>
* <span data-ttu-id="6d5c3-2252">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6d5c3-2253">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2253">new cmdlets added</span></span>
    - <span data-ttu-id="6d5c3-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6d5c3-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6d5c3-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6d5c3-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6d5c3-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6d5c3-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6d5c3-2260">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6d5c3-2261">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6d5c3-2262">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6d5c3-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2263">Az.RedisCache</span></span>
* <span data-ttu-id="6d5c3-2264">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6d5c3-2265">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6d5c3-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2266">Az.Resources</span></span>
* <span data-ttu-id="6d5c3-2267">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6d5c3-2268">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6d5c3-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2269">Az.Sql</span></span>
* <span data-ttu-id="6d5c3-2270">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6d5c3-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2271">Az.Websites</span></span>
* <span data-ttu-id="6d5c3-2272">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6d5c3-2273">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6d5c3-2274">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6d5c3-2275">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="6d5c3-2275">Initial Release</span></span>
