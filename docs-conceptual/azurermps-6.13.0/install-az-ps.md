---
title: Instalar “Az” do Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet no Windows, macOS e Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 32e96c6459c9db0c4b9eda0cc170c85ba99a22ca
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259398"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="58263-103">Instalar módulo “Az” do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58263-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="58263-104">Este artigo informa como instalar os módulos do Azure PowerShell usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="58263-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="58263-105">Essas instruções funcionam nas plataformas Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="58263-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="58263-106">A versão de visualização do Az, não há suporte para nenhum outro método de instalação.</span><span class="sxs-lookup"><span data-stu-id="58263-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="58263-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58263-107">Requirements</span></span>

<span data-ttu-id="58263-108">O Azure PowerShell funciona com o PowerShell 5.x no Windows ou o PowerShell 6.x em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="58263-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="58263-109">Para verificar a versão do PowerShell em execução no computador, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58263-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="58263-110">Se você tiver uma versão desatualizada ou precisar instalar o PowerShell, confira [Instalando várias versões do PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="58263-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="58263-111">As informações de instalação para sua plataforma estão vinculadas a partir dessa página.</span><span class="sxs-lookup"><span data-stu-id="58263-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="58263-112">Instalar módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58263-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="58263-113">Você não deve ter ambos os módulos `AzureRM` e `Az` instalados em um sistema ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="58263-113">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="58263-114">Para instalar o módulo `Az`, `AzureRM` deve ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="58263-114">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="58263-115">Para obter instruções sobre como fazer isso, confira [Desinstalar o módulo Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="58263-115">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="58263-116">Para instalar os módulos em um escopo global, você precisa de privilégios elevados para instalar os módulos da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58263-116">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="58263-117">Para instalar o Azure PowerShell, execute o seguinte comando em uma sessão elevada ("Executar como Administrador" no Windows ou com privilégios de superusuário no macOS ou no Linux):</span><span class="sxs-lookup"><span data-stu-id="58263-117">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="58263-118">Se você não tiver acesso aos privilégios de administrador, você pode instalar para o usuário atual adicionando o argumento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="58263-118">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="58263-119">Por padrão, a galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="58263-119">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="58263-120">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="58263-120">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="58263-121">Responda `Yes` ou `Yes to All` para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="58263-121">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="58263-122">O módulo `Az` é um módulo de rollup para os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58263-122">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="58263-123">A instalação dele baixa todos os módulos disponíveis do Azure Resource Manager e possibilita usar seus cmdlets.</span><span class="sxs-lookup"><span data-stu-id="58263-123">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="58263-124">Entrar</span><span class="sxs-lookup"><span data-stu-id="58263-124">Sign in</span></span>

<span data-ttu-id="58263-125">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="58263-125">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="58263-126">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="58263-126">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="58263-127">Por causa da maneira como o módulo está estruturado, isso pode levar alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="58263-127">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="58263-128">Será necessário repetir essas etapas para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="58263-128">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="58263-129">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="58263-129">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="58263-130">Atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58263-130">Update the Azure PowerShell module</span></span>

<span data-ttu-id="58263-131">Você pode atualizar sua instalação do Azure PowerShell executando [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="58263-131">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="58263-132">Esse comando __não__ desinstala as versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="58263-132">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="58263-133">Se quiser remover as versões mais antigas do Azure PowerShell do sistema, consulte [Desinstalar o módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="58263-133">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="58263-134">Usar várias versões do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="58263-134">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="58263-135">É possível instalar mais de uma versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58263-135">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="58263-136">Para verificar se você tem diversas versões do Azure PowerShell instaladas, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58263-136">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="58263-137">Para remover uma versão do Azure PowerShell, confira [Desinstalar módulo do Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="58263-137">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="58263-138">Você pode carregar uma versão específica do módulo `Az` usando o argumento `-RequiredVersion` com `Install-Module` e `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="58263-138">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="58263-139">Se tiver mais de uma versão do módulo instalada, a versão mais recente será carregada por padrão.</span><span class="sxs-lookup"><span data-stu-id="58263-139">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="58263-140">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="58263-140">Provide feedback</span></span>

<span data-ttu-id="58263-141">Se você encontrar um bug ao usar o Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="58263-141">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="58263-142">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="58263-142">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="58263-143">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="58263-143">Next Steps</span></span>

<span data-ttu-id="58263-144">Para começar a usar o Azure PowerShell, consulte [Introdução ao Azure PowerShell](get-started-azureps.md) para saber mais sobre o módulo e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="58263-144">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
