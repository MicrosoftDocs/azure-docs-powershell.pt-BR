---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: 0ee905b741c9f79b4f831bb4ea628f97566b2f1d
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427268"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="b35d5-103">Módulo do Azure Stack 1.8.1</span><span class="sxs-lookup"><span data-stu-id="b35d5-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="b35d5-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="b35d5-104">Requirements:</span></span>

<span data-ttu-id="b35d5-105">A versão mínima do Azure Stack compatível é a 1910.</span><span class="sxs-lookup"><span data-stu-id="b35d5-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="b35d5-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="b35d5-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="b35d5-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="b35d5-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="b35d5-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="b35d5-108">Release Notes</span></span>

* <span data-ttu-id="b35d5-109">Compatível com a atualização 1910</span><span class="sxs-lookup"><span data-stu-id="b35d5-109">Supported with 1910 update</span></span>