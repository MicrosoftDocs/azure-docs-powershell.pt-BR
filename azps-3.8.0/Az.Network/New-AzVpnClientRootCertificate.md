---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943210"
---
# New-AzVpnClientRootCertificate

## Sinopse
Cria um novo certificado raiz de cliente VPN.

## SYNTAX

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzVpnClientRootCertificate** cria um novo certificado raiz de VPN para ser usado em um gateway virtual de rede.
Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.
Esse cmdlet cria um certificado autônomo que não está atribuído a um gateway virtual.
Em vez disso, o certificado criado por **New-AzVpnClientRootCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway ao criar um novo gateway.
Por exemplo, suponha que você crie um novo certificado e o armazene em uma variável chamada $Certificate.
Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.
Por exemplo, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Para obter mais informações, consulte a documentação do cmdlet New-AzVirtualNetworkGateway.

## EXEMPLOS

### Exemplo 1: criar um certificado raiz de cliente
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Este exemplo cria um certificado raiz do cliente e armazena o objeto do certificado em uma variável chamada $Certificate.
Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar um certificado raiz a um novo gateway de rede virtual.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz; esses dados de texto são armazenados em uma variável chamada $Text.
Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha, armazenando o texto extraído em uma variável chamada $CertificateText.
O terceiro comando usa o cmdlet **New-AzVpnClientRootCertificate** para criar o certificado, armazenando o objeto criado em uma variável chamada $Certificate.

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
Especifica um nome para o novo certificado raiz do cliente.

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

### -PublicCertData
Especifica uma representação de texto do certificado raiz a ser adicionado.
Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.
Você deve ver uma saída semelhante a esta (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar o certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----END CERTIFICATE-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.
Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a este: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## INFORMA

## LINKS RELACIONADOS

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


