---
title: Gerenciar assinaturas do Aure com o Azure PowerShell | Microsoft Docs
description: Gerenciar assinaturas do Azure com o Azure PowerShell
keywords: Azure PowerShell, assinatura
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 4f066118373c9ea7deffe7c6474552f1ce91cb56
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820588"
---
# <a name="manage-multiple-azure-subscriptions"></a>Gerenciar várias assinaturas do Azure

Se você for novo no Azure, provavelmente tem apenas uma única assinatura. Mas se você já usa o Azure por algum tempo, poderá criar várias assinaturas do Azure. Você pode configurar o Azure PowerShell para executar comandos em uma assinatura específica.

1. Obtenha uma lista de todas as assinaturas em sua conta.

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. Defina o padrão.

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. Verifique a alteração ao executar o cmdlet `Get-AzureRmContext`.

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

Depois que você configurar sua assinatura padrão, todos os comandos subsequentes do Azure PowerShell serão executados nessa assinatura.
