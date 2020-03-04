---
title: Instalar o Azure PowerShell com um MSI
description: Como instalar o Azure PowerShell sem o PowerShellGet usando uma MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 9f161d6a2bbe696bca5d2a63d39ab734cfc25cb8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264359"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="0bae6-103">Instalar o Azure PowerShell no Windows com a MSI</span><span class="sxs-lookup"><span data-stu-id="0bae6-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="0bae6-104">Este artigo explica como instalar o Azure PowerShell no Windows usando um instalador da MSI.</span><span class="sxs-lookup"><span data-stu-id="0bae6-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="0bae6-105">O instalador do MSI (Microsoft Windows Installer) é fornecido para ambientes em que a Galeria do PowerShell pode ser bloqueada por um firewall ou em que um instalador offline é necessário.</span><span class="sxs-lookup"><span data-stu-id="0bae6-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="0bae6-106">A maneira recomendada de instalar o Azure PowerShell é com o PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0bae6-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="0bae6-107">Para obter instruções sobre como usar o PowerShellGet para instalar o Azure PowerShell, confira [Instalar o Azure PowerShell com o PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="0bae6-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bae6-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bae6-108">Requirements</span></span>

<span data-ttu-id="0bae6-109">O instalador MSI para Azure PowerShell funciona __somente__ para o PowerShell 5.1 no Windows.</span><span class="sxs-lookup"><span data-stu-id="0bae6-109">The MSI installer for Azure PowerShell works __only__ for PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="0bae6-110">Para instalação em plataformas que não são Windows ou versões posteriores do PowerShell, [Instale com PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="0bae6-110">For installation on non-Windows platforms or later versions of powershell, [Install with PowerShellGet](install-az-ps.md).</span></span>
<span data-ttu-id="0bae6-111">Para verificar sua versão do PowerShell, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="0bae6-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="0bae6-112">Para usar o Azure PowerShell no PowerShell 5.1, é necessário:</span><span class="sxs-lookup"><span data-stu-id="0bae6-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="0bae6-113">Atualize para o [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) se necessário.</span><span class="sxs-lookup"><span data-stu-id="0bae6-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="0bae6-114">Se você estiver usando o Windows 10, você já tem o PowerShell 5.1 instalado.</span><span class="sxs-lookup"><span data-stu-id="0bae6-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="0bae6-115">Instale o [.NET Framework 4.7.2 ou posterior](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="0bae6-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="0bae6-116">Instalar ou atualizar no Windows usando o pacote MSI</span><span class="sxs-lookup"><span data-stu-id="0bae6-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="0bae6-117">O Azure PowerShell para Windows é instalado usando o arquivo MSI disponível no [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v3.5.0-February2020).</span><span class="sxs-lookup"><span data-stu-id="0bae6-117">Azure PowerShell for Windows is installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v3.5.0-February2020).</span></span> <span data-ttu-id="0bae6-118">Se você tiver instalado versões anteriores dos módulos do Azure como um MSI, o instalador as removerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0bae6-118">If you have installed earlier versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="0bae6-119">O pacote de MSI instala os módulos em `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="0bae6-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="0bae6-120">Para começar a trabalhar com o Azure PowerShell, entre com suas credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bae6-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="0bae6-121">Se você desabilitou o carregamento automático do módulo, precisará importar manualmente o módulo com `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="0bae6-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="0bae6-122">Por causa da maneira como o módulo está estruturado, isso pode levar até um minuto.</span><span class="sxs-lookup"><span data-stu-id="0bae6-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="0bae6-123">Será necessário repetir essa etapa para cada sessão nova do PowerShell que você iniciar.</span><span class="sxs-lookup"><span data-stu-id="0bae6-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="0bae6-124">Para aprender a manter a entrada no Azure entre as sessões do PowerShell, confira [Manter credenciais do usuário entre as sessões do PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0bae6-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="0bae6-125">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="0bae6-125">Provide feedback</span></span>

<span data-ttu-id="0bae6-126">Se você encontrar um bug no Azure Powershell, [registre o problema no GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="0bae6-126">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="0bae6-127">Para fazer comentários na linha de comando, use o cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="0bae6-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0bae6-128">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0bae6-128">Next Steps</span></span>

<span data-ttu-id="0bae6-129">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0bae6-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="0bae6-130">Se você estiver familiarizado com o Azure PowerShell e precisar migrar do AzureRM, confira [Migrar do AzureRM para Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="0bae6-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
