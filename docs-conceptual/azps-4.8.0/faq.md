---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001659"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Perguntas frequentes sobre o Azure PowerShell

## <a name="what-is-azure-powershell"></a>O que é o Azure PowerShell?

O Azure PowerShell é um conjunto de cmdlets que permite gerenciar recursos do Azure diretamente com o PowerShell. Em dezembro de 2018, o módulo Az do PowerShell entrou em disponibilidade geral. Ele agora é o módulo do PowerShell recomendado para interagir com o Azure. Para saber mais sobre o módulo Az do PowerShell, confira [Apresentação do novo módulo Az do Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Como fazer para desabilitar mensagens de aviso de alteração da falha no Azure PowerShell?

Para suprimir as mensagens de aviso de alteração da falha no Azure PowerShell, você precisará definir a variável de ambiente `SuppressAzurePowerShellBreakingChangeWarnings` como `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```