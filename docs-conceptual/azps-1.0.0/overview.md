---
title: Visão geral do Azure PowerShell
description: Uma visão geral do módulo Az do Azure PowerShell, com informações sobre como instalar e começar.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736453"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="f3305-103">Visão geral do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3305-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="f3305-104">O Azure PowerShell fornece um conjunto de cmdlets que usa o modelo do [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) para gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3305-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="f3305-105">O Azure PowerShell usa o .NET Standard, disponibilizando-o para Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="f3305-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="f3305-106">O Azure PowerShell também está disponível no Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="f3305-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="f3305-107">Use o [Azure Cloud Shell](/azure/cloud-shell/overview) para executar o Azure PowerShell em seu navegador ou [instale-o localmente](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f3305-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="f3305-108">Confira o artigo [Introdução](get-started-azureps.md) para conhecer os fundamentos do Azure PowerShell e começar a usar o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3305-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="f3305-109">Para saber mais sobre a versão mais recente do Azure PowerShell, confira as [notas de versão](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f3305-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="f3305-110">Sobre o novo módulo Az</span><span class="sxs-lookup"><span data-stu-id="f3305-110">About the new Az module</span></span>

<span data-ttu-id="f3305-111">Esta documentação descreve o novo módulo Az para o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3305-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="f3305-112">Este novo módulo é escrito desde o início no .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="f3305-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="f3305-113">O uso do .NET Standard permite que o Azure PowerShell seja executado no PowerShell 5.x no Windows ou no PowerShell 6 em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="f3305-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="f3305-114">O módulo Az agora é a maneira pretendida de interagir com o Azure por meio do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3305-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="f3305-115">O AzureRM continuará recebendo correções de bugs, mas já não receberá novos recursos.</span><span class="sxs-lookup"><span data-stu-id="f3305-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="f3305-116">Conheça os detalhes completos sobre o novo módulo, incluindo como os comandos foram renomeados e os planos de manutenção do AzureRM, no [módulo Az de Introdução ao Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="f3305-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="f3305-117">Se você quiser começar a usar o novo módulo imediatamente, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="f3305-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="f3305-118">A [documentação do AzureRM](/powershell/azure/azurerm) também está disponível.</span><span class="sxs-lookup"><span data-stu-id="f3305-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f3305-119">Enquanto a documentação do Azure estiver sendo atualizada para refletir os novos nomes de cmdlets do módulo, os artigos ainda poderão usar os comandos do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="f3305-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="f3305-120">Depois de instalar o módulo Az, é recomendável habilitar os aliases de cmdlet do AzureRM com `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="f3305-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="f3305-121">Confira o artigo [migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="f3305-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="f3305-122">Cenários comuns</span><span class="sxs-lookup"><span data-stu-id="f3305-122">Common scenarios</span></span>

<span data-ttu-id="f3305-123">Os exemplos a seguir podem ajudar você a saber mais sobre como executar cenários comuns com o Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f3305-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="f3305-124">Máquinas Virtuais do Linux</span><span class="sxs-lookup"><span data-stu-id="f3305-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f3305-125">Máquinas Virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="f3305-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f3305-126">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="f3305-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f3305-127">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f3305-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="f3305-128">Saiba mais sobre os conceitos básicos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3305-128">Learn PowerShell basics</span></span>

<span data-ttu-id="f3305-129">Se você estiver familiarizado com o PowerShell, uma introdução poderá ser útil.</span><span class="sxs-lookup"><span data-stu-id="f3305-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="f3305-130">Instalando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3305-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* <span data-ttu-id="f3305-131">[Scripting with PowerShell](/powershell/scripting/powershell-scripting) (Script com o PowerShell)</span><span class="sxs-lookup"><span data-stu-id="f3305-131">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>

<span data-ttu-id="f3305-132">Você também pode assistir a esse vídeo: [Conceitos básicos do PowerShell: (Parte 1) Introdução ao PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="f3305-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="f3305-133">Ou participar da [Introdução ao PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) do Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="f3305-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="f3305-134">Desenvolva suas habilidades com o Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="f3305-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="f3305-135">Automatizar tarefas do Azure usando scripts com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3305-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="f3305-136">Mais aprendizado interativo...</span><span class="sxs-lookup"><span data-stu-id="f3305-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="f3305-137">Outros módulos do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3305-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="f3305-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f3305-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="f3305-139">Proteção de Informações do Azure</span><span class="sxs-lookup"><span data-stu-id="f3305-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="f3305-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f3305-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="f3305-141">ElasticDB do Azure</span><span class="sxs-lookup"><span data-stu-id="f3305-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
