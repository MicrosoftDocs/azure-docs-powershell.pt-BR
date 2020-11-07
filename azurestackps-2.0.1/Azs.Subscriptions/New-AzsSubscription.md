---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945175"
---
# <span data-ttu-id="5f72d-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="5f72d-101">New-AzsSubscription</span></span>

## <span data-ttu-id="5f72d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f72d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f72d-103">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="5f72d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f72d-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5f72d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f72d-105">DESCRIPTION</span></span>
<span data-ttu-id="5f72d-106">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="5f72d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f72d-107">EXAMPLES</span></span>

### <span data-ttu-id="5f72d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f72d-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="5f72d-109">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-109">Create a subscription.</span></span>

## <span data-ttu-id="5f72d-110">OS</span><span class="sxs-lookup"><span data-stu-id="5f72d-110">PARAMETERS</span></span>

### <span data-ttu-id="5f72d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f72d-111">-DefaultProfile</span></span>
<span data-ttu-id="5f72d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f72d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f72d-113">-DisplayName</span></span>
<span data-ttu-id="5f72d-114">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="5f72d-115">-Id</span></span>
<span data-ttu-id="5f72d-116">Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5f72d-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="5f72d-117">-OfferId</span></span>
<span data-ttu-id="5f72d-118">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="5f72d-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="5f72d-119">-State</span></span>
<span data-ttu-id="5f72d-120">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f72d-121">-SubscriptionId</span></span>
<span data-ttu-id="5f72d-122">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f72d-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-123">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="5f72d-123">-TenantId</span></span>
<span data-ttu-id="5f72d-124">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="5f72d-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f72d-125">-Confirm</span></span>
<span data-ttu-id="5f72d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f72d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f72d-127">-WhatIf</span></span>
<span data-ttu-id="5f72d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f72d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f72d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f72d-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f72d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f72d-130">CommonParameters</span></span>
<span data-ttu-id="5f72d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f72d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f72d-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f72d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f72d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f72d-133">INPUTS</span></span>

## <span data-ttu-id="5f72d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f72d-134">OUTPUTS</span></span>

### <span data-ttu-id="5f72d-135">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="5f72d-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="5f72d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f72d-136">NOTES</span></span>

## <span data-ttu-id="5f72d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f72d-137">RELATED LINKS</span></span>

