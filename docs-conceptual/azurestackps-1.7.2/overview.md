---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037679"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="bde93-103">Módulo do Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="bde93-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="bde93-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="bde93-104">Requirements:</span></span>

<span data-ttu-id="bde93-105">A versão mínima do Azure Stack compatível é a 1904.</span><span class="sxs-lookup"><span data-stu-id="bde93-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="bde93-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="bde93-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="bde93-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="bde93-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="bde93-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="bde93-108">Release Notes</span></span>

* <span data-ttu-id="bde93-109">Compatível com a atualização 1904</span><span class="sxs-lookup"><span data-stu-id="bde93-109">Supported with 1904 update</span></span>
* <span data-ttu-id="bde93-110">Essa é uma versão com alteração de falhas.</span><span class="sxs-lookup"><span data-stu-id="bde93-110">This a breaking change release.</span></span> <span data-ttu-id="bde93-111">Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="bde93-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="bde93-112">Alterações da falha: Alterações de backup do modo de criptografia baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="bde93-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="bde93-113">O suporte para chaves simétricas está preterido.</span><span class="sxs-lookup"><span data-stu-id="bde93-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="bde93-114">Para obter detalhes sobre as alterações de falhas, confira https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="bde93-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="bde93-115">Módulo Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="bde93-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="bde93-116">Correção de bug – Nova Cota de Armazenamento usará os padrões se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="bde93-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
