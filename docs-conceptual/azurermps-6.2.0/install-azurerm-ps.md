---
title: Instalar o Azure PowerShell com o PowerShellGet
description: Como instalar o Azure PowerShell com o PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323094"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="b38c7-103">Instalar o Azure PowerShell com o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="b38c7-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="b38c7-104">Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows usando o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b38c7-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="b38c7-105">Este é o modo preferencial para instalar o Azure PowerShell, mas se você preferir instalar com o pacote do Web Platform Installer ou MSI, confira [Outros métodos de instalação](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="b38c7-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="b38c7-106">Se você quiser usar o Azure PowerShell em macOS ou Linux, consulte o seguinte artigo: [Instalar e configurar o Azure PowerShell em macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="b38c7-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="b38c7-107">Requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="b38c7-107">System requirements</span></span>

<span data-ttu-id="b38c7-108">A versão 6.1.0 do Azure PowerShell requer a versão 5.0 (ou superior) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="b38c7-109">Para obter informações sobre como atualizar para o PowerShell 5.0, confira [Atualizações atuais do Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="b38c7-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="b38c7-110">O PowerShellGet é automaticamente incluído como parte do PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="b38c7-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="b38c7-111">Instalar ou atualizar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b38c7-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="b38c7-112">Instalando o Azure PowerShell a partir da Galeria do PowerShell requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="b38c7-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="b38c7-113">Execute o comando a seguir em uma sessão do PowerShell com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="b38c7-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="b38c7-114">Este comando atualizará qualquer instalação existente do Azure PowerShell em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="b38c7-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="b38c7-115">Se você precisar ter mais de uma versão instalada, confira as respostas de Perguntas frequentes para [Posso instalar várias versões do Azure PowerShell?](#multiple-versions)</span><span class="sxs-lookup"><span data-stu-id="b38c7-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="b38c7-116">Por padrão, a Galeria do PowerShell não está configurada como um repositório confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b38c7-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="b38c7-117">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="b38c7-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="b38c7-118">Responda “Sim” ou “Sim para Todos” para continuar com a instalação.</span><span class="sxs-lookup"><span data-stu-id="b38c7-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="b38c7-119">Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.</span><span class="sxs-lookup"><span data-stu-id="b38c7-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="b38c7-120">O AzureRM é um módulo do pacote cumulativo de atualizações para os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b38c7-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="b38c7-121">Ao instalar o módulo AzureRM, qualquer outro módulo do Azure PowerShell que não tiver sido instalado anteriormente será baixado da Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="b38c7-122">Carregar o módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b38c7-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="b38c7-123">Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="b38c7-124">Isso deve ser feito em uma sessão normal (não elevada) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="b38c7-125">Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b38c7-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="b38c7-126">Relatando comentários e problemas</span><span class="sxs-lookup"><span data-stu-id="b38c7-126">Reporting issues and feedback</span></span>

<span data-ttu-id="b38c7-127">Se você encontrar quaisquer erros com a ferramenta, [relate um problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="b38c7-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="b38c7-128">Para fornecer comentários na linha de comando, use o cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="b38c7-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b38c7-129">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b38c7-129">Next Steps</span></span>

<span data-ttu-id="b38c7-130">Para obter mais informações sobre como usar o Azure PowerShell, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="b38c7-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="b38c7-131">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b38c7-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="b38c7-132">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="b38c7-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="b38c7-133">Como posso verificar a versão do Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="b38c7-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="b38c7-134">Embora recomendemos que você atualize para a última versão o mais cedo possível, várias versões do Azure PowerShell têm suporte.</span><span class="sxs-lookup"><span data-stu-id="b38c7-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="b38c7-135">Para determinar a versão do Azure PowerShell instalada, execute `Get-Module AzureRM` na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b38c7-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="b38c7-136">Posso usar o Azure PowerShell para implantações clássicas do Azure?</span><span class="sxs-lookup"><span data-stu-id="b38c7-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="b38c7-137">Se você tiver implantações que usam o modelo de implantação clássico, será possível instalar a versão de Gerenciamento de Serviços do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="b38c7-138">Para obter mais informações, veja [Instalar o módulo Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="b38c7-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="b38c7-139">Os módulos Azure e AzureRM compartilham dependências em comum.</span><span class="sxs-lookup"><span data-stu-id="b38c7-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="b38c7-140">Caso você use ambos os módulos, Azure e AzureRM, instale a mesma versão de cada pacote.</span><span class="sxs-lookup"><span data-stu-id="b38c7-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="b38c7-141"><a name="multiple-versions"/>Posso instalar várias versões do Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="b38c7-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="b38c7-142">O PowerShellGet é o único método de instalação que oferece suporte a várias versões.</span><span class="sxs-lookup"><span data-stu-id="b38c7-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="b38c7-143">Para instalar várias versões, você pode adicionar o parâmetro `-RequiredVersion` para o cmdlet `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="b38c7-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="b38c7-144">Por exemplo, para instalar as duas versões 6.1.0 e 1.2.9:</span><span class="sxs-lookup"><span data-stu-id="b38c7-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="b38c7-145">somente uma versão do módulo pode ser carregada em uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="b38c7-146">Você deve abrir uma nova janela do PowerShell e usar `Import-Module` para importar uma versão específica do módulo do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b38c7-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="b38c7-147">A versão 2.1.0 e a versão 1.2.6 são as primeiras versões do módulo projetadas para ser instaladas e usadas lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b38c7-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="b38c7-148">Ao carregar uma versão anterior do Azure PowerShell, versões incompatíveis do módulo **AzureRM.Profile** serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="b38c7-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="b38c7-149">Desse modo, os cmdlets solicitarão que você faça logon sempre que um cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b38c7-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
