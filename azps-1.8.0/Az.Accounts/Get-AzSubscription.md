---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: 24896d405a4760b0db004dcb67f876263c9eb17f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595794"
---
# <span data-ttu-id="a6740-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a6740-101">Get-AzSubscription</span></span>

## <span data-ttu-id="a6740-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6740-102">SYNOPSIS</span></span>
<span data-ttu-id="a6740-103">Obter assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="a6740-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a6740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6740-104">SYNTAX</span></span>

### <span data-ttu-id="a6740-105">ListByIdInTenant (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6740-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6740-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="a6740-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6740-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6740-107">DESCRIPTION</span></span>
<span data-ttu-id="a6740-108">O cmdlet Get-AzSubscription Obtém a ID da assinatura, o nome da assinatura e o locatário doméstico para assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="a6740-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a6740-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6740-109">EXAMPLES</span></span>

### <span data-ttu-id="a6740-110">Exemplo 1: obter todas as assinaturas em todos os locatários</span><span class="sxs-lookup"><span data-stu-id="a6740-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="a6740-111">Esse comando obtém todas as assinaturas em todos os locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="a6740-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a6740-112">Exemplo 2: obter todas as assinaturas para um locatário específico</span><span class="sxs-lookup"><span data-stu-id="a6740-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a6740-113">Listar todas as assinaturas no locatário especificado que são autorizadas para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="a6740-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a6740-114">Exemplo 3: obter todas as assinaturas no locatário atual</span><span class="sxs-lookup"><span data-stu-id="a6740-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a6740-115">Esse comando obtém todas as assinaturas no locatário atual que são autorizadas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="a6740-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a6740-116">Exemplo 4: alterar o contexto atual para usar uma assinatura específica</span><span class="sxs-lookup"><span data-stu-id="a6740-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a6740-117">Este comando obtém a assinatura especificada e, em seguida, define o contexto atual para usá-la.</span><span class="sxs-lookup"><span data-stu-id="a6740-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="a6740-118">Todos os cmdlets subsequentes nesta sessão usam a nova assinatura (contoso assinatura 1) por padrão.</span><span class="sxs-lookup"><span data-stu-id="a6740-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a6740-119">OS</span><span class="sxs-lookup"><span data-stu-id="a6740-119">PARAMETERS</span></span>

### <span data-ttu-id="a6740-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6740-120">-AsJob</span></span>
<span data-ttu-id="a6740-121">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a6740-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6740-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6740-122">-DefaultProfile</span></span>
<span data-ttu-id="a6740-123">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6740-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6740-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6740-124">-SubscriptionId</span></span>
<span data-ttu-id="a6740-125">Especifica a ID da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="a6740-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="a6740-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="a6740-126">-SubscriptionName</span></span>
<span data-ttu-id="a6740-127">Especifica o nome da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="a6740-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="a6740-128">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="a6740-128">-TenantId</span></span>
<span data-ttu-id="a6740-129">Especifica a ID do locatário que contém assinaturas a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="a6740-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="a6740-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6740-130">CommonParameters</span></span>
<span data-ttu-id="a6740-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6740-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6740-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6740-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6740-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6740-133">INPUTS</span></span>

### <span data-ttu-id="a6740-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6740-134">System.String</span></span>

## <span data-ttu-id="a6740-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6740-135">OUTPUTS</span></span>

### <span data-ttu-id="a6740-136">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a6740-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a6740-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6740-137">NOTES</span></span>

## <span data-ttu-id="a6740-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6740-138">RELATED LINKS</span></span>
