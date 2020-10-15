---
title: Instalar o Azure PowerShell com um MSI
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001648"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="86cd3-103">Instalar o Azure PowerShell no Windows com a MSI</span><span class="sxs-lookup"><span data-stu-id="86cd3-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="86cd3-104">Este artigo explica como instalar o Azure PowerShell no Windows usando um instalador da MSI.</span><span class="sxs-lookup"><span data-stu-id="86cd3-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="86cd3-105">O instalador do MSI (Microsoft Windows Installer) é fornecido para ambientes em que a Galeria do PowerShell pode ser bloqueada por um firewall ou em que um instalador offline é necessário.</span><span class="sxs-lookup"><span data-stu-id="86cd3-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="86cd3-106">A maneira recomendada de instalar o Azure PowerShell é com o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="86cd3-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="86cd3-107">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="86cd3-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86cd3-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86cd3-108">Requirements</span></span>

<span data-ttu-id="86cd3-109">O instalador do MSI no Windows foi projetado para instalar o Azure PowerShell somente para o PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="86cd3-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="86cd3-110">Para instalação em plataformas que não são Windows ou versões posteriores do PowerShell, [Instalar com PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="86cd3-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="86cd3-111">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="86cd3-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="86cd3-112">Para usar o Azure PowerShell no PowerShell 5.1, é necessário:</span><span class="sxs-lookup"><span data-stu-id="86cd3-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="86cd3-113">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário.</span><span class="sxs-lookup"><span data-stu-id="86cd3-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="86cd3-114">Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="86cd3-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="86cd3-115">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="86cd3-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="86cd3-116">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="86cd3-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="86cd3-117">O pacote MSI para o Azure PowerShell está disponível no [GitHub](https://github.com/Azure/azure-powershell/releases):</span><span class="sxs-lookup"><span data-stu-id="86cd3-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="86cd3-118">Acesse https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="86cd3-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="86cd3-119">Procure o Módulo da Galeria mais recente para Azure PowerShell (eles estão listados cronologicamente e normalmente são apenas uma versão de lançamento sem nome, como "4.7.0").</span><span class="sxs-lookup"><span data-stu-id="86cd3-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="86cd3-120">Role para baixo até a parte inferior das observações de patch e clique na seta ao lado de "Ativos" para revelar as opções de MSI.</span><span class="sxs-lookup"><span data-stu-id="86cd3-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="86cd3-121">Clique no MSI Az-Cmdlets de sua escolha para iniciar o download.</span><span class="sxs-lookup"><span data-stu-id="86cd3-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="86cd3-122">Se você tiver instalado versões anteriores do Azure PowerShell usando o MSI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="86cd3-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="86cd3-123">O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="86cd3-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="86cd3-124">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="86cd3-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="86cd3-125">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="86cd3-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="86cd3-126">Por causa da maneira como o módulo está estruturado, isso pode levar até um minuto.</span><span class="sxs-lookup"><span data-stu-id="86cd3-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="86cd3-127">Será necessário repetir essa etapa para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="86cd3-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="86cd3-128">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="86cd3-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="86cd3-129">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="86cd3-129">Provide feedback</span></span>

<span data-ttu-id="86cd3-130">Se você encontrar um bug no Azure PowerShell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="86cd3-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="86cd3-131">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="86cd3-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="86cd3-132">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="86cd3-132">Next Steps</span></span>

<span data-ttu-id="86cd3-133">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="86cd3-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="86cd3-134">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="86cd3-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
