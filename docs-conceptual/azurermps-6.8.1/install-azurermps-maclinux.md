---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560109"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="2b5ee-103">Instale o Azure PowerShell no macOS ou no Linux</span><span class="sxs-lookup"><span data-stu-id="2b5ee-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="2b5ee-104">Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="2b5ee-105">Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="2b5ee-106">Para trabalhar com essas plataformas, há uma versão do .NET Standard do Azure PowerShell disponível.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="2b5ee-107">Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="2b5ee-108">O suporte para esses produtos é limitado.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-108">Support for these products is limited.</span></span> <span data-ttu-id="2b5ee-109">Se você tiver problemas ou detectar erros, relate os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="2b5ee-110">Problemas do PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="2b5ee-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="2b5ee-111">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b5ee-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="2b5ee-112">Instalar PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="2b5ee-112">Install PowerShell Core</span></span>

<span data-ttu-id="2b5ee-113">As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="2b5ee-114">Instruções detalhadas podem ser encontradas nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="2b5ee-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="2b5ee-115">Instalar o PowerShell Core no macOS</span><span class="sxs-lookup"><span data-stu-id="2b5ee-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="2b5ee-116">Instalar o PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="2b5ee-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="2b5ee-117">Instalar o Azure PowerShell para .NET Core</span><span class="sxs-lookup"><span data-stu-id="2b5ee-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="2b5ee-118">O PowerShell Core é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="2b5ee-119">A instalação dos módulos no PowerShell requer privilégios elevados, portanto será necessário iniciar sua sessão como superusuário:</span><span class="sxs-lookup"><span data-stu-id="2b5ee-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="2b5ee-120">Para instalar o Azure PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="2b5ee-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="2b5ee-121">O módulo `AzureRM` detalhado em outros artigos não foi compilado para o .NET Core e não funcionará com o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="2b5ee-122">Os módulos `Az` contêm aliases de comando para todos os cmdlets `AzureRM` e, portanto, toda a documentação do `AzureRM` se aplica.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="2b5ee-123">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="2b5ee-124">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="2b5ee-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="2b5ee-125">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="2b5ee-126">Entrar</span><span class="sxs-lookup"><span data-stu-id="2b5ee-126">Sign in</span></span>

<span data-ttu-id="2b5ee-127">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="2b5ee-128">__Não__ é necessário ter privilégios elevados para importar um módulo.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2b5ee-129">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2b5ee-130">A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="2b5ee-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2b5ee-131">No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="2b5ee-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="2b5ee-132">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2b5ee-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2b5ee-133">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="2b5ee-133">Next Steps</span></span>

<span data-ttu-id="2b5ee-134">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="2b5ee-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
