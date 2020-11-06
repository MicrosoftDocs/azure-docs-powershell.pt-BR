---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425841"
---
# <span data-ttu-id="8b5cd-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="8b5cd-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="8b5cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5cd-103">Obter assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="8b5cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b5cd-104">SYNTAX</span></span>

### <span data-ttu-id="8b5cd-105">ListByIdInTenant (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b5cd-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="8b5cd-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="8b5cd-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8b5cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b5cd-107">DESCRIPTION</span></span>
<span data-ttu-id="8b5cd-108">O cmdlet Get-AzureRmSubscription Obtém a ID da assinatura, o nome da assinatura e o locatário doméstico para assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="8b5cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b5cd-109">EXAMPLES</span></span>

### <span data-ttu-id="8b5cd-110">Exemplo 1: obter todas as assinaturas em todos os locatários</span><span class="sxs-lookup"><span data-stu-id="8b5cd-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8b5cd-111">Esse comando obtém todas as assinaturas em todos os locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="8b5cd-112">Exemplo 2: obter todas as assinaturas para um locatário específico</span><span class="sxs-lookup"><span data-stu-id="8b5cd-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8b5cd-113">Listar todas as assinaturas no locatário especificado que são autorizadas para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="8b5cd-114">Exemplo 3: obter todas as assinaturas no locatário atual</span><span class="sxs-lookup"><span data-stu-id="8b5cd-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="8b5cd-115">Esse comando obtém todas as assinaturas no locatário atual que são autorizadas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="8b5cd-116">Exemplo 4: alterar o contexto atual para usar uma assinatura específica</span><span class="sxs-lookup"><span data-stu-id="8b5cd-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="8b5cd-117">Este comando obtém a assinatura especificada e, em seguida, define o contexto atual para usá-la.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="8b5cd-118">Todos os cmdlets subsequentes nesta sessão usam a nova assinatura (contoso assinatura 1) por padrão.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="8b5cd-119">OS</span><span class="sxs-lookup"><span data-stu-id="8b5cd-119">PARAMETERS</span></span>

### <span data-ttu-id="8b5cd-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b5cd-120">-SubscriptionId</span></span>
<span data-ttu-id="8b5cd-121">Especifica a ID da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5cd-122">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="8b5cd-122">-SubscriptionName</span></span>
<span data-ttu-id="8b5cd-123">Especifica o nome da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5cd-124">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="8b5cd-124">-TenantId</span></span>
<span data-ttu-id="8b5cd-125">Especifica a ID do locatário que contém assinaturas a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5cd-126">CommonParameters</span></span>
<span data-ttu-id="8b5cd-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5cd-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5cd-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b5cd-129">INPUTS</span></span>

## <span data-ttu-id="8b5cd-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b5cd-130">OUTPUTS</span></span>

### <span data-ttu-id="8b5cd-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8b5cd-131">PSAzureSubscription</span></span>

## <span data-ttu-id="8b5cd-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b5cd-132">NOTES</span></span>

## <span data-ttu-id="8b5cd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b5cd-133">RELATED LINKS</span></span>

