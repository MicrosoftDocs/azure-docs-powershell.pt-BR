---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3151ffb45064d1cb85b69d11a1ccbd49d4c045e8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775449"
---
# Get-AzVpnClientRevokedCertificate

## Sinopse
Obtém informações sobre o cliente VPN-certificados de revogação.

## SYNTAX

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzVpnClientRevokedCertificate** retorna informações sobre os certificados de revogação de cliente atribuídos a um gateway de rede virtual.
Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.
**Get-AzVpnClientRevokedCertificate** permite retornar informações sobre todos os certificados de revogação de cliente no gateway ou usando o parâmetro *VpnClientRevokedCertificateName* para obter informações sobre um único certificado.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os certificados de revogação de cliente
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

Esse comando obtém informações sobre todos os certificados de revogação de cliente associados ao gateway de rede virtual chamado ContosoVirtualNetworkGateway.

### Exemplo 2: obter informações sobre certificados de revogação do cliente específico
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

###  
**Get-AzVpnClientRevokedCertificate** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[New-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


