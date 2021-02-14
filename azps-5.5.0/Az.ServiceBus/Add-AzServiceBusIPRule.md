---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117141"
---
# <span data-ttu-id="adfe0-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="adfe0-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="adfe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="adfe0-103">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="adfe0-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="adfe0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adfe0-104">SYNTAX</span></span>

### <span data-ttu-id="adfe0-105">IPRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="adfe0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adfe0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adfe0-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adfe0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="adfe0-107">DESCRIPTION</span></span>
<span data-ttu-id="adfe0-108">Adicionar uma única regra IP ao NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="adfe0-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="adfe0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="adfe0-109">EXAMPLES</span></span>

### <span data-ttu-id="adfe0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adfe0-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="adfe0-111">Nome : DefaultAction padrão: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="adfe0-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="adfe0-112">adicione o IPRule com IpMask "11.22.33.44" e a Ação Permitir até o namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="adfe0-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="adfe0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="adfe0-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="adfe0-114">Nome : DefaultAction padrão: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="adfe0-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="adfe0-115">adicione o IPRule com IpMask "11.22.33.44" e a Ação Permitir até o namespace determinado.</span><span class="sxs-lookup"><span data-stu-id="adfe0-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="adfe0-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adfe0-116">PARAMETERS</span></span>

### <span data-ttu-id="adfe0-117">-Ação</span><span class="sxs-lookup"><span data-stu-id="adfe0-117">-Action</span></span>
<span data-ttu-id="adfe0-118">A Ação de Filtro IP</span><span class="sxs-lookup"><span data-stu-id="adfe0-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="adfe0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfe0-119">-DefaultProfile</span></span>
<span data-ttu-id="adfe0-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adfe0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adfe0-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="adfe0-121">-IpMask</span></span>
<span data-ttu-id="adfe0-122">ID do Recurso da Sub-rede</span><span class="sxs-lookup"><span data-stu-id="adfe0-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="adfe0-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="adfe0-123">-IpRuleObject</span></span>
<span data-ttu-id="adfe0-124">Objeto de Configuração IPRule a ser adicionado</span><span class="sxs-lookup"><span data-stu-id="adfe0-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adfe0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="adfe0-125">-Name</span></span>
<span data-ttu-id="adfe0-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="adfe0-126">Namespace Name</span></span>

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

### <span data-ttu-id="adfe0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfe0-127">-ResourceGroupName</span></span>
<span data-ttu-id="adfe0-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="adfe0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="adfe0-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="adfe0-129">-Confirm</span></span>
<span data-ttu-id="adfe0-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adfe0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adfe0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adfe0-131">-WhatIf</span></span>
<span data-ttu-id="adfe0-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="adfe0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adfe0-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adfe0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adfe0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfe0-134">CommonParameters</span></span>
<span data-ttu-id="adfe0-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adfe0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="adfe0-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adfe0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfe0-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="adfe0-137">INPUTS</span></span>

### <span data-ttu-id="adfe0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="adfe0-138">System.String</span></span>

### <span data-ttu-id="adfe0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="adfe0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="adfe0-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="adfe0-140">OUTPUTS</span></span>

### <span data-ttu-id="adfe0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="adfe0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="adfe0-142">Notas</span><span class="sxs-lookup"><span data-stu-id="adfe0-142">NOTES</span></span>

## <span data-ttu-id="adfe0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adfe0-143">RELATED LINKS</span></span>