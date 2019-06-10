---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365741"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="bcae8-103">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bcae8-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="bcae8-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bcae8-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="bcae8-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="bcae8-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="bcae8-106">Para o módulo Az, atualmente não há suporte para outros métodos de instalação.</span><span class="sxs-lookup"><span data-stu-id="bcae8-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcae8-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcae8-107">Requirements</span></span>

<span data-ttu-id="bcae8-108">O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="bcae8-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="bcae8-109">Se você não tiver certeza se tem o PowerShell ou se está no macOS ou no Linux, [instale a última versão do PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="bcae8-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="bcae8-110">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="bcae8-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="bcae8-111">Para executar o Azure PowerShell no PowerShell 5.1 no Windows:</span><span class="sxs-lookup"><span data-stu-id="bcae8-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="bcae8-112">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário.</span><span class="sxs-lookup"><span data-stu-id="bcae8-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="bcae8-113">Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="bcae8-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="bcae8-114">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="bcae8-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="bcae8-115">Não há nenhum requisito adicional para o Azure PowerShell ao usar o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="bcae8-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="bcae8-116">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bcae8-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="bcae8-117">É possível ter ambos os módulos AzureRM e Az instalados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bcae8-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="bcae8-118">Caso tenha ambos os módulos instalados, __não habilite aliases__.</span><span class="sxs-lookup"><span data-stu-id="bcae8-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="bcae8-119">Habilitar aliases causará conflitos entre os cmdlets AzureRM e os aliases de comando Az, podendo levar a comportamentos inesperados.</span><span class="sxs-lookup"><span data-stu-id="bcae8-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="bcae8-120">Antes de instalar o módulo Az, recomenda-se desinstalar o AzureRM.</span><span class="sxs-lookup"><span data-stu-id="bcae8-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="bcae8-121">É possível desinstalar o AzureRM ou habilitar aliases a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="bcae8-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="bcae8-122">Para saber mais sobre os aliases de comando do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="bcae8-123">Para obter instruções de desinstalação, confira [Desinstalar o módulo AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="bcae8-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="bcae8-124">Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcae8-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="bcae8-125">Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):</span><span class="sxs-lookup"><span data-stu-id="bcae8-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="bcae8-126">Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="bcae8-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="bcae8-127">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bcae8-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="bcae8-128">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="bcae8-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="bcae8-129">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="bcae8-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="bcae8-130">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcae8-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="bcae8-131">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="bcae8-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="bcae8-132">Entrar</span><span class="sxs-lookup"><span data-stu-id="bcae8-132">Sign in</span></span>

<span data-ttu-id="bcae8-133">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="bcae8-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="bcae8-134">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="bcae8-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="bcae8-135">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="bcae8-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="bcae8-136">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="bcae8-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bcae8-137">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="bcae8-138">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bcae8-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="bcae8-139">Devido ao modo de empacotamento do módulo Az, o comando [Update-Module](/powershell/module/powershellget/update-module) não atualizará a instalação corretamente.</span><span class="sxs-lookup"><span data-stu-id="bcae8-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="bcae8-140">O Az é tecnicamente um metamódulo, abrangendo todos os submódulos que contêm cmdlets para interagir com os serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="bcae8-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="bcae8-141">Isso significa que, para atualizar o módulo do Azure PowerShell, você precisará fazer uma __reinstalação__, em vez de apenas uma __atualização__.</span><span class="sxs-lookup"><span data-stu-id="bcae8-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="bcae8-142">Isso é feito da mesma forma que a instalação, mas talvez você precise adicionar o argumento `-Force`:</span><span class="sxs-lookup"><span data-stu-id="bcae8-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="bcae8-143">Embora isso possa substituir os módulos instalados, você ainda poderá ter versões mais antigas no sistema.</span><span class="sxs-lookup"><span data-stu-id="bcae8-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="bcae8-144">Para saber como remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="bcae8-145">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bcae8-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="bcae8-146">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcae8-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="bcae8-147">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="bcae8-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="bcae8-148">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="bcae8-149">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="bcae8-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="bcae8-150">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="bcae8-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="bcae8-151">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="bcae8-151">Provide feedback</span></span>

<span data-ttu-id="bcae8-152">Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="bcae8-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="bcae8-153">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="bcae8-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bcae8-154">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="bcae8-154">Next Steps</span></span>

<span data-ttu-id="bcae8-155">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="bcae8-156">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="bcae8-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
