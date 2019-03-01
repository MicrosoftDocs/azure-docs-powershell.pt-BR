---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837700"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrar do AzureRM para o Az do Azure PowerShell

O módulo Az tem paridade de recursos com o AzureRM, mas usa nomes de cmdlets menores e mais consistentes.
Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo. Para facilitar a transição, o Az oferece ferramentas para permitir a execução de seus scripts existentes usando o AzureRM. A migração para um novo conjunto de comandos nem sempre é conveniente, mas este artigo ajudará você a começar a realizar a transição para o novo módulo.

Para ver a lista completa de alterações recentes entre o AzureRM e o Az, confira o [Guia de migração para o Az 1.0.0](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>Verificar se há versões instaladas do AzureRM

O módulo Az pode ser instalado lado a lado com o módulo do AzureRM, mas isso não é recomendado. Antes de executar qualquer etapa de migração, verifique quais versões do AzureRM estão instaladas em seu sistema. Isso permite que você verifique se os scripts já estão sendo executados na versão mais recente e se você pode ativar os aliases de comando sem desinstalar o AzureRM.

Para verificar qual versão do AzureRM você instalou, execute o comando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Garanta que seus scripts existentes funcionem com a versão mais recente do AzureRM

Essa é a etapa mais importante! Execute seus scripts existentes e certifique-se de que eles funcionam com a versão _mais recente_ do AzureRM (__6.13.1__). Se os scripts não funcionarem, certifique-se de ler o [Guia de migração do AzureRM](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Instalar o módulo Az do Azure PowerShell

A primeira etapa é instalar o módulo Az em sua plataforma. Quando você instala o Az, é recomendável desinstalar o AzureRM. Nas etapas a seguir, você aprenderá como continuar executando seus scripts existentes e habilitar a compatibilidade para os nomes de cmdlet antigos.

Para instalar o módulo Az do Azure PowerShell, siga estas etapas:

* __RECOMENDÁVEL__: [Desinstale o módulo AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Certifique-se de remover _todas_ as versões instaladas do AzureRM, não apenas a versão mais recente.
* [Instale o módulo Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Habilitar o alias de compatibilidade do AzureRM 

> [!IMPORTANT]
>
> Habilite o modo de compatibilidade somente se você tiver desinstalado _todas as_ versões do AzureRM. A ativação do modo de compatibilidade com os cmdlets do AzureRM ainda disponíveis poderá resultar em um comportamento imprevisível. Ignore esta etapa se tiver decidido manter o AzureRM instalado, mas esteja ciente de que os cmdlets do AzureRM usarão os módulos mais antigos e não chamarão cmdlets do Az.

Com o AzureRM desinstalado e seus scripts funcionando com a versão mais recente do AzureRM, a próxima etapa é habilitar o modo de compatibilidade para o módulo Az. A compatibilidade é habilitada com o comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Os aliases permitem a capacidade de usar nomes de cmdlets antigos com o módulo Az instalado. Esses aliases são gravados no perfil do usuário para o escopo escolhido. Se não existir perfis de usuário, um perfil será criado.

> [!WARNING]
>
> Você pode usar outro `-Scope` para este comando, mas isso não é recomendado. Os aliases são gravados no perfil do usuário do escopo escolhido, portanto, mantenha-os habilitados para um escopo o mais limitado possível. Habilitar os aliases em todo o sistema também pode causar problemas para outros usuários que têm o AzureRM instalado em seu escopo local.

Após habilitar o modo de alias, execute seus scripts novamente para confirmar que eles ainda funcionam conforme o esperado. 

## <a name="change-module-imports-and-cmdlet-names"></a>Alterar os nomes de cmdlets e as importações de módulos

Em geral, os nomes de módulos foram alterados para que `AzureRM` e `Azure` tornem-se `Az`, e o mesmo ocorreu com os cmdlets.
Por exemplo, o módulo `AzureRM.Compute` foi renomeado para `Az.Compute`. `New-AzureRMVM` se tornou `New-AzVM`, e `Get-AzureStorageBlob` agora é `Get-AzStorageBlob`.

Há exceções para essa alteração de nomenclatura e você deve estar atento. Alguns módulos foram renomeados ou mesclados em módulos existentes sem que isso afetasse o sufixo de seus cmdlets, além de alterar `AzureRM` ou `Azure` para `Az`. Caso contrário, o sufixo completo do cmdlet foi alterado para refletir o novo nome do módulo.

| Módulo AzureRM | Módulo Az | O sufixo do cmdlet foi alterado? |
|----------------|-----------|------------------------|
| AzureRM.profile | Az.Accounts | Sim |
| AzureRM.Insights | Az.Monitor | Sim |
| AzureRM.DataFactories | Az.DataFactory | Sim |
| AzureRM.DataFactoryV2 | Az.DataFactory | Sim |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | Não  |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | Não  |
| AzureRM.Tags | Az.Resources | Não  |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Não  |
| AzureRM.UsageAggregates | Az.Billing | Não  |
| AzureRM.Consumption | Az.Billing | Não  |

## <a name="summary"></a>Resumo

Seguindo essas etapas, é possível atualizar todos os scripts existentes para usar o novo módulo. Se você tiver dúvidas ou problemas com estas etapas que dificultaram a migração, deixe seu comentário sobre este artigo para que possamos melhorar as instruções.
