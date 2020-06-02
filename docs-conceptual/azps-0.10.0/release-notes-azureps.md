---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9dd733865ba8235eed6dcef4637a63ad93999338
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121923"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="39d7f-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="39d7f-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="39d7f-104">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="39d7f-105">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-105">General</span></span>
* <span data-ttu-id="39d7f-106">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="39d7f-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="39d7f-107">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="39d7f-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="39d7f-108">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="39d7f-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="39d7f-109">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="39d7f-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="39d7f-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="39d7f-110">Az.Billing</span></span>
  - <span data-ttu-id="39d7f-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-111">Az.Compute</span></span>
  - <span data-ttu-id="39d7f-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39d7f-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="39d7f-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-113">Az.EventHub</span></span>
  - <span data-ttu-id="39d7f-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-114">Az.IotHub</span></span>
  - <span data-ttu-id="39d7f-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-115">Az.KeyVault</span></span>
  - <span data-ttu-id="39d7f-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-116">Az.Monitor</span></span>
  - <span data-ttu-id="39d7f-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-117">Az.Network</span></span>
  - <span data-ttu-id="39d7f-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-118">Az.Resources</span></span>
  - <span data-ttu-id="39d7f-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-119">Az.Storage</span></span>
  - <span data-ttu-id="39d7f-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-120">Az.Websites</span></span>
* <span data-ttu-id="39d7f-121">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="39d7f-122">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="39d7f-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="39d7f-123">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="39d7f-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-124">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-125">Atualização da ADAL para a MSAL</span><span class="sxs-lookup"><span data-stu-id="39d7f-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="39d7f-126">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-127">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-128">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="39d7f-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-129">Az.Compute</span></span>
* <span data-ttu-id="39d7f-130">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="39d7f-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="39d7f-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="39d7f-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="39d7f-132">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="39d7f-133">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="39d7f-134">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="39d7f-134">[#11354]</span></span>
* <span data-ttu-id="39d7f-135">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="39d7f-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="39d7f-136">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39d7f-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39d7f-137">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39d7f-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39d7f-138">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39d7f-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39d7f-139">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39d7f-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="39d7f-140">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="39d7f-141">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="39d7f-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="39d7f-142">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="39d7f-143">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="39d7f-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-144">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-145">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="39d7f-146">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="39d7f-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-148">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="39d7f-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="39d7f-149">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="39d7f-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-150">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-151">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="39d7f-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-152">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-153">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39d7f-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="39d7f-154">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-155">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="39d7f-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="39d7f-156">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="39d7f-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-157">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-158">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="39d7f-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-159">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-160">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="39d7f-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-161">Az.Network</span></span>
* <span data-ttu-id="39d7f-162">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="39d7f-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="39d7f-163">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="39d7f-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="39d7f-164">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="39d7f-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="39d7f-165">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="39d7f-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="39d7f-166">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="39d7f-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="39d7f-167">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="39d7f-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-169">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="39d7f-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-171">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="39d7f-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="39d7f-172">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="39d7f-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="39d7f-173">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="39d7f-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="39d7f-174">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="39d7f-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="39d7f-175">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="39d7f-176">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-177">Az.Resources</span></span>
* <span data-ttu-id="39d7f-178">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="39d7f-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="39d7f-179">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="39d7f-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="39d7f-180">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="39d7f-181">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-181">Added example.</span></span>
* <span data-ttu-id="39d7f-182">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="39d7f-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="39d7f-183">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="39d7f-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-184">Az.Sql</span></span>
* <span data-ttu-id="39d7f-185">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="39d7f-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="39d7f-186">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="39d7f-187">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="39d7f-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="39d7f-188">Az.Support</span></span>
* <span data-ttu-id="39d7f-189">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="39d7f-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-190">Az.Websites</span></span>
* <span data-ttu-id="39d7f-191">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="39d7f-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="39d7f-192">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39d7f-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39d7f-193">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39d7f-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39d7f-194">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39d7f-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39d7f-195">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39d7f-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="39d7f-196">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-197">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-198">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="39d7f-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="39d7f-199">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="39d7f-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="39d7f-200">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="39d7f-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-201">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-202">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="39d7f-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="39d7f-203">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="39d7f-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="39d7f-204">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="39d7f-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="39d7f-205">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="39d7f-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-207">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="39d7f-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-208">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-209">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="39d7f-210">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-211">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-212">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-213">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-214">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="39d7f-215">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="39d7f-216">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-217">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39d7f-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="39d7f-218">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39d7f-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="39d7f-219">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39d7f-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="39d7f-220">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39d7f-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="39d7f-221">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="39d7f-222">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="39d7f-223">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="39d7f-224">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-225">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="39d7f-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="39d7f-226">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="39d7f-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="39d7f-227">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39d7f-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-228">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-229">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="39d7f-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-230">Az.Network</span></span>
* <span data-ttu-id="39d7f-231">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="39d7f-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="39d7f-232">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="39d7f-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="39d7f-233">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="39d7f-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="39d7f-234">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-235">Az.Resources</span></span>
* <span data-ttu-id="39d7f-236">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="39d7f-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="39d7f-237">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="39d7f-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="39d7f-238">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="39d7f-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="39d7f-239">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="39d7f-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="39d7f-240">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="39d7f-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="39d7f-241">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="39d7f-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="39d7f-242">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="39d7f-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="39d7f-243">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="39d7f-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="39d7f-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="39d7f-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="39d7f-247">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="39d7f-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="39d7f-249">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-250">Az.Sql</span></span>
* <span data-ttu-id="39d7f-251">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="39d7f-252">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="39d7f-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="39d7f-253">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="39d7f-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="39d7f-254">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="39d7f-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="39d7f-255">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="39d7f-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="39d7f-256">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="39d7f-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="39d7f-257">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="39d7f-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="39d7f-258">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="39d7f-259">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-260">Az.Storage</span></span>
* <span data-ttu-id="39d7f-261">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="39d7f-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="39d7f-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="39d7f-263">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="39d7f-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="39d7f-264">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="39d7f-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="39d7f-265">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="39d7f-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-266">Az.Websites</span></span>
* <span data-ttu-id="39d7f-267">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="39d7f-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="39d7f-268">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="39d7f-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="39d7f-269">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="39d7f-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="39d7f-270">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="39d7f-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="39d7f-271">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="39d7f-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="39d7f-272">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-273">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-273">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-274">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="39d7f-275">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="39d7f-276">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="39d7f-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-277">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-278">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="39d7f-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-279">Az.Automation</span></span>
* <span data-ttu-id="39d7f-280">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39d7f-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-282">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="39d7f-283">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="39d7f-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-284">Az.Compute</span></span>
* <span data-ttu-id="39d7f-285">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="39d7f-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-286">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-287">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="39d7f-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-288">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-289">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="39d7f-290">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-291">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-292">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-293">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39d7f-294">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39d7f-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-295">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-296">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="39d7f-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-297">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-298">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="39d7f-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="39d7f-299">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="39d7f-300">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="39d7f-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-301">Az.Network</span></span>
* <span data-ttu-id="39d7f-302">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="39d7f-303">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="39d7f-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="39d7f-304">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="39d7f-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="39d7f-305">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="39d7f-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="39d7f-306">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-306">No new cmdlets are added.</span></span> <span data-ttu-id="39d7f-307">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="39d7f-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-309">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="39d7f-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-310">Az.Resources</span></span>
* <span data-ttu-id="39d7f-311">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="39d7f-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="39d7f-312">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39d7f-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="39d7f-313">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="39d7f-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="39d7f-314">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="39d7f-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="39d7f-315">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="39d7f-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="39d7f-316">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="39d7f-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="39d7f-317">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="39d7f-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="39d7f-318">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-319">Az.Sql</span></span>
* <span data-ttu-id="39d7f-320">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="39d7f-321">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="39d7f-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="39d7f-322">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="39d7f-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="39d7f-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39d7f-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="39d7f-324">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="39d7f-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39d7f-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39d7f-325">Az.StorageSync</span></span>
* <span data-ttu-id="39d7f-326">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="39d7f-327">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-328">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-328">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-329">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39d7f-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="39d7f-330">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-331">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-332">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="39d7f-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="39d7f-333">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="39d7f-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-334">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-335">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="39d7f-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="39d7f-336">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="39d7f-336">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="39d7f-337">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="39d7f-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="39d7f-338">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="39d7f-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-339">Az.Compute</span></span>
* <span data-ttu-id="39d7f-340">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="39d7f-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="39d7f-341">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="39d7f-342">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="39d7f-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="39d7f-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="39d7f-344">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="39d7f-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-345">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-346">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="39d7f-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="39d7f-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="39d7f-348">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="39d7f-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="39d7f-349">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="39d7f-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-350">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-351">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="39d7f-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-352">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-353">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="39d7f-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-354">Az.Network</span></span>
* <span data-ttu-id="39d7f-355">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="39d7f-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="39d7f-356">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="39d7f-357">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="39d7f-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="39d7f-358">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="39d7f-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="39d7f-359">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="39d7f-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="39d7f-360">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="39d7f-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="39d7f-361">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="39d7f-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="39d7f-362">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="39d7f-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="39d7f-363">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-363">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="39d7f-365">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="39d7f-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="39d7f-367">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="39d7f-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-369">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="39d7f-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="39d7f-370">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="39d7f-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="39d7f-371">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="39d7f-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="39d7f-372">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="39d7f-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-374">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="39d7f-375">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="39d7f-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-376">Az.Resources</span></span>
* <span data-ttu-id="39d7f-377">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="39d7f-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="39d7f-378">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="39d7f-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-379">Az.Sql</span></span>
<span data-ttu-id="39d7f-380">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="39d7f-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-381">Az.Storage</span></span>
* <span data-ttu-id="39d7f-382">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="39d7f-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="39d7f-384">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="39d7f-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="39d7f-385">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-386">Az.Websites</span></span>
* <span data-ttu-id="39d7f-387">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="39d7f-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="39d7f-388">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="39d7f-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="39d7f-389">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="39d7f-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-390">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-391">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="39d7f-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-392">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-393">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-394">Az.Compute</span></span>
* <span data-ttu-id="39d7f-395">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="39d7f-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="39d7f-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="39d7f-397">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="39d7f-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39d7f-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="39d7f-399">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39d7f-400">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="39d7f-401">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39d7f-402">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="39d7f-403">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39d7f-404">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="39d7f-405">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39d7f-406">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="39d7f-407">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39d7f-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39d7f-408">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="39d7f-409">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39d7f-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39d7f-410">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="39d7f-411">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39d7f-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39d7f-412">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="39d7f-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="39d7f-413">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="39d7f-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="39d7f-414">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="39d7f-415">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="39d7f-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="39d7f-416">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="39d7f-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-417">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-418">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39d7f-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="39d7f-419">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="39d7f-420">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="39d7f-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="39d7f-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="39d7f-422">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="39d7f-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-423">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-424">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="39d7f-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-425">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-426">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="39d7f-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="39d7f-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39d7f-427">Az.MachineLearning</span></span>
* <span data-ttu-id="39d7f-428">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="39d7f-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="39d7f-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39d7f-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="39d7f-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="39d7f-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39d7f-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="39d7f-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39d7f-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="39d7f-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39d7f-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="39d7f-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="39d7f-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="39d7f-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="39d7f-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-436">Az.Network</span></span>
* <span data-ttu-id="39d7f-437">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="39d7f-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-439">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="39d7f-440">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="39d7f-441">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="39d7f-442">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-443">Az.Resources</span></span>
* <span data-ttu-id="39d7f-444">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-445">Az.Sql</span></span>
* <span data-ttu-id="39d7f-446">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="39d7f-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="39d7f-447">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="39d7f-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="39d7f-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39d7f-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="39d7f-449">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="39d7f-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-450">Az.Storage</span></span>
* <span data-ttu-id="39d7f-451">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="39d7f-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="39d7f-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="39d7f-453">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="39d7f-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="39d7f-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="39d7f-455">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="39d7f-456">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-456">General</span></span>
* <span data-ttu-id="39d7f-457">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="39d7f-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-458">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-459">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="39d7f-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="39d7f-460">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="39d7f-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39d7f-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-461">Az.Batch</span></span>
* <span data-ttu-id="39d7f-462">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="39d7f-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-463">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-464">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-465">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-466">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="39d7f-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="39d7f-467">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="39d7f-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="39d7f-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="39d7f-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="39d7f-469">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="39d7f-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-470">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-471">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="39d7f-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="39d7f-472">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="39d7f-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="39d7f-473">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="39d7f-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-474">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-475">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="39d7f-476">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="39d7f-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="39d7f-477">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="39d7f-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-478">Az.Network</span></span>
* <span data-ttu-id="39d7f-479">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="39d7f-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-480">Az.Resources</span></span>
* <span data-ttu-id="39d7f-481">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="39d7f-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="39d7f-482">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-483">Az.Sql</span></span>
* <span data-ttu-id="39d7f-484">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="39d7f-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-485">Az.Storage</span></span>
* <span data-ttu-id="39d7f-486">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="39d7f-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="39d7f-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="39d7f-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="39d7f-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="39d7f-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="39d7f-489">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="39d7f-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="39d7f-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="39d7f-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="39d7f-491">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="39d7f-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="39d7f-492">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="39d7f-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="39d7f-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="39d7f-495">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="39d7f-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="39d7f-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="39d7f-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="39d7f-497">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="39d7f-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="39d7f-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="39d7f-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="39d7f-499">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-500">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-500">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-501">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="39d7f-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="39d7f-502">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="39d7f-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-503">Az.Compute</span></span>
* <span data-ttu-id="39d7f-504">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="39d7f-504">VM Reapply feature</span></span>
    - <span data-ttu-id="39d7f-505">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="39d7f-506">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="39d7f-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="39d7f-507">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="39d7f-508">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="39d7f-509">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="39d7f-510">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="39d7f-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="39d7f-511">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="39d7f-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="39d7f-512">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="39d7f-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="39d7f-513">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="39d7f-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="39d7f-514">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="39d7f-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39d7f-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="39d7f-516">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39d7f-517">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="39d7f-517">Get the Order</span></span>
* <span data-ttu-id="39d7f-518">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39d7f-519">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="39d7f-519">Create new Order</span></span>
* <span data-ttu-id="39d7f-520">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39d7f-521">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="39d7f-521">Remove the Order</span></span>
* <span data-ttu-id="39d7f-522">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="39d7f-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="39d7f-523">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="39d7f-523">Now creates Local Share</span></span>
* <span data-ttu-id="39d7f-524">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="39d7f-525">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="39d7f-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="39d7f-526">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="39d7f-527">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="39d7f-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="39d7f-528">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39d7f-529">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="39d7f-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="39d7f-530">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39d7f-531">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="39d7f-531">Create new Triggers</span></span>
* <span data-ttu-id="39d7f-532">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39d7f-533">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="39d7f-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-534">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-535">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="39d7f-536">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-538">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="39d7f-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-539">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-540">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="39d7f-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-541">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-542">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="39d7f-543">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="39d7f-544">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="39d7f-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="39d7f-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-546">Az.Network</span></span>
* <span data-ttu-id="39d7f-547">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="39d7f-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="39d7f-548">Az.PrivateDns</span></span>
* <span data-ttu-id="39d7f-549">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-551">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="39d7f-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="39d7f-552">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="39d7f-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="39d7f-553">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39d7f-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39d7f-554">Az.RedisCache</span></span>
* <span data-ttu-id="39d7f-555">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="39d7f-556">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="39d7f-557">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="39d7f-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-558">Az.Resources</span></span>
- <span data-ttu-id="39d7f-559">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="39d7f-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="39d7f-560">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="39d7f-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="39d7f-561">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="39d7f-562">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="39d7f-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="39d7f-563">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-564">Az.Sql</span></span>
* <span data-ttu-id="39d7f-565">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="39d7f-566">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="39d7f-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="39d7f-567">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="39d7f-568">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-568">General</span></span>
* <span data-ttu-id="39d7f-569">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="39d7f-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-570">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-571">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="39d7f-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39d7f-572">Az.Advisor</span></span>
* <span data-ttu-id="39d7f-573">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d7f-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39d7f-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-574">Az.Batch</span></span>
* <span data-ttu-id="39d7f-575">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="39d7f-576">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="39d7f-577">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="39d7f-578">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="39d7f-579">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="39d7f-580">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="39d7f-581">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="39d7f-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="39d7f-582">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="39d7f-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="39d7f-583">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="39d7f-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="39d7f-584">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="39d7f-585">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="39d7f-586">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="39d7f-587">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="39d7f-588">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="39d7f-589">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="39d7f-590">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="39d7f-591">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="39d7f-592">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="39d7f-593">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="39d7f-594">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="39d7f-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="39d7f-595">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="39d7f-596">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="39d7f-597">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="39d7f-598">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="39d7f-599">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="39d7f-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="39d7f-600">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="39d7f-601">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="39d7f-602">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="39d7f-603">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="39d7f-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="39d7f-604">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="39d7f-605">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="39d7f-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="39d7f-606">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="39d7f-607">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="39d7f-608">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="39d7f-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="39d7f-609">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="39d7f-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="39d7f-610">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="39d7f-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-611">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-612">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="39d7f-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="39d7f-613">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="39d7f-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-614">Az.Compute</span></span>
* <span data-ttu-id="39d7f-615">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="39d7f-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="39d7f-616">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="39d7f-617">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="39d7f-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="39d7f-618">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39d7f-619">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="39d7f-620">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="39d7f-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="39d7f-621">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="39d7f-622">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="39d7f-622">Breaking changes</span></span>
    - <span data-ttu-id="39d7f-623">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="39d7f-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="39d7f-624">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="39d7f-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-625">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-626">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-628">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="39d7f-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="39d7f-629">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="39d7f-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="39d7f-630">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="39d7f-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="39d7f-631">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="39d7f-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="39d7f-632">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="39d7f-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="39d7f-633">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="39d7f-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-634">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-635">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="39d7f-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-636">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-637">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="39d7f-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="39d7f-638">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="39d7f-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="39d7f-639">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="39d7f-640">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="39d7f-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="39d7f-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39d7f-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39d7f-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39d7f-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39d7f-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39d7f-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39d7f-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39d7f-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="39d7f-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39d7f-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="39d7f-646">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="39d7f-647">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39d7f-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="39d7f-648">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39d7f-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="39d7f-649">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39d7f-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="39d7f-650">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="39d7f-651">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="39d7f-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="39d7f-652">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="39d7f-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="39d7f-653">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="39d7f-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="39d7f-654">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="39d7f-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="39d7f-655">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="39d7f-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="39d7f-656">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="39d7f-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="39d7f-657">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="39d7f-658">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-659">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-660">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="39d7f-660">Breaking changes:</span></span>
    - <span data-ttu-id="39d7f-661">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="39d7f-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39d7f-662">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39d7f-663">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="39d7f-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39d7f-664">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39d7f-665">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="39d7f-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="39d7f-666">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="39d7f-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="39d7f-667">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="39d7f-668">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="39d7f-669">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="39d7f-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39d7f-670">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39d7f-671">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="39d7f-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39d7f-672">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-674">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-675">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="39d7f-676">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="39d7f-677">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-678">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-679">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-680">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-681">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-682">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="39d7f-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-683">Az.Resources</span></span>
* <span data-ttu-id="39d7f-684">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="39d7f-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-685">Az.Network</span></span>
* <span data-ttu-id="39d7f-686">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="39d7f-687">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="39d7f-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="39d7f-693">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="39d7f-694">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-694">New cmdlet:</span></span>
        - <span data-ttu-id="39d7f-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="39d7f-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="39d7f-696">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="39d7f-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="39d7f-697">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="39d7f-698">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="39d7f-699">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="39d7f-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="39d7f-700">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="39d7f-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="39d7f-701">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="39d7f-702">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="39d7f-703">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-703">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="39d7f-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="39d7f-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39d7f-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39d7f-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39d7f-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="39d7f-709">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="39d7f-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="39d7f-710">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="39d7f-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39d7f-711">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="39d7f-712">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="39d7f-713">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="39d7f-714">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="39d7f-715">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="39d7f-716">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-716">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="39d7f-718">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="39d7f-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39d7f-719">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39d7f-720">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39d7f-721">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39d7f-722">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39d7f-723">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="39d7f-724">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="39d7f-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="39d7f-725">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-725">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="39d7f-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="39d7f-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="39d7f-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="39d7f-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="39d7f-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="39d7f-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="39d7f-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="39d7f-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="39d7f-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="39d7f-732">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="39d7f-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39d7f-733">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="39d7f-734">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="39d7f-735">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="39d7f-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="39d7f-736">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="39d7f-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="39d7f-737">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="39d7f-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39d7f-738">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="39d7f-739">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="39d7f-740">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="39d7f-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="39d7f-741">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="39d7f-742">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="39d7f-743">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-743">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="39d7f-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="39d7f-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="39d7f-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-749">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="39d7f-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-750">Az.Sql</span></span>
* <span data-ttu-id="39d7f-751">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="39d7f-752">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="39d7f-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="39d7f-753">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="39d7f-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="39d7f-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="39d7f-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="39d7f-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="39d7f-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="39d7f-756">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="39d7f-757">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="39d7f-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="39d7f-758">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="39d7f-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="39d7f-759">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-760">Az.Storage</span></span>
* <span data-ttu-id="39d7f-761">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="39d7f-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="39d7f-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="39d7f-764">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="39d7f-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="39d7f-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39d7f-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="39d7f-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39d7f-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="39d7f-767">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="39d7f-768">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-768">General</span></span>
* <span data-ttu-id="39d7f-769">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-770">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-771">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="39d7f-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-772">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-773">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="39d7f-774">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="39d7f-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-775">Az.Automation</span></span>
* <span data-ttu-id="39d7f-776">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="39d7f-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39d7f-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-777">Az.Batch</span></span>
* <span data-ttu-id="39d7f-778">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="39d7f-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-779">Az.Compute</span></span>
* <span data-ttu-id="39d7f-780">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="39d7f-781">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="39d7f-782">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="39d7f-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="39d7f-783">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="39d7f-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-784">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-785">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="39d7f-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="39d7f-786">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="39d7f-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="39d7f-787">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-789">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="39d7f-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="39d7f-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="39d7f-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="39d7f-791">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="39d7f-792">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="39d7f-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="39d7f-793">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="39d7f-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="39d7f-794">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-795">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-796">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="39d7f-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="39d7f-797">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="39d7f-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-798">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-799">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="39d7f-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="39d7f-800">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="39d7f-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="39d7f-801">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="39d7f-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="39d7f-802">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39d7f-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-803">Az.Network</span></span>
* <span data-ttu-id="39d7f-804">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="39d7f-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="39d7f-805">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="39d7f-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="39d7f-806">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-806">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="39d7f-808">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="39d7f-809">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="39d7f-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="39d7f-810">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="39d7f-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39d7f-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39d7f-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="39d7f-814">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="39d7f-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="39d7f-815">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="39d7f-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="39d7f-816">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="39d7f-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="39d7f-817">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="39d7f-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39d7f-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39d7f-818">Az.RedisCache</span></span>
* <span data-ttu-id="39d7f-819">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="39d7f-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-820">Az.Sql</span></span>
* <span data-ttu-id="39d7f-821">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="39d7f-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-822">Az.Storage</span></span>
* <span data-ttu-id="39d7f-823">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="39d7f-824">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="39d7f-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="39d7f-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="39d7f-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="39d7f-826">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="39d7f-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="39d7f-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39d7f-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39d7f-828">Az.StorageSync</span></span>
* <span data-ttu-id="39d7f-829">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="39d7f-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-830">Az.Websites</span></span>
* <span data-ttu-id="39d7f-831">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="39d7f-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="39d7f-832">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-833">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-834">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="39d7f-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="39d7f-835">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="39d7f-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="39d7f-836">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-837">Az.Automation</span></span>
* <span data-ttu-id="39d7f-838">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="39d7f-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="39d7f-839">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="39d7f-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="39d7f-840">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="39d7f-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-841">Az.Compute</span></span>
* <span data-ttu-id="39d7f-842">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="39d7f-843">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39d7f-844">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="39d7f-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="39d7f-845">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="39d7f-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="39d7f-846">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="39d7f-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="39d7f-847">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="39d7f-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="39d7f-848">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="39d7f-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="39d7f-849">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="39d7f-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="39d7f-850">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="39d7f-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-851">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-852">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="39d7f-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="39d7f-853">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="39d7f-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-854">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-855">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="39d7f-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-856">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-857">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="39d7f-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="39d7f-858">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="39d7f-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="39d7f-859">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="39d7f-859">New cmdlets are:</span></span>
    - <span data-ttu-id="39d7f-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39d7f-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39d7f-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39d7f-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39d7f-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39d7f-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39d7f-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39d7f-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-864">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-865">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="39d7f-866">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="39d7f-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="39d7f-867">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="39d7f-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="39d7f-868">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="39d7f-869">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="39d7f-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="39d7f-870">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="39d7f-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="39d7f-871">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="39d7f-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="39d7f-872">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="39d7f-873">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="39d7f-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="39d7f-874">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="39d7f-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="39d7f-875">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="39d7f-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="39d7f-876">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="39d7f-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="39d7f-877">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="39d7f-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="39d7f-878">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="39d7f-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="39d7f-879">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="39d7f-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="39d7f-880">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="39d7f-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="39d7f-881">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="39d7f-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="39d7f-882">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="39d7f-883">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="39d7f-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="39d7f-884">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-884">Overall improved help files</span></span>
* <span data-ttu-id="39d7f-885">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="39d7f-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-886">Az.Network</span></span>
* <span data-ttu-id="39d7f-887">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="39d7f-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="39d7f-888">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="39d7f-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="39d7f-889">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="39d7f-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="39d7f-890">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="39d7f-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="39d7f-891">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="39d7f-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="39d7f-892">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="39d7f-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="39d7f-893">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="39d7f-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="39d7f-894">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39d7f-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="39d7f-895">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="39d7f-896">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="39d7f-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="39d7f-897">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="39d7f-898">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="39d7f-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="39d7f-899">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-899">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="39d7f-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="39d7f-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="39d7f-902">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="39d7f-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="39d7f-903">New-VpnSite</span></span>
        - <span data-ttu-id="39d7f-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="39d7f-904">Update-VpnSite</span></span>
        - <span data-ttu-id="39d7f-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-905">New-VpnConnection</span></span>
        - <span data-ttu-id="39d7f-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-906">Update-VpnConnection</span></span>
* <span data-ttu-id="39d7f-907">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="39d7f-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-909">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="39d7f-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="39d7f-910">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="39d7f-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-911">Az.Resources</span></span>
* <span data-ttu-id="39d7f-912">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="39d7f-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-914">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="39d7f-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="39d7f-915">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="39d7f-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="39d7f-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39d7f-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39d7f-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39d7f-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39d7f-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39d7f-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39d7f-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="39d7f-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="39d7f-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39d7f-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39d7f-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39d7f-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39d7f-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39d7f-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39d7f-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39d7f-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39d7f-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="39d7f-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="39d7f-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39d7f-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39d7f-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39d7f-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39d7f-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39d7f-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39d7f-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="39d7f-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="39d7f-929">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="39d7f-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39d7f-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39d7f-930">Az.SignalR</span></span>
* <span data-ttu-id="39d7f-931">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="39d7f-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-932">Az.Sql</span></span>
* <span data-ttu-id="39d7f-933">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="39d7f-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="39d7f-934">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="39d7f-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="39d7f-935">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="39d7f-936">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="39d7f-937">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="39d7f-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-938">Az.Storage</span></span>
* <span data-ttu-id="39d7f-939">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="39d7f-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="39d7f-940">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="39d7f-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="39d7f-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="39d7f-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="39d7f-943">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="39d7f-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="39d7f-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="39d7f-945">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="39d7f-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39d7f-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39d7f-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39d7f-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-950">Az.Websites</span></span>
* <span data-ttu-id="39d7f-951">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="39d7f-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="39d7f-952">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="39d7f-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="39d7f-953">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="39d7f-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="39d7f-954">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="39d7f-955">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-955">General</span></span>
* <span data-ttu-id="39d7f-956">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="39d7f-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-957">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-958">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="39d7f-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="39d7f-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="39d7f-959">Az.Aks</span></span>
* <span data-ttu-id="39d7f-960">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="39d7f-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="39d7f-961">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="39d7f-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-962">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-963">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="39d7f-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="39d7f-964">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="39d7f-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="39d7f-965">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="39d7f-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="39d7f-966">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="39d7f-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="39d7f-967">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39d7f-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-968">Az.Batch</span></span>
* <span data-ttu-id="39d7f-969">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="39d7f-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-970">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-971">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="39d7f-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-972">Az.Compute</span></span>
* <span data-ttu-id="39d7f-973">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="39d7f-974">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="39d7f-975">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="39d7f-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="39d7f-976">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="39d7f-977">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="39d7f-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="39d7f-978">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="39d7f-979">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="39d7f-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="39d7f-980">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="39d7f-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-981">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-982">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="39d7f-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="39d7f-983">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="39d7f-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="39d7f-984">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="39d7f-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="39d7f-985">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="39d7f-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-987">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-988">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-989">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="39d7f-990">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="39d7f-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="39d7f-991">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="39d7f-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="39d7f-992">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="39d7f-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="39d7f-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="39d7f-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="39d7f-994">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="39d7f-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-995">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-996">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-997">Az.Network</span></span>
* <span data-ttu-id="39d7f-998">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="39d7f-999">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="39d7f-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="39d7f-1000">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="39d7f-1001">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="39d7f-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="39d7f-1002">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="39d7f-1003">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="39d7f-1004">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="39d7f-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1006">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="39d7f-1007">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1007">Added example</span></span>
    - <span data-ttu-id="39d7f-1008">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="39d7f-1009">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="39d7f-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="39d7f-1010">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="39d7f-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1012">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1013">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1014">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="39d7f-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="39d7f-1015">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="39d7f-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="39d7f-1016">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="39d7f-1017">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-1019">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="39d7f-1020">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="39d7f-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="39d7f-1021">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="39d7f-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-1023">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="39d7f-1024">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="39d7f-1025">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="39d7f-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="39d7f-1026">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="39d7f-1027">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="39d7f-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="39d7f-1028">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="39d7f-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1029">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1030">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1031">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1032">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="39d7f-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="39d7f-1033">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="39d7f-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="39d7f-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="39d7f-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="39d7f-1036">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="39d7f-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="39d7f-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1038">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1039">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39d7f-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="39d7f-1040">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1041">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1042">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39d7f-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="39d7f-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="39d7f-1044">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1045">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1046">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-1048">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1049">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1050">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="39d7f-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="39d7f-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="39d7f-1052">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="39d7f-1053">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="39d7f-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1054">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1055">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="39d7f-1056">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="39d7f-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1057">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-1058">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="39d7f-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="39d7f-1059">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="39d7f-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1060">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-1061">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="39d7f-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39d7f-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1062">Az.LogicApp</span></span>
* <span data-ttu-id="39d7f-1063">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="39d7f-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="39d7f-1064">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="39d7f-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="39d7f-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="39d7f-1066">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1067">Az.Network</span></span>
* <span data-ttu-id="39d7f-1068">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="39d7f-1069">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1069">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39d7f-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39d7f-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39d7f-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="39d7f-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="39d7f-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="39d7f-1078">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="39d7f-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="39d7f-1079">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="39d7f-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="39d7f-1080">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="39d7f-1081">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="39d7f-1082">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="39d7f-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="39d7f-1083">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="39d7f-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="39d7f-1084">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="39d7f-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39d7f-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39d7f-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="39d7f-1088">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="39d7f-1089">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="39d7f-1090">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="39d7f-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="39d7f-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="39d7f-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="39d7f-1094">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="39d7f-1095">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="39d7f-1096">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1098">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="39d7f-1099">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="39d7f-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1101">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="39d7f-1102">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="39d7f-1103">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="39d7f-1104">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="39d7f-1105">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="39d7f-1106">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="39d7f-1107">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="39d7f-1108">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="39d7f-1109">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="39d7f-1110">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1111">Az.Resources</span></span>
- <span data-ttu-id="39d7f-1112">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="39d7f-1113">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="39d7f-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-1115">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="39d7f-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="39d7f-1116">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="39d7f-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1117">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1118">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="39d7f-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="39d7f-1119">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="39d7f-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="39d7f-1120">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1121">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1122">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="39d7f-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39d7f-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39d7f-1123">Az.StorageSync</span></span>
* <span data-ttu-id="39d7f-1124">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="39d7f-1125">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="39d7f-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1126">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1127">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="39d7f-1128">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="39d7f-1129">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="39d7f-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="39d7f-1130">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1131">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1132">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="39d7f-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="39d7f-1133">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="39d7f-1134">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="39d7f-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="39d7f-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1135">Az.Advisor</span></span>
* <span data-ttu-id="39d7f-1136">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="39d7f-1137">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-1139">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="39d7f-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="39d7f-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="39d7f-1141">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="39d7f-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="39d7f-1142">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="39d7f-1143">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="39d7f-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="39d7f-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="39d7f-1145">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="39d7f-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1146">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1147">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1148">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1149">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1150">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1151">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39d7f-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39d7f-1152">Az.EventGrid</span></span>
* <span data-ttu-id="39d7f-1153">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1154">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-1155">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1156">Az.Network</span></span>
* <span data-ttu-id="39d7f-1157">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="39d7f-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="39d7f-1158">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-1160">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="39d7f-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="39d7f-1161">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="39d7f-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1163">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="39d7f-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1165">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="39d7f-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1166">Az.Resources</span></span>
    - <span data-ttu-id="39d7f-1167">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="39d7f-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="39d7f-1168">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="39d7f-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="39d7f-1169">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="39d7f-1170">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-1172">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1173">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1174">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="39d7f-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="39d7f-1175">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="39d7f-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39d7f-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39d7f-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39d7f-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="39d7f-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="39d7f-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="39d7f-1182">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="39d7f-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1183">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1184">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="39d7f-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39d7f-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="39d7f-1186">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="39d7f-1187">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="39d7f-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="39d7f-1188">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="39d7f-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="39d7f-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="39d7f-1191">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="39d7f-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39d7f-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="39d7f-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39d7f-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39d7f-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39d7f-1194">Az.StorageSync</span></span>
* <span data-ttu-id="39d7f-1195">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="39d7f-1196">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1197">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1198">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="39d7f-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="39d7f-1199">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="39d7f-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="39d7f-1200">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="39d7f-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="39d7f-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="39d7f-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="39d7f-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="39d7f-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1203">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1204">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="39d7f-1205">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="39d7f-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="39d7f-1206">Az.Dns</span></span>
* <span data-ttu-id="39d7f-1207">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39d7f-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39d7f-1208">Az.EventGrid</span></span>
* <span data-ttu-id="39d7f-1209">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="39d7f-1210">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1210">New cmdlets:</span></span>
    - <span data-ttu-id="39d7f-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39d7f-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39d7f-1212">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39d7f-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39d7f-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39d7f-1214">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="39d7f-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39d7f-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39d7f-1216">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39d7f-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="39d7f-1218">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39d7f-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="39d7f-1220">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="39d7f-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="39d7f-1222">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="39d7f-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="39d7f-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="39d7f-1224">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="39d7f-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="39d7f-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="39d7f-1226">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="39d7f-1227">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="39d7f-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="39d7f-1229">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="39d7f-1230">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="39d7f-1231">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="39d7f-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="39d7f-1232">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="39d7f-1233">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="39d7f-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="39d7f-1234">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="39d7f-1235">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="39d7f-1236">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="39d7f-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="39d7f-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="39d7f-1238">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="39d7f-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="39d7f-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="39d7f-1240">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="39d7f-1241">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="39d7f-1244">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="39d7f-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="39d7f-1246">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="39d7f-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1247">Az.Network</span></span>
* <span data-ttu-id="39d7f-1248">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="39d7f-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="39d7f-1249">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1249">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="39d7f-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="39d7f-1251">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="39d7f-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="39d7f-1252">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1252">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="39d7f-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="39d7f-1254">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="39d7f-1255">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1255">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39d7f-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39d7f-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39d7f-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="39d7f-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="39d7f-1261">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="39d7f-1262">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1262">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39d7f-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39d7f-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d7f-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39d7f-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="39d7f-1267">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="39d7f-1268">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="39d7f-1269">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="39d7f-1270">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="39d7f-1271">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="39d7f-1272">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39d7f-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="39d7f-1273">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="39d7f-1274">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="39d7f-1275">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="39d7f-1276">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="39d7f-1277">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="39d7f-1278">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="39d7f-1279">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="39d7f-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="39d7f-1280">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="39d7f-1281">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="39d7f-1282">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="39d7f-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="39d7f-1283">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="39d7f-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="39d7f-1284">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="39d7f-1285">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="39d7f-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="39d7f-1286">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="39d7f-1287">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="39d7f-1288">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="39d7f-1289">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1291">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1292">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1293">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="39d7f-1294">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="39d7f-1295">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="39d7f-1296">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-1298">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1299">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1300">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="39d7f-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="39d7f-1301">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="39d7f-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="39d7f-1302">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="39d7f-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39d7f-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39d7f-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39d7f-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39d7f-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="39d7f-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="39d7f-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="39d7f-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1308">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1309">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="39d7f-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="39d7f-1311">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="39d7f-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="39d7f-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1313">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1314">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="39d7f-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="39d7f-1315">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="39d7f-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="39d7f-1316">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="39d7f-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-1317">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-1318">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1319">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1320">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="39d7f-1321">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1322">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-1323">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="39d7f-1324">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d7f-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1325">Az.Network</span></span>
* <span data-ttu-id="39d7f-1326">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="39d7f-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="39d7f-1327">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="39d7f-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-1329">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1331">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="39d7f-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-1333">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d7f-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-1335">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="39d7f-1336">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1337">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1338">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="39d7f-1339">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="39d7f-1340">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="39d7f-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="39d7f-1341">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1342">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1343">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="39d7f-1344">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="39d7f-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-1346">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="39d7f-1347">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="39d7f-1348">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="39d7f-1349">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="39d7f-1350">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="39d7f-1351">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="39d7f-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="39d7f-1352">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="39d7f-1353">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="39d7f-1354">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="39d7f-1355">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="39d7f-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="39d7f-1356">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="39d7f-1357">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="39d7f-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="39d7f-1358">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="39d7f-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="39d7f-1359">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="39d7f-1360">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="39d7f-1361">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="39d7f-1362">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="39d7f-1363">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="39d7f-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="39d7f-1364">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="39d7f-1365">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="39d7f-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="39d7f-1366">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="39d7f-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="39d7f-1367">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="39d7f-1368">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="39d7f-1369">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="39d7f-1370">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="39d7f-1371">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="39d7f-1372">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="39d7f-1373">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="39d7f-1374">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="39d7f-1375">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="39d7f-1376">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="39d7f-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="39d7f-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="39d7f-1378">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="39d7f-1379">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39d7f-1380">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="39d7f-1381">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="39d7f-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="39d7f-1382">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="39d7f-1383">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="39d7f-1384">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="39d7f-1385">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39d7f-1386">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="39d7f-1387">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="39d7f-1388">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="39d7f-1389">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="39d7f-1390">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39d7f-1391">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="39d7f-1392">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="39d7f-1393">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="39d7f-1394">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="39d7f-1395">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="39d7f-1396">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="39d7f-1397">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="39d7f-1398">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="39d7f-1399">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="39d7f-1400">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="39d7f-1401">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="39d7f-1402">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="39d7f-1403">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="39d7f-1404">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="39d7f-1405">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="39d7f-1406">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39d7f-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="39d7f-1407">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="39d7f-1408">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="39d7f-1409">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="39d7f-1410">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="39d7f-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="39d7f-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="39d7f-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="39d7f-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="39d7f-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="39d7f-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="39d7f-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="39d7f-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="39d7f-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="39d7f-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="39d7f-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="39d7f-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="39d7f-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="39d7f-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="39d7f-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1423">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1424">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="39d7f-1425">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="39d7f-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="39d7f-1426">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="39d7f-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="39d7f-1427">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="39d7f-1428">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="39d7f-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="39d7f-1429">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="39d7f-1430">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1431">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1432">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="39d7f-1433">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-1435">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1436">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-1437">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1438">Az.Network</span></span>
* <span data-ttu-id="39d7f-1439">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="39d7f-1440">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="39d7f-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="39d7f-1442">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39d7f-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1443">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1444">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1445">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1446">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="39d7f-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="39d7f-1447">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1448">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1449">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="39d7f-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-1451">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="39d7f-1452">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1453">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1454">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="39d7f-1455">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="39d7f-1456">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="39d7f-1457">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="39d7f-1458">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="39d7f-1459">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="39d7f-1460">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="39d7f-1460">Breaking changes</span></span>
    - <span data-ttu-id="39d7f-1461">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="39d7f-1462">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="39d7f-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="39d7f-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="39d7f-1464">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="39d7f-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="39d7f-1465">Az.Dns</span></span>
* <span data-ttu-id="39d7f-1466">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="39d7f-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="39d7f-1467">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="39d7f-1468">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="39d7f-1470">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="39d7f-1471">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-1472">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-1473">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="39d7f-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39d7f-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="39d7f-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39d7f-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="39d7f-1476">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39d7f-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="39d7f-1477">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="39d7f-1478">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="39d7f-1479">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1480">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-1481">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="39d7f-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="39d7f-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="39d7f-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="39d7f-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="39d7f-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="39d7f-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="39d7f-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="39d7f-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="39d7f-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="39d7f-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="39d7f-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39d7f-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39d7f-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39d7f-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39d7f-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39d7f-1493">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="39d7f-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="39d7f-1494">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1495">Az.Network</span></span>
* <span data-ttu-id="39d7f-1496">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="39d7f-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="39d7f-1497">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="39d7f-1497">New cmdlets</span></span>
        - <span data-ttu-id="39d7f-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="39d7f-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="39d7f-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="39d7f-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="39d7f-1502">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="39d7f-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="39d7f-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="39d7f-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="39d7f-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="39d7f-1505">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="39d7f-1506">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="39d7f-1507">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-1509">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="39d7f-1510">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="39d7f-1511">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1513">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="39d7f-1514">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="39d7f-1515">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="39d7f-1516">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="39d7f-1517">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="39d7f-1518">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="39d7f-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="39d7f-1519">Az.Relay</span></span>
* <span data-ttu-id="39d7f-1520">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="39d7f-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-1522">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="39d7f-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1523">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1524">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="39d7f-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="39d7f-1525">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="39d7f-1526">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="39d7f-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="39d7f-1528">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="39d7f-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="39d7f-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="39d7f-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1532">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1533">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="39d7f-1534">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="39d7f-1535">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-1536">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-1537">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39d7f-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="39d7f-1538">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39d7f-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39d7f-1539">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39d7f-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39d7f-1540">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39d7f-1541">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39d7f-1542">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39d7f-1543">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="39d7f-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1544">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1545">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="39d7f-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39d7f-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-1546">Az.Batch</span></span>
* <span data-ttu-id="39d7f-1547">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-1548">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-1549">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-1551">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1552">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1553">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="39d7f-1554">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1555">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="39d7f-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1556">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1557">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-1559">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39d7f-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39d7f-1560">Az.EventGrid</span></span>
* <span data-ttu-id="39d7f-1561">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1562">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-1563">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="39d7f-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39d7f-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39d7f-1564">Az.HDInsight</span></span>
* <span data-ttu-id="39d7f-1565">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1566">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-1567">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1568">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-1569">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1570">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="39d7f-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="39d7f-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39d7f-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="39d7f-1572">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="39d7f-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="39d7f-1573">Az.Media</span></span>
* <span data-ttu-id="39d7f-1574">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1575">Az.Monitor</span></span>
  * <span data-ttu-id="39d7f-1576">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="39d7f-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="39d7f-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="39d7f-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="39d7f-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="39d7f-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39d7f-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="39d7f-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39d7f-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="39d7f-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39d7f-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="39d7f-1582">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="39d7f-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1583">Az.Network</span></span>
* <span data-ttu-id="39d7f-1584">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1585">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="39d7f-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="39d7f-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="39d7f-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="39d7f-1587">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1589">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="39d7f-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="39d7f-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="39d7f-1591">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1593">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1594">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="39d7f-1595">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="39d7f-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="39d7f-1596">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="39d7f-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39d7f-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39d7f-1597">Az.RedisCache</span></span>
* <span data-ttu-id="39d7f-1598">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1599">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1600">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="39d7f-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1601">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1602">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="39d7f-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="39d7f-1603">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1604">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="39d7f-1605">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="39d7f-1606">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="39d7f-1607">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="39d7f-1608">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="39d7f-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1609">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1610">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="39d7f-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="39d7f-1611">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39d7f-1612">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="39d7f-1613">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="39d7f-1614">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-1615">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-1616">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39d7f-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="39d7f-1617">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39d7f-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39d7f-1618">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39d7f-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39d7f-1619">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39d7f-1620">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39d7f-1621">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39d7f-1622">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="39d7f-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1623">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1624">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="39d7f-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39d7f-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="39d7f-1626">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="39d7f-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="39d7f-1627">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="39d7f-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1628">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1629">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="39d7f-1630">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="39d7f-1631">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1632">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1633">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39d7f-1634">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="39d7f-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="39d7f-1636">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="39d7f-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1637">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1638">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="39d7f-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="39d7f-1639">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1640">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1641">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="39d7f-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="39d7f-1642">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="39d7f-1643">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="39d7f-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="39d7f-1644">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="39d7f-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="39d7f-1645">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="39d7f-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="39d7f-1646">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="39d7f-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1647">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1648">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1649">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1650">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="39d7f-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="39d7f-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="39d7f-1652">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="39d7f-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="39d7f-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="39d7f-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="39d7f-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="39d7f-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="39d7f-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="39d7f-1657">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="39d7f-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="39d7f-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="39d7f-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="39d7f-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39d7f-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="39d7f-1662">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39d7f-1663">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="39d7f-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="39d7f-1664">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39d7f-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="39d7f-1665">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39d7f-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39d7f-1666">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39d7f-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39d7f-1667">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39d7f-1668">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39d7f-1669">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39d7f-1670">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="39d7f-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1671">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1672">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="39d7f-1673">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="39d7f-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="39d7f-1674">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1674">Pre-Post script</span></span>
    * <span data-ttu-id="39d7f-1675">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="39d7f-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1676">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1677">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="39d7f-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="39d7f-1678">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1679">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-1680">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1681">Az.Network</span></span>
* <span data-ttu-id="39d7f-1682">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="39d7f-1683">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1685">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="39d7f-1686">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="39d7f-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1687">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1688">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39d7f-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="39d7f-1689">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="39d7f-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1690">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1691">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1692">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1693">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="39d7f-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39d7f-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39d7f-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39d7f-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="39d7f-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="39d7f-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="39d7f-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="39d7f-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1700">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1701">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="39d7f-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="39d7f-1702">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1703">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1704">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="39d7f-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="39d7f-1705">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1706">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1707">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="39d7f-1708">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="39d7f-1709">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="39d7f-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-1710">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-1711">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1712">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1713">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="39d7f-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1714">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1715">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39d7f-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1716">Az.LogicApp</span></span>
* <span data-ttu-id="39d7f-1717">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1718">Az.Network</span></span>
* <span data-ttu-id="39d7f-1719">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1721">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="39d7f-1722">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="39d7f-1722">SDK Update</span></span>
* <span data-ttu-id="39d7f-1723">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39d7f-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="39d7f-1724">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39d7f-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1725">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1726">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="39d7f-1727">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="39d7f-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="39d7f-1728">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="39d7f-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="39d7f-1729">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="39d7f-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="39d7f-1730">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="39d7f-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="39d7f-1731">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="39d7f-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1732">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1733">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="39d7f-1734">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1735">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1736">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="39d7f-1737">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="39d7f-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="39d7f-1739">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1740">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1741">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="39d7f-1742">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="39d7f-1743">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-1745">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1746">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1747">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="39d7f-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="39d7f-1748">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="39d7f-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="39d7f-1749">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="39d7f-1750">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-1752">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="39d7f-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39d7f-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1753">Az.EventHub</span></span>
* <span data-ttu-id="39d7f-1754">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1755">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-1756">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="39d7f-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39d7f-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1757">Az.LogicApp</span></span>
* <span data-ttu-id="39d7f-1758">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="39d7f-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="39d7f-1759">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="39d7f-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="39d7f-1760">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="39d7f-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="39d7f-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39d7f-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39d7f-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39d7f-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39d7f-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39d7f-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39d7f-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39d7f-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="39d7f-1765">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="39d7f-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="39d7f-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39d7f-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39d7f-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39d7f-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="39d7f-1770">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39d7f-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1771">Az.Monitor</span></span>
* <span data-ttu-id="39d7f-1772">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1773">Az.Network</span></span>
* <span data-ttu-id="39d7f-1774">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="39d7f-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="39d7f-1776">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="39d7f-1777">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="39d7f-1778">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1779">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1780">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="39d7f-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="39d7f-1781">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="39d7f-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="39d7f-1782">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="39d7f-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="39d7f-1783">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="39d7f-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1784">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1785">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="39d7f-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="39d7f-1786">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="39d7f-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1787">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1788">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="39d7f-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="39d7f-1789">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1790">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1791">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39d7f-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39d7f-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="39d7f-1793">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1794">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1795">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="39d7f-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="39d7f-1796">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="39d7f-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="39d7f-1797">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="39d7f-1799">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1800">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1801">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="39d7f-1802">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="39d7f-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="39d7f-1803">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="39d7f-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="39d7f-1804">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="39d7f-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1805">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1806">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39d7f-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="39d7f-1807">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="39d7f-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="39d7f-1808">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="39d7f-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="39d7f-1809">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1810">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1811">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="39d7f-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39d7f-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="39d7f-1813">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="39d7f-1815">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="39d7f-1816">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1817">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1818">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39d7f-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39d7f-1819">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39d7f-1820">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="39d7f-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="39d7f-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="39d7f-1821">Az.Aks</span></span>
* <span data-ttu-id="39d7f-1822">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39d7f-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-1823">Az.Automation</span></span>
* <span data-ttu-id="39d7f-1824">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="39d7f-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="39d7f-1825">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39d7f-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39d7f-1826">Az.Cdn</span></span>
* <span data-ttu-id="39d7f-1827">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1828">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1829">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="39d7f-1830">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39d7f-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="39d7f-1831">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39d7f-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="39d7f-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="39d7f-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="39d7f-1833">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39d7f-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39d7f-1834">Az.DataFactory</span></span>
* <span data-ttu-id="39d7f-1835">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="39d7f-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-1837">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="39d7f-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="39d7f-1838">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="39d7f-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="39d7f-1839">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1840">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-1841">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1842">Az.KeyVault</span></span>
* <span data-ttu-id="39d7f-1843">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1844">Az.Network</span></span>
* <span data-ttu-id="39d7f-1845">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1846">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1847">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="39d7f-1848">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="39d7f-1849">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="39d7f-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="39d7f-1850">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="39d7f-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="39d7f-1851">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="39d7f-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="39d7f-1852">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="39d7f-1853">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="39d7f-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-1855">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="39d7f-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="39d7f-1856">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1856">Fix some error messages.</span></span>
* <span data-ttu-id="39d7f-1857">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="39d7f-1858">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39d7f-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39d7f-1859">Az.SignalR</span></span>
* <span data-ttu-id="39d7f-1860">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1861">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1862">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39d7f-1863">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="39d7f-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="39d7f-1864">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="39d7f-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="39d7f-1865">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1866">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1867">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39d7f-1868">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="39d7f-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="39d7f-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="39d7f-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="39d7f-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="39d7f-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="39d7f-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="39d7f-1872">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1873">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1874">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="39d7f-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39d7f-1875">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="39d7f-1876">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="39d7f-1877">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="39d7f-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39d7f-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1878">Az.Accounts</span></span>
* <span data-ttu-id="39d7f-1879">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="39d7f-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1880">Az.Compute</span></span>
* <span data-ttu-id="39d7f-1881">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="39d7f-1882">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="39d7f-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="39d7f-1883">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-1885">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="39d7f-1886">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="39d7f-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39d7f-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39d7f-1887">Az.EventGrid</span></span>
* <span data-ttu-id="39d7f-1888">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="39d7f-1889">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="39d7f-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="39d7f-1890">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="39d7f-1891">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="39d7f-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="39d7f-1892">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="39d7f-1893">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="39d7f-1894">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="39d7f-1895">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="39d7f-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="39d7f-1896">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="39d7f-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="39d7f-1897">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="39d7f-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="39d7f-1898">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="39d7f-1899">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39d7f-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1900">Az.IotHub</span></span>
* <span data-ttu-id="39d7f-1901">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="39d7f-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39d7f-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39d7f-1902">Az.LogicApp</span></span>
* <span data-ttu-id="39d7f-1903">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="39d7f-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1904">Az.Resources</span></span>
* <span data-ttu-id="39d7f-1905">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="39d7f-1906">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="39d7f-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="39d7f-1907">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="39d7f-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="39d7f-1908">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="39d7f-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="39d7f-1909">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="39d7f-1910">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="39d7f-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39d7f-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39d7f-1911">Az.SignalR</span></span>
* <span data-ttu-id="39d7f-1912">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1913">Az.Sql</span></span>
* <span data-ttu-id="39d7f-1914">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39d7f-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1915">Az.Storage</span></span>
* <span data-ttu-id="39d7f-1916">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="39d7f-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="39d7f-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="39d7f-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="39d7f-1918">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="39d7f-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="39d7f-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-1920">Az.Websites</span></span>
* <span data-ttu-id="39d7f-1921">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="39d7f-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="39d7f-1922">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="39d7f-1923">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="39d7f-1924">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-1924">General</span></span>

- <span data-ttu-id="39d7f-1925">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="39d7f-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="39d7f-1926">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1926">Online help for each module</span></span>
- <span data-ttu-id="39d7f-1927">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="39d7f-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="39d7f-1928">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="39d7f-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="39d7f-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1929">Az.Accounts</span></span>
- <span data-ttu-id="39d7f-1930">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39d7f-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="39d7f-1931">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="39d7f-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="39d7f-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="39d7f-1933">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="39d7f-1933">Fixes for #7002</span></span>
- <span data-ttu-id="39d7f-1934">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="39d7f-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39d7f-1935">Az.Batch</span></span>
- <span data-ttu-id="39d7f-1936">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="39d7f-1937">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="39d7f-1938">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="39d7f-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="39d7f-1939">Az.Billing</span></span>
- <span data-ttu-id="39d7f-1940">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="39d7f-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="39d7f-1942">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="39d7f-1943">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="39d7f-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="39d7f-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="39d7f-1945">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="39d7f-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="39d7f-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="39d7f-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="39d7f-1947">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="39d7f-1949">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="39d7f-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39d7f-1950">Az.Monitor</span></span>
- <span data-ttu-id="39d7f-1951">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="39d7f-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39d7f-1952">Az.KeyVault</span></span>
- <span data-ttu-id="39d7f-1953">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="39d7f-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="39d7f-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39d7f-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="39d7f-1955">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="39d7f-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="39d7f-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="39d7f-1956">Az.Media</span></span>
- <span data-ttu-id="39d7f-1957">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="39d7f-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="39d7f-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-1958">Az.Network</span></span>
<span data-ttu-id="39d7f-1959">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="39d7f-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="39d7f-1960">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="39d7f-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="39d7f-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="39d7f-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="39d7f-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d7f-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="39d7f-1969">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39d7f-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="39d7f-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39d7f-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="39d7f-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="39d7f-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="39d7f-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="39d7f-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="39d7f-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="39d7f-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="39d7f-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="39d7f-1976">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="39d7f-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="39d7f-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39d7f-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="39d7f-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39d7f-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="39d7f-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39d7f-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="39d7f-1980">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="39d7f-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="39d7f-1981">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="39d7f-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="39d7f-1983">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="39d7f-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39d7f-1984">Az.Profile</span></span>
- <span data-ttu-id="39d7f-1985">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39d7f-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="39d7f-1987">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="39d7f-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-1988">Az.Resources</span></span>
- <span data-ttu-id="39d7f-1989">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="39d7f-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="39d7f-1991">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="39d7f-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="39d7f-1992">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="39d7f-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="39d7f-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="39d7f-1994">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="39d7f-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="39d7f-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-1995">Az.Sql</span></span>
- <span data-ttu-id="39d7f-1996">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="39d7f-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="39d7f-1997">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="39d7f-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="39d7f-1998">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="39d7f-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-1999">Az.Storage</span></span>
- <span data-ttu-id="39d7f-2000">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="39d7f-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-2001">Az.Websites</span></span>
- <span data-ttu-id="39d7f-2002">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="39d7f-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="39d7f-2003">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="39d7f-2004">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-2004">General</span></span>

* <span data-ttu-id="39d7f-2005">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="39d7f-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="39d7f-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-2006">Az.Compute</span></span>

* <span data-ttu-id="39d7f-2007">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="39d7f-2009">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="39d7f-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="39d7f-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39d7f-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="39d7f-2011">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="39d7f-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="39d7f-2012">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="39d7f-2013">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="39d7f-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="39d7f-2015">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="39d7f-2016">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="39d7f-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-2017">Az.Resources</span></span>

* <span data-ttu-id="39d7f-2018">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="39d7f-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="39d7f-2019">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="39d7f-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-2020">Az.Sql</span></span>

* <span data-ttu-id="39d7f-2021">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="39d7f-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="39d7f-2022">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="39d7f-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="39d7f-2023">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="39d7f-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-2024">Az.Storage</span></span>

* <span data-ttu-id="39d7f-2025">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="39d7f-2026">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="39d7f-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="39d7f-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="39d7f-2028">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="39d7f-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="39d7f-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39d7f-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="39d7f-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39d7f-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="39d7f-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-2031">Az.Websites</span></span>

* <span data-ttu-id="39d7f-2032">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39d7f-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="39d7f-2033">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="39d7f-2034">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="39d7f-2035">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="39d7f-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39d7f-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="39d7f-2037">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="39d7f-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="39d7f-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39d7f-2038">Az.Automation</span></span>
* <span data-ttu-id="39d7f-2039">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="39d7f-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="39d7f-2040">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="39d7f-2041">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="39d7f-2042">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="39d7f-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="39d7f-2043">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="39d7f-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="39d7f-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-2044">Az.Compute</span></span>
* <span data-ttu-id="39d7f-2045">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="39d7f-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="39d7f-2046">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="39d7f-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="39d7f-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="39d7f-2048">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="39d7f-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="39d7f-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="39d7f-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="39d7f-2050">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="39d7f-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="39d7f-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-2051">Az.Network</span></span>
* <span data-ttu-id="39d7f-2052">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="39d7f-2053">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="39d7f-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="39d7f-2054">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="39d7f-2055">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="39d7f-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="39d7f-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="39d7f-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="39d7f-2057">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="39d7f-2058">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="39d7f-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="39d7f-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="39d7f-2060">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39d7f-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="39d7f-2061">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="39d7f-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="39d7f-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="39d7f-2062">Az.Relay</span></span>
* <span data-ttu-id="39d7f-2063">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="39d7f-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-2064">Az.Resources</span></span>
* <span data-ttu-id="39d7f-2065">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="39d7f-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="39d7f-2066">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="39d7f-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="39d7f-2067">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="39d7f-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="39d7f-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-2069">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="39d7f-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="39d7f-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-2070">Az.Sql</span></span>
* <span data-ttu-id="39d7f-2071">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="39d7f-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="39d7f-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39d7f-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39d7f-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39d7f-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39d7f-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39d7f-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39d7f-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39d7f-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39d7f-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39d7f-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39d7f-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39d7f-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39d7f-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="39d7f-2080">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="39d7f-2081">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="39d7f-2082">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="39d7f-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="39d7f-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="39d7f-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="39d7f-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="39d7f-2087">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39d7f-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="39d7f-2088">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="39d7f-2089">Geral</span><span class="sxs-lookup"><span data-stu-id="39d7f-2089">General</span></span>
* <span data-ttu-id="39d7f-2090">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="39d7f-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="39d7f-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2091">Az.Profile</span></span>
* <span data-ttu-id="39d7f-2092">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39d7f-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="39d7f-2093">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="39d7f-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="39d7f-2094">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="39d7f-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="39d7f-2095">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="39d7f-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="39d7f-2096">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="39d7f-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="39d7f-2097">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="39d7f-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="39d7f-2098">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="39d7f-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-2100">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-2101">Az.Compute</span></span>
* <span data-ttu-id="39d7f-2102">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="39d7f-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="39d7f-2103">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="39d7f-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="39d7f-2104">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-2106">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="39d7f-2107">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="39d7f-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="39d7f-2108">Az.Insights</span></span>
* <span data-ttu-id="39d7f-2109">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="39d7f-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="39d7f-2110">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="39d7f-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="39d7f-2111">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="39d7f-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="39d7f-2112">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="39d7f-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-2113">Az.Network</span></span>
* <span data-ttu-id="39d7f-2114">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="39d7f-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="39d7f-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="39d7f-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="39d7f-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="39d7f-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="39d7f-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="39d7f-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="39d7f-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="39d7f-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="39d7f-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39d7f-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39d7f-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="39d7f-2122">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="39d7f-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-2123">Az.Resources</span></span>
* <span data-ttu-id="39d7f-2124">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="39d7f-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="39d7f-2125">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="39d7f-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39d7f-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39d7f-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="39d7f-2127">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39d7f-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39d7f-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="39d7f-2129">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="39d7f-2130">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="39d7f-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="39d7f-2131">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="39d7f-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="39d7f-2132">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="39d7f-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="39d7f-2133">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="39d7f-2134">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="39d7f-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2135">Az.Profile</span></span>
* <span data-ttu-id="39d7f-2136">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="39d7f-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="39d7f-2137">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39d7f-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-2138">Az.Compute</span></span>
* <span data-ttu-id="39d7f-2139">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="39d7f-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="39d7f-2140">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39d7f-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39d7f-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="39d7f-2142">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="39d7f-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="39d7f-2143">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="39d7f-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="39d7f-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="39d7f-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-2147">Az.Network</span></span>
* <span data-ttu-id="39d7f-2148">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="39d7f-2149">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-2150">Az.Resources</span></span>
* <span data-ttu-id="39d7f-2151">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="39d7f-2152">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="39d7f-2153">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="39d7f-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="39d7f-2154">Azure.Storage</span></span>
* <span data-ttu-id="39d7f-2155">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="39d7f-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="39d7f-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="39d7f-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="39d7f-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="39d7f-2158">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="39d7f-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="39d7f-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39d7f-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39d7f-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="39d7f-2161">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39d7f-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39d7f-2162">Az.Compute</span></span>
* <span data-ttu-id="39d7f-2163">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="39d7f-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="39d7f-2164">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="39d7f-2165">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="39d7f-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="39d7f-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="39d7f-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="39d7f-2167">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39d7f-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39d7f-2168">Az.Network</span></span>
* <span data-ttu-id="39d7f-2169">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="39d7f-2170">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="39d7f-2170">new cmdlets added</span></span>
    - <span data-ttu-id="39d7f-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="39d7f-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="39d7f-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="39d7f-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39d7f-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="39d7f-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="39d7f-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="39d7f-2177">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="39d7f-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="39d7f-2178">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39d7f-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="39d7f-2179">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="39d7f-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39d7f-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39d7f-2180">Az.RedisCache</span></span>
* <span data-ttu-id="39d7f-2181">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="39d7f-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="39d7f-2182">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="39d7f-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="39d7f-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39d7f-2183">Az.Resources</span></span>
* <span data-ttu-id="39d7f-2184">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="39d7f-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="39d7f-2185">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="39d7f-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="39d7f-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39d7f-2186">Az.Sql</span></span>
* <span data-ttu-id="39d7f-2187">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="39d7f-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39d7f-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39d7f-2188">Az.Websites</span></span>
* <span data-ttu-id="39d7f-2189">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="39d7f-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="39d7f-2190">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="39d7f-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="39d7f-2191">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="39d7f-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="39d7f-2192">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="39d7f-2192">Initial Release</span></span>
