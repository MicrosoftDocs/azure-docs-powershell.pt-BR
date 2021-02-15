---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 54a12f4485e56b592b2e42d7b9515af595d4b6c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111625"
---
# New-AzRouteConfig

## Sinopse
Cria uma rota para uma tabela de rota.

## Sintaxe

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzRouteConfig** cria uma rota para uma tabela de rota do Azure.

## Exemplos

### Exemplo 1: Criar uma rota
```powershell
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

O primeiro comando cria uma rota chamada Roteada07 e, em seguida, armazena-a na variável $Route dados.
Essa rota encaminha pacotes para a rede virtual local.
O segundo comando exibe as propriedades da rota.

### Exemplo 2

Cria uma rota para uma tabela de rota. (gerado automaticamente)

<!-- Aladdin Generated Example -->
```powershell
New-AzRouteConfig -AddressPrefix 10.1.0.0/16 -Name 'Route07' -NextHopIpAddress '12.0.0.5' -NextHopType 'VnetLocal'
```

## Parâmetros

### -AddressPrefix
Especifica o destino, no formato CIDR (Roteamento Interdomínio sem Classe), ao qual a rota se aplica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Nome
Especifica um nome para a rota.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
Especifica o endereço IP de um dispositivo virtual que você adiciona à sua rede Azure virtual.
Essa rota encaminha pacotes para esse endereço.
Especifique esse parâmetro somente se você especificar um valor de VirtualAppliance para o *parâmetro NextType.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextType
Especifica como essa rota encaminha pacotes.
Os valores aceitáveis para este parâmetro são:
- Internet.
O gateway de Internet padrão fornecido pelo Azure. 
- Nenhum.
Se você especificar esse valor, a rota não encaminhará pacotes. 
- VirtualAppliance.
Um dispositivo virtual que você adiciona à sua rede virtual do Azure. 
- VirtualNetworkGateway.
Um gateway de rede virtual privada do Azure servidor para servidor. 
- VnetLocal.
A rede virtual local.
Se você tiver duas sub-redes, 10.1.0.0/16 e 10.2.0.0/16 na mesma rede virtual, selecione um valor de VnetLocal para cada sub-rede para encaminhar para a outra sub-rede.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSRoute

## Notas

## LINKS RELACIONADOS

[Add-AzRouteConfig](./Add-AzRouteConfig.md)

[Get-AzRouteConfig](./Get-AzRouteConfig.md)

[Remove-AzRouteConfig](./Remove-AzRouteConfig.md)

[Set-AzRouteConfig](./Set-AzRouteConfig.md)


