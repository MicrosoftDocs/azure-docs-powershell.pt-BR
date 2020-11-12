---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 39b0a700c1568f7c241c1abff38665428f326825
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408416"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="07dab-103">Instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07dab-103">Install Azure PowerShell</span></span>

<span data-ttu-id="07dab-104">Este artigo explica como instalar os módulos do Azure PowerShell usando o [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="07dab-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="07dab-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="07dab-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="07dab-106">O Azure PowerShell também está disponível no Azure [Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="07dab-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="07dab-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07dab-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="07dab-108">O PowerShell 7.x e posterior é a versão recomendada do PowerShell para uso com Azure PowerShell em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="07dab-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="07dab-109">O Azure PowerShell funciona com o PowerShell 6.2.4 e posterior em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="07dab-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="07dab-110">Ele também é compatível com o PowerShell 5.1 no Windows.</span><span class="sxs-lookup"><span data-stu-id="07dab-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="07dab-111">Instale a [versão mais recente do PowerShell](/powershell/scripting/install/installing-powershell) disponível para seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="07dab-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="07dab-112">O Azure PowerShell não tem requisitos adicionais quando executado no PowerShell 6.2.4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="07dab-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="07dab-113">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="07dab-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="07dab-114">Para usar o Azure PowerShell no PowerShell 5.1 no Windows:</span><span class="sxs-lookup"><span data-stu-id="07dab-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="07dab-115">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="07dab-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="07dab-116">Se você está usando o Windows 10 versão 1607 ou superior, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="07dab-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="07dab-117">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="07dab-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="07dab-118">Verifique se tem a versão mais recente do PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="07dab-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="07dab-119">Execute `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="07dab-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="07dab-120">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07dab-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="07dab-121">Não há compatibilidade na instalação dos módulos AzureRM e Az no PowerShell 5.1 para Windows ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="07dab-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="07dab-122">Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell Core 6.x ou posterior.</span><span class="sxs-lookup"><span data-stu-id="07dab-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="07dab-123">O uso dos cmdlets do PowerShellGet é o método de instalação preferencial.</span><span class="sxs-lookup"><span data-stu-id="07dab-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="07dab-124">Instale o módulo Az somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="07dab-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="07dab-125">Este é o escopo de instalação recomendado.</span><span class="sxs-lookup"><span data-stu-id="07dab-125">This is the recommended installation scope.</span></span> <span data-ttu-id="07dab-126">Esse método funciona da mesma forma nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="07dab-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="07dab-127">Execute o seguinte comando em uma sessão do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="07dab-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="07dab-128">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="07dab-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="07dab-129">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="07dab-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="07dab-130">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="07dab-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="07dab-131">A instalação do módulo para todos os usuários de um sistema requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="07dab-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="07dab-132">Inicie a sessão do PowerShell usando **Executar como administrador** no Windows ou use o comando `sudo` no macOS ou Linux:</span><span class="sxs-lookup"><span data-stu-id="07dab-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="07dab-133">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07dab-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="07dab-134">A instalação dele baixa todos os módulos em disponibilidade geral do Az Powershell e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="07dab-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="07dab-135">Instalar offline</span><span class="sxs-lookup"><span data-stu-id="07dab-135">Install offline</span></span>

<span data-ttu-id="07dab-136">Em alguns ambientes, não é possível se conectar à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07dab-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="07dab-137">Nessas situações, você ainda pode instalar offline usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="07dab-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="07dab-138">Baixe os módulos em outro local da sua rede e use-os como uma origem de instalação.</span><span class="sxs-lookup"><span data-stu-id="07dab-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="07dab-139">Esse método permite que você armazene módulos do PowerShell em cache em um único servidor ou compartilhamento de arquivo para serem implantados com o PowerShellGet em sistemas desconectados.</span><span class="sxs-lookup"><span data-stu-id="07dab-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="07dab-140">Saiba como configurar um repositório local e instalar em sistemas desconectados com [Trabalhar com repositórios PowerShellGet locais](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="07dab-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="07dab-141">[Baixe o MSI (Microsoft Windows Installer) do Azure PowerShell](install-az-ps-msi.md) em um computador conectado à rede e, em seguida, copie o instalador para sistemas sem acesso à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07dab-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="07dab-142">Tenha em mente que o instalador do MSI só funciona para PowerShell 5.1 no Windows.</span><span class="sxs-lookup"><span data-stu-id="07dab-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="07dab-143">Salve o módulo com [Save-Module](/powershell/module/PowershellGet/Save-Module) em um compartilhamento de arquivo ou salve-o em outra fonte e copie-o manualmente para outros computadores:</span><span class="sxs-lookup"><span data-stu-id="07dab-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="07dab-144">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="07dab-144">Troubleshooting</span></span>

<span data-ttu-id="07dab-145">Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07dab-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="07dab-146">Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="07dab-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="07dab-147">Conexão de blocos de proxy</span><span class="sxs-lookup"><span data-stu-id="07dab-147">Proxy blocks connection</span></span>

<span data-ttu-id="07dab-148">Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy.</span><span class="sxs-lookup"><span data-stu-id="07dab-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="07dab-149">Sistemas operacionais e ambientes de rede diferentes têm requisitos diferentes para configurar um proxy para todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="07dab-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="07dab-150">Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="07dab-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="07dab-151">O PowerShell em si pode não ser configurado para usar esse proxy automaticamente.</span><span class="sxs-lookup"><span data-stu-id="07dab-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="07dab-152">Com o PowerShell 5.1 e posterior, configure a sessão do PowerShell para usar um proxy por meio dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="07dab-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="07dab-153">Caso suas credenciais do sistema operacional estejam configuradas corretamente, essa configuração roteará as solicitações do PowerShell por meio do proxy.</span><span class="sxs-lookup"><span data-stu-id="07dab-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="07dab-154">Para manter essa configuração entre as sessões, adicione os comandos ao seu [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="07dab-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="07dab-155">Para instalar o pacote, o proxy precisa permitir conexões HTTPS com o seguinte endereço:</span><span class="sxs-lookup"><span data-stu-id="07dab-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="07dab-156">Entrar</span><span class="sxs-lookup"><span data-stu-id="07dab-156">Sign in</span></span>

<span data-ttu-id="07dab-157">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="07dab-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="07dab-158">Se você desabilitou o carregamento automático do módulo, importe manualmente o módulo com `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="07dab-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="07dab-159">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="07dab-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="07dab-160">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="07dab-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="07dab-161">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="07dab-162">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07dab-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="07dab-163">Para atualizar qualquer módulo do PowerShell, você deve usar o mesmo método usado para instalar o módulo.</span><span class="sxs-lookup"><span data-stu-id="07dab-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="07dab-164">Por exemplo, caso tenha usado `Install-Module` originalmente, você deverá usar [Update-Module](/powershell/module/powershellget/update-module) para obter a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="07dab-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="07dab-165">Caso tenha usado originalmente o pacote MSI, você deverá baixar e instalar o novo pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="07dab-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="07dab-166">Os cmdlets do PowerShellGet não podem atualizar os módulos que foram instalados por meio de um pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="07dab-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="07dab-167">Os pacotes MSI não atualizam módulos que foram instalados usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="07dab-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="07dab-168">Se você tiver problemas ao atualizar usando o PowershellGet, deverá **reinstalar** em vez de **atualizar**.</span><span class="sxs-lookup"><span data-stu-id="07dab-168">If you have any issues updating using PowershellGet, then you should **reinstall** , rather than **update**.</span></span> <span data-ttu-id="07dab-169">A reinstalação é feita da mesma forma que a instalação, mas você precisa adicionar o parâmetro `-Force`:</span><span class="sxs-lookup"><span data-stu-id="07dab-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="07dab-170">Diferentemente das instalações baseadas em MSI, instalar ou atualizar usando o PowerShellGet não remove as versões mais antigas que possam existir em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="07dab-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="07dab-171">Para remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="07dab-172">Para obter mais informações sobre instalações baseadas em MSI, consulte [Instalar o Azure PowerShell com um MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="07dab-173">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="07dab-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="07dab-174">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07dab-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="07dab-175">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="07dab-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="07dab-176">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="07dab-177">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="07dab-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="07dab-178">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o parâmetro `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="07dab-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 1.8.0
Install-Module -Name Az -RequiredVersion 1.8.0
# Load Az version 1.8.0
Import-Module -Name Az -RequiredVersion 1.8.0
```

## <a name="provide-feedback"></a><span data-ttu-id="07dab-179">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="07dab-179">Provide feedback</span></span>

<span data-ttu-id="07dab-180">Se você encontrar um bug no Azure PowerShell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="07dab-180">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="07dab-181">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="07dab-181">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="07dab-182">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="07dab-182">Next Steps</span></span>

<span data-ttu-id="07dab-183">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-183">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="07dab-184">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="07dab-184">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
