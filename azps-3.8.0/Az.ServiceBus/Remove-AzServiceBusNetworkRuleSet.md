---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941295"
---
# <span data-ttu-id="755af-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="755af-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="755af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="755af-102">SYNOPSIS</span></span>
<span data-ttu-id="755af-103">Remove o NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="755af-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="755af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="755af-104">SYNTAX</span></span>

### <span data-ttu-id="755af-105">NetworkRuleSetPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="755af-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755af-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="755af-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755af-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="755af-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="755af-108">DESCRIPTION</span></span>
<span data-ttu-id="755af-109">Remove o NetworkRuleSet para o namespace especificado</span><span class="sxs-lookup"><span data-stu-id="755af-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="755af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="755af-110">EXAMPLES</span></span>

### <span data-ttu-id="755af-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="755af-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="755af-112">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft. ServiceBus/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="755af-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="755af-113">Exclui o NetworkRuleSet para o namespace "ServiceBus-Namespace1-1375" especificado</span><span class="sxs-lookup"><span data-stu-id="755af-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="755af-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="755af-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="755af-115">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="755af-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="755af-116">Exclui o NetworkRuleSet usando InputObject</span><span class="sxs-lookup"><span data-stu-id="755af-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="755af-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="755af-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="755af-118">Nome: DefaultAction padrão: allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default tipo: Microsoft. EventHub/namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="755af-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="755af-119">Exclui o NetworkRuleSet usando o ResourceId do namespace</span><span class="sxs-lookup"><span data-stu-id="755af-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="755af-120">OS</span><span class="sxs-lookup"><span data-stu-id="755af-120">PARAMETERS</span></span>

### <span data-ttu-id="755af-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755af-121">-AsJob</span></span>
<span data-ttu-id="755af-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="755af-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="755af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755af-123">-DefaultProfile</span></span>
<span data-ttu-id="755af-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="755af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755af-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="755af-125">-InputObject</span></span>
<span data-ttu-id="755af-126">Objeto namespace</span><span class="sxs-lookup"><span data-stu-id="755af-126">Namespace Object</span></span>

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

### <span data-ttu-id="755af-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="755af-127">-Name</span></span>
<span data-ttu-id="755af-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="755af-128">Namespace Name</span></span>

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

### <span data-ttu-id="755af-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="755af-129">-PassThru</span></span>
<span data-ttu-id="755af-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="755af-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="755af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755af-131">-ResourceGroupName</span></span>
<span data-ttu-id="755af-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="755af-132">Resource Group Name</span></span>

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

### <span data-ttu-id="755af-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="755af-133">-ResourceId</span></span>
<span data-ttu-id="755af-134">ID do recurso namespace</span><span class="sxs-lookup"><span data-stu-id="755af-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="755af-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="755af-135">-Confirm</span></span>
<span data-ttu-id="755af-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755af-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755af-137">-WhatIf</span></span>
<span data-ttu-id="755af-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="755af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755af-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="755af-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755af-140">CommonParameters</span></span>
<span data-ttu-id="755af-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="755af-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755af-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755af-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="755af-143">INPUTS</span></span>

### <span data-ttu-id="755af-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="755af-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="755af-145">System. String</span><span class="sxs-lookup"><span data-stu-id="755af-145">System.String</span></span>

## <span data-ttu-id="755af-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="755af-146">OUTPUTS</span></span>

### <span data-ttu-id="755af-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="755af-147">System.Boolean</span></span>

## <span data-ttu-id="755af-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="755af-148">NOTES</span></span>

## <span data-ttu-id="755af-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="755af-149">RELATED LINKS</span></span>
