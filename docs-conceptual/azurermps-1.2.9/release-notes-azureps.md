---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

## <a name="version-129"></a>Versão 1.2.9

Alterações nesta Versão

* Módulo AzureRm.AzureStackAdmin
    + Alterações no cmdlet Add-AzureRmResourceProviderRegistration para o suporte do Azure Resource Manager de Administração e divisão do Azure Resource Manager. Um novo parâmetro -ResourceManagerType foi adicionado.
    + Remoção dos parâmetros -AdminUri, -ApiVersion, -SubscriptionId e -Token de cada cmdlet. Estivemos imprimindo avisos de que esses parâmetros seriam substituídos e agora eles foram removidos.
* Módulo AzureStackStorage
    + Novos cmdlets adicionados para oferecer suporte aos cenários de migração do contêiner.
    + Cmdlets removidos referindo-se aos componentes internos e aos recursos subjacentes.
* AzureRM.BootStrapper
    + Novo módulo criado para gerenciar as versões dos cmdlets do Azure PowerShell com o uso dos perfis da versão