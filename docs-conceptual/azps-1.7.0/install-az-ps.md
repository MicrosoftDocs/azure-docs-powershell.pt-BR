---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363620"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="d14da-103">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d14da-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="d14da-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d14da-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="d14da-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="d14da-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="d14da-106">Para o módulo Az, atualmente não há suporte para outros métodos de instalação.</span><span class="sxs-lookup"><span data-stu-id="d14da-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d14da-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d14da-107">Requirements</span></span>

<span data-ttu-id="d14da-108">O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell 6 em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="d14da-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="d14da-109">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="d14da-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="d14da-110">Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="d14da-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="d14da-111">As informações de instalação para sua plataforma estão vinculadas a partir dessa página.</span><span class="sxs-lookup"><span data-stu-id="d14da-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="d14da-112">Se você estiver usando o PowerShell 5 no Windows, também precisará ter instalado o .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="d14da-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="d14da-113">Para obter instruções sobre como atualizar ou instalar uma nova versão do .NET Framework, confira o [guia de instalação do .NET Framework](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="d14da-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="d14da-114">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d14da-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d14da-115">É possível ter ambos os módulos AzureRM e Az instalados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d14da-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="d14da-116">Caso tenha ambos os módulos instalados, __não habilite aliases__.</span><span class="sxs-lookup"><span data-stu-id="d14da-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="d14da-117">Habilitar aliases causará conflitos entre os cmdlets AzureRM e os aliases de comando Az, podendo levar a comportamentos inesperados.</span><span class="sxs-lookup"><span data-stu-id="d14da-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="d14da-118">Antes de instalar o módulo Az, recomenda-se desinstalar o AzureRM.</span><span class="sxs-lookup"><span data-stu-id="d14da-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="d14da-119">É possível desinstalar o AzureRM ou habilitar aliases a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d14da-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="d14da-120">Para saber mais sobre os aliases de comando do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="d14da-121">Para obter instruções de desinstalação, confira [Desinstalar o módulo AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="d14da-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="d14da-122">Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d14da-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="d14da-123">Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):</span><span class="sxs-lookup"><span data-stu-id="d14da-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="d14da-124">Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="d14da-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="d14da-125">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d14da-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="d14da-126">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="d14da-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="d14da-127">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="d14da-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="d14da-128">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d14da-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d14da-129">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d14da-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="d14da-130">Entrar</span><span class="sxs-lookup"><span data-stu-id="d14da-130">Sign in</span></span>

<span data-ttu-id="d14da-131">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="d14da-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="d14da-132">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="d14da-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="d14da-133">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="d14da-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="d14da-134">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="d14da-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d14da-135">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="d14da-136">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d14da-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="d14da-137">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="d14da-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="d14da-138">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d14da-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="d14da-139">Para saber como remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="d14da-140">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d14da-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="d14da-141">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d14da-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="d14da-142">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d14da-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="d14da-143">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="d14da-144">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="d14da-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="d14da-145">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="d14da-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="d14da-146">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="d14da-146">Provide feedback</span></span>

<span data-ttu-id="d14da-147">Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d14da-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="d14da-148">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d14da-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d14da-149">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d14da-149">Next Steps</span></span>

<span data-ttu-id="d14da-150">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="d14da-151">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="d14da-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
