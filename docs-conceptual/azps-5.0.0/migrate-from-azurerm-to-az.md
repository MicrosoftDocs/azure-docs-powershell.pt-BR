---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753330"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="c3d4e-103">Migrar o Azure PowerShell do AzureRM para o Az</span><span class="sxs-lookup"><span data-stu-id="c3d4e-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="c3d4e-104">Todas as versões do módulo AzureRM PowerShell estão desatualizadas, mas o suporte continua.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="c3d4e-105">Agora, o [módulo Az PowerShell](install-az-ps.md) é o módulo do PowerShell recomendado para interagir com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="c3d4e-106">Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="c3d4e-107">Para facilitar a transição, foi desenvolvido o [kit de ferramentas de migração do AzureRM para o Az](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="c3d4e-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="c3d4e-108">Nenhuma migração para um novo conjunto de comandos é conveniente, mas este artigo ajudará você a começar a realizar a transição para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="c3d4e-109">Para saber mais sobre o módulo Az do PowerShell, confira [Introdução do novo módulo Az do Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="c3d4e-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="c3d4e-110">Para ver a lista completa de alterações da falha entre o AzureRM e o Az, confira as [alterações completas do AzureRM para o Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="c3d4e-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="c3d4e-111">Verifique se os scripts existentes funcionam com a última versão do AzureRM</span><span class="sxs-lookup"><span data-stu-id="c3d4e-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="c3d4e-112">Antes de executar qualquer etapa de migração, verifique quais versões do AzureRM estão instaladas em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="c3d4e-113">Esse procedimento permite que você verifique se os scripts já estão em execução na última versão e se você sabe quais versões do AzureRM precisam ser desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="c3d4e-114">Para verificar qual versão do AzureRM você instalou, execute o seguinte exemplo:</span><span class="sxs-lookup"><span data-stu-id="c3d4e-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="c3d4e-115">A **última** versão disponível do AzureRM é a **6.13.1** .</span><span class="sxs-lookup"><span data-stu-id="c3d4e-115">The **latest** available release of AzureRM is **6.13.1** .</span></span> <span data-ttu-id="c3d4e-116">Se você não tiver essa versão instalada, os scripts existentes poderão precisar de modificação adicional para funcionar com o módulo Az, além do que foi descrito neste artigo e na [lista de alterações da falha](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="c3d4e-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="c3d4e-117">Se os scripts não funcionarem com o AzureRM 6.13.1, atualize-os de acordo com o [guia de migração do AzureRM 5.x para o 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="c3d4e-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="c3d4e-118">Se você usar uma versão anterior do módulo AzureRM, haverá guias de migração disponíveis para cada versão principal.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="c3d4e-119">Instalar o kit de ferramentas de migração do AzureRM para o Az</span><span class="sxs-lookup"><span data-stu-id="c3d4e-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="c3d4e-120">Migrar automaticamente os scripts do PowerShell</span><span class="sxs-lookup"><span data-stu-id="c3d4e-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="c3d4e-121">Com o kit de ferramentas de migração do AzureRM para o Az, você poderá gerar um plano para determinar quais alterações serão executadas nos scripts antes de fazer qualquer modificação neles e antes de instalar o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="c3d4e-122">O início rápido [Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) orienta você ao longo do processo inteiro de atualização automática dos scripts do PowerShell do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3d4e-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c3d4e-123">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c3d4e-123">Next steps</span></span>

<span data-ttu-id="c3d4e-124">[Instalar o Azure PowerShell](install-az-ps.md)
[Desinstalar o AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="c3d4e-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
