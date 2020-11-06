---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599162"
---
# <span data-ttu-id="2f1ef-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f1ef-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="2f1ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1ef-103">Remove o NetwrokRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="2f1ef-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="2f1ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f1ef-104">SYNTAX</span></span>

### <span data-ttu-id="2f1ef-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f1ef-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f1ef-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f1ef-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f1ef-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f1ef-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f1ef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f1ef-108">DESCRIPTION</span></span>
<span data-ttu-id="2f1ef-109">Remove o NetwrokRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="2f1ef-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="2f1ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f1ef-110">EXAMPLES</span></span>

### <span data-ttu-id="2f1ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f1ef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="2f1ef-112">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="2f1ef-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="2f1ef-113">Exclui o NetwrokRuleSet de um determinado "ServiceBus-Namespace1-1375" namesapce</span><span class="sxs-lookup"><span data-stu-id="2f1ef-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="2f1ef-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f1ef-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="2f1ef-115">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="2f1ef-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="2f1ef-116">Exclui o NetwrokRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="2f1ef-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="2f1ef-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2f1ef-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="2f1ef-118">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="2f1ef-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="2f1ef-119">Exclui o NetwrokRuleSet usando o ResourceId do namepsace</span><span class="sxs-lookup"><span data-stu-id="2f1ef-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="2f1ef-120">OS</span><span class="sxs-lookup"><span data-stu-id="2f1ef-120">PARAMETERS</span></span>

### <span data-ttu-id="2f1ef-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f1ef-121">-AsJob</span></span>
<span data-ttu-id="2f1ef-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2f1ef-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f1ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1ef-123">-DefaultProfile</span></span>
<span data-ttu-id="2f1ef-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1ef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f1ef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f1ef-125">-InputObject</span></span>
<span data-ttu-id="2f1ef-126">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="2f1ef-126">Namespace Object</span></span>

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

### <span data-ttu-id="2f1ef-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f1ef-127">-Name</span></span>
<span data-ttu-id="2f1ef-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2f1ef-128">Namespace Name</span></span>

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

### <span data-ttu-id="2f1ef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f1ef-129">-PassThru</span></span>
<span data-ttu-id="2f1ef-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="2f1ef-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f1ef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1ef-131">-ResourceGroupName</span></span>
<span data-ttu-id="2f1ef-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2f1ef-132">Resource Group Name</span></span>

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

### <span data-ttu-id="2f1ef-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f1ef-133">-ResourceId</span></span>
<span data-ttu-id="2f1ef-134">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="2f1ef-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2f1ef-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f1ef-135">-Confirm</span></span>
<span data-ttu-id="2f1ef-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f1ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f1ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f1ef-137">-WhatIf</span></span>
<span data-ttu-id="2f1ef-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f1ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f1ef-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f1ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f1ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1ef-140">CommonParameters</span></span>
<span data-ttu-id="2f1ef-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2f1ef-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1ef-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1ef-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f1ef-143">INPUTS</span></span>

### <span data-ttu-id="2f1ef-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2f1ef-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="2f1ef-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2f1ef-145">System.String</span></span>

## <span data-ttu-id="2f1ef-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f1ef-146">OUTPUTS</span></span>

### <span data-ttu-id="2f1ef-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1ef-147">System.Boolean</span></span>

## <span data-ttu-id="2f1ef-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f1ef-148">NOTES</span></span>

## <span data-ttu-id="2f1ef-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f1ef-149">RELATED LINKS</span></span>
