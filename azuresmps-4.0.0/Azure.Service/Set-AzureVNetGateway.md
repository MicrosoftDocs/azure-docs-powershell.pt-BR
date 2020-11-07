---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946414"
---
# Set-AzureVNetGateway

## Sinopse
Habilita ou desabilita um gateway VPN para uma rede virtual do Azure.

## SYNTAX

### Conectar (padrão)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Automática
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureVNetGateway** habilita ou desabilita um gateway de rede virtual privada (VPN) para uma rede virtual do Azure.
Um gateway de rede virtual é um ponto de extremidade VPN para se conectar a uma rede virtual.
Especifique o parâmetro *Connect* ou *Disconnect* para habilitar ou desabilitar a conexão VPN entre um site de rede local e uma rede virtual local.

## EXEMPLOS

### Exemplo 1: habilitar um gateway de rede virtual para uma rede virtual
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Esse comando habilita o gateway de rede virtual entre a rede virtual do Azure nomeada ContosoProdNet e o dispositivo VPN para o site de rede local chamado ContosoBranchOffice.

### Exemplo 2: desabilitar um gateway de rede virtual para uma rede virtual
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

Esse comando desabilita o gateway de rede virtual entre a rede virtual do Azure chamada ContosoProdNet e o dispositivo VPN para o site de rede local chamado ContosoBranchOffice.

## OS

### -Conectar
Indica que esse cmdlet habilita a conexão VPN entre uma rede virtual e um site de rede local.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Desconectar
Indica que esse cmdlet desabilita a conexão VPN entre uma rede virtual e um site de rede local.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Especifica o nome do site de rede local no local para o qual este cmdlet habilita ou desabilita a conexão VPN.

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

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Especifica a rede virtual para a qual esse cmdlet habilita ou desabilita a conexão VPN.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[New-AzureVNetGateway](./New-AzureVNetGateway.md)

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Redimensionar-AzureVNetGateway](./Resize-AzureVNetGateway.md)


