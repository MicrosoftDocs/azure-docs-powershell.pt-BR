---
title: Introdução do módulo Az PowerShell do Azure
description: Introdução do módulo Az PowerShell, recomendado para interagir com o Azure e como substituição para o módulo AzureRM PowerShell.
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b52b6995fb50a6ce502d42e7df588ca72340a1e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872202"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Introdução do módulo Az PowerShell do Azure

## <a name="overview"></a>Visão geral

O módulo Az PowerShell é um conjunto de cmdlets para gerenciar recursos do Azure diretamente do PowerShell. O PowerShell fornece recursos avançados para automação que podem ser aproveitados para gerenciar os recursos do Azure a fim de obter exemplos no contexto de um pipeline de CI/CD.

O módulo Az PowerShell é a substituição do AzureRM e é a versão recomendada a ser usada para interagir com o Azure.

Você pode usar o módulo Az PowerShell com um dos seguintes métodos:

* [Instalar o módulo Az PowerShell por meio do PowerShellGet](install-az-ps.md) (opção recomendada).
* [Instalar o módulo Az PowerShell com MSI](install-az-ps-msi.md).
* [Usar o Azure Cloud Shell](/azure/cloud-shell/overview).
* [Usar o contêiner do Docker do Az PowerShell](azureps-in-docker.md).

## <a name="features"></a>Recursos

O módulo Az PowerShell apresenta os seguintes benefícios:

* Segurança e estabilidade
  * Criptografia de cache de token
  * Prevenção de ataque do tipo man-in-the-middle
  * Suporte à autenticação com o ADFS 2019
  * Autenticação de nome de usuário e senha no PowerShell 7
  * Suporte para recursos como avaliação contínua de acesso (chegando em 2021)
* Suporte para todos os serviços do Azure
  * Todos os serviços do Azure em disponibilidade geral têm um módulo PowerShell correspondente com suporte
  * Várias correções de bug e atualizações de versão de API desde o AzureRM
* Novos recursos
  * Suporte no Cloud Shell e em multiplataforma
  * Pode obter e usar o token de acesso para acessar recursos do Azure
  * Cmdlet disponível para operações REST avançadas com recursos do Azure

> [!NOTE]
> O PowerShell 7 e posterior é a versão recomendada do PowerShell para uso com o Az PowerShell em todas as plataformas.

O módulo Az PowerShell é baseado na biblioteca de .NET Standard e funciona com o PowerShell 7 e posterior em todas as plataformas, incluindo Windows, macOS e Linux. Também é compatível com o Windows PowerShell 5.1.

Estamos comprometidos em oferecer o suporte do Azure em todas as plataformas e todos os módulos Az PowerShell são multiplataforma.

## <a name="upgrade-your-environment-to-az"></a>Atualizar o ambiente para o Az

Para se manter atualizado com os recursos mais recentes do Azure no PowerShell, você deverá migrar para o módulo Az. Caso você não esteja pronto para instalar o módulo Az como uma substituição para o AzureRM, você terá duas opções disponíveis para experimentar o Az:

* Usar um ambiente do `PowerShell` com o [Azure Cloud Shell](/azure/cloud-shell/overview). O Azure Cloud Shell é um ambiente de shell baseado em navegador que vem com o módulo Az instalado e aliases de compatibilidade com o `Enable-AzureRM` habilitados.
* Mantenha o módulo AzureRM instalado no Windows PowerShell 5.1 e instale o módulo Az no PowerShell 7 ou posterior. O Windows PowerShell 5.1, o Windows PowerShell 7 e as versões posteriores usam coleções separadas de módulos. Siga as instruções para instalar a [última versão do PowerShell](/powershell/scripting/install/installing-powershell) e [instale o módulo Az](install-az-ps.md) do PowerShell 7 ou posterior.

Para atualizar de uma instalação existente do AzureRM:

1. [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Instalar o módulo Az do Azure PowerShell](install-az-ps.md)
1. **OPCIONAL**: Habilite o modo de compatibilidade para adicionar aliases para cmdlets do AzureRM com [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) enquanto você se familiariza com o novo conjunto de comandos. Para obter mais informações, confira a próxima seção ou [Inicie a migração do AzureRM para o Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Migrar os scripts existentes do AzureRM para o Az

Se os scripts ainda estiverem baseados no módulo AzureRM, temos vários recursos para ajudar você na migração:

* [Introdução à migração do AzureRM para o Az](migrate-from-azurerm-to-az.md)
* [Lista completa das alterações da falha do AzureRM para o Az 1.0.0](migrate-az-1.0.0.md)
* O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Capacidade de suporte

O Az é o módulo do PowerShell mais atual para o Azure. Problemas ou solicitações de recursos podem ser registrados diretamente no [repositório do GitHub](https://github.com/Azure/azure-powershell) ou por meio do suporte da Microsoft se você tiver um contrato de suporte. As solicitações de recursos serão implementadas na última versão do Az. Problemas críticos serão implementados nas duas últimas versões do Az.

Como os módulos do AZ PowerShell agora têm todas as funcionalidades dos módulos do AzureRM PowerShell e muito mais, vamos desativar os módulos do AzureRM PowerShell em 29 de fevereiro de 2024.

Para evitar interrupções de serviço, [atualize seus scripts](https://aka.ms/azpsmigrate) que usam módulos do AzureRM PowerShell para usar módulos do AZ PowerShell em 29 de fevereiro de 2024. Para atualizar seus scripts automaticamente, siga o [guia de início rápido](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).

## <a name="data-collection"></a>Coleta de dados

O Azure PowerShell coleta dados telemétricos por padrão. A Microsoft agrega dados coletados não só para identificar padrões de uso e problemas comuns, mas também para aprimorar a experiência do Azure PowerShell.
O Microsoft Azure PowerShell não coleta dados privados ou pessoais. Por exemplo, os dados de uso ajudam a identificar problemas – como cmdlets com baixo índice de sucesso – e a priorizar o trabalho.

Embora apreciemos os insights fornecidos por esses dados, também entendemos que nem todos desejam enviar dados de uso. Você pode desabilitar a coleta de dados com o cmdlet [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection). Você também pode ler a nossa [política de privacidade](https://privacy.microsoft.com/privacystatement) para saber mais.
