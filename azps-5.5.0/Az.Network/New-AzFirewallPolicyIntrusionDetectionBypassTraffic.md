---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112837"
---
# New-AzFirewallPolicyIntrusionDetectionBypassTraffic

## Sinopse
Cria uma nova configuração de tráfego de detecção de invasão de firewall do Azure

## Sintaxe

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cria um Objeto de Tráfego de Detecção de Invasão de Política de Firewall do Azure.

## Exemplos

### Exemplo 1: 1. Criar tráfego de bypass com porta e endereço de origem específicos
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

Este exemplo cria a detecção de invasão com a configuração de desvio de tráfego

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Descrição
Ignorar a descrição da configuração.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddress
Lista de intervalos ou endereços IP de destino.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationIpGroup
Lista de IpGroups de destino.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPort
Lista de portas ou intervalos de destino.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Ignorar o nome da configuração.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Ignorar o protocolo de configuração.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Lista de intervalos ou endereços IP de origem.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceIpGroup
Lista de IpGroups de origem.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting

## Notas

## LINKS RELACIONADOS
