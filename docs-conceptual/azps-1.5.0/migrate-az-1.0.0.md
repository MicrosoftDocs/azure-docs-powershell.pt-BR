---
title: Alterações significativas no Microsoft Azure PowerShell Az 1.0.0
description: Este guia de migração contém uma lista de alterações significativas criadas para o Azure PowerShell na versão de lançamento 1 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882127"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="a08db-103">Guia de Migração para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a08db-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="a08db-104">Este documento descreve as alterações entre as versões 6.x do AzureRM e da versão 1.0.0 do Az.</span><span class="sxs-lookup"><span data-stu-id="a08db-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a08db-105">Sumário</span><span class="sxs-lookup"><span data-stu-id="a08db-105">Table of Contents</span></span>
- [<span data-ttu-id="a08db-106">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="a08db-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="a08db-107">Alterações de prefixo de substantivo do cmdlet</span><span class="sxs-lookup"><span data-stu-id="a08db-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="a08db-108">Alterações de nome de módulo</span><span class="sxs-lookup"><span data-stu-id="a08db-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="a08db-109">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="a08db-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="a08db-110">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="a08db-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="a08db-111">Remoção temporária de logon de usuário usando PSCredential</span><span class="sxs-lookup"><span data-stu-id="a08db-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="a08db-112">Logon de código de dispositivo padrão em vez de prompt de navegador da Web</span><span class="sxs-lookup"><span data-stu-id="a08db-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="a08db-113">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="a08db-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="a08db-114">Az.ApiManagement (anteriormente AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="a08db-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="a08db-115">Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="a08db-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="a08db-116">Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="a08db-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="a08db-117">Az.Compute (anteriormente AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="a08db-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="a08db-118">Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="a08db-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="a08db-119">Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="a08db-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="a08db-120">Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="a08db-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="a08db-121">Az.KeyVault (anteriormente AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="a08db-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="a08db-122">Az.Media (anteriormente AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="a08db-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="a08db-123">Az.Monitor (anteriormente AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="a08db-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="a08db-124">Az.Network (anteriormente AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="a08db-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="a08db-125">Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="a08db-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="a08db-126">Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="a08db-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="a08db-127">Az.Resources (anteriormente AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="a08db-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="a08db-128">Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="a08db-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="a08db-129">Az.Sql (anteriormente AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="a08db-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="a08db-130">Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="a08db-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="a08db-131">Az.Websites (anteriormente AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="a08db-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="a08db-132">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="a08db-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="a08db-133">Alterações de prefixo de substantivo do cmdlet</span><span class="sxs-lookup"><span data-stu-id="a08db-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="a08db-134">No AzureRM, os cmdlets usavam “AzureRM” ou “Azure” como um prefixo de substantivo.</span><span class="sxs-lookup"><span data-stu-id="a08db-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="a08db-135">O Az simplifica e normaliza os nomes do cmndlet, para que todos os cmdlets usem “Az” como seu prefixo de substantivo do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a08db-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="a08db-136">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="a08db-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="a08db-137">Foram alterados para</span><span class="sxs-lookup"><span data-stu-id="a08db-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="a08db-138">Para simplificar a transição para esses novos nomes de cmdlet, o Az apresenta dois novos cmdlets, ```Enable-AzureRmAlias``` e ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="a08db-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="a08db-139">```Enable-AzureRmAlias``` cria os aliases de nomes de cmdlet mais antigos no AzureRM para os nomes de cmdlet mais recentes do Az.</span><span class="sxs-lookup"><span data-stu-id="a08db-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="a08db-140">O cmdlet permite criar aliases na sessão atual ou em todas as sessões, alterando seu usuário ou o perfil do computador.</span><span class="sxs-lookup"><span data-stu-id="a08db-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="a08db-141">Por exemplo, o script a seguir no AzureRM:</span><span class="sxs-lookup"><span data-stu-id="a08db-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a08db-142">Pode ser executado com alterações mínimas usando ```Enable-AzureRmAlias```:</span><span class="sxs-lookup"><span data-stu-id="a08db-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a08db-143">Executar ```Enable-AzureRmAlias -Scope CurrentUser``` habilitará os aliases para todas as sessões do Powershell, para que após executar esse cmdlet, um script como este não precise ser alterado:</span><span class="sxs-lookup"><span data-stu-id="a08db-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a08db-144">Para obter detalhes completos sobre o uso dos cmdlets do alias, execute ```Get-Help -Online Enable-AzureRmAlias``` no prompt do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a08db-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="a08db-145">```Disable-AzureRmAlias``` remove os aliases de cmdlet do AzureRM criados pelo ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="a08db-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="a08db-146">Para obter detalhes completos, execute ```Get-Help -Online Disable-AzureRmAlias``` no prompt do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a08db-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="a08db-147">Alterações de nome de módulo</span><span class="sxs-lookup"><span data-stu-id="a08db-147">Module Name Changes</span></span>
- <span data-ttu-id="a08db-148">Os nomes do módulo foram alterados de `AzureRM.*` para `Az.*`, exceto para os seguintes módulos:</span><span class="sxs-lookup"><span data-stu-id="a08db-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="a08db-149">As alterações nos nomes dos módulos significam que qualquer script que usa ```#Requires``` ou ```Import-Module``` para carregar módulos específicos precisarão ser alterados para usar o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="a08db-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="a08db-150">Migração de instruções #Requires</span><span class="sxs-lookup"><span data-stu-id="a08db-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="a08db-151">Scripts que usam #Requires para declarar uma dependência em módulos AzureRM devem ser atualizados para usar os novos nomes de módulo</span><span class="sxs-lookup"><span data-stu-id="a08db-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="a08db-152">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="a08db-153">Migração de instruções Import-Module</span><span class="sxs-lookup"><span data-stu-id="a08db-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="a08db-154">Scripts que usam ```Import-Module``` para carregar módulos do AzureRM precisarão ser atualizados para refletir os novos nomes de módulo.</span><span class="sxs-lookup"><span data-stu-id="a08db-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="a08db-155">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="a08db-156">Migração de invocações de cmdlet totalmente qualificadas</span><span class="sxs-lookup"><span data-stu-id="a08db-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="a08db-157">Scripts que usam as invocações de cmdlet qualificadas por módulo, como</span><span class="sxs-lookup"><span data-stu-id="a08db-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="a08db-158">Devem ser alterados para usar os novos nomes de módulo e de cmdlet</span><span class="sxs-lookup"><span data-stu-id="a08db-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="a08db-159">Migração de dependências de manifesto do módulo</span><span class="sxs-lookup"><span data-stu-id="a08db-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="a08db-160">Módulos que expressam as dependências em módulos AzureRM por meio de um arquivo de manifesto (.psd1) do módulo precisarão atualizar os nomes do módulo em sua seção “RequiredModules”</span><span class="sxs-lookup"><span data-stu-id="a08db-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="a08db-161">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="a08db-162">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="a08db-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="a08db-163">Não há mais suporte ativo para as ferramentas para esses serviços.</span><span class="sxs-lookup"><span data-stu-id="a08db-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="a08db-164">Os clientes são incentivados a mudar para serviços alternativos, assim que for conveniente.</span><span class="sxs-lookup"><span data-stu-id="a08db-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="a08db-165">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="a08db-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="a08db-166">Usar o Az com o Windows PowerShell 5.1 requer a instalação do .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="a08db-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="a08db-167">No entanto, usar o Az com o PowerShell Core não exige o .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="a08db-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="a08db-168">Remoção temporária de logon de usuário usando PSCredential</span><span class="sxs-lookup"><span data-stu-id="a08db-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="a08db-169">Devido a alterações no fluxo de autenticação para o .NET Standard, estamos temporariamente removendo o logon de usuário por meio do PSCredential.</span><span class="sxs-lookup"><span data-stu-id="a08db-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="a08db-170">Essa funcionalidade será lançada novamente no lançamento de 15/1/2019 para o Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a08db-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="a08db-171">Isso é discutido detalhadamente [neste problema.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="a08db-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="a08db-172">Logon de código de dispositivo padrão em vez de prompt de navegador da Web</span><span class="sxs-lookup"><span data-stu-id="a08db-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="a08db-173">Devido a alterações no fluxo de autenticação para o .NET Standard, estamos usando o logon do dispositivo como o fluxo de logon padrão durante o logon interativo.</span><span class="sxs-lookup"><span data-stu-id="a08db-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="a08db-174">O logon baseado em navegador da Web será reintroduzido novamente para o Windows PowerShell 5.1 como padrão no lançamento de 15/1/2019.</span><span class="sxs-lookup"><span data-stu-id="a08db-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="a08db-175">Nesse momento, os usuários poderão escolher logon de dispositivo usando um parâmetro Switch.</span><span class="sxs-lookup"><span data-stu-id="a08db-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="a08db-176">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="a08db-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="a08db-177">Az.ApiManagement (anteriormente AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="a08db-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="a08db-178">Remoção dos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a08db-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="a08db-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a08db-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="a08db-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a08db-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="a08db-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a08db-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="a08db-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a08db-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="a08db-183">Use o cmdlet **Set-AzApiManagement** cmdlet para definir essas propriedades</span><span class="sxs-lookup"><span data-stu-id="a08db-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="a08db-184">As propriedades a seguir foram removidas</span><span class="sxs-lookup"><span data-stu-id="a08db-184">Following properties were removed</span></span>
  - <span data-ttu-id="a08db-185">Removidas as propriedades `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` do tipo `PsApiManagementHostnameConfiguration` de `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="a08db-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="a08db-186">Em vez disso, use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` do tipo `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a08db-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="a08db-187">Removida a propriedade `StaticIPs` de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a08db-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="a08db-188">A propriedade foi dividida em `PublicIPAddresses` e `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="a08db-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="a08db-189">Removida a propriedade necessária `Location` do cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a08db-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="a08db-190">Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="a08db-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="a08db-191">O parâmetro `InvoiceName` foi removido em favor do cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="a08db-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="a08db-192">Os scripts precisarão usar outros parâmetros de identidade para a fatura.</span><span class="sxs-lookup"><span data-stu-id="a08db-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="a08db-193">Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="a08db-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="a08db-194">Removido o conjunto de parâmetros `GetSkusWithAccountParamSetName` do cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="a08db-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="a08db-195">Você deve obter Skus por Account Type e Location, em vez de usar ResourceGroupName e Account Name.</span><span class="sxs-lookup"><span data-stu-id="a08db-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="a08db-196">Az.Compute (anteriormente AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="a08db-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="a08db-197">`IdentityIds` foram removidos da propriedade `Identity` nos Scripts dos objetos `PSVirtualMachine` e `PSVirtualMachineScaleSet`, que não devem mais usar o valor desse campo para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="a08db-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="a08db-198">O tipo de propriedade `InstanceView` do objeto `PSVirtualMachineScaleSetVM` foi alterado de `VirtualMachineInstanceView` para `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="a08db-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="a08db-199">As propriedades `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` foram removidas da propriedade `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="a08db-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="a08db-200">O tipo de propriedade `Sku` do objeto `PSSnapshotUpdate` foi alterado de `DiskSku` para `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="a08db-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="a08db-201">`VmScaleSetVMParameterSet` foi removido do cmdlet `Add-AzVMDataDisk`, você não pode mais adicionar um disco de dados individualmente em uma VM ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="a08db-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="a08db-202">Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="a08db-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="a08db-203">O parâmetro `GatewayName` agora é obrigatório no cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="a08db-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="a08db-204">Removido o cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="a08db-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="a08db-205">Removido o parâmetro `LinkedServiceName` dos Scripts cmdlet `Get-AzDataFactoryV2ActivityRun`, que não devem mais usar o valor desse campo para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="a08db-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="a08db-206">Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="a08db-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="a08db-207">Removidos os cmdlets preteridos: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, e `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="a08db-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="a08db-208">Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="a08db-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="a08db-209">Os cmdlets a seguir tiveram o parâmetro `Encoding` alterado do tipo `FileSystemCmdletProviderEncoding` para `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="a08db-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="a08db-210">Essa alteração remove os valores de codificação `String` e `Oem`.</span><span class="sxs-lookup"><span data-stu-id="a08db-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="a08db-211">Todos os outros valores de codificação anteriores permanecem.</span><span class="sxs-lookup"><span data-stu-id="a08db-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="a08db-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a08db-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="a08db-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a08db-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="a08db-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a08db-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="a08db-215">Removido o alias da propriedade preterida `Tags` dos cmdlets `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="a08db-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="a08db-216">Uso de scripts</span><span class="sxs-lookup"><span data-stu-id="a08db-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="a08db-217">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="a08db-218">Removidas as propriedades preteridas ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` e ```FirewallAllowAzureIps``` do objeto ```PSDataLakeStoreAccountBasic```.</span><span class="sxs-lookup"><span data-stu-id="a08db-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="a08db-219">Qualquer script que use o ```PSDatalakeStoreAccount``` retornado de ```Get-AzDataLakeStoreAccount``` não deve fazer referência a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a08db-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="a08db-220">Az.KeyVault (anteriormente AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="a08db-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="a08db-221">A propriedade `PurgeDisabled` foi removida dos Scripts dos objetos `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes`, que não devem fazer referência à propriedade ```PurgeDisabled``` para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="a08db-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="a08db-222">Az.Media (anteriormente AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="a08db-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="a08db-223">Removido o alias da propriedade preterida `Tags` dos Scripts cmdlet `New-AzMediaService` sendo usados</span><span class="sxs-lookup"><span data-stu-id="a08db-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="a08db-224">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="a08db-225">Az.Monitor (anteriormente AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="a08db-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="a08db-226">Removidos os nomes no plural dos parâmetros `Categories` e `Timegrains` em favor de nomes de parâmetro no singular dos Scripts cmdlet `Set-AzDiagnosticSetting` sendo usados</span><span class="sxs-lookup"><span data-stu-id="a08db-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="a08db-227">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="a08db-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="a08db-228">Az.Network (anteriormente AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="a08db-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="a08db-229">Removido o parâmetro preterido `ResourceId` do cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="a08db-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="a08db-230">Removida a propriedade preterida `EnableVmProtection` do objeto `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="a08db-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="a08db-231">Removido o cmdlet preteridos `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="a08db-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="a08db-232">Os scripts não devem mais tomar decisões de processamento com base nos valores desses campos.</span><span class="sxs-lookup"><span data-stu-id="a08db-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="a08db-233">Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="a08db-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="a08db-234">O conjunto de parâmetros padrão para `Get-AzOperationalInsightsDataSource` foi removido, e `ByWorkspaceNameByKind` tornou-se o conjunto de parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="a08db-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="a08db-235">Os scripts que listavam as fontes de dados sendo usadas</span><span class="sxs-lookup"><span data-stu-id="a08db-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="a08db-236">Devem ser alterados para especificar um Kind</span><span class="sxs-lookup"><span data-stu-id="a08db-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a08db-237">Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="a08db-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="a08db-238">Removido o parâmetro `Encryption` do cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="a08db-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="a08db-239">O parâmetro `TargetStorageAccountName` agora é obrigatório para restaurações de disco gerenciado no cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="a08db-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="a08db-240">Removidos os parâmetros `StorageAccountName` e `StorageAccountResourceGroupName` no cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="a08db-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="a08db-241">Removido o parâmetro `Name` no cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="a08db-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="a08db-242">Az.Resources (anteriormente AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="a08db-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="a08db-243">Removido o parâmetro `Sku` do cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a08db-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="a08db-244">Removido o parâmetro de `Password` das Senhas cmdlets `New-AzADServicePrincipal` e `New-AzADSpCredential` automaticamente geradas, nos scripts que forneciam a senha:</span><span class="sxs-lookup"><span data-stu-id="a08db-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="a08db-245">Devem ser alterados para recuperar a senha da saída:</span><span class="sxs-lookup"><span data-stu-id="a08db-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="a08db-246">Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="a08db-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="a08db-247">Os seguintes tipos de retorno de cmdlet foram alterados:</span><span class="sxs-lookup"><span data-stu-id="a08db-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="a08db-248">A propriedade `SerivceTypeHealthPolicies` do tipo `ApplicationHealthPolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="a08db-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="a08db-249">A propriedade `ApplicationHealthPolicies` do tipo `ClusterUpgradeDeltaHealthPolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="a08db-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="a08db-250">A propriedade `OverrideUserUpgradePolicy` do tipo `ClusterUpgradePolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="a08db-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="a08db-251">Essas alterações afetam os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a08db-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="a08db-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a08db-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="a08db-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a08db-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="a08db-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a08db-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="a08db-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a08db-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="a08db-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a08db-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="a08db-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a08db-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="a08db-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a08db-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="a08db-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a08db-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="a08db-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a08db-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="a08db-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a08db-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="a08db-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a08db-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="a08db-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a08db-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="a08db-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a08db-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="a08db-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a08db-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="a08db-266">Az.Sql (anteriormente AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="a08db-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="a08db-267">Removidos os parâmetros `State` e `ResourceId` do cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="a08db-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="a08db-268">Removidos os cmdlets preteridos: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="a08db-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="a08db-269">Removido o parâmetro preterido `Current` do cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="a08db-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="a08db-270">Removido o parâmetro preterido `DatabaseName` do cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="a08db-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="a08db-271">Removido o parâmetro preterido `PrivilegedLogin` do cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="a08db-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="a08db-272">Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="a08db-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="a08db-273">Para dar suporte à criação de um contexto de armazenamento Oauth com apenas o nome da conta de armazenamento, o conjunto de parâmetros padrão foi alterado para `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="a08db-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="a08db-274">Exemplo: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="a08db-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="a08db-275">O parâmetro `Location` agora é obrigatório no cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="a08db-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="a08db-276">Os métodos da API de armazenamento agora usam o padrão assíncrono baseado em tarefas (TAP), em vez de chamadas à API síncronas.</span><span class="sxs-lookup"><span data-stu-id="a08db-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="a08db-277">1. Instantâneo de Blob</span><span class="sxs-lookup"><span data-stu-id="a08db-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="a08db-278">Antes:</span><span class="sxs-lookup"><span data-stu-id="a08db-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="a08db-279">Depois:</span><span class="sxs-lookup"><span data-stu-id="a08db-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="a08db-280">2. Compartilhar instantâneo</span><span class="sxs-lookup"><span data-stu-id="a08db-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="a08db-281">Antes:</span><span class="sxs-lookup"><span data-stu-id="a08db-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="a08db-282">Depois:</span><span class="sxs-lookup"><span data-stu-id="a08db-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="a08db-283">3. Restaurar um blob de exclusão reversível</span><span class="sxs-lookup"><span data-stu-id="a08db-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="a08db-284">Antes:</span><span class="sxs-lookup"><span data-stu-id="a08db-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="a08db-285">Depois:</span><span class="sxs-lookup"><span data-stu-id="a08db-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="a08db-286">4. Definir camada do Blob</span><span class="sxs-lookup"><span data-stu-id="a08db-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="a08db-287">Antes:</span><span class="sxs-lookup"><span data-stu-id="a08db-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="a08db-288">Depois:</span><span class="sxs-lookup"><span data-stu-id="a08db-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="a08db-289">Az.Websites (anteriormente AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="a08db-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="a08db-290">Removidas as propriedades preteridas `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite` dos objetos</span><span class="sxs-lookup"><span data-stu-id="a08db-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>