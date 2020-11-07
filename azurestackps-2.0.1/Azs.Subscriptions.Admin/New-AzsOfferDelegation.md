---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945185"
---
# <span data-ttu-id="4e4e4-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4e4e4-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="4e4e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4e4-103">Criar ou atualizar a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="4e4e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e4e4-104">SYNTAX</span></span>

### <span data-ttu-id="4e4e4-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="4e4e4-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e4e4-106">Criados</span><span class="sxs-lookup"><span data-stu-id="4e4e4-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e4e4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e4e4-107">DESCRIPTION</span></span>
<span data-ttu-id="4e4e4-108">Criar ou atualizar a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="4e4e4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e4e4-109">EXAMPLES</span></span>

### <span data-ttu-id="4e4e4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e4e4-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="4e4e4-111">Criar uma nova delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="4e4e4-112">OS</span><span class="sxs-lookup"><span data-stu-id="4e4e4-112">PARAMETERS</span></span>

### <span data-ttu-id="4e4e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4e4-113">-DefaultProfile</span></span>
<span data-ttu-id="4e4e4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4e4-115">-Local</span><span class="sxs-lookup"><span data-stu-id="4e4e4-115">-Location</span></span>
<span data-ttu-id="4e4e4-116">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="4e4e4-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e4e4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e4e4-117">-Name</span></span>
<span data-ttu-id="4e4e4-118">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="4e4e4-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="4e4e4-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="4e4e4-120">Oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-120">Offer delegation.</span></span>
<span data-ttu-id="4e4e4-121">Para construir, consulte a seção notas para propriedades OFFERDELEGATIONDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4e4e4-122">-Offername</span><span class="sxs-lookup"><span data-stu-id="4e4e4-122">-OfferName</span></span>
<span data-ttu-id="4e4e4-123">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-123">Name of an offer.</span></span>

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

### <span data-ttu-id="4e4e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e4e4-125">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4e4e4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e4e4-126">-SubscriptionId</span></span>
<span data-ttu-id="4e4e4-127">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e4e4-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e4e4-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="4e4e4-129">Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e4e4-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4e4e4-130">-Confirm</span></span>
<span data-ttu-id="4e4e4-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4e4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4e4-132">-WhatIf</span></span>
<span data-ttu-id="4e4e4-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4e4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4e4-135">CommonParameters</span></span>
<span data-ttu-id="4e4e4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4e4-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e4e4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4e4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e4e4-138">INPUTS</span></span>

### <span data-ttu-id="4e4e4-139">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4e4e4-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="4e4e4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e4e4-140">OUTPUTS</span></span>

### <span data-ttu-id="4e4e4-141">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4e4e4-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="4e4e4-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e4e4-142">ALIASES</span></span>

## <span data-ttu-id="4e4e4-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e4e4-143">NOTES</span></span>

<span data-ttu-id="4e4e4-144">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e4e4-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4e4e4-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="4e4e4-147">`[Location <String>]`: Localização do recurso</span><span class="sxs-lookup"><span data-stu-id="4e4e4-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="4e4e4-148">`[SubscriptionId <String>]`: Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="4e4e4-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="4e4e4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e4e4-149">RELATED LINKS</span></span>

