---
title: Gerenciar assinaturas do Azure com o Azure PowerShell
description: Gerenciar assinaturas do Azure com o Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 96b94ffcb5075764eb5d2dcaec7b13c5933b83da
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239597"
---
# <a name="use-multiple-azure-subscriptions"></a>Usar várias assinaturas do Azure

A maioria dos usuários do Azure terá somente uma assinatura. No entanto, se você fizer parte de mais de uma organização ou se sua organização tiver dividido o acesso a determinados recursos nos agrupamentos, poderá ter várias assinaturas no Azure. A CLI é compatível com a escolha de uma assinatura globalmente e por comando.

Para obter informações detalhadas sobre assinaturas, cobrança e gerenciamento de custos, confira a [documentação sobre cobrança e gerenciamento de custos](/azure/billing/).

## <a name="tenants-users-and-subscriptions"></a>Locatários, usuários e assinaturas

Talvez você tenha alguma confusão sobre a diferença entre locatários, usuários e assinaturas no Azure. Um _locatário_ é a entidade do Azure Active Directory que abrange toda a organização. Esse locatário tem pelo menos uma _assinatura_ e _usuário_. Um usuário é um indivíduo e é associado a somente um locatário: a organização à qual pertence. Os usuários são as contas que se conectam ao Azure para criar, gerenciar e usar recursos.
Um usuário pode ter acesso a várias _assinaturas_, que são contratos com a Microsoft para usar os serviços de nuvem, incluindo o Azure. Cada recurso é associado a uma assinatura.

Para saber mais sobre as diferenças entre locatários, usuários e assinaturas, confira o [dicionário de terminologia de nuvem do Azure](/azure/azure-glossary-cloud-terminology).  Para saber como adicionar uma nova assinatura ao seu locatário do Azure Active Directory, confira [Como associar ou adicionar uma assinatura do Azure ao locatário do Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Para saber como se conectar a um locatário específico, confira [Entrar com o Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Alterar a assinatura ativa

No Azure PowerShell, para acessar os recursos de uma assinatura é preciso alterar a assinatura associada à sessão atual do Azure.
Isso é feito modificando o contexto da sessão ativa, as informações com base nas quais os cmdlets de locatário, a assinatura e o usuário devem ser executados.
Para alterar as assinaturas, primeiro um objeto de contexto do Azure PowerShell precisa ser recuperado com [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e, em seguida, o contexto atual é alterado com [Set-AzContext](/powershell/module/az.accounts/set-azcontext).

O exemplo a seguir mostra como obter uma assinatura no locatário do Active Directory atual e defini-lo como a sessão ativa:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Para saber mais sobre os contextos do Azure PowerShell, incluindo como salvá-los e alternar rapidamente entre eles para trabalhar com várias assinaturas com facilidade, confira [Persistir credenciais com contextos do Azure PowerShell](context-persistence.md).
