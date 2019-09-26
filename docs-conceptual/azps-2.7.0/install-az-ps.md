---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: e302e49d95b6bc15750366c9eb960a6fec80c1a4
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226245"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="d7961-103">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7961-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="d7961-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d7961-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="d7961-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="d7961-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="d7961-106">Para o módulo Az, atualmente não há suporte para outros métodos de instalação.</span><span class="sxs-lookup"><span data-stu-id="d7961-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7961-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7961-107">Requirements</span></span>

<span data-ttu-id="d7961-108">O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="d7961-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="d7961-109">Se você não tiver certeza se tem o PowerShell ou se está no macOS ou no Linux, [instale a última versão do PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="d7961-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="d7961-110">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="d7961-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="d7961-111">Para executar o Azure PowerShell no PowerShell 5.1 no Windows:</span><span class="sxs-lookup"><span data-stu-id="d7961-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="d7961-112">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário.</span><span class="sxs-lookup"><span data-stu-id="d7961-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="d7961-113">Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="d7961-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="d7961-114">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="d7961-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="d7961-115">Não há nenhum requisito adicional para o Azure PowerShell ao usar o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="d7961-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="d7961-116">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7961-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="d7961-117">__Não__ é possível instalar os módulos AzureRM e Az para o PowerShell 5.1 para Windows ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d7961-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="d7961-118">Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell Core 6.x ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d7961-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="d7961-119">Para fazer isso, [instale o PowerShell Core 6.x ou posterior](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) e, depois, siga estas instruções em um terminal do PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="d7961-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="d7961-120">O método de instalação recomendado deve apenas ser instalado para o usuário ativo:</span><span class="sxs-lookup"><span data-stu-id="d7961-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="d7961-121">Se desejar instalar para todos os usuários em um sistema, isso requererá privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="d7961-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="d7961-122">Em uma sessão do PowerShell com privilégios elevados executada como administrador ou com o comando `sudo` em macOS ou Linux:</span><span class="sxs-lookup"><span data-stu-id="d7961-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="d7961-123">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d7961-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="d7961-124">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="d7961-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="d7961-125">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="d7961-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="d7961-126">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d7961-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d7961-127">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d7961-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d7961-128">solução de problemas</span><span class="sxs-lookup"><span data-stu-id="d7961-128">Troubleshooting</span></span>

<span data-ttu-id="d7961-129">Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d7961-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="d7961-130">Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d7961-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="d7961-131">Conexão de blocos de proxy</span><span class="sxs-lookup"><span data-stu-id="d7961-131">Proxy blocks connection</span></span>

<span data-ttu-id="d7961-132">Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy.</span><span class="sxs-lookup"><span data-stu-id="d7961-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="d7961-133">Sistemas operacionais diferentes terão requisitos diferentes para configurar um proxy de todo o sistema, que não são abordados detalhadamente aqui.</span><span class="sxs-lookup"><span data-stu-id="d7961-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="d7961-134">Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d7961-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="d7961-135">O PowerShell em si pode não ser configurado para usar esse proxy automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d7961-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="d7961-136">Com o PowerShell 5.1 e posterior, configure o proxy a ser usado para uma sessão do PowerShell com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d7961-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="d7961-137">Caso suas credenciais do sistema operacional estejam configuradas corretamente, isso roteará as solicitações do PowerShell por meio do proxy.</span><span class="sxs-lookup"><span data-stu-id="d7961-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="d7961-138">Para manter essa configuração entre as sessões, adicione o comando a um [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d7961-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="d7961-139">Para instalar o pacote, o proxy precisa permitir conexões HTTPS para o seguinte endereço:</span><span class="sxs-lookup"><span data-stu-id="d7961-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="d7961-140">Entrar</span><span class="sxs-lookup"><span data-stu-id="d7961-140">Sign in</span></span>

<span data-ttu-id="d7961-141">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7961-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="d7961-142">Se você desabilitou o carregamento automático do módulo, importe manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="d7961-142">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="d7961-143">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="d7961-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="d7961-144">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="d7961-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d7961-145">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d7961-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="d7961-146">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7961-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="d7961-147">Devido ao modo de empacotamento do módulo Az, o comando [Update-Module](/powershell/module/powershellget/update-module) não atualizará a instalação corretamente.</span><span class="sxs-lookup"><span data-stu-id="d7961-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="d7961-148">Quando você instala o módulo Az, na verdade, ele coleta e instala todos os submódulos dependentes e que fornecem os cmdlets para cada serviço.</span><span class="sxs-lookup"><span data-stu-id="d7961-148">When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service.</span></span>
<span data-ttu-id="d7961-149">Isso significa que, para atualizar o módulo do Azure PowerShell, você precisará fazer uma __reinstalação__, em vez de apenas uma __atualização__.</span><span class="sxs-lookup"><span data-stu-id="d7961-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="d7961-150">Isso é feito da mesma forma que a instalação, mas talvez você precise adicionar o argumento `-Force`:</span><span class="sxs-lookup"><span data-stu-id="d7961-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="d7961-151">Embora isso possa substituir os módulos instalados, você ainda poderá ter versões mais antigas no sistema.</span><span class="sxs-lookup"><span data-stu-id="d7961-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="d7961-152">Para saber como remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d7961-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="d7961-153">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7961-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="d7961-154">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d7961-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="d7961-155">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d7961-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="d7961-156">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d7961-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="d7961-157">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="d7961-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="d7961-158">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="d7961-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="d7961-159">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="d7961-159">Provide feedback</span></span>

<span data-ttu-id="d7961-160">Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d7961-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="d7961-161">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d7961-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d7961-162">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d7961-162">Next Steps</span></span>

<span data-ttu-id="d7961-163">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d7961-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="d7961-164">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="d7961-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>