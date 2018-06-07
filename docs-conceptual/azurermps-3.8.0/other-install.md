---
title: Outras maneiras de instalar o Azure PowerShell | Microsoft Docs
description: Como instalar o Azure PowerShell usando o pacote MSI ou o Web Platform Installer.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 354061987951728fd8a5802b01f3cb8b7c60a072
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820911"
---
# <a name="other-installation-methods"></a><span data-ttu-id="00f74-103">Outros métodos de instalação</span><span class="sxs-lookup"><span data-stu-id="00f74-103">Other installation methods</span></span>

<span data-ttu-id="00f74-104">O Azure PowerShell tem vários métodos de instalação.</span><span class="sxs-lookup"><span data-stu-id="00f74-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="00f74-105">O uso do PowerShellGet com a Galeria do PowerShell é o método preferencial.</span><span class="sxs-lookup"><span data-stu-id="00f74-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="00f74-106">O Azure PowerShell pode ser instalado no Windows usando o Web Platform Installer (WebPI) ou usando o MSI de arquivo disponível no GitHub.</span><span class="sxs-lookup"><span data-stu-id="00f74-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="00f74-107">O Azure PowerShell também pode ser instalado em um contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="00f74-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="00f74-108">Instalar no Windows usando o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="00f74-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="00f74-109">A instalação do Azure PowerShell mais recente do WebPI é feita da mesma maneira como era nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="00f74-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="00f74-110">Baixe o [pacote WebPI do Azure PowerShell](http://aka.ms/webpi-azps) e inicie a instalação.</span><span class="sxs-lookup"><span data-stu-id="00f74-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="00f74-111">Se você já tiver instalado módulos do Azure da Galeria do PowerShell, o instalador os removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="00f74-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="00f74-112">Isso simplifica a seu ambiente, garantindo que apenas uma versão do Azure PowerShell está instalada.</span><span class="sxs-lookup"><span data-stu-id="00f74-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="00f74-113">No entanto, há cenários em que será necessário ter diversas versões instaladas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="00f74-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="00f74-114">Os módulos da Galeria do PowerShell instalam módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="00f74-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="00f74-115">Por outro lado, o instalador do WebPI instalam os módulos do Azure no `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="00f74-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="00f74-116">Se ocorrer um erro durante a instalação, você poderá remover manualmente as pastas do Azure\* de sua pasta `$env:ProgramFiles\WindowsPowerShell\Modules` e tentar instalar novamente.</span><span class="sxs-lookup"><span data-stu-id="00f74-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="00f74-117">Quando a instalação for concluída, a configuração do `$env:PSModulePath` deverá incluir os diretórios que contêm os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00f74-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="00f74-118">O comando a seguir pode ser usado para verificar se o Azure PowerShell foi instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="00f74-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="00f74-119">Há um problema conhecido que pode ocorrer durante a instalação do WebPI.</span><span class="sxs-lookup"><span data-stu-id="00f74-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="00f74-120">Se o computador precisar de uma reinicialização devido a atualizações do sistema ou outras instalações, isso poderá fazer com que as atualizações do `$env:PSModulePath` falhem ao incluir o caminho em que o Azure PowerShell está instalado.</span><span class="sxs-lookup"><span data-stu-id="00f74-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="00f74-121">Ao tentar carregar ou executar cmdlets após a instalação, você poderá receber a seguinte mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="00f74-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="00f74-122">Esse erro pode ser corrigido ao reiniciar o computador ou importar o módulo usando o caminho totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="00f74-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="00f74-123">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="00f74-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="00f74-124">Instalar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="00f74-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="00f74-125">O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="00f74-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="00f74-126">Se você tiver versões anteriores dos módulos do Azure instaladas, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="00f74-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="00f74-127">O pacote MSI instala módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`, mas não cria pastas específicas de versão.</span><span class="sxs-lookup"><span data-stu-id="00f74-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="00f74-128">Instalar em um contêiner do Docker</span><span class="sxs-lookup"><span data-stu-id="00f74-128">Install in a Docker container</span></span>

<span data-ttu-id="00f74-129">Vamos manter uma imagem do Docker pré-configurada no Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00f74-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="00f74-130">Execute o contêiner com `docker run`.</span><span class="sxs-lookup"><span data-stu-id="00f74-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="00f74-131">Além disso, vamos manter um subconjunto de cmdlets como um contêiner do PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="00f74-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="00f74-132">Para Mac/Linux, use a imagem `latest`.</span><span class="sxs-lookup"><span data-stu-id="00f74-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="00f74-133">Para Windows, use a imagem `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="00f74-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="00f74-134">O Azure PowerShell é instalado na imagem por meio de `Install-Module` da [Galeria do PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="00f74-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>