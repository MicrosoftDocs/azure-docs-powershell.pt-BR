---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 52fa80542af39a2a768cc54e5b6bd8d0b8246c9f
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399018"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="3b6c0-103">Instalar o Azure PowerShell no Windows com a MSI</span><span class="sxs-lookup"><span data-stu-id="3b6c0-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="3b6c0-104">Este artigo explica como instalar o Azure PowerShell no Windows usando um instalador da MSI.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="3b6c0-105">Use esses métodos de instalação somente se eles forem necessários para o seu sistema.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="3b6c0-106">A forma recomendada de Instalar o Azure PowerShell no Windows é com o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="3b6c0-107">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3b6c0-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="3b6c0-108">O método Web Platform Installer da instalação não está mais disponível para as versões do Azure PowerShell 6.x e superior.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="3b6c0-109">Se você precisar usar o Web Platform Installer, considere usar a MSI ou pode instalar uma versão mais antiga do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="3b6c0-110">Para instalar em ambientes Linux ou macOS, confira [Instalar o Azure PowerShell no macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="3b6c0-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="3b6c0-111">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="3b6c0-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="3b6c0-112">O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="3b6c0-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="3b6c0-113">Se você tiver versões anteriores dos módulos do Azure instaladas como uma MSI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="3b6c0-114">O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="3b6c0-115">Os módulos `AzureRM` e `Azure` são instalados.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="3b6c0-116">Use o módulo `Azure` apenas se estiver trabalhando com o modelo de implantação clássico do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="3b6c0-117">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="3b6c0-118">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="3b6c0-119">A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="3b6c0-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="3b6c0-120">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="3b6c0-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
