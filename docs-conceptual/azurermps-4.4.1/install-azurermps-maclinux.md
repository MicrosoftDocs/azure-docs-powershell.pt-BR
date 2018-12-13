---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217517"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="95980-103">Instale o Azure PowerShell no macOS ou no Linux</span><span class="sxs-lookup"><span data-stu-id="95980-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="95980-104">Para as plataformas não Windows, é possível executar o Azure PowerShell no PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="95980-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="95980-105">Essa versão do PowerShell foi criada para usar em qualquer plataforma que dê suporte ao .NET Core.</span><span class="sxs-lookup"><span data-stu-id="95980-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="95980-106">Para trabalhar com essas plataformas, há uma versão especial do .NET Core do Azure PowerShell disponível.</span><span class="sxs-lookup"><span data-stu-id="95980-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="95980-107">Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.</span><span class="sxs-lookup"><span data-stu-id="95980-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="95980-108">O suporte para esses produtos é limitado.</span><span class="sxs-lookup"><span data-stu-id="95980-108">Support for these products is limited.</span></span> <span data-ttu-id="95980-109">Se você tiver problemas ou detectar erros, relate os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="95980-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="95980-110">Problemas do PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="95980-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="95980-111">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="95980-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="95980-112">Instalar PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="95980-112">Install PowerShell Core</span></span>

<span data-ttu-id="95980-113">As instruções de instalação do PowerShell Core são diferentes para o macOS e a maioria das distribuições do Linux.</span><span class="sxs-lookup"><span data-stu-id="95980-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="95980-114">Instruções detalhadas podem ser encontradas nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="95980-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="95980-115">Instalar o PowerShell Core no macOS</span><span class="sxs-lookup"><span data-stu-id="95980-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="95980-116">Instalar o PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="95980-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="95980-117">Instalar o Azure PowerShell para .NET Core</span><span class="sxs-lookup"><span data-stu-id="95980-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="95980-118">O PowerShell Core é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="95980-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="95980-119">A instalação dos módulos no PowerShell requer privilégios elevados, portanto será necessário iniciar sua sessão como superusuário:</span><span class="sxs-lookup"><span data-stu-id="95980-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="95980-120">Para instalar o Azure PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="95980-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="95980-121">O módulo `AzureRM` detalhado em outros artigos não foi compilado para o .NET Core e não funcionará com o PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="95980-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="95980-122">`AzureRM` e `AzureRM.NetCore` usam os mesmos nomes de cmdlet, portanto a única diferença é o nome do módulo de rollup e para qual versão do .NET foram criados.</span><span class="sxs-lookup"><span data-stu-id="95980-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="95980-123">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="95980-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="95980-124">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="95980-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="95980-125">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="95980-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="95980-126">Entrar</span><span class="sxs-lookup"><span data-stu-id="95980-126">Sign in</span></span>

<span data-ttu-id="95980-127">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `AzureRM.Netcore` em sua sessão do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="95980-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="95980-128">__Não__ é necessário ter privilégios elevados para importar um módulo.</span><span class="sxs-lookup"><span data-stu-id="95980-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="95980-129">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="95980-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="95980-130">A importação automática do módulo `AzureRM` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="95980-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="95980-131">No macOS e no Linux, trabalhe com seu perfil usando a variável de ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="95980-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="95980-132">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="95980-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="95980-133">Cmdlets disponíveis</span><span class="sxs-lookup"><span data-stu-id="95980-133">Available cmdlets</span></span>

<span data-ttu-id="95980-134">Os módulos do Azure PowerShell para .NET Core ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="95980-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="95980-135">Esses módulos não fornecem o conjunto completo de cmdlets que estão disponíveis para a versão do Windows dos módulos.</span><span class="sxs-lookup"><span data-stu-id="95980-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="95980-136">As funções a seguir são implementadas em módulos AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="95980-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="95980-137">Gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="95980-137">Account management</span></span>
  * <span data-ttu-id="95980-138">Entrar com a conta da Microsoft, conta Organizacional ou Entidade de Serviço por meio do Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="95980-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="95980-139">Salvar credenciais para o disco com Save-AzureRmContext e carregar as credenciais salvas usando Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="95980-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="95980-140">Ambiente</span><span class="sxs-lookup"><span data-stu-id="95980-140">Environment</span></span>
  * <span data-ttu-id="95980-141">Obter os diferentes ambientes do Microsoft Azure prontos para uso</span><span class="sxs-lookup"><span data-stu-id="95980-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="95980-142">Adicionar/definir/remover ambientes personalizados (como seus ambientes do Azure Stack ou do Pacote do Microsoft Azure)</span><span class="sxs-lookup"><span data-stu-id="95980-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="95980-143">Cmdlets de plano de gerenciamento para os Serviços do Azure usando as interfaces do Resource Manager e do Gerenciamento de Serviços.</span><span class="sxs-lookup"><span data-stu-id="95980-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="95980-144">Máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="95980-144">Virtual Machine</span></span>
  * <span data-ttu-id="95980-145">Serviço de Aplicativo (Sites)</span><span class="sxs-lookup"><span data-stu-id="95980-145">App Service (Websites)</span></span>
  * <span data-ttu-id="95980-146">Banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="95980-146">SQL Database</span></span>
  * <span data-ttu-id="95980-147">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="95980-147">Storage</span></span>
  * <span data-ttu-id="95980-148">Rede</span><span class="sxs-lookup"><span data-stu-id="95980-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="95980-149">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="95980-149">Next Steps</span></span>

<span data-ttu-id="95980-150">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="95980-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
