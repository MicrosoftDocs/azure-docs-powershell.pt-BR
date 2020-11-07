---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785693"
---
# Get-AzureRmVpnClientRevokedCertificate

## Sinopse
Obtém informações sobre o cliente VPN-certificados de revogação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação de cliente atribuídos a um gateway de rede virtual.
Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.
**Get-AzureRmVpnClientRevokedCertificate** permite retornar informações sobre todos os certificados de revogação de cliente no gateway ou usando o parâmetro *VpnClientRevokedCertificateName* para obter informações sobre um único certificado.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os certificados de revogação de cliente
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

Esse comando obtém informações sobre todos os certificados de revogação de cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.

### Exemplo 2: obter informações sobre certificados de revogação do cliente específico
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

Esse comando é uma variação do comando mostrado no exemplo 1.
Nesse caso, no entanto, o parâmetro *VpnClientRevokedCertificateName* é usado para limitar os dados retornados a um certificado revogado pelo cliente específico: o certificado com o nome ContosoRevokedClientCertificate.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.

Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.

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

### -VirtualNetworkGatewayName
Especifica o nome do gateway de rede virtual onde as informações de certificado revogado são atribuídas.

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

### -VpnClientRevokedCertificateName
Especifica o nome do certificado de cliente VPN que este cmdlet obtém.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

###  
**Get-AzureRmVpnClientRevokedCertificate** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[New-AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


