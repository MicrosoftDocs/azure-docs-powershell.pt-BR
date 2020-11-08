---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110877"
---
# <span data-ttu-id="ae759-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ae759-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="ae759-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae759-102">SYNOPSIS</span></span>
<span data-ttu-id="ae759-103">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="ae759-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="ae759-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae759-104">SYNTAX</span></span>

### <span data-ttu-id="ae759-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae759-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae759-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae759-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae759-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae759-107">DESCRIPTION</span></span>
<span data-ttu-id="ae759-108">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="ae759-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="ae759-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae759-109">EXAMPLES</span></span>

### <span data-ttu-id="ae759-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae759-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="ae759-111">Define o tipo de preço da central de segurança do Azure de assinatura como "padrão"</span><span class="sxs-lookup"><span data-stu-id="ae759-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="ae759-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae759-112">PARAMETERS</span></span>

### <span data-ttu-id="ae759-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae759-113">-DefaultProfile</span></span>
<span data-ttu-id="ae759-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae759-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae759-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae759-115">-InputObject</span></span>
<span data-ttu-id="ae759-116">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae759-116">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae759-117">-Name</span></span>
<span data-ttu-id="ae759-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae759-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="ae759-119">-PricingTier</span></span>
<span data-ttu-id="ae759-120">Tipo de preço.</span><span class="sxs-lookup"><span data-stu-id="ae759-120">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae759-121">-Confirm</span></span>
<span data-ttu-id="ae759-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae759-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae759-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae759-123">-WhatIf</span></span>
<span data-ttu-id="ae759-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae759-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae759-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae759-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae759-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae759-126">CommonParameters</span></span>
<span data-ttu-id="ae759-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae759-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae759-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae759-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae759-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae759-129">INPUTS</span></span>

### <span data-ttu-id="ae759-130">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ae759-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="ae759-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae759-131">OUTPUTS</span></span>

### <span data-ttu-id="ae759-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="ae759-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="ae759-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae759-133">NOTES</span></span>

## <span data-ttu-id="ae759-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae759-134">RELATED LINKS</span></span>
