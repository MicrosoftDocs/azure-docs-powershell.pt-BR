---
title: Instalar e configurar o Azure PowerShell em macOS e Linux | Microsoft Docs
description: Como instalar e configurar o Azure PowerShell para o primeiro uso em macOS e Linux.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="8de19-103">Instalar e configurar o Azure PowerShell em macOS e Linux</span><span class="sxs-lookup"><span data-stu-id="8de19-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="8de19-104">Agora é possível instalar o PowerShell Core v6 e o Azure PowerShell em plataformas não Windows.</span><span class="sxs-lookup"><span data-stu-id="8de19-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="8de19-105">O processo de instalação do Azure PowerShell no macOS e Linux não é diferente do Windows, no entanto, você deve primeiro instalar PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="8de19-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="8de19-106">Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.</span><span class="sxs-lookup"><span data-stu-id="8de19-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="8de19-107">O suporte para esses produtos é limitado.</span><span class="sxs-lookup"><span data-stu-id="8de19-107">Support for these products is limited.</span></span> <span data-ttu-id="8de19-108">Se você tiver problemas ou detectar erros, envie os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="8de19-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="8de19-109">Problemas do PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="8de19-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="8de19-110">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8de19-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="8de19-111">Etapa 1: Instalar o PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="8de19-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="8de19-112">O processo de instalação do PowerShell Core v6 varia dependendo do sistema operacional de destino.</span><span class="sxs-lookup"><span data-stu-id="8de19-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="8de19-113">Embora seja possível instalar o PowerShell Core v6 no Windows, este artigo concentra-se em macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="8de19-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="8de19-114">Se você quiser usar o Azure PowerShell no Windows, consulte o artigo de [instalação](./install-azurerm-ps.md) para Windows.</span><span class="sxs-lookup"><span data-stu-id="8de19-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="8de19-115">A instalação do **PowerShell Core v6** no Linux ou no macOS varia de acordo com a distribuição de Linux e a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8de19-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="8de19-116">Instruções detalhadas podem ser encontradas no seguinte artigo:</span><span class="sxs-lookup"><span data-stu-id="8de19-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="8de19-117">Instalação do PowerShell Core no macOS e no Linux</span><span class="sxs-lookup"><span data-stu-id="8de19-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="8de19-118">Etapa 2: instalar o Azure PowerShell para .NET Core</span><span class="sxs-lookup"><span data-stu-id="8de19-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="8de19-119">O PowerShell Core v6 é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="8de19-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="8de19-120">Isso torna fácil instalar qualquer módulo que está publicado na Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8de19-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="8de19-121">Para instalar o Azure PowerShell, abra uma nova sessão do PowerShell e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="8de19-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="8de19-122">Etapa 3: carregar o módulo AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="8de19-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="8de19-123">Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8de19-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="8de19-124">Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8de19-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="8de19-125">Depois que a importação for concluída, você poderá testar seu módulo recém-instalado tentando entrar no Azure usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="8de19-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="8de19-126">O comando acima solicitará que você acesse `https://aka.ms/devicelogin` e insira o código fornecido.</span><span class="sxs-lookup"><span data-stu-id="8de19-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="8de19-127">Cmdlets disponíveis</span><span class="sxs-lookup"><span data-stu-id="8de19-127">Available cmdlets</span></span>

<span data-ttu-id="8de19-128">Os módulos do Azure PowerShell para .NET padrão ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="8de19-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="8de19-129">Esses módulos não fornecem o conjunto completo de cmdlets que estão disponíveis para a versão do Windows dos módulos.</span><span class="sxs-lookup"><span data-stu-id="8de19-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="8de19-130">As funções a seguir são implementadas em módulos AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="8de19-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="8de19-131">Gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="8de19-131">Account management</span></span>
  - <span data-ttu-id="8de19-132">Fazer logon com a conta da Microsoft, conta organizacional ou entidade de serviço por meio do Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8de19-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="8de19-133">Salvar credenciais para o disco com Save-AzureRmContext e carregar as credenciais salvas usando Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8de19-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="8de19-134">Ambiente</span><span class="sxs-lookup"><span data-stu-id="8de19-134">Environment</span></span>
  - <span data-ttu-id="8de19-135">Obter os diferentes ambientes do Microsoft Azure prontos para uso</span><span class="sxs-lookup"><span data-stu-id="8de19-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="8de19-136">Adicionar/definir/remover ambientes personalizados (como seus ambientes do Azure Stack ou do Pacote do Microsoft Azure)</span><span class="sxs-lookup"><span data-stu-id="8de19-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="8de19-137">Cmdlets de plano de gerenciamento para os Serviços do Azure usando as interfaces do Resource Manager e do Gerenciamento de Serviços.</span><span class="sxs-lookup"><span data-stu-id="8de19-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="8de19-138">Máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="8de19-138">Virtual Machine</span></span>
  - <span data-ttu-id="8de19-139">Serviço de Aplicativo (Sites)</span><span class="sxs-lookup"><span data-stu-id="8de19-139">App Service (Websites)</span></span>
  - <span data-ttu-id="8de19-140">Banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8de19-140">SQL Database</span></span>
  - <span data-ttu-id="8de19-141">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="8de19-141">Storage</span></span>
  - <span data-ttu-id="8de19-142">Rede</span><span class="sxs-lookup"><span data-stu-id="8de19-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="8de19-143">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="8de19-143">Next Steps</span></span>

<span data-ttu-id="8de19-144">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8de19-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
