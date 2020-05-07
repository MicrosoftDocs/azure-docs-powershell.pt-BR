---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053308"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="c10c1-103">Módulo do Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="c10c1-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c10c1-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="c10c1-104">Requirements:</span></span>
<span data-ttu-id="c10c1-105">A versão mínima do Azure Stack com suporte é 1811.</span><span class="sxs-lookup"><span data-stu-id="c10c1-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="c10c1-106">Observação: Se você estiver usando uma versão anterior, instale a versão 1.6.0</span><span class="sxs-lookup"><span data-stu-id="c10c1-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="c10c1-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="c10c1-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="c10c1-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="c10c1-108">Release Notes</span></span>
* <span data-ttu-id="c10c1-109">Com suporte com a atualização 1811</span><span class="sxs-lookup"><span data-stu-id="c10c1-109">Supported with 1811 update</span></span>
* <span data-ttu-id="c10c1-110">Módulo Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="c10c1-111">Correção do prefixo Azs ausente para New-DataDiskObject e adição de alias com aviso de reprovação futura.</span><span class="sxs-lookup"><span data-stu-id="c10c1-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="c10c1-112">Módulo Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="c10c1-113">Adição de um aviso para recomendar a execução do Test-AzureStack antes do Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="c10c1-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="c10c1-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="c10c1-115">Novo cmdlet (o Azure Stack 1811 ou superior tem suporte para os recursos)</span><span class="sxs-lookup"><span data-stu-id="c10c1-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="c10c1-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="c10c1-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="c10c1-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="c10c1-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="c10c1-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c10c1-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="c10c1-119">Reprovação</span><span class="sxs-lookup"><span data-stu-id="c10c1-119">Deprecation</span></span>
        * <span data-ttu-id="c10c1-120">Agora Get-AzsInfrastructureVolume é um alias para o cmdlet Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="c10c1-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="c10c1-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="c10c1-122">Adição de um novo cmdlet Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c10c1-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="c10c1-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="c10c1-124">Correção de bug onde não estão sendo usados valores de cota padrão</span><span class="sxs-lookup"><span data-stu-id="c10c1-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="c10c1-125">Módulo Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="c10c1-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="c10c1-126">Correção do prefixo Azs ausente para New-AddonPlanDefinitionObject e adição de alias com aviso de reprovação futura.</span><span class="sxs-lookup"><span data-stu-id="c10c1-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
