---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 21d41b6e14d1b39a78e40daee74b80de3a80c2a0
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861258"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Apresentação do novo módulo Az do Azure PowerShell

A partir de dezembro de 2018, o módulo Az do Azure PowerShell foi lançado e é agora o módulo do PowerShell utilizado para interagir com o Azure. O Az oferece comandos menores, maior estabilidade e dá suporte à plataforma cruzada. O Az também tem paridade de recursos com o AzureRM, oferecendo um fácil caminho de migração.

Com o módulo Az, o Azure PowerShell agora é compatível com o PowerShell 5.1 no Windows e com o PowerShell Core 6.x e posterior em todas as plataformas compatíveis – incluindo Windows, macOS e Linux.

O Az é um novo módulo, portanto, a versão foi redefinida para 1.0.0.

## <a name="why-a-new-module"></a>Por que um novo módulo?

Atualizações importantes podem ser inconvenientes. Dessa forma, é importante informá-lo por que a decisão de introduzir um novo conjunto de módulos foi tomada, com novos cmdlets para interagir com o Azure por meio do PowerShell.

A maior e mais importante alteração é que o PowerShell tem sido um produto multiplataforma desde a introdução do [PowerShell Core 6.x](/powershell/scripting/overview), com base na biblioteca .NET Standard.
Estamos comprometidos em levar o suporte do Azure a todas as plataformas, o que significa que os módulos do Azure PowerShell precisavam ser atualizados para usarem o .NET Standard e serem compatíveis com o PowerShell Core. Em vez de usar o módulo AzureRM existente e introduzir alterações complexas para adicionar esse suporte, o módulo Az foi criado.

A criação de um módulo também deu a nossos engenheiros a oportunidade de tornar consistentes o design e a nomeação de cmdlets e módulos. Todos os módulos agora começam com o prefixo `Az.` e todos os cmdlets usam o formato _Verbo_-`Az`_Substantivo_. Anteriormente, os nomes dos cmdlets não eram só mais longos, mas continham inconsistências.

O número de módulos também foi reduzido: Alguns módulos que funcionavam com os mesmos serviços foram revertidos juntos, e os cmdlets do plano de dados e do plano de gerenciamento agora estão contidos em módulos únicos para seus serviços. Para aqueles que gerenciam dependências e importações manualmente, isso simplifica muito as tarefas.

Ao fazer essas alterações importantes que precisavam da criação de um módulo do Azure PowerShell, a equipe se comprometeu em tornar o uso do Azure com cmdlets do PowerShell mais fácil do que nunca e em mais plataformas do que o que era possível anteriormente.

## <a name="upgrade-to-az"></a>Atualizar para o Az

Para se manter atualizado com os recursos mais recentes do Azure no PowerShell, você deverá migrar para o módulo Az assim que possível. Caso você não esteja pronto para instalar o módulo Az como uma substituição para o AzureRM, você terá duas opções disponíveis para experimentar o Az:

* Usar um ambiente do `PowerShell` com o [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview).
  O Azure Cloud Shell é um ambiente de shell baseado em navegador que vem com o módulo Az instalado e aliases de compatibilidade com o `Enable-AzureRM` habilitados.
* Manter o módulo AzureRM instalado com o PowerShell 5.1 para Windows, mas instalar o módulo Az para o PowerShell Core 6.x ou posterior. O PowerShell 5.1 para Windows e o PowerShell Core usam coleções separadas de módulos. Siga as instruções para [instalar o PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) e, em seguida, [instalar o módulo Az](install-az-ps.md) em um terminal do PowerShell Core.

Para atualizar de uma instalação existente do AzureRM:

1. [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Instalar o módulo Az do Azure PowerShell](install-az-ps.md)
3. __OPCIONAL__: Habilite o modo de compatibilidade para adicionar aliases para cmdlets do AzureRM com [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) enquanto você se familiariza com o novo conjunto de comandos. Confira a próxima seção ou [Iniciar uma migração do AzureRM para o Az](migrate-from-azurerm-to-az.md) para obter mais detalhes.

## <a name="migrate-existing-scripts-to-az"></a>Migrar os scripts existentes para o Az

Os novos nomes de cmdlets foram projetados para serem fáceis de aprender. Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`. Por exemplo, o comando antigo `New-AzureRMVm` tornou-se `New-AzVm`.
Apesar disso, a migração é mais do que apenas se familiarizar com os novos nomes de cmdlets: Há módulos e parâmetros renomeados, além de outras alterações importantes.

Para ajudá-lo com o processo de migração do AzureRM para o Az, temos uma série de recursos:

* [Introdução à migração do AzureRM para o Az](migrate-from-azurerm-to-az.md)
* [Lista completa das alterações da falha do AzureRM para o Az 1.0.0](migrate-az-1.0.0.md)
* O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

O módulo Az tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você atualiza para a nova sintaxe. O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) habilita um modo de compatibilidade por meio de aliases, para permitir que você use os scripts existentes com modificação mínima enquanto estiver trabalhando para realizar uma migração completa para o Az.

> [!IMPORTANT]
> Embora os nomes dos cmdlets sejam convertidos em alias, ainda poderá haver parâmetros novos (ou renomeados) ou valores retornados alterados para os cmdlets do Az. Não espere que a habilitação de aliases cuide da migração para você. Confira a [lista completa de alterações da falha](migrate-az-1.0.0.md) para descobrir quando seus scripts podem exigir atualizações.

## <a name="continued-support-for-azurerm"></a>Suporte contínuo para o AzureRM

O AzureRM deixará de receber novos cmdlets ou recursos. No entanto, o módulo AzureRM ainda será oficialmente mantido e terá correções de bugs até dezembro de 2020.