---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363954"
---
## <a name="170---april-2019"></a><span data-ttu-id="aba25-101">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aba25-102">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="aba25-102">Highlights since the last major release</span></span>
* <span data-ttu-id="aba25-103">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="aba25-103">General availability of `Az` module</span></span>
* <span data-ttu-id="aba25-104">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aba25-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aba25-105">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aba25-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aba25-106">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aba25-107">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aba25-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aba25-108">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aba25-109">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="aba25-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aba25-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-110">Az.Accounts</span></span>
* <span data-ttu-id="aba25-111">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="aba25-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aba25-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aba25-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="aba25-113">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="aba25-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="aba25-114">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="aba25-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aba25-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-115">Az.Automation</span></span>
* <span data-ttu-id="aba25-116">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="aba25-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="aba25-117">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="aba25-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="aba25-118">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-119">Az.Compute</span></span>
* <span data-ttu-id="aba25-120">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="aba25-121">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="aba25-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="aba25-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="aba25-123">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="aba25-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aba25-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aba25-124">Az.DataFactory</span></span>
* <span data-ttu-id="aba25-125">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="aba25-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="aba25-126">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aba25-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-127">Az.Resources</span></span>
* <span data-ttu-id="aba25-128">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="aba25-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="aba25-129">Melhorar o tratamento de erros para “Test-AzDeployment” e “Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="aba25-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="aba25-130">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="aba25-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="aba25-131">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aba25-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="aba25-132">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="aba25-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="aba25-133">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aba25-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-134">Az.Sql</span></span>
* <span data-ttu-id="aba25-135">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="aba25-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aba25-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-136">Az.Storage</span></span>
* <span data-ttu-id="aba25-137">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="aba25-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aba25-138">New-AzStorageContext</span></span>
* <span data-ttu-id="aba25-139">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="aba25-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="aba25-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aba25-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aba25-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aba25-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aba25-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="aba25-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="aba25-144">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="aba25-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="aba25-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aba25-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aba25-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aba25-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aba25-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aba25-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="aba25-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aba25-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="aba25-149">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aba25-150">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="aba25-150">Highlights since the last major release</span></span>
* <span data-ttu-id="aba25-151">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="aba25-151">General availability of `Az` module</span></span>
* <span data-ttu-id="aba25-152">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aba25-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aba25-153">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aba25-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aba25-154">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aba25-155">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aba25-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aba25-156">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aba25-157">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="aba25-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aba25-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-158">Az.Automation</span></span>
* <span data-ttu-id="aba25-159">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="aba25-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="aba25-160">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="aba25-160">Dynamic grouping</span></span>
    * <span data-ttu-id="aba25-161">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="aba25-161">Pre-Post script</span></span>
    * <span data-ttu-id="aba25-162">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="aba25-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-163">Az.Compute</span></span>
* <span data-ttu-id="aba25-164">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="aba25-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="aba25-165">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="aba25-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aba25-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aba25-166">Az.KeyVault</span></span>
* <span data-ttu-id="aba25-167">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="aba25-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-168">Az.Network</span></span>
* <span data-ttu-id="aba25-169">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="aba25-170">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="aba25-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="aba25-172">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="aba25-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="aba25-173">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="aba25-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-174">Az.Resources</span></span>
* <span data-ttu-id="aba25-175">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aba25-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="aba25-176">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="aba25-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-177">Az.Sql</span></span>
* <span data-ttu-id="aba25-178">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="aba25-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aba25-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-179">Az.Storage</span></span>
* <span data-ttu-id="aba25-180">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="aba25-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="aba25-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aba25-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aba25-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aba25-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aba25-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="aba25-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="aba25-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="aba25-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aba25-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aba25-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-187">Az.Websites</span></span>
* <span data-ttu-id="aba25-188">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="aba25-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="aba25-189">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aba25-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-190">Az.Accounts</span></span>
* <span data-ttu-id="aba25-191">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="aba25-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="aba25-192">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aba25-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-193">Az.Automation</span></span>
* <span data-ttu-id="aba25-194">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="aba25-195">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="aba25-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="aba25-196">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="aba25-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aba25-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aba25-197">Az.Cdn</span></span>
* <span data-ttu-id="aba25-198">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="aba25-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-199">Az.Compute</span></span>
* <span data-ttu-id="aba25-200">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="aba25-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aba25-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aba25-201">Az.DataFactory</span></span>
* <span data-ttu-id="aba25-202">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="aba25-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aba25-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aba25-203">Az.LogicApp</span></span>
* <span data-ttu-id="aba25-204">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="aba25-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-205">Az.Network</span></span>
* <span data-ttu-id="aba25-206">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="aba25-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="aba25-208">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="aba25-209">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="aba25-209">SDK Update</span></span>
* <span data-ttu-id="aba25-210">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aba25-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="aba25-211">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aba25-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-212">Az.Resources</span></span>
* <span data-ttu-id="aba25-213">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="aba25-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="aba25-214">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="aba25-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="aba25-215">Corrigir problema ao redirecionar o resultado de `Get-AzResource` para</span><span class="sxs-lookup"><span data-stu-id="aba25-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="aba25-216">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="aba25-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="aba25-217">Corrigir problema com a alteração no tipo de dados JSON ao executar</span><span class="sxs-lookup"><span data-stu-id="aba25-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="aba25-218">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="aba25-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-219">Az.Sql</span></span>
* <span data-ttu-id="aba25-220">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="aba25-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="aba25-221">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="aba25-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aba25-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-222">Az.Storage</span></span>
* <span data-ttu-id="aba25-223">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="aba25-224">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="aba25-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aba25-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="aba25-226">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aba25-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-227">Az.Automation</span></span>
* <span data-ttu-id="aba25-228">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="aba25-229">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="aba25-230">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aba25-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aba25-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="aba25-232">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="aba25-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-233">Az.Compute</span></span>
* <span data-ttu-id="aba25-234">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="aba25-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="aba25-235">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="aba25-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="aba25-236">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="aba25-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="aba25-237">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="aba25-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aba25-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="aba25-239">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="aba25-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aba25-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aba25-240">Az.EventHub</span></span>
* <span data-ttu-id="aba25-241">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="aba25-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="aba25-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aba25-242">Az.KeyVault</span></span>
* <span data-ttu-id="aba25-243">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aba25-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aba25-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aba25-244">Az.LogicApp</span></span>
* <span data-ttu-id="aba25-245">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="aba25-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="aba25-246">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="aba25-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="aba25-247">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="aba25-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="aba25-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aba25-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aba25-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aba25-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aba25-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aba25-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aba25-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aba25-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="aba25-252">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="aba25-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="aba25-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aba25-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aba25-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aba25-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="aba25-257">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="aba25-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aba25-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aba25-258">Az.Monitor</span></span>
* <span data-ttu-id="aba25-259">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="aba25-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-260">Az.Network</span></span>
* <span data-ttu-id="aba25-261">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="aba25-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aba25-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aba25-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="aba25-263">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="aba25-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="aba25-264">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="aba25-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="aba25-265">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="aba25-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="aba25-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-266">Az.Resources</span></span>
* <span data-ttu-id="aba25-267">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aba25-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aba25-268">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aba25-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="aba25-269">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="aba25-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="aba25-270">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="aba25-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-271">Az.Sql</span></span>
* <span data-ttu-id="aba25-272">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="aba25-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="aba25-273">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="aba25-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aba25-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-274">Az.Websites</span></span>
* <span data-ttu-id="aba25-275">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="aba25-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="aba25-276">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aba25-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-277">Az.Accounts</span></span>
* <span data-ttu-id="aba25-278">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="aba25-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aba25-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aba25-279">Az.AnalysisServices</span></span>
<span data-ttu-id="aba25-280">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="aba25-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-281">Az.Compute</span></span>
* <span data-ttu-id="aba25-282">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="aba25-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="aba25-283">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="aba25-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="aba25-284">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="aba25-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-285">Az.RecoveryServices</span></span>
<span data-ttu-id="aba25-286">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="aba25-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-287">Az.Resources</span></span>
* <span data-ttu-id="aba25-288">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="aba25-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="aba25-289">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aba25-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aba25-290">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="aba25-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="aba25-291">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aba25-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-292">Az.Sql</span></span>
* <span data-ttu-id="aba25-293">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba25-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="aba25-294">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="aba25-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="aba25-295">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="aba25-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="aba25-296">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aba25-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-297">Az.Accounts</span></span>
* <span data-ttu-id="aba25-298">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="aba25-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aba25-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aba25-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="aba25-300">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="aba25-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="aba25-302">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="aba25-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="aba25-303">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aba25-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-304">Az.Accounts</span></span>
* <span data-ttu-id="aba25-305">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="aba25-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aba25-306">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aba25-307">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="aba25-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="aba25-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="aba25-308">Az.Aks</span></span>
* <span data-ttu-id="aba25-309">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aba25-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-310">Az.Automation</span></span>
* <span data-ttu-id="aba25-311">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="aba25-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="aba25-312">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aba25-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aba25-313">Az.Cdn</span></span>
* <span data-ttu-id="aba25-314">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-315">Az.Compute</span></span>
* <span data-ttu-id="aba25-316">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="aba25-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="aba25-317">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aba25-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="aba25-318">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="aba25-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="aba25-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aba25-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="aba25-320">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aba25-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aba25-321">Az.DataFactory</span></span>
* <span data-ttu-id="aba25-322">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="aba25-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aba25-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="aba25-324">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="aba25-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="aba25-325">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="aba25-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="aba25-326">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aba25-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aba25-327">Az.IotHub</span></span>
* <span data-ttu-id="aba25-328">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="aba25-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aba25-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aba25-329">Az.KeyVault</span></span>
* <span data-ttu-id="aba25-330">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-331">Az.Network</span></span>
* <span data-ttu-id="aba25-332">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-333">Az.Resources</span></span>
* <span data-ttu-id="aba25-334">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="aba25-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="aba25-335">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aba25-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="aba25-336">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="aba25-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="aba25-337">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="aba25-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="aba25-338">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="aba25-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="aba25-339">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="aba25-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="aba25-340">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="aba25-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aba25-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aba25-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="aba25-342">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="aba25-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="aba25-343">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="aba25-343">Fix some error messages.</span></span>
* <span data-ttu-id="aba25-344">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="aba25-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="aba25-345">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="aba25-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aba25-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aba25-346">Az.SignalR</span></span>
* <span data-ttu-id="aba25-347">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-348">Az.Sql</span></span>
* <span data-ttu-id="aba25-349">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aba25-350">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="aba25-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="aba25-351">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="aba25-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="aba25-352">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="aba25-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aba25-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-353">Az.Storage</span></span>
* <span data-ttu-id="aba25-354">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aba25-355">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="aba25-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="aba25-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aba25-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="aba25-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="aba25-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="aba25-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aba25-358">Az.TrafficManager</span></span>
* <span data-ttu-id="aba25-359">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aba25-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-360">Az.Websites</span></span>
* <span data-ttu-id="aba25-361">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="aba25-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aba25-362">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="aba25-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="aba25-363">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="aba25-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="aba25-364">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="aba25-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aba25-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-365">Az.Accounts</span></span>
* <span data-ttu-id="aba25-366">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="aba25-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-367">Az.Compute</span></span>
* <span data-ttu-id="aba25-368">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="aba25-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="aba25-369">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="aba25-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="aba25-370">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aba25-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="aba25-372">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="aba25-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="aba25-373">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="aba25-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aba25-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aba25-374">Az.EventGrid</span></span>
* <span data-ttu-id="aba25-375">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="aba25-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="aba25-376">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="aba25-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="aba25-377">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="aba25-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aba25-378">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="aba25-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aba25-379">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="aba25-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aba25-380">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="aba25-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="aba25-381">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="aba25-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aba25-382">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="aba25-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aba25-383">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="aba25-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aba25-384">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="aba25-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="aba25-385">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="aba25-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="aba25-386">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="aba25-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aba25-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aba25-387">Az.IotHub</span></span>
* <span data-ttu-id="aba25-388">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="aba25-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aba25-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aba25-389">Az.LogicApp</span></span>
* <span data-ttu-id="aba25-390">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="aba25-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-391">Az.Resources</span></span>
* <span data-ttu-id="aba25-392">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="aba25-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="aba25-393">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="aba25-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="aba25-394">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aba25-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aba25-395">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="aba25-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="aba25-396">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="aba25-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="aba25-397">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="aba25-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aba25-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aba25-398">Az.SignalR</span></span>
* <span data-ttu-id="aba25-399">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-400">Az.Sql</span></span>
* <span data-ttu-id="aba25-401">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="aba25-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aba25-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-402">Az.Storage</span></span>
* <span data-ttu-id="aba25-403">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="aba25-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="aba25-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aba25-404">New-AzStorageContext</span></span>
* <span data-ttu-id="aba25-405">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="aba25-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="aba25-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="aba25-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aba25-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-407">Az.Websites</span></span>
* <span data-ttu-id="aba25-408">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="aba25-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="aba25-409">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="aba25-410">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="aba25-411">Geral</span><span class="sxs-lookup"><span data-stu-id="aba25-411">General</span></span>

- <span data-ttu-id="aba25-412">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="aba25-412">General Availability of Az Module</span></span>
- <span data-ttu-id="aba25-413">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="aba25-413">Online help for each module</span></span>
- <span data-ttu-id="aba25-414">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="aba25-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="aba25-415">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="aba25-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="aba25-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-416">Az.Accounts</span></span>
- <span data-ttu-id="aba25-417">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aba25-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="aba25-418">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="aba25-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aba25-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba25-419">Az.ApiManagement</span></span>
- <span data-ttu-id="aba25-420">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="aba25-420">Fixes for #7002</span></span>
- <span data-ttu-id="aba25-421">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="aba25-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aba25-422">Az.Batch</span></span>
- <span data-ttu-id="aba25-423">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="aba25-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="aba25-424">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="aba25-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="aba25-425">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="aba25-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aba25-426">Az.Billing</span></span>
- <span data-ttu-id="aba25-427">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="aba25-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="aba25-428">Az.CognitivServices</span></span>
- <span data-ttu-id="aba25-429">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="aba25-430">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="aba25-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aba25-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="aba25-432">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="aba25-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="aba25-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aba25-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="aba25-434">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aba25-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="aba25-436">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="aba25-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aba25-437">Az.Monitor</span></span>
- <span data-ttu-id="aba25-438">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="aba25-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aba25-439">Az.KeyVault</span></span>
- <span data-ttu-id="aba25-440">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="aba25-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="aba25-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aba25-441">Az.MachineLearning</span></span>
- <span data-ttu-id="aba25-442">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="aba25-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="aba25-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aba25-443">Az.Media</span></span>
- <span data-ttu-id="aba25-444">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aba25-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aba25-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-445">Az.Network</span></span>
<span data-ttu-id="aba25-446">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="aba25-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="aba25-447">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="aba25-447">New cmdlets added:</span></span>
        - <span data-ttu-id="aba25-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="aba25-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="aba25-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="aba25-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="aba25-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="aba25-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="aba25-456">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aba25-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="aba25-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aba25-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="aba25-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aba25-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aba25-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aba25-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aba25-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="aba25-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="aba25-462">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="aba25-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="aba25-463">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aba25-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="aba25-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aba25-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aba25-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aba25-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aba25-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aba25-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="aba25-467">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aba25-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="aba25-468">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="aba25-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aba25-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="aba25-470">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="aba25-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aba25-471">Az.Profile</span></span>
- <span data-ttu-id="aba25-472">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aba25-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="aba25-474">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="aba25-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-475">Az.Resources</span></span>
- <span data-ttu-id="aba25-476">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aba25-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aba25-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="aba25-478">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="aba25-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="aba25-479">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="aba25-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aba25-480">Az.SIgnalR</span></span>
- <span data-ttu-id="aba25-481">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aba25-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="aba25-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-482">Az.Sql</span></span>
- <span data-ttu-id="aba25-483">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="aba25-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="aba25-484">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="aba25-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="aba25-485">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="aba25-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-486">Az.Storage</span></span>
- <span data-ttu-id="aba25-487">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aba25-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-488">Az.Websites</span></span>
- <span data-ttu-id="aba25-489">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="aba25-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="aba25-490">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="aba25-491">Geral</span><span class="sxs-lookup"><span data-stu-id="aba25-491">General</span></span>

* <span data-ttu-id="aba25-492">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="aba25-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="aba25-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-493">Az.Compute</span></span>

* <span data-ttu-id="aba25-494">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="aba25-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aba25-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="aba25-496">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="aba25-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="aba25-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aba25-497">Az.FrontDoor</span></span>

* <span data-ttu-id="aba25-498">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="aba25-498">Fixed some broken links</span></span>
    - <span data-ttu-id="aba25-499">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="aba25-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="aba25-500">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="aba25-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aba25-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aba25-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="aba25-502">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="aba25-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="aba25-503">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="aba25-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="aba25-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-504">Az.Resources</span></span>

* <span data-ttu-id="aba25-505">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="aba25-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="aba25-506">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="aba25-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="aba25-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-507">Az.Sql</span></span>

* <span data-ttu-id="aba25-508">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="aba25-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="aba25-509">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="aba25-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="aba25-510">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="aba25-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="aba25-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-511">Az.Storage</span></span>

* <span data-ttu-id="aba25-512">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="aba25-513">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="aba25-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="aba25-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aba25-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aba25-515">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="aba25-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="aba25-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aba25-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="aba25-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aba25-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aba25-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-518">Az.Websites</span></span>

* <span data-ttu-id="aba25-519">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="aba25-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="aba25-520">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="aba25-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="aba25-521">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="aba25-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="aba25-522">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aba25-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba25-523">Az.ApiManagement</span></span>
* <span data-ttu-id="aba25-524">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="aba25-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="aba25-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aba25-525">Az.Automation</span></span>
* <span data-ttu-id="aba25-526">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="aba25-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="aba25-527">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="aba25-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="aba25-528">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="aba25-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="aba25-529">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="aba25-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="aba25-530">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="aba25-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="aba25-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-531">Az.Compute</span></span>
* <span data-ttu-id="aba25-532">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="aba25-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="aba25-533">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="aba25-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aba25-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="aba25-535">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="aba25-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="aba25-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="aba25-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="aba25-537">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="aba25-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aba25-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-538">Az.Network</span></span>
* <span data-ttu-id="aba25-539">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="aba25-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="aba25-540">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="aba25-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="aba25-541">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="aba25-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="aba25-542">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aba25-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="aba25-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aba25-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aba25-544">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="aba25-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="aba25-545">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="aba25-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="aba25-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aba25-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aba25-547">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aba25-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="aba25-548">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="aba25-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="aba25-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aba25-549">Az.Relay</span></span>
* <span data-ttu-id="aba25-550">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="aba25-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="aba25-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-551">Az.Resources</span></span>
* <span data-ttu-id="aba25-552">Atualizar documentação de ajuda para os parâmetros relacionados à identidade de recurso em `New-AzureRmPolicyAssignment` e</span><span class="sxs-lookup"><span data-stu-id="aba25-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="aba25-553">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="aba25-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="aba25-554">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="aba25-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aba25-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aba25-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="aba25-556">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="aba25-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="aba25-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-557">Az.Sql</span></span>
* <span data-ttu-id="aba25-558">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="aba25-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="aba25-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aba25-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aba25-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aba25-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aba25-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aba25-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aba25-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aba25-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aba25-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aba25-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aba25-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aba25-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aba25-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="aba25-567">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="aba25-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="aba25-568">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="aba25-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="aba25-569">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="aba25-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="aba25-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aba25-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aba25-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aba25-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aba25-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aba25-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="aba25-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aba25-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="aba25-574">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="aba25-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="aba25-575">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aba25-576">Geral</span><span class="sxs-lookup"><span data-stu-id="aba25-576">General</span></span>
* <span data-ttu-id="aba25-577">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="aba25-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="aba25-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aba25-578">Az.Profile</span></span>
* <span data-ttu-id="aba25-579">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="aba25-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="aba25-580">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="aba25-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="aba25-581">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="aba25-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="aba25-582">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="aba25-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="aba25-583">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="aba25-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="aba25-584">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="aba25-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="aba25-585">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="aba25-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="aba25-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aba25-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="aba25-587">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="aba25-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-588">Az.Compute</span></span>
* <span data-ttu-id="aba25-589">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aba25-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="aba25-590">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="aba25-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="aba25-591">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="aba25-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aba25-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="aba25-593">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="aba25-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="aba25-594">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="aba25-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="aba25-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="aba25-595">Az.Insights</span></span>
* <span data-ttu-id="aba25-596">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="aba25-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="aba25-597">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="aba25-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="aba25-598">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="aba25-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="aba25-599">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="aba25-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-600">Az.Network</span></span>
* <span data-ttu-id="aba25-601">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="aba25-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="aba25-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="aba25-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="aba25-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="aba25-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="aba25-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aba25-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="aba25-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="aba25-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aba25-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="aba25-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aba25-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aba25-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aba25-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aba25-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="aba25-609">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="aba25-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-610">Az.Resources</span></span>
* <span data-ttu-id="aba25-611">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="aba25-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="aba25-612">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="aba25-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aba25-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aba25-613">Az.ServiceBus</span></span>
* <span data-ttu-id="aba25-614">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="aba25-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aba25-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aba25-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="aba25-616">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="aba25-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="aba25-617">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="aba25-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="aba25-618">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="aba25-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="aba25-619">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="aba25-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="aba25-620">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="aba25-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="aba25-621">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="aba25-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aba25-622">Az.Profile</span></span>
* <span data-ttu-id="aba25-623">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="aba25-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="aba25-624">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="aba25-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-625">Az.Compute</span></span>
* <span data-ttu-id="aba25-626">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="aba25-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="aba25-627">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="aba25-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aba25-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aba25-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="aba25-629">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="aba25-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="aba25-630">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aba25-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="aba25-631">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="aba25-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aba25-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="aba25-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aba25-633">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aba25-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-634">Az.Network</span></span>
* <span data-ttu-id="aba25-635">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="aba25-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="aba25-636">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="aba25-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-637">Az.Resources</span></span>
* <span data-ttu-id="aba25-638">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="aba25-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="aba25-639">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="aba25-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="aba25-640">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="aba25-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="aba25-641">Azure.Storage</span></span>
* <span data-ttu-id="aba25-642">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="aba25-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="aba25-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="aba25-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="aba25-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aba25-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aba25-645">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="aba25-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="aba25-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aba25-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="aba25-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aba25-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="aba25-648">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="aba25-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aba25-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aba25-649">Az.Compute</span></span>
* <span data-ttu-id="aba25-650">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="aba25-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="aba25-651">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="aba25-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="aba25-652">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="aba25-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="aba25-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aba25-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="aba25-654">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="aba25-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aba25-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aba25-655">Az.Network</span></span>
* <span data-ttu-id="aba25-656">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="aba25-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="aba25-657">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="aba25-657">new cmdlets added</span></span>
    - <span data-ttu-id="aba25-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aba25-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="aba25-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aba25-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="aba25-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aba25-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="aba25-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aba25-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="aba25-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="aba25-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="aba25-664">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="aba25-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="aba25-665">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="aba25-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="aba25-666">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="aba25-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aba25-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aba25-667">Az.RedisCache</span></span>
* <span data-ttu-id="aba25-668">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="aba25-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="aba25-669">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="aba25-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="aba25-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aba25-670">Az.Resources</span></span>
* <span data-ttu-id="aba25-671">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aba25-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aba25-672">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="aba25-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="aba25-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aba25-673">Az.Sql</span></span>
* <span data-ttu-id="aba25-674">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="aba25-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aba25-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aba25-675">Az.Websites</span></span>
* <span data-ttu-id="aba25-676">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="aba25-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="aba25-677">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="aba25-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="aba25-678">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="aba25-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="aba25-679">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="aba25-679">Initial Release</span></span>