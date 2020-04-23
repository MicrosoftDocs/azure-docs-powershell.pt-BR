---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740245"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="c301d-103">Instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c301d-103">Install Azure PowerShell</span></span>

<span data-ttu-id="c301d-104">Este artigo explica como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c301d-104">This article explains how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="c301d-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="c301d-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="c301d-106">O Azure PowerShell também está disponível no Azure [Cloud Shell](/azure/cloud-shell/overview) e agora é pré-instalado em [imagens do Docker](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c301d-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c301d-107">Requirements</span></span>

<span data-ttu-id="c301d-108">O Azure PowerShell funciona com o PowerShell 5.1 ou superior no Windows ou com o PowerShell Core 6.x e posterior em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="c301d-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="c301d-109">Você deve instalar a [versão mais recente do PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) disponível para seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c301d-109">You should install the [latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) available for your operating system.</span></span> <span data-ttu-id="c301d-110">O Azure PowerShell não tem requisitos adicionais quando executado no PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="c301d-110">Azure PowerShell has no additional requirements when run on PowerShell Core.</span></span>

<span data-ttu-id="c301d-111">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="c301d-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="c301d-112">Para usar o Azure PowerShell no PowerShell 5.1 no Windows:</span><span class="sxs-lookup"><span data-stu-id="c301d-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="c301d-113">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário.</span><span class="sxs-lookup"><span data-stu-id="c301d-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="c301d-114">Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="c301d-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="c301d-115">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="c301d-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="c301d-116">Verifique se tem a versão mais recente do PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c301d-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="c301d-117">Execute `Update-Module PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="c301d-117">Run `Update-Module PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="c301d-118">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c301d-118">Install the Azure PowerShell module</span></span>

<span data-ttu-id="c301d-119">O uso dos cmdlets do PowerShellGet é o método de instalação preferencial.</span><span class="sxs-lookup"><span data-stu-id="c301d-119">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="c301d-120">Esse método funciona da mesma forma nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="c301d-120">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="c301d-121">Execute o seguinte comando em uma sessão do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c301d-121">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="c301d-122">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c301d-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c301d-123">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="c301d-123">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c301d-124">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="c301d-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="c301d-125">O módulo Az é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c301d-125">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c301d-126">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c301d-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

> [!WARNING]
> <span data-ttu-id="c301d-127">Não há compatibilidade na instalação dos módulos AzureRM e Az no PowerShell 5.1 para Windows ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c301d-127">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="c301d-128">Caso você precise manter o AzureRM disponível no sistema, instale o módulo Az para o PowerShell Core 6.x ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c301d-128">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="c301d-129">Primeiro, [instale o PowerShell Core 6.x ou posterior](/powershell/scripting/install/installing-powershell-core-on-windows)</span><span class="sxs-lookup"><span data-stu-id="c301d-129">First, [install PowerShell Core 6.x or later](/powershell/scripting/install/installing-powershell-core-on-windows)</span></span>

<span data-ttu-id="c301d-130">Em seguida, em uma sessão do PowerShell Core, instale o módulo Az somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c301d-130">Then, from a PowerShell Core session, install the Az module for the current user only.</span></span> <span data-ttu-id="c301d-131">Este é o escopo de instalação recomendado.</span><span class="sxs-lookup"><span data-stu-id="c301d-131">This is the recommended installation scope.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="c301d-132">A instalação do módulo para todos os usuários de um sistema requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="c301d-132">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="c301d-133">Inicie a sessão do PowerShell usando **Executar como administrador** no Windows ou use o comando `sudo` no macOS ou Linux:</span><span class="sxs-lookup"><span data-stu-id="c301d-133">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a><span data-ttu-id="c301d-134">Instalar offline</span><span class="sxs-lookup"><span data-stu-id="c301d-134">Install offline</span></span>

<span data-ttu-id="c301d-135">Em alguns ambientes, não é possível se conectar à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c301d-135">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="c301d-136">Nessas situações, você ainda pode instalar offline usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="c301d-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="c301d-137">Baixe os módulos em outro local da sua rede e use-os como uma origem de instalação.</span><span class="sxs-lookup"><span data-stu-id="c301d-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="c301d-138">Isso permite que você armazene módulos do PowerShell em cache em um único servidor ou compartilhamento de arquivo para serem implantados com o PowerShellGet em sistemas desconectados.</span><span class="sxs-lookup"><span data-stu-id="c301d-138">This allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="c301d-139">Saiba como configurar um repositório local e instalar em sistemas desconectados com [Trabalhar com repositórios PowerShellGet locais](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="c301d-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="c301d-140">[Baixe o MSI (Microsoft Windows Installer) do Azure PowerShell](install-az-ps-msi.md) em um computador conectado à rede e, em seguida, copie o instalador para sistemas sem acesso à Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c301d-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="c301d-141">Tenha em mente que o instalador do MSI só funciona para PowerShell 5.1 no Windows.</span><span class="sxs-lookup"><span data-stu-id="c301d-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="c301d-142">Salve o módulo com [Save-Module](/powershell/module/PowershellGet/Save-Module) em um compartilhamento de arquivo ou salve-o em outra fonte e copie-o manualmente para outros computadores:</span><span class="sxs-lookup"><span data-stu-id="c301d-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="c301d-143">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="c301d-143">Troubleshooting</span></span>

<span data-ttu-id="c301d-144">Estes são alguns problemas comuns observados durante a instalação do módulo do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c301d-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="c301d-145">Caso você tenha um problema que não foi listado aqui, [registre um problema no GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c301d-145">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="c301d-146">Conexão de blocos de proxy</span><span class="sxs-lookup"><span data-stu-id="c301d-146">Proxy blocks connection</span></span>

<span data-ttu-id="c301d-147">Se você obtiver erros de `Install-Module` que indicam que a Galeria do PowerShell está inacessível, talvez você esteja protegido por um proxy.</span><span class="sxs-lookup"><span data-stu-id="c301d-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="c301d-148">Sistemas operacionais e ambientes de rede diferentes têm requisitos diferentes para configurar um proxy para todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="c301d-148">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="c301d-149">Entre em contato com o administrador do sistema para obter as configurações de proxy e saber como defini-las para seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="c301d-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="c301d-150">O PowerShell em si pode não ser configurado para usar esse proxy automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c301d-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="c301d-151">Com o PowerShell 5.1 e posterior, configure a sessão do PowerShell para usar um proxy por meio dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="c301d-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="c301d-152">Caso suas credenciais do sistema operacional estejam configuradas corretamente, essa configuração roteará as solicitações do PowerShell por meio do proxy.</span><span class="sxs-lookup"><span data-stu-id="c301d-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="c301d-153">Para manter essa configuração entre as sessões, adicione os comandos ao seu [perfil do PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="c301d-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="c301d-154">Para instalar o pacote, o proxy precisa permitir conexões HTTPS com o seguinte endereço:</span><span class="sxs-lookup"><span data-stu-id="c301d-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="c301d-155">Entrar</span><span class="sxs-lookup"><span data-stu-id="c301d-155">Sign in</span></span>

<span data-ttu-id="c301d-156">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="c301d-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="c301d-157">Se você desabilitou o carregamento automático do módulo, importe manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="c301d-157">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="c301d-158">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="c301d-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="c301d-159">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="c301d-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c301d-160">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-160">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="c301d-161">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c301d-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="c301d-162">Para atualizar qualquer módulo do PowerShell, você deve usar o mesmo método usado para instalar o módulo.</span><span class="sxs-lookup"><span data-stu-id="c301d-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="c301d-163">Por exemplo, caso tenha usado `Install-Module` originalmente, você deverá usar [Update-Module](/powershell/module/powershellget/update-module) para obter a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="c301d-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="c301d-164">Caso tenha usado originalmente o pacote MSI, você deverá baixar e instalar o novo pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="c301d-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="c301d-165">Os cmdlets do PowerShellGet não podem atualizar os módulos que foram instalados por meio de um pacote MSI.</span><span class="sxs-lookup"><span data-stu-id="c301d-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="c301d-166">Os pacotes MSI não atualizam módulos que foram instalados usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c301d-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="c301d-167">Se você tiver problemas ao atualizar usando o PowershellGet, deverá **reinstalar**, em vez de **atualizar**.</span><span class="sxs-lookup"><span data-stu-id="c301d-167">If you have any issues updating using PowershellGet then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="c301d-168">A reinstalação é feita da mesma forma que a instalação, mas você precisa adicionar o parâmetro `-Force`:</span><span class="sxs-lookup"><span data-stu-id="c301d-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="c301d-169">Diferentemente das instalações baseadas em MSI, instalar ou atualizar usando o PowerShellGet não remove as versões mais antigas que possam existir em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="c301d-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="c301d-170">Para remover as versões antigas do Azure PowerShell do sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="c301d-171">Para obter mais informações sobre instalações baseadas em MSI, consulte [Instalar o Azure PowerShell com um MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="c301d-172">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c301d-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="c301d-173">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c301d-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="c301d-174">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="c301d-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="c301d-175">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="c301d-176">Se você tiver mais de uma versão do módulo instalada, o carregamento automático do módulo e o `Import-Module` carregarão a versão mais recente por padrão.</span><span class="sxs-lookup"><span data-stu-id="c301d-176">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="c301d-177">Você pode instalar ou carregar uma versão específica do módulo `Az` usando o parâmetro `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="c301d-177">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="c301d-178">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="c301d-178">Provide feedback</span></span>

<span data-ttu-id="c301d-179">Se você encontrar um bug no Azure PowerShell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c301d-179">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="c301d-180">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="c301d-180">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c301d-181">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c301d-181">Next Steps</span></span>

<span data-ttu-id="c301d-182">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-182">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="c301d-183">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="c301d-183">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>