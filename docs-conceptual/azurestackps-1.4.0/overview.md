# <a name="azure-stack-module-140"></a><span data-ttu-id="7babd-101">Módulo do Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="7babd-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="7babd-102">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="7babd-102">Requirements:</span></span>
<span data-ttu-id="7babd-103">A versão mínima suportada do Azure Stack é 1804.</span><span class="sxs-lookup"><span data-stu-id="7babd-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="7babd-104">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="7babd-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="7babd-105">Problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="7babd-105">Known issues:</span></span>

- <span data-ttu-id="7babd-106">Fechar o Alerta requer a versão Azure Stack 1803</span><span class="sxs-lookup"><span data-stu-id="7babd-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="7babd-107">O New-AzsOffer não permite criar uma oferta com o estado público.</span><span class="sxs-lookup"><span data-stu-id="7babd-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="7babd-108">O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="7babd-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="7babd-109">Um Pool de IPs não pode ser removido sem uma reimplantação</span><span class="sxs-lookup"><span data-stu-id="7babd-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="7babd-110">Alterações significativas</span><span class="sxs-lookup"><span data-stu-id="7babd-110">Breaking Changes</span></span>
<span data-ttu-id="7babd-111">Não há nenhuma alteração significativa a partir da versão 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="7babd-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="7babd-112">Todas as alterações significativas migrando de 1.2.11 estão documentadas aqui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="7babd-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="7babd-113">Instalar</span><span class="sxs-lookup"><span data-stu-id="7babd-113">Install</span></span>
```
# 1.4.0 can be installed side by side with 1.3.0
# Remove previous version 1.2.11
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="7babd-114">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="7babd-114">Release Notes</span></span>
    * <span data-ttu-id="7babd-115">O Azure Stack versão 1.4.0 não tem alterações significativas a partir da versão anterior 1.3.0</span><span class="sxs-lookup"><span data-stu-id="7babd-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="7babd-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="7babd-117">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="7babd-119">Novos parâmetros adicionados, BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays, no cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="7babd-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="7babd-120">Um cmdlet New-EncyptionKeyBase64 adicionado para facilitar a criação da chave de criptografia</span><span class="sxs-lookup"><span data-stu-id="7babd-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="7babd-121">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="7babd-123">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="7babd-125">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="7babd-126">Um cmdlet Add-AzsScaleUnitNode adicionado para permitir ao administrador adicionar novos nós da unidade de escala ao carimbo de data azurestack</span><span class="sxs-lookup"><span data-stu-id="7babd-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="7babd-127">Um cmdlet adicionado e New-AzsScaleUnitNodeObject para facilitar a criação dos objetos de parâmetro da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="7babd-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="7babd-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="7babd-129">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="7babd-131">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="7babd-133">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="7babd-135">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="7babd-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="7babd-137">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7babd-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="7babd-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="7babd-139">Um cmdlet Move-AzsSubscription adicionado para mover assinaturas entre as ofertas do provedor delegadas</span><span class="sxs-lookup"><span data-stu-id="7babd-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="7babd-140">Um cmdlet Test-AzsMoveSubscription adicionado para validar se as assinaturas do usuário podem ser movidas entre as ofertas do provedor delegadas</span><span class="sxs-lookup"><span data-stu-id="7babd-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="7babd-141">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="7babd-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="7babd-142">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="7babd-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="7babd-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="7babd-143">Azure Bridge</span></span>
<span data-ttu-id="7babd-144">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="7babd-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="7babd-145">Backup</span><span class="sxs-lookup"><span data-stu-id="7babd-145">Backup</span></span>
<span data-ttu-id="7babd-146">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="7babd-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="7babd-147">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="7babd-147">Configure where backups are stored</span></span>
- <span data-ttu-id="7babd-148">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="7babd-148">Perform backups</span></span>
- <span data-ttu-id="7babd-149">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="7babd-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="7babd-150">Comércio</span><span class="sxs-lookup"><span data-stu-id="7babd-150">Commerce</span></span>
<span data-ttu-id="7babd-151">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="7babd-152">Computação</span><span class="sxs-lookup"><span data-stu-id="7babd-152">Compute</span></span>
<span data-ttu-id="7babd-153">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7babd-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="7babd-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="7babd-154">Fabric</span></span>
<span data-ttu-id="7babd-155">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="7babd-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="7babd-156">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="7babd-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="7babd-157">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="7babd-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="7babd-158">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="7babd-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="7babd-159">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="7babd-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="7babd-160">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="7babd-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="7babd-161">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="7babd-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="7babd-162">Galeria</span><span class="sxs-lookup"><span data-stu-id="7babd-162">Gallery</span></span>
<span data-ttu-id="7babd-163">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="7babd-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="7babd-164">Infrastructure Insights</span></span>
<span data-ttu-id="7babd-165">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="7babd-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="7babd-166">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="7babd-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="7babd-167">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="7babd-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="7babd-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7babd-168">KeyVault</span></span>
<span data-ttu-id="7babd-169">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7babd-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="7babd-170">Rede</span><span class="sxs-lookup"><span data-stu-id="7babd-170">Network</span></span>
<span data-ttu-id="7babd-171">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="7babd-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="7babd-172">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="7babd-172">Management of network quotas</span></span>
- <span data-ttu-id="7babd-173">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="7babd-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="7babd-174">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="7babd-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="7babd-175">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="7babd-175">Storage</span></span>
<span data-ttu-id="7babd-176">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="7babd-177">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="7babd-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="7babd-178">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7babd-178">Manage storage quotas</span></span>
- <span data-ttu-id="7babd-179">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="7babd-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="7babd-180">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="7babd-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="7babd-181">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="7babd-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="7babd-182">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="7babd-182">View information about the individual storage components</span></span>
- <span data-ttu-id="7babd-183">Exibir informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="7babd-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="7babd-184">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="7babd-184">Subscription Admin</span></span>
<span data-ttu-id="7babd-185">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="7babd-186">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="7babd-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="7babd-187">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="7babd-187">Manage plans and offers</span></span>
- <span data-ttu-id="7babd-188">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="7babd-188">View usage and performance information</span></span>
- <span data-ttu-id="7babd-189">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="7babd-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="7babd-190">Assinatura</span><span class="sxs-lookup"><span data-stu-id="7babd-190">Subscription</span></span>
<span data-ttu-id="7babd-191">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="7babd-192">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="7babd-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="7babd-193">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="7babd-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="7babd-194">Atualizar</span><span class="sxs-lookup"><span data-stu-id="7babd-194">Update</span></span>
<span data-ttu-id="7babd-195">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7babd-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="7babd-196">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="7babd-196">In this module administrators can:</span></span>
- <span data-ttu-id="7babd-197">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="7babd-197">List and install available updates</span></span>
- <span data-ttu-id="7babd-198">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="7babd-198">Resume interrupted updates</span></span>
- <span data-ttu-id="7babd-199">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="7babd-199">View installed updates</span></span>
