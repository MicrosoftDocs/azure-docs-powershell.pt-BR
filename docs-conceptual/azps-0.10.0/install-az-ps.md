---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: fa5b2d80b9caf216f218c85fe49ea4cc7f062404
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121982"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="1e3e8-103">Instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e3e8-103">Install Azure PowerShell</span></span>

<span data-ttu-id="1e3e8-104">Este artigo explica como instalar os módulos do Azure PowerShell usando o [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="1e3e8-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="1e3e8-106">O Azure PowerShell também está disponível no Azure [Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e3e8-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e3e8-107">Requirements</span></span>

<span data-ttu-id="1e3e8-108">O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="1e3e8-109">Você deve instalar a [versão mais recente do PowerShell](/powershell/scripting/install/installing-powershell) disponível para seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-109">You should install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="1e3e8-110">O Azure PowerShell não tem requisitos adicionais quando executado no PowerShell 6.2.4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-110">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="1e3e8-111">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-111">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="1e3e8-112">Para usar o Azure PowerShell no PowerShell 5.1 no Windows:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="1e3e8-113">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="1e3e8-114">Se você está usando o Windows 10 versão 1607 ou superior, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-114">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="1e3e8-115">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="1e3e8-116">Verifique se tem a versão mais recente do PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="1e3e8-117">Execute `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-117">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="1e3e8-118">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e3e8-118">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="1e3e8-119">Não há compatibilidade na instalação dos módulos AzureRM e Az no PowerShell 5.1 para Windows ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-119">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="1e3e8-120">Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell 6.2.4.x ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-120">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="1e3e8-121">O uso dos cmdlets do PowerShellGet é o método de instalação preferencial.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-121">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="1e3e8-122">Instale o módulo Az somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-122">Install the Az module for the current user only.</span></span> <span data-ttu-id="1e3e8-123">Este é o escopo de instalação recomendado.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-123">This is the recommended installation scope.</span></span> <span data-ttu-id="1e3e8-124">Esse método funciona da mesma forma nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-124">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="1e3e8-125">Execute o seguinte comando em uma sessão do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-125">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="1e3e8-126">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-126">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1e3e8-127">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1e3e8-128">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-128">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="1e3e8-129">A instalação do módulo para todos os usuários de um sistema requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-129">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="1e3e8-130">Inicie a sessão do PowerShell usando **Executar como administrador** no Windows ou use o comando `sudo` no macOS ou Linux:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-130">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="1e3e8-131">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-131">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1e3e8-132">A instalação dele baixa todos os módulos em disponibilidade geral do Az Powershell e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-132">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="1e3e8-133">Instalar offline</span><span class="sxs-lookup"><span data-stu-id="1e3e8-133">Install offline</span></span>

<span data-ttu-id="1e3e8-134">Em alguns ambientes, não é possível se conectar à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-134">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="1e3e8-135">Nessas situações, você ainda pode instalar offline usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-135">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="1e3e8-136">Baixe os módulos em outro local da sua rede e use-os como uma origem de instalação.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-136">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="1e3e8-137">Esse método permite que você armazene módulos do PowerShell em cache em um único servidor ou compartilhamento de arquivo para serem implantados com o PowerShellGet em sistemas desconectados.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-137">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="1e3e8-138">Saiba como configurar um repositório local e instalar em sistemas desconectados com [Trabalhar com repositórios PowerShellGet locais](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-138">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="1e3e8-139">[Baixe o MSI (Microsoft Windows Installer) do Azure PowerShell](install-az-ps-msi.md) em um computador conectado à rede e, em seguida, copie o instalador para sistemas sem acesso à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-139">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="1e3e8-140">Tenha em mente que o instalador do MSI só funciona para PowerShell 5.1 no Windows.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-140">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="1e3e8-141">Salve o módulo com [Save-Module](/powershell/module/PowershellGet/Save-Module) em um compartilhamento de arquivo ou salve-o em outra fonte e copie-o manualmente para outros computadores:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-141">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="1e3e8-142">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="1e3e8-142">Troubleshooting</span></span>

<span data-ttu-id="1e3e8-143">Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-143">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="1e3e8-144">Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-144">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="1e3e8-145">Conexão de blocos de proxy</span><span class="sxs-lookup"><span data-stu-id="1e3e8-145">Proxy blocks connection</span></span>

<span data-ttu-id="1e3e8-146">Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-146">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="1e3e8-147">Sistemas operacionais e ambientes de rede diferentes têm requisitos diferentes para configurar um proxy para todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-147">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="1e3e8-148">Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-148">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="1e3e8-149">O PowerShell em si pode não ser configurado para usar esse proxy automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-149">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="1e3e8-150">Com o PowerShell 5.1 e posterior, configure a sessão do PowerShell para usar um proxy por meio dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-150">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="1e3e8-151">Caso suas credenciais do sistema operacional estejam configuradas corretamente, essa configuração roteará as solicitações do PowerShell por meio do proxy.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-151">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="1e3e8-152">Para manter essa configuração entre as sessões, adicione os comandos ao seu [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-152">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="1e3e8-153">Para instalar o pacote, o proxy precisa permitir conexões HTTPS com o seguinte endereço:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-153">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="1e3e8-154">Entrar</span><span class="sxs-lookup"><span data-stu-id="1e3e8-154">Sign in</span></span>

<span data-ttu-id="1e3e8-155">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-155">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="1e3e8-156">Se você desabilitou o carregamento automático do módulo, importe manualmente o módulo com `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-156">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="1e3e8-157">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-157">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="1e3e8-158">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-158">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1e3e8-159">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-159">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="1e3e8-160">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e3e8-160">Update the Azure PowerShell module</span></span>

<span data-ttu-id="1e3e8-161">Para atualizar qualquer módulo do PowerShell, você deve usar o mesmo método usado para instalar o módulo.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-161">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="1e3e8-162">Por exemplo, caso tenha usado `Install-Module` originalmente, você deverá usar [Update-Module](/powershell/module/powershellget/update-module) para obter a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-162">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="1e3e8-163">Caso tenha usado originalmente o pacote MSI, você deverá baixar e instalar o novo pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-163">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="1e3e8-164">Os cmdlets do PowerShellGet não podem atualizar os módulos que foram instalados por meio de um pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-164">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="1e3e8-165">Os pacotes MSI não atualizam módulos que foram instalados usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-165">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="1e3e8-166">Se você tiver problemas ao atualizar usando o PowershellGet, deverá **reinstalar** em vez de **atualizar**.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-166">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="1e3e8-167">A reinstalação é feita da mesma forma que a instalação, mas você precisa adicionar o parâmetro `-Force`:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-167">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="1e3e8-168">Diferentemente das instalações baseadas em MSI, instalar ou atualizar usando o PowerShellGet não remove as versões mais antigas que possam existir em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-168">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="1e3e8-169">Para remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-169">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="1e3e8-170">Para obter mais informações sobre instalações baseadas em MSI, consulte [Instalar o Azure PowerShell com um MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-170">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="1e3e8-171">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e3e8-171">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="1e3e8-172">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-172">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="1e3e8-173">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-173">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="1e3e8-174">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-174">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="1e3e8-175">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-175">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="1e3e8-176">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o parâmetro `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="1e3e8-176">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="1e3e8-177">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="1e3e8-177">Provide feedback</span></span>

<span data-ttu-id="1e3e8-178">Se você encontrar um bug no Azure PowerShell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-178">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="1e3e8-179">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-179">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1e3e8-180">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1e3e8-180">Next Steps</span></span>

<span data-ttu-id="1e3e8-181">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-181">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="1e3e8-182">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1e3e8-182">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
