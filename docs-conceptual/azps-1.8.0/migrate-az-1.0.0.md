---
title: Todas as alterações do AzureRM para o Azure PowerShell Az 1.0.0
description: Este guia de migração contém uma lista de alterações significativas criadas para o Azure PowerShell na versão de lançamento 1 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035822"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="f4dd8-103">Alterações da falha para Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f4dd8-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="f4dd8-104">Este documento fornece informações detalhadas sobre as alterações entre o AzureRM 6.x e o novo módulo Az, versão 1.x e posterior.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="f4dd8-105">O sumário ajudará a orientá-lo por um caminho de migração completa, incluindo alterações específicas do módulo que possam afetar seus scripts.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="f4dd8-106">Para obter orientações gerais sobre como iniciar uma migração do AzureRM para o Az, confira [Iniciar uma migração do AzureRM para o Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="f4dd8-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="f4dd8-107">Table of Contents</span></span>

- [<span data-ttu-id="f4dd8-108">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="f4dd8-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="f4dd8-109">Alterações de prefixo de substantivo do cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4dd8-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="f4dd8-110">Alterações de nome de módulo</span><span class="sxs-lookup"><span data-stu-id="f4dd8-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="f4dd8-111">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="f4dd8-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="f4dd8-112">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f4dd8-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="f4dd8-113">Remoção temporária de logon de usuário usando PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd8-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="f4dd8-114">Logon de código de dispositivo padrão em vez de prompt do navegador da Web</span><span class="sxs-lookup"><span data-stu-id="f4dd8-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="f4dd8-115">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="f4dd8-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="f4dd8-116">Az.ApiManagement (anteriormente AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="f4dd8-117">Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="f4dd8-118">Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="f4dd8-119">Az.Compute (anteriormente AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="f4dd8-120">Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="f4dd8-121">Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="f4dd8-122">Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="f4dd8-123">Az.KeyVault (anteriormente AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="f4dd8-124">Az.Media (anteriormente AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="f4dd8-125">Az.Monitor (anteriormente AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="f4dd8-126">Az.Network (anteriormente AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="f4dd8-127">Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="f4dd8-128">Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="f4dd8-129">Az.Resources (anteriormente AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="f4dd8-130">Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="f4dd8-131">Az.Sql (anteriormente AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="f4dd8-132">Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="f4dd8-133">Az.Websites (anteriormente AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="f4dd8-134">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="f4dd8-134">General breaking changes</span></span>

<span data-ttu-id="f4dd8-135">Esta seção fornece detalhes sobre as alterações gerais da falha que fazem parte do novo design do módulo Az.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="f4dd8-136">Alterações de prefixo de substantivo do cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4dd8-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="f4dd8-137">No módulo AzureRM, os cmdlets usavam `AzureRM` ou `Azure` como prefixo de substantivo.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="f4dd8-138">O Az simplifica e normaliza os nomes dos cmdlets, de modo que todos os cmdlets usem 'Az' como seu prefixo de substantivo do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="f4dd8-139">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="f4dd8-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="f4dd8-140">Foi alterado para:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="f4dd8-141">Para simplificar a transição para esses novos nomes de cmdlets, o Az introduz dois novos cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) e [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="f4dd8-142">`Enable-AzureRmAlias` cria aliases para os nomes de cmdlets mais antigos no AzureRM que são mapeados para os nomes de cmdlets mais recentes do Az.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="f4dd8-143">O uso do argumento `-Scope` com `Enable-AzureRmAlias` permite que você escolha em que local os aliases serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="f4dd8-144">Por exemplo, o script a seguir no AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4dd8-145">Pode ser executado com alterações mínimas usando `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4dd8-146">A execução de `Enable-AzureRmAlias -Scope CurrentUser` habilitará os aliases para todas as sessões do PowerShell, para que, após a execução desse cmdlet, um script como este não precise ser alterado:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4dd8-147">Para obter detalhes completos sobre o uso dos cmdlets de alias, confira a [referência de Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="f4dd8-148">Quando você estiver pronto para desabilitar os aliases, `Disable-AzureRmAlias` removerá os aliases criados.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="f4dd8-149">Para obter detalhes completos, confira a [referência de Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4dd8-150">Ao desabilitar os aliases, verifique se eles estão desabilitados para _todos_ os escopos que tinham aliases habilitados.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="f4dd8-151">Alterações de nome de módulo</span><span class="sxs-lookup"><span data-stu-id="f4dd8-151">Module Name Changes</span></span>

<span data-ttu-id="f4dd8-152">Os nomes do módulo foram alterados de `AzureRM.*` para `Az.*`, exceto para os seguintes módulos:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="f4dd8-153">Módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="f4dd8-153">AzureRM module</span></span> | <span data-ttu-id="f4dd8-154">Módulo Az</span><span class="sxs-lookup"><span data-stu-id="f4dd8-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="f4dd8-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f4dd8-155">Azure.Storage</span></span> | <span data-ttu-id="f4dd8-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4dd8-156">Az.Storage</span></span> |
| <span data-ttu-id="f4dd8-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4dd8-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="f4dd8-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4dd8-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="f4dd8-159">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="f4dd8-159">AzureRM.Profile</span></span> | <span data-ttu-id="f4dd8-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4dd8-160">Az.Accounts</span></span> |
| <span data-ttu-id="f4dd8-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f4dd8-161">AzureRM.Insights</span></span> | <span data-ttu-id="f4dd8-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4dd8-162">Az.Monitor</span></span> |
| <span data-ttu-id="f4dd8-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f4dd8-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="f4dd8-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4dd8-164">Az.DataFactory</span></span> |
| <span data-ttu-id="f4dd8-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f4dd8-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="f4dd8-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4dd8-166">Az.DataFactory</span></span> |
| <span data-ttu-id="f4dd8-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f4dd8-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="f4dd8-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4dd8-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="f4dd8-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f4dd8-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="f4dd8-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4dd8-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="f4dd8-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f4dd8-171">AzureRM.Tags</span></span> | <span data-ttu-id="f4dd8-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4dd8-172">Az.Resources</span></span> |
| <span data-ttu-id="f4dd8-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f4dd8-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="f4dd8-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f4dd8-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="f4dd8-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f4dd8-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="f4dd8-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4dd8-176">Az.Billing</span></span> |
| <span data-ttu-id="f4dd8-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f4dd8-177">AzureRM.Consumption</span></span> | <span data-ttu-id="f4dd8-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4dd8-178">Az.Billing</span></span> |

<span data-ttu-id="f4dd8-179">As alterações nos nomes dos módulos significam que qualquer script que usa `#Requires` ou `Import-Module` para carregar módulos específicos precisarão ser alterados para usar o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="f4dd8-180">Para os módulos em que o sufixo do cmdlet não foi alterado, isso significa que, embora o nome do módulo tenha sido alterado, isso _não_ ocorreu com o sufixo que indica o espaço da operação.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="f4dd8-181">Como migrar as instruções #Requires e Import-Module</span><span class="sxs-lookup"><span data-stu-id="f4dd8-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="f4dd8-182">Os scripts que usam `#Requires` ou `Import-Module` para declarar uma dependência de módulos AzureRM precisam ser atualizados para usar os novos nomes de módulos.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="f4dd8-183">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="f4dd8-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="f4dd8-184">Deve ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="f4dd8-185">Para `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="f4dd8-186">Deve ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="f4dd8-187">Migração de invocações de cmdlet totalmente qualificadas</span><span class="sxs-lookup"><span data-stu-id="f4dd8-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="f4dd8-188">Os scripts que usam as invocações de cmdlet qualificadas por módulo, como:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="f4dd8-189">Precisam ser alterados para usar os novos nomes de módulos e cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="f4dd8-190">Como migrar dependências de manifesto de módulo</span><span class="sxs-lookup"><span data-stu-id="f4dd8-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="f4dd8-191">Os módulos que expressam dependências de módulos AzureRM por meio de um arquivo de manifesto (.psd1) de módulo precisarão atualizar os nomes de módulos em sua seção `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="f4dd8-192">Precisa ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="f4dd8-193">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="f4dd8-193">Removed modules</span></span>

<span data-ttu-id="f4dd8-194">Os seguintes módulos foram removidos:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="f4dd8-195">Não há mais suporte ativo para as ferramentas desses serviços.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="f4dd8-196">Os clientes são incentivados a mudar para serviços alternativos, assim que for conveniente.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="f4dd8-197">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f4dd8-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="f4dd8-198">O uso do Az com o PowerShell 5.1 para Windows exige a instalação do .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="f4dd8-199">O uso do PowerShell Core 6.x ou posterior não exige o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="f4dd8-200">Remoção temporária de logon de usuário usando PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd8-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="f4dd8-201">Devido a alterações no fluxo de autenticação para o .NET Standard, estamos temporariamente removendo o logon de usuário por meio do PSCredential.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="f4dd8-202">Essa funcionalidade será introduzida novamente na versão de 15/1/2019 do PowerShell 5.1 para Windows.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="f4dd8-203">Isso é abordado detalhadamente [neste problema do GitHub.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="f4dd8-204">Logon de código de dispositivo padrão em vez de prompt do navegador da Web</span><span class="sxs-lookup"><span data-stu-id="f4dd8-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="f4dd8-205">Devido a alterações no fluxo de autenticação para o .NET Standard, estamos usando o logon do dispositivo como o fluxo de logon padrão durante o logon interativo.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="f4dd8-206">O logon baseado em navegador da Web será reintroduzido no PowerShell 5.1 para Windows como o padrão na versão de 15/1/2019.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="f4dd8-207">Nesse momento, os usuários poderão escolher logon de dispositivo usando um parâmetro Switch.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="f4dd8-208">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="f4dd8-208">Module breaking changes</span></span>

<span data-ttu-id="f4dd8-209">Esta seção fornece detalhes sobre alterações específicas da falha para cmdlets e módulos individuais.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="f4dd8-210">Az.ApiManagement (anteriormente AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="f4dd8-211">Remoção dos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="f4dd8-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4dd8-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="f4dd8-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f4dd8-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="f4dd8-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f4dd8-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="f4dd8-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f4dd8-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="f4dd8-216">Use o cmdlet **Set-AzApiManagement** para definir essas propriedades</span><span class="sxs-lookup"><span data-stu-id="f4dd8-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="f4dd8-217">Remoção das seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-217">Removed the following properties:</span></span>
  - <span data-ttu-id="f4dd8-218">Removidas as propriedades `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` do tipo `PsApiManagementHostnameConfiguration` de `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="f4dd8-219">Em vez disso, use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` do tipo `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="f4dd8-220">Removida a propriedade `StaticIPs` de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="f4dd8-221">A propriedade foi dividida em `PublicIPAddresses` e `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="f4dd8-222">Removida a propriedade necessária `Location` do cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="f4dd8-223">Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="f4dd8-224">O parâmetro `InvoiceName` foi removido em favor do cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="f4dd8-225">Os scripts precisarão usar outros parâmetros de identidade para a fatura.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="f4dd8-226">Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="f4dd8-227">Removido o conjunto de parâmetros `GetSkusWithAccountParamSetName` do cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="f4dd8-228">Você deve obter Skus por Account Type e Location, em vez de usar ResourceGroupName e Account Name.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="f4dd8-229">Az.Compute (anteriormente AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="f4dd8-230">`IdentityIds` foram removidos da propriedade `Identity` nos Scripts dos objetos `PSVirtualMachine` e `PSVirtualMachineScaleSet`, que não devem mais usar o valor desse campo para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="f4dd8-231">O tipo de propriedade `InstanceView` do objeto `PSVirtualMachineScaleSetVM` foi alterado de `VirtualMachineInstanceView` para `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="f4dd8-232">As propriedades `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` foram removidas da propriedade `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="f4dd8-233">O tipo de propriedade `Sku` do objeto `PSSnapshotUpdate` foi alterado de `DiskSku` para `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="f4dd8-234">`VmScaleSetVMParameterSet` foi removido do cmdlet `Add-AzVMDataDisk`. Não é mais possível adicionar um disco de dados individualmente em uma VM ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="f4dd8-235">Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="f4dd8-236">O parâmetro `GatewayName` agora é obrigatório no cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="f4dd8-237">Removido o cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="f4dd8-238">Removido o parâmetro `LinkedServiceName` dos Scripts cmdlet `Get-AzDataFactoryV2ActivityRun`, que não devem mais usar o valor desse campo para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="f4dd8-239">Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="f4dd8-240">Removidos os cmdlets preteridos: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, e `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="f4dd8-241">Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="f4dd8-242">Os cmdlets a seguir tiveram o parâmetro `Encoding` alterado do tipo `FileSystemCmdletProviderEncoding` para `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="f4dd8-243">Essa alteração remove os valores de codificação `String` e `Oem`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="f4dd8-244">Todos os outros valores de codificação anteriores permanecem.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="f4dd8-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4dd8-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="f4dd8-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f4dd8-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="f4dd8-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f4dd8-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="f4dd8-248">Removido o alias da propriedade preterida `Tags` dos cmdlets `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="f4dd8-249">Uso de scripts</span><span class="sxs-lookup"><span data-stu-id="f4dd8-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f4dd8-250">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="f4dd8-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="f4dd8-251">Removidas as propriedades preteridas `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` e `FirewallAllowAzureIps` do objeto `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="f4dd8-252">Qualquer script que use o `PSDatalakeStoreAccount` retornado de `Get-AzDataLakeStoreAccount` não deve fazer referência a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="f4dd8-253">Az.KeyVault (anteriormente AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="f4dd8-254">A propriedade `PurgeDisabled` foi removida dos objetos `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes` e os Scripts não devem fazer referência à propriedade ```PurgeDisabled``` para tomar decisões de processamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="f4dd8-255">Az.Media (anteriormente AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="f4dd8-256">Removido o alias da propriedade preterida `Tags` dos Scripts cmdlet `New-AzMediaService` sendo usados</span><span class="sxs-lookup"><span data-stu-id="f4dd8-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f4dd8-257">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="f4dd8-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="f4dd8-258">Az.Monitor (anteriormente AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="f4dd8-259">Removidos os nomes no plural dos parâmetros `Categories` e `Timegrains` em favor de nomes de parâmetro no singular dos Scripts cmdlet `Set-AzDiagnosticSetting` sendo usados</span><span class="sxs-lookup"><span data-stu-id="f4dd8-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="f4dd8-260">Deve ser alterado para</span><span class="sxs-lookup"><span data-stu-id="f4dd8-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="f4dd8-261">Az.Network (anteriormente AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="f4dd8-262">Removido o parâmetro preterido `ResourceId` do cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="f4dd8-263">Removida a propriedade preterida `EnableVmProtection` do objeto `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="f4dd8-264">Removido o cmdlet preteridos `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="f4dd8-265">Os scripts não devem mais tomar decisões de processamento com base nos valores desses campos.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="f4dd8-266">Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="f4dd8-267">O conjunto de parâmetros padrão para `Get-AzOperationalInsightsDataSource` foi removido, e `ByWorkspaceNameByKind` tornou-se o conjunto de parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="f4dd8-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="f4dd8-268">Os scripts que listavam as fontes de dados sendo usadas</span><span class="sxs-lookup"><span data-stu-id="f4dd8-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="f4dd8-269">Devem ser alterados para especificar um Kind</span><span class="sxs-lookup"><span data-stu-id="f4dd8-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f4dd8-270">Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="f4dd8-271">Removido o parâmetro `Encryption` do cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="f4dd8-272">O parâmetro `TargetStorageAccountName` agora é obrigatório para restaurações de disco gerenciado no cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f4dd8-273">Removidos os parâmetros `StorageAccountName` e `StorageAccountResourceGroupName` no cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f4dd8-274">Removido o parâmetro `Name` no cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="f4dd8-275">Az.Resources (anteriormente AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="f4dd8-276">Removido o parâmetro `Sku` do cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="f4dd8-277">Removido o parâmetro de `Password` das Senhas cmdlets `New-AzADServicePrincipal` e `New-AzADSpCredential` automaticamente geradas, nos scripts que forneciam a senha:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="f4dd8-278">Devem ser alterados para recuperar a senha da saída:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="f4dd8-279">Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="f4dd8-280">Os seguintes tipos de retorno de cmdlet foram alterados:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="f4dd8-281">A propriedade `ServiceTypeHealthPolicies` do tipo `ApplicationHealthPolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f4dd8-282">A propriedade `ApplicationHealthPolicies` do tipo `ClusterUpgradeDeltaHealthPolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f4dd8-283">A propriedade `OverrideUserUpgradePolicy` do tipo `ClusterUpgradePolicy` foi removida.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="f4dd8-284">Essas alterações afetam os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="f4dd8-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f4dd8-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f4dd8-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f4dd8-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f4dd8-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f4dd8-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f4dd8-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f4dd8-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f4dd8-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f4dd8-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="f4dd8-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f4dd8-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f4dd8-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f4dd8-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f4dd8-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f4dd8-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f4dd8-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f4dd8-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f4dd8-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f4dd8-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f4dd8-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f4dd8-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f4dd8-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f4dd8-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="f4dd8-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="f4dd8-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="f4dd8-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f4dd8-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="f4dd8-299">Az.Sql (anteriormente AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="f4dd8-300">Removidos os parâmetros `State` e `ResourceId` do cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f4dd8-301">Removidos os cmdlets preteridos: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="f4dd8-302">Removido o parâmetro preterido `Current` do cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f4dd8-303">Removido o parâmetro preterido `DatabaseName` do cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="f4dd8-304">Removido o parâmetro preterido `PrivilegedLogin` do cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="f4dd8-305">Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="f4dd8-306">Para dar suporte à criação de um contexto de armazenamento Oauth com apenas o nome da conta de armazenamento, o conjunto de parâmetros padrão foi alterado para `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="f4dd8-307">Exemplo: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="f4dd8-308">O parâmetro `Location` agora é obrigatório no cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="f4dd8-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="f4dd8-309">Os métodos da API de armazenamento agora usam o padrão assíncrono baseado em tarefas (TAP), em vez de chamadas à API síncronas.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="f4dd8-310">Os seguintes exemplos demonstram os novos comandos assíncronos:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="f4dd8-311">Instantâneo de Blob</span><span class="sxs-lookup"><span data-stu-id="f4dd8-311">Blob Snapshot</span></span>

<span data-ttu-id="f4dd8-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="f4dd8-313">Az:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="f4dd8-314">Compartilhar instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4dd8-314">Share Snapshot</span></span>

<span data-ttu-id="f4dd8-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="f4dd8-316">Az:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="f4dd8-317">Cancelar a exclusão de blob com exclusão reversível</span><span class="sxs-lookup"><span data-stu-id="f4dd8-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="f4dd8-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="f4dd8-319">Az:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="f4dd8-320">Definir camada do Blob</span><span class="sxs-lookup"><span data-stu-id="f4dd8-320">Set Blob Tier</span></span>

<span data-ttu-id="f4dd8-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="f4dd8-322">Az:</span><span class="sxs-lookup"><span data-stu-id="f4dd8-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="f4dd8-323">Az.Websites (anteriormente AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f4dd8-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="f4dd8-324">Removidas as propriedades preteridas `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite` dos objetos</span><span class="sxs-lookup"><span data-stu-id="f4dd8-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
