---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261488"
---
# New-AzVpnClientRevokedCertificate

## Sinopse
Cria um novo cliente VPN-certificado de revogação.

## SYNTAX

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzVpnClientRevokedCertificate** cria um novo cliente de rede virtual privada (VPN)-certificado de revogação para uso em um gateway virtual de rede.
Cliente-certificados de revogação impedem que computadores cliente usem o certificado especificado para autenticação.
Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.
Em vez disso, o certificado criado por **New-AzVpnClientRevokedCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway quando ele cria um novo gateway.
Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.
Em seguida, você pode usar esse objeto de certificado quando criar um novo gateway virtual.
Por exemplo, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway.

## EXEMPLOS

### Exemplo 1: criar um novo certificado revogado pelo cliente
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Esse comando cria um novo certificado revogado pelo cliente e armazena o objeto do certificado em uma variável chamada $Certificate.
Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar o certificado a um novo gateway de rede virtual.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Você pode retornar informações de impressão digital para seus certificados usando um comando do Windows PowerShell semelhante a este: `Get-ChildItem -Path Cert:\LocalMachine\Root`
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate

## INFORMA

## LINKS RELACIONADOS

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


