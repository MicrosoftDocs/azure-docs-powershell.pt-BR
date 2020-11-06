---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429412"
---
# Set-AzureRmVirtualNetworkGatewayVpnClientConfig

## Sinopse
Define o pool de endereços do cliente VPN para um gateway de rede virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Padrão (padrão)
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RadiusServerConfiguration
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVirtualNetworkVpnClientConfig** configura o pool de endereços do cliente para um gateway de rede virtual.
Os clientes de rede virtual privada (VPN) que se conectam a esse gateway recebem um endereço IP desse pool de endereços.

## EXEMPLOS

### Exemplo 1: atribuir um pool de endereços de cliente VPN a um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.
O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.

### Exemplo 2: configurar a autenticação baseada em RADIUS externa no gateway existente
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.
O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway. Ele também configura o servidor RADIUS externo "TestRadiusServer" para ser usado para autenticação para clientes VPN.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RadiusServerAddress
P2S endereço do servidor RADIUS externo.

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
P2S segredo do servidor RADIUS externo.

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Especifica uma referência de objeto ao gateway de rede virtual que contém as definições de configuração de cliente VPN que esse cmdlet modifica.
Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnClientAddressPool
Especifica os endereços IP a serem atribuídos a clientes que se conectam a este gateway

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Parâmetros: VirtualNetworkGateway (ByValue)

### System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

### System. Security. SecureString

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Redimensionar-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)


