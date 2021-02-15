---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114097"
---
# Set-AzFirewall

## Sinopse
Salva um Firewall modificado.

## Sintaxe

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzFirewall** atualiza um Firewall do Azure.

## Exemplos

### 1: Prioridade de atualização de um conjunto de regras do aplicativo Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Este exemplo atualiza a prioridade de um conjunto de regras existente de um Firewall do Azure.
Supondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "rg" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente. Sem o Set-AzFirewall, todas as operações executadas no $azFw local não são refletidas no servidor.

### 2: Criar um Firewall do Azure e definir uma coleção de regras de aplicativo mais tarde
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

Neste exemplo, um Firewall é criado primeiro sem nenhum conjunto de regras de aplicativo. Posteriormente, uma Regra de Aplicativo e Um Conjunto de Regras de Aplicativo são criados e, em seguida, o objeto Firewall é modificado na memória, sem afetar a configuração real na nuvem. Para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.

### 3: Atualizar o modo de operação Da Intel de Ameaças do Firewall do Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Este exemplo atualiza o modo de operação de Inteligência contra Ameaças do Firewall do Azure "AzureFirewall" no grupo de recursos "rg".
Sem o Set-AzFirewall, todas as operações executadas no $azFw local não são refletidas no servidor.

### 4: Desloque e aloque o Firewall
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
Este exemplo recupera um Firewall, locado o firewall e o salva. O comando Deallocate remove o serviço em execução, mas preserva a configuração do firewall. Para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.
Se o usuário quiser iniciar o serviço novamente, o método Alocar deverá ser chamado no firewall.
O novo VNet e o IP público devem estar no mesmo grupo de recursos que o Firewall. Novamente, para que as alterações sejam refletidas na nuvem, Set-AzFirewall deve ser chamada.

### 5: Alocar com um endereço IP público de gerenciamento para cenários de túnel forçado
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Este exemplo aloca o firewall com um endereço IP público de gerenciamento e uma sub-rede para cenários de túnel forçados. A VNet deve conter uma sub-rede chamada "AzureFirewallManagementSubnet".

### 6: Adicionar um endereço IP público a um Firewall do Azure
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Neste exemplo, o Endereço IP Público "azFwPublicIp1" conforme anexado ao Firewall.

### 7: Remover um endereço IP público de um Firewall do Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Neste exemplo, o Endereço IP Público "azFwPublicIp1" conforme desconectado do Firewall.

### 8: Alterar o endereço IP público de gerenciamento em um Firewall do Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

Neste exemplo, o endereço IP público de gerenciamento do firewall será alterado para "AzFwMgmtPublicIp2"

### 9: Adicionar configuração DNS a um Firewall do Azure
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

Neste exemplo, a configuração do Proxy DNS e do Servidor DNS está anexada ao Firewall.

### 10: Atualizar o destino de uma regra existente dentro de um conjunto de regras de aplicativo firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Este exemplo atualiza o destino de uma regra existente em um conjunto de regras de um Firewall do Azure. Isso permite que você atualize automaticamente suas regras quando os endereços IP mudarem dinamicamente.

### 11: Permitir FTP Ativo no Firewall do Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

Neste exemplo, FTP Ativo é permitido no Firewall.

## Parâmetros

### -AsJob
Executar cmdlet em segundo plano

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

### -AzureFirewall
O AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## Notas

## LINKS RELACIONADOS

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
