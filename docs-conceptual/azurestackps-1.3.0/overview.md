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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882496"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="84705-103">Módulo Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="84705-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="84705-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="84705-104">Requirements:</span></span>
<span data-ttu-id="84705-105">A versão mínima suportada do Azure Stack é 1804.</span><span class="sxs-lookup"><span data-stu-id="84705-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="84705-106">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="84705-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="84705-107">Problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="84705-107">Known issues:</span></span>

- <span data-ttu-id="84705-108">Fechar o Alerta requer a versão Azure Stack 1803</span><span class="sxs-lookup"><span data-stu-id="84705-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="84705-109">Alguns cmdlets de armazenamento requerem a versão Azure Stack 1804</span><span class="sxs-lookup"><span data-stu-id="84705-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="84705-110">O New-AzsOffer não permite criar uma oferta com o estado público.</span><span class="sxs-lookup"><span data-stu-id="84705-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="84705-111">O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.</span><span class="sxs-lookup"><span data-stu-id="84705-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="84705-112">Um Pool de IPs não pode ser removido sem uma reimplantação</span><span class="sxs-lookup"><span data-stu-id="84705-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="84705-113">Alterações significativas</span><span class="sxs-lookup"><span data-stu-id="84705-113">Breaking Changes</span></span>
<span data-ttu-id="84705-114">Todas as alterações significativas migrando de 1.2.11 estão documentadas aqui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="84705-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="84705-115">Instalar</span><span class="sxs-lookup"><span data-stu-id="84705-115">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="84705-116">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="84705-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="84705-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="84705-117">Azure Bridge</span></span>
<span data-ttu-id="84705-118">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="84705-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="84705-119">Backup</span><span class="sxs-lookup"><span data-stu-id="84705-119">Backup</span></span>
<span data-ttu-id="84705-120">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="84705-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="84705-121">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="84705-121">Configure where backups are stored</span></span>
- <span data-ttu-id="84705-122">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="84705-122">Perform backups</span></span>
- <span data-ttu-id="84705-123">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="84705-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="84705-124">Comércio</span><span class="sxs-lookup"><span data-stu-id="84705-124">Commerce</span></span>
<span data-ttu-id="84705-125">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="84705-126">Computação</span><span class="sxs-lookup"><span data-stu-id="84705-126">Compute</span></span>
<span data-ttu-id="84705-127">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="84705-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="84705-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="84705-128">Fabric</span></span>
<span data-ttu-id="84705-129">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="84705-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="84705-130">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="84705-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="84705-131">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="84705-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="84705-132">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="84705-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="84705-133">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="84705-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="84705-134">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="84705-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="84705-135">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="84705-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="84705-136">Galeria</span><span class="sxs-lookup"><span data-stu-id="84705-136">Gallery</span></span>
<span data-ttu-id="84705-137">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="84705-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="84705-138">Infrastructure Insights</span></span>
<span data-ttu-id="84705-139">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="84705-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="84705-140">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="84705-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="84705-141">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="84705-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="84705-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="84705-142">KeyVault</span></span>
<span data-ttu-id="84705-143">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="84705-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="84705-144">Rede</span><span class="sxs-lookup"><span data-stu-id="84705-144">Network</span></span>
<span data-ttu-id="84705-145">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="84705-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="84705-146">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="84705-146">Management of network quotas</span></span>
- <span data-ttu-id="84705-147">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="84705-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="84705-148">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="84705-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="84705-149">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="84705-149">Storage</span></span>
<span data-ttu-id="84705-150">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="84705-151">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="84705-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="84705-152">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="84705-152">Manage storage quotas</span></span>
- <span data-ttu-id="84705-153">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="84705-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="84705-154">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="84705-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="84705-155">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="84705-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="84705-156">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="84705-156">View information about the individual storage components</span></span>
- <span data-ttu-id="84705-157">Exibir informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="84705-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="84705-158">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="84705-158">Subscription Admin</span></span>
<span data-ttu-id="84705-159">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="84705-160">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="84705-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="84705-161">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="84705-161">Manage plans and offers</span></span>
- <span data-ttu-id="84705-162">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="84705-162">View usage and performance information</span></span>
- <span data-ttu-id="84705-163">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="84705-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="84705-164">Assinatura</span><span class="sxs-lookup"><span data-stu-id="84705-164">Subscription</span></span>
<span data-ttu-id="84705-165">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="84705-166">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="84705-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="84705-167">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="84705-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="84705-168">Atualizar</span><span class="sxs-lookup"><span data-stu-id="84705-168">Update</span></span>
<span data-ttu-id="84705-169">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="84705-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="84705-170">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="84705-170">In this module administrators can:</span></span>
- <span data-ttu-id="84705-171">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="84705-171">List and install available updates</span></span>
- <span data-ttu-id="84705-172">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="84705-172">Resume interrupted updates</span></span>
- <span data-ttu-id="84705-173">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="84705-173">View installed updates</span></span>
