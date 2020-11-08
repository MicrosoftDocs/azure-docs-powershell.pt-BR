---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125562"
---
# Set-AzFirewall

## Sinopse
Salva um firewall modificado.

## SYNTAX

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzFirewall** atualiza um firewall do Azure.

## EXEMPLOS

### 1: atualizar a prioridade de um conjunto de regras de aplicativo de firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Este exemplo atualiza a prioridade de um conjunto de regras existente de um firewall do Azure.
Pressupondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "RG" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente. Sem o comando Set-AzFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.

### 2: criar um firewall do Azure e definir uma coleção de regras de aplicativo mais tarde
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

Neste exemplo, um firewall é criado primeiro sem nenhuma coleção de regras de aplicativo. Posteriormente, uma regra de aplicativo e uma coleção de regras de aplicativo são criadas, o objeto de firewall é modificado na memória, sem afetar a configuração real na nuvem. Para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.

### 3: atualizar a ameaça do modo de operação da Intel do firewall do Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Este exemplo atualiza o modo de operação de ameaças da Intel do firewall do Azure "AzureFirewall" no grupo de recursos "RG".
Sem o comando Set-AzFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.

### 4: desatribuir e alocar o firewall
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
Este exemplo recupera um firewall, desatribui o firewall e salva-o. O comando DEALLOCATE remove o serviço em execução, mas preserva a configuração do firewall. Para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.
Se o usuário quiser iniciar o serviço novamente, o método de alocação deve ser chamado no firewall.
O novo VNet e o IP público devem estar no mesmo grupo de recursos do firewall. Novamente, para que as alterações sejam refletidas na nuvem, Set-AzFirewall devem ser chamadas.

### 5: atribuir com um endereço IP público de gerenciamento para cenários de encapsulamento forçado
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Este exemplo aloca o firewall com um endereço IP público de gerenciamento e uma sub-rede para cenários de encapsulamento forçado. A VNet deve conter uma sub-rede chamada "AzureFirewallManagementSubnet".

### 6: adicionar um endereço IP público a um firewall do Azure
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Neste exemplo, o endereço IP público "azFwPublicIp1" como anexado ao firewall.

### 7: remover um endereço IP público de um firewall do Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Neste exemplo, o endereço IP público "azFwPublicIp1" como separado do firewall.

### 8: alterar o endereço IP público de gerenciamento em um firewall do Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

Neste exemplo, o endereço IP público de gerenciamento do firewall será alterado para "AzFwMgmtPublicIp2"

### 9: adicionar a configuração de DNS a um firewall do Azure
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

Neste exemplo, o proxy DNS e a configuração do servidor DNS estão conectados ao firewall.

### 10: Atualize o destino de uma regra existente dentro de um conjunto de regras de aplicativo de firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Este exemplo atualiza o destino de uma regra existente dentro de uma coleção de regras de um firewall do Azure. Isso permite que você atualize automaticamente suas regras quando endereços IP são alterados dinamicamente.

### 11: permitir FTP ativo no firewall do Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

Neste exemplo, o FTP ativo é permitido no firewall.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Confirme
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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## INFORMA

## LINKS RELACIONADOS

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
