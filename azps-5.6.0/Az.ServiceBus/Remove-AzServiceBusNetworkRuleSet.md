---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901574"
---
# <span data-ttu-id="22c1f-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="22c1f-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="22c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="22c1f-103">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="22c1f-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="22c1f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="22c1f-104">SYNTAX</span></span>

### <span data-ttu-id="22c1f-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="22c1f-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c1f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22c1f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c1f-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22c1f-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c1f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="22c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="22c1f-109">Remove o NetworkRuleSet para o Namespace Dado</span><span class="sxs-lookup"><span data-stu-id="22c1f-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="22c1f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="22c1f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22c1f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="22c1f-112">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="22c1f-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="22c1f-113">Exclui o networkRuleSet para o namespace "ServiceBus-Namespace1-1375" dado</span><span class="sxs-lookup"><span data-stu-id="22c1f-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="22c1f-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22c1f-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="22c1f-115">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="22c1f-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="22c1f-116">Exclui o NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="22c1f-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="22c1f-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="22c1f-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="22c1f-118">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="22c1f-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="22c1f-119">Exclui o NetworkRuleSet usando ResourceId do Namespace</span><span class="sxs-lookup"><span data-stu-id="22c1f-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="22c1f-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="22c1f-120">PARAMETERS</span></span>

### <span data-ttu-id="22c1f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22c1f-121">-AsJob</span></span>
<span data-ttu-id="22c1f-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="22c1f-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c1f-123">-DefaultProfile</span></span>
<span data-ttu-id="22c1f-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22c1f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c1f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22c1f-125">-InputObject</span></span>
<span data-ttu-id="22c1f-126">Objeto Namespace</span><span class="sxs-lookup"><span data-stu-id="22c1f-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="22c1f-127">-Name</span></span>
<span data-ttu-id="22c1f-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="22c1f-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22c1f-129">-PassThru</span></span>
<span data-ttu-id="22c1f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="22c1f-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c1f-131">-ResourceGroupName</span></span>
<span data-ttu-id="22c1f-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="22c1f-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22c1f-133">-ResourceId</span></span>
<span data-ttu-id="22c1f-134">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="22c1f-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c1f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22c1f-135">-Confirm</span></span>
<span data-ttu-id="22c1f-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c1f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c1f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c1f-137">-WhatIf</span></span>
<span data-ttu-id="22c1f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22c1f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c1f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22c1f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c1f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c1f-140">CommonParameters</span></span>
<span data-ttu-id="22c1f-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c1f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="22c1f-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c1f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c1f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22c1f-143">INPUTS</span></span>

### <span data-ttu-id="22c1f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="22c1f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="22c1f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="22c1f-145">System.String</span></span>

## <span data-ttu-id="22c1f-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="22c1f-146">OUTPUTS</span></span>

### <span data-ttu-id="22c1f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22c1f-147">System.Boolean</span></span>

## <span data-ttu-id="22c1f-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="22c1f-148">NOTES</span></span>

## <span data-ttu-id="22c1f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22c1f-149">RELATED LINKS</span></span>
