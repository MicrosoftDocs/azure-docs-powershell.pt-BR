---
title: Visão geral do Azure PowerShell
description: Uma visão geral do módulo Az do Azure PowerShell, com informações sobre como instalar e começar.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863748"
---
# <a name="overview-of-azure-powershell"></a>Visão geral do Azure PowerShell

O Azure PowerShell fornece um conjunto de cmdlets que usa o modelo do [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) para gerenciar os recursos do Azure. O Azure PowerShell usa o .NET Standard, disponibilizando-o para Windows, macOS e Linux.
O Azure PowerShell também está disponível no Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>Sobre o novo módulo Az

Esta documentação descreve o novo módulo Az para o Azure PowerShell. Este novo módulo é escrito desde o início no .NET Standard. O uso do .NET Standard permite que o Azure PowerShell seja executado no PowerShell 5.1 no Windows ou no PowerShell Core 6.x e posterior em qualquer plataforma. O módulo Az agora é a maneira pretendida de interagir com o Azure por meio do PowerShell.
O AzureRM continuará recebendo correções de bugs, mas já não receberá novos recursos.

Conheça os detalhes completos sobre o novo módulo, incluindo como os comandos foram renomeados e os planos de manutenção do AzureRM, no [módulo Az de Introdução ao Azure PowerShell](new-azureps-module-az.md). Se você quiser começar a usar o novo módulo imediatamente, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).

A [documentação do AzureRM](/powershell/azure/azurerm) também está disponível.

> [!IMPORTANT]
>
> Enquanto a documentação do Azure estiver sendo atualizada para refletir os novos nomes de cmdlets do módulo, os artigos ainda poderão usar os comandos do AzureRM. Depois de instalar o módulo Az, é recomendável habilitar os aliases de cmdlet do AzureRM com `Enable-AzureRmAlias`. Confira o artigo [migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md) para obter mais detalhes.

## <a name="run-or-install"></a>Executar ou instalar

Você pode instalar o Azure PowerShell no PowerShell 5.1 ou superior no Windows, no PowerShell Core 6.x e posterior em qualquer plataforma ou executá-lo no Azure Cloud Shell.

* Para executar no seu navegador com o Azure Cloud Shell, confira [Início Rápido para PowerShell no Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Para instalar o Azure PowerShell em seu sistema, confira [Instalar o Azure PowerShell](install-az-ps.md).

Para saber mais sobre a versão mais recente do Azure PowerShell, confira as [notas de versão](release-notes-azureps.md).

## <a name="get-started"></a>Introdução

Leia o artigo [Introdução ao Azure PowerShell](get-started-azureps.md) para aprender as noções básicas do Azure PowerShell. Se não estiver familiarizado com o PowerShell, uma introdução poderá ser útil:

* [Instalar o PowerShell](/powershell/scripting/install/installing-powershell)
* [Scripting with PowerShell](/powershell/scripting/powershell-scripting) (Script com o PowerShell)
* [Conceitos básicos do PowerShell: (Parte 1) Introdução ao PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

Os exemplos a seguir podem ajudar você com alguns usos comuns do Azure:

* [Máquinas Virtuais do Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Máquinas Virtuais do Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Aplicativos Web](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Bancos de dados SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Desenvolva suas habilidades com o Microsoft Learn

- [Automatizar tarefas do Azure usando scripts com o PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Mais aprendizado interativo...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Outros módulos do Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [ElasticDB do Azure](/powershell/azure/elasticdbjobs/)
