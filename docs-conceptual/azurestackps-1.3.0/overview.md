# <a name="azure-stack-module-130"></a><span data-ttu-id="3e7df-101">Módulo Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="3e7df-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="3e7df-102">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="3e7df-102">Requirements:</span></span>
<span data-ttu-id="3e7df-103">A versão mínima suportada do Azure Stack é 1804.</span><span class="sxs-lookup"><span data-stu-id="3e7df-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="3e7df-104">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="3e7df-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="3e7df-105">Problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="3e7df-105">Known issues:</span></span>

- <span data-ttu-id="3e7df-106">Fechar o Alerta requer a versão Azure Stack 1803</span><span class="sxs-lookup"><span data-stu-id="3e7df-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="3e7df-107">Alguns cmdlets de armazenamento requerem a versão Azure Stack 1804</span><span class="sxs-lookup"><span data-stu-id="3e7df-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="3e7df-108">O New-AzsOffer não permite criar uma oferta com o estado público.</span><span class="sxs-lookup"><span data-stu-id="3e7df-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="3e7df-109">O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="3e7df-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="3e7df-110">Um Pool de IPs não pode ser removido sem uma reimplantação</span><span class="sxs-lookup"><span data-stu-id="3e7df-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="3e7df-111">Alterações significativas</span><span class="sxs-lookup"><span data-stu-id="3e7df-111">Breaking Changes</span></span>
<span data-ttu-id="3e7df-112">Todas as alterações significativas migrando de 1.2.11 estão documentadas aqui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="3e7df-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="3e7df-113">Instalar</span><span class="sxs-lookup"><span data-stu-id="3e7df-113">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="3e7df-114">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="3e7df-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="3e7df-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="3e7df-115">Azure Bridge</span></span>
<span data-ttu-id="3e7df-116">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e7df-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="3e7df-117">Backup</span><span class="sxs-lookup"><span data-stu-id="3e7df-117">Backup</span></span>
<span data-ttu-id="3e7df-118">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="3e7df-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="3e7df-119">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="3e7df-119">Configure where backups are stored</span></span>
- <span data-ttu-id="3e7df-120">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="3e7df-120">Perform backups</span></span>
- <span data-ttu-id="3e7df-121">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="3e7df-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="3e7df-122">Comércio</span><span class="sxs-lookup"><span data-stu-id="3e7df-122">Commerce</span></span>
<span data-ttu-id="3e7df-123">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="3e7df-124">Computação</span><span class="sxs-lookup"><span data-stu-id="3e7df-124">Compute</span></span>
<span data-ttu-id="3e7df-125">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3e7df-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="3e7df-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="3e7df-126">Fabric</span></span>
<span data-ttu-id="3e7df-127">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="3e7df-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="3e7df-128">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="3e7df-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="3e7df-129">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="3e7df-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="3e7df-130">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="3e7df-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="3e7df-131">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="3e7df-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="3e7df-132">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="3e7df-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="3e7df-133">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="3e7df-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="3e7df-134">Galeria</span><span class="sxs-lookup"><span data-stu-id="3e7df-134">Gallery</span></span>
<span data-ttu-id="3e7df-135">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="3e7df-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="3e7df-136">Infrastructure Insights</span></span>
<span data-ttu-id="3e7df-137">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="3e7df-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="3e7df-138">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3e7df-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="3e7df-139">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="3e7df-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="3e7df-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="3e7df-140">KeyVault</span></span>
<span data-ttu-id="3e7df-141">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3e7df-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="3e7df-142">Rede</span><span class="sxs-lookup"><span data-stu-id="3e7df-142">Network</span></span>
<span data-ttu-id="3e7df-143">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="3e7df-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="3e7df-144">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="3e7df-144">Management of network quotas</span></span>
- <span data-ttu-id="3e7df-145">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="3e7df-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="3e7df-146">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="3e7df-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="3e7df-147">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="3e7df-147">Storage</span></span>
<span data-ttu-id="3e7df-148">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="3e7df-149">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="3e7df-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="3e7df-150">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3e7df-150">Manage storage quotas</span></span>
- <span data-ttu-id="3e7df-151">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="3e7df-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="3e7df-152">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="3e7df-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="3e7df-153">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="3e7df-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="3e7df-154">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="3e7df-154">View information about the individual storage components</span></span>
- <span data-ttu-id="3e7df-155">Exibir informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="3e7df-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="3e7df-156">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="3e7df-156">Subscription Admin</span></span>
<span data-ttu-id="3e7df-157">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="3e7df-158">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="3e7df-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="3e7df-159">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="3e7df-159">Manage plans and offers</span></span>
- <span data-ttu-id="3e7df-160">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="3e7df-160">View usage and performance information</span></span>
- <span data-ttu-id="3e7df-161">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="3e7df-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="3e7df-162">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3e7df-162">Subscription</span></span>
<span data-ttu-id="3e7df-163">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="3e7df-164">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="3e7df-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="3e7df-165">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="3e7df-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="3e7df-166">Atualizar</span><span class="sxs-lookup"><span data-stu-id="3e7df-166">Update</span></span>
<span data-ttu-id="3e7df-167">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3e7df-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="3e7df-168">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="3e7df-168">In this module administrators can:</span></span>
- <span data-ttu-id="3e7df-169">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="3e7df-169">List and install available updates</span></span>
- <span data-ttu-id="3e7df-170">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="3e7df-170">Resume interrupted updates</span></span>
- <span data-ttu-id="3e7df-171">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="3e7df-171">View installed updates</span></span>
