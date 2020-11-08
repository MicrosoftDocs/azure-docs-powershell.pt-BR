---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114980"
---
# <span data-ttu-id="d14a7-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="d14a7-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="d14a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d14a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d14a7-103">Adicionar uma única regra de IP à NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="d14a7-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="d14a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d14a7-104">SYNTAX</span></span>

### <span data-ttu-id="d14a7-105">IPRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d14a7-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d14a7-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d14a7-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d14a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d14a7-107">DESCRIPTION</span></span>
<span data-ttu-id="d14a7-108">Adicionar uma única regra de IP à NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="d14a7-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="d14a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d14a7-109">EXAMPLES</span></span>

### <span data-ttu-id="d14a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d14a7-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="d14a7-111">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="d14a7-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="d14a7-112">Adicione o IPRule com IpMask "11.22.33.44" e a ação permitir para o namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="d14a7-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="d14a7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d14a7-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="d14a7-114">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="d14a7-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="d14a7-115">Adicione o IPRule com IpMask "11.22.33.44" e a ação permitir para o namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="d14a7-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="d14a7-116">OS</span><span class="sxs-lookup"><span data-stu-id="d14a7-116">PARAMETERS</span></span>

### <span data-ttu-id="d14a7-117">-Ação</span><span class="sxs-lookup"><span data-stu-id="d14a7-117">-Action</span></span>
<span data-ttu-id="d14a7-118">A ação de filtro IP</span><span class="sxs-lookup"><span data-stu-id="d14a7-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="d14a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14a7-119">-DefaultProfile</span></span>
<span data-ttu-id="d14a7-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d14a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d14a7-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="d14a7-121">-IpMask</span></span>
<span data-ttu-id="d14a7-122">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="d14a7-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="d14a7-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d14a7-123">-IpRuleObject</span></span>
<span data-ttu-id="d14a7-124">Objeto de configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="d14a7-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="d14a7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d14a7-125">-Name</span></span>
<span data-ttu-id="d14a7-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="d14a7-126">Namespace Name</span></span>

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

### <span data-ttu-id="d14a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="d14a7-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d14a7-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d14a7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d14a7-129">-Confirm</span></span>
<span data-ttu-id="d14a7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d14a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d14a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d14a7-131">-WhatIf</span></span>
<span data-ttu-id="d14a7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d14a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d14a7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d14a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d14a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14a7-134">CommonParameters</span></span>
<span data-ttu-id="d14a7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d14a7-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d14a7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14a7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d14a7-137">INPUTS</span></span>

### <span data-ttu-id="d14a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d14a7-138">System.String</span></span>

### <span data-ttu-id="d14a7-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d14a7-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="d14a7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d14a7-140">OUTPUTS</span></span>

### <span data-ttu-id="d14a7-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d14a7-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d14a7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d14a7-142">NOTES</span></span>

## <span data-ttu-id="d14a7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d14a7-143">RELATED LINKS</span></span>
