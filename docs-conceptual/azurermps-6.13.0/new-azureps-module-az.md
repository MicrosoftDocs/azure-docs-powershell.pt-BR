---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828103"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="710fe-103">Apresentação do novo módulo Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="710fe-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="710fe-104">A partir de novembro de 2018, o módulo `Az` do Azure PowerShell estará disponível para visualização pública completa.</span><span class="sxs-lookup"><span data-stu-id="710fe-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="710fe-105">O Az oferece comandos menores, maior estabilidade e dá suporte ao Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="710fe-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="710fe-106">O Az também oferece paridade de recursos e um caminho de migração fácil do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="710fe-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="710fe-107">O Az usa a biblioteca .NET Standard, ou seja, ele é executado no PowerShell 5.x e no PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="710fe-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="710fe-108">Uma vez que o PowerShell 6.x pode ser executado no Linux, macOS e Windows, significa que o Az está disponível para todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="710fe-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="710fe-109">O .NET Standard permite unificar a base de código do Azure PowerShell com impacto mínimo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="710fe-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="710fe-110">O Az é um novo módulo, portanto, a versão foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="710fe-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="710fe-111">A primeira versão estável será a 1.0. No entanto, o módulo terá paridade de recursos com o AzureRm a partir de novembro de 2018.</span><span class="sxs-lookup"><span data-stu-id="710fe-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="710fe-112">Atualizar para o Az</span><span class="sxs-lookup"><span data-stu-id="710fe-112">Upgrade to Az</span></span>

<span data-ttu-id="710fe-113">É recomendável que os usuários atualizem para o novo módulo `Az`.</span><span class="sxs-lookup"><span data-stu-id="710fe-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="710fe-114">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="710fe-114">To do so:</span></span>

* [<span data-ttu-id="710fe-115">Desinstalar o módulo AzureRM do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="710fe-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="710fe-116">Instalar o módulo Az do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="710fe-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="710fe-117">Habilitar o modo de compatibilidade para o AzureRM com `Enable-AzureRMAlias` enquanto você se familiariza com o novo conjunto de comandos.</span><span class="sxs-lookup"><span data-stu-id="710fe-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="710fe-118">Migrar os scripts existentes para o Az</span><span class="sxs-lookup"><span data-stu-id="710fe-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="710fe-119">Atualizações importantes podem ser inconvenientes.</span><span class="sxs-lookup"><span data-stu-id="710fe-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="710fe-120">No entanto, o módulo `Az` tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você trabalha nas atualizações da nova sintaxe.</span><span class="sxs-lookup"><span data-stu-id="710fe-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="710fe-121">Use o cmdlet `Enable-AzureRmAlias` para habilitar o modo de compatibilidade do `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="710fe-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="710fe-122">Esse cmdlet define os nomes de cmdlets `AzureRM` como aliases para os novos nomes de cmdlets `Az`.</span><span class="sxs-lookup"><span data-stu-id="710fe-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="710fe-123">Os novos nomes de cmdlets foram projetados para serem fáceis de aprender.</span><span class="sxs-lookup"><span data-stu-id="710fe-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="710fe-124">Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`.</span><span class="sxs-lookup"><span data-stu-id="710fe-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="710fe-125">Por exemplo, o comando antigo `New-AzureRmVm` tornou-se `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="710fe-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="710fe-126">Para obter uma descrição completa do processo de migração, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="710fe-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="710fe-127">O futuro do suporte do AzureRM</span><span class="sxs-lookup"><span data-stu-id="710fe-127">The future of support for AzureRM</span></span>

<span data-ttu-id="710fe-128">O módulo `AzureRM` existente deixará de receber novos cmdlets ou recursos quando o `Az` versão 1.0 for lançado em dezembro de 2018.</span><span class="sxs-lookup"><span data-stu-id="710fe-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="710fe-129">No entanto, o `AzureRM` ainda será oficialmente mantido e terá correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="710fe-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="710fe-130">Para se manter atualizado com os recursos e serviços do Azure mais recentes, você deve alternar para o módulo `Az`.</span><span class="sxs-lookup"><span data-stu-id="710fe-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>