---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947027"
---
# <span data-ttu-id="020fc-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="020fc-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="020fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="020fc-102">SYNOPSIS</span></span>
<span data-ttu-id="020fc-103">Obter a oferta especificada para o provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="020fc-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="020fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="020fc-104">SYNTAX</span></span>

### <span data-ttu-id="020fc-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="020fc-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="020fc-106">Obter</span><span class="sxs-lookup"><span data-stu-id="020fc-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="020fc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="020fc-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="020fc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="020fc-108">DESCRIPTION</span></span>
<span data-ttu-id="020fc-109">Obter a oferta especificada para o provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="020fc-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="020fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="020fc-110">EXAMPLES</span></span>

### <span data-ttu-id="020fc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="020fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="020fc-112">Obter a lista de ofertas para o provedor delegado especificado</span><span class="sxs-lookup"><span data-stu-id="020fc-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="020fc-113">OS</span><span class="sxs-lookup"><span data-stu-id="020fc-113">PARAMETERS</span></span>

### <span data-ttu-id="020fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020fc-114">-DefaultProfile</span></span>
<span data-ttu-id="020fc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="020fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020fc-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="020fc-116">-DelegatedProviderId</span></span>
<span data-ttu-id="020fc-117">ID do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="020fc-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="020fc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="020fc-118">-InputObject</span></span>
<span data-ttu-id="020fc-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="020fc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="020fc-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="020fc-120">-OfferName</span></span>
<span data-ttu-id="020fc-121">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="020fc-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="020fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020fc-122">CommonParameters</span></span>
<span data-ttu-id="020fc-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020fc-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="020fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020fc-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="020fc-125">INPUTS</span></span>

### <span data-ttu-id="020fc-126">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="020fc-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="020fc-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="020fc-127">OUTPUTS</span></span>

### <span data-ttu-id="020fc-128">Microsoft. Azure. PowerShell. cmdlets. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="020fc-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="020fc-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="020fc-129">NOTES</span></span>

<span data-ttu-id="020fc-130">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="020fc-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="020fc-131">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="020fc-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="020fc-132">INPUTobject <ISubscriptionIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="020fc-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="020fc-133">`[DelegatedProviderId <String>]`: ID do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="020fc-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="020fc-134">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="020fc-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="020fc-135">`[OfferName <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="020fc-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="020fc-136">`[SubscriptionId <String>]`: ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="020fc-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="020fc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="020fc-137">RELATED LINKS</span></span>

