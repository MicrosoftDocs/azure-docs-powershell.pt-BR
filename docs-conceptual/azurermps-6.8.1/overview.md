---
title: Visão geral do Azure PowerShell | Microsoft Docs
description: Visão geral do Azure PowerShell com links para instalação e configuração.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: fcb6213dab12f94796ab0ca9de4d5e391d570f4f
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304124"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="d4f93-103">Visão geral do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4f93-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="d4f93-104">O Azure PowerShell fornece um conjunto de cmdlets que usa o modelo do [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) para gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f93-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="d4f93-105">Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou você pode instalá-lo em seu computador local e usá-lo em qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4f93-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="d4f93-106">Use o [Cloud Shell](/azure/cloud-shell/overview) para executar o Azure PowerShell no seu navegador, ou [instale-o](install-azurerm-ps.md) no seu próprio computador.</span><span class="sxs-lookup"><span data-stu-id="d4f93-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="d4f93-107">Em seguida, leia o artigo de [Introdução](get-started-azureps.md) para começar a usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d4f93-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="d4f93-108">Para saber mais sobre a versão mais recente, veja as [notas de versão](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d4f93-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="d4f93-109">Os exemplos a seguir podem ajudar você a saber mais sobre como executar cenários comuns com o Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d4f93-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="d4f93-110">Máquinas Virtuais do Linux</span><span class="sxs-lookup"><span data-stu-id="d4f93-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d4f93-111">Máquinas Virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="d4f93-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d4f93-112">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="d4f93-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d4f93-113">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d4f93-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="d4f93-114">Se você tiver implantações que usam o modelo de implantação clássico que não pode ser convertido, será possível instalar a versão de Gerenciamento de Serviços do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4f93-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="d4f93-115">Para obter mais informações, veja [Instalar o módulo Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="d4f93-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="d4f93-116">Saiba mais sobre os conceitos básicos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4f93-116">Learn PowerShell basics</span></span>

<span data-ttu-id="d4f93-117">Se você não estiver familiarizado com o PowerShell, uma introdução ao PowerShell poderá ser útil.</span><span class="sxs-lookup"><span data-stu-id="d4f93-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="d4f93-118">Instalando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4f93-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* <span data-ttu-id="d4f93-119">[Scripting with PowerShell](/powershell/scripting/powershell-scripting) (Script com o PowerShell)</span><span class="sxs-lookup"><span data-stu-id="d4f93-119">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>

<span data-ttu-id="d4f93-120">Você também pode assistir a este vídeo: [Noções básicas do PowerShell: (Parte 1) Introdução ao PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="d4f93-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="d4f93-121">Ou participar da [Introdução ao PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) do Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="d4f93-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="d4f93-122">Outros módulos do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4f93-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="d4f93-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d4f93-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="d4f93-124">Proteção de Informações do Azure</span><span class="sxs-lookup"><span data-stu-id="d4f93-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="d4f93-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d4f93-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="d4f93-126">ElasticDB do Azure</span><span class="sxs-lookup"><span data-stu-id="d4f93-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
