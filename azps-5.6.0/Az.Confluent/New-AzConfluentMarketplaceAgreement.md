---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893225"
---
# <span data-ttu-id="1003c-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="1003c-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="1003c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1003c-102">SYNOPSIS</span></span>
<span data-ttu-id="1003c-103">Aceitar termos de marketplace.</span><span class="sxs-lookup"><span data-stu-id="1003c-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="1003c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1003c-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1003c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1003c-105">DESCRIPTION</span></span>
<span data-ttu-id="1003c-106">Aceitar termos de marketplace.</span><span class="sxs-lookup"><span data-stu-id="1003c-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="1003c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1003c-107">EXAMPLES</span></span>

### <span data-ttu-id="1003c-108">Exemplo 1: Criar contrato de marketplace confluente sob uma assinatura</span><span class="sxs-lookup"><span data-stu-id="1003c-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="1003c-109">Este comando cria um contrato de marketplace confluente sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1003c-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="1003c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1003c-110">PARAMETERS</span></span>

### <span data-ttu-id="1003c-111">-Accepted</span><span class="sxs-lookup"><span data-stu-id="1003c-111">-Accepted</span></span>
<span data-ttu-id="1003c-112">Se qualquer versão dos termos tiver sido aceita, caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="1003c-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="1003c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1003c-113">-DefaultProfile</span></span>
<span data-ttu-id="1003c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1003c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1003c-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="1003c-115">-LicenseTextLink</span></span>
<span data-ttu-id="1003c-116">Link para HTML com termos microsoft e publisher.</span><span class="sxs-lookup"><span data-stu-id="1003c-116">Link to HTML with Microsoft and Publisher terms.</span></span>

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

### <span data-ttu-id="1003c-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="1003c-117">-Plan</span></span>
<span data-ttu-id="1003c-118">Planejar cadeia de caracteres de identificador.</span><span class="sxs-lookup"><span data-stu-id="1003c-118">Plan identifier string.</span></span>

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

### <span data-ttu-id="1003c-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="1003c-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="1003c-120">Link para a política de privacidade do editor.</span><span class="sxs-lookup"><span data-stu-id="1003c-120">Link to the privacy policy of the publisher.</span></span>

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

### <span data-ttu-id="1003c-121">-Product</span><span class="sxs-lookup"><span data-stu-id="1003c-121">-Product</span></span>
<span data-ttu-id="1003c-122">Cadeia de caracteres do identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="1003c-122">Product identifier string.</span></span>

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

### <span data-ttu-id="1003c-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1003c-123">-Publisher</span></span>
<span data-ttu-id="1003c-124">Cadeia de caracteres de identificador do publisher.</span><span class="sxs-lookup"><span data-stu-id="1003c-124">Publisher identifier string.</span></span>

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

### <span data-ttu-id="1003c-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="1003c-125">-RetrieveDatetime</span></span>
<span data-ttu-id="1003c-126">Data e hora em UTC de quando os termos foram aceitos.</span><span class="sxs-lookup"><span data-stu-id="1003c-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="1003c-127">Isso será vazio se Accepted for false.</span><span class="sxs-lookup"><span data-stu-id="1003c-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1003c-128">-Signature</span><span class="sxs-lookup"><span data-stu-id="1003c-128">-Signature</span></span>
<span data-ttu-id="1003c-129">Assinatura de termos.</span><span class="sxs-lookup"><span data-stu-id="1003c-129">Terms signature.</span></span>

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

### <span data-ttu-id="1003c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1003c-130">-SubscriptionId</span></span>
<span data-ttu-id="1003c-131">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="1003c-131">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="1003c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1003c-132">-Confirm</span></span>
<span data-ttu-id="1003c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1003c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1003c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1003c-134">-WhatIf</span></span>
<span data-ttu-id="1003c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1003c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1003c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1003c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1003c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1003c-137">CommonParameters</span></span>
<span data-ttu-id="1003c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1003c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1003c-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1003c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1003c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1003c-140">INPUTS</span></span>

## <span data-ttu-id="1003c-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1003c-141">OUTPUTS</span></span>

### <span data-ttu-id="1003c-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="1003c-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="1003c-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="1003c-143">NOTES</span></span>

<span data-ttu-id="1003c-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1003c-144">ALIASES</span></span>

## <span data-ttu-id="1003c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1003c-145">RELATED LINKS</span></span>

