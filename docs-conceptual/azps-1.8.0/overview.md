---
title: Visão geral do Azure PowerShell
description: Uma visão geral do módulo Az do Azure PowerShell, com informações sobre como instalar e começar.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863886"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="523d7-103">Visão geral do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="523d7-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="523d7-104">O Azure PowerShell fornece um conjunto de cmdlets que usa o modelo do [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) para gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="523d7-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="523d7-105">O Azure PowerShell usa o .NET Standard, disponibilizando-o para Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="523d7-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="523d7-106">O Azure PowerShell também está disponível no Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="523d7-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="523d7-107">Sobre o novo módulo Az</span><span class="sxs-lookup"><span data-stu-id="523d7-107">About the new Az module</span></span>

<span data-ttu-id="523d7-108">Esta documentação descreve o novo módulo Az para o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="523d7-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="523d7-109">Este novo módulo é escrito desde o início no .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="523d7-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="523d7-110">O uso do .NET Standard permite que o Azure PowerShell seja executado no PowerShell 5.1 no Windows ou no PowerShell Core 6.x e posterior em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="523d7-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="523d7-111">O módulo Az agora é a maneira pretendida de interagir com o Azure por meio do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="523d7-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="523d7-112">O AzureRM continuará recebendo correções de bugs, mas já não receberá novos recursos.</span><span class="sxs-lookup"><span data-stu-id="523d7-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="523d7-113">Conheça os detalhes completos sobre o novo módulo, incluindo como os comandos foram renomeados e os planos de manutenção do AzureRM, no [módulo Az de Introdução ao Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="523d7-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="523d7-114">Se você quiser começar a usar o novo módulo imediatamente, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="523d7-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="523d7-115">A [documentação do AzureRM](/powershell/azure/azurerm) também está disponível.</span><span class="sxs-lookup"><span data-stu-id="523d7-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="523d7-116">Enquanto a documentação do Azure estiver sendo atualizada para refletir os novos nomes de cmdlets do módulo, os artigos ainda poderão usar os comandos do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="523d7-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="523d7-117">Depois de instalar o módulo Az, é recomendável habilitar os aliases de cmdlet do AzureRM com `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="523d7-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="523d7-118">Confira o artigo [migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="523d7-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="523d7-119">Executar ou instalar</span><span class="sxs-lookup"><span data-stu-id="523d7-119">Run or install</span></span>

<span data-ttu-id="523d7-120">Você pode instalar o Azure PowerShell no PowerShell 5.1 ou superior no Windows, no PowerShell Core 6.x e posterior em qualquer plataforma ou executá-lo no Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="523d7-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="523d7-121">Para executar no seu navegador com o Azure Cloud Shell, confira [Início Rápido para PowerShell no Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="523d7-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="523d7-122">Para instalar o Azure PowerShell em seu sistema, confira [Instalar o Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="523d7-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="523d7-123">Para saber mais sobre a versão mais recente do Azure PowerShell, confira as [notas de versão](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="523d7-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="523d7-124">Introdução</span><span class="sxs-lookup"><span data-stu-id="523d7-124">Get Started</span></span>

<span data-ttu-id="523d7-125">Leia o artigo [Introdução ao Azure PowerShell](get-started-azureps.md) para aprender as noções básicas do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="523d7-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="523d7-126">Se não estiver familiarizado com o PowerShell, uma introdução poderá ser útil:</span><span class="sxs-lookup"><span data-stu-id="523d7-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="523d7-127">Instalar o PowerShell</span><span class="sxs-lookup"><span data-stu-id="523d7-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* <span data-ttu-id="523d7-128">[Scripting with PowerShell](/powershell/scripting/powershell-scripting) (Script com o PowerShell)</span><span class="sxs-lookup"><span data-stu-id="523d7-128">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>
* [<span data-ttu-id="523d7-129">Conceitos básicos do PowerShell: (Parte 1) Introdução ao PowerShell</span><span class="sxs-lookup"><span data-stu-id="523d7-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

<span data-ttu-id="523d7-130">Os exemplos a seguir podem ajudar você com alguns usos comuns do Azure:</span><span class="sxs-lookup"><span data-stu-id="523d7-130">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="523d7-131">Máquinas Virtuais do Linux</span><span class="sxs-lookup"><span data-stu-id="523d7-131">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="523d7-132">Máquinas Virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="523d7-132">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="523d7-133">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="523d7-133">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="523d7-134">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="523d7-134">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="523d7-135">Desenvolva suas habilidades com o Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="523d7-135">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="523d7-136">Automatizar tarefas do Azure usando scripts com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="523d7-136">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="523d7-137">Mais aprendizado interativo...</span><span class="sxs-lookup"><span data-stu-id="523d7-137">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="523d7-138">Outros módulos do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="523d7-138">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="523d7-139">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="523d7-139">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="523d7-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="523d7-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="523d7-141">ElasticDB do Azure</span><span class="sxs-lookup"><span data-stu-id="523d7-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
