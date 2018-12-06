---
title: Instalar “Az” do Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet no Windows, macOS e Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826775"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="96014-103">Instalar módulo “Az” do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="96014-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="96014-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="96014-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="96014-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="96014-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="96014-106">A versão de visualização do Az, não há suporte para nenhum outro método de instalação.</span><span class="sxs-lookup"><span data-stu-id="96014-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="96014-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96014-107">Requirements</span></span>

<span data-ttu-id="96014-108">O Azure PowerShell funciona com o PowerShell 5.x no Windows ou o PowerShell 6.x em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="96014-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="96014-109">Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="96014-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="96014-110">Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="96014-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="96014-111">As informações de instalação para sua plataforma estão vinculadas a partir dessa página.</span><span class="sxs-lookup"><span data-stu-id="96014-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="96014-112">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="96014-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="96014-113">É possível ter ambos os módulos `AzureRM` e `Az` instalados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="96014-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="96014-114">Caso tenha ambos os módulos instalados, __não habilite aliases__.</span><span class="sxs-lookup"><span data-stu-id="96014-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="96014-115">Habilitar aliases causa conflitos entre os cmdlets `AzureRM` e os aliases de comando `Az`, podendo levar a comportamentos inesperados.</span><span class="sxs-lookup"><span data-stu-id="96014-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="96014-116">Antes de instalar o módulo `Az`, recomenda-se desinstalar o `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="96014-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="96014-117">É possível desinstalar o `AzureRM` ou habilitar aliases a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="96014-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="96014-118">Para obter instruções de desinstalação, consulte [Desinstalar o módulo do Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="96014-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="96014-119">Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96014-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="96014-120">Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):</span><span class="sxs-lookup"><span data-stu-id="96014-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="96014-121">Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="96014-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="96014-122">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="96014-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="96014-123">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="96014-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="96014-124">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="96014-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="96014-125">O módulo `Az` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96014-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="96014-126">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="96014-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="96014-127">Entrar</span><span class="sxs-lookup"><span data-stu-id="96014-127">Sign in</span></span>

<span data-ttu-id="96014-128">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="96014-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="96014-129">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="96014-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="96014-130">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="96014-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="96014-131">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="96014-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="96014-132">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="96014-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="96014-133">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="96014-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="96014-134">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="96014-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="96014-135">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="96014-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="96014-136">Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="96014-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="96014-137">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="96014-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="96014-138">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96014-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="96014-139">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="96014-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="96014-140">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="96014-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="96014-141">Você pode carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion` com `Install-Module` e `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="96014-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="96014-142">Se tiver mais de uma versão do módulo instalada, a versão mais recente será carregada por padrão.</span><span class="sxs-lookup"><span data-stu-id="96014-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="96014-143">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="96014-143">Provide feedback</span></span>

<span data-ttu-id="96014-144">Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="96014-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="96014-145">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="96014-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="96014-146">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="96014-146">Next Steps</span></span>

<span data-ttu-id="96014-147">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="96014-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
