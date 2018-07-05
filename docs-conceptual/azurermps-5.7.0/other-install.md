---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell sem o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f6c52b413aa2981dc24c7e60fe832e37dcbc8baa
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091445"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="92733-103">Instalar o Azure PowerShell no Windows com a MSI ou com o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="92733-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="92733-104">Este artigo explica como instalar o Azure PowerShell no Windows usando uma MSI ou o Web Platform Installer (WebPI).</span><span class="sxs-lookup"><span data-stu-id="92733-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="92733-105">Use esses métodos de instalação somente se eles forem necessários para o seu sistema.</span><span class="sxs-lookup"><span data-stu-id="92733-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="92733-106">A forma recomendada de Instalar o Azure PowerShell no Windows é com o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="92733-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="92733-107">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="92733-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="92733-108">Para executar o Azure PowerShell em um contêiner do Docker, confira [Executar o Azure PowerShell no Docker](azurerm-ps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="92733-108">To run Azure PowerShell in a Docker container, see [Run Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span></span>

<span data-ttu-id="92733-109">Para instalar em ambientes Linux ou macOS, confira [Instalar o Azure PowerShell no macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="92733-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="92733-110">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="92733-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="92733-111">O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="92733-111">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="92733-112">Se você tiver versões anteriores dos módulos do Azure instaladas como uma MSI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92733-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="92733-113">O pacote de MSI instala os módulos no `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="92733-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="92733-114">Os módulos `AzureRM` e `Azure` são instalados.</span><span class="sxs-lookup"><span data-stu-id="92733-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="92733-115">Uso o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássica do Azure.</span><span class="sxs-lookup"><span data-stu-id="92733-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="92733-116">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="92733-116">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="92733-117">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="92733-117">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="92733-118">A importação automática do módulo `AzureRM` exige a configuração de um perfil de PowerShell. Saiba mais sobre isso em [Sobre perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="92733-118">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="92733-119">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Persistir as credenciais do usuário entre sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="92733-119">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="92733-120">Instalar ou atualizar no Windows usando o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="92733-120">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="92733-121">Baixe o [pacote WebPI do Azure PowerShell](http://aka.ms/webpi-azps) e inicie a instalação.</span><span class="sxs-lookup"><span data-stu-id="92733-121">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="92733-122">Se você tiver versões anteriores dos módulos do Azure instaladas de uma MSI ou com o WebPI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92733-122">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="92733-123">Os módulos são instalados no `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="92733-123">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="92733-124">Os módulos `AzureRM` e `Azure` são instalados.</span><span class="sxs-lookup"><span data-stu-id="92733-124">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="92733-125">Uso o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássica do Azure.</span><span class="sxs-lookup"><span data-stu-id="92733-125">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="92733-126">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="92733-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="92733-127">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="92733-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="92733-128">A importação automática do módulo `AzureRM` exige a configuração de um perfil de PowerShell. Saiba mais sobre isso em [Sobre perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="92733-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="92733-129">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Persistir as credenciais do usuário entre sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="92733-129">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>