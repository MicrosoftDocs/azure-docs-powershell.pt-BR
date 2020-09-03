---
title: Gerenciar assinaturas do Aure com o Azure PowerShell | Microsoft Docs
description: Gerenciar assinaturas do Azure com o Azure PowerShell
keywords: Azure PowerShell, assinatura
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: d2674e37a211d1c1896a13e234cda95beea4479a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243983"
---
# <a name="manage-multiple-azure-subscriptions"></a>Gerenciar várias assinaturas do Azure

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Se você for novo no Azure, provavelmente tem apenas uma única assinatura. Mas se você já usa o Azure por algum tempo, poderá criar várias assinaturas do Azure. Você pode configurar o Azure PowerShell para executar comandos em uma assinatura específica.

1. Obtenha uma lista de todas as assinaturas em sua conta.

    ```powershell-interactive
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

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. Verifique a alteração ao executar o cmdlet `Get-AzureRmContext`.

    ```powershell-interactive
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
