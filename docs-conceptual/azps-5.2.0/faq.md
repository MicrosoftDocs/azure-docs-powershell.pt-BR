---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856057"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="d34ce-103">Perguntas frequentes sobre o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d34ce-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="d34ce-104">O que é o Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="d34ce-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="d34ce-105">O Azure PowerShell é um conjunto de cmdlets que permite gerenciar recursos do Azure diretamente com o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d34ce-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="d34ce-106">Em dezembro de 2018, o módulo Az do PowerShell entrou em disponibilidade geral.</span><span class="sxs-lookup"><span data-stu-id="d34ce-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="d34ce-107">Ele agora é o módulo do PowerShell recomendado para interagir com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d34ce-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="d34ce-108">Para saber mais sobre o módulo Az do PowerShell, confira [Apresentação do novo módulo Az do Azure PowerShell](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="d34ce-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="d34ce-109">Como fazer para desabilitar mensagens de aviso de alteração da falha no Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="d34ce-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="d34ce-110">Para suprimir as mensagens de aviso de alteração da falha no Azure PowerShell, você precisará definir a variável de ambiente `SuppressAzurePowerShellBreakingChangeWarnings` como `true`.</span><span class="sxs-lookup"><span data-stu-id="d34ce-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
