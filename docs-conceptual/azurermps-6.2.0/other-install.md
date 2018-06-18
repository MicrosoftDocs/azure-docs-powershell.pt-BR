---
title: Outras maneiras de instalar o Azure PowerShell
description: Como instalar o Azure PowerShell usando o pacote MSI ou o Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323315"
---
# <a name="other-installation-methods"></a><span data-ttu-id="7c087-103">Outros métodos de instalação</span><span class="sxs-lookup"><span data-stu-id="7c087-103">Other installation methods</span></span>

<span data-ttu-id="7c087-104">Este artigo explica como instalar o Azure PowerShell usando uma MSI ou o Web Platform Installer (WebPI).</span><span class="sxs-lookup"><span data-stu-id="7c087-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="7c087-105">Você também pode executar o Azure PowerShell de dentro de um contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="7c087-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="7c087-106">Use esses métodos de instalação somente se eles forem necessários para o seu sistema.</span><span class="sxs-lookup"><span data-stu-id="7c087-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="7c087-107">A maneira canônica para instalar o Azure PowerShell é através do PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="7c087-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="7c087-108">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7c087-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="7c087-109">Para instalar em ambientes Linux ou macOS, confira [Instalar o Azure PowerShell no macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="7c087-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="7c087-110">Instalar ou atualizar no Windows usando o Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="7c087-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="7c087-111">A instalação do Azure PowerShell mais recente do WebPI é feita da mesma maneira como era nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7c087-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="7c087-112">Baixe o [pacote WebPI do Azure PowerShell](http://aka.ms/webpi-azps) e inicie a instalação.</span><span class="sxs-lookup"><span data-stu-id="7c087-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="7c087-113">Se você já tiver instalado módulos do Azure da Galeria do PowerShell, o instalador os removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c087-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="7c087-114">Isso simplifica a seu ambiente, garantindo que apenas uma versão do Azure PowerShell está instalada.</span><span class="sxs-lookup"><span data-stu-id="7c087-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="7c087-115">No entanto, há cenários em que será necessário ter diversas versões instaladas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7c087-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="7c087-116">Os módulos da Galeria do PowerShell instalam módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="7c087-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="7c087-117">Por outro lado, o instalador do WebPI instalam os módulos do Azure no `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="7c087-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="7c087-118">Se ocorrer um erro durante a instalação, você poderá remover manualmente as pastas do `Azure*` de sua pasta `$env:ProgramFiles\WindowsPowerShell\Modules` e tentar instalar novamente.</span><span class="sxs-lookup"><span data-stu-id="7c087-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="7c087-119">Quando a instalação for concluída, a configuração do `$env:PSModulePath` deverá incluir os diretórios que contêm os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c087-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="7c087-120">O comando a seguir pode ser usado para verificar se o Azure PowerShell foi instalado corretamente:</span><span class="sxs-lookup"><span data-stu-id="7c087-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="7c087-121">Há um problema conhecido que pode ocorrer durante a instalação do WebPI.</span><span class="sxs-lookup"><span data-stu-id="7c087-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="7c087-122">Se o computador precisar de uma reinicialização devido a atualizações do sistema ou outras instalações, isso poderá fazer com que as atualizações do `$env:PSModulePath` falhem ao incluir o caminho em que o Azure PowerShell está instalado.</span><span class="sxs-lookup"><span data-stu-id="7c087-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="7c087-123">Ao tentar carregar ou executar cmdlets após a instalação, você poderá receber a seguinte mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="7c087-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="7c087-124">Esse erro pode ser corrigido ao reiniciar o computador ou importar o módulo usando o caminho totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="7c087-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="7c087-125">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="7c087-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="7c087-126">O Azure PowerShell pode ser instalado usando o arquivo MSI disponível no [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="7c087-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="7c087-127">Se você tiver versões anteriores dos módulos do Azure instaladas, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c087-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="7c087-128">O pacote MSI instala módulos no `$env:ProgramFiles\WindowsPowerShell\Modules`, mas não cria pastas específicas de versão.</span><span class="sxs-lookup"><span data-stu-id="7c087-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="7c087-129">Executar em um contêiner do Docker</span><span class="sxs-lookup"><span data-stu-id="7c087-129">Run in a Docker container</span></span>

<span data-ttu-id="7c087-130">Vamos manter um conjunto de imagens do Docker pré-configuradas no Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c087-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="7c087-131">Há dois tipos de contêineres disponíveis: os que estão executando o PowerShell tradicional no Windows, e um contêiner executando o PowerShell Core no Windows ou no Linux.</span><span class="sxs-lookup"><span data-stu-id="7c087-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="7c087-132">Ambiente</span><span class="sxs-lookup"><span data-stu-id="7c087-132">Environment</span></span> | <span data-ttu-id="7c087-133">Imagem do Docker</span><span class="sxs-lookup"><span data-stu-id="7c087-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="7c087-134">PowerShell no Windows</span><span class="sxs-lookup"><span data-stu-id="7c087-134">PowerShell on Windows</span></span> | [<span data-ttu-id="7c087-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="7c087-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="7c087-136">PowerShell Core no Windows</span><span class="sxs-lookup"><span data-stu-id="7c087-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="7c087-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="7c087-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="7c087-138">PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="7c087-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="7c087-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="7c087-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="7c087-140">Para executar qualquer um desses contêineres, você deve usar `docker run -it $ImageName` para obter um terminal interativo.</span><span class="sxs-lookup"><span data-stu-id="7c087-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="7c087-141">Por exemplo, para executar o PowerShell Core no contêiner do Linux, use:</span><span class="sxs-lookup"><span data-stu-id="7c087-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="7c087-142">Para executar um contêiner do Windows no Docker, o sistema operacional do host deve ser Windows e o Docker deve ser definido para executar contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="7c087-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="7c087-143">Para obter informações sobre como alternar entre ambientes Windows e Linux no Docker, confira a documentação do Docker [Alternar entre contêineres do Windows e do Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="7c087-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>