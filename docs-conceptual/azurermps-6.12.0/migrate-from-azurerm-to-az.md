---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574406"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrar do AzureRM para o Az do Azure PowerShell

O módulo Az tem paridade de recursos com o AzureRM, mas usa nomes de cmdlets menores e mais consistentes.
Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo. Para facilitar a transição, o Az oferece ferramentas para permitir a execução de seus scripts existentes usando o AzureRM. A migração para um novo conjunto de comandos nem sempre é conveniente, mas este artigo ajudará você a começar a realizar a transição para o novo módulo.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Garanta que seus scripts existentes funcionem com a versão mais recente do AzureRM

Essa é a etapa mais importante! Execute seus scripts existentes e certifique-se de que eles funcionam com a versão _mais recente_ do AzureRM (__6.12.0__). Se os scripts não funcionarem, certifique-se de ler o [Guia de migração do AzureRM](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Instalar o módulo Az do Azure PowerShell

A primeira etapa é instalar o módulo Az em sua plataforma. Para instalar o Az, você precisa desinstalar o AzureRM.
Nas etapas a seguir, você aprenderá como continuar executando seus scripts existentes e habilitar a compatibilidade para os nomes de cmdlet antigos.

Para instalar o módulo Az do Azure PowerShell, siga estas etapas:

* [Desinstale o módulo AzureRM](uninstall-azurerm-ps.md). Certifique-se de remover _todas_ as versões instaladas do AzureRM, não apenas a versão mais recente.
* [Instale o módulo Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Habilite o modo de alias do AzureRM

Com o AzureRM desinstalado e seus scripts funcionando com a versão mais recente do AzureRM, chegou o momento de habilitar o modo de compatibilidade para o módulo Az. A compatibilidade é habilitada com o comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Os aliases permitem a capacidade de usar nomes de cmdlets antigos com o módulo `Az` instalado. Esses aliases são gravados no perfil do usuário para o escopo escolhido. Se não existir perfis de usuário, um perfil será criado.

> [!WARNING]
>
> Você pode usar outro `-Scope` para este comando, mas isso não é recomendado! Os aliases são gravados no perfil do usuário do escopo escolhido, portanto, mantenha-os habilitados para um escopo o mais limitado possível. Habilitar os aliases em todo o sistema também pode causar problemas para outros usuários que têm o `AzureRM` instalado em seu escopo local.

Após habilitar o modo de alias, execute seus scripts novamente para confirmar que eles ainda funcionam conforme o esperado. 

## <a name="change-module-imports-and-cmdlet-names"></a>Alterar os nomes de cmdlets e as importações de módulos

Em geral, os nomes de módulos foram alterados para que `AzureRM` e `Azure` tornem-se `Az`, e o mesmo ocorreu com os cmdlets.
Por exemplo, o módulo `AzureRM.Compute` foi renomeado para `Az.Compute`. `New-AzureRmVM` se tornou `New-AzVM`, e `Get-AzureStorageBlob` agora é `Get-AzStorageBlob`.

Há exceções para essa alteração de nomenclatura e você deve estar atento antes de fazer qualquer renomeação:

| Módulo AzureRM | Módulo Az |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Resumo

Seguindo essas etapas, é possível atualizar todos os scripts existentes para usar o novo módulo. Se você tiver dúvidas ou problemas com estas etapas que dificultaram a migração, deixe seu comentário sobre este artigo para que possamos melhorar as instruções.