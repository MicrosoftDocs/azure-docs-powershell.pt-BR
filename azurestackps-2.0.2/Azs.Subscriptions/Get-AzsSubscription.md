---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947026"
---
# <span data-ttu-id="3f870-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="3f870-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="3f870-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f870-102">SYNOPSIS</span></span>
<span data-ttu-id="3f870-103">Obtém detalhes sobre uma assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="3f870-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="3f870-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f870-104">SYNTAX</span></span>

### <span data-ttu-id="3f870-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f870-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f870-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3f870-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f870-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f870-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3f870-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f870-108">DESCRIPTION</span></span>
<span data-ttu-id="3f870-109">Obtém detalhes sobre uma assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="3f870-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="3f870-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f870-110">EXAMPLES</span></span>

### <span data-ttu-id="3f870-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f870-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="3f870-112">Obter a lista de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="3f870-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="3f870-113">OS</span><span class="sxs-lookup"><span data-stu-id="3f870-113">PARAMETERS</span></span>

### <span data-ttu-id="3f870-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f870-114">-DefaultProfile</span></span>
<span data-ttu-id="3f870-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f870-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f870-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f870-116">-InputObject</span></span>
<span data-ttu-id="3f870-117">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3f870-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3f870-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f870-118">-SubscriptionId</span></span>
<span data-ttu-id="3f870-119">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f870-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f870-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f870-120">CommonParameters</span></span>
<span data-ttu-id="3f870-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f870-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f870-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f870-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f870-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f870-123">INPUTS</span></span>

### <span data-ttu-id="3f870-124">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="3f870-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="3f870-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f870-125">OUTPUTS</span></span>

### <span data-ttu-id="3f870-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="3f870-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="3f870-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f870-127">NOTES</span></span>

<span data-ttu-id="3f870-128">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3f870-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f870-129">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f870-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f870-130">INPUTobject <ISubscriptionIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3f870-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f870-131">`[DelegatedProviderId <String>]`: ID do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="3f870-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="3f870-132">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3f870-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f870-133">`[OfferName <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="3f870-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3f870-134">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f870-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="3f870-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f870-135">RELATED LINKS</span></span>

