---
title: Gerenciar assinaturas do Azure com o Azure PowerShell
description: Gerenciar assinaturas do Azure com o Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 41cf9b06f736f22eb3c2a9e2fbe1f047534cc09d
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594619"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="fd6d5-103">Gerenciar várias assinaturas do Azure</span><span class="sxs-lookup"><span data-stu-id="fd6d5-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="fd6d5-104">Se você for novo no Azure, provavelmente tem apenas uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="fd6d5-105">Mas se você já usa o Azure por algum tempo, poderá criar várias assinaturas do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="fd6d5-106">Você pode configurar o Azure PowerShell para executar comandos em uma assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="fd6d5-107">Obtenha uma lista de todas as assinaturas em sua conta.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzSubscription
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

2. <span data-ttu-id="fd6d5-108">Defina o padrão.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="fd6d5-109">Verifique a alteração ao executar o cmdlet `Get-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-109">Verify the change by running the `Get-AzContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="fd6d5-110">Depois que você configurar sua assinatura padrão, todos os comandos do Azure PowerShell serão executados nessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd6d5-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
