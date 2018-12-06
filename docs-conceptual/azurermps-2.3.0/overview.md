---
title: Visão geral do Azure Stack PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack PowerShell com instruções de instalação e configuração.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826843"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="ace67-103">Módulo do AzureRM 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ace67-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ace67-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="ace67-104">Requirements:</span></span>
<span data-ttu-id="ace67-105">A versão mínima do Azure Stack com suporte é 1808.</span><span class="sxs-lookup"><span data-stu-id="ace67-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="ace67-106">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="ace67-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="ace67-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="ace67-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="ace67-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="ace67-108">Release Notes</span></span>
* <span data-ttu-id="ace67-109">A versão 2.3.0 vem com uma lista de alterações significativas.</span><span class="sxs-lookup"><span data-stu-id="ace67-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="ace67-110">Para atualizar a partir da versão 1.2.11, criamos um guia de migração em https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="ace67-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="ace67-111">Essa versão corresponde ao perfil de API específico do Azure Stack 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="ace67-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="ace67-112">Todos os módulos estão usando dependências maior que ou igual a no módulo AzureRM.Profile.</span><span class="sxs-lookup"><span data-stu-id="ace67-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="ace67-113">As versões de API com suporte por cada um dos módulos são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="ace67-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="ace67-114">Computação - 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="ace67-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="ace67-115">Rede - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="ace67-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="ace67-116">Armazenamento - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="ace67-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="ace67-117">Recursos - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="ace67-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="ace67-118">Keyvault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="ace67-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="ace67-119">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="ace67-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="ace67-120">O mapa de versão de API completo para cada um dos tipos de recursos pode ser encontrado em https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="ace67-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="ace67-121">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="ace67-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ace67-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ace67-122">Azure Bridge</span></span>
<span data-ttu-id="ace67-123">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="ace67-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ace67-124">Backup</span><span class="sxs-lookup"><span data-stu-id="ace67-124">Backup</span></span>
<span data-ttu-id="ace67-125">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="ace67-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ace67-126">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="ace67-126">Configure where backups are stored</span></span>
- <span data-ttu-id="ace67-127">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="ace67-127">Perform backups</span></span>
- <span data-ttu-id="ace67-128">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="ace67-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ace67-129">Comércio</span><span class="sxs-lookup"><span data-stu-id="ace67-129">Commerce</span></span>
<span data-ttu-id="ace67-130">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ace67-131">Computação</span><span class="sxs-lookup"><span data-stu-id="ace67-131">Compute</span></span>
<span data-ttu-id="ace67-132">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma, discos gerenciados e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ace67-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ace67-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="ace67-133">Fabric</span></span>
<span data-ttu-id="ace67-134">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="ace67-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ace67-135">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="ace67-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ace67-136">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="ace67-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ace67-137">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="ace67-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ace67-138">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="ace67-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ace67-139">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="ace67-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ace67-140">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="ace67-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ace67-141">Galeria</span><span class="sxs-lookup"><span data-stu-id="ace67-141">Gallery</span></span>
<span data-ttu-id="ace67-142">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ace67-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="ace67-143">Infrastructure Insights</span></span>
<span data-ttu-id="ace67-144">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="ace67-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ace67-145">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="ace67-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ace67-146">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="ace67-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ace67-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ace67-147">KeyVault</span></span>
<span data-ttu-id="ace67-148">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ace67-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ace67-149">Rede</span><span class="sxs-lookup"><span data-stu-id="ace67-149">Network</span></span>
<span data-ttu-id="ace67-150">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="ace67-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ace67-151">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="ace67-151">Management of network quotas</span></span>
- <span data-ttu-id="ace67-152">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="ace67-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ace67-153">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="ace67-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ace67-154">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="ace67-154">Storage</span></span>
<span data-ttu-id="ace67-155">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ace67-156">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="ace67-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ace67-157">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ace67-157">Manage storage quotas</span></span>
- <span data-ttu-id="ace67-158">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="ace67-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ace67-159">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="ace67-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ace67-160">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="ace67-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ace67-161">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="ace67-161">View information about the individual storage components</span></span>
- <span data-ttu-id="ace67-162">Exibir informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="ace67-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ace67-163">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="ace67-163">Subscription Admin</span></span>
<span data-ttu-id="ace67-164">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ace67-165">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="ace67-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ace67-166">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="ace67-166">Manage plans and offers</span></span>
- <span data-ttu-id="ace67-167">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="ace67-167">View usage and performance information</span></span>
- <span data-ttu-id="ace67-168">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="ace67-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ace67-169">Assinatura</span><span class="sxs-lookup"><span data-stu-id="ace67-169">Subscription</span></span>
<span data-ttu-id="ace67-170">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ace67-171">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="ace67-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ace67-172">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="ace67-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ace67-173">Atualizar</span><span class="sxs-lookup"><span data-stu-id="ace67-173">Update</span></span>
<span data-ttu-id="ace67-174">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ace67-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ace67-175">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="ace67-175">In this module administrators can:</span></span>
- <span data-ttu-id="ace67-176">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="ace67-176">List and install available updates</span></span>
- <span data-ttu-id="ace67-177">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="ace67-177">Resume interrupted updates</span></span>
- <span data-ttu-id="ace67-178">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="ace67-178">View installed updates</span></span>
