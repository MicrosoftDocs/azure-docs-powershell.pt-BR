---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 6b01211b7efa20983f868c7e70e54be02d5ad5c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891847"
---
# <span data-ttu-id="80f2e-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="80f2e-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="80f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="80f2e-103">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="80f2e-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="80f2e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80f2e-104">SYNTAX</span></span>

### <span data-ttu-id="80f2e-105">IPRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80f2e-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f2e-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f2e-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80f2e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="80f2e-108">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="80f2e-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="80f2e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80f2e-109">EXAMPLES</span></span>

### <span data-ttu-id="80f2e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80f2e-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="80f2e-111">Nome : DefaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="80f2e-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="80f2e-112">adicione o IPRule com IpMask "11.22.33.44" e Action Allow para o namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="80f2e-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="80f2e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80f2e-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="80f2e-114">Nome : DefaultAction padrão : Permitir Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="80f2e-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="80f2e-115">adicione o IPRule com IpMask "11.22.33.44" e Action Allow para o namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="80f2e-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="80f2e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80f2e-116">PARAMETERS</span></span>

### <span data-ttu-id="80f2e-117">-Action</span><span class="sxs-lookup"><span data-stu-id="80f2e-117">-Action</span></span>
<span data-ttu-id="80f2e-118">A ação de filtro IP</span><span class="sxs-lookup"><span data-stu-id="80f2e-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f2e-119">-DefaultProfile</span></span>
<span data-ttu-id="80f2e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80f2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80f2e-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="80f2e-121">-IpMask</span></span>
<span data-ttu-id="80f2e-122">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="80f2e-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f2e-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="80f2e-123">-IpRuleObject</span></span>
<span data-ttu-id="80f2e-124">Objeto de configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="80f2e-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f2e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="80f2e-125">-Name</span></span>
<span data-ttu-id="80f2e-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="80f2e-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f2e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f2e-127">-ResourceGroupName</span></span>
<span data-ttu-id="80f2e-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="80f2e-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f2e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80f2e-129">-Confirm</span></span>
<span data-ttu-id="80f2e-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80f2e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f2e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f2e-131">-WhatIf</span></span>
<span data-ttu-id="80f2e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80f2e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f2e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80f2e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f2e-134">CommonParameters</span></span>
<span data-ttu-id="80f2e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80f2e-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f2e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f2e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80f2e-137">INPUTS</span></span>

### <span data-ttu-id="80f2e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="80f2e-138">System.String</span></span>

### <span data-ttu-id="80f2e-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="80f2e-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="80f2e-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80f2e-140">OUTPUTS</span></span>

### <span data-ttu-id="80f2e-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="80f2e-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="80f2e-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="80f2e-142">NOTES</span></span>

## <span data-ttu-id="80f2e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80f2e-143">RELATED LINKS</span></span>
