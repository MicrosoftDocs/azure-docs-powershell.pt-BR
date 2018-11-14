---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276023"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="aad7e-103">Instalar o Azure PowerShell com o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="aad7e-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="aad7e-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="aad7e-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="aad7e-105">A versão de visualização do Az, não há suporte para nenhum outro método de instalação.</span><span class="sxs-lookup"><span data-stu-id="aad7e-105">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="aad7e-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aad7e-106">Requirements</span></span>

<span data-ttu-id="aad7e-107">O Azure PowerShell funciona com o PowerShell 5.x no Windows ou o PowerShell 6.x em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="aad7e-107">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="aad7e-108">Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="aad7e-108">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="aad7e-109">Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="aad7e-109">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="aad7e-110">As informações de instalação para sua plataforma estão vinculadas a partir dessa página.</span><span class="sxs-lookup"><span data-stu-id="aad7e-110">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="aad7e-111">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aad7e-111">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="aad7e-112">Você não deve ter ambos os módulos `AzureRM` e `Az` instalados em um sistema ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="aad7e-112">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="aad7e-113">Para instalar o módulo `Az`, `AzureRM` deve ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="aad7e-113">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="aad7e-114">Para obter instruções sobre como fazer isso, confira [Desinstalar o módulo Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="aad7e-114">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="aad7e-115">Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aad7e-115">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="aad7e-116">Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):</span><span class="sxs-lookup"><span data-stu-id="aad7e-116">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="aad7e-117">Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="aad7e-117">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="aad7e-118">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="aad7e-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="aad7e-119">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="aad7e-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="aad7e-120">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="aad7e-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="aad7e-121">O módulo `Az` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aad7e-121">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="aad7e-122">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="aad7e-122">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="aad7e-123">Entrar</span><span class="sxs-lookup"><span data-stu-id="aad7e-123">Sign in</span></span>

<span data-ttu-id="aad7e-124">Para começar a trabalhar com o Azure PowerShell, você precisa carregar `Az` em sua sessão atual do PowerShell com o cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), depois, entrar com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="aad7e-124">To start working with Azure PowerShell, you need to load `Az` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

<span data-ttu-id="aad7e-125">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="aad7e-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="aad7e-126">A importação automática do módulo `Az` requer a configuração de um perfil do PowerShell. Saiba mais sobre isso em [Sobre Perfis](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="aad7e-126">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="aad7e-127">Para aprender a manter sua entrada no Azure entre as sessões, consulte [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="aad7e-127">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="aad7e-128">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aad7e-128">Update the Azure PowerShell module</span></span>

<span data-ttu-id="aad7e-129">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="aad7e-129">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="aad7e-130">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="aad7e-130">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="aad7e-131">Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="aad7e-131">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="aad7e-132">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aad7e-132">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="aad7e-133">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aad7e-133">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="aad7e-134">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="aad7e-134">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="aad7e-135">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="aad7e-135">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="aad7e-136">Você pode carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion` com `Install-Module` ou `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="aad7e-136">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` or `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="aad7e-137">Se você tiver mais de uma versão do módulo instalado, a versão mais recente é carregada, por padrão, durante a importação.</span><span class="sxs-lookup"><span data-stu-id="aad7e-137">If you have more than one version of the module installed, the latest version is loaded by default when importing.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="aad7e-138">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="aad7e-138">Provide feedback</span></span>

<span data-ttu-id="aad7e-139">Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="aad7e-139">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="aad7e-140">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="aad7e-140">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="aad7e-141">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="aad7e-141">Next Steps</span></span>

<span data-ttu-id="aad7e-142">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="aad7e-142">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>