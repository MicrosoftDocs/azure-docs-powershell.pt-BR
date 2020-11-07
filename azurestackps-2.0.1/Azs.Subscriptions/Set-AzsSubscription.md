---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945250"
---
# <span data-ttu-id="5d8cf-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="5d8cf-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="5d8cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8cf-103">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="5d8cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d8cf-104">SYNTAX</span></span>

### <span data-ttu-id="5d8cf-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d8cf-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d8cf-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="5d8cf-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5d8cf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="5d8cf-108">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="5d8cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="5d8cf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d8cf-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="5d8cf-111">Atualiza uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-111">Updates a subscription.</span></span>

## <span data-ttu-id="5d8cf-112">OS</span><span class="sxs-lookup"><span data-stu-id="5d8cf-112">PARAMETERS</span></span>

### <span data-ttu-id="5d8cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8cf-113">-DefaultProfile</span></span>
<span data-ttu-id="5d8cf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8cf-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d8cf-115">-DisplayName</span></span>
<span data-ttu-id="5d8cf-116">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5d8cf-117">-Id</span></span>
<span data-ttu-id="5d8cf-118">Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="5d8cf-119">-OfferId</span></span>
<span data-ttu-id="5d8cf-120">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-121">-Estado</span><span class="sxs-lookup"><span data-stu-id="5d8cf-121">-State</span></span>
<span data-ttu-id="5d8cf-122">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="5d8cf-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="5d8cf-124">Lista de operações com suporte.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-124">List of supported operations.</span></span>
<span data-ttu-id="5d8cf-125">Para construir, consulte a seção notas para propriedades SUBSCRIPTIONDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d8cf-126">-SubscriptionId</span></span>
<span data-ttu-id="5d8cf-127">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-128">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="5d8cf-128">-TenantId</span></span>
<span data-ttu-id="5d8cf-129">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5d8cf-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d8cf-130">-Confirm</span></span>
<span data-ttu-id="5d8cf-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8cf-132">-WhatIf</span></span>
<span data-ttu-id="5d8cf-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d8cf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8cf-135">CommonParameters</span></span>
<span data-ttu-id="5d8cf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8cf-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d8cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8cf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d8cf-138">INPUTS</span></span>

### <span data-ttu-id="5d8cf-139">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="5d8cf-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="5d8cf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d8cf-140">OUTPUTS</span></span>

### <span data-ttu-id="5d8cf-141">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="5d8cf-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="5d8cf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d8cf-142">NOTES</span></span>

<span data-ttu-id="5d8cf-143">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d8cf-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5d8cf-145">SUBSCRIPTIONDEFINITION <ISubscription> : lista de operações com suporte.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="5d8cf-146">`[DisplayName <String>]`: Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="5d8cf-147">`[Id <String>]`: Identificador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="5d8cf-148">`[OfferId <String>]`: Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="5d8cf-149">`[State <SubscriptionState?>]`: Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="5d8cf-150">`[SubscriptionId <String>]`: Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="5d8cf-151">`[TenantId <String>]`: Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="5d8cf-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="5d8cf-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d8cf-152">RELATED LINKS</span></span>

