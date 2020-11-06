---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427857"
---
# New-AzureRmVpnClientRevokedCertificate

## Sinopse
Cria um novo cliente VPN-certificado de revogação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmVpnClientRevokedCertificate** cria um novo cliente de rede virtual privada (VPN)-certificado de revogação para uso em um gateway virtual de rede.
Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.

Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.
Em vez disso, o certificado criado por **New-AzureRmVpnClientRevokedCertificate** é usado em conjunto com o cmdlet New-AzureRmVirtualNetworkGateway quando ele cria um novo gateway.
Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.
Em seguida, você pode usar esse objeto de certificado quando criar um novo gateway virtual.
Por exemplo,

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

Para obter mais informações, consulte a documentação do cmdlet New-AzureRmVirtualNetworkGateway.

## EXEMPLOS

### Exemplo 1: criar um novo certificado revogado pelo cliente
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Esse comando cria um novo certificado revogado pelo cliente e armazena o objeto do certificado em uma variável chamada $Certificate.
Essa variável pode ser usada pelo cmdlet **New-AzureRmVirtualNetworkGateway** para adicionar o certificado a um novo gateway de rede virtual.

## OS

### -Nome
Especifica um nome exclusivo para o novo certificado de revogação de cliente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Impressão digital
Especifica o identificador exclusivo do certificado que está sendo adicionado.

Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

O comando anterior retorna informações para todos os certificados do computador local encontrados no repositório de certificados raiz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Esse cmdlet não aceita entrada em pipeline.

## EXIBE

###  
Esse cmdlet cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


