---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945102"
---
# <span data-ttu-id="a2834-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2834-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="a2834-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2834-102">SYNOPSIS</span></span>
<span data-ttu-id="a2834-103">Criar ou atualizar a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="a2834-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a2834-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2834-104">SYNTAX</span></span>

### <span data-ttu-id="a2834-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2834-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2834-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="a2834-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2834-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2834-107">DESCRIPTION</span></span>
<span data-ttu-id="a2834-108">Criar ou atualizar a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="a2834-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a2834-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2834-109">EXAMPLES</span></span>

### <span data-ttu-id="a2834-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2834-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="a2834-111">Atualiza a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="a2834-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="a2834-112">OS</span><span class="sxs-lookup"><span data-stu-id="a2834-112">PARAMETERS</span></span>

### <span data-ttu-id="a2834-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2834-113">-DefaultProfile</span></span>
<span data-ttu-id="a2834-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2834-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2834-115">-Local</span><span class="sxs-lookup"><span data-stu-id="a2834-115">-Location</span></span>
<span data-ttu-id="a2834-116">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="a2834-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2834-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2834-117">-Name</span></span>
<span data-ttu-id="a2834-118">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="a2834-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a2834-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="a2834-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="a2834-120">Oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="a2834-120">Offer delegation.</span></span>
<span data-ttu-id="a2834-121">Para construir, consulte a seção notas para propriedades OFFERDELEGATIONDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a2834-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a2834-122">-Offername</span><span class="sxs-lookup"><span data-stu-id="a2834-122">-OfferName</span></span>
<span data-ttu-id="a2834-123">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="a2834-123">Name of an offer.</span></span>

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

### <span data-ttu-id="a2834-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2834-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="a2834-125">Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="a2834-125">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="a2834-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2834-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2834-127">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="a2834-127">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a2834-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2834-128">-SubscriptionId</span></span>
<span data-ttu-id="a2834-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a2834-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a2834-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2834-130">-Confirm</span></span>
<span data-ttu-id="a2834-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2834-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2834-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2834-132">-WhatIf</span></span>
<span data-ttu-id="a2834-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2834-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2834-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2834-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2834-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2834-135">CommonParameters</span></span>
<span data-ttu-id="a2834-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2834-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2834-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2834-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2834-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2834-138">INPUTS</span></span>

### <span data-ttu-id="a2834-139">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2834-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="a2834-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2834-140">OUTPUTS</span></span>

### <span data-ttu-id="a2834-141">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2834-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="a2834-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a2834-142">ALIASES</span></span>

## <span data-ttu-id="a2834-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2834-143">NOTES</span></span>

<span data-ttu-id="a2834-144">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a2834-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2834-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2834-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a2834-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : oferecer delegação.</span><span class="sxs-lookup"><span data-stu-id="a2834-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="a2834-147">`[Location <String>]`: Localização do recurso</span><span class="sxs-lookup"><span data-stu-id="a2834-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="a2834-148">`[SubscriptionId <String>]`: Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="a2834-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="a2834-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2834-149">RELATED LINKS</span></span>

