---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475125"
---
## <a name="160---march-2019"></a><span data-ttu-id="eb8c7-101">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="eb8c7-102">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="eb8c7-102">Highlights since the last major release</span></span>
* <span data-ttu-id="eb8c7-103">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="eb8c7-103">General availability of `Az` module</span></span>
* <span data-ttu-id="eb8c7-104">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="eb8c7-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="eb8c7-105">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="eb8c7-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="eb8c7-106">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="eb8c7-107">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="eb8c7-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eb8c7-108">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="eb8c7-109">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="eb8c7-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eb8c7-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-110">Az.Automation</span></span>
* <span data-ttu-id="eb8c7-111">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="eb8c7-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="eb8c7-112">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="eb8c7-112">Dynamic grouping</span></span>
    * <span data-ttu-id="eb8c7-113">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="eb8c7-113">Pre-Post script</span></span>
    * <span data-ttu-id="eb8c7-114">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="eb8c7-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-115">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-116">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="eb8c7-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="eb8c7-117">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eb8c7-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eb8c7-118">Az.KeyVault</span></span>
* <span data-ttu-id="eb8c7-119">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="eb8c7-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-120">Az.Network</span></span>
* <span data-ttu-id="eb8c7-121">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="eb8c7-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="eb8c7-122">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="eb8c7-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="eb8c7-124">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="eb8c7-125">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="eb8c7-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-126">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-127">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb8c7-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="eb8c7-128">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="eb8c7-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-129">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-130">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eb8c7-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-131">Az.Storage</span></span>
* <span data-ttu-id="eb8c7-132">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="eb8c7-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="eb8c7-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eb8c7-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eb8c7-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eb8c7-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="eb8c7-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="eb8c7-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="eb8c7-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="eb8c7-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="eb8c7-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eb8c7-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-139">Az.Websites</span></span>
* <span data-ttu-id="eb8c7-140">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="eb8c7-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="eb8c7-141">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eb8c7-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-142">Az.Accounts</span></span>
* <span data-ttu-id="eb8c7-143">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="eb8c7-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="eb8c7-144">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eb8c7-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-145">Az.Automation</span></span>
* <span data-ttu-id="eb8c7-146">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="eb8c7-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="eb8c7-147">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="eb8c7-148">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="eb8c7-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eb8c7-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eb8c7-149">Az.Cdn</span></span>
* <span data-ttu-id="eb8c7-150">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-151">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-152">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="eb8c7-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eb8c7-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb8c7-153">Az.DataFactory</span></span>
* <span data-ttu-id="eb8c7-154">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="eb8c7-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eb8c7-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eb8c7-155">Az.LogicApp</span></span>
* <span data-ttu-id="eb8c7-156">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-157">Az.Network</span></span>
* <span data-ttu-id="eb8c7-158">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="eb8c7-160">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="eb8c7-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="eb8c7-161">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="eb8c7-161">SDK Update</span></span>
* <span data-ttu-id="eb8c7-162">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="eb8c7-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="eb8c7-163">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="eb8c7-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-164">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-165">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="eb8c7-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="eb8c7-166">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="eb8c7-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="eb8c7-167">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="eb8c7-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="eb8c7-168">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="eb8c7-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="eb8c7-169">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="eb8c7-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="eb8c7-170">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="eb8c7-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-171">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-172">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="eb8c7-173">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eb8c7-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-174">Az.Storage</span></span>
* <span data-ttu-id="eb8c7-175">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="eb8c7-176">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="eb8c7-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="eb8c7-178">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eb8c7-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-179">Az.Automation</span></span>
* <span data-ttu-id="eb8c7-180">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="eb8c7-181">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="eb8c7-182">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="eb8c7-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="eb8c7-184">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-185">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-186">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="eb8c7-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="eb8c7-187">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="eb8c7-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="eb8c7-188">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="eb8c7-189">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="eb8c7-191">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eb8c7-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eb8c7-192">Az.EventHub</span></span>
* <span data-ttu-id="eb8c7-193">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="eb8c7-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="eb8c7-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eb8c7-194">Az.KeyVault</span></span>
* <span data-ttu-id="eb8c7-195">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eb8c7-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eb8c7-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eb8c7-196">Az.LogicApp</span></span>
* <span data-ttu-id="eb8c7-197">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="eb8c7-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="eb8c7-198">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="eb8c7-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="eb8c7-199">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="eb8c7-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="eb8c7-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb8c7-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eb8c7-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb8c7-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eb8c7-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb8c7-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eb8c7-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eb8c7-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="eb8c7-204">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="eb8c7-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="eb8c7-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eb8c7-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eb8c7-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eb8c7-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="eb8c7-209">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="eb8c7-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eb8c7-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eb8c7-210">Az.Monitor</span></span>
* <span data-ttu-id="eb8c7-211">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="eb8c7-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-212">Az.Network</span></span>
* <span data-ttu-id="eb8c7-213">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="eb8c7-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eb8c7-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eb8c7-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="eb8c7-215">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="eb8c7-216">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="eb8c7-217">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="eb8c7-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-218">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-219">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="eb8c7-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eb8c7-220">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="eb8c7-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="eb8c7-221">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="eb8c7-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="eb8c7-222">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="eb8c7-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-223">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-224">Adição de suporte para a camada de hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="eb8c7-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="eb8c7-225">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="eb8c7-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eb8c7-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-226">Az.Websites</span></span>
* <span data-ttu-id="eb8c7-227">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="eb8c7-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="eb8c7-228">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eb8c7-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-229">Az.Accounts</span></span>
* <span data-ttu-id="eb8c7-230">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eb8c7-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eb8c7-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-231">Az.AnalysisServices</span></span>
<span data-ttu-id="eb8c7-232">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-233">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-234">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="eb8c7-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="eb8c7-235">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="eb8c7-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="eb8c7-236">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-237">Az.RecoveryServices</span></span>
<span data-ttu-id="eb8c7-238">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-239">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-240">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="eb8c7-241">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="eb8c7-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eb8c7-242">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="eb8c7-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="eb8c7-243">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="eb8c7-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-244">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-245">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="eb8c7-246">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="eb8c7-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="eb8c7-247">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="eb8c7-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="eb8c7-248">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eb8c7-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-249">Az.Accounts</span></span>
* <span data-ttu-id="eb8c7-250">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="eb8c7-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eb8c7-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="eb8c7-252">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="eb8c7-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="eb8c7-254">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="eb8c7-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="eb8c7-255">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eb8c7-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-256">Az.Accounts</span></span>
* <span data-ttu-id="eb8c7-257">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="eb8c7-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eb8c7-258">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eb8c7-259">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="eb8c7-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="eb8c7-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="eb8c7-260">Az.Aks</span></span>
* <span data-ttu-id="eb8c7-261">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eb8c7-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-262">Az.Automation</span></span>
* <span data-ttu-id="eb8c7-263">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="eb8c7-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="eb8c7-264">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eb8c7-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eb8c7-265">Az.Cdn</span></span>
* <span data-ttu-id="eb8c7-266">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-267">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-268">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="eb8c7-269">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eb8c7-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="eb8c7-270">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="eb8c7-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="eb8c7-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eb8c7-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="eb8c7-272">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eb8c7-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb8c7-273">Az.DataFactory</span></span>
* <span data-ttu-id="eb8c7-274">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="eb8c7-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="eb8c7-276">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="eb8c7-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="eb8c7-277">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="eb8c7-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="eb8c7-278">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eb8c7-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eb8c7-279">Az.IotHub</span></span>
* <span data-ttu-id="eb8c7-280">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eb8c7-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eb8c7-281">Az.KeyVault</span></span>
* <span data-ttu-id="eb8c7-282">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-283">Az.Network</span></span>
* <span data-ttu-id="eb8c7-284">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-285">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-286">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="eb8c7-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="eb8c7-287">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="eb8c7-288">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="eb8c7-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="eb8c7-289">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="eb8c7-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="eb8c7-290">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="eb8c7-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="eb8c7-291">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="eb8c7-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="eb8c7-292">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="eb8c7-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eb8c7-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eb8c7-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="eb8c7-294">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="eb8c7-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="eb8c7-295">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-295">Fix some error messages.</span></span>
* <span data-ttu-id="eb8c7-296">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="eb8c7-297">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eb8c7-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eb8c7-298">Az.SignalR</span></span>
* <span data-ttu-id="eb8c7-299">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-300">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-301">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eb8c7-302">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="eb8c7-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="eb8c7-303">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="eb8c7-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="eb8c7-304">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="eb8c7-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eb8c7-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-305">Az.Storage</span></span>
* <span data-ttu-id="eb8c7-306">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eb8c7-307">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="eb8c7-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="eb8c7-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="eb8c7-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="eb8c7-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="eb8c7-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eb8c7-310">Az.TrafficManager</span></span>
* <span data-ttu-id="eb8c7-311">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eb8c7-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-312">Az.Websites</span></span>
* <span data-ttu-id="eb8c7-313">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="eb8c7-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eb8c7-314">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="eb8c7-315">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="eb8c7-316">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="eb8c7-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eb8c7-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-317">Az.Accounts</span></span>
* <span data-ttu-id="eb8c7-318">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="eb8c7-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-319">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-320">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="eb8c7-321">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="eb8c7-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="eb8c7-322">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="eb8c7-324">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="eb8c7-325">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="eb8c7-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eb8c7-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eb8c7-326">Az.EventGrid</span></span>
* <span data-ttu-id="eb8c7-327">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="eb8c7-328">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="eb8c7-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="eb8c7-329">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="eb8c7-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eb8c7-330">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="eb8c7-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eb8c7-331">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eb8c7-332">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="eb8c7-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="eb8c7-333">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="eb8c7-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eb8c7-334">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="eb8c7-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eb8c7-335">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eb8c7-336">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="eb8c7-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="eb8c7-337">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="eb8c7-338">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eb8c7-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eb8c7-339">Az.IotHub</span></span>
* <span data-ttu-id="eb8c7-340">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="eb8c7-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eb8c7-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eb8c7-341">Az.LogicApp</span></span>
* <span data-ttu-id="eb8c7-342">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="eb8c7-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-343">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-344">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="eb8c7-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="eb8c7-345">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="eb8c7-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="eb8c7-346">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb8c7-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eb8c7-347">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="eb8c7-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="eb8c7-348">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="eb8c7-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="eb8c7-349">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="eb8c7-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eb8c7-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eb8c7-350">Az.SignalR</span></span>
* <span data-ttu-id="eb8c7-351">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-352">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-353">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eb8c7-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-354">Az.Storage</span></span>
* <span data-ttu-id="eb8c7-355">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="eb8c7-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="eb8c7-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb8c7-356">New-AzStorageContext</span></span>
* <span data-ttu-id="eb8c7-357">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="eb8c7-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="eb8c7-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eb8c7-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-359">Az.Websites</span></span>
* <span data-ttu-id="eb8c7-360">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="eb8c7-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="eb8c7-361">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="eb8c7-362">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="eb8c7-363">Geral</span><span class="sxs-lookup"><span data-stu-id="eb8c7-363">General</span></span>

- <span data-ttu-id="eb8c7-364">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="eb8c7-364">General Availability of Az Module</span></span>
- <span data-ttu-id="eb8c7-365">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-365">Online help for each module</span></span>
- <span data-ttu-id="eb8c7-366">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="eb8c7-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="eb8c7-367">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="eb8c7-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="eb8c7-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-368">Az.Accounts</span></span>
- <span data-ttu-id="eb8c7-369">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="eb8c7-370">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="eb8c7-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eb8c7-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb8c7-371">Az.ApiManagement</span></span>
- <span data-ttu-id="eb8c7-372">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="eb8c7-372">Fixes for #7002</span></span>
- <span data-ttu-id="eb8c7-373">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="eb8c7-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eb8c7-374">Az.Batch</span></span>
- <span data-ttu-id="eb8c7-375">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="eb8c7-376">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="eb8c7-377">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="eb8c7-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="eb8c7-378">Az.Billing</span></span>
- <span data-ttu-id="eb8c7-379">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="eb8c7-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-380">Az.CognitivServices</span></span>
- <span data-ttu-id="eb8c7-381">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="eb8c7-382">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="eb8c7-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eb8c7-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="eb8c7-384">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="eb8c7-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="eb8c7-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eb8c7-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="eb8c7-386">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="eb8c7-388">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="eb8c7-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eb8c7-389">Az.Monitor</span></span>
- <span data-ttu-id="eb8c7-390">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="eb8c7-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eb8c7-391">Az.KeyVault</span></span>
- <span data-ttu-id="eb8c7-392">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="eb8c7-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="eb8c7-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="eb8c7-393">Az.MachineLearning</span></span>
- <span data-ttu-id="eb8c7-394">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="eb8c7-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="eb8c7-395">Az.Media</span></span>
- <span data-ttu-id="eb8c7-396">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="eb8c7-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eb8c7-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-397">Az.Network</span></span>
<span data-ttu-id="eb8c7-398">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="eb8c7-399">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="eb8c7-399">New cmdlets added:</span></span>
        - <span data-ttu-id="eb8c7-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eb8c7-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="eb8c7-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="eb8c7-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb8c7-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="eb8c7-408">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="eb8c7-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb8c7-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="eb8c7-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb8c7-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eb8c7-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb8c7-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eb8c7-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eb8c7-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="eb8c7-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="eb8c7-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="eb8c7-414">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="eb8c7-415">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eb8c7-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="eb8c7-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eb8c7-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eb8c7-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eb8c7-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eb8c7-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eb8c7-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="eb8c7-419">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eb8c7-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="eb8c7-420">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="eb8c7-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eb8c7-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="eb8c7-422">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="eb8c7-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-423">Az.Profile</span></span>
- <span data-ttu-id="eb8c7-424">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eb8c7-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="eb8c7-426">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="eb8c7-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-427">Az.Resources</span></span>
- <span data-ttu-id="eb8c7-428">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eb8c7-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eb8c7-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="eb8c7-430">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="eb8c7-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="eb8c7-431">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="eb8c7-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="eb8c7-432">Az.SIgnalR</span></span>
- <span data-ttu-id="eb8c7-433">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="eb8c7-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="eb8c7-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-434">Az.Sql</span></span>
- <span data-ttu-id="eb8c7-435">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="eb8c7-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="eb8c7-436">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="eb8c7-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="eb8c7-437">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="eb8c7-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-438">Az.Storage</span></span>
- <span data-ttu-id="eb8c7-439">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eb8c7-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-440">Az.Websites</span></span>
- <span data-ttu-id="eb8c7-441">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="eb8c7-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="eb8c7-442">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="eb8c7-443">Geral</span><span class="sxs-lookup"><span data-stu-id="eb8c7-443">General</span></span>

* <span data-ttu-id="eb8c7-444">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="eb8c7-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="eb8c7-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-445">Az.Compute</span></span>

* <span data-ttu-id="eb8c7-446">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="eb8c7-448">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="eb8c7-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="eb8c7-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="eb8c7-449">Az.FrontDoor</span></span>

* <span data-ttu-id="eb8c7-450">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="eb8c7-450">Fixed some broken links</span></span>
    - <span data-ttu-id="eb8c7-451">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="eb8c7-452">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eb8c7-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="eb8c7-454">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="eb8c7-455">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="eb8c7-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-456">Az.Resources</span></span>

* <span data-ttu-id="eb8c7-457">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="eb8c7-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="eb8c7-458">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="eb8c7-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-459">Az.Sql</span></span>

* <span data-ttu-id="eb8c7-460">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="eb8c7-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="eb8c7-461">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="eb8c7-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="eb8c7-462">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="eb8c7-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-463">Az.Storage</span></span>

* <span data-ttu-id="eb8c7-464">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="eb8c7-465">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="eb8c7-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="eb8c7-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eb8c7-467">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="eb8c7-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="eb8c7-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eb8c7-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="eb8c7-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eb8c7-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eb8c7-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-470">Az.Websites</span></span>

* <span data-ttu-id="eb8c7-471">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eb8c7-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="eb8c7-472">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="eb8c7-473">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="eb8c7-474">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eb8c7-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb8c7-475">Az.ApiManagement</span></span>
* <span data-ttu-id="eb8c7-476">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="eb8c7-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eb8c7-477">Az.Automation</span></span>
* <span data-ttu-id="eb8c7-478">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="eb8c7-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="eb8c7-479">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="eb8c7-480">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="eb8c7-481">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="eb8c7-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="eb8c7-482">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="eb8c7-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="eb8c7-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-483">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-484">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="eb8c7-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="eb8c7-485">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eb8c7-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="eb8c7-487">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="eb8c7-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eb8c7-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="eb8c7-489">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="eb8c7-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eb8c7-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-490">Az.Network</span></span>
* <span data-ttu-id="eb8c7-491">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="eb8c7-492">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="eb8c7-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="eb8c7-493">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="eb8c7-494">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb8c7-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="eb8c7-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="eb8c7-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eb8c7-496">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="eb8c7-497">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="eb8c7-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="eb8c7-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eb8c7-499">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="eb8c7-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="eb8c7-500">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="eb8c7-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="eb8c7-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="eb8c7-501">Az.Relay</span></span>
* <span data-ttu-id="eb8c7-502">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="eb8c7-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-503">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-504">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="eb8c7-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="eb8c7-505">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="eb8c7-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="eb8c7-506">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="eb8c7-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eb8c7-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eb8c7-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="eb8c7-508">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="eb8c7-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="eb8c7-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-509">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-510">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="eb8c7-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="eb8c7-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eb8c7-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eb8c7-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eb8c7-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eb8c7-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eb8c7-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8c7-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eb8c7-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8c7-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eb8c7-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8c7-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eb8c7-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8c7-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="eb8c7-519">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="eb8c7-520">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="eb8c7-521">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="eb8c7-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eb8c7-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eb8c7-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="eb8c7-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="eb8c7-526">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eb8c7-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="eb8c7-527">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eb8c7-528">Geral</span><span class="sxs-lookup"><span data-stu-id="eb8c7-528">General</span></span>
* <span data-ttu-id="eb8c7-529">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="eb8c7-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="eb8c7-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-530">Az.Profile</span></span>
* <span data-ttu-id="eb8c7-531">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eb8c7-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="eb8c7-532">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="eb8c7-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="eb8c7-533">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="eb8c7-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="eb8c7-534">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="eb8c7-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="eb8c7-535">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="eb8c7-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="eb8c7-536">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="eb8c7-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="eb8c7-537">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="eb8c7-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="eb8c7-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="eb8c7-539">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-540">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-541">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="eb8c7-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="eb8c7-542">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="eb8c7-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="eb8c7-543">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="eb8c7-545">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="eb8c7-546">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="eb8c7-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="eb8c7-547">Az.Insights</span></span>
* <span data-ttu-id="eb8c7-548">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="eb8c7-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="eb8c7-549">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="eb8c7-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="eb8c7-550">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="eb8c7-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="eb8c7-551">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="eb8c7-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-552">Az.Network</span></span>
* <span data-ttu-id="eb8c7-553">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="eb8c7-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="eb8c7-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb8c7-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="eb8c7-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eb8c7-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="eb8c7-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eb8c7-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="eb8c7-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="eb8c7-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eb8c7-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb8c7-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eb8c7-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eb8c7-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eb8c7-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eb8c7-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="eb8c7-561">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="eb8c7-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-562">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-563">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="eb8c7-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="eb8c7-564">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="eb8c7-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eb8c7-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eb8c7-565">Az.ServiceBus</span></span>
* <span data-ttu-id="eb8c7-566">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eb8c7-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eb8c7-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="eb8c7-568">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="eb8c7-569">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="eb8c7-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="eb8c7-570">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="eb8c7-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="eb8c7-571">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="eb8c7-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="eb8c7-572">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="eb8c7-573">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="eb8c7-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-574">Az.Profile</span></span>
* <span data-ttu-id="eb8c7-575">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="eb8c7-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="eb8c7-576">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eb8c7-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-577">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-578">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="eb8c7-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="eb8c7-579">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eb8c7-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eb8c7-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="eb8c7-581">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="eb8c7-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="eb8c7-582">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="eb8c7-583">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eb8c7-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eb8c7-585">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-586">Az.Network</span></span>
* <span data-ttu-id="eb8c7-587">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="eb8c7-588">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-589">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-590">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="eb8c7-591">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="eb8c7-592">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="eb8c7-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-593">Azure.Storage</span></span>
* <span data-ttu-id="eb8c7-594">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="eb8c7-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="eb8c7-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eb8c7-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eb8c7-597">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="eb8c7-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="eb8c7-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="eb8c7-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eb8c7-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="eb8c7-600">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eb8c7-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eb8c7-601">Az.Compute</span></span>
* <span data-ttu-id="eb8c7-602">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="eb8c7-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="eb8c7-603">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="eb8c7-604">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="eb8c7-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="eb8c7-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eb8c7-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="eb8c7-606">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eb8c7-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eb8c7-607">Az.Network</span></span>
* <span data-ttu-id="eb8c7-608">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="eb8c7-609">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="eb8c7-609">new cmdlets added</span></span>
    - <span data-ttu-id="eb8c7-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="eb8c7-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="eb8c7-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="eb8c7-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eb8c7-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="eb8c7-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="eb8c7-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="eb8c7-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8c7-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="eb8c7-616">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="eb8c7-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="eb8c7-617">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="eb8c7-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="eb8c7-618">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="eb8c7-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="eb8c7-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eb8c7-619">Az.RedisCache</span></span>
* <span data-ttu-id="eb8c7-620">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="eb8c7-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="eb8c7-621">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="eb8c7-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="eb8c7-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eb8c7-622">Az.Resources</span></span>
* <span data-ttu-id="eb8c7-623">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb8c7-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eb8c7-624">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="eb8c7-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="eb8c7-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eb8c7-625">Az.Sql</span></span>
* <span data-ttu-id="eb8c7-626">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="eb8c7-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eb8c7-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eb8c7-627">Az.Websites</span></span>
* <span data-ttu-id="eb8c7-628">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="eb8c7-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="eb8c7-629">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="eb8c7-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="eb8c7-630">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="eb8c7-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="eb8c7-631">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="eb8c7-631">Initial Release</span></span>