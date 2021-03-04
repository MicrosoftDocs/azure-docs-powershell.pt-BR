---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: f55c42178daacdbf2be80982fb151514372d2d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889736"
---
# <span data-ttu-id="f4f19-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="f4f19-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="f4f19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f19-102">SYNOPSIS</span></span>

<span data-ttu-id="f4f19-103">Habilita ou desabilita os planos do Azure Defender para uma assinatura no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f19-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="f4f19-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4f19-104">SYNTAX</span></span>

### <span data-ttu-id="f4f19-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4f19-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4f19-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f19-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f19-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4f19-107">DESCRIPTION</span></span>

<span data-ttu-id="f4f19-108">Habilitar ou desabilitar qualquer um dos planos do Azure Defender para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4f19-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="f4f19-109">Para obter detalhes sobre o Azure Defender e os planos disponíveis, consulte [Introdução ao Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="f4f19-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="f4f19-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4f19-110">EXAMPLES</span></span>

### <span data-ttu-id="f4f19-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4f19-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="f4f19-112">Habilita **o Azure Defender para servidores** para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4f19-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="f4f19-113">"Standard" refere-se ao estado "On" de um plano do Azure Defender, conforme mostrado na área de preços e configurações do Azure Security Center do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f19-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="f4f19-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4f19-114">PARAMETERS</span></span>

### <span data-ttu-id="f4f19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f19-115">-DefaultProfile</span></span>

<span data-ttu-id="f4f19-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f19-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f19-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f19-117">-InputObject</span></span>

<span data-ttu-id="f4f19-118">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="f4f19-118">Input Object.</span></span>

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

### <span data-ttu-id="f4f19-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f4f19-119">-Name</span></span>

<span data-ttu-id="f4f19-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f4f19-120">Resource name.</span></span>

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

### <span data-ttu-id="f4f19-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="f4f19-121">-PricingTier</span></span>

<span data-ttu-id="f4f19-122">Camada de preços.</span><span class="sxs-lookup"><span data-stu-id="f4f19-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="f4f19-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4f19-123">-Confirm</span></span>

<span data-ttu-id="f4f19-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f19-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f19-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f19-125">-WhatIf</span></span>

<span data-ttu-id="f4f19-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4f19-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4f19-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4f19-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f19-128">CommonParameters</span></span>

<span data-ttu-id="f4f19-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f19-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4f19-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f19-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f19-131">INPUTS</span></span>

### <span data-ttu-id="f4f19-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="f4f19-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="f4f19-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4f19-133">OUTPUTS</span></span>

### <span data-ttu-id="f4f19-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="f4f19-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="f4f19-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4f19-135">NOTES</span></span>

## <span data-ttu-id="f4f19-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4f19-136">RELATED LINKS</span></span>
