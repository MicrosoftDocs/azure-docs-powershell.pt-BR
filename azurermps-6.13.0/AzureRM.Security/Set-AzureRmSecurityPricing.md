---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430028"
---
# <span data-ttu-id="e8ba0-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e8ba0-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="e8ba0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba0-103">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ba0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8ba0-104">SYNTAX</span></span>

### <span data-ttu-id="e8ba0-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8ba0-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8ba0-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ba0-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ba0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8ba0-108">DESCRIPTION</span></span>
<span data-ttu-id="e8ba0-109">Define o preço do nível da central de segurança do Azure para um escopo.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="e8ba0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8ba0-110">EXAMPLES</span></span>

### <span data-ttu-id="e8ba0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8ba0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="e8ba0-112">Define o tipo de preço da central de segurança do Azure de assinatura como "padrão"</span><span class="sxs-lookup"><span data-stu-id="e8ba0-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="e8ba0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8ba0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="e8ba0-114">Define o tipo de preço da central de segurança do grupo de recursos "myService1" do Azure para "padrão"</span><span class="sxs-lookup"><span data-stu-id="e8ba0-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="e8ba0-115">OS</span><span class="sxs-lookup"><span data-stu-id="e8ba0-115">PARAMETERS</span></span>

### <span data-ttu-id="e8ba0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba0-116">-DefaultProfile</span></span>
<span data-ttu-id="e8ba0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ba0-118">-InputObject</span></span>
<span data-ttu-id="e8ba0-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8ba0-120">-Name</span></span>
<span data-ttu-id="e8ba0-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="e8ba0-122">-PricingTier</span></span>
<span data-ttu-id="e8ba0-123">Tipo de preço.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ba0-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8ba0-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8ba0-126">-Confirm</span></span>
<span data-ttu-id="e8ba0-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba0-128">-WhatIf</span></span>
<span data-ttu-id="e8ba0-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ba0-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba0-131">CommonParameters</span></span>
<span data-ttu-id="e8ba0-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba0-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ba0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba0-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8ba0-134">INPUTS</span></span>

### <span data-ttu-id="e8ba0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ba0-135">System.String</span></span>
<span data-ttu-id="e8ba0-136">Microsoft. Azure. Commands. Security. cmdlets. pricings. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="e8ba0-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="e8ba0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8ba0-137">OUTPUTS</span></span>

### <span data-ttu-id="e8ba0-138">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="e8ba0-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="e8ba0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8ba0-139">NOTES</span></span>

## <span data-ttu-id="e8ba0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8ba0-140">RELATED LINKS</span></span>
