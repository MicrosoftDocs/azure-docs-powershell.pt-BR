---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048692"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="ba2c0-103">Apresentação do novo módulo Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba2c0-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="ba2c0-104">A partir de dezembro de 2018, o módulo Az do Azure PowerShell foi lançado e é agora o módulo do PowerShell utilizado para interagir com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="ba2c0-105">O Az oferece comandos menores, maior estabilidade e dá suporte à plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="ba2c0-106">O Az também oferece paridade de recursos e um caminho de migração fácil do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="ba2c0-107">O Az usa a biblioteca .NET Standard, ou seja, ele é executado no PowerShell 5 e no PowerShell 6.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="ba2c0-108">Como o PowerShell 6 pode ser executado no Linux, macOS e Windows, o Azure PowerShell agora está disponível para todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="ba2c0-109">O .NET Standard permite unificar a base de código do Azure PowerShell com impacto mínimo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="ba2c0-110">O Az é um novo módulo, portanto, a versão foi redefinida para 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="ba2c0-111">Atualizar para o Az</span><span class="sxs-lookup"><span data-stu-id="ba2c0-111">Upgrade to Az</span></span>

<span data-ttu-id="ba2c0-112">É recomendável que todos os usuários atualizem para o novo módulo Az.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="ba2c0-113">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="ba2c0-113">To do so:</span></span>

* <span data-ttu-id="ba2c0-114">__RECOMENDÁVEL__: [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="ba2c0-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="ba2c0-115">Instalar o módulo Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba2c0-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="ba2c0-116">Habilitar o modo de compatibilidade para adicionar aliases para cmdlets AzureRM com `Enable-AzureRMAlias` enquanto você se familiariza com o novo conjunto de comandos.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="ba2c0-117">Habilite __apenas__ os aliases se você não tiver o AzureRM instalado.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="ba2c0-118">Migrar os scripts existentes para o Az</span><span class="sxs-lookup"><span data-stu-id="ba2c0-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="ba2c0-119">Atualizações importantes podem ser inconvenientes.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="ba2c0-120">No entanto, o módulo Az tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você trabalha nas atualizações da nova sintaxe.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="ba2c0-121">Use o cmdlet `Enable-AzureRmAlias` para habilitar o modo de compatibilidade do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="ba2c0-122">Esse cmdlet define os nomes de cmdlets AzureRM como aliases para os novos nomes de cmdlets Az.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="ba2c0-123">Os novos nomes de cmdlets foram projetados para serem fáceis de aprender.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="ba2c0-124">Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="ba2c0-125">Por exemplo, o comando antigo `New-AzureRMVm` tornou-se `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="ba2c0-126">Para obter uma descrição completa do processo de migração, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="ba2c0-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="ba2c0-127">O futuro do suporte do AzureRM</span><span class="sxs-lookup"><span data-stu-id="ba2c0-127">The future of support for AzureRM</span></span>

<span data-ttu-id="ba2c0-128">O módulo AzureRM existente deixará de receber novos cmdlets ou recursos.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="ba2c0-129">No entanto, o AzureRM ainda será oficialmente mantido e terá correções de bugs até dezembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="ba2c0-130">Para se manter atualizado com os recursos e serviços do Azure mais recentes, você deve trocar para o módulo Az.</span><span class="sxs-lookup"><span data-stu-id="ba2c0-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>