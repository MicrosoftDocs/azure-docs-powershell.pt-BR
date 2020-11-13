---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a0a6fcbc0a7bdae507ff5e16dd844e8425c929d5
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410359"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrar o Azure PowerShell do AzureRM para o Az

O módulo Az tem paridade de recursos com o AzureRM, mas usa nomes de cmdlets menores e mais consistentes.
Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo. Para facilitar a transição, o Az oferece ferramentas para permitir a execução de seus scripts existentes usando o AzureRM. A migração para um novo conjunto de comandos nem sempre é conveniente, mas este artigo ajudará você a começar a realizar a transição para o novo módulo.

Para ver a lista completa de alterações da falha entre o AzureRM e o Az, confira as [alterações completas do AzureRM para o Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verifique se os scripts existentes funcionam com a última versão do AzureRM

Antes de executar qualquer etapa de migração, verifique quais versões do AzureRM estão instaladas em seu sistema. Esse procedimento permite que você verifique se os scripts já estão em execução na última versão e se você sabe quais versões do AzureRM precisam ser desinstaladas.

Para verificar qual versão do AzureRM você instalou, execute o comando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

A __última__ versão disponível do AzureRM é a __6.13.1__. Se você não tiver essa versão instalada, os scripts existentes poderão precisar de modificação adicional para trabalhar com o módulo Az, além do que foi descrito aqui e na [lista de alterações da falha](migrate-az-1.0.0.md).

Se os scripts não funcionarem com o AzureRM 6.13.1, atualize-os de acordo com o [guia de migração do AzureRM 5.x para o 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Se você usar uma versão anterior do módulo AzureRM, haverá guias de migração disponíveis para cada versão principal.

## <a name="uninstall-azurerm"></a>Desinstalar o AzureRM

Não há nenhuma garantia de que o módulo Az seja compatível com as instalações existentes do AzureRM no PowerShell 5.1 para Windows. Antes de instalar o módulo Az, [desinstale o AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Se não estiver pronto para remover o módulo AzureRM do sistema, instale o módulo Az para o [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x ou posterior. O PowerShell Core e o PowerShell 5.1 para Windows usam bibliotecas de módulo diferentes e, portanto, não haverá nenhum conflito. Você ainda poderá [habilitar aliases](#enable-azurerm-compatibility-aliases) no PowerShell Core.

## <a name="install-the-azure-powershell-az-module"></a>Instalar o módulo Az do Azure PowerShell

A primeira etapa é instalar o módulo Az em sua plataforma. Quando você instala o Az, é recomendável desinstalar o AzureRM. Nas etapas a seguir, você aprenderá como continuar executando seus scripts existentes e habilitar a compatibilidade para os nomes de cmdlet antigos.

Para instalar o módulo Az do Azure PowerShell, siga as instruções descritas em [Instalar o módulo Az](install-az-ps.md).

> [!NOTE]
> Nesta altura, o ideal é executar o cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) fornecido no módulo Az, apenas para ter certeza de que todas as versões do AzureRM foram desinstaladas e não causarão conflitos.

## <a name="enable-azurerm-compatibility-aliases"></a>Habilitar aliases de compatibilidade do AzureRM

Com o AzureRM desinstalado e seus scripts funcionando com a versão mais recente do AzureRM, a próxima etapa é habilitar o modo de compatibilidade para o módulo Az. A compatibilidade é habilitada com o comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Os aliases permitem a capacidade de usar nomes de cmdlets antigos com o módulo Az instalado. Esses aliases são gravados no perfil do escopo selecionado. Se não existir nenhum perfil, um perfil será criado.
Ao usar um `-Scope` mais abrangente que `CurrentUser`, as permissões apropriadas serão necessárias para criar ou atualizar o arquivo de perfil correspondente.

> [!IMPORTANT]
> __Somente__ os nomes dos cmdlets são convertidos em alias – os nomes dos módulos não. Se você estiver usando `#Requires`, `Import-Module`, listas de dependência em um `.psd1` ou nomes de cmdlets totalmente qualificados, migre-os neste momento seguindo o processo descrito na [lista de alterações da falha](migrate-az-1.0.0.md) referente a nomes de módulos.

> [!WARNING]
>
> Você pode usar outro `-Scope` para este comando, mas isso não é recomendado. Os aliases são gravados no perfil do usuário do escopo escolhido, portanto, mantenha-os habilitados para um escopo o mais limitado possível. A habilitação de aliases em todo o sistema pode causar problemas para outros usuários que têm o AzureRM instalado em seu escopo local.

Após habilitar o modo de alias, execute seus scripts novamente para confirmar que eles ainda funcionam conforme o esperado.
Alguns nomes de parâmetros foram alterados, adicionados ou se tornaram obrigatórios para o módulo Az. Os tipos de saída dos cmdlets também podem ter sido alterados. Essas alterações são detalhadas na [lista de alterações da falha](migrate-az-1.0.0.md).

## <a name="update-cmdlets-modules-and-parameters"></a>Atualizar cmdlets, módulos e parâmetros

Com os scripts atualizados e em execução com aliases, você pode aproveitar seu tempo para atualizá-los para usar os novos cmdlets e aproveitar outras alterações, como novos recursos. Para a maioria dos scripts, você só precisará atualizar os nomes dos cmdlets [seguindo o novo esquema de nomeação de cmdlets do Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). Também poderá haver outras alterações que você precise fazer para que os scripts funcionem, dependendo do que eles fazem e de quais recursos do Azure PowerShell eles utilizam.

Por exemplo, os [cmdlets do Armazenamento de Blobs](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) foram completamente reformulados para usar um novo modelo assíncrono, de modo que os scripts que os utilizarem exigirão mais trabalho para serem atualizados do que aqueles em que apenas as alterações relevantes foram nomes dos cmdlets.

Mesmo que você precise fazer apenas pequenas alterações simples nos scripts até este ponto – ou que eles funcionam mesmo sem modificações adicionais quando os aliases são habilitados, leia a [lista completa das alterações da falha no Az 1.0.0](migrate-az-1.0.0.md) para verificar se você não depende do comportamento 'transparente' de aliases, que poderá desaparecer após a alteração dos nomes dos cmdlets e a desabilitação de aliases.

## <a name="disable-aliases"></a>Desabilitar aliases

Depois que você concluir a migração e não depender mais do comportamento de nome alternativo, será recomendável que você desabilite os aliases. Isso é feito com o cmdlet [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Ao executar esse cmdlet __lembre-se__ de invocá-lo para cada `-Scope` para o qual `Enable-AzureRmAlias` foi invocado; caso contrário, ainda poderá haver scripts no sistema dependentes do comportamento de nome alternativo.
