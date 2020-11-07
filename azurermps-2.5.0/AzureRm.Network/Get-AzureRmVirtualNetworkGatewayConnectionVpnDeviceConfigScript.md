---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786088"
---
# Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## Sinopse
Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais. O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais. O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

O exemplo acima usa Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice para obter as marcas de dispositivo VPN, os modelos e as versões de firmware com suporte.
Em seguida, usa uma das informações de modelos retornados para gerar um script de configuração de dispositivo VPN para o VirtualNetworkGatewayConnection "TestConnection". O dispositivo usado neste exemplo tem o DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.

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

### -DeviceFamily
Nome do modelo/família de dispositivo VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeviceVendor
Nome do fornecedor do dispositivo VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirmwareVersion
Versão do firmware do dispositivo VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
O nome do recurso da conexão para a qual a configuração será gerada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
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
Mostra o que aconteceria se o cmdlet fosse executado.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

