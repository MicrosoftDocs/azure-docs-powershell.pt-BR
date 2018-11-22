---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259406"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="d2369-103">Instale o Azure PowerShell no macOS ou no Linux</span><span class="sxs-lookup"><span data-stu-id="d2369-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="d2369-104">Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="d2369-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="d2369-105">Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d2369-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="d2369-106">Para trabalhar com essas plataformas, há uma versão do .NET Standard do Azure PowerShell disponível.</span><span class="sxs-lookup"><span data-stu-id="d2369-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="d2369-107">Neste momento, o Azure PowerShell para o .NET Standard ainda está na versão beta.</span><span class="sxs-lookup"><span data-stu-id="d2369-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="d2369-108">Se você tiver problemas ou detectar erros, relate os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="d2369-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="d2369-109">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2369-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="d2369-110">Instalar PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="d2369-110">Install PowerShell Core</span></span>

<span data-ttu-id="d2369-111">As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.</span><span class="sxs-lookup"><span data-stu-id="d2369-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="d2369-112">Instruções detalhadas podem ser encontradas nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="d2369-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="d2369-113">Instalar o PowerShell Core no macOS</span><span class="sxs-lookup"><span data-stu-id="d2369-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="d2369-114">Instalar o PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="d2369-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="d2369-115">Instalar o Azure PowerShell para .NET Standard</span><span class="sxs-lookup"><span data-stu-id="d2369-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2369-116">O módulo `AzureRM` detalhado em outros artigos não funciona com o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="d2369-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="d2369-117">Você deve instalar o módulo `Az` para obter a funcionalidade do Azure PowerShell no PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="d2369-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="d2369-118">O PowerShell Core é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="d2369-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="d2369-119">Inicie o PowerShell com o comando:</span><span class="sxs-lookup"><span data-stu-id="d2369-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="d2369-120">Para instalar o Azure PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d2369-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="d2369-121">Se você encontrar um erro de permissões ao tentar instalar o módulo, precisará executar o PowerShell no modo de superusuário para instalar os módulos.</span><span class="sxs-lookup"><span data-stu-id="d2369-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="d2369-122">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d2369-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="d2369-123">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="d2369-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="d2369-124">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="d2369-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="d2369-125">Habilitar aliases</span><span class="sxs-lookup"><span data-stu-id="d2369-125">Enable aliases</span></span>

<span data-ttu-id="d2369-126">Para ter compatibilidade com o módulo `AzureRM`, o novo módulo `Az` é capaz de criar aliases compatíveis com versões anteriores para os cmdlets do `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="d2369-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="d2369-127">Antes de usar o módulo pela primeira vez, configure esses aliases com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d2369-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="d2369-128">Isso configura aliases apenas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d2369-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="d2369-129">Verifique a Ajuda do cmdlet para ver outros valores que podem ser fornecidos para `-Scope` a fim de configurar os aliases.</span><span class="sxs-lookup"><span data-stu-id="d2369-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="d2369-130">Se você encontrar um erro de localização de caminho, verifique se ele existe em seu sistema local.</span><span class="sxs-lookup"><span data-stu-id="d2369-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="d2369-131">Para o escopo `CurrentUser`, esse erro pode ser resolvido executando o seguinte comando em `bash`:</span><span class="sxs-lookup"><span data-stu-id="d2369-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="d2369-132">Entrar</span><span class="sxs-lookup"><span data-stu-id="d2369-132">Sign in</span></span>

<span data-ttu-id="d2369-133">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2369-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="d2369-134">__Não__ é necessário ter privilégios elevados para importar um módulo.</span><span class="sxs-lookup"><span data-stu-id="d2369-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="d2369-135">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="d2369-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d2369-136">A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d2369-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="d2369-137">No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="d2369-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="d2369-138">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d2369-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d2369-139">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d2369-139">Next Steps</span></span>

<span data-ttu-id="d2369-140">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d2369-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
