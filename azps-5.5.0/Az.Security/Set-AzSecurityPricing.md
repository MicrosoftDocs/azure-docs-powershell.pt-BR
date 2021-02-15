---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112609"
---
# <span data-ttu-id="184a1-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="184a1-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="184a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="184a1-102">SYNOPSIS</span></span>

<span data-ttu-id="184a1-103">Habilita ou desabilita os planos do Azure Defender para uma assinatura no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="184a1-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="184a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="184a1-104">SYNTAX</span></span>

### <span data-ttu-id="184a1-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="184a1-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184a1-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="184a1-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184a1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="184a1-107">DESCRIPTION</span></span>

<span data-ttu-id="184a1-108">Habilitar ou desabilitar qualquer um dos planos do Azure Defender para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="184a1-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="184a1-109">Para obter detalhes sobre o Azure Defender e os planos disponíveis, consulte [Introdução ao Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="184a1-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="184a1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="184a1-110">EXAMPLES</span></span>

### <span data-ttu-id="184a1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="184a1-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="184a1-112">**Habilita o Azure Defender para servidores** para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="184a1-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="184a1-113">"Padrão" refere-se ao estado "On" de um plano do Azure Defender, conforme mostrado na área de preços e configurações do Azure Security Center do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="184a1-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="184a1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="184a1-114">PARAMETERS</span></span>

### <span data-ttu-id="184a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184a1-115">-DefaultProfile</span></span>

<span data-ttu-id="184a1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="184a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184a1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184a1-117">-InputObject</span></span>

<span data-ttu-id="184a1-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="184a1-118">Input Object.</span></span>

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

### <span data-ttu-id="184a1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="184a1-119">-Name</span></span>

<span data-ttu-id="184a1-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="184a1-120">Resource name.</span></span>

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

### <span data-ttu-id="184a1-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="184a1-121">-PricingTier</span></span>

<span data-ttu-id="184a1-122">Nível de preço.</span><span class="sxs-lookup"><span data-stu-id="184a1-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="184a1-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="184a1-123">-Confirm</span></span>

<span data-ttu-id="184a1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="184a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184a1-125">-WhatIf</span></span>

<span data-ttu-id="184a1-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="184a1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="184a1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="184a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184a1-128">CommonParameters</span></span>

<span data-ttu-id="184a1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184a1-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="184a1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184a1-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="184a1-131">INPUTS</span></span>

### <span data-ttu-id="184a1-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="184a1-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="184a1-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="184a1-133">OUTPUTS</span></span>

### <span data-ttu-id="184a1-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="184a1-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="184a1-135">Notas</span><span class="sxs-lookup"><span data-stu-id="184a1-135">NOTES</span></span>

## <span data-ttu-id="184a1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="184a1-136">RELATED LINKS</span></span>
