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
ms.openlocfilehash: f9bb71e19ecfe34f2c8646973f7a10526d2e8673
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427914"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="03212-103">Módulo do Azure Stack Hub 2.0.1</span><span class="sxs-lookup"><span data-stu-id="03212-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="03212-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="03212-104">Requirements:</span></span>

<span data-ttu-id="03212-105">A versão mínima do Azure Stack Hub compatível é a 2002.</span><span class="sxs-lookup"><span data-stu-id="03212-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="03212-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="03212-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="03212-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="03212-107">Install</span></span>

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


## <a name="release-notes"></a><span data-ttu-id="03212-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="03212-108">Release Notes</span></span>

* <span data-ttu-id="03212-109">Compatível com a atualização 2002.</span><span class="sxs-lookup"><span data-stu-id="03212-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="03212-110">O Azure Stack Hub 2.0.0 é uma alteração da falha.</span><span class="sxs-lookup"><span data-stu-id="03212-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="03212-111">O módulo usa o módulo Az em vez do AzureRM.</span><span class="sxs-lookup"><span data-stu-id="03212-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="03212-112">Você pode encontrar um guia de migração e uma lista de alterações da falha em [Migrar do AzureRM para o Azure PowerShell Az no Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="03212-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>