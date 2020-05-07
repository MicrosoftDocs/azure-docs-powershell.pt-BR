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
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053351"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="b3dc1-103">Módulo do Azure Stack 1.5.0</span><span class="sxs-lookup"><span data-stu-id="b3dc1-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dc1-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-104">Requirements:</span></span>
<span data-ttu-id="b3dc1-105">A versão mínima do Azure Stack com suporte é 1808.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="b3dc1-106">Nota: se você estiver usando uma versão anterior, instale a versão 1.4.0</span><span class="sxs-lookup"><span data-stu-id="b3dc1-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="b3dc1-107">Problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-107">Known issues:</span></span>

- <span data-ttu-id="b3dc1-108">O New-AzsOffer não permite criar uma oferta com o estado público.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="b3dc1-109">O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="b3dc1-110">Um Pool de IPs não pode ser removido sem uma reimplantação</span><span class="sxs-lookup"><span data-stu-id="b3dc1-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="b3dc1-111">Instalar</span><span class="sxs-lookup"><span data-stu-id="b3dc1-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="b3dc1-112">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="b3dc1-112">Release Notes</span></span>
* <span data-ttu-id="b3dc1-113">Todos os módulos do Azure Stack Admin foram atualizados para dependência maior que ou igual a no módulo AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b3dc1-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="b3dc1-114">Suporte para lidar com nomes de recurso aninhado em todos os módulos</span><span class="sxs-lookup"><span data-stu-id="b3dc1-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="b3dc1-115">Correção de bug em todos os módulos em que ErrorActionPreference está sendo substituído por Stop</span><span class="sxs-lookup"><span data-stu-id="b3dc1-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="b3dc1-116">Módulo Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="b3dc1-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="b3dc1-117">Novas propriedades de cota adicionadas para o suporte de disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="b3dc1-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="b3dc1-118">Adição de cmdlets relacionados à migração de disco</span><span class="sxs-lookup"><span data-stu-id="b3dc1-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="b3dc1-119">Propriedades adicionais nos objetos de extensão de VM e Imagem da Plataforma</span><span class="sxs-lookup"><span data-stu-id="b3dc1-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="b3dc1-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="b3dc1-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="b3dc1-121">Novo cmdlet para adicionar nó de unidade de escala</span><span class="sxs-lookup"><span data-stu-id="b3dc1-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="b3dc1-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="b3dc1-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="b3dc1-123">Set-AzsBackupShare agora é um alias para o cmdlet Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3dc1-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="b3dc1-124">Get-AzsBackupLocation agora é um alias para o cmdlet Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3dc1-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="b3dc1-125">Set-AzsBackupConfiguration, o parâmetro BackupShare agora é um alias para o caminho do parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3dc1-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="b3dc1-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="b3dc1-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="b3dc1-127">Get-AzsDelegatedProviderOffer; o parâmetro OfferName agora é um alias para a oferta</span><span class="sxs-lookup"><span data-stu-id="b3dc1-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="b3dc1-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="b3dc1-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="b3dc1-129">Get-AzsDelegatedProviderOffer; o parâmetro OfferName agora é um alias para a oferta</span><span class="sxs-lookup"><span data-stu-id="b3dc1-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="b3dc1-130">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="b3dc1-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="b3dc1-131">Azure Bridge</span></span>
<span data-ttu-id="b3dc1-132">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="b3dc1-133">Backup</span><span class="sxs-lookup"><span data-stu-id="b3dc1-133">Backup</span></span>
<span data-ttu-id="b3dc1-134">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="b3dc1-135">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="b3dc1-135">Configure where backups are stored</span></span>
- <span data-ttu-id="b3dc1-136">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="b3dc1-136">Perform backups</span></span>
- <span data-ttu-id="b3dc1-137">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="b3dc1-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="b3dc1-138">Comércio</span><span class="sxs-lookup"><span data-stu-id="b3dc1-138">Commerce</span></span>
<span data-ttu-id="b3dc1-139">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="b3dc1-140">Computação</span><span class="sxs-lookup"><span data-stu-id="b3dc1-140">Compute</span></span>
<span data-ttu-id="b3dc1-141">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma, discos gerenciados e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="b3dc1-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="b3dc1-142">Fabric</span></span>
<span data-ttu-id="b3dc1-143">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="b3dc1-144">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="b3dc1-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="b3dc1-145">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="b3dc1-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="b3dc1-146">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="b3dc1-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="b3dc1-147">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="b3dc1-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="b3dc1-148">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="b3dc1-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="b3dc1-149">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="b3dc1-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="b3dc1-150">Galeria</span><span class="sxs-lookup"><span data-stu-id="b3dc1-150">Gallery</span></span>
<span data-ttu-id="b3dc1-151">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="b3dc1-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="b3dc1-152">Infrastructure Insights</span></span>
<span data-ttu-id="b3dc1-153">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="b3dc1-154">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="b3dc1-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="b3dc1-155">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="b3dc1-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3dc1-156">KeyVault</span></span>
<span data-ttu-id="b3dc1-157">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="b3dc1-158">Rede</span><span class="sxs-lookup"><span data-stu-id="b3dc1-158">Network</span></span>
<span data-ttu-id="b3dc1-159">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="b3dc1-160">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="b3dc1-160">Management of network quotas</span></span>
- <span data-ttu-id="b3dc1-161">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="b3dc1-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="b3dc1-162">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="b3dc1-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="b3dc1-163">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="b3dc1-163">Storage</span></span>
<span data-ttu-id="b3dc1-164">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="b3dc1-165">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="b3dc1-166">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b3dc1-166">Manage storage quotas</span></span>
- <span data-ttu-id="b3dc1-167">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="b3dc1-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="b3dc1-168">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="b3dc1-169">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="b3dc1-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="b3dc1-170">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="b3dc1-170">View information about the individual storage components</span></span>
- <span data-ttu-id="b3dc1-171">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="b3dc1-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="b3dc1-172">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="b3dc1-172">Subscription Admin</span></span>
<span data-ttu-id="b3dc1-173">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="b3dc1-174">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="b3dc1-175">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-175">Manage plans and offers</span></span>
- <span data-ttu-id="b3dc1-176">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="b3dc1-176">View usage and performance information</span></span>
- <span data-ttu-id="b3dc1-177">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="b3dc1-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="b3dc1-178">Subscription</span><span class="sxs-lookup"><span data-stu-id="b3dc1-178">Subscription</span></span>
<span data-ttu-id="b3dc1-179">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="b3dc1-180">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="b3dc1-181">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="b3dc1-182">Atualizar</span><span class="sxs-lookup"><span data-stu-id="b3dc1-182">Update</span></span>
<span data-ttu-id="b3dc1-183">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="b3dc1-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="b3dc1-184">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="b3dc1-184">In this module administrators can:</span></span>
- <span data-ttu-id="b3dc1-185">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="b3dc1-185">List and install available updates</span></span>
- <span data-ttu-id="b3dc1-186">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-186">Resume interrupted updates</span></span>
- <span data-ttu-id="b3dc1-187">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="b3dc1-187">View installed updates</span></span>
