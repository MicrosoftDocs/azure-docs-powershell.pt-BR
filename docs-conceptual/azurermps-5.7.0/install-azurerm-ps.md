---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: dc5a1c59d23e37acf11aa7831ddc6e1edbd7f73e
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091411"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="68c35-103">Instalar o Azure PowerShell no Windows com o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="68c35-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="68c35-104">Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="68c35-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="68c35-105">O PowerShellGet e o gerenciamento de módulo são os modos preferenciais de instalação do Azure PowerShell, mas se você preferir instalar com o Web Platform Installer ou com o pacote do MSI, confira [Outros métodos de instalação](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="68c35-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="68c35-106">Para obter instruções de instalação do Azure PowerShell em outras plataformas, confira [Instalar e configurar o Azure PowerShell no macOS e no Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="68c35-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="68c35-107">Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68c35-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="68c35-108">Para obter suporte com implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="68c35-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="68c35-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c35-109">Requirements</span></span>

<span data-ttu-id="68c35-110">Para instalar o Azure PowerShell, você precisa do PowerShellGet versão 1.1.2.0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="68c35-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="68c35-111">Para verificar se ele está disponível em seu sistema, execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="68c35-111">To check if it is available on your system, run the following command:</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="68c35-112">Você deverá ver algo semelhante à seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="68c35-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="68c35-113">Se for necessário atualizar sua instalação do PowerShellGet, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="68c35-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="68c35-114">Se você não tiver o PowerShellGet instalado, siga as instruções referentes ao seu sistema na tabela abaixo.</span><span class="sxs-lookup"><span data-stu-id="68c35-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="68c35-115">Cenário</span><span class="sxs-lookup"><span data-stu-id="68c35-115">Scenario</span></span>|<span data-ttu-id="68c35-116">Instalar instruções</span><span class="sxs-lookup"><span data-stu-id="68c35-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="68c35-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="68c35-117">Windows 10</span></span><br/><span data-ttu-id="68c35-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68c35-118">Windows Server 2016</span></span>|<span data-ttu-id="68c35-119">Compilado no Windows Management Framework (WMF) 5.0 incluído no SO</span><span class="sxs-lookup"><span data-stu-id="68c35-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="68c35-120">Fazer upgrade para o PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="68c35-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="68c35-121">Instalar a versão mais recente do WMF</span><span class="sxs-lookup"><span data-stu-id="68c35-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="68c35-122">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="68c35-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="68c35-123">Windows com PowerShell 3 ou PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="68c35-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="68c35-124"><il>[Obter os módulos do PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="68c35-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="68c35-125">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="68c35-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="68c35-126">Usar o PowerShellGet requer uma Política de Execução que permite executar scripts.</span><span class="sxs-lookup"><span data-stu-id="68c35-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="68c35-127">Para obter mais informações sobre a Política de Execução do PowerShell, consulte [Sobre as Políticas de Execução](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="68c35-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="68c35-128">Instalar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="68c35-128">Install the Azure PowerShell module</span></span>

<span data-ttu-id="68c35-129">Você precisa de privilégios elevados para instalar módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68c35-129">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="68c35-130">Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:</span><span class="sxs-lookup"><span data-stu-id="68c35-130">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="68c35-131">Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.</span><span class="sxs-lookup"><span data-stu-id="68c35-131">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="68c35-132">Por padrão, a Galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="68c35-132">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="68c35-133">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="68c35-133">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="68c35-134">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="68c35-134">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="68c35-135">O módulo `AzureRM` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68c35-135">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="68c35-136">A instalação dele baixa todos os módulos do Azure Resource Manager disponíveis e disponibiliza seus cmdlets para uso.</span><span class="sxs-lookup"><span data-stu-id="68c35-136">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="68c35-137">Entrar</span><span class="sxs-lookup"><span data-stu-id="68c35-137">Sign in</span></span>

<span data-ttu-id="68c35-138">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c35-138">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="68c35-139">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="68c35-139">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="68c35-140">A importação automática do módulo `AzureRM` exige a configuração de um perfil de PowerShell. Saiba mais sobre isso em [Sobre perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="68c35-140">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="68c35-141">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Persistir as credenciais do usuário entre sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="68c35-141">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="68c35-142">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="68c35-142">Update the Azure PowerShell module</span></span>

<span data-ttu-id="68c35-143">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="68c35-143">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="68c35-144">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="68c35-144">This command does __not__ uninstall earlier versions.</span></span>

```powershell
Update-Module -Name AzureRM
```

<span data-ttu-id="68c35-145">Se você quiser remover versões mais antigas do Azure PowerShell de seu sistema, confira [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="68c35-145">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="68c35-146">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="68c35-146">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="68c35-147">É possível instalar várias versões do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68c35-147">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="68c35-148">Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows que não permite a atualização para o PowerShell 5.0 ou usar o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c35-148">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="68c35-149">Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="68c35-149">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="68c35-150">Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão.</span><span class="sxs-lookup"><span data-stu-id="68c35-150">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="68c35-151">Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="68c35-151">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="68c35-152">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="68c35-152">Provide feedback</span></span>

<span data-ttu-id="68c35-153">Se você encontrar um bug ao usar o Azure Powershell, [registre um problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="68c35-153">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="68c35-154">Para fornecer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="68c35-154">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="68c35-155">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="68c35-155">Next Steps</span></span>

<span data-ttu-id="68c35-156">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="68c35-156">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>