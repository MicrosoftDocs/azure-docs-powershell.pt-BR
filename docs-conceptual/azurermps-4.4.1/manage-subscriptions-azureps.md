---
title: Gerenciar assinaturas do Aure com o Azure PowerShell | Microsoft Docs
description: Gerenciar assinaturas do Azure com o Azure PowerShell
keywords: Azure PowerShell, assinatura
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 921da316b1e8a57f0879c87820297de662b2cfd0
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386724"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="08470-104">Gerenciar várias assinaturas do Azure</span><span class="sxs-lookup"><span data-stu-id="08470-104">Manage multiple Azure subscriptions</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="08470-105">Se você for novo no Azure, provavelmente tem apenas uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="08470-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="08470-106">Mas se você já usa o Azure por algum tempo, poderá criar várias assinaturas do Azure.</span><span class="sxs-lookup"><span data-stu-id="08470-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="08470-107">Você pode configurar o Azure PowerShell para executar comandos em uma assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="08470-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="08470-108">Obtenha uma lista de todas as assinaturas em sua conta.</span><span class="sxs-lookup"><span data-stu-id="08470-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="08470-109">Defina o padrão.</span><span class="sxs-lookup"><span data-stu-id="08470-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="08470-110">Verifique a alteração ao executar o cmdlet `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="08470-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="08470-111">Depois que você configurar sua assinatura padrão, todos os comandos subsequentes do Azure PowerShell serão executados nessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="08470-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
