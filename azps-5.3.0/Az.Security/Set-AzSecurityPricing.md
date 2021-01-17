---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433237"
---
# <span data-ttu-id="325e7-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="325e7-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="325e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="325e7-102">SYNOPSIS</span></span>

<span data-ttu-id="325e7-103">Habilita ou desabilita os planos do Azure defender para uma assinatura na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="325e7-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="325e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="325e7-104">SYNTAX</span></span>

### <span data-ttu-id="325e7-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="325e7-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325e7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="325e7-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="325e7-107">DESCRIPTION</span></span>

<span data-ttu-id="325e7-108">Habilite ou desabilite qualquer um dos planos do Azure defender para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="325e7-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="325e7-109">Para obter detalhes sobre o Azure defender e os planos disponíveis, consulte [introdução ao Azure defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="325e7-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="325e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="325e7-110">EXAMPLES</span></span>

### <span data-ttu-id="325e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="325e7-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="325e7-112">Habilita o **Azure defender para servidores** para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="325e7-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="325e7-113">"Padrão" refere-se ao estado "ligado" para um plano do Azure defender, conforme mostrado na área de preços e configurações da central de segurança do Azure do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="325e7-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="325e7-114">OS</span><span class="sxs-lookup"><span data-stu-id="325e7-114">PARAMETERS</span></span>

### <span data-ttu-id="325e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325e7-115">-DefaultProfile</span></span>

<span data-ttu-id="325e7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="325e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325e7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="325e7-117">-InputObject</span></span>

<span data-ttu-id="325e7-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="325e7-118">Input Object.</span></span>

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

### <span data-ttu-id="325e7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="325e7-119">-Name</span></span>

<span data-ttu-id="325e7-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="325e7-120">Resource name.</span></span>

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

### <span data-ttu-id="325e7-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="325e7-121">-PricingTier</span></span>

<span data-ttu-id="325e7-122">Tipo de preço.</span><span class="sxs-lookup"><span data-stu-id="325e7-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="325e7-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="325e7-123">-Confirm</span></span>

<span data-ttu-id="325e7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="325e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325e7-125">-WhatIf</span></span>

<span data-ttu-id="325e7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="325e7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="325e7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="325e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325e7-128">CommonParameters</span></span>

<span data-ttu-id="325e7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325e7-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="325e7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325e7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="325e7-131">INPUTS</span></span>

### <span data-ttu-id="325e7-132">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="325e7-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="325e7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="325e7-133">OUTPUTS</span></span>

### <span data-ttu-id="325e7-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="325e7-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="325e7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="325e7-135">NOTES</span></span>

## <span data-ttu-id="325e7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="325e7-136">RELATED LINKS</span></span>
