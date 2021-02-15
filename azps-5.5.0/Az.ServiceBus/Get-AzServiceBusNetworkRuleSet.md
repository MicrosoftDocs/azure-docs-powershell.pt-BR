---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118678"
---
# <span data-ttu-id="1ef49-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ef49-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="1ef49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ef49-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef49-103">Obtém os detalhes de um NetworkruleSet de Hubs de Eventos do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef49-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1ef49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ef49-104">SYNTAX</span></span>

### <span data-ttu-id="1ef49-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ef49-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ef49-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1ef49-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ef49-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ef49-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ef49-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ef49-108">DESCRIPTION</span></span>
<span data-ttu-id="1ef49-109">Obtém os detalhes de um NetworkruleSet de Hubs de Eventos do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef49-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="1ef49-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ef49-110">EXAMPLES</span></span>

### <span data-ttu-id="1ef49-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ef49-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="1ef49-112">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="1ef49-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1ef49-113">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando parâmetros ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="1ef49-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="1ef49-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1ef49-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="1ef49-115">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="1ef49-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1ef49-116">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando o Namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1ef49-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="1ef49-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1ef49-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="1ef49-118">Nome : DefaultAction padrão: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvgroupst1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="1ef49-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="1ef49-119">Obter os detalhes do NetworkruleSet de Hubs de Eventos do namespace usando a ID de Recurso de outro Namespace</span><span class="sxs-lookup"><span data-stu-id="1ef49-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="1ef49-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ef49-120">PARAMETERS</span></span>

### <span data-ttu-id="1ef49-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef49-121">-DefaultProfile</span></span>
<span data-ttu-id="1ef49-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef49-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ef49-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ef49-123">-Namespace</span></span>
<span data-ttu-id="1ef49-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="1ef49-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef49-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ef49-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ef49-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1ef49-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef49-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ef49-127">-ResourceId</span></span>
<span data-ttu-id="1ef49-128">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="1ef49-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="1ef49-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef49-129">CommonParameters</span></span>
<span data-ttu-id="1ef49-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef49-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1ef49-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef49-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef49-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ef49-132">INPUTS</span></span>

### <span data-ttu-id="1ef49-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1ef49-133">System.String</span></span>

## <span data-ttu-id="1ef49-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ef49-134">OUTPUTS</span></span>

### <span data-ttu-id="1ef49-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1ef49-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1ef49-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1ef49-136">NOTES</span></span>

## <span data-ttu-id="1ef49-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ef49-137">RELATED LINKS</span></span>