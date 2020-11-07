---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786492"
---
# Add-AzureRmVpnClientRevokedCertificate

## Sinopse
Adiciona um certificado de revogação do cliente VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVpnClientRevokedCertificate** atribui um certificado de revogação de cliente a um gateway de rede virtual.
Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.
Você precisa especificar o nome do certificado e a impressão digital do certificado para usar esse cmdlet.

## EXEMPLOS

### Exemplo 1: adicionar um novo certificado de revogação de cliente a um gateway de rede virtual
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Esse comando adiciona um novo certificado de revogação de cliente ao gateway de rede virtual chamado ContosoVirtualNetwork.
Para adicionar o certificado, você deve especificar o nome do certificado e a impressão digital do certificado.

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

### -Impressão digital
Especifica o identificador exclusivo do certificado que está sendo adicionado.
Por exemplo:

-Impressão digital "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"

Você pode obter informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root` .

O comando anterior obtém informações para todos os certificados do computador local encontrados no repositório de certificados raiz.

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

### -VirtualNetworkGatewayName
Especifica o nome do gateway de rede virtual onde o certificado deve ser adicionado.

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
Especifica o nome do certificado de cliente VPN a ser adicionado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[New-AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


