---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179234"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="12283-103">Instale o Azure PowerShell no macOS ou no Linux</span><span class="sxs-lookup"><span data-stu-id="12283-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="12283-104">Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="12283-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="12283-105">Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core.</span><span class="sxs-lookup"><span data-stu-id="12283-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="12283-106">Para trabalhar com essas plataformas, há uma versão do .NET Standard do Azure PowerShell disponível.</span><span class="sxs-lookup"><span data-stu-id="12283-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="12283-107">Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Standard ainda estão na versão beta.</span><span class="sxs-lookup"><span data-stu-id="12283-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="12283-108">O suporte para esses produtos é limitado.</span><span class="sxs-lookup"><span data-stu-id="12283-108">Support for these products is limited.</span></span> <span data-ttu-id="12283-109">Se você tiver problemas ou detectar erros, relate os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="12283-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="12283-110">Problemas do PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="12283-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="12283-111">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="12283-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="12283-112">Instalar PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="12283-112">Install PowerShell Core</span></span>

<span data-ttu-id="12283-113">As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.</span><span class="sxs-lookup"><span data-stu-id="12283-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="12283-114">Instruções detalhadas podem ser encontradas nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="12283-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="12283-115">Instalar o PowerShell Core no macOS</span><span class="sxs-lookup"><span data-stu-id="12283-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="12283-116">Instalar o PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="12283-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="12283-117">Instalar o Azure PowerShell para .NET Standard</span><span class="sxs-lookup"><span data-stu-id="12283-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12283-118">O módulo `AzureRM` detalhado em outros artigos não funciona com o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="12283-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="12283-119">Você deve instalar o módulo `Az` para obter a funcionalidade do Azure PowerShell no PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="12283-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="12283-120">O PowerShell Core é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="12283-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="12283-121">Inicie o PowerShell com o comando:</span><span class="sxs-lookup"><span data-stu-id="12283-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="12283-122">Para instalar o Azure PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="12283-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="12283-123">Se você encontrar um erro de permissões ao tentar instalar o módulo, precisará executar o PowerShell no modo de superusuário para instalar os módulos.</span><span class="sxs-lookup"><span data-stu-id="12283-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="12283-124">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="12283-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="12283-125">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="12283-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="12283-126">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="12283-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="12283-127">Habilitar aliases</span><span class="sxs-lookup"><span data-stu-id="12283-127">Enable aliases</span></span>

<span data-ttu-id="12283-128">Para ter compatibilidade com o módulo `AzureRM`, o novo módulo `Az` é capaz de criar aliases compatíveis com versões anteriores para os cmdlets do `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="12283-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="12283-129">Antes de usar o módulo pela primeira vez, configure esses aliases com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="12283-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="12283-130">Isso configura aliases apenas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="12283-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="12283-131">Verifique a Ajuda do cmdlet para ver outros valores que podem ser fornecidos para `-Scope` a fim de configurar os aliases.</span><span class="sxs-lookup"><span data-stu-id="12283-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="12283-132">Se você encontrar um erro de localização de caminho, verifique se ele existe em seu sistema local.</span><span class="sxs-lookup"><span data-stu-id="12283-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="12283-133">Para o escopo `CurrentUser`, esse erro pode ser resolvido executando o seguinte comando em `bash`:</span><span class="sxs-lookup"><span data-stu-id="12283-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="12283-134">Entrar</span><span class="sxs-lookup"><span data-stu-id="12283-134">Sign in</span></span>

<span data-ttu-id="12283-135">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="12283-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="12283-136">__Não__ é necessário ter privilégios elevados para importar um módulo.</span><span class="sxs-lookup"><span data-stu-id="12283-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="12283-137">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="12283-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="12283-138">A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="12283-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="12283-139">No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="12283-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="12283-140">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="12283-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="12283-141">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="12283-141">Next Steps</span></span>

<span data-ttu-id="12283-142">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="12283-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
