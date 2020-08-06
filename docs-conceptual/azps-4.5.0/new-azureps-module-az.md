---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: f051930132c6e1f1979a7cde1f75fd4856f83284
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566030"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Apresentação do novo módulo Az do Azure PowerShell

Desde dezembro de 2018, o módulo Az do Azure PowerShell está em versão geral e é agora o módulo do PowerShell utilizado para interagir com o Azure. O Az oferece comandos menores, maior estabilidade e dá suporte à plataforma cruzada. O Az também tem paridade de recursos com o AzureRM, oferecendo um fácil caminho de migração.

> [!NOTE]
> O PowerShell 7.x e posterior é a versão recomendada do PowerShell para uso com Azure PowerShell em todas as plataformas.

Com o módulo Az mais recente, o Azure PowerShell funciona com o PowerShell 6.2.4 e posterior em todas as plataformas, incluindo Windows, macOS e Linux. Ele também é compatível com o PowerShell 5.1 no Windows.

O Az é um novo módulo, portanto, a versão foi redefinida para 1.0.0.

## <a name="why-a-new-module"></a>Por que um novo módulo?

Atualizações importantes podem ser inconvenientes. Dessa forma, é importante informá-lo por que a decisão de introduzir um novo conjunto de módulos foi tomada, com novos cmdlets para interagir com o Azure por meio do PowerShell.

A maior e mais importante alteração é que o PowerShell tem sido um produto multiplataforma desde a introdução do [PowerShell](/powershell/scripting/overview), com base na biblioteca .NET Standard.
Estamos comprometidos em levar o suporte do Azure a todas as plataformas, o que significa que os módulos do Azure PowerShell precisavam ser atualizados para usarem o .NET Standard e serem compatíveis com o PowerShell Core. Em vez de usar o módulo AzureRM existente e introduzir alterações complexas para adicionar esse suporte, o módulo Az foi criado.

A criação de um módulo também permitiu que nossos engenheiros tornassem consistentes o design e a nomeação de cmdlets e módulos. Todos os módulos agora começam com o prefixo `Az.` e todos os cmdlets usam o formato _Verbo_-`Az`_Substantivo_. Anteriormente, os nomes dos cmdlets não eram só mais longos, mas também continham inconsistências.

O número de módulos também foi reduzido: Alguns módulos que funcionaram com os mesmos serviços foram combinados. Os cmdlets plano de gerenciamento e plano de dados agora estão contidos em módulos únicos para seus serviços. Para aqueles que gerenciam dependências e importações manualmente, isso simplifica muito as tarefas.

Ao fazer essas alterações importantes que precisavam da criação de um módulo do Azure PowerShell, a equipe se comprometeu em tornar o uso do Azure com cmdlets do PowerShell mais fácil do que nunca e em mais plataformas do que o que era possível anteriormente.

## <a name="upgrade-to-az"></a>Atualizar para o Az

Para se manter atualizado com os recursos mais recentes do Azure no PowerShell, você deverá migrar para o módulo Az assim que possível. Caso você não esteja pronto para instalar o módulo Az como uma substituição para o AzureRM, você terá duas opções disponíveis para experimentar o Az:

- Usar um ambiente do `PowerShell` com o [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview). O Azure Cloud Shell é um ambiente de shell baseado em navegador que vem com o módulo Az instalado e aliases de compatibilidade com o `Enable-AzureRM` habilitados.
- Manter o módulo AzureRM instalado com o PowerShell 5.1 para Windows, mas instalar o módulo Az para o PowerShell 6.2.4 ou posterior. O PowerShell 5.1 para Windows e o PowerShell 6.2.4 e posterior usam coleções separadas de módulos. Siga as instruções para instalar a [versão mais recente do PowerShell](/powershell/scripting/install/installing-powershell) e [instale o módulo Az](install-az-ps.md) do PowerShell 6.2.4 ou posterior.

Para atualizar de uma instalação existente do AzureRM:

1. [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Instalar o módulo Az do Azure PowerShell](install-az-ps.md)
3. **OPCIONAL**: Habilite o modo de compatibilidade para adicionar aliases para cmdlets do AzureRM com [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) enquanto você se familiariza com o novo conjunto de comandos. Confira a próxima seção ou [Iniciar uma migração do AzureRM para o Az](migrate-from-azurerm-to-az.md) para obter mais detalhes.

## <a name="migrate-existing-scripts-to-az"></a>Migrar os scripts existentes para o Az

Os novos nomes de cmdlets foram projetados para serem fáceis de aprender. Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`. Por exemplo, o comando antigo `New-AzureRMVm` tornou-se `New-AzVm`.
Apesar disso, a migração é mais do que apenas se familiarizar com os novos nomes de cmdlets. Há módulos e parâmetros renomeados, além de outras alterações importantes.

Temos diversos recursos para ajudar você com o processo de migração do AzureRM para o Az:

- [Introdução à migração do AzureRM para o Az](migrate-from-azurerm-to-az.md)
- [Lista completa das alterações da falha do AzureRM para o Az 1.0.0](migrate-az-1.0.0.md)
- O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

O módulo Az tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você atualiza para a nova sintaxe. O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) habilita um modo de compatibilidade por meio de aliases, para permitir que você use os scripts existentes com modificação mínima enquanto estiver trabalhando para realizar uma migração completa para o Az. Por padrão, `Enable-AzureRmAlias` habilita apenas aliases de compatibilidade para a sessão atual do PowerShell. Use seu parâmetro `Scope` para persistir os aliases de compatibilidade entre as sessões do PowerShell. Para obter mais informações, confira a [documentação de referência de Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Embora os nomes dos cmdlets sejam convertidos em alias, ainda poderá haver parâmetros novos (ou renomeados) ou valores retornados alterados para os cmdlets do Az. Não espere que a habilitação de aliases cuide da migração para você. Confira a [lista completa de alterações da falha](migrate-az-1.0.0.md) para descobrir quando seus scripts podem exigir atualizações.

## <a name="continued-support-for-azurerm"></a>Suporte contínuo para o AzureRM

O AzureRM deixará de receber novos cmdlets ou recursos. No entanto, o módulo AzureRM ainda será oficialmente mantido e terá correções de bugs até dezembro de 2020.
