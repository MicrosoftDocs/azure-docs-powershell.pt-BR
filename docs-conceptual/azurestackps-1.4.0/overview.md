---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178792"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="679c7-103">Módulo do Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="679c7-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="679c7-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="679c7-104">Requirements:</span></span>
<span data-ttu-id="679c7-105">A versão mínima suportada do Azure Stack é 1804.</span><span class="sxs-lookup"><span data-stu-id="679c7-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="679c7-106">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="679c7-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="679c7-107">Problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="679c7-107">Known issues:</span></span>

- <span data-ttu-id="679c7-108">Fechar o Alerta requer a versão Azure Stack 1803</span><span class="sxs-lookup"><span data-stu-id="679c7-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="679c7-109">O New-AzsOffer não permite criar uma oferta com o estado público.</span><span class="sxs-lookup"><span data-stu-id="679c7-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="679c7-110">O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="679c7-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="679c7-111">Um Pool de IPs não pode ser removido sem uma reimplantação</span><span class="sxs-lookup"><span data-stu-id="679c7-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="679c7-112">Alterações significativas</span><span class="sxs-lookup"><span data-stu-id="679c7-112">Breaking Changes</span></span>
<span data-ttu-id="679c7-113">Não há nenhuma alteração significativa a partir da versão 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="679c7-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="679c7-114">Todas as alterações significativas migrando de 1.2.11 estão documentadas aqui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="679c7-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="679c7-115">Instalar</span><span class="sxs-lookup"><span data-stu-id="679c7-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="679c7-116">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="679c7-116">Release Notes</span></span>
    * <span data-ttu-id="679c7-117">O Azure Stack versão 1.4.0 não tem alterações significativas a partir da versão anterior 1.3.0</span><span class="sxs-lookup"><span data-stu-id="679c7-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="679c7-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="679c7-119">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="679c7-121">Novos parâmetros adicionados, BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays, no cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="679c7-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="679c7-122">Um cmdlet New-EncyptionKeyBase64 adicionado para facilitar a criação da chave de criptografia</span><span class="sxs-lookup"><span data-stu-id="679c7-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="679c7-123">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="679c7-125">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="679c7-127">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="679c7-128">Um cmdlet Add-AzsScaleUnitNode adicionado para permitir ao administrador adicionar novos nós da unidade de escala ao carimbo de data azurestack</span><span class="sxs-lookup"><span data-stu-id="679c7-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="679c7-129">Um cmdlet adicionado e New-AzsScaleUnitNodeObject para facilitar a criação dos objetos de parâmetro da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="679c7-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="679c7-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="679c7-131">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="679c7-133">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="679c7-135">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="679c7-137">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="679c7-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="679c7-139">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="679c7-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="679c7-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="679c7-141">Um cmdlet Move-AzsSubscription adicionado para mover assinaturas entre as ofertas do provedor delegadas</span><span class="sxs-lookup"><span data-stu-id="679c7-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="679c7-142">Um cmdlet Test-AzsMoveSubscription adicionado para validar se as assinaturas do usuário podem ser movidas entre as ofertas do provedor delegadas</span><span class="sxs-lookup"><span data-stu-id="679c7-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="679c7-143">Correção do bug que retornou uma única página nos resultados com páginas</span><span class="sxs-lookup"><span data-stu-id="679c7-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="679c7-144">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="679c7-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="679c7-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="679c7-145">Azure Bridge</span></span>
<span data-ttu-id="679c7-146">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="679c7-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="679c7-147">Backup</span><span class="sxs-lookup"><span data-stu-id="679c7-147">Backup</span></span>
<span data-ttu-id="679c7-148">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="679c7-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="679c7-149">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="679c7-149">Configure where backups are stored</span></span>
- <span data-ttu-id="679c7-150">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="679c7-150">Perform backups</span></span>
- <span data-ttu-id="679c7-151">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="679c7-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="679c7-152">Comércio</span><span class="sxs-lookup"><span data-stu-id="679c7-152">Commerce</span></span>
<span data-ttu-id="679c7-153">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="679c7-154">Computação</span><span class="sxs-lookup"><span data-stu-id="679c7-154">Compute</span></span>
<span data-ttu-id="679c7-155">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="679c7-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="679c7-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="679c7-156">Fabric</span></span>
<span data-ttu-id="679c7-157">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="679c7-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="679c7-158">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="679c7-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="679c7-159">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="679c7-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="679c7-160">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="679c7-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="679c7-161">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="679c7-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="679c7-162">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="679c7-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="679c7-163">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="679c7-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="679c7-164">Galeria</span><span class="sxs-lookup"><span data-stu-id="679c7-164">Gallery</span></span>
<span data-ttu-id="679c7-165">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="679c7-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="679c7-166">Infrastructure Insights</span></span>
<span data-ttu-id="679c7-167">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="679c7-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="679c7-168">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="679c7-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="679c7-169">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="679c7-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="679c7-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="679c7-170">KeyVault</span></span>
<span data-ttu-id="679c7-171">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="679c7-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="679c7-172">Rede</span><span class="sxs-lookup"><span data-stu-id="679c7-172">Network</span></span>
<span data-ttu-id="679c7-173">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="679c7-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="679c7-174">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="679c7-174">Management of network quotas</span></span>
- <span data-ttu-id="679c7-175">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="679c7-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="679c7-176">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="679c7-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="679c7-177">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="679c7-177">Storage</span></span>
<span data-ttu-id="679c7-178">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="679c7-179">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="679c7-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="679c7-180">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="679c7-180">Manage storage quotas</span></span>
- <span data-ttu-id="679c7-181">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="679c7-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="679c7-182">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="679c7-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="679c7-183">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="679c7-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="679c7-184">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="679c7-184">View information about the individual storage components</span></span>
- <span data-ttu-id="679c7-185">Exibir informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="679c7-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="679c7-186">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="679c7-186">Subscription Admin</span></span>
<span data-ttu-id="679c7-187">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="679c7-188">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="679c7-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="679c7-189">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="679c7-189">Manage plans and offers</span></span>
- <span data-ttu-id="679c7-190">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="679c7-190">View usage and performance information</span></span>
- <span data-ttu-id="679c7-191">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="679c7-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="679c7-192">Assinatura</span><span class="sxs-lookup"><span data-stu-id="679c7-192">Subscription</span></span>
<span data-ttu-id="679c7-193">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="679c7-194">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="679c7-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="679c7-195">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="679c7-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="679c7-196">Atualizar</span><span class="sxs-lookup"><span data-stu-id="679c7-196">Update</span></span>
<span data-ttu-id="679c7-197">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="679c7-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="679c7-198">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="679c7-198">In this module administrators can:</span></span>
- <span data-ttu-id="679c7-199">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="679c7-199">List and install available updates</span></span>
- <span data-ttu-id="679c7-200">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="679c7-200">Resume interrupted updates</span></span>
- <span data-ttu-id="679c7-201">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="679c7-201">View installed updates</span></span>
