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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67038186"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="0adf4-103">AzureRM Módulo 2.5.0</span><span class="sxs-lookup"><span data-stu-id="0adf4-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="0adf4-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="0adf4-104">Requirements:</span></span>
<span data-ttu-id="0adf4-105">A versão mínima do Azure Stack compatível é a 1904.</span><span class="sxs-lookup"><span data-stu-id="0adf4-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="0adf4-106">Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11</span><span class="sxs-lookup"><span data-stu-id="0adf4-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="0adf4-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="0adf4-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="0adf4-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="0adf4-108">Release Notes</span></span>
* <span data-ttu-id="0adf4-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="0adf4-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="0adf4-110">Novo módulo de recursos que dá suporte à API versão 2018-05-01 com perfil 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="0adf4-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="0adf4-111">As operações de PolicyDefinition(2016-12-01) e PolicyAssisgment(2017-06-01-preview) ainda estão com versões antigas da API</span><span class="sxs-lookup"><span data-stu-id="0adf4-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="0adf4-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="0adf4-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="0adf4-113">Novo módulo de computação que dá suporte à API versão 2017-12-01.'</span><span class="sxs-lookup"><span data-stu-id="0adf4-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="0adf4-114">Essa versão corresponde ao perfil de API específico do azurestack 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="0adf4-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="0adf4-115">Todos os módulos estão usando dependências maior que ou igual a no módulo AzureRM.Profile.</span><span class="sxs-lookup"><span data-stu-id="0adf4-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="0adf4-116">As versões de API com suporte por cada um dos módulos são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="0adf4-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="0adf4-117">Computação – 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="0adf4-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="0adf4-118">Rede - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="0adf4-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="0adf4-119">Armazenamento - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="0adf4-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="0adf4-120">Recursos - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="0adf4-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="0adf4-121">Keyvault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="0adf4-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="0adf4-122">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="0adf4-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="0adf4-123">O mapa de versão de API completo para cada um dos tipos de recursos pode ser encontrado em https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="0adf4-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="0adf4-124">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="0adf4-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="0adf4-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="0adf4-125">Azure Bridge</span></span>
<span data-ttu-id="0adf4-126">Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.</span><span class="sxs-lookup"><span data-stu-id="0adf4-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="0adf4-127">Backup</span><span class="sxs-lookup"><span data-stu-id="0adf4-127">Backup</span></span>
<span data-ttu-id="0adf4-128">Versão prévia do módulo administrador de Backup que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="0adf4-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="0adf4-129">Configurarem onde os backups são armazenados</span><span class="sxs-lookup"><span data-stu-id="0adf4-129">Configure where backups are stored</span></span>
- <span data-ttu-id="0adf4-130">Executarem backups</span><span class="sxs-lookup"><span data-stu-id="0adf4-130">Perform backups</span></span>
- <span data-ttu-id="0adf4-131">Listarem e restaurarem o backup completo</span><span class="sxs-lookup"><span data-stu-id="0adf4-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="0adf4-132">Comércio</span><span class="sxs-lookup"><span data-stu-id="0adf4-132">Commerce</span></span>
<span data-ttu-id="0adf4-133">Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="0adf4-134">Computação</span><span class="sxs-lookup"><span data-stu-id="0adf4-134">Compute</span></span>
<span data-ttu-id="0adf4-135">Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma, discos gerenciados e extensões da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0adf4-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="0adf4-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="0adf4-136">Fabric</span></span>
<span data-ttu-id="0adf4-137">Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="0adf4-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="0adf4-138">Parar, Iniciar e Desligar os nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="0adf4-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="0adf4-139">Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU</span><span class="sxs-lookup"><span data-stu-id="0adf4-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="0adf4-140">Reparar nós da unidade de escala</span><span class="sxs-lookup"><span data-stu-id="0adf4-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="0adf4-141">Reinicializar função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="0adf4-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="0adf4-142">Parar, Iniciar e Desligar instâncias da função de Infraestrutura</span><span class="sxs-lookup"><span data-stu-id="0adf4-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="0adf4-143">Criar novos Pools de IPs</span><span class="sxs-lookup"><span data-stu-id="0adf4-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="0adf4-144">Galeria</span><span class="sxs-lookup"><span data-stu-id="0adf4-144">Gallery</span></span>
<span data-ttu-id="0adf4-145">Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="0adf4-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="0adf4-146">Infrastructure Insights</span></span>
<span data-ttu-id="0adf4-147">Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:</span><span class="sxs-lookup"><span data-stu-id="0adf4-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="0adf4-148">Exibirem a integridade de seus recursos de carimbo do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="0adf4-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="0adf4-149">Exibirem e gerenciarem alertas</span><span class="sxs-lookup"><span data-stu-id="0adf4-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="0adf4-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0adf4-150">KeyVault</span></span>
<span data-ttu-id="0adf4-151">Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0adf4-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="0adf4-152">Rede</span><span class="sxs-lookup"><span data-stu-id="0adf4-152">Network</span></span>
<span data-ttu-id="0adf4-153">Versão prévia do módulo administrador da Rede que permite:</span><span class="sxs-lookup"><span data-stu-id="0adf4-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="0adf4-154">Gerenciar as cotas de rede</span><span class="sxs-lookup"><span data-stu-id="0adf4-154">Management of network quotas</span></span>
- <span data-ttu-id="0adf4-155">Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga</span><span class="sxs-lookup"><span data-stu-id="0adf4-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="0adf4-156">Fornecer um cmdlet que exibe uma visão geral do administrador</span><span class="sxs-lookup"><span data-stu-id="0adf4-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="0adf4-157">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="0adf4-157">Storage</span></span>
<span data-ttu-id="0adf4-158">Versão prévia do módulo administrador do Armazenamento do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="0adf4-159">Nessa versão, fornecemos funcionalidade para:</span><span class="sxs-lookup"><span data-stu-id="0adf4-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="0adf4-160">Gerenciar as cotas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0adf4-160">Manage storage quotas</span></span>
- <span data-ttu-id="0adf4-161">Coletar o lixo dos recursos de armazenamento excluídos</span><span class="sxs-lookup"><span data-stu-id="0adf4-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="0adf4-162">Restaurar as contas de armazenamento excluídas</span><span class="sxs-lookup"><span data-stu-id="0adf4-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="0adf4-163">Migrar os contêineres de um compartilhamento para outro</span><span class="sxs-lookup"><span data-stu-id="0adf4-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="0adf4-164">Exibir informações sobre os componentes de armazenamento individuais</span><span class="sxs-lookup"><span data-stu-id="0adf4-164">View information about the individual storage components</span></span>
- <span data-ttu-id="0adf4-165">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="0adf4-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="0adf4-166">Administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="0adf4-166">Subscription Admin</span></span>
<span data-ttu-id="0adf4-167">Versão prévia do módulo administrador de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="0adf4-168">Esse módulo fornece funcionalidade para os administradores:</span><span class="sxs-lookup"><span data-stu-id="0adf4-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="0adf4-169">Gerenciarem planos e ofertas</span><span class="sxs-lookup"><span data-stu-id="0adf4-169">Manage plans and offers</span></span>
- <span data-ttu-id="0adf4-170">Exibirem informações de uso e desempenho</span><span class="sxs-lookup"><span data-stu-id="0adf4-170">View usage and performance information</span></span>
- <span data-ttu-id="0adf4-171">Gerenciar o RBAC</span><span class="sxs-lookup"><span data-stu-id="0adf4-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="0adf4-172">Subscription</span><span class="sxs-lookup"><span data-stu-id="0adf4-172">Subscription</span></span>
<span data-ttu-id="0adf4-173">Versão prévia do módulo de Assinatura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="0adf4-174">Esse módulo fornece funcionalidade para os Usuários:</span><span class="sxs-lookup"><span data-stu-id="0adf4-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="0adf4-175">Criar, Excluir e Atualizar Assinaturas</span><span class="sxs-lookup"><span data-stu-id="0adf4-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="0adf4-176">Atualizar</span><span class="sxs-lookup"><span data-stu-id="0adf4-176">Update</span></span>
<span data-ttu-id="0adf4-177">Versão prévia do módulo administrador de Atualização do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="0adf4-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="0adf4-178">Nesse módulo, os administradores podem:</span><span class="sxs-lookup"><span data-stu-id="0adf4-178">In this module administrators can:</span></span>
- <span data-ttu-id="0adf4-179">Listar e instalar as atualizações disponíveis</span><span class="sxs-lookup"><span data-stu-id="0adf4-179">List and install available updates</span></span>
- <span data-ttu-id="0adf4-180">Retomar as atualizações interrompidas</span><span class="sxs-lookup"><span data-stu-id="0adf4-180">Resume interrupted updates</span></span>
- <span data-ttu-id="0adf4-181">Exibir as atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="0adf4-181">View installed updates</span></span>
