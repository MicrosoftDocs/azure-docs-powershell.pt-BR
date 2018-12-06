---
title: Instalar o Azure PowerShell no Windows com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 616a9e14c3944e3151676d89b8a22e35d8f9d406
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828409"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="79c56-103">Instalar o Azure PowerShell no Windows com o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="79c56-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="79c56-104">Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="79c56-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="79c56-105">O PowerShellGet e o gerenciamento de módulos são os modos preferidos de instalação do Azure PowerShell, mas se você quiser instalar com o Web Platform Installer ou o pacote do MSI, consulte [Outros métodos de instalação](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="79c56-106">Para obter instruções de instalação do Azure PowerShell em outras plataformas, consulte [Instalar e configurar o Azure PowerShell no macOS e no Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="79c56-107">Não há suporte para o modelo de implantação clássico do Azure desta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79c56-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="79c56-108">Para obter suporte com as implantações clássicas, siga as instruções em [Instalar o módulo de Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="79c56-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a><span data-ttu-id="79c56-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c56-109">Requirements</span></span>

<span data-ttu-id="79c56-110">Começando com o Azure PowerShell versão 6.0, o Azure PowerShell requer o PowerShell versão 5.0.</span><span class="sxs-lookup"><span data-stu-id="79c56-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="79c56-111">Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="79c56-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="79c56-112">Se você tiver uma versão desatualizada, consulte [Atualizar o Windows PowerShell existente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="79c56-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79c56-113">O módulo descrito neste documento, AzureRM, usa o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="79c56-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="79c56-114">Isso o torna incompatível com o PowerShell 6.0, que usa o .NET Core.</span><span class="sxs-lookup"><span data-stu-id="79c56-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="79c56-115">Se você estiver usando o PowerShell 6.0, siga as [instruções de instalação para o macOS e o Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="79c56-116">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="79c56-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="79c56-117">Você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79c56-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="79c56-118">Para instalar o Azure PowerShell, execute o comando a seguir em uma sessão elevada:</span><span class="sxs-lookup"><span data-stu-id="79c56-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="79c56-119">Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.</span><span class="sxs-lookup"><span data-stu-id="79c56-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="79c56-120">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="79c56-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="79c56-121">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="79c56-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="79c56-122">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="79c56-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="79c56-123">O módulo `AzureRM` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79c56-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="79c56-124">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="79c56-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="79c56-125">Entrar</span><span class="sxs-lookup"><span data-stu-id="79c56-125">Sign in</span></span>

<span data-ttu-id="79c56-126">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="79c56-126">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="79c56-127">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="79c56-127">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="79c56-128">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="79c56-128">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="79c56-129">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="79c56-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="79c56-130">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-130">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="79c56-131">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="79c56-131">Update the Azure PowerShell module</span></span>

<span data-ttu-id="79c56-132">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="79c56-132">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="79c56-133">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="79c56-133">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="79c56-134">Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-134">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="79c56-135">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="79c56-135">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="79c56-136">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79c56-136">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="79c56-137">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="79c56-137">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

<span data-ttu-id="79c56-138">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="79c56-138">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="79c56-139">Talvez seja necessário mais de uma versão se você trabalhar com recursos locais do Azure Stack, executar uma versão anterior do Windows ou usar o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="79c56-139">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="79c56-140">Para instalar uma versão mais antiga, forneça o argumento `-RequiredVersion` na instalação.</span><span class="sxs-lookup"><span data-stu-id="79c56-140">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="79c56-141">Ao carregar o módulo do Azure PowerShell, a versão mais recente é carregada por padrão.</span><span class="sxs-lookup"><span data-stu-id="79c56-141">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="79c56-142">Para carregar uma versão diferente, forneça o argumento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="79c56-142">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="79c56-143">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="79c56-143">Provide feedback</span></span>

<span data-ttu-id="79c56-144">Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="79c56-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="79c56-145">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="79c56-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="79c56-146">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="79c56-146">Next Steps</span></span>

<span data-ttu-id="79c56-147">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="79c56-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
