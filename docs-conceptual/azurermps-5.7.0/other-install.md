---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell sem o PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7148188603e84efbcd784264de4c78819edf6833
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243711"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="43984-103">Instalar o Azure PowerShell no Windows com a MSI ou com o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="43984-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="43984-104">Este artigo explica como instalar o Azure PowerShell no Windows usando uma MSI ou o Web Platform Installer (WebPI).</span><span class="sxs-lookup"><span data-stu-id="43984-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>
<span data-ttu-id="43984-105">Use esses métodos de instalação somente se eles forem necessários para o seu sistema.</span><span class="sxs-lookup"><span data-stu-id="43984-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="43984-106">A forma recomendada de Instalar o Azure PowerShell no Windows é com o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="43984-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="43984-107">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="43984-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="43984-108">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="43984-108">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="43984-109">O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="43984-109">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="43984-110">Se você tiver versões anteriores dos módulos do Azure instaladas como uma MSI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="43984-110">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="43984-111">O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="43984-111">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="43984-112">Os módulos `AzureRM` e `Azure` são instalados.</span><span class="sxs-lookup"><span data-stu-id="43984-112">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="43984-113">Use o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="43984-113">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="43984-114">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="43984-114">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="43984-115">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="43984-115">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="43984-116">A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="43984-116">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="43984-117">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="43984-117">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="43984-118">Instalar ou atualizar no Windows usando o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="43984-118">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="43984-119">Baixe o [pacote WebPI do Azure PowerShell](https://aka.ms/webpi-azps) e inicie a instalação.</span><span class="sxs-lookup"><span data-stu-id="43984-119">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="43984-120">Se você tiver versões anteriores dos módulos do Azure instaladas de uma MSI ou com o WebPI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="43984-120">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="43984-121">Os módulos são instalados no `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="43984-121">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="43984-122">Os módulos `AzureRM` e `Azure` são instalados.</span><span class="sxs-lookup"><span data-stu-id="43984-122">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="43984-123">Use o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="43984-123">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="43984-124">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="43984-124">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="43984-125">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="43984-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="43984-126">A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="43984-126">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="43984-127">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="43984-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
