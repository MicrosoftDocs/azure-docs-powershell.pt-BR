---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430681"
---
# <span data-ttu-id="0cf91-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="0cf91-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="0cf91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf91-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf91-103">Obter assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="0cf91-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cf91-104">SYNTAX</span></span>

### <span data-ttu-id="0cf91-105">ListByIdInTenant (padrão)</span><span class="sxs-lookup"><span data-stu-id="0cf91-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf91-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="0cf91-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf91-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cf91-107">DESCRIPTION</span></span>
<span data-ttu-id="0cf91-108">O cmdlet Get-AzureRmSubscription Obtém a ID da assinatura, o nome da assinatura e o locatário doméstico para assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="0cf91-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="0cf91-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cf91-109">EXAMPLES</span></span>

### <span data-ttu-id="0cf91-110">Exemplo 1: obter todas as assinaturas em todos os locatários</span><span class="sxs-lookup"><span data-stu-id="0cf91-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="0cf91-111">Esse comando obtém todas as assinaturas em todos os locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="0cf91-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="0cf91-112">Exemplo 2: obter todas as assinaturas para um locatário específico</span><span class="sxs-lookup"><span data-stu-id="0cf91-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0cf91-113">Listar todas as assinaturas no locatário especificado que são autorizadas para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="0cf91-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="0cf91-114">Exemplo 3: obter todas as assinaturas no locatário atual</span><span class="sxs-lookup"><span data-stu-id="0cf91-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="0cf91-115">Esse comando obtém todas as assinaturas no locatário atual que são autorizadas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0cf91-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="0cf91-116">Exemplo 4: alterar o contexto atual para usar uma assinatura específica</span><span class="sxs-lookup"><span data-stu-id="0cf91-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="0cf91-117">Este comando obtém a assinatura especificada e, em seguida, define o contexto atual para usá-la.</span><span class="sxs-lookup"><span data-stu-id="0cf91-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="0cf91-118">Todos os cmdlets subsequentes nesta sessão usam a nova assinatura (contoso assinatura 1) por padrão.</span><span class="sxs-lookup"><span data-stu-id="0cf91-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="0cf91-119">OS</span><span class="sxs-lookup"><span data-stu-id="0cf91-119">PARAMETERS</span></span>

### <span data-ttu-id="0cf91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf91-120">-DefaultProfile</span></span>
<span data-ttu-id="0cf91-121">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0cf91-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf91-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0cf91-122">-SubscriptionId</span></span>
<span data-ttu-id="0cf91-123">Especifica a ID da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="0cf91-123">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="0cf91-124">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="0cf91-124">-SubscriptionName</span></span>
<span data-ttu-id="0cf91-125">Especifica o nome da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="0cf91-125">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="0cf91-126">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="0cf91-126">-TenantId</span></span>
<span data-ttu-id="0cf91-127">Especifica a ID do locatário que contém assinaturas a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="0cf91-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="0cf91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf91-128">CommonParameters</span></span>
<span data-ttu-id="0cf91-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf91-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf91-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cf91-131">INPUTS</span></span>

## <span data-ttu-id="0cf91-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cf91-132">OUTPUTS</span></span>

### <span data-ttu-id="0cf91-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0cf91-133">PSAzureSubscription</span></span>

## <span data-ttu-id="0cf91-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cf91-134">NOTES</span></span>

## <span data-ttu-id="0cf91-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf91-135">RELATED LINKS</span></span>

