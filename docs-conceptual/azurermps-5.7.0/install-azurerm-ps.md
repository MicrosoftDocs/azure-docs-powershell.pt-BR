---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: bd9cbdd66c1a9a623461ca8b0291ac1cb61f1e54
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177468"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="64da7-103">Instalar o Azure PowerShell no Windows com o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="64da7-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="64da7-104">Esse artigo explica as etapas para instalar os módulos do Azure PowerShell para o PowerShell 5.x do Windows usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="64da7-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="64da7-105">O PowerShellGet e o gerenciamento de módulos são os modos preferidos de instalação do Azure PowerShell, mas se você quiser instalar com o Web Platform Installer ou o pacote do MSI, consulte [Outros métodos de instalação](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="64da7-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="64da7-106">Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64da7-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="64da7-107">Para obter suporte com as implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="64da7-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64da7-108">Não há suporte para o módulo do AzureRM para macOS ou Linux.</span><span class="sxs-lookup"><span data-stu-id="64da7-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="64da7-109">Para usar os cmdlets do Azure PowerShell nessas plataformas, [Instalar o módulo Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="64da7-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="64da7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64da7-110">Requirements</span></span>

<span data-ttu-id="64da7-111">Para instalar o Azure PowerShell, você precisa do PowerShellGet versão 1.1.2.0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="64da7-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="64da7-112">Para verificar se ele está disponível em seu sistema, execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="64da7-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="64da7-113">Você deverá ver algo semelhante à seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="64da7-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="64da7-114">Se for necessário atualizar sua instalação do PowerShellGet, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="64da7-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="64da7-115">Se você não tiver o PowerShellGet instalado, siga as instruções referentes ao seu sistema na tabela abaixo.</span><span class="sxs-lookup"><span data-stu-id="64da7-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="64da7-116">Cenário</span><span class="sxs-lookup"><span data-stu-id="64da7-116">Scenario</span></span>|<span data-ttu-id="64da7-117">Instalar instruções</span><span class="sxs-lookup"><span data-stu-id="64da7-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="64da7-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="64da7-118">Windows 10</span></span><br/><span data-ttu-id="64da7-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64da7-119">Windows Server 2016</span></span>|<span data-ttu-id="64da7-120">Compilado no Windows Management Framework (WMF) 5.0 incluído no SO</span><span class="sxs-lookup"><span data-stu-id="64da7-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="64da7-121">Fazer upgrade para o PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="64da7-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="64da7-122">Instalar a versão mais recente do WMF</span><span class="sxs-lookup"><span data-stu-id="64da7-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="64da7-123">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="64da7-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="64da7-124">Windows com PowerShell 3 ou PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="64da7-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="64da7-125"><il>[Obter os módulos do PackageManagement](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="64da7-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="64da7-126">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="64da7-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="64da7-127">Usar o PowerShellGet requer uma Política de Execução que permite executar scripts.</span><span class="sxs-lookup"><span data-stu-id="64da7-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="64da7-128">Para obter mais informações sobre a Política de Execução do PowerShell, consulte [Sobre as Políticas de Execução](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="64da7-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="64da7-129">O módulo descrito neste documento, AzureRM, usa o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="64da7-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="64da7-130">Isso o torna incompatível com o PowerShell 6.0, que usa o .NET Core.</span><span class="sxs-lookup"><span data-stu-id="64da7-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="64da7-131">Se você estiver usando o PowerShell 6.0, siga as [instruções de instalação para o macOS e o Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="64da7-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="64da7-132">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64da7-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="64da7-133">Você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64da7-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="64da7-134">Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:</span><span class="sxs-lookup"><span data-stu-id="64da7-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="64da7-135">Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.</span><span class="sxs-lookup"><span data-stu-id="64da7-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="64da7-136">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="64da7-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="64da7-137">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="64da7-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="64da7-138">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="64da7-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="64da7-139">O módulo `AzureRM` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64da7-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="64da7-140">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="64da7-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="64da7-141">Entrar</span><span class="sxs-lookup"><span data-stu-id="64da7-141">Sign in</span></span>

<span data-ttu-id="64da7-142">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da7-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="64da7-143">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="64da7-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="64da7-144">A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="64da7-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="64da7-145">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="64da7-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="64da7-146">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64da7-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="64da7-147">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="64da7-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="64da7-148">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="64da7-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="64da7-149">Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="64da7-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="64da7-150">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64da7-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="64da7-151">É possível instalar diversas versões do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64da7-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="64da7-152">Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows que não permite a atualização para o PowerShell 5.0 ou usar o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da7-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="64da7-153">Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` na instalação.</span><span class="sxs-lookup"><span data-stu-id="64da7-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="64da7-154">Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão.</span><span class="sxs-lookup"><span data-stu-id="64da7-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="64da7-155">Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="64da7-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="64da7-156">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="64da7-156">Provide feedback</span></span>

<span data-ttu-id="64da7-157">Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="64da7-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="64da7-158">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="64da7-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="64da7-159">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="64da7-159">Next Steps</span></span>

<span data-ttu-id="64da7-160">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="64da7-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
