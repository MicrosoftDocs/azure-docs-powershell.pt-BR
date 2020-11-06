---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 824c1ea3462b2a15e74ca4c02eb69fe566f97d78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596502"
---
# <span data-ttu-id="1b440-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="1b440-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="1b440-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b440-102">SYNOPSIS</span></span>
<span data-ttu-id="1b440-103">Adicionar uma única regra de IP à NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="1b440-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1b440-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b440-104">SYNTAX</span></span>

### <span data-ttu-id="1b440-105">IPRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b440-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b440-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b440-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b440-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b440-107">DESCRIPTION</span></span>
<span data-ttu-id="1b440-108">Adicionar uma única regra de IP à NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="1b440-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="1b440-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b440-109">EXAMPLES</span></span>

### <span data-ttu-id="1b440-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b440-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="1b440-111">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="1b440-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="1b440-112">Adicione o IPRule com IpMask "11.22.33.44" e a ação permitir para o namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="1b440-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="1b440-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1b440-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="1b440-114">Nome: DefaultAction padrão: allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="1b440-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="1b440-115">Adicione o IPRule com IpMask "11.22.33.44" e a ação permitir para o namespace fornecido.</span><span class="sxs-lookup"><span data-stu-id="1b440-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="1b440-116">OS</span><span class="sxs-lookup"><span data-stu-id="1b440-116">PARAMETERS</span></span>

### <span data-ttu-id="1b440-117">-Ação</span><span class="sxs-lookup"><span data-stu-id="1b440-117">-Action</span></span>
<span data-ttu-id="1b440-118">A ação de filtro IP</span><span class="sxs-lookup"><span data-stu-id="1b440-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="1b440-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b440-119">-DefaultProfile</span></span>
<span data-ttu-id="1b440-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b440-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b440-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="1b440-121">-IpMask</span></span>
<span data-ttu-id="1b440-122">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="1b440-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="1b440-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1b440-123">-IpRuleObject</span></span>
<span data-ttu-id="1b440-124">Objeto de configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="1b440-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="1b440-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b440-125">-Name</span></span>
<span data-ttu-id="1b440-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="1b440-126">Namespace Name</span></span>

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

### <span data-ttu-id="1b440-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b440-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b440-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1b440-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1b440-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b440-129">-Confirm</span></span>
<span data-ttu-id="1b440-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b440-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b440-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b440-131">-WhatIf</span></span>
<span data-ttu-id="1b440-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b440-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b440-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b440-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b440-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b440-134">CommonParameters</span></span>
<span data-ttu-id="1b440-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b440-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1b440-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b440-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b440-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b440-137">INPUTS</span></span>

### <span data-ttu-id="1b440-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b440-138">System.String</span></span>

### <span data-ttu-id="1b440-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1b440-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="1b440-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b440-140">OUTPUTS</span></span>

### <span data-ttu-id="1b440-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1b440-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1b440-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b440-142">NOTES</span></span>

## <span data-ttu-id="1b440-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b440-143">RELATED LINKS</span></span>
