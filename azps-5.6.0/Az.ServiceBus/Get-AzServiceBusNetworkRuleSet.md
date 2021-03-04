---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 1183ba239ee86f8b587777f26cc3f04154fb5b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890724"
---
# <span data-ttu-id="d645e-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d645e-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="d645e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d645e-102">SYNOPSIS</span></span>
<span data-ttu-id="d645e-103">Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d645e-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d645e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d645e-104">SYNTAX</span></span>

### <span data-ttu-id="d645e-105">NetworkRuleSetPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d645e-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d645e-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d645e-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d645e-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d645e-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d645e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d645e-108">DESCRIPTION</span></span>
<span data-ttu-id="d645e-109">Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d645e-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d645e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d645e-110">EXAMPLES</span></span>

### <span data-ttu-id="d645e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d645e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="d645e-112">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="d645e-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="d645e-113">Obter os detalhes de Event Hubs NetworkruleSet do namespace usando parâmetros ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="d645e-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="d645e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d645e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="d645e-115">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="d645e-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="d645e-116">Obter os detalhes de Event Hubs NetworkruleSet do namespace usando Namespace que está na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d645e-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="d645e-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d645e-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="d645e-118">Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="d645e-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="d645e-119">Obter os detalhes de Hubs de Eventos NetworkruleSet do namespace usando a ID de Recurso de outro Namespace</span><span class="sxs-lookup"><span data-stu-id="d645e-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="d645e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d645e-120">PARAMETERS</span></span>

### <span data-ttu-id="d645e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d645e-121">-DefaultProfile</span></span>
<span data-ttu-id="d645e-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d645e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d645e-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d645e-123">-Namespace</span></span>
<span data-ttu-id="d645e-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d645e-124">Namespace Name</span></span>

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

### <span data-ttu-id="d645e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d645e-125">-ResourceGroupName</span></span>
<span data-ttu-id="d645e-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d645e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d645e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d645e-127">-ResourceId</span></span>
<span data-ttu-id="d645e-128">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="d645e-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d645e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d645e-129">CommonParameters</span></span>
<span data-ttu-id="d645e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d645e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d645e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d645e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d645e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d645e-132">INPUTS</span></span>

### <span data-ttu-id="d645e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d645e-133">System.String</span></span>

## <span data-ttu-id="d645e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d645e-134">OUTPUTS</span></span>

### <span data-ttu-id="d645e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d645e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d645e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d645e-136">NOTES</span></span>

## <span data-ttu-id="d645e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d645e-137">RELATED LINKS</span></span>