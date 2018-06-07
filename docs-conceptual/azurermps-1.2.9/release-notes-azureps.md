---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819704"
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