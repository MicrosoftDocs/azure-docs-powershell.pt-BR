---
title: Visão geral do Azure PowerShell | Microsoft Docs
description: Visão geral do Azure PowerShell com links para instalação e configuração.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: 5ee8572ccb8e9fc2de11c2253a1815a666e038a7
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736488"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="cadb9-103">Visão geral do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cadb9-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="cadb9-104">O Azure PowerShell fornece um conjunto de cmdlets que usa o modelo do [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) para gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cadb9-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="cadb9-105">Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou você pode instalá-lo em seu computador local e usá-lo em qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cadb9-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="cadb9-106">Use o [Cloud Shell](/azure/cloud-shell/overview) para executar o Azure PowerShell no seu navegador, ou [instale-o](install-azurerm-ps.md) no seu próprio computador.</span><span class="sxs-lookup"><span data-stu-id="cadb9-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="cadb9-107">Em seguida, leia o artigo de [Introdução](get-started-azureps.md) para começar a usá-lo.</span><span class="sxs-lookup"><span data-stu-id="cadb9-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="cadb9-108">Para saber mais sobre a versão mais recente, veja as [notas de versão](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="cadb9-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="cadb9-109">Os exemplos a seguir podem ajudar você a saber mais sobre como executar cenários comuns com o Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cadb9-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="cadb9-110">Máquinas Virtuais do Linux</span><span class="sxs-lookup"><span data-stu-id="cadb9-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="cadb9-111">Máquinas Virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="cadb9-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="cadb9-112">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="cadb9-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="cadb9-113">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cadb9-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="cadb9-114">Saiba mais sobre os conceitos básicos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="cadb9-114">Learn PowerShell basics</span></span>

<span data-ttu-id="cadb9-115">Se você não estiver familiarizado com o PowerShell, uma introdução ao PowerShell poderá ser útil.</span><span class="sxs-lookup"><span data-stu-id="cadb9-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="cadb9-116">Instalando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="cadb9-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* <span data-ttu-id="cadb9-117">[Scripting with PowerShell](/powershell/scripting/scripting-with-windows-powershell) (Script com o PowerShell)</span><span class="sxs-lookup"><span data-stu-id="cadb9-117">[Scripting with PowerShell](/powershell/scripting/scripting-with-windows-powershell)</span></span>

<span data-ttu-id="cadb9-118">Você também pode assistir a esse vídeo: [Conceitos básicos do PowerShell: (Parte 1) Introdução ao PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="cadb9-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="cadb9-119">Ou participar da [Introdução ao PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) do Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="cadb9-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="cadb9-120">Outros módulos do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cadb9-120">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="cadb9-121">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cadb9-121">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="cadb9-122">Proteção de Informações do Azure</span><span class="sxs-lookup"><span data-stu-id="cadb9-122">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="cadb9-123">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="cadb9-123">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="cadb9-124">ElasticDB do Azure</span><span class="sxs-lookup"><span data-stu-id="cadb9-124">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
