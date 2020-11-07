---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943755"
---
# <span data-ttu-id="289a9-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="289a9-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="289a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="289a9-102">SYNOPSIS</span></span>
<span data-ttu-id="289a9-103">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="289a9-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="289a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="289a9-104">SYNTAX</span></span>

### <span data-ttu-id="289a9-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="289a9-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="289a9-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="289a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="289a9-107">DESCRIPTION</span></span>
<span data-ttu-id="289a9-108">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="289a9-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="289a9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="289a9-109">EXAMPLES</span></span>

### <span data-ttu-id="289a9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="289a9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="289a9-111">Define o tipo de preço da central de segurança do Azure de assinatura como "padrão"</span><span class="sxs-lookup"><span data-stu-id="289a9-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="289a9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="289a9-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="289a9-113">Define o tipo de preço da central de segurança do grupo de recursos "myService1" do Azure para "padrão"</span><span class="sxs-lookup"><span data-stu-id="289a9-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="289a9-114">OS</span><span class="sxs-lookup"><span data-stu-id="289a9-114">PARAMETERS</span></span>

### <span data-ttu-id="289a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289a9-115">-DefaultProfile</span></span>
<span data-ttu-id="289a9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="289a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="289a9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="289a9-117">-InputObject</span></span>
<span data-ttu-id="289a9-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="289a9-118">Input Object.</span></span>

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

### <span data-ttu-id="289a9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="289a9-119">-Name</span></span>
<span data-ttu-id="289a9-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="289a9-120">Resource name.</span></span>

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

### <span data-ttu-id="289a9-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="289a9-121">-PricingTier</span></span>
<span data-ttu-id="289a9-122">Tipo de preço.</span><span class="sxs-lookup"><span data-stu-id="289a9-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="289a9-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="289a9-123">-Confirm</span></span>
<span data-ttu-id="289a9-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="289a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="289a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="289a9-125">-WhatIf</span></span>
<span data-ttu-id="289a9-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="289a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="289a9-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="289a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="289a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289a9-128">CommonParameters</span></span>
<span data-ttu-id="289a9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="289a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289a9-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289a9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289a9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="289a9-131">INPUTS</span></span>

### <span data-ttu-id="289a9-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="289a9-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="289a9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="289a9-133">OUTPUTS</span></span>

### <span data-ttu-id="289a9-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="289a9-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="289a9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="289a9-135">NOTES</span></span>

## <span data-ttu-id="289a9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="289a9-136">RELATED LINKS</span></span>
