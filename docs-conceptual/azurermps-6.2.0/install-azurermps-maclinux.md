---
title: Instale o Azure PowerShell no macOS ou no Linux
description: Como instalar o Azure PowerShell no macOS ou no Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323162"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="08b5d-103">Instale o Azure PowerShell no macOS ou no Linux</span><span class="sxs-lookup"><span data-stu-id="08b5d-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="08b5d-104">Para plataformas não Windows, é possível executar o Azure PowerShell em cima do PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="08b5d-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="08b5d-105">Em vez do Azure PowerShell padrão criado no .NET Framework para Windows, este produto é criado para .NET Core e pode ser executado em qualquer plataforma que ofereça suporte ao tempo de execução do .Net Core.</span><span class="sxs-lookup"><span data-stu-id="08b5d-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="08b5d-106">Atualmente, o PowerShell Core v6 e o Azure PowerShell para .NET Core ainda estão na versão beta.</span><span class="sxs-lookup"><span data-stu-id="08b5d-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="08b5d-107">O suporte para esses produtos é limitado.</span><span class="sxs-lookup"><span data-stu-id="08b5d-107">Support for these products is limited.</span></span> <span data-ttu-id="08b5d-108">Se você tiver problemas ou detectar erros, relate os problemas no GitHub.</span><span class="sxs-lookup"><span data-stu-id="08b5d-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="08b5d-109">Problemas do PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="08b5d-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="08b5d-110">Problemas do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="08b5d-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="08b5d-111">Instalar o PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="08b5d-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="08b5d-112">A instalação do PowerShell Core v6 no Linux ou no macOS varia de acordo com a distribuição de Linux e a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08b5d-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="08b5d-113">Instruções detalhadas podem ser encontradas nos seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="08b5d-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="08b5d-114">Instalar o PowerShell Core no macOS</span><span class="sxs-lookup"><span data-stu-id="08b5d-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="08b5d-115">Instalar o PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="08b5d-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="08b5d-116">Instalar o Azure PowerShell para .NET Core</span><span class="sxs-lookup"><span data-stu-id="08b5d-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="08b5d-117">O PowerShell Core v6 é fornecido com o módulo PowerShellGet já instalado.</span><span class="sxs-lookup"><span data-stu-id="08b5d-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="08b5d-118">Isso torna fácil instalar qualquer módulo que está publicado na Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08b5d-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="08b5d-119">Para instalar o Azure PowerShell, abra uma nova sessão do PowerShell e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="08b5d-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="08b5d-120">Carregar o módulo AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="08b5d-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="08b5d-121">Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08b5d-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="08b5d-122">Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="08b5d-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="08b5d-123">Depois que a importação for concluída, você poderá testar seu módulo recém-instalado tentando entrar no Azure usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="08b5d-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="08b5d-124">O comando acima solicitará que você acesse `https://aka.ms/devicelogin` e insira o código fornecido.</span><span class="sxs-lookup"><span data-stu-id="08b5d-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="08b5d-125">Cmdlets disponíveis</span><span class="sxs-lookup"><span data-stu-id="08b5d-125">Available cmdlets</span></span>

<span data-ttu-id="08b5d-126">Os módulos do Azure PowerShell para .NET padrão ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="08b5d-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="08b5d-127">Esses módulos não fornecem o conjunto completo de cmdlets que estão disponíveis para a versão do Windows dos módulos.</span><span class="sxs-lookup"><span data-stu-id="08b5d-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="08b5d-128">As funções a seguir são implementadas em módulos AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="08b5d-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="08b5d-129">Gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="08b5d-129">Account management</span></span>
  - <span data-ttu-id="08b5d-130">Fazer logon com a conta da Microsoft, conta organizacional ou entidade de serviço por meio do Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="08b5d-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="08b5d-131">Salvar credenciais para o disco com Save-AzureRmContext e carregar as credenciais salvas usando Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="08b5d-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="08b5d-132">Ambiente</span><span class="sxs-lookup"><span data-stu-id="08b5d-132">Environment</span></span>
  - <span data-ttu-id="08b5d-133">Obter os diferentes ambientes do Microsoft Azure prontos para uso</span><span class="sxs-lookup"><span data-stu-id="08b5d-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="08b5d-134">Adicionar/definir/remover ambientes personalizados (como seus ambientes do Azure Stack ou do Pacote do Microsoft Azure)</span><span class="sxs-lookup"><span data-stu-id="08b5d-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="08b5d-135">Cmdlets de plano de gerenciamento para os Serviços do Azure usando as interfaces do Resource Manager e do Gerenciamento de Serviços.</span><span class="sxs-lookup"><span data-stu-id="08b5d-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="08b5d-136">Máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="08b5d-136">Virtual Machine</span></span>
  - <span data-ttu-id="08b5d-137">Serviço de Aplicativo (Sites)</span><span class="sxs-lookup"><span data-stu-id="08b5d-137">App Service (Websites)</span></span>
  - <span data-ttu-id="08b5d-138">Banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="08b5d-138">SQL Database</span></span>
  - <span data-ttu-id="08b5d-139">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="08b5d-139">Storage</span></span>
  - <span data-ttu-id="08b5d-140">Rede</span><span class="sxs-lookup"><span data-stu-id="08b5d-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="08b5d-141">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="08b5d-141">Next Steps</span></span>

<span data-ttu-id="08b5d-142">Para saber mais sobre como usar o Azure PowerShell, confira o artigo [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="08b5d-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
