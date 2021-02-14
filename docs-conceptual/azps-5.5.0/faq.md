---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100011934"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Perguntas frequentes sobre o Azure PowerShell

## <a name="what-is-azure-powershell"></a>O que é o Azure PowerShell?

O Azure PowerShell é um conjunto de cmdlets que permite gerenciar recursos do Azure diretamente com o PowerShell. Em dezembro de 2018, o módulo Az do PowerShell entrou em disponibilidade geral. Ele agora é o módulo do PowerShell recomendado para interagir com o Azure. Para saber mais sobre o módulo Az do PowerShell, confira [Apresentação do novo módulo Az do Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Como fazer para desabilitar mensagens de aviso de alteração da falha no Azure PowerShell?

Para suprimir as mensagens de aviso de alteração da falha no Azure PowerShell, você precisará definir a variável de ambiente `SuppressAzurePowerShellBreakingChangeWarnings` como `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
