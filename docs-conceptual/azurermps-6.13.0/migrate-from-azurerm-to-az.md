---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828715"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="3b337-103">Migrar do AzureRM para o Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b337-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="3b337-104">O módulo Az tem paridade de recursos com o AzureRM, mas usa nomes de cmdlets menores e mais consistentes.</span><span class="sxs-lookup"><span data-stu-id="3b337-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="3b337-105">Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="3b337-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="3b337-106">Para facilitar a transição, o Az oferece ferramentas para permitir a execução de seus scripts existentes usando o AzureRM.</span><span class="sxs-lookup"><span data-stu-id="3b337-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="3b337-107">A migração para um novo conjunto de comandos nem sempre é conveniente, mas este artigo ajudará você a começar a realizar a transição para o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="3b337-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="3b337-108">Garanta que seus scripts existentes funcionem com a versão mais recente do AzureRM</span><span class="sxs-lookup"><span data-stu-id="3b337-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="3b337-109">Essa é a etapa mais importante!</span><span class="sxs-lookup"><span data-stu-id="3b337-109">This is the most important step!</span></span> <span data-ttu-id="3b337-110">Execute seus scripts existentes e certifique-se de que eles funcionam com a versão _mais recente_ do AzureRM (__6.13.0__).</span><span class="sxs-lookup"><span data-stu-id="3b337-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.13.0__).</span></span> <span data-ttu-id="3b337-111">Se os scripts não funcionarem, certifique-se de ler o [Guia de migração do AzureRM](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="3b337-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="3b337-112">Instalar o módulo Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b337-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="3b337-113">A primeira etapa é instalar o módulo Az em sua plataforma.</span><span class="sxs-lookup"><span data-stu-id="3b337-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="3b337-114">Para instalar o Az, você precisa desinstalar o AzureRM.</span><span class="sxs-lookup"><span data-stu-id="3b337-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="3b337-115">Nas etapas a seguir, você aprenderá como continuar executando seus scripts existentes e habilitar a compatibilidade para os nomes de cmdlet antigos.</span><span class="sxs-lookup"><span data-stu-id="3b337-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="3b337-116">Para instalar o módulo Az do Azure PowerShell, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="3b337-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="3b337-117">[Desinstale o módulo AzureRM](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3b337-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="3b337-118">Certifique-se de remover _todas_ as versões instaladas do AzureRM, não apenas a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="3b337-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="3b337-119">Instale o módulo Az</span><span class="sxs-lookup"><span data-stu-id="3b337-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="3b337-120"><a name="aliases"/>Habilite o modo de alias do AzureRM</span><span class="sxs-lookup"><span data-stu-id="3b337-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="3b337-121">Com o AzureRM desinstalado e seus scripts funcionando com a versão mais recente do AzureRM, chegou o momento de habilitar o modo de compatibilidade para o módulo Az.</span><span class="sxs-lookup"><span data-stu-id="3b337-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="3b337-122">A compatibilidade é habilitada com o comando:</span><span class="sxs-lookup"><span data-stu-id="3b337-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="3b337-123">Os aliases permitem a capacidade de usar nomes de cmdlets antigos com o módulo `Az` instalado.</span><span class="sxs-lookup"><span data-stu-id="3b337-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="3b337-124">Esses aliases são gravados no perfil do usuário para o escopo escolhido.</span><span class="sxs-lookup"><span data-stu-id="3b337-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="3b337-125">Se não existir perfis de usuário, um perfil será criado.</span><span class="sxs-lookup"><span data-stu-id="3b337-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="3b337-126">Você pode usar outro `-Scope` para este comando, mas isso não é recomendado!</span><span class="sxs-lookup"><span data-stu-id="3b337-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="3b337-127">Os aliases são gravados no perfil do usuário do escopo escolhido, portanto, mantenha-os habilitados para um escopo o mais limitado possível.</span><span class="sxs-lookup"><span data-stu-id="3b337-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="3b337-128">Habilitar os aliases em todo o sistema também pode causar problemas para outros usuários que têm o `AzureRM` instalado em seu escopo local.</span><span class="sxs-lookup"><span data-stu-id="3b337-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="3b337-129">Após habilitar o modo de alias, execute seus scripts novamente para confirmar que eles ainda funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="3b337-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="3b337-130">Alterar os nomes de cmdlets e as importações de módulos</span><span class="sxs-lookup"><span data-stu-id="3b337-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="3b337-131">Em geral, os nomes de módulos foram alterados para que `AzureRM` e `Azure` tornem-se `Az`, e o mesmo ocorreu com os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3b337-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="3b337-132">Por exemplo, o módulo `AzureRM.Compute` foi renomeado para `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="3b337-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="3b337-133">`New-AzureRmVM` se tornou `New-AzVM`, e `Get-AzureStorageBlob` agora é `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="3b337-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="3b337-134">Há exceções para essa alteração de nomenclatura e você deve estar atento antes de fazer qualquer renomeação:</span><span class="sxs-lookup"><span data-stu-id="3b337-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="3b337-135">Módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="3b337-135">AzureRM module</span></span> | <span data-ttu-id="3b337-136">Módulo Az</span><span class="sxs-lookup"><span data-stu-id="3b337-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="3b337-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="3b337-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="3b337-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3b337-138">Az.DataFactory</span></span> |
| <span data-ttu-id="3b337-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3b337-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="3b337-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3b337-140">Az.DataFactory</span></span> |
| <span data-ttu-id="3b337-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3b337-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="3b337-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3b337-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="3b337-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3b337-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="3b337-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3b337-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="3b337-145">Resumo</span><span class="sxs-lookup"><span data-stu-id="3b337-145">Summary</span></span>

<span data-ttu-id="3b337-146">Seguindo essas etapas, é possível atualizar todos os scripts existentes para usar o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="3b337-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="3b337-147">Se você tiver dúvidas ou problemas com estas etapas que dificultaram a migração, deixe seu comentário sobre este artigo para que possamos melhorar as instruções.</span><span class="sxs-lookup"><span data-stu-id="3b337-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>
