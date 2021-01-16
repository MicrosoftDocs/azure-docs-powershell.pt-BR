---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271780"
---
# New-AzApplicationGatewayPrivateLinkIpConfiguration

## Sinopse
Cria uma configuração de IP a ser associada à configuração do PrivateLink

## SYNTAX

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** cria uma configuração de IP para ser associada à configuração do PrivateLink para um gateway do aplicativo do Azure.

## EXEMPLOS

### Exemplo 1: configuração de IP do PrivateLink
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

Esse comando cria uma configuração de IP PrivateLink chamada ' ipConfig01 ' que armazena o resultado na variável chamada $PrivateLinkIpConfiguration. 

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Nome
O nome da IpConfiguration

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

### -Principal
Indicar que a configuração de IP é primária.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
O endereço IP privado da ipConfiguration se desejar uma atribuição estática.

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

### -PrivateIpAddressVersion
A versão de IP da configuração de IP

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Redes

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration

## INFORMA

## LINKS RELACIONADOS

[New-AzApplicationGatewayPrivateLinkConfiguration](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
