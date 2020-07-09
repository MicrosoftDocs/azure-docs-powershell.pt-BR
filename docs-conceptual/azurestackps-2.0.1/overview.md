---
title: Visão geral do Azure Stack Hub Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Hub Admin PowerShell com instruções de instalação e de configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: 860a32d120e203093038130a535e8b6801e2bce2
ms.sourcegitcommit: 7b368a9be1cea2ac4e7d269e1a51529271269a42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2020
ms.locfileid: "86098817"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="549ee-103">Módulo do Azure Stack Hub 2.0.1</span><span class="sxs-lookup"><span data-stu-id="549ee-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="549ee-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="549ee-104">Requirements:</span></span>

<span data-ttu-id="549ee-105">A versão mínima do Azure Stack Hub compatível é a 2002.</span><span class="sxs-lookup"><span data-stu-id="549ee-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="549ee-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="549ee-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="549ee-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="549ee-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="549ee-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="549ee-108">Release Notes</span></span>

* <span data-ttu-id="549ee-109">Compatível com a atualização 2002.</span><span class="sxs-lookup"><span data-stu-id="549ee-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="549ee-110">O Azure Stack Hub 2.0.0 é uma alteração da falha.</span><span class="sxs-lookup"><span data-stu-id="549ee-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="549ee-111">O módulo usa o módulo Az em vez do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="549ee-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="549ee-112">Você pode encontrar um guia de migração e uma lista de alterações da falha em [Migrar do AzureRM para o Azure PowerShell Az no Azure Stack Hub](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="549ee-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
