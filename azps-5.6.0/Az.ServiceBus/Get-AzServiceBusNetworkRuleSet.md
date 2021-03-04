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
# Get-AzServiceBusNetworkRuleSet

## SYNOPSIS
Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.

## SINTAXE

### NetworkRuleSetPropertiesSet (Padrão)
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NetworkRuleSetNamespacePropertiesSet
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NetworkRuleSetResourceIdParameterSet
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
Obtém os detalhes de um Event Hubs NetworkruleSet do namespace na assinatura atual do Azure.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}

Obter os detalhes de Event Hubs NetworkruleSet do namespace usando parâmetros ResourceGroup e Namespace. 

### Exemplo 2
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}

Obter os detalhes de Event Hubs NetworkruleSet do namespace usando Namespace que está na assinatura atual.

### Exemplo 3
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

Nome : defaultAction padrão : Permitir Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}

Obter os detalhes de Hubs de Eventos NetworkruleSet do namespace usando a ID de Recurso de outro Namespace 

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Namespace
Namespace Name

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

### -ResourceGroupName
Nome do Grupo de Recursos

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

### -ResourceId
Namespace Resource Id

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes

## NOTES

## LINKS RELACIONADOS