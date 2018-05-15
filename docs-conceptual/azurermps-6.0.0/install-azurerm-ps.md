---
title: Instalar e configurar o Azure PowerShell | Microsoft Docs
description: Como instalar e configurar o Azure PowerShell para o primeiro uso.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: c6b8e2e8aa4afb9e58a2d357c4e51e19410a8188
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="9d7f9-103">Instalar e configurar o PowerShell do Azure</span><span class="sxs-lookup"><span data-stu-id="9d7f9-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="9d7f9-104">Este artigo explica as etapas para instalar os módulos do Azure PowerShell em um ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="9d7f9-105">Se você quiser usar o Azure PowerShell em macOS ou Linux, consulte o seguinte artigo: [Instalar e configurar o Azure PowerShell em macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="9d7f9-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="9d7f9-106">Requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="9d7f9-106">System requirements</span></span>

<span data-ttu-id="9d7f9-107">A versão 6.0.0 do Azure PowerShell requer a versão 5.0 (ou superior) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-107">Azure PowerShell version 6.0.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="9d7f9-108">As versões anteriores do Azure PowerShell necessitam de _pelo menos_ a versão 3.0 do PowerShell para executar qualquer cmdlet. Para obter informações sobre como atualizar para o PowerShell 5.0, consulte [esta tabela](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="9d7f9-108">Previous versions of Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="9d7f9-109">Etapa 1: Instalar o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="9d7f9-109">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="9d7f9-110">Instalar o Azure PowerShell na Galeria do PowerShell é o método preferencial de instalação.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-110">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

<span data-ttu-id="9d7f9-111">Instalar os itens da Galeria do PowerShell requer o módulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="9d7f9-112">Verifique se que você tem a versão apropriada do PowerShellGet e outros requisitos do sistema.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="9d7f9-113">Execute o seguinte comando para ver se você tem o PowerShellGet instalado em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="9d7f9-114">Você deverá ver algo semelhante à seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="9d7f9-115">Você precisa do PowerShellGet versão 1.1.2.0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="9d7f9-116">Para atualizar o PowerShellGet, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-116">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="9d7f9-117">Se você não tiver o PowerShellGet instalado, consulte a seção [Como obter o PowerShellGet](#how-to-get-powershellget) deste artigo.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9d7f9-118">Usar o PowerShellGet requer uma Política de Execução que permite executar scripts.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="9d7f9-119">Para obter mais informações sobre a Política de Execução do PowerShell, consulte [Sobre as Políticas de Execução](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="9d7f9-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="9d7f9-120">Etapa 2: instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d7f9-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="9d7f9-121">Instalando o Azure PowerShell a partir da Galeria do PowerShell requer privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="9d7f9-122">Execute o comando a seguir em uma sessão do PowerShell com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="9d7f9-123">Por padrão, a Galeria do PowerShell não está configurada como um repositório Confiável para o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9d7f9-124">Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="9d7f9-125">Responda “Sim” ou “Sim para Todos” para continuar com a instalação.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="9d7f9-126">Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="9d7f9-127">O AzureRM é um módulo do pacote cumulativo de atualizações para os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="9d7f9-128">Ao instalar o módulo AzureRM, qualquer outro módulo do Azure PowerShell que não tiver sido instalado anteriormente será baixado usando a Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="9d7f9-129">Um erro poderá ocorrer se a versão anterior do Azure PowerShell estiver instalada.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="9d7f9-130">Para resolver esse problema, consulte a seção [Atualizando para uma nova versão do Azure PowerShell](#update-azps) deste artigo.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="9d7f9-131">Etapa 3: Carregar o módulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="9d7f9-131">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="9d7f9-132">Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9d7f9-133">Isso deve ser feito em uma sessão normal (não elevada) do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="9d7f9-134">Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="9d7f9-135">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9d7f9-135">Next Steps</span></span>

<span data-ttu-id="9d7f9-136">Para obter mais informações sobre como usar o Azure PowerShell, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="9d7f9-137">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d7f9-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="9d7f9-138">Relatando comentários e problemas</span><span class="sxs-lookup"><span data-stu-id="9d7f9-138">Reporting issues and feedback</span></span>

<span data-ttu-id="9d7f9-139">Se você encontrar erros com a ferramenta, emita um problema na seção [Problemas](https://github.com/Azure/azure-powershell/issues) de nosso repositório do GitHub.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="9d7f9-140">Para fornecer comentários na linha de comando, use o cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9d7f9-141">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="9d7f9-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="9d7f9-142">Como obter o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="9d7f9-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="9d7f9-143">Cenário</span><span class="sxs-lookup"><span data-stu-id="9d7f9-143">Scenario</span></span>|<span data-ttu-id="9d7f9-144">Instalar instruções</span><span class="sxs-lookup"><span data-stu-id="9d7f9-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="9d7f9-145">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d7f9-145">Windows 10</span></span><br/><span data-ttu-id="9d7f9-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d7f9-146">Windows Server 2016</span></span>|<span data-ttu-id="9d7f9-147">Compilado no Windows Management Framework (WMF) 5.0 incluído no SO</span><span class="sxs-lookup"><span data-stu-id="9d7f9-147">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="9d7f9-148">Desejo fazer uma atualização para o PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="9d7f9-148">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="9d7f9-149">Instalar a versão mais recente do WMF</span><span class="sxs-lookup"><span data-stu-id="9d7f9-149">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="9d7f9-150">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="9d7f9-151">Estou executando uma versão do Windows com o PowerShell 3 ou 4</span><span class="sxs-lookup"><span data-stu-id="9d7f9-151">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="9d7f9-152"><il>[Obter os módulos do PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="9d7f9-152"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="9d7f9-153">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-153">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="9d7f9-154">Verificando a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d7f9-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="9d7f9-155">Embora recomendemos que você atualize para a última versão o mais cedo possível, várias versões do Azure PowerShell têm suporte.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="9d7f9-156">Para determinar a versão do Azure PowerShell instalada, execute `Get-Module AzureRM` na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-156">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="9d7f9-157">Suporte para métodos de implantação clássicos</span><span class="sxs-lookup"><span data-stu-id="9d7f9-157">Support for classic deployment methods</span></span>

<span data-ttu-id="9d7f9-158">Se você tiver implantações que usam o modelo de implantação clássico, será possível instalar a versão de Gerenciamento de Serviços do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="9d7f9-159">Para obter mais informações, veja [Instalar o módulo Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="9d7f9-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="9d7f9-160">Os módulos Azure e AzureRM compartilham dependências em comum.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="9d7f9-161">Caso você use ambos os módulos, Azure e AzureRM, instale a mesma versão de cada pacote.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="9d7f9-162">Atualizando para uma nova versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d7f9-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="9d7f9-163">Se houver uma versão anterior do Azure PowerShell instalada que inclua o módulo de Gerenciamento de Serviços, o seguinte erro poderá ocorrer:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="9d7f9-164">Assim como indicado pela mensagem de erro, é necessário usar o parâmetro AllowClobber para instalar o módulo.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="9d7f9-165">Use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-165">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="9d7f9-166">Para saber mais, confira o tópico de ajuda para [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="9d7f9-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="9d7f9-167">Instalando versões de módulo lado a lado</span><span class="sxs-lookup"><span data-stu-id="9d7f9-167">Installing module versions side by side</span></span>

<span data-ttu-id="9d7f9-168">O método PowerShellGet de instalação é o único método que suporta a instalação de diversas versões.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="9d7f9-169">Por exemplo, é possível ter scripts escritos usando uma versão anterior do Azure PowerShell que você não tem tempo nem recursos para atualizar.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="9d7f9-170">Os comandos a seguir ilustram como instalar diversas versões do Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="9d7f9-171">somente uma versão do módulo pode ser carregada em uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="9d7f9-172">Você deve abrir uma nova janela do PowerShell e usar `Import-Module` para importar uma versão específica dos cmdlets do AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="9d7f9-173">A versão 2.1.0 e a versão 1.2.6 são as primeiras versões do módulo projetadas para ser instaladas e usadas lado a lado.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="9d7f9-174">Ao carregar uma versão anterior do Azure PowerShell, versões incompatíveis do módulo **AzureRM.Profile** serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="9d7f9-175">Desse modo, os cmdlets solicitarão que você faça logon sempre que um cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-175">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="9d7f9-176">Outros métodos de instalação</span><span class="sxs-lookup"><span data-stu-id="9d7f9-176">Other installation methods</span></span>

<span data-ttu-id="9d7f9-177">Para obter informações sobre como instalar usando o Web Platform Installer ou o Pacote MSI, consulte [Outros métodos de instalação](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="9d7f9-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
