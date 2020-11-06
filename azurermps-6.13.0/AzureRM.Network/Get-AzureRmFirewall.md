---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610561"
---
# Get-AzureRmFirewall

## Sinopse
Obtém um firewall do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmFirewall** Obtém um ou mais firewalls em um grupo de recursos.

## EXEMPLOS

### 1: recuperar todos os firewalls em um grupo de recursos
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

Este exemplo recupera todos os firewalls no grupo de recursos "rgName".

### 2: recuperar um firewall por nome
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

Este exemplo recupera o firewall chamado "azFw" no grupo de recursos "rgName".

### 3: recuperar um firewall e adicionar uma coleção de regras de aplicativo ao firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

Este exemplo recupera um firewall e, em seguida, adiciona um conjunto de regras de aplicativo ao firewall chamando o método AddApplicationRuleCollection.

### 4: recuperar um firewall e adicionar uma coleção de regras de rede ao firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

Este exemplo recupera um firewall e, em seguida, adiciona um conjunto de regras de rede ao firewall chamando o método AddNetworkRuleCollection.

### 5: recuperar um firewall e recuperar uma coleção de regras de aplicativo por nome do firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetApplicationRuleCollectionByName no objeto de firewall. O nome da coleção de regras para o método GetApplicationRuleCollectionByName não diferencia maiúsculas de minúsculas.

### 6: recuperar um firewall e recuperar uma coleção de regras de rede por nome do firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetNetworkRuleCollectionByName no objeto de firewall. O nome da coleção de regras para o método GetNetworkRuleCollectionByName não diferencia maiúsculas de minúsculas.

### 7: recuperar um firewall e remover uma coleção de regras de aplicativo por nome do firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

Este exemplo recupera um firewall e, em seguida, remove uma coleção de regras por nome, método de chamada RemoveApplicationRuleCollectionByName no objeto de firewall. O nome da coleção de regras para o método RemoveApplicationRuleCollectionByName não diferencia maiúsculas de minúsculas.

### 8: recuperar um firewall e remover uma coleção de regras de rede por nome do firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Este exemplo recupera um firewall e, em seguida, remove uma coleção de regras por nome, método de chamada RemoveNetworkRuleCollectionByName no objeto de firewall. O nome da coleção de regras para o método RemoveNetworkRuleCollectionByName não diferencia maiúsculas de minúsculas.

### 9: recuperar um firewall e depois atribuir o firewall
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

Este exemplo recupera um firewall e chama Allocate no firewall para iniciar o serviço de firewall usando a configuração (coleções de regras de aplicativo e de rede) associadas ao firewall.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do firewall que este cmdlet obtém.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o firewall pertence.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
