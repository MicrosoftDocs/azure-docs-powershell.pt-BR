---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114337"
---
# <span data-ttu-id="7fc18-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="7fc18-101">Get-AzSubscription</span></span>

## <span data-ttu-id="7fc18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fc18-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc18-103">Obter assinaturas que a conta atual pode acessar.</span><span class="sxs-lookup"><span data-stu-id="7fc18-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="7fc18-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fc18-104">SYNTAX</span></span>

### <span data-ttu-id="7fc18-105">ListByIdInTenant (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7fc18-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc18-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="7fc18-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fc18-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fc18-107">DESCRIPTION</span></span>
<span data-ttu-id="7fc18-108">O Get-AzSubscription cmdlet obtém a ID da assinatura, o nome da assinatura e o locatário ínteque das assinaturas que a conta atual pode acessar.</span><span class="sxs-lookup"><span data-stu-id="7fc18-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="7fc18-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7fc18-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc18-110">Exemplo 1: Obter todas as assinaturas em todos os locatários</span><span class="sxs-lookup"><span data-stu-id="7fc18-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="7fc18-111">Esse comando obtém todas as assinaturas em todos os locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="7fc18-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="7fc18-112">Exemplo 2: Obter todas as assinaturas de um locatário específico</span><span class="sxs-lookup"><span data-stu-id="7fc18-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="7fc18-113">Liste todas as assinaturas do locatário que estão autorizadas para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="7fc18-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="7fc18-114">Exemplo 3: Obter todas as assinaturas no locatário atual</span><span class="sxs-lookup"><span data-stu-id="7fc18-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="7fc18-115">Esse comando obtém todas as assinaturas no locatário atual que estão autorizadas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7fc18-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="7fc18-116">Exemplo 4: alterar o contexto atual para usar uma assinatura específica</span><span class="sxs-lookup"><span data-stu-id="7fc18-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="7fc18-117">Esse comando obtém a assinatura especificada e define o contexto atual para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="7fc18-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="7fc18-118">Todos os cmdlets subsequentes nesta sessão usam a nova assinatura (Assinatura Contoso 1) por padrão.</span><span class="sxs-lookup"><span data-stu-id="7fc18-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="7fc18-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fc18-119">PARAMETERS</span></span>

### <span data-ttu-id="7fc18-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fc18-120">-AsJob</span></span>
<span data-ttu-id="7fc18-121">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="7fc18-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc18-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc18-122">-DefaultProfile</span></span>
<span data-ttu-id="7fc18-123">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7fc18-123">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fc18-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fc18-124">-SubscriptionId</span></span>
<span data-ttu-id="7fc18-125">Especifica a ID da assinatura a ser obter.</span><span class="sxs-lookup"><span data-stu-id="7fc18-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc18-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7fc18-126">-SubscriptionName</span></span>
<span data-ttu-id="7fc18-127">Especifica o nome da assinatura a ser obter.</span><span class="sxs-lookup"><span data-stu-id="7fc18-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc18-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7fc18-128">-TenantId</span></span>
<span data-ttu-id="7fc18-129">Especifica a ID do locatário que contém assinaturas a obter.</span><span class="sxs-lookup"><span data-stu-id="7fc18-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc18-130">CommonParameters</span></span>
<span data-ttu-id="7fc18-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc18-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc18-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc18-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="7fc18-133">INPUTS</span></span>

### <span data-ttu-id="7fc18-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7fc18-134">System.String</span></span>

## <span data-ttu-id="7fc18-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="7fc18-135">OUTPUTS</span></span>

### <span data-ttu-id="7fc18-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7fc18-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="7fc18-137">Notas</span><span class="sxs-lookup"><span data-stu-id="7fc18-137">NOTES</span></span>

## <span data-ttu-id="7fc18-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fc18-138">RELATED LINKS</span></span>
