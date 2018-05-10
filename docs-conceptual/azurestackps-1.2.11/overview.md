---
title: Visão geral do Azure Stack PowerShell | Microsoft Docs
description: Visão geral da instalação e configuração do Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

O Azure Stack requer os dois módulos do PowerShell a seguir:  

1. Módulo do **AzureRM** compatível com o Azure Stack que está disponível com a instalação do Perfil da Versão da API **2017-03-09-profile**. Os cmdlets instalados usando esse perfil podem ser usados pelos operadores e usuários do Azure Stack.

2. A versão mais atual é a instalação **1.2.11** do módulo do **AzureStack**. Os cmdlets instalados usando esse módulo podem ser usados apenas pelos operadores do Azure Stack. Os operadores podem executar operações como gerenciar ofertas, planos, serviços, cotas etc., usando os cmdlets do PowerShell fornecidos por esse módulo. Para saber mais sobre os cmdlets do PowerShell disponíveis neste módulo, consulte o conteúdo de referência do [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) e [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).

## <a name="next-steps"></a>Próximas etapas

* [Instalar o PowerShell para o Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [Configurar o PowerShell para usar com o Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
